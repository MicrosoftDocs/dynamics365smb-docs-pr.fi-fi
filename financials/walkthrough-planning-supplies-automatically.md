---
title: "Vaihekuvaus – Toimitusten automaattinen suunnittelu | Microsoft Docs"
description: "Suunnittelutyökirjan ajolla ja tarvolaskennan ajolla viitataan päätuotantoaikataulun (MPS) ja materiaalien tarvelaskentaan (MRP), joka perustuu todelliseen ja ennustettuun kysyntään."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bbe470538bb79e9f6fb6860ee32d75b5d56db9e8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-planning-supplies-automatically"></a>Vaihekuvaus: Toimitusten automaattinen suunnittelu
Suunnittelutyökirjan ajolla ja tarvelaskennan ajolla viitataan päätuotantoaikataulun laskentaan (MPS) ja materiaalien tarvelaskentaan (MRP), joka perustuu todelliseen ja ennustettuun kysyntään.  

-   Tuotanto-ohjelma tarkoittaa todelliseen tarpeeseen ja tuotantoennusteeseen perustuvaa tuotanto-ohjelman laskentaa. Tuotanto-ohjelman laskenta tehdään lopullisille nimikkeille, joilla on ennuste ja/tai myyntitilauksen rivi. Näitä nimikkeitä kutsutaan tuotanto-ohjelmanimikkeiksi, ja ne tunnistetaan dynaamisesti laskennan alkaessa.  
-   MRP tarkoittaa komponenttien todelliseen tarpeeseen ja komponenttitason tuotantoennusteeseen perustuvaa materiaalitarpeen laskentaa. Tarvelaskenta tehdään vain nimikkeille, jotka eivät ole tuotanto-ohjelmanimikkeitä. Tuotanto-ohjelman yleistavoitteena on tuottaa aikavaiheistetut, viralliset nimikekohtaiset suunnitelmat, jotta oikeaa tuotetta voidaan toimittaa oikea määrä oikeaan aikaan ja oikeassa paikassa.  

 Tuotanto-ohjelmassa ja tarvelaskennassa käytetään identtisiä suunnittelualgoritmeja. Suunnittelualgoritmeissa käytetään verkotusta, aiemmin luotuja toimitustilauksia ja toimenpideviestejä. Suunnittelujärjestelmä selvittää, mitä nyt tai vastaisuudessa tarvitaan (kysyntä) sekä mitä on käsivarastossa ja mitä tulossa (tarjonta). Kun nämä määrät yhdistetään, suunnittelutyökirjassa tulee näkyviin toimenpidesanomia. Toimenpidesanomissa ehdotetaan luomaan uusi toimitustilaus, muuttamaan toimitustilausta (määrää tai päivämäärää) tai peruuttamaan aiemmin luotu toimitustilaus. Toimitustilaukset voivat olla tuotantotilauksia, ostotilauksia tai siirtotilauksia. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Toimitusten suunnittelu](design-details-supply-planning.md)  

 Suunnittelun tulos lasketaan osittain kysyntä- ja tuotantojoukoista sekä osittain varastoyksikön korttien tai nimikkeen korttien, tuotannon tuoterakenteen ja reititysten asetusten mukaan.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
 Tässä vaihekuvauksessa esitetään, kuinka tuotannonsuunnitelmajärjestelmää käytetään suunniteltaessa automaattisesti kaikkia osto- ja tuotantotilauksia, joita tarvitaan 15 retkipyörän valmistamiseen eri myyntitilauksisssa. Antaakseen selkeän ja realistisen vaihekuvauksen, suunnittelurivien määrä on erotettu suodattamalla pois kaikki muut kysyntä- ja tuotantojoukot CRONUS Finland Oy -esittely-yrityksessä lukuun ottamatta myynnin kysyntää sijainnissa SININEN.  

 Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

-   myyntitilauksen luominen ja kysyntäsuunnitelman laskeminen  
-   suunnittelurivien suunnitteluparametrien ja tilausten jäljitysmerkintöjen tarkasteleminen  
-   ehdotettujen toimitustilausten luominen automaattisesti  
-   myynnin kysynnän luominen ja uudelleensuunnittelu.  

## <a name="roles"></a>Roolit  

-   Tuotantosuunnittelija  
-   Ostaja  

## <a name="prerequisites"></a>Vaatimukset  
 Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

