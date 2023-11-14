---
title: Vaihekuvaus – Toimitusten automaattinen suunnittelu
description: 'Tässä vaihekuvauksessa esitetään, kuinka tuotannonsuunnitelmajärjestelmää käytetään suunniteltaessa automaattisesti osto- ja tuotantotilauksia, joita tarvitaan eri myyntitilauksisssa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# Vaihekuvaus: Toimitusten automaattinen suunnittelu

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Suunnittelutyökirjan ajolla ja tarvelaskennan ajolla viitataan päätuotantoaikataulun (MPS) ja materiaalien tarvelaskentaan (MRP), joka perustuu todelliseen ja ennustettuun kysyntään.  

-   Tuotanto-ohjelma tarkoittaa todelliseen tarpeeseen ja kysyntäennusteeseen perustuvaa tuotanto-ohjelman laskentaa. Tuotanto-ohjelman laskenta tehdään lopullisille nimikkeille, joilla on ennuste ja/tai myyntitilauksen rivi. Näitä nimikkeitä kutsutaan tuotanto-ohjelmanimikkeiksi, ja ne tunnistetaan dynaamisesti laskennan alkaessa.  
-   MRP tarkoittaa komponenttien todelliseen tarpeeseen ja komponenttitason kysyntäennusteeseen perustuvaa materiaalitarpeen laskentaa. Tarvelaskenta tehdään vain nimikkeille, jotka eivät ole tuotanto-ohjelmanimikkeitä. Tuotanto-ohjelman yleistavoitteena on tuottaa aikavaiheistetut, viralliset nimikekohtaiset suunnitelmat, jotta oikeaa tuotetta voidaan toimittaa oikea määrä oikeaan aikaan ja oikeassa paikassa.  

 Tuotanto-ohjelmassa ja tarvelaskennassa käytetään identtisiä suunnittelualgoritmeja. Suunnittelualgoritmeissa käytetään verkotusta, aiemmin luotuja toimitustilauksia ja toimenpideviestejä. Suunnittelujärjestelmä selvittää, mitä nyt tai vastaisuudessa tarvitaan (kysyntä) sekä mitä on käsivarastossa ja mitä tulossa (tarjonta). Kun nämä määrät yhdistetään, suunnittelutyökirjassa tulee näkyviin toimenpidesanomia. Toimenpidesanomissa ehdotetaan luomaan uusi toimitustilaus, muuttamaan toimitustilausta (määrää tai päivämäärää) tai peruuttamaan aiemmin luotu toimitustilaus. Toimitustilaukset voivat olla tuotantotilauksia, ostotilauksia tai siirtotilauksia. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Toimitusten suunnittelu](design-details-supply-planning.md)  

 Suunnittelun tulos lasketaan osittain kysyntä- ja tuotantojoukoista sekä osittain varastoyksikön korttien tai nimikkeen korttien, tuotannon tuoterakenteen ja reititysten asetusten mukaan.  

## Tietoja tästä vaihekuvauksesta  
 Tässä vaihekuvauksessa esitetään, kuinka tuotannonsuunnitelmajärjestelmää käytetään suunniteltaessa automaattisesti kaikkia osto- ja tuotantotilauksia, joita tarvitaan 15 retkipyörän valmistamiseen eri myyntitilauksisssa. Antaakseen selkeän ja realistisen vaihekuvauksen, suunnittelurivien määrä on erotettu suodattamalla pois kaikki muut kysyntä- ja tuotantojoukot CRONUS-esittely-yrityksessä lukuun ottamatta myynnin kysyntää sijainnissa ITÄ.  

 Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

-   myyntitilauksen luominen ja kysyntäsuunnitelman laskeminen  
-   suunnittelurivien suunnitteluparametrien ja tilausten jäljitysmerkintöjen tarkasteleminen  
-   ehdotettujen toimitustilausten luominen automaattisesti  
-   myynnin kysynnän luominen ja uudelleensuunnittelu.  

## Roolit  

-   Tuotantosuunnittelija  
-   Ostaja  

## Vaatimukset  
 Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

-   CRONUS Finland Oy -esittely-yritys.  
-   Muuta useita nimikkeen asetusarvoja noudattamalla osan Esimerkkitietojen valmisteleminen ohjeita jäljempänä tässä vaihekuvauksessa.  

