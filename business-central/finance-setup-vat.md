---
title: Määritä arvolisävero
description: 'Varmista, että lasket, kirjaat ja raportoit myynnin ja ostojen ALV:n oikein. Tämän oppaan käyttö on suositeltavaa ALV:tä määritettäessä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 01/31/2023
ms.author: bholtorf
---

# Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen

Kuluttajat ja yritykset maksavat arvonlisäveroa (ALV:tä), kun he ostavat tavaroita tai palveluja. ALV:n määrä voi vaihdella useiden tekijöiden mukaan. ALV määritetään [!INCLUDE[prod_short](includes/prod_short.md)]issa määrittämään prosentti, joita käytettiin verosummien laskemiseen, seuraavien parametrien perusteella:

* Kenelle myydään  
* Keneltä ostetaan  
* Mitä myydään  
* Mitä ostetaan  

Voit määrittää ALV-laskelmat manuaalisesti, mutta se voi olla hankalaa ja aikaavievää. Tämä johtuu siitä, että on erittäin helppoa käyttää vahingossa erilaisia ALV-kantoja ja luoda epätarkkoja ALV-raportteja. Jotta ALV-asetukset olisi helpompi määrittää, on suositeltavaa käyttää tuotteessa olevaa avustettua **ALV-määritys**-opasta. 

Jos haluat kuitenkin määrittää ALV-laskelmat itse tai jos haluat lisätietoja kustakin vaiheesta, kukin vaihe käsitellään tässä artikkelissa:  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## Käytä ALV:n määrityksessä asetusten ohjattua määritysopasta (suositus)

> [!NOTE]
> Voit käyttää **ALV:n määritys** -opasta vain siinä tapauksessa, että olet luonut *Oman yrityksen* etkä ole vielä kirjannut ALV:n sisältäviä tapahtumia.

Avaa avustettu asennusopas seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake ja kirjoita **Asetusten ohjattu määritys**. 
2. Valitse **Määritä arvonlisävero (ALV)** ja suorita vaiheet.
3. Kun olet suorittanut avustetut asetukset, käy **ALV-kirjausten asetukset** -sivulla ja tarkista, onko sinun täytettävä lisää kenttiä paikallisen vaatimusten mukaan [!INCLUDE [prod_short](includes/prod_short.md)] -versiossasi. Lue lisätietoja kohdasta [Business Centralin paikalliset toiminnot](about-localization.md).  

### Tarkista ALV-kirjausasetukset.

Jos haluat tukea nopeaa aloitusta, [!INCLUDE [prod_short](includes/prod_short.md)] ilmoittaa, jos kirjausryhmistä tai kirjausasetuksissa (esimerkiksi **ALV-kirjausten asetukset** -sivulla) puuttuu KP-tilit. Voit ottaa tämäntyyppisen ilmoituksen käyttöön tai poistaa sen käytöstä käyttämällä *KP-tili puuttuu kirjausryhmästä tai määrityksestä* -ilmoitusta **Omat ilmoitukset** -sivulla. Siirry **Omat asetukset** -sivulle ja valitse *Ilmoitusten vastaanottoajankohdan muuttaminen*. linkki.  

Jos valitset tällaisen ilmoituksen, [!INCLUDE [prod_short](includes/prod_short.md)] luo nämä kirjausasetukset automaattisesti sen asiakirjan tai päiväkirjan kirjausryhmien perusteella, jota parhaillaan käsittelet.  

Tässä vaiheessa saatat vain täyttää puuttuvat KP-tilit. Mutta myöhemmin, kun tarkennat asetuksia tarkemmin, saatat huomata, että alkuperäinen asetus on virheellinen. Eikä [!INCLUDE [prod_short](includes/prod_short.md)] salli ALV-kirjausasetusten ja yleisten kirjausasetusten poistoa silloin, kun on luotuna tapahtumia, jotka perustuvat tällaisiin konfiguraatioihin. Joten vuoden 2022 1. julkaisuaallossa voit käyttää **ALV-kirjausasetukset** -sivun **Estetty**-kenttää, jos haluat estää käyttäjiä vahingossa käyttämästä asetuksia, jotka eivät enää ole merkityksellisiä uusissa kirjauksissa.