-   CRONUS Finland Oy -esittely-yritys.  
-   Muuta useita nimikkeen asetusarvoja noudattamalla osan Esimerkkitietojen valmisteleminen ohjeita jäljempänä tässä vaihekuvauksessa.  

## <a name="story"></a>Taustatietoja  
 Asiakas Tuotantoyhtymä tilaa viisi retkipyörää ja pyytää toimituspäiväksi 2.5.2014 (5. helmikuuta).  

 Tuotantosuunnittelija Karl suorittaa tuotantosuunnittelun helmikuun 2014 ensimmäiselle viikolle. Hän suodattaa oman sijaintinsa (SININEN) tiedot ja määrittää suunnitteluväliksi työpäivät 23.1.– 7.2.2014, ennen kuin hän laskee alustavan tuotantosuunnitelman.  

 Tuotantoyhtymän myyntitilaus on ainoa kyseisen viikon kysyntä. Karl havaitsee, ettei suunnitteluriveillä ole varoituksia, joten hän luo ilman muutoksia toimitustilaukset ehdotetuista suunnitteluriveistä.  

 Seuraavana päivänä ennen alkuperäisten toimitustilausten aloittamista tai kirjaamista Karl huomaa, että toinen asiakas on tilannut kymmenen retkipyörää ja pyytänyt lähetyspäiväksi 12.2.2014. Karl laskee tiedot uudelleen ja oikaisee näin tuotantosuunnitelman kysynnän muutoksen mukaan. Uudelleenlaskenta tuottaa nettomuutossuunnitelman, jossa ehdotetaan muutoksia ensimmäisen ajon toimitustilausten aikaan ja määrään.  

 Eri suunnitteluvaiheiden aikana Karl etsii suunnitteluun liittyvät tilaukset ja tarkistaa Tilauksen seuranta -toiminnolla, mikä toimitus kattaa minkäkin kysynnän.  

## <a name="preparing-sample-data"></a>Esimerkkitietojen valmisteleminen  
 Luo varastointiyksiköt retkipyörälle ja sen komponenteille. Niiden nimikenumerot ovat 1001–1300. (Tietyt osat jätetään pois yksinkertaisuuden vuoksi.) Oikaise sitten kaikkien komponenttien suunnitteluparametreja niin, että suunnittelun tulokset ovat selkeämpiä.  

### <a name="to-create-stockkeeping-units"></a>Varastointiyksikän luominen  

1.  Avaa nimikkeen 1001 (Retkipyörä) kortti.  
2.  Valitse **Luo varastointiyksikkö** -toiminto.  
3.  Älä muuta **Luo varastointiyksikkö** -ikkunan asetuksia tai suodattimia vaan valitse **OK**.  
4.  Toista vaiheet 1-3 nimikkeille numerovälillä 1100-1300.  

### <a name="to-change-selected-planning-parameters"></a>Vaihda valitut suunnitteluparametrit  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Varastointiyksiköt** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa nimikkeen 1100 (Etupyörä) SININEN varastointiyksikön kortti.  
3.  Täytä **Suunnittelu**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Uusintatilaustapa|Varmuusvaraston määrä|Erän koontijakso|Uudelleenajoitusjakso|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Erä-erästä|Tyhjä|2VI|2VI|  

4.  Toista vaiheet 2-3 kaikille nimikkeille 1100-1300.  

 Esimerkkitiedot on nyt valmisteltu tätä vaihekuvausta varten.  

## <a name="creating-a-regenerative-supply-plan"></a>Toimituksen uudelleensuunnittelun luominen  
 Kun Riku saa uuden myyntitilauksen viidestä retkipyörästä, hän aloittaa suunnitteluprosessin määrittämällä asetukset, suodattimet ja suunnittelun aikavälin jättääksen pois kaiken muun paitsi helmikuun viikon kysynnän SININEN-sijainnissa. Karl aloittaa laskemalla päätuotantoaikataulun (MPS) suodattimien sisällä, minkä jälkeen hän laskee täydellisen toimitussuunnitelman alatason kysynnälle (MRP) suodattimien sisällä.  

### <a name="to-create-the-sales-order"></a>Myyntitilauksen luominen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Täytä **Myyntitilaus**-ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Tilausasiakkaan nimi|Lähetyksen pvm|Nimikkeen nro|Sijainti|määrä.|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Cannon Group|5.2.2014|1001|SININEN|5|  