## Taustatietoja  
 Asiakas Cannon Group PLC tilaa viisi retkipyörää ja pyytää toimituspäiväksi 5.2.2021 (5. helmikuuta).  

 Tuotantosuunnittelija Karl suorittaa tuotantosuunnittelun helmikuun 2021 ensimmäiselle viikolle. Hän suodattaa oman sijaintinsa (ITÄ) tiedot ja määrittää suunnitteluväliksi työpäivät 23.1.– 7.2.2021, ennen kuin hän laskee alustavan tuotantosuunnitelman.  

 Tuotantoyhtymän myyntitilaus on ainoa kyseisen viikon kysyntä. Karl havaitsee, ettei suunnitteluriveillä ole varoituksia, joten hän luo ilman muutoksia toimitustilaukset ehdotetuista suunnitteluriveistä.  

 Seuraavana päivänä ennen alkuperäisten toimitustilausten aloittamista tai kirjaamista Karl huomaa, että toinen asiakas on tilannut kymmenen retkipyörää ja pyytänyt lähetyspäiväksi 12.2.2021. Karl laskee tiedot uudelleen ja oikaisee näin tuotantosuunnitelman kysynnän muutoksen mukaan. Uudelleenlaskenta tuottaa nettomuutossuunnitelman, jossa ehdotetaan muutoksia ensimmäisen ajon toimitustilausten aikaan ja määrään.  

 Eri suunnitteluvaiheiden aikana Karl etsii suunnitteluun liittyvät tilaukset ja tarkistaa Tilauksen seuranta -toiminnolla, mikä toimitus kattaa minkäkin kysynnän.  

## Esimerkkitietojen valmisteleminen  
 Luo varastointiyksiköt retkipyörälle ja sen komponenteille. Niiden nimikenumerot ovat 1001–1300. (Tietyt osat jätetään pois yksinkertaisuuden vuoksi.) Oikaise sitten kaikkien komponenttien suunnitteluparametreja niin, että suunnittelun tulokset ovat selkeämpiä.  

### Varastointiyksikän luominen  

1.  Avaa nimikkeen 1001 (Retkipyörä) kortti.  
2.  Valitse **Luo varastointiyksikkö** -toiminto.  
3.  Älä muuta **Luo varastointiyksikkö** -sivun asetuksia tai suodattimia vaan valitse **OK**.  
4.  Toista vaiheet 1-3 nimikkeille numerovälillä 1100-1300.  

### Vaihda valitut suunnitteluparametrit  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastointiyksiköt** ja valitse sitten vastaava linkki.  
2.  Avaa ITÄ-varastointiyksikön kortti nimikkeelle 1100 (Etupyörä).  
3.  Täytä **Suunnittelu**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Uusintatilaustapa|Varmuusvaraston määrä|Erän koontijakso|Uudelleenajoitusjakso|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Erä-erästä|Tyhjä|2VI|2VI|  

4.  Toista vaiheet 2-3 kaikille nimikkeille 1100-1300.  

 Esimerkkitiedot on nyt valmisteltu tätä vaihekuvausta varten.  

## Toimituksen uudelleensuunnittelun luominen  
 Kun Riku saa uuden myyntitilauksen viidestä retkipyörästä, hän aloittaa suunnitteluprosessin määrittämällä asetukset, suodattimet ja suunnittelun aikavälin jättääksen pois kaiken muun paitsi helmikuun viikon kysynnän ITÄ-sijainnissa. Riku aloittaa laskemalla päätuotantoaikataulun (MPS) suodattimien sisällä, minkä jälkeen hän laskee täydellisen toimitussuunnitelman alatason kysynnälle (MRP) suodattimien sisällä.  

### Myyntitilauksen luominen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Täytä **Myyntitilaus**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Tilausasiakkaan nimi|Lähetyksen pvm|Nimikkeen nro|Sijainti|määrä|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Cannon Group|5.2.2014|1001|ITÄ|5|  

4.  Hyväksy saatavuusvaroitus ja valitse **Kyllä**. Uusi kysyntämäärä kirjataan.  

