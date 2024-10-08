---
title: Arvonlisäveron määrittäminen
description: 'Varmista, että lasket, kirjaat ja raportoit myynnin ja ostojen ALV:n oikein. Tämän oppaan käyttö on suositeltavaa ALV:tä määritettäessä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 08/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen

Kuluttajat ja yritykset maksavat arvonlisäveroa (ALV:tä), kun he ostavat tavaroita tai palveluja. ALV:n määrä voi vaihdella useiden tekijöiden mukaan. ALV määritetään [!INCLUDE[prod_short](includes/prod_short.md)]issa määrittämään prosentti, joita käytettiin verosummien laskemiseen, seuraavien parametrien perusteella:

* Kenelle myydään  
* Keneltä ostetaan  
* Mitä myydään  
* Mitä ostetaan  

Voit määrittää ALV-laskelmat manuaalisesti, mutta se voi olla hankalaa ja aikaavievää. On helppo käyttää vahingossa erilaisia ALV-kantoja ja luoda epätarkkoja ALV-raportteja. ALV-määrityksen helpottamiseksi suosittelemme käyttämään **ALV-asetusten asennus** -avustettua asennusopasta.

Jos haluat kuitenkin määrittää ALV-laskelmat itse tai jos haluat lisätietoja kustakin vaiheesta, kukin vaihe käsitellään tässä artikkelissa.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended"></a>Käytä ALV:n määrityksessä asetusten ohjattua määritysopasta (suositus)