4.  Hyväksy saatavuusvaroitus ja valitse **Kyllä**. Uusi kysyntämäärä kirjataan.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-blue"></a>Uudelleensuunnittelun luominen SININEN-sijainnin kysynnän täyttämiseksi  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Suunnittelutyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Laske uudelleensuunnittelu** -toiminto.  
3.  Täytä **Laske suunn. - Suunn.työk.** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Laske suunnitelma|Aloituspvm|Lopetuspvm|Näytä tulokset:|Rajoita kokonaisarvoksi|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Kyllä<br /><br /> **MRP** = Ei|23.1.2014<br /><br /> (Käsittelypäivämäärä)|7.2.2014|1001..1300|Sijaintisuodatus = SININEN|  

4.  Käynnistä suunnitteluajo valitsemalla **OK**.  

     Järjestelmä luo yhden suunnittelurivin, jolla ehdotetaan, suunnitellulla tuotantotilauksella tuotetaan 10 retkipyörää, nimike 1001 5.2.2014 mennessä. Tämä on myyntitilauksen toimituspäivä.  

     Varmista seuraavaksi, että tämä suunnittelurivi vastaa Tuotantoyhtymän myyntitilausta. Tämä onnistuu **Tilauksen seuranta** -toiminnolla, joka linkittää kysynnän dynaamisesti suunniteltuun toimitukseen.  

5.  Valitse ensin uusi suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  
6.  Valitse **Tilauksen seuranta** -ikkunassa **Näytä**-toiminto.  

     Näyttöön tulee viiden retkipyörän myyntitilaus asiakasnumerolle 10000 5.2.2013 esitetyn mukaisesti.  

7.  Sulje **Myyntitilaus**- ja **Tilauksen seuranta** -ikkunat.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a>Laske tarvelaskenta sisällyttäen pohjana olevat osat  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Suunnittelutyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Laske uudelleensuunnittelu** -toiminto.  
3.  Täytä **Laske suunn. - Suunn.työk.** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Laske|Aloituspvm|Lopetuspvm|Näytä tulokset:|Rajoita kokonaisarvoiksi:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Kyllä<br /><br /> **MRP** = Kyllä|23.1.2014|7.2.2014|1001..1300|Sijaintisuodatus = SININEN|  

4.  Käynnistä suunnitteluajo valitsemalla **OK**.  

     Järjestelmä luo 14 suunnitteluriviä. Niillä ehdotetaan toimitustilauksia kysynnälle, jonka SININEN-sijainnin retkipyörien myyntitilaus edustaa.  

## <a name="analyzing-the-planning-result"></a>Suunnittelun tulosten analysoiminen  
 Karl analysoi ehdotetut määrät. Hän siirtyy valituille suunnitteluriveille ja tarkistaa nimikkeen suunnitteluparametrit sekä tilauksen seurannan merkinnät.  

 Huomaa **Suunnittelutyökirja** -ikkunan **Eräpäivä**-sarakkeessa, että ehdotetut toimitustilaukset ajoitetaan taaksepäin myyntitilauksen eräpäivästä 5.2.2014. Aikajana alkaa tuotantotilauksen ylimmästä suunnittelurivistä, joka liittyy viimeisteltyjen retkipyörien tuotantoon. Aikajana päättyy alimmaiseen suunnitteluriviin yhteen alimman tason nimikkeeseen, 1255, Takaistukka, eräpäivä 3.3.2014, liittyvän ostotilauksen kohdalla. Kuten nimikkeen 1251 suunnittelurivi, takarenkaan akseli, tämä rivi edustaa ostotilauksen osia, jotka erääntyvät tuotetun päänimikkeen aloituspäivämääränä, osakokoonpanonimike 1250, joka puolestaan erääntyy 3.2.2014. Voit nähdä koko laskentataulukossa, että kaikki taustalla olevat nimikkeet erääntyvät päätietueidensa aloituspäivänä.  

 Nimikkeen 1300, Ketjun kokoonpano, ehdotetaan kymmentä kappaletta. Tämä poikkeaa viidestä kappaleesta, joita odotamme myyntitilauksen täyttämiseksi. Siirry tarkastelemaan tilauksen seurantatapahtumia.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a>Tarkastele kohteen 1300 tilauksen merkintää  