## ALV:n oletuspäivämäärän määrittäminen asiakirjoille ja päiväkirjoille

ALV-raportointi, jota [!INCLUDE [prod_short](includes/prod_short.md)] käyttää, perustuu **ALV-päivämäärään**, joka sisällytetään ALV-tapahtumiin ALV-kauden ALV-raporteissa. ALV-päivämäärää voi muuttaa kaikissa asiakirjoissa ja päiväkirjoissa, mutta sille on määritettävä oletusarvo.

> [!NOTE]
> Kun asiakirja tai päiväkirja on kirjattu, **ALV-päivämäärä** tulee näkyviin **ALV-tapahtumat**- ja **KP-tapahtumat**-kohdissa sekä mahdollisessa kirjatussa asiakirjassa.

Voit määrittää ALV-päivämääräksi oletusarvon seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Yleiset**-pikavälilehden **ALV-oletuspäivämäärä**-kentässä **kirjauspäivämäärä** tai **asiakirjan päivämäärä**.
3. Sulje sivu.  

> [!NOTE]
> Oletusarvoisesti **ALV-oletuspäivämäärä** on **kirjauspäivämäärä**.

### ALV-päivämääräominaisuuden ottaminen käyttöön tai poistaminen käytöstä

Joissakin maissa ja joillakin alueilla edellytetään, että yritykset käyttävät tiettyä ALV-päivämäärää. Joissakin maissa ja joillakin alueilla yritykset voivat myös muuttaa ALV-päivämäärää tietyissä tilanteissa, kun ne ovat kirjoittaneet asiakirjoja, mutta toiset maat eivät salli ALV-päivämäärien muuttamista. Jos haluat sallia eri konteksteja, voit valita, haluatko käyttää tätä toimintoa ja missä määrin.

Voit määrittää ALV-päivämäärän käytön tason seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **yleinen**-pikavälilehden **ALV-päivämäärän käyttö** -kentässä, missä määrin ALV-päivämääräominaisuutta haluat käyttää. Voit valita yhden seuraavista vaihtoehdoista:

| Tyyppi | Kuvaus |
|--------------------|-----------------------------------------|
| **Käytä täydellistä ALV-päivämäärä-toimintoa** | Kaikki **ALV-päivämäärään** liittyvät toiminnot ovat oletusarvon mukaan käytössä ja antavat sinulle maksimaalisen **ALV-päivämäärä**-toiminnon. Voit määrittää päivämäärän, muuttaa sitä asiakirjoissa, raportoida sen perusteella ja muuttaa päivämäärää kirjauksen jälkeen niin kauan kuin jaksoa ei ole suljettu tai suojattu päivämäärien kirjauksen yhteydessä. |
| **Käytä, mutta älä salli muutoksia** | Kaikki **ALV-päivämäärään** liittyvät asiat toimivat oletusarvoisesti yhtä poikkeusta lukuun ottamatta. **ALV-päivämäärää** ei voi muuttaa **ALV-tapahtumissa**. |
| **Ei käytä ALV-päivämäärä-toimintoa** | [!INCLUDE [prod_short](includes/prod_short.md)] piilottaa ja määrittää **ALV-päivämäärä**-kentät ei käytettäviksi oleviksi asiakirjoissa, kirjauskansioissa ja tapahtumissa. **ALV-oletuspäivämäärä** määritetään **Kirjauspäivämääräksi**. |

3. Sulje sivu.

> [!IMPORTANT]
> Vaikka valitsisit **Ei käytä ALV-päivämäärää -toimintoa** -asetuksen, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää **ALV-päivämäärää** taustalla. Koska **ALV-oletuspäivämäärä** on määritetty **Kirjaus päivämääräksi** etkä voi muuttaa sitä tässä tapauksessa, saat saman kokemuksen kuin ilman tätä ominaisuutta. **ALV-päivämäärä**-kentät poistetaan kaikilta sivuilta, mutta tämä kenttä on edelleen taulukoissa ja raportit toimivat sen perusteella.

### Kausien rajoittaminen ALV-päivämäärän kirjaamista ja muuttamista varten