### Uudelleensuunnittelun luominen ITÄ-sijainnin kysynnän täyttämiseksi  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suunnittelutyökirja** ja valitse sitten vastaava linkki.  
2.  Valitse **Laske uudelleensuunnittelu** -toiminto.  
3.  Täytä **Laske suunn. - Suunn.työk.** -sivulla kenttä seuraavassa taulukossa kuvatulla tavalla.  

    |Laske suunnitelma|Aloituspvm|Lopetuspvm|Näytä tulokset:|Rajoita kokonaisarvoksi|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Kyllä<br /><br /> **MRP** = Ei|01-23-2021<br /><br /> (Käsittelypäivämäärä)|02-07-2021|1001..1300|Sijaintisuodatus = ITÄ|  

4.  Käynnistä suunnitteluajo valitsemalla **OK**.  

     Järjestelmä luo yhden suunnittelurivin, jolla ehdotetaan, suunnitellulla tuotantotilauksella tuotetaan 10 retkipyörää, nimike 1001 5.2.2021 mennessä. Tämä on myyntitilauksen toimituspäivä.  

     Varmista seuraavaksi, että tämä suunnittelurivi vastaa Tuotantoyhtymän myyntitilausta. Tämä onnistuu **Tilauksen seuranta** -toiminnolla, joka linkittää kysynnän dynaamisesti suunniteltuun toimitukseen.  

5.  Valitse ensin uusi suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  
6.  Valitse **Tilauksen seuranta** -sivulla **Näytä**-toiminto.  

     Näyttöön tulee viiden retkipyörän myyntitilaus asiakasnumerolle 10000 5.2.2021 esitetyn mukaisesti.  

7.  Sulje **Myyntitilaus**- ja **Tilauksen seuranta** -sivut.  

### Laske tarvelaskenta sisällyttäen pohjana olevat osat  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suunnittelutyökirja** ja valitse sitten vastaava linkki.  
2.  Valitse **Laske uudelleensuunnittelu** -toiminto.  
3.  Täytä **Laske suunn. - Suunn.työk.** -sivulla kenttä seuraavassa taulukossa kuvatulla tavalla.  

    |Laske|Aloituspvm|Lopetuspvm|Näytä tulokset:|Rajoita kokonaisarvoiksi:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Kyllä<br /><br /> **MRP** = Kyllä|01-23-2021|02-07-2021|1001..1300|Sijaintisuodatus = ITÄ|  

4.  Käynnistä suunnitteluajo valitsemalla **OK**.  

     Järjestelmä luo 14 suunnitteluriviä. Niillä ehdotetaan toimitustilauksia kysynnälle, jonka ITÄ-sijainnin retkipyörien myyntitilaus edustaa.  

## Suunnittelun tulosten analysoiminen  
 Karl analysoi ehdotetut määrät. Hän siirtyy valituille suunnitteluriveille ja tarkistaa nimikkeen suunnitteluparametrit sekä tilauksen seurannan merkinnät.  

 Huomaa **Suunnittelutyökirja** -sivun **Eräpäivä**-sarakkeessa, että ehdotetut toimitustilaukset ajoitetaan taaksepäin myyntitilauksen eräpäivästä 5.2.2021. Aikajana alkaa tuotantotilauksen ylimmästä suunnittelurivistä, joka liittyy viimeisteltyjen retkipyörien tuotantoon. Aikajana päättyy alimmaiseen suunnitteluriviin yhteen alimman tason nimikkeeseen, 1255, Takaistukka, eräpäivä 30.1.2021, liittyvän ostotilauksen kohdalla. Kuten nimikkeen 1251 suunnittelurivi, takarenkaan akseli, tämä rivi edustaa ostotilauksen osia, jotka erääntyvät tuotetun päänimikkeen aloituspäivämääränä, osakokoonpanonimike 1250, joka puolestaan erääntyy 3.2.2014. Voit nähdä koko laskentataulukossa, että kaikki taustalla olevat nimikkeet erääntyvät päätietueidensa aloituspäivänä.  

 Nimikkeen 1300, Ketjun kokoonpano, ehdotetaan kymmentä kappaletta. Tämä poikkeaa viidestä kappaleesta, joita odotamme myyntitilauksen täyttämiseksi. Siirry tarkastelemaan tilauksen seurantatapahtumia.  

### Tarkastele kohteen 1300 tilauksen merkintää  