1.  Valitse ensin nimikkeen 1300 suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  

     **Tilauksen seuranta** -ikkunan kahdella rivillä näkyy, että viittä kappaletta seurataan suunnitteluriviltä (ensimmäinen tilauksen seurannan rivi) myyntitilaukseen 1001 (toinen tilauksen seurannan rivi). Suunnittelurivillä ehdotetut viisi kappaletta eivät liity asiakirjariveihin, vaan ne on määritetty suunnitteluparametrin, ennusteen tai puitetilauksen perusteella. Tällaisten ei-seurattujen määrien summa on **Tilauksen seuranta** -ikkunan **Ei seurattu määrä** -kentässä.  

2.  Valitse **Ei seurattu määrä** -kenttä.  

     **Ei-seurattu suunnitteluelementti** -ikkunassa näkyy, että nimike 1300 käyttää suunnitteluparametria Vähimmäistilausmäärä, jonka arvo on 10,00. Siksi suunnittelurivin kokonaismäärä on kymmenen kappaletta, mutta vain viittä voidaan seurata kysyntään. Toiset viisi kappaletta ovat ei-seurattu määrä, jolla täytetään suunnitteluparametrin edellytykset. Siirry suunnittelun parametrien tarkasteluun.  

### <a name="to-check-the-planning-parameter"></a>Tarkista suunnitteluparametri  

1.  Valitse **Ei-seuratut suunnitteluelementit** -ikkunassa nimikkeen 1300 tilauksen seurantarivi.  
2.  Valitse ensin **Nimikenro**-kenttä ja sitten **Lisäasetukset**-toiminto.  
3.  Valitse **Nimikeluettelo**-ikkunassa **Varastointiyksiköt**-toiminto.  
4.  Avaa **Varastointiyksikön luettelo** -ikkunassa SININEN varastointiyksikön kortti.  
5.  Huomaa, että **Suunnittelu**-pikavälilehden **Vähimmäistilausmäärä**-kentässä on arvo 10.  
6.  Sulje kaikki ikkunat **Suunnittelutyökirja**-ikkunaa lukuun ottamatta.  

### <a name="to-view-more-order-tracking-entries"></a>Tarkastele lisää tilauksen seurantatapahtumia  

1.  Valitse ensin nimikkeen 1110 (Vanne) suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  

     **Tilauksen seuranta** -ikkunassa näkyy, että viisi vannetta tarvitaan kutakin tuotantotilausta varten eteen ja taakse.  

     Sama tilauksen seuranta koskee nimikkeiden 1120, 1160 ja 1170 suunnittelurivejä. Nimikkeen 1120 kunkin renkaan tuotannon tuotantorakenteen **Määrä per** -kentän arvo on 50 kappaletta, joten kokonaistarve on 100.  

     Suunnitelurivi nimikkeen 1150 kuudelle kappaleelle näyttää epäsäännölliseltä. Siirry analysoimaan.  

2.  Valitse ensin nimikkeen 1150 suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  

     **Tilauksen seuranta** -ikkunassa näkyy, että viisi yksikköä on jäljitetty etupyörään ja yksi yksikkö on seurannan ulkopuolella. Siirry tarkastelemaan ei-seurattua määrää.  

3.  Valitse **Ei seurattu määrä** -kenttä.  

     **Ei-seuratut suunnitteluelementit** -ikkunassa näkyy, että nimike 1150 käyttää suunnitteluparametria Tilauskerrannainen, jonka arvo on 2,00. Tämä määrittää, että nimikettä on tilattava määrä, joka on jaollinen luvulla 2. Viittä lähinnä oleva kahdella jaollinen luku on kuusi.  

     Saman tilauksen seuranta koskee etukeskiön komponentteja 1151 ja 1155. Jokainen tarve lasketaan kuitenkin kertomalla hävikkiprosentti, joka on määritetty nimikkeelle 1150 nimikkeen kortin **Hukkaprosentti** -kentässä.  

 Nyt alkuperäisen tuotantosuunnitelman analyysi on valmis. Huomaa, että **Hyväksy toimenpideviesti** -valintaruutu on valittuna kaikilla suunnitteluriveillä, mikä ilmaisee, että ne voidaan muuntaa toimitustilauksiksi.  

## <a name="carrying-out-action-messages"></a>Toimenpideviestien toteuttaminen  
 Seuraavaksi Karl muuntaa ehdotetut suunnittelurivit toimitustilauksiksi **Toteuta toim.pideviesti** -toiminnolla.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a>Ehdotettujen toimitustilausten luominen automaattisesti  