Voit estää käyttäjiä kirjaamasta tai vaihtamasta tiettyjen päivämäärävälien ALV-tapahtumia. Rajoitus määritetään käyttämällä kahta asetusta:

* Suljetun **ALV-palautusjakson** perusteella
* **Salli kirjaaminen kohteesta**- ja **Salli kirjaaminen kohteeseen** -kenttien perusteella.

#### ALV-palautusjaksoon perustuvan kirjauksen rajoittaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Yleinen**-pikavälilehdellä **ALV-kauden hallinta** -kentässä ALV-palautusjakson ohjausaste. Asetukset kuvaillaan seuraavassa taulukossa.

| Tyyppi | Kuvaus |
|--------------------|-----------------------------------------|
| **Estä kirjaaminen suljetulla jaksolla ja varoita vapautetusta jaksosta** | Estä käyttäjiä kirjaamasta asiakirjaa tai kirjauskansiota tai muuttamalla ALV-tapahtumia, joilla on ALV-päivämäärä suljetulla **ALV-palautusjaksolla**. [!INCLUDE [prod_short](includes/prod_short.md)] näyttää varoituksen myös silloin, kun **ALV-palautusjakso** on avoinna, mutta **ALV-palautuksen** tila on **Vapautettu** tai **Lähetetty**. |
| **Estä kirjaaminen suljetulla jaksolla** | Estä käyttäjiä kirjaamasta asiakirjaa tai kirjauskansiota tai muuttamalla ALV-tapahtumia, joilla on ALV-päivämäärä suljetulla **ALV-palautusjaksolla**. |
| **Varoita kirjattaessa suljetulla jaksolla** | Näytä varoitus, mutta älä estä kirjausta, jos haluat kirjata asiakirjan tai kirjauskansion, jolla on ALV-päivämäärä suljetussa **ALV-palautusjaksossa**. |
| **Poistettu käytöstä** | Älä tee toimenpiteitä suljetun **ALV-palautuskauden** perusteella. |

#### Voit rajoittaa kirjauksen, joka perustuu sallimiseen kohteesta/kohteeseen

Voit määrittää rajoituksia yritykselle tai tietyille käyttäjätasoille.

Koko yrityksen kaikkien kirjausten rajoittaminen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **yleinen**-pikavälilehden **Salli kirjaus kohteesta** -kentässä ALV-päivämäärä, josta kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärällä ennen tätä päivämäärää ei ole sallittua.  
3. Valitse **yleinen**-pikavälilehden **Salli kirjaus kohteeseen** -kentässä ALV-päivämäärä, johon kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärälle tämän päivämäärän jälkeen ei ole sallittua.

Tietyn käyttäjän kirjausten rajoittaminen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.  
2. Valitse **käyttäjätunnus**-kentässä käyttäjä, jonka haluat sallia kirjaavan tiettynä ajanjaksona.  
3. Valitse **Salli kirjaus kohteesta** -kentässä ALV-päivämäärä, josta kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärällä ennen tätä päivämäärää ei ole sallittua.
4. Valitse **Salli kirjaus kohteeseen** -kentässä ALV-päivämäärä, johon asti kirjaus sallitaan. Asiakirjan tai kirjauskansion kirjaaminen ALV-päivämäärälle tämän päivämäärän jälkeen ei ole sallittua.

## Määritä oman maan tai alueen ALV-rekisteröintinumerot

Voit auttaa varmistamaan, että annettavat ALV-rekisteröintinumerot ovat kelvollisia, määrittämällä niiden maiden tai alueiden ALV-rekisteröintinumeroiden muodot, joissa sinulla on liiketoimintaa. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää virhesanoman, jos joku tekee virheen tai käyttää muotoa, jota ei hyväksytä maassa tai alueella.

ALV-rekisteröintinumeroiden määritysohjeet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maat/alueet**.
2. Valitse ensin maa tai alue ja sitten **ALV-rekisteröintinron muodot** -toiminto.
3. Määritä muoto **Muodot**-kenttään antamalla vähintään yksi seuraavista merkeistä:  