1.  Valitse ensin nimikkeen 1300 suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  

     **Tilauksen seuranta** -sivun kahdella rivillä näkyy, että viittä kappaletta seurataan suunnitteluriviltä (ensimmäinen tilauksen seurannan rivi) myyntitilaukseen 1001 (toinen tilauksen seurannan rivi). Suunnittelurivillä ehdotetut viisi kappaletta eivät liity asiakirjariveihin, vaan ne on määritetty suunnitteluparametrin, ennusteen tai puitetilauksen perusteella. Tällaisten ei-seurattujen määrien summa on **Tilauksen seuranta** -sivun **Ei seurattu määrä** -kentässä.  

2.  Valitse **Ei seurattu määrä** -kenttä.  

     **Ei-seurattu suunnitteluelementti** -sivulla näkyy, että nimike 1300 käyttää suunnitteluparametria Vähimmäistilausmäärä, jonka arvo on 10,00. Siksi suunnittelurivin kokonaismäärä on kymmenen kappaletta, mutta vain viittä voidaan seurata kysyntään. Toiset viisi kappaletta ovat ei-seurattu määrä, jolla täytetään suunnitteluparametrin edellytykset. Siirry suunnittelun parametrien tarkasteluun.  

### Tarkista suunnitteluparametri  

1.  Valitse **Ei-seuratut suunnitteluelementit** -sivulla nimikkeen 1300 tilauksen seurantarivi.  
2.  Valitse ensin **Nimikenro**-kenttä ja sitten **Lisäasetukset**-toiminto.  
3.  Valitse **Nimikeluettelo**-sivulla **Varastointiyksiköt**-toiminto.  
4.  Avaa **Varastointiyksikön luettelo** -sivulla ITÄ varastointiyksikön kortti.  
5.  Huomaa, että **Suunnittelu**-pikavälilehden **Vähimmäistilausmäärä**-kentässä on arvo 10.  
6.  Sulje kaikki sivut **Suunnittelutyökirja**-sivua lukuun ottamatta.  

### Tarkastele lisää tilauksen seurantatapahtumia  

1.  Valitse ensin nimikkeen 1110 (Vanne) suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  

     **Tilauksen seuranta** -sivulla näkyy, että viisi vannetta tarvitaan kutakin tuotantotilausta varten eteen ja taakse.  

     Sama tilauksen seuranta koskee nimikkeiden 1120, 1160 ja 1170 suunnittelurivejä. Nimikkeen 1120 kunkin renkaan tuotannon tuotantorakenteen **Määrä per** -kentän arvo on 50 kappaletta, joten kokonaistarve on 100.  

     Suunnitelurivi nimikkeen 1150 kuudelle kappaleelle näyttää epäsäännölliseltä. Siirry analysoimaan.  

2.  Valitse ensin nimikkeen 1150 suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  

     **Tilauksen seuranta** -sivulla näkyy, että viisi yksikköä on jäljitetty etupyörään ja yksi yksikkö on seurannan ulkopuolella. Siirry tarkastelemaan ei-seurattua määrää.  

3.  Valitse **Ei seurattu määrä** -kenttä.  

     **Ei-seuratut suunnitteluelementit** -sivulla näkyy, että nimike 1150 käyttää suunnitteluparametria Tilauskerrannainen, jonka arvo on 2,00. Tämä määrittää, että nimikettä on tilattava määrä, joka on jaollinen luvulla 2. Viittä lähinnä oleva kahdella jaollinen luku on kuusi.  

     Saman tilauksen seuranta koskee etukeskiön komponentteja 1151 ja 1155. Jokainen tarve lasketaan kuitenkin kertomalla hävikkiprosentti, joka on määritetty nimikkeelle 1150 nimikkeen kortin **Hukkaprosentti** -kentässä.  

 Nyt alkuperäisen tuotantosuunnitelman analyysi on valmis. Huomaa, että **Hyväksy toimenpideviesti** -valintaruutu on valittuna kaikilla suunnitteluriveillä, mikä ilmaisee, että ne voidaan muuntaa toimitustilauksiksi.  

## Toimenpideviestien toteuttaminen  
 Seuraavaksi Karl muuntaa ehdotetut suunnittelurivit toimitustilauksiksi **Toteuta toim.pideviesti** -toiminnolla.  