> [!NOTE]
> Voit käyttää **ALV:n määritys** -opasta vain siinä tapauksessa, että olet luonut *Oman yrityksen* etkä ole vielä kirjannut ALV:n sisältäviä tapahtumia. Lisätietoja Omasta yrityksestä on kohdassa [Uusien yritysten luonti [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](about-new-company.md).

Avaa avustettu asennusopas seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake ja kirjoita **Asetusten ohjattu määritys**. 
2. Valitse **Määritä arvonlisävero (ALV)** ja suorita vaiheet.
3. Kun olet suorittanut avustetut asetukset, käy **ALV-kirjausten asetukset** -sivulla ja tarkista, onko sinun täytettävä lisää kenttiä paikallisen vaatimusten mukaan [!INCLUDE [prod_short](includes/prod_short.md)] -versiossasi. Lue lisätietoja kohdasta [Business Centralin paikalliset toiminnot](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Tarkista ALV-kirjausasetukset.

Jos haluat tukea nopeaa aloitusta, [!INCLUDE [prod_short](includes/prod_short.md)] ilmoittaa, jos kirjausryhmistä tai kirjausasetuksissa (esimerkiksi **ALV-kirjausten asetukset** -sivulla) puuttuu KP-tilit. Voit ottaa tämäntyyppisen ilmoituksen käyttöön tai poistaa sen käytöstä käyttämällä **KP-tili puuttuu kirjausryhmästä tai määrityksestä** -ilmoitusta **Omat ilmoitukset** -sivulla. Siirry **Omat asetukset** -sivulle ja valitse **Ilmoitusten vastaanottoajankohdan muuttaminen** -linkki.  

Jos valitset tällaisen ilmoituksen, [!INCLUDE [prod_short](includes/prod_short.md)] luo nämä kirjausasetukset sen asiakirjan tai päiväkirjan kirjausryhmien perusteella, jota parhaillaan käsittelet.  

Tässä vaiheessa saatat vain täyttää puuttuvat KP-tilit. Mutta myöhemmin, kun tarkennat asetuksia tarkemmin, saatat huomata, että alkuperäinen asetus on virheellinen. [!INCLUDE [prod_short](includes/prod_short.md)] ei salli ALV-kirjausasetusten ja yleisten kirjausasetusten poistamista sen jälkeen, kun niitä on käytetty tapahtumien luomiseen. Voit estää ihmisiä käyttämästä vahingossa asetuksia, jotka eivät enää ole merkityksellisiä uusille julkaisuille, käyttämällä **Yleiset julkaisuasetukset** -sivun **Estetty**-kenttää.

## <a name="set-up-a-default-vat-date-for-documents-and-journals"></a>ALV:n oletuspäivämäärän määrittäminen asiakirjoille ja päiväkirjoille

ALV-raportointi, jota [!INCLUDE [prod_short](includes/prod_short.md)] käyttää, perustuu **ALV-päivämäärään**, joka sisällytetään ALV-tapahtumiin ALV-kauden ALV-raporteissa. ALV-päivämäärää voi muuttaa kaikissa asiakirjoissa ja päiväkirjoissa, mutta sille on määritettävä oletusarvo.

> [!NOTE]
> Kun asiakirja tai päiväkirja on kirjattu, **ALV-päivämäärä** tulee näkyviin **ALV-tapahtumat**- ja **KP-tapahtumat**-kohdissa sekä mahdollisessa kirjatussa asiakirjassa.

Voit määrittää ALV-päivämääräksi oletusarvon seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Yleiset**-pikavälilehden **ALV-oletuspäivämäärä**-kentässä **kirjauspäivämäärä** tai **asiakirjan päivämäärä**.
3. Sulje sivu.  

> [!NOTE]
> Oletusarvoisesti **ALV-oletuspäivämäärä** on **kirjauspäivämäärä**.

### <a name="enable-or-disable-the-vat-date-feature"></a>ALV-pvm-ominaisuuden ottaminen käyttöön tai poistaminen käytöstä

Joissakin maissa ja joillakin alueilla edellytetään, että yritykset käyttävät tiettyä ALV-päivämäärää. Joissakin maissa ja joillakin alueilla yritykset voivat myös muuttaa ALV-päivämäärää tietyissä tilanteissa, kun ne ovat kirjoittaneet asiakirjoja, mutta toiset maat tai alueet eivät salli ALV-päivämäärien muuttamista. Jos haluat sallia eri konteksteja, voit valita, haluatko käyttää tätä toimintoa ja missä määrin.

Voit määrittää ALV-päivämäärän käytön tason seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **yleinen**-pikavälilehden **ALV-päivämäärän käyttö** -kentässä, missä määrin ALV-päivämääräominaisuutta haluat käyttää. Voit valita yhden seuraavista vaihtoehdoista:

   | Tyyppi | Kuvaus |
   |--------------------|-----------------------------------------|
   | **Käytä täydellistä ALV-päivämäärä-toimintoa** | Kaikki **ALV-päivämäärään** liittyvät toiminnot ovat oletusarvon mukaan käytössä ja antavat sinulle maksimaalisen **ALV-päivämäärä**-toiminnon. Voit määrittää päivämäärän, muuttaa sitä asiakirjoissa, raportoida sen perusteella ja muuttaa päivämäärää kirjauksen jälkeen niin kauan kuin jaksoa ei ole suljettu tai suojattu päivämäärien kirjauksen yhteydessä. |
   | **Käytä, mutta älä salli muutoksia** | Kaikki **ALV-päivämäärään** liittyvät asiat toimivat oletusarvoisesti yhtä poikkeusta lukuun ottamatta. **ALV-päivämäärää** ei voi muuttaa **ALV-tapahtumissa**. |
   | **Ei käytä ALV-päivämäärä-toimintoa** | [!INCLUDE [prod_short](includes/prod_short.md)] piilottaa ja määrittää **ALV-päivämäärä**-kentät ei käytettäviksi oleviksi asiakirjoissa, kirjauskansioissa ja tapahtumissa. **ALV-oletuspäivämäärä** määritetään **kirjauspäivämääräksi**. |

3. Sulje sivu.

> [!IMPORTANT]
> Vaikka valitsisit **Ei käytä ALV-päivämäärää -toimintoa** -asetuksen, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää **ALV-päivämäärää** taustalla. Koska **ALV-oletuspäivämäärä** on määritetty **Kirjaus päivämääräksi** etkä voi muuttaa sitä tässä tapauksessa, saat saman kokemuksen kuin ilman tätä ominaisuutta. **ALV-päivämäärä**-kentät poistetaan kaikilta sivuilta, mutta tämä kenttä on edelleen taulukoissa ja raportit toimivat sen perusteella.

### <a name="limiting-periods-for-posting-and-changing-the-vat-date"></a>Kausien rajoittaminen ALV-päivämäärän kirjaamista ja muuttamista varten

Voit estää käyttäjiä kirjaamasta tai vaihtamasta tiettyjen päivämäärävälien ALV-tapahtumia. Rajoitus määritetään käyttämällä kahta seuraavaa asetusta:

* Suljetun **ALV-palautusjakson** perusteella
* **Salli kirjaaminen kohteesta**- ja **Salli kirjaaminen kohteeseen** -kenttien perusteella.

#### <a name="to-limit-posting-based-on-vat-return-period"></a>ALV-palautusjaksoon perustuvan kirjauksen rajoittaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Yleinen**-pikavälilehdellä **ALV-kauden hallinta** -kentässä ALV-palautusjakson ohjausaste. Asetukset kuvaillaan seuraavassa taulukossa.

| Tyyppi | Kuvaus |
|--------------------|-----------------------------------------|
| **Estä kirjaaminen suljetulla jaksolla ja varoita vapautetusta jaksosta** | Estä käyttäjiä kirjaamasta asiakirjaa tai kirjauskansiota tai muuttamalla ALV-tapahtumia, joilla on ALV-päivämäärä suljetulla **ALV-palautusjaksolla**. [!INCLUDE [prod_short](includes/prod_short.md)] näyttää varoituksen myös silloin, kun **ALV-palautusjakso** on avoinna, mutta **ALV-palautuksen** tila on **Vapautettu** tai **Lähetetty**. |
| **Estä kirjaaminen suljetulla jaksolla** | Estä käyttäjiä kirjaamasta asiakirjaa tai kirjauskansiota tai muuttamalla ALV-tapahtumia, joilla on ALV-päivämäärä suljetulla **ALV-palautusjaksolla**. |
| **Varoita kirjattaessa suljetulla jaksolla** | Näytä varoitus, mutta älä estä kirjausta, jos haluat kirjata asiakirjan tai kirjauskansion, jolla on ALV-päivämäärä suljetussa **ALV-palautusjaksossa**. |
| **Poistettu käytöstä** | Älä tee toimenpiteitä suljetun **ALV-palautuskauden** perusteella. |

#### <a name="limit-posting-based-on-allow-fromto-period"></a>Sellaisen kirjauksen rajoittaminen, joka perustuu sallimiseen kohteesta/kohteeseen

> [!NOTE]
> Business Centralin versiosta 23.1 lähtien tätä ohjausobjektia on muutettu. Aiemmissa versioissa **Pääkirjanpidon asetukset** -sivulla oli vain yksi ohjausobjekti sekä kirjaus- että ALV-päivämäärälle. Nyt nämä ohjausobjektit on jaettu niin, että **Pääkirjanpidon asetukset** -sivulla on vain **kirjauspäivämäärän** ohjausobjekti ja **ALV-asetukset**-sivulla vain **ALV-päivämäärän** ohjausobjekti. **Käyttäjäasetukset**-sivulla on uusia päivämääräohjausobjekteja.  

##### <a name="version-231-or-newer"></a>Versio 23.1 tai uudempi

> [!IMPORTANT]
> Varmista uuteen versioon päivitettäessä, että arvot päivitetään uudessa **Salli ALV-päivämäärästä alkaen / Salli ALV-päivämäärään asti** -kohdassa **ALV-asetukset**-sivulla **Ensimm. sallittu kirjauspvm / Viimeinen sallittu kirjauspvm** -kohdasta **Pääkirjanpidon asetukset** -sivulla. Jos haluat käyttää eri päivämääräohjausobjekteja, avaa **ALV-asetukset**-sivu ja tee muutokset.  

Voit määrittää rajoituksia yritykselle tai tietyille käyttäjätasoille.

Koko yrityksen kaikkien kirjausten rajoittaminen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV:n määrittäminen** ja valitse sitten vastaava linkki.  
2. Valitse **ALV-asetukset**-pikavälilehden **Salli ALV-päivämäärästä alkaen** -kentässä ALV-päivämäärä, josta kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärällä ennen tätä päivämäärää ei ole sallittua.  
3. Valitse **ALV-asetukset**-pikavälilehden **Salli ALV-päivämäärään asti** -kentässä ALV-päivämäärä, johon asti kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärälle tämän päivämäärän jälkeen ei ole sallittua. 

Tietyn käyttäjän kirjausten rajoittaminen:  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.  
2. Valitse **Käyttäjätunnus**-kentässä käyttäjä, joka voi kirjata tiettynä ajanjaksona.  
3. Valitse **Salli ALV-päivämäärästä alkaen** -kentässä ALV-päivämäärä, josta kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärällä ennen tätä päivämäärää ei ole sallittua. 
4. Valitse **Salli ALV-päivämäärään asti** -kentässä ALV-päivämäärä, johon asti kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärälle tämän päivämäärän jälkeen ei ole sallittua.  

##### <a name="versions-before-231"></a>Versiot ennen versiota 23.1

Voit määrittää rajoituksia yritykselle tai tietyille käyttäjätasoille.

Koko yrityksen kaikkien kirjausten rajoittaminen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **yleinen**-pikavälilehden **Salli kirjaus kohteesta** -kentässä ALV-päivämäärä, josta kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärällä ennen tätä päivämäärää ei ole sallittua.  
3. Valitse **yleinen**-pikavälilehden **Salli kirjaus kohteeseen** -kentässä ALV-päivämäärä, johon kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärälle tämän päivämäärän jälkeen ei ole sallittua.

Tietyn käyttäjän kirjausten rajoittaminen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.  
2. Valitse **Käyttäjätunnus**-kentässä käyttäjä, joka voi kirjata tiettynä ajanjaksona.  
3. Valitse **Salli kirjaus kohteesta** -kentässä ALV-päivämäärä, josta kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärällä ennen tätä päivämäärää ei ole sallittua.
4. Valitse **Salli kirjaus kohteeseen** -kentässä ALV-päivämäärä, johon asti kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärälle tämän päivämäärän jälkeen ei ole sallittua.

## <a name="set-up-vat-registration-numbers-for-your-countryregion"></a>Määritä oman maan tai alueen ALV-rekisteröintinumerot

Voit auttaa varmistamaan, että annettavat ALV-rekisteröintinumerot ovat kelvollisia, määrittämällä niiden maiden tai alueiden ALV-rekisteröintinumeroiden muodot, joissa sinulla on liiketoimintaa. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää virhesanoman, jos joku tekee virheen tai käyttää muotoa, jota ei hyväksytä maassa tai alueella.

Voit määrittää ALV-rekisteröintinumerot seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maat/alueet**.
2. Valitse ensin maa tai alue ja sitten **ALV-rekisteröintinron muodot** -toiminto.
3. Määritä muoto **Muodot**-kenttään antamalla vähintään yksi seuraavista merkeistä:  

* **#** - edellyttää yksimerkkistä lukua.  
* **@** - edellyttää kirjainta. Muodon kirjainkoolla ei ole merkitystä.  
* **?** Mikä tahansa merkki sallitaan.  

    > [!TIP]
    > Voit käyttää muita merkkejä, kunhan niitä käytetään maan tai alueen muodossa. Joten, jos sinun on sisällytettävä esimerkiksi numeroiden välinen piste tai yhdysviiva, voit määrittää muodon seuraavasti: ##.####.### tai @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Liiketoiminnan ALV-kirjausryhmien määrittäminen

Liiketoiminnan ALV-kirjausryhmien on vastattava niitä markkinoita, joilla teet kauppaa asiakkaiden ja toimittajien kanssa, ja niiden määritettävä ALV:n laskeminen ja kirjaaminen kullakin markkinalla. Esimerkkejä liiketoiminnan ALV-kirjausryhmistä: **Kotimaa** ja **Euroopan unioni (EU)**.  

Käytä koodeja, jotka on helppo muistaa ja jotka kuvaavat liiketoiminnan kirjausryhmää, kuten **EU**, **Muu kuin EU** tai **Kotimaa**. Kunkin koodin on oltava yksilöllinen, joten voit määrittää niin monta koodia kuin haluat, mutta sama koodi ei voi olla samassa taulukossa kahdesti.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoim. ALV-kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.

Liiketoiminnan ALV-kirjausryhmien oletusarvot voidaan luoda linkittämällä ne liiketoiminnan kirjausryhmiin. [!INCLUDE[prod_short](includes/prod_short.md)] määrittää automaattisesti liiketoiminnan ALV-kirjausryhmän koodin, kun määrität liiketoiminnan kirjausryhmän asiakkaaseen, toimittajaan tai pääkirjanpidon tiliin.

## <a name="set-up-vat-product-posting-groups"></a>Tuotteen ALV-kirjausryhmien määrittäminen

ALV-tuotekirjausryhmät edustavat tuotteita ja resursseja, joita ostat tai myyt, ja määrittävät, kuinka ALV lasketaan ja kirjataan tuotteen tai resurssin tyypin mukaan.

Kannattaa käyttää koodeja, jotka on helppo muistaa ja joissa on viittaus ALV-prosenttiin, kuten **EI-ALV** tai **Nolla**, **ALV10** tai **Alennettu**, jos ALV on 10 prosenttia, ja **ALV25** tai **Vakio**, jos ALV on 25 prosenttia.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotteen ALV-kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>ALV-kirjausryhmien yhdistäminen ALV-kirjausasetuksissa

[!INCLUDE[prod_short](includes/prod_short.md)] laskee myynnin ja ostojen ALV-summat ALV-kirjausryhmien perusteella. Nämä ryhmät puolestaan ovat yhdistelmä liiketoiminnan ja tuotteen ALV-kirjausryhmiä. Voit määrittää kullekin yhdistelmälle ALV-prosentin, ALV-laskennan tyypin sekä myyntiin, ostoihin ja vastakirjaukseen liittyvien ALV-kirjausten pääkirjanpidon tilit. Voit määrittää myös, lasketaanko ALV uudelleen, kun maksualennusta käytetään tai vastaanotetaan.  

Voit määrittää niin monta yhdistelmää kuin haluat. Voit ryhmitellä ALV-kirjausasetusten yhdistelmät, joissa on samanlaiset määritteet määrittämällä **ALV-tunnuksen** kullekin ryhmälle ja liittämällä tunnuksen ryhmän jäsenille.  

> [!NOTE]
> A **ALV-tunnus** on koodi, jonka avulla voit ryhmitellä samanlaisia määritteitä. Suosittelemme, että käytät eri ALV-tunnuksia eri ALV-prosenteille.  

ALV-kirjausasetukset yhdistetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 5.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>ALV-kirjausryhmien määrittäminen oletusarvoisesti useille objekteille

Jos haluat käyttää samoja ALV-kirjausryhmiä useissa objekteissa, voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in tekemään niin oletusarvoisesti.

* Voit määrittää liiketoiminnan ALV-kirjausryhmät yleisiin liiketoiminnan kirjausryhmiin tai asiakas- tai toimittajamalleihin.
* Voit määrittää tuotteen ALV-kirjausryhmät yleisiin tuotteen kirjausryhmiin.  

Liiketoiminnan tai tuotteen ALV-kirjausryhmä määritetään, kun valitse asiakkaan, toimittajan, nimikkeen tai resurssin liiketoiminnan tai tuotteen kirjausryhmän.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Määritä ALV-kirjausryhmät yksittäisille tileille, asiakkaille, toimittajille, nimikkeille ja resursseille

Seuraavissa osissa käsitellään ALV-kirjausryhmien määrittämistä yksittäisille objekteille.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>ALV-kirjausryhmien määrittäminen yksittäisille pääkirjanpidon tileille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 6.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2.  **Avaa tilin KP-tilin kortti** .  
3. Valitse **Kirjaus**-pikavälilehden **Yleinen kirjaustyyppi** -kentässä joko **Myynti** tai **Osto**.  
4. Valitse myynti- tai ostotilillä käytettävät ALV-kirjausryhmät.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Liiketoiminnan ALV-kirjausryhmien määrittäminen asiakkaille ja toimittajille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 7.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten vastaava linkki.  
2. Laajenna **Laskutus**-pikavälilehti **Asiakas**- tai **Toimittaja**-kortissa.  
3. Valitse Liiketoiminnan **ALV-kirjausryhmä**.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Tuotteen ALV-kirjausryhmien määritetään yksittäisille nimikkeille ja resursseille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 8.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** tai **Resurssi** ja valitse sitten vastaava linkki.  
2. Tee jompikumpi seuraavista:  

    * Laajenna Nimikkeen kortti Hinta ja kirjaus - **pikavälilehti ja näytä** tuotteen ALV-kirjausryhmä **-kenttä valitsemalla** Näytä lisää **.**  **·**   
    * Laajenna **Resurssi**-kortissa **Laskutus**-pikavälilehti.  
3. Valitse tuotteen ALV-kirjausryhmä.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-nonstandard-vat-rates"></a>Määritä lausekkeet ALV-vapautuksen tai poikkeavien ALV-prosenttien selittämiseksi

Määritä ALV-lause kuvaamaan tietoja käytettävästä ALV-tyypistä. Hallituksen asetukset voivat vaatia näitä tietoja. Kun olet määrittänyt ALV-lauseen ja liittänyt sen ALV-kirjausasetukseen, ALV-lause näkyy kaikissa tulostetuissa myyntiasiakirjoissa, jotka käyttävät ALV-kirjausten asetusryhmää.

Voit tarvittaessa määrittää myös, miten ALV-lauseet käännetään muille kielille. Kun luot ja tulostat ALV-tunnuksen sisältävän myyntiasiakirjan, asiakirja sisältää käännetyn ALV-lauseen. Asiakaskortissa määritetty kielikoodi määrittää käytetyn kielen.

Kun käytät erityyppisissä asiakirjoissa, kuten laskuissa tai hyvityslaskuissa, epätäsmääviä ALV-määriä, voit joutua sisällyttämään poikkeuksen tekstin (ALV-lauseke). Vapautustekstissä kerrotaan, miksi laskit alennetun ALV:in tai nolla-ALV:in. Voit määritellä liiketoiminnan asiakirjoihin sisällytettävät eri ALV-lausekkeet kunkin asiakirjatyypin osalta **ALV-lausekkeet asiakirjatyypin mukaan** -sivulla.

Voit muokata tai poistaa ALV-lauseen, ja muutokset näkyvät luodussa raportissa. [!INCLUDE[prod_short](includes/prod_short.md)] ei kuitenkaan säilytä muutoshistoriaa. Raportissa ALV-lauseen kuvaukset tulostetaan ja näytetään raportin kaikille riveille ALV-summan ja ALV-perusteen summan rinnalla. Jos ALV-lausetta ei ole määritetty millekään myyntiasiakirjan riville, koko osa jätetään pois raporttia tulostettaessa.

### <a name="to-set-up-vat-clauses"></a>ALV-lauseiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 9.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten vastaava linkki.  
2. Luo **ALV-lauseet**-sivulla uusi rivi.  
3. Kirjoita lauseen tunnus **Koodi**-kenttään. Lause määritetään tällä koodilla ALV-kirjausryhmiin.  
4. Kirjoita **Kuvaus**-kenttään ALV-vapautusteksti, jonka haluat näkyvän asiakirjoissa, joihin ALV voi sisältyä. Voit tarvittaessa kirjoittaa lisätekstin **Kuvaus 2** -kenttään. Teksti näkyy uusilla tiedostoriveillä.
5. Valitse **Kuvaus asiakirjatyypin mukaan** -toiminto.
6. Määritä **ALV-lausekkeille asiakirjatyyppi** -sivulla kentät, jotka sisältävät sen ALV-vapautustekstin, jonka asiakirjatyypin haluat näyttää.  
7. Valinnainen: ALV-lauseen voi määrittää ALV-kirjausryhmään heti valitsemalla ensin **Asetukset** ja sitten lauseen. Jos halua odottaa, voit määrittää lauseen myöhemmin **ALV-kirjausten asetukset** -sivulla.  
8. Valinnainen: Valitsemalla **Käännökset** toiminnon voit määrittää, miten ALV-lause käännetään.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>ALV-lauseen määrittäminen ALV-kirjausryhmään

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 10.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.  
2.  **Valitse ALV-lauseke koodi -** sarakkeessa lauseke, jota käytetään jokaiselle ALV-kirjausasetukselle, jota se koskee.  

### <a name="to-specify-translations-for-vat-clauses"></a>ALV-lauseiden käännösten määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 11.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten vastaava linkki.  
2. Valitse **Käännökset**-toiminto.  
3. Valitse **Kielikoodi**-kentässä kieli, jolle käännetään.  
4. Kirjoita kuvausten käännökset **Kuvaus**- ja **Kuvaus 2** -kenttiin. Tämä teksti näkyy käännetyissä ALV-raporttiasiakirjoissa.  

### <a name="to-specify-extended-text-for-vat-clauses"></a>ALV-lauseiden lisätekstin määrittäminen

> [!NOTE]  
> Jos maasi tai alueesi vaatii ALV-lausekkeille oletusversion tukemaa pidemmän tekstin, voit määrittää pidemmän tekstin ALV-lausekkeille *lisätekstinä*, jotta se tulostetaan myynti-ja ostoraportteihin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 11.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten vastaava linkki.  
2. Valitse **Lisätekstit**-toiminto.  
3. Valitse **Uusi**-toiminto.  
4. Täytä **Kielikoodi**- ja **Kuvaus**-kentät.  
5. Vaihtoehtoisesti voit valita **Kaikki kielikoodit**-kentän tai määrittää haluamasi kielen **Kielikoodi**-kentässä, jos käytät kielikoodeja.  
6. Anna arvot **Aloituspvm**- ja/tai **Lopetuspvm**-kenttään, jos haluat rajoittaa lisätekstin käyttöpäiviä.  
7. Kirjoita **Teksti**-riveille ALV-lausekkeidesi lisäteksti.  
8. Valitse asianmukaiset kentät niitä asiakirjatyyppejä varten, joihin haluat lisätekstin tulostuvan.  
9. Sulje sivu.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>ALV-kirjausten asetukset luominen käsittelemään tuonnin ALV:tä

Käytä *Tuonnin ALV* -ominaisuutta kirjataksesi asiakirjan, jossa koko summaa on ALV:tä. Tämän ominaisuuden käyttö on tarpeellista, jos saat veroviranomaisilta laskun tuontitavaroiden arvonlisäverosta.  

Määritä tuonnin ALV:n koodit seuraavasti:  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 12.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotteen ALV-kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Määritä Tuotteen ALV-kirjausryhmät -sivulla uusi tuotteen ALV-kirjausryhmä tuonnin ALV:tä varten.  
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 13.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.  
4. Luo ALV-kirjausten asetukset -sivulla uusi rivi tai käytä aiemmin luotua liiketoiminnan ALV-kirjausryhmää yhdessä tuonnin ALV:tä varten luodun uuden tuotteen ALV-kirjausryhmän kanssa.  
5. Valitse **ALV-laskennan tyyppi** -kentässä **Täysi ALV**.  
6. Anna **Ostojen ALV-tili** -kentässä se pääkirjanpidon tili, jota käytetään tuonnin ALV:n kirjaamiseen. Kaikki muut tilit ovat valinnaisia.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countriesregions"></a>ALV-vastakirjaus EU-maiden tai alueiden välisessä kaupassa

Joiden yritysten on käytettävä ALV-vastakirjausta tehdessään kauppaa muiden yritysten kanssa. Sääntö koskee esimerkiksi EU:n maiden tai alueiden välisiä myyntejä ja ostoja.  

> [!NOTE]  
> Tämä sääntö on voimassa, kun käydään kauppaa yritysten kanssa, jotka ovat ALV-velvollisia toisessa EU-maassa / toisella EU-alueella. Jos harjoitat liiketoimintaa suoraan muiden EU-maiden/alueiden kuluttajien kanssa, pyydä soveltuvat ALV-säännöt veroviranomaisilta.  

> [!TIP]  
> Voit tarkistaa EU:n ALV-rekisteröintinumeron vahvistuspalvelun avulla, onko yritys rekisteröity ALV-velvolliseksi toisessa EU-maassa tai toisella EU-alueella. Palvelua voi käyttää maksutta [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on ohje aiheessa [ALV-rekisterinumeroiden vahvistaminen](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countriesregions"></a>Myynnit EU-maihin/alueille

ALV:tä ei lasketa myynneistä muiden EU-maiden/alueiden ALV-velvollisille yrityksille. Näiden EU-maihin/alueille tapahtuvien myyntien arvo on raportoitava erikseen ALV-ilmoituksessa.  

Laskeaksesi asianmukaisesti ALV:t myynneistä EU-maissa/-alueilla, sinun pitäisi:  

* Määritä myyntirivi, jossa on samat tiedot kuin ostoja varten. Jos määrität rivejä EU-maista/alueilta tapahtuvia ostoja varten **ALV-kirjausten asetukset** -sivulla, voit käyttää näitä rivejä myös myynteihin.  
* Liitä liiketoiminnan ALV-kirjausryhmät asiakkaan kortin **Laskutus**-pikavälilehden **Liiketoiminnan ALV-kirjausryhmä** -kenttään kullekin EU-asiakkaalle. Asiakkaan ALV-rekisterinumero on myös lisättävä **Ulkomaankauppa**-pikavälilehden **ALV-rekisterinro**-kenttään.  

Kun kirjaat myynnin toisen EU-maan/alueen asiakkaalle, [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelma laskee ALV-summan ja luo ALV-tapahtuman, jossa on tiedot ALV-vastakirjauksesta ja ALV-perusteesta. ALV-summa lasketaan tämän summan avulla. Yleisen päiväkirjan ALV-tileille ei kirjata tapahtumia.

Jos haluat käyttää liiketoiminnan ALV-kirjausryhmän ja tuotteen ALV-kirjausryhmän yhdistelmää, kun haluat raportoida palveluina jaksoittaisissa ALV-raporteissa, merkitse **EU-palvelu** -kenttä.

> [!NOTE]  
> **EU-palvelu** -kenttä on käytettävissä vain ALV-raporteissa. Kenttä ei liity **Palveluilmoitus**- tai **Palveluiden Intrastat** -ominaisuuksiin.

## <a name="vat-rounding-for-documents"></a>ALV:n pyöristäminen asiakirjoja varten

Vielä kirjaamattomien asiakirjojen summat pyöristetään ja näytetään kirjattujen summien lopullista pyöristämistä vastaavalla tavalla. [!INCLUDE [prod_short](includes/prod_short.md)] laskee ALV:n koko asiakirjalle. ALV-laskelma perustuu kaikkien saman ALV-tunnisteen sisältävien tositteen rivien summaan.  

## <a name="set-up-vat-reporting"></a>Määritä ALV-raportointi

Sinun on määritettävä tiedot siitä, mitä vaatimuksia maasi veroviranomaisella on ALV-raporttien lähettämisen suhteen. Seuraavissa vaiheissa kuvataan yleisimmin käytettävät tiedot. Maasi tai alueesi voi kuitenkin edellyttää muitakin vaiheita. Lisätietoja saat asianomaisesta artikkelista vasemman paneelin *Paikalliset toiminnot* -osasta.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Katso myös

[ALV-ilmoitusmallien ja ALV-ilmoitusten nimien määrittäminen](finance-how-setup-vat-statement.md)    
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)    
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)    
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)    
[ALV-kannan muutostyökalun käyttö](finance-how-use-vat-rate-change-tool.md)    
[ALV-rekisterinumeroiden tarkistaminen](finance-how-validate-vat-registration-number.md)    
[Business Centralin paikalliset toiminnot](about-localization.md)    
[ALV-raportointi saksankielisessä versiossa](LocalFunctionality/Germany/vat-reporting.md)    
[Belgian ALV](LocalFunctionality/Belgium/belgian-vat.md)    
[Italian ALV](LocalFunctionality/Italy/italian-vat.md)    
[Verkko-ALV- ja ICP-ilmoitusten määrittäminen Hollannin versiossa](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)    
[ALV-raportit espanjaksi](LocalFunctionality/Spain/vat-reports.md)    
[Tavaroiden ja palveluiden verokirjausten määrittäminen Australian versiossa](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)    
[ALV Tšekin versiossa](LocalFunctionality/Czech/finance-vat.md)    
[ALV-raportointi Norjassa](LocalFunctionality/Norway/norwegian-vat-reporting.md)    
[Tuote-/palveluveron ja harmonisoidun arvonlisäveron ilmoittaminen Kanadassa](LocalFunctionality/Canada/sales-tax-goods-services.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