* **#** - edellyttää yksimerkkistä lukua.  
* **@** - edellyttää kirjainta. Muodon kirjainkoolla ei ole merkitystä.  
* **?** Mikä tahansa merkki sallitaan.  

    > [!TIP]
    > Voit käyttää muita merkkejä, kunhan niitä käytetään maan tai alueen muodossa. Joten, jos sinun on sisällytettävä esimerkiksi numeroiden välinen piste tai yhdysviiva, voit määrittää muodon seuraavasti: ##.####.### tai @@-###-###.  

## Liiketoiminnan ALV-kirjausryhmien määrittäminen

Liiketoiminnan ALV-kirjausryhmien on vastattava niitä markkinoita, joilla teet kauppaa asiakkaiden ja toimittajien kanssa, ja niiden määritettävä ALV:n laskeminen ja kirjaaminen kullakin markkinalla. Esimerkkejä liiketoiminnan ALV-kirjausryhmistä: **Kotimaa** ja **Euroopan unioni (EU)**.  

Käytä koodeja, jotka on helppo muistaa ja jotka kuvaavat liiketoiminnan kirjausryhmää, kuten **EU**, **Muu kuin EU** tai **Kotimaa**. Kunkin koodin on oltava yksilöllinen, joten voit määrittää niin monta koodia kuin haluat, mutta sama koodi ei voi olla samassa taulukossa kahdesti.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoim. ALV-kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.

Liiketoiminnan ALV-kirjausryhmien oletusarvot voidaan luoda linkittämällä ne liiketoiminnan kirjausryhmiin. [!INCLUDE[prod_short](includes/prod_short.md)] määrittää automaattisesti liiketoiminnan ALV-kirjausryhmän koodin, kun määrität liiketoiminnan kirjausryhmän asiakkaaseen, toimittajaan tai pääkirjanpidon tiliin.

## Tuotteen ALV-kirjausryhmien määrittäminen

ALV-tuotekirjausryhmät edustavat tuotteita ja resursseja, joita ostat tai myyt, ja määrittävät, kuinka ALV lasketaan ja kirjataan tuotteen tai resurssin tyypin mukaan.

Olisi hyvä käyttää koodeja, jotka on helppo muistaa ja joissa on viittaus ALV-prosenttiin, kuten **EI-ALV** tai **Nolla**, **ALV10** tai **Alennettu**, jos ALV on 10 prosenttia, ja **ALV25** tai **Vakio**, jos ALV on 25 prosenttia.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotteen ALV-kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.

## ALV-kirjausryhmien yhdistäminen ALV-kirjausasetuksissa

[!INCLUDE[prod_short](includes/prod_short.md)] laskee myynnin ja ostojen ALV-summat ALV-kirjausryhmien perusteella. Nämä ryhmät puolestaan ovat yhdistelmä liiketoiminnan ja tuotteen ALV-kirjausryhmiä. Voit määrittää kullekin yhdistelmälle ALV-prosentin, ALV-laskennan tyypin sekä myyntiin, ostoihin ja vastakirjaukseen liittyvien ALV-kirjausten pääkirjanpidon tilit. Voit määrittää myös, lasketaanko ALV uudelleen, kun maksualennusta käytetään tai vastaanotetaan.  

Voit määrittää niin monta yhdistelmää kuin haluat. Jos haluat ryhmitellä ALV-kirjausasetusten yhdistelmät, joissa on samanlaiset määritteet, voit määrittää **ALV-tunnuksen** kullekin ryhmälle ja liittää tunnuksen ryhmän jäsenille.

ALV-kirjausasetukset yhdistetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 5.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## ALV-kirjausryhmien määrittäminen oletusarvoisesti useille objekteille

Jos haluat käyttää samoja ALV-kirjausryhmiä useissa objekteissa, voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in tekemään niin oletusarvoisesti. Määrityksen voi tehdä kahdella tavalla:

* Voit määrittää liiketoiminnan ALV-kirjausryhmät yleisiin liiketoiminnan kirjausryhmiin tai asiakas- tai toimittajamalleihin.
* Voit määrittää tuotteen ALV-kirjausryhmät yleisiin tuotteen kirjausryhmiin.  