1.  Valitse **Hyväksy toimenpideviesti** -valintaruutu kaikille suunnitteluriveille, joilla on Poikkeus-tyyppinen varoitus.  
2.  Valitse **Toteuta toimenpideviesti** -toiminto.  
3.  Täytä **Toteuta toim.pideviesti - Suun.** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Tuotantotilaus|Ostotilaus|Siirtotilaus|  
    |----------------------|--------------------|--------------------|  
    |Sitovasti suunniteltu|Tee ostotilaukset|Tee siirtotilaukset|  

4.  Luo kaikki ehdotetut toimitustilaukset automaattisesti valitsemalla **OK**.  
5.  Sulje tyhjä **Suunnittelutyökirja**-ikkuna.  

 Toimitussuunnitelman alkuperäinen laskenta, analyysi ja luonti SININEN-sijainnin kysynnälle helmikuun ensimmäisellä viikolla on nyt valmis. Seuraavassa osassa toinen asiakas tilaa kymmenen retkipyörää, ja Karlin on laskettava suunnitelma uudelleen.  

## <a name="creating-a-net-change-plan"></a>Nettomuutossuunnitelman luominen  
 Seuraavana päivänä ennen toimitustilausten aloittamista tai kirjaamista saapuu uusi myyntitilaus yritykseltä Libros S.A. Tilaus käsittää kymmenen retkipyörää, ja tilauksen toimituspäivä on 12.2.2014. Karl saa ilmoituksen uudesta kysynnästä, joten hän laskee suunnitelman uudelleen. Karl laskee Nettomuutos suunnittelu -toiminnolla ainoastaan edellisen suunnitteluajon jälkeen tulleet kysynnän tai toimituksen muutokset. Lisäksi hän laajentaa suunnittelujakson 14.2.2014 asti kattamaan toisen kysyntäpäivän 14.2.2014.  

 Suunnittelujärjestelmä laskee parhaan tavan kattaa kahden identtisen tuotteen kysynnän. Järjestelmä määrittää, miten osa osto- ja tuotantotilauksista kannattaa yhdistää ja miten muut tilaukset lasketaan uudelleen. Järjestelmä luo myös tarvittaessa uusia tilauksia.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>Myynnin kysynnän luominen ja uudelleensuunnittelu  

1.  Valitse **Uusi**-toiminto.  
2.  Täytä **Myyntitilaus**-ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Tilausasiakkaan nimi|Lähetyksen pvm|Nimikkeen nro|Sijainti|määrä.|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.A|12.2.2014|1001|SININEN|10|  

3.  Hyväksy saatavuusvaroitus ja valitse **Kyllä**. Uusi kysyntämäärä kirjataan.  
4.  Seuraavaksi on tarpeen oikaista nykyinen toimitussuunnitelma.  
5.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Suunnittelutyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
6.  Valitse **Laske nettomuutossuunnitelma** -toiminto.  
7.  Täytä **Laske suunn. - Suunn.työk.** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Laske suunnitelma|Aloituspvm|Lopetuspvm|Näytä tulokset:|Rajoita kokonaisarvoksi|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Kyllä<br /><br /> **MRP** = Kyllä|23.1.2014|14.2.2014|1001..1300|Sijaintisuodatus = SININEN|  

8.  Käynnistä suunnitteluajo valitsemalla **OK**.  

 Yhteensä 14 suunnittelutyökirjan riviä on luotu. Huomaa, että ensimmäisen suunnittelurivin **Toimenpideviesti**-kentässä lukee **Uusi**, **Määrä**-kentässä 10 ja **Eräpäivä**-kentässä 12.2.2014. Tämä uusi rivi luodaan yläpäänimikkeelle 1001, Retkipyörä, koska nimikkeen uusintatilaustapa on **Tilaus**. Tämä tarkoittaa, että se on toimitettava yhden suhde yhteen -suhteessa kysyntään, joka on kymmenen kappaleen myyntitilaus.  

 Seuraavat kaksi suunnitteluriviä ovat retkipyörien kiekkojen tuotantotilaukset. Jokaista viittä **Alkuperäinen määrä** -kentässä olemassa olevaa tilausta kasvatetaan arvoon 15 **Määrä**-kentässä. Molemmissa tuotantotilauksissa on muuttumaton eräpäivä, mistä on osoituksena **Toimenpideviesti**-kentässä näkyvä **Muuta määrä**. Tämä koskee myös nimikkeen 1300 suunnittelurivillä, joskin sen tilauskerrannainen 10,00 pyöristää seuratun kysynnän 15 kappaleesta 20 kappaleeseen.  

 Kaikilla muilla suunnitteluriveillä on toimenpideviestit **Aikataul. uud. ja Muuta määrä**. Tämä tarkoittaa, että määrän muutoksen vuoksi eräpäiviä on siirretty ensimmäisen toimitussuunnitelman mukaisesti ( -kenttä), jotta lisämäärä voidaan sisällyttää käytettävissä olevaan tuotantoaikaan (kapasiteetti). Ostetut komponentit ajoitetaan ja lisätään tuotantotilausten lisäämiseksi. Siirry uuden suunnitelman analysointiin.  