### Ehdotettujen toimitustilausten luominen automaattisesti  

1.  Valitse **Hyväksy toimenpideviesti** -valintaruutu kaikille suunnitteluriveille, joilla on Poikkeus-tyyppinen varoitus.  
2.  Valitse **Toteuta toimenpideviesti** -toiminto.  
3.  Täytä **Toteuta toim.pideviesti - Suun.** -sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Tuotantotilaus|Ostotilaus|Siirtotilaus|  
    |----------------------|--------------------|--------------------|  
    |Sitovasti suunniteltu|Tee ostotilaukset|Tee siirtotilaukset|  

4.  Luo kaikki ehdotetut toimitustilaukset automaattisesti valitsemalla **OK**.  
5.  Sulje tyhjä **Suunnittelutyökirja**-sivu.  

 Toimitussuunnitelman alkuperäinen laskenta, analyysi ja luonti ITÄ-sijainnin kysynnälle helmikuun ensimmäisellä viikolla on nyt valmis. Seuraavassa osassa toinen asiakas tilaa kymmenen retkipyörää, ja Karlin on laskettava suunnitelma uudelleen.  

## Nettomuutossuunnitelman luominen  
 Seuraavana päivänä ennen toimitustilausten aloittamista tai kirjaamista saapuu uusi myyntitilaus yritykseltä Libros S.A. Tilaus käsittää kymmenen retkipyörää, ja tilauksen toimituspäivä on 12.2.2021. Karl saa ilmoituksen uudesta kysynnästä, joten hän laskee suunnitelman uudelleen. Karl laskee Nettomuutos suunnittelu -toiminnolla ainoastaan edellisen suunnitteluajon jälkeen tulleet kysynnän tai toimituksen muutokset. Lisäksi hän laajentaa suunnittelujakson 14.2.2021 asti kattamaan toisen kysyntäpäivän 12.2.2021.  

 Suunnittelujärjestelmä laskee parhaan tavan kattaa kahden identtisen tuotteen kysynnän. Järjestelmä määrittää, miten osa osto- ja tuotantotilauksista kannattaa yhdistää ja miten muut tilaukset lasketaan uudelleen. Järjestelmä luo myös tarvittaessa uusia tilauksia.  

### Myynnin kysynnän luominen ja uudelleensuunnittelu  

1.  Valitse **Uusi**-toiminto.  
2.  Täytä **Myyntitilaus**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Tilausasiakkaan nimi|Lähetyksen pvm|Nimikkeen nro|Sijainti|määrä|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.A|02-12-2021|1001|ITÄ|10|  

3.  Hyväksy saatavuusvaroitus ja valitse **Kyllä**. Uusi kysyntämäärä kirjataan.  
4.  Seuraavaksi on tarpeen oikaista nykyinen toimitussuunnitelma.  
5.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suunnittelutyökirja** ja valitse sitten vastaava linkki.  
6.  Valitse **Laske nettomuutossuunnitelma** -toiminto.  
7.  Täytä **Laske suunn. - Suunn.työk.** -sivulla kenttä seuraavassa taulukossa kuvatulla tavalla.  

    |Laske suunnitelma|Aloituspvm|Lopetuspvm|Näytä tulokset:|Rajoita kokonaisarvoksi|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Kyllä<br /><br /> **MRP** = Kyllä|01-23-2021|02-14-2021|1001..1300|Sijaintisuodatus = ITÄ|  