Liiketoiminnan tai tuotteen ALV-kirjausryhmä määritetään, kun valitse asiakkaan, toimittajan, nimikkeen tai resurssin liiketoiminnan tai tuotteen kirjausryhmän.

## Määritä ALV-kirjausryhmät yksittäisille tileille, asiakkaille, toimittajille, nimikkeille ja resursseille

Seuraavissa osissa käsitellään ALV-kirjausryhmien määrittämistä yksittäisille objekteille.

### ALV-kirjausryhmien määrittäminen yksittäisille pääkirjanpidon tileille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 6.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Avaa valitun tilin **KP-tilin** kortti.  
3. Valitse **Kirjaus**-pikavälilehden **Yleinen kirjaustyyppi** -kentässä joko **Myynti** tai **Osto**.  
4. Valitse myynti- tai ostotilillä käytettävät ALV-kirjausryhmät.  

### Liiketoiminnan ALV-kirjausryhmien määrittäminen asiakkaille ja toimittajille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 7.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten vastaava linkki.  
2. Laajenna **Laskutus**-pikavälilehti **Asiakas**- tai **Toimittaja**-kortissa.  
3. Valitse liiketoiminnan ALV-kirjausryhmä.  

### Tuotteen ALV-kirjausryhmien määritetään yksittäisille nimikkeille ja resursseille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 8.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** tai **Resurssi** ja valitse sitten vastaava linkki.  
2. Tee jompikumpi seuraavista toimista:  

    * Laajenna **Nimike**-kortin **Hinta ja kirjaus** -pikavälilehti ja valitse sitten **Näytä lisää**. **Tuotteen ALV-kirjausryhmä** -kenttä avautuu.  
    * Laajenna **Resurssi**-kortissa **Laskutus**-pikavälilehti.  
3. Valitse tuotteen ALV-kirjausryhmä.  

## Määritä lausekkeet ALV-vapautuksen tai poikkeavien ALV-prosenttien selittämiseksi

Määritä ALV-lause kuvaamaan tietoja käytettävästä ALV-tyypistä. Tietoja voidaan vaatia hallituksen asetuksilla. Kun olet määrittänyt ALV-lauseen ja liittänyt sen ALV-kirjausasetukseen, ALV-lause näkyy kaikissa tulostetuissa myyntiasiakirjoissa, jotka käyttävät ALV-kirjausten asetusryhmää.

Voit tarvittaessa määrittää myös, miten ALV-lauseet käännetään muille kielille. Kun luot ja tulostat ALV-tunnuksen sisältävän myyntiasiakirjan, asiakirja sisältää käännetyn ALV-lauseen. Asiakaskortissa määritetty kielikoodi määrittää käytetyn kielen.

Kun poikkeavia ALV-prosentteja käytetään erityyppisissä asiakirjoissa, kuten laskuissa tai hyvityslaskuissa, yritysten on yleensä sisällytettävä vapautusteksti (ALV-lauseke), jossa ilmoitetaan, miksi alennettu ALV tai nolla-ALV on laskettu. Voit määrittää eri ALV-lausekkeita, jotka sisällytetään liiketoiminta-asiakirjoihin asiakirja tyypin mukaan, esimerkiksi laskun tai hyvityslaskun mukaan. Tämä tehdään **ALV-lausekkeet asiakirjatyypin mukaan** -sivulla.

Voit muokata tai poistaa ALV-lauseen, ja muutokset näkyvät luodussa raportissa. [!INCLUDE[prod_short](includes/prod_short.md)] ei kuitenkaan säilytä muutoshistoriaa. Raportissa ALV-lauseen kuvaukset tulostetaan ja näytetään raportin kaikille riveille ALV-summan ja ALV-perusteen summan rinnalla. Jos ALV-lausetta ei ole määritetty millekään myyntiasiakirjan riville, koko osa jätetään pois raporttia tulostettaessa.