## <a name="analyzing-the-changed-planning-result"></a>Muutetun suunnittelun tulosten analysoiminen  
 Koska kaikilla erä-erästä-suunnitelluilla suodattimessa olevilla nimikkeillä 1100-1300 on kahden viikon uudelleenajoitusjakso, niiden nykyiset toimitustilaukset muokataan vastaamaan uutta kysyntää, joka tapahtuu määritetyn kahden viikon kuluessa.  

 Useat suunnittelurivit kerrotaan yksinkertaisesti kolmella, jotta saadaan 15 retkipyörää 5 sijasta. Eräpäivät siirretään taaksepäin ajassa, jotta lisätyt määrät voidaan tuottaa Cannon Groupin myyntitilauksen toimituspäivän perusteella. Näillä suunnitteluriveillä voidaan seurata kaikkia määriä. Jäljellä olevia suunnittelurivejä korotetaan kymmenellä kappaleella niiden eräpäivien siirtämisen lisäksi. Näille suunnitteluriveille osa määristä on seurannan ulkopuolella eri suunnitteluparametrien vuoksi. Siirry tarkastelemaan joitakin näistä seurantatapahtumista.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a>Tarkastele kohteen 1250 tilauksen merkintää  

1.  Valitse ensin nimikkeen 1250 suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  

     Seitsemän **Tilauksen seuranta** -ikkunan riviä näyttää, että viittä ja kymmentä kappaletta seurataan takarenkaan kautta retkipyöriin vastaavasti kahdessa myyntitilauksessa.  

     Viimeiset viisi kappaletta ovat seurannan ulkopuolella. Siirry analysoimaan.  

2.  Valitse **Ei seurattu määrä** -kenttä.  

     **Ei-seurattu suunnitteluelementti** -ikkunassa näkyy, että nimike 1250 käyttää suunnitteluparametria Tilauskerrannainen, jonka arvo on 10,00. Tämän vuoksi suunnittelurivin arvo on yhteensä 20 kappaletta; todellinen tarve on siis pyöristetty ylöspäin lähimpään 10:llä jaolliseen lukuun. Toiset viisi kappaletta ovat ei-seurattu määrä, jolla täytetään suunnitteluparametrin edellytykset.  

3.  Sulje kaikki ikkunat **Suunnittelutyökirja**-ikkunaa lukuun ottamatta.  

### <a name="to-view-an-existing-order"></a>Olemassa olevan tilauksen tarkasteleminen  

1.  Valitse nimikkeen 1250 suunnittelurivin **Viitatun tilauksen numero** -kentässä.  
2.  Takakeskiön **Sitovasti suun. tuotantotil.**-ikkuna. Olemassa oleva kymmenen kappaleen tilaus, johon olet luonut ensimmäisen suunnitteluajon, avautuu.  
3.  Sitovasti suunnitellut tuotantotilaukset  

 Olet nyt käynyt läpi vaihekuvauksen, jossa havainnollistettiin, miten suunnittelujärjestelmässä havaitaan kysyntä automaattisesti, lasketaan toimitustilaukset kysynnän ja suunnitteluparametrien mukaan ja luodaan automaattisesti erilaisia toimitustilauksia sopivia päivämääriä ja määriä käyttäen.  

## <a name="see-also"></a>Katso myös  
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)   
 [Vaihekuvaus: Toimitusten manuaalinen suunnittelu](walkthrough-planning-supplies-manually.md)   
 [Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)