8.  Käynnistä suunnitteluajo valitsemalla **OK**.  

 Yhteensä 14 suunnittelutyökirjan riviä on luotu. Huomaa, että ensimmäisen suunnittelurivin **Toimenpideviesti**-kentässä lukee **Uusi**, **Määrä**-kentässä 10 ja **Eräpäivä**-kentässä 12.2.2021. Tämä uusi rivi luodaan yläpäänimikkeelle 1001, Retkipyörä, koska nimikkeen uusintatilaustapa on **Tilaus**. Tämä tarkoittaa, että se on toimitettava yhden suhde yhteen -suhteessa kysyntään, joka on kymmenen kappaleen myyntitilaus.  

 Seuraavat kaksi suunnitteluriviä ovat retkipyörien kiekkojen tuotantotilaukset. Jokaista viittä **Alkuperäinen määrä** -kentässä olemassa olevaa tilausta kasvatetaan arvoon 15 **Määrä**-kentässä. Molemmissa tuotantotilauksissa on muuttumaton eräpäivä, mistä on osoituksena **Toimenpideviesti**-kentässä näkyvä **Muuta määrä**. Tämä koskee myös nimikkeen 1300 suunnittelurivillä, joskin sen tilauskerrannainen 10,00 pyöristää seuratun kysynnän 15 kappaleesta 20 kappaleeseen.  

 Kaikilla muilla suunnitteluriveillä on toimenpideviestit **Aikataul. uud. ja Muuta määrä**. Tämä tarkoittaa, että määrän muutoksen vuoksi eräpäiviä on siirretty ensimmäisen toimitussuunnitelman mukaisesti ( -kenttä), jotta lisämäärä voidaan sisällyttää käytettävissä olevaan tuotantoaikaan (kapasiteetti). Ostetut komponentit ajoitetaan ja lisätään tuotantotilausten lisäämiseksi. Siirry uuden suunnitelman analysointiin.  

## Muutetun suunnittelun tulosten analysoiminen  
 Koska kaikilla erä-erästä-suunnitelluilla suodattimessa olevilla nimikkeillä 1100-1300 on kahden viikon uudelleenajoitusjakso, niiden nykyiset toimitustilaukset muokataan vastaamaan uutta kysyntää, joka tapahtuu määritetyn kahden viikon kuluessa.  

 Useat suunnittelurivit kerrotaan yksinkertaisesti kolmella, jotta saadaan 15 retkipyörää 5 sijasta. Eräpäivät siirretään taaksepäin ajassa, jotta lisätyt määrät voidaan tuottaa Cannon Groupin myyntitilauksen toimituspäivän perusteella. Näillä suunnitteluriveillä voidaan seurata kaikkia määriä. Jäljellä olevia suunnittelurivejä korotetaan kymmenellä kappaleella niiden eräpäivien siirtämisen lisäksi. Näille suunnitteluriveille osa määristä on seurannan ulkopuolella eri suunnitteluparametrien vuoksi. Siirry tarkastelemaan joitakin näistä seurantatapahtumista.  

### Tarkastele kohteen 1250 tilauksen merkintää  

1.  Valitse ensin nimikkeen 1250 suunnittelurivi ja sitten **Tilauksen seuranta** -toiminto.  

     Seitsemän **Tilauksen seuranta** -sivun riviä näyttää, että viittä ja kymmentä kappaletta seurataan takarenkaan kautta retkipyöriin vastaavasti kahdessa myyntitilauksessa.  

     Viimeiset viisi kappaletta ovat seurannan ulkopuolella. Siirry analysoimaan.  

2.  Valitse **Ei seurattu määrä** -kenttä.  

     **Ei-seurattu suunnitteluelementti** -sivulla näkyy, että nimike 1250 käyttää suunnitteluparametria Tilauskerrannainen, jonka arvo on 10,00. Tämän vuoksi suunnittelurivin arvo on yhteensä 20 kappaletta; todellinen tarve on siis pyöristetty ylöspäin lähimpään 10:llä jaolliseen lukuun. Toiset viisi kappaletta ovat ei-seurattu määrä, jolla täytetään suunnitteluparametrin edellytykset.  

3.  Sulje kaikki sivut **Suunnittelutyökirja**-sivua lukuun ottamatta.  

### Olemassa olevan tilauksen tarkasteleminen  

1.  Valitse nimikkeen 1250 suunnittelurivin **Viitatun tilauksen numero** -kentässä.  
2.  Takakeskiön **Sitovasti suun. tuotantotil.**-sivulla. Olemassa oleva kymmenen kappaleen tilaus, johon olet luonut ensimmäisen suunnitteluajon, avautuu.  
3.  Sitovasti suunnitellut tuotantotilaukset  

 Olet nyt käynyt läpi vaihekuvauksen, jossa havainnollistettiin, miten suunnittelujärjestelmässä havaitaan kysyntä automaattisesti, lasketaan toimitustilaukset kysynnän ja suunnitteluparametrien mukaan ja luodaan automaattisesti erilaisia toimitustilauksia sopivia päivämääriä ja määriä käyttäen.  

## Katso myös  
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)    -->
 [Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