### ALV-lauseiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 9.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten vastaava linkki.  
2. Luo **ALV-lauseet**-sivulla uusi rivi.  
3. Kirjoita lauseen tunnus **Koodi**-kenttään. Lause määritetään tällä koodilla ALV-kirjausryhmiin.  
4. Kirjoita **Kuvaus**-kenttään ALV-vapautusteksti, jonka haluat näkyvän asiakirjoissa, joihin ALV voi sisältyä. Voit tarvittaessa kirjoittaa lisätekstin **Kuvaus 2** -kenttään. Teksti näkyy uusilla tiedostoriveillä.
5. Valitse **Kuvaus asiakirjatyypin mukaan** -toiminto.
6. Määritä **ALV-lausekkeille asiakirjatyyppi** -sivulla kentät, jotka sisältävät sen ALV-vapautustekstin, jonka asiakirjatyypin haluat näyttää.  
7. Valinnainen: ALV-lauseen voi määrittää ALV-kirjausryhmään heti valitsemalla ensin **Asetukset** ja sitten lauseen. Jos halua odottaa, voit määrittää lauseen myöhemmin **ALV-kirjausten asetukset** -sivulla.  
8. Valinnainen: Valitsemalla **Käännökset** toiminnon voit määrittää, miten ALV-lause käännetään.

### ALV-lauseen määrittäminen ALV-kirjausryhmään

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 10.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **ALV-lause**-sarakkeessa lause, jota käytetään kussakin ALV-kirjauksen asetuksissa, joihin sitä sovelletaan.  

### ALV-lauseiden käännösten määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 11.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten vastaava linkki.  
2. Valitse **Käännökset**-toiminto.  
3. Valitse **Kielikoodi**-kentässä kieli, jolle käännetään.  
4. Kirjoita kuvausten käännökset **Kuvaus**- ja **Kuvaus 2** -kenttiin. Tämä teksti näkyy käännetyissä ALV-raporttiasiakirjoissa.  

### ALV-lauseiden lisätekstin määrittäminen

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

## ALV-kirjausten asetukset luominen käsittelemään tuonnin ALV:tä

*Tuonnin ALV* -ominaisuudella kirjataan asiakirja, jossa koko summaa on ALV:tä. Tämä on tarpeellista, jos saat veroviranomaisilta laskun tuontitavaroiden arvonlisäverosta.  

Määritä tuonnin ALV:n koodit seuraavasti:  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 12.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotteen ALV-kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Määritä Tuotteen ALV-kirjausryhmät -sivulla uusi tuotteen ALV-kirjausryhmä tuonnin ALV:tä varten.  
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 13.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.  
4. Luo ALV-kirjausten asetukset -sivulla uusi rivi tai käytä aiemmin luotua liiketoiminnan ALV-kirjausryhmää yhdessä tuonnin ALV:tä varten luodun uuden tuotteen ALV-kirjausryhmän kanssa.  
5. Valitse **ALV-laskennan tyyppi** -kentässä **Täysi ALV**.  
6. Anna **Ostojen ALV-tili** -kentässä se pääkirjanpidon tili, jota käytetään tuonnin ALV:n kirjaamiseen. Kaikki muut tilit ovat valinnaisia.  

## ALV-vastakirjauksen käyttäminen EU-maiden tai -alueiden välisessä kaupassa

Joiden yritysten on käytettävä ALV-vastakirjausta tehdessään kauppaa muiden yritysten kanssa. Sääntö koskee esimerkiksi EU:n maiden tai alueiden välisiä myyntejä ja ostoja.  

> [!NOTE]  
> Tämä sääntö on voimassa, kun käydään kauppaa yritysten kanssa, jotka ovat ALV-velvollisia toisessa EU-maassa / toisella EU-alueella. Jos harjoitat liiketoimintaa suoraan muiden EU-maiden/alueiden kuluttajien kanssa, pyydä soveltuvat ALV-säännöt veroviranomaisilta.  

> [!TIP]  
> Voit tarkistaa EU:n ALV-rekisteröintinumeron vahvistuspalvelun avulla, onko yritys rekisteröity ALV-velvolliseksi toisessa EU-maassa tai toisella EU-alueella. Palvelua voi käyttää maksutta [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on ohje aiheessa [ALV-rekisterinumeroiden vahvistaminen](finance-how-validate-vat-registration-number.md).

### Myynti EU-maihin tai -alueille

ALV:tä ei lasketa myynneistä muiden EU-maiden/alueiden ALV-velvollisille yrityksille. Näiden EU-maihin/alueille tapahtuvien myyntien arvo on raportoitava erikseen ALV-ilmoituksessa.  

Laskeaksesi asianmukaisesti ALV:t myynneistä EU-maissa/-alueilla, sinun pitäisi:  

* Määritä myyntirivi, jossa on samat tiedot kuin ostoja varten. Jos olet jo määrittänyt rivejä EU-maista/alueilta tapahtuvia ostoja varten **ALV-kirjausten asetukset** -sivulla, voit käyttää näitä rivejä myös myynteihin.  
* Liitä liiketoiminnan ALV-kirjausryhmät asiakkaan kortin **Laskutus**-pikavälilehden **Liiketoiminnan ALV-kirjausryhmä** -kenttään kullekin EU-asiakkaalle. Asiakkaan ALV-rekisterinumero on myös lisättävä **Ulkomaankauppa**-pikavälilehden **ALV-rekisterinro**-kenttään.  

Kun kirjaat myynnin toisen EU-maan/alueen asiakkaalle, ohjelma laskee ALV-summan ja luo ALV-tapahtuman, jossa on tiedot ALV-vastakirjauksesta ja ALV-perusteesta (ALV-summan laskemiseen käytettävästä summasta). Yleisen päiväkirjan ALV-tileille ei kirjata tapahtumia.

Jos haluat käyttää liiketoiminnan ALV-kirjausryhmän ja tuotteen ALV-kirjausryhmän yhdistelmää, kun haluat raportoida palveluina jaksoittaisissa ALV-raporteissa, merkitse **EU-palvelu** -kenttä.

> [!NOTE]  
> **EU-palvelu** -kenttä on käytettävissä vain ALV-raporteissa. Kenttä ei liity **Palveluilmoitus**- tai **Palveluiden Intrastat** -ominaisuuksiin.

## ALV:n pyöristäminen asiakirjoja varten

Vielä kirjaamattomien asiakirjojen summat pyöristetään ja näytetään kirjattujen summien lopullista pyöristämistä vastaavalla tavalla. ALV lasketaan koko asiakirjalle, mikä tarkoittaa sitä, että laskettu ALV perustuu kaikkien rivien summaan, joilla on sama ALV-tunnus asiakirjassa.  

## Määritä ALV-raportointi

Sinun on määritettävä tiedot siitä, mitä vaatimuksia maasi veroviranomaisella on ALV-raporttien lähettämisen suhteen. Seuraavissa vaiheissa kuvataan yleisimmin käytettävät tiedot. Maasi tai alueesi voi kuitenkin edellyttää muitakin vaiheita. Lisätietoja saat asianomaisesta artikkelista vasemman paneelin *Paikalliset toiminnot* -osasta.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## Katso myös

[ALV-ilmoitusmallien ja ALV-ilmoitusten nimien määrittäminen](finance-how-setup-vat-statement.md)  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[ALV-kannan muutostyökalun käyttö](finance-how-use-vat-rate-change-tool.md)  
[ALV-rekisterinumeroiden tarkistaminen](finance-how-validate-vat-registration-number.md)  
[Business Centralin paikalliset toiminnot](about-localization.md)  
[ALV-raportointi Saksan versiossa](LocalFunctionality/Germany/vat-reporting.md)  
[Belgian ALV](LocalFunctionality/Belgium/belgian-vat.md)  
[Italian ALV](LocalFunctionality/Italy/italian-vat.md)  
[Sähköisten ALV-ja ICP-ilmoitusten määrittäminen Hollannin versiossa](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[ALV-raportit Espanjan versiossa](LocalFunctionality/Spain/vat-reports.md)  
[Määritä tavaroiden ja palveluiden veron kirjaus Australian versiossa](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[ALV Tšekin versiossa](LocalFunctionality/Czech/finance-vat.md)  
[ALV-raportointi Norjan versiossa](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Tuote-/palveluveron ja harmonisoidun arvonlisäveron ilmoittaminen Kanadassa](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
