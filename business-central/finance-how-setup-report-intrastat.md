---
title: Intrastat-raportoinnin määrittäminen
description: Opi määrittämään Intrastat-raportointiominaisuudet raportoimaan muiden EU-maissa toimivien yritysten kanssa käyty kauppa.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077
ms.date: 09/02/2022
ms.author: altotovi
ms.openlocfilehash: b6adddb338af36f07abe4c6cb67c8113657ccb7c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605486"
---
# <a name="set-up-intrastat-reporting"></a>Intrastat-raportoinnin määrittäminen

Kaikkien Euroopan unionin (EU) alueen yritysten täytyy raportoida kaupastaan muiden EU-maiden/alueiden kanssa. Yritysten tulee raportoida tavaran liikkuminen kotimaan/-alueen tilastoviranomaisille kuukausittain ja raportti on toimitettava veroviranomaisille. Intrastat on järjestelmä, jolla kerätään kauppatilastoja tavaroista näissä maissa/alueilla. **Intrastat-raportin** avulla voit suorittaa jaksoittaisen Intrastat-raportoinnin (tyypillisesti kuukausittain), keräämisen, kirjaamisen ja raportoinnin kauppatavaran paikallisen lainsäädännön mukaisesti.

Intrastat-raportointi perustuu kaikkiin maihin sovellettaviin EU:n perussäädöksiin; käytännössä on kuitenkin eroja yksittäisten maiden välillä. Jokaisella maalla on omat sääntönsä siitä, mitä ja miten tarkalleen raportoidaan.

> [!NOTE]
> Intrastat-tietoja ei sovelleta maiden välisten palvelujen siirtoon, vaan vain tavaroihin (nimikkeisiin ja käyttöomaisuuteen). Jos paikallishallinto vaatii rekisteröimään palvelujen liikkumisen maiden välillä, se voidaan tehdä käyttämällä **palvelun määrittely** -toimintoa.
>
> Tämä ominaisuus on tarkoitus olla saatavilla marraskuusta 2022 alkaen sovelluksena [AppSourcessa](https://go.microsoft.com/fwlink/?linkid=2081646), joten jos haluat käyttää sitä, sinun on ensin asennettava se **Laajennustenhallinta**-sivulla.

> [!IMPORTANT]
> Tämä artikkeli kattaa uuden Intrastat-kokemuksen, joka on saatavilla [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman versiosta 21 lähtien. Ota yhteyttä järjestelmänvalvojaan ja ota selvää, mitä versiota yrityksesi käyttää ja miten uudet toiminnot otetaan käyttöön.
>
> Lue edellisen version Intrastat-asetukset- ja käyttö-artikkeli kohdassa [Määritä ja raportoi Intrastat](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a>Ota käyttöön uusi Intrastat-käyttökokemus

Vuoden 2022 2. julkaisuaallossa [!INCLUDE[prod_short](includes/prod_short.md)] sisältää uudelleensuunnitellun Intrastat-kokemuksen ja laajennettuja ominaisuuksia. Jos uusi Intrastat-toiminto ei ole käytössä ympäristössäsi, järjestelmänvalvoja voi ottaa sen manuaalisesti käyttöön **Ominaisuuksien hallinta** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ominaisuuksien hallinta** ja valitse sitten vastaava linkki.
2. Valitse **Ominaisuuksien hallinta** -sivulla **Ominaisuuspäivitys: Korvaa aiemmat Intrastat-toiminnot uudella Intrastat-laajennuksella** -rivi. Lisätietoja ominaisuuksien hallinnasta on kohdassa [Tulevien ominaisuuksien käyttöönotto etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management) hallinann sisällössä.
3. Valitse **Ota käyttöön** -sarakkeessa **Kaikki käyttäjät**.
4. Lue selitys siitä, miten järjestelmä päivitetään, ja valitse **Kyllä**, jos olet samaa mieltä.
5. Valitse **Seuraava** ja Intrastatin perusasetukset tulevat näyttöön. Lue lisää Intrastat-asetuksista [Intrastat-määritys](#intrastat-configuration)-osiossa.
6. Kun asetukset on määritetty, aloita uuden Intrastat-kokemuksen käyttö valitsemalla **valmis**.

> [!IMPORTANT]
> Muista, että vanhoja ja uusia kokemuksia ei voi käyttää rinnakkain. Ennen kuin otat laajennuksen käyttöön tuotantoympäristössä, on suositeltavaa ottaa tämä ominaisuus käyttöön ja testata sitä eristysympäristössä tuotantotiedon kopion kanssa ennen kuin teet sen tuotantoympäristössä. Kun uusi käyttäjäkokemus on aktivoitu tuotantoympäristössä, et voi palata takaisin vanhaan Intrastat-toimintoon.

> [!NOTE]
> Yrityksen sijainnista riippuen yllä kuvatun ominaisuuden ottaminen käyttöön on riittävää. Sellaisten maiden osalta, joilla on erityistoimintoja Intrastat-raportointia varten, ota käyttöön päälaajennuksen lisäksi maakohtaiset Intrastat-sovellukset.

## <a name="intrastat-configuration"></a>Intrastatin määritys

Ennen kuin Intrastat-raportteja voi käyttää, on määritettävä useita konfiguraatioita.

### <a name="intrastat-reporting-setup"></a>Intrastat-raportoinnin määrittäminen

**Intrastat-raportoinnin asetukset** -sivua käytetään Intrastat-raportoinnin käyttöönottoon ja sen oletusaletusten määrittelyyn. Voit määrittää sen, tarvitkseeko sinun raportoida Intrastat lähetyksistä (toimitukset), kuiteista (saapuvat) vai molemmista, riippuen paikkalisten asetuksien rajoista. Voit myös määrittää oletusasetukset tapahtumatyypeille tavallisia ja palautusdokumentteja koskien, joita käytetään maksuliikenteen raportointiin.

Intrastat-raportoinnin määrittäminen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-raportoinnin asetukset** ja valitse sitten vastaava linkki.
2. Avaa **Yleiset**-pikavälilehti ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Seuraavassa taulukossa on kuvattu joitakin avainkenttiä:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Raportoi vastaanotot** | Määrittää, että vastaanotettujen tavaroiden saapuminen sisällytetään Intrastat-raportteihin. |
   | **Raportoi toimitukset** | Määrittää, että lähetettyjen nimikkeiden toimitukset sisällytetään Intrastat-raportteihin. |
   | **Lähetykset, joiden peruste on**  | Määrittää, minkä maakoodin perusteella Intrastat-raportin rivit määritetään. Voit valita yhden vaihtoehdoista: **Tilaus asiakkaan maahan**, **Laskutus asiakkaan maahan** tai **Toimitus asiakkaan maahan**. |
   | **ALV-numero, jonka perusteena on** | Määrittää, minkä asiakas-/toimittajakoodin perusteella Intrastat-raportin ALV-numero määritetään. Voit valita yhden vaihtoehdoista: **Tilaus asiakkaan ALV** tai **Laskutus asiakkaan ALV**. |
   | **Järjestelmään tallennettu yrityksen ALV-numero** | Määrittää, miten yrityksen ALV-rekisterinumero viedään Intrastat-tiedostoon. Voit valita yhden vaihtoehdoista: ALV-rekisterinumero, lisäämällä EU-maakoodin etuliitteeksi ja poistamalla EU-maakoodin ALV-rekisterinrosta. |
   | **Järjestelmään tallennettu toimittajan ALV-numero** | Määrittää, miten toimittajan ALV-rekisterinumero viedään Intrastat-tiedostoon. Voit valita yhden vaihtoehdoista: ALV-rekisterinumero, lisäämällä EU-maakoodin etuliitteeksi ja poistamalla EU-maakoodin ALV-rekisterinrosta. |
   | **Järjestelmään tallennettu asiakkaan ALV-numero** | Määrittää, miten asiakkaan ALV-rekisterinumero viedään Intrastat-tiedostoon. Voit valita yhden vaihtoehdoista: ALV-rekisterinumero, lisäämällä EU-maakoodin etuliitteeksi ja poistamalla EU-maakoodin ALV-rekisterinrosta. |
   | **Hanki kumppanin ALV-tunnus** | Määrittää sen **Intrastat-raportin** rivin tyypin, josta kumppanin ALV-rekisterinumero päivitetään. Paikallisista tarpeista riippuen voit valita vain vastaanottoa varten, vain toimitusta varten tai molemmille rivityypeille. |
3. Avaa **Oletustransaktiot**-pikavälilehti ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Seuraavassa taulukossa on kuvattu joitakin avainkenttiä:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Oletustapahtumatyyppi** | Määrittää säännöllisten myyntitoimitusten, huoltotoimitusten ja ostovastaanottojen oletustapahtumatyypin. |
   | **Oletustapahtumatyyppi – Palautukset** | Määrittää myyntipalautusten, huoltopalautusten ja ostopalautusten oletustapahtumatyypin. |
   | **Oletusarvoinen yksityishenkilön ALV-numero** | Määrittää yksityisen henkilön ALV-numeron, jos yksityishenkilöllä on oltava oma ALV-numero Intrastat-raportissa. |
   | **Oletusarvoinen kolmikantakaupan ALV-numero** | Määrittää oletusarvoisen kolmikantakaupan ALV-numeron siinä tapauksessa, että sinulla ei ole sen ALV-numeroa. |
   | **Oletusarvoinen tuntemattoman tilan ALV** | Määrittää oletusarvoisen ALV-numeron tuntemattomalle tilalle. |
   | **Oletusarvoinen maa-/aluekoodi** | Määrittää oletusarvoisen vastaanottomaan koodin. |
4. Avaa **Raportointi**-pikavälilehti ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Seuraavassa taulukossa on kuvattu joitakin avainkenttiä:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Tiedonsiirtomäärityksen koodi** | Määrittää Intrastat-tiedoston luontiin käytettävän tiedonsiirtomäärityksen koodin. Se toimii vain, jos **jaettujen vastaanottojen/toimitusten tiedostot** -kentän arvona on **ei**. |
   | **Jaa Vastaanotot-/Toimitukset-tiedostot** | Määrittää, raportoidaanko vastaanotot ja toimitukset kahdessa erillisessä tiedostossa. |
   | **Zip-tiedostot** | Määrittää, lisätäänkö raporttitiedostot zip-tiedostoon. |
   | **Tiedonsiirtomäärityksen koodi – Vastaanotto** | Määrittää vastaanotettujen tavaroiden Intrastat-tiedoston luontiin käytettävän tiedonsiirtomäärityksen koodin. Se toimii vain, jos **jaettujen vastaanottojen/toimitusten tiedostot** -kentän arvona on **Kyllä**. |
   | **Tiedonsiirtomäärityksen koodi – Toimitus** | Määrittää toimitettujen tavaroiden Intrastat-tiedoston luontiin käytettävän tiedonsiirtomäärityksen koodin. Se toimii vain, jos **jaettujen vastaanottojen/toimitusten tiedostot** -kentän arvona on **Kyllä**. |
5. Avaa **Numerointi**-pikavälilehti määrittääksesi **Intrastat-nrot**.

### <a name="set-up-a-reporting-file"></a>Määritä raportointitiedosto

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tietojenvaihtomääritykset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Kuvaa **Yleiset**-pikavälilehdellä tiedonsiirron määritelmä, datatiedostotyyppi, sarakeerotin, liittyvät koodiyksiköt, XMLport ja muut kentät täyttämällä kentät.
4. Kuvaile **Rivimääritykset**-pikavälilehdessä datatiedoston rivien muotoilua täyttämällä kentät **rivityyppi**-kenttään ja missä sinun täytyy määrittää tämän rivin sarakkeiden määrä.
5. Täytä **Sarakemääritykset**-pikavälilehden kunkin suunniteltujen sarakkeiden rivi. Voit määrittää sarakkeiden nimet, tietotyypit (*teksti*, *päivämäärä* tai *desimaaliluku*), sarakkeen omistavan kiinteäleveyksisen rivin pituuden, jos tiedoston tyyppi on vakioteksti ja joitakin muita parametreja.
6. Valitse **kenttien vastaavuus** -toiminto **rivimääritykset**-pikavälilehdessä, kun haluat avata **kenttien vastaavuus** -sivun.
7. Luo uusi tapahtuma ja valitse **Yleinen**-pikavälilehdessä oikea **taulukkotunnus** (**Intrastat-raportin riville**, valitse 4812) ja täytä sitten lisää kenttiä:
   1. Määritä avainindeksi, jota käytetään lähdetietueiden lajittelussa ennen vientiä **Avainindeksi**-kentässä.
   2. Valitse oikea **Yhdistämis-codeunit**.
8. Lisää **Kenttien vastaavuus** -pikavälilehdessä sarakkeet, jotka olet määrittänyt aiemmin **Sarakemääritykset** -pikavälilehdessä, ja lisää sitten seuraava:
   1. Määrittää kunkin sarakkeen **kenttätunnuksen**.
   2. Määrittele **muunnossääntö** jokaiselle tarvitsemallesi sarakkeelle. Se määrittää säännön, joka muuntaa tuodun tekstin tuetuksi arvoksi ennen kuin se voidaan yhdistää määritettyyn kenttään [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Kun valitset arvon tässä kentässä, täsmälleen sama arvo syötetään **Muunnossääntö**-kenttään **tiedonvaihto-kentän kartoituspuskuri** -taulukkoon ja päinvastoin.
9. Jos sinun täytyy ryhmitellä tapahtumia tiettyjen sarakkeiden perusteella, valitse **Kenttien ryhmittely** -pikavälilehdessä kentät, joita haluat käyttää ryhmittelemiseen.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] sisältää kaikkien lokalisoitujen maiden Intrastatin esimääritetyn tiedonvaihtomäärityksen. Lue lisätietoja uuden tietojenvaihtomäärityksen luomisesta tai muuttamisesta kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Pakollisten kenttien määrittäminen Intrastat-raportin tarkistusluettelon avulla

Joissakin maissa viranomaiset vaativat Intrastat-raportteihin esimerkiksi ostojen toimitustavan tai joitakin arvoja myynnin ylittäessä tietyn raja-arvon.

Pakollisten kenttien ja/tai arvojen määrittäminen **Intrastat-raportti**-sivulla:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-raporttiasetukset**, valitse sitten vastaava linkki.
2. Valitse **Intrastat-raportin tarkistusluettelo** -toiminto.
3. Lisää tarvittavat rivit tarkistusta varten seuraavien ohjeiden avulla:
   1. Määritä **Kentän nro** -kenttä kenttään, jonka arvon on oltava jokin muu kuin tyhjä.
   2. Täytä **Suodatuskenttä** tarvittaessa seuraavien sääntöjen perusteella:
      1. Kun avaat **Suodatinsivun**, valitse **Suodatin**, jota haluat käyttää tarkistuksessa.
      2. Valitse seuraavassa vaiheessa käytettyyn **suodattimeen** liittyvä arvo.
      3. Jos sinulla on lisää suodattimia, joita tarvitset tämän kentän täyttämiseen, voit lisätä toisen suodattimen noudattamalla samoja vaiheita.
      4. Kun olet kirjoittanut valitun kentän suodattimet, valitse **OK**.
   3. Valitse **Käänteinen suodatinlauseke** -kenttä määrittääksesi, että kenttien tarkistus suoritetaan vain riveillä, jotka eivät vastaa suodatinlauseketta. Jos riviä ei ole suodatettu, tämä kenttä ohitetaan.

> [!NOTE]
> Kun avaat **suodatinsivun** **suodatinlauseke**-riviltä, voit käyttää kaikkia vakiosuodatuslausekkeita, jotka liittyvät suodatettavaan kenttään.
>
> Ole varovainen määrittäessäsi oikeellisuustarkistussääntöjä, koska ne voivat vaihdella maittain.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a>Käytä mukautettuja codeunitseja Intrastat-raporteissa

Jos haluat muuttaa tapaa, jolla Intrastat toimii ja oletuskonfiguraatio ei riitä, voit mukauttaa järjestelmää laajentamalla vakio-ominaisuuksia. Jos sinun on muutettava Intrastat-käyttäytymistä, voit kehittää omia codeunitseja. Kun luot codeunitseja, sinun täytyy kuitenkin tehdä lisää muutoksia niiden käyttöön. Järjestelmän määrittäminen käyttämään omia objekteja:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-raporttien määrittäminen** ja valitse sitten vastaava linkki.
2. Lisää uusi rivi **ALV-raporttien määritys** -sivulla.
3. Valitse **ALV-raportin tyyppi** -kentässä **Intrastat-raportti** -valinta.
4. **ALV-raportin versio** -kentässä määritetään raportin versio.
5. Sen jälkeen voit lisätä koodiyksiköt seuraaville vaihtoehdoille: a. Määrittele **Ehdota rivejä codeunit-tunnukseen** -kentässä uusi codeunit Intrastat-raporttirivien ehdottamista varten.
   b. Määritä **Sisällön codeunitin tunnus** -kentässä uusi koodiyksikkö tietojen viemistä varten tiedonsiirtomääritystä käyttämällä.
   c. Määrittele **Validoi codeunit-tunnus** -kentässä uusi codeunit Intrastat-raporttirivien ehdottamista varten.

> [!IMPORTANT]
>
> Tämän rivin on oltava tyhjä, jos käytät vakiocodeuniteja. Luo rivi ja määritä se vain, jos olet kehittänyt mukautettuja codeunitseja.

## <a name="other-intrastat-configurations"></a>Muut Intrastatin määritykset

> [!IMPORTANT]
> Asiakas- ja toimittajakortit sisältävät **Intrastat-kumppanin tyyppi**-kentän, jolla on samat arvovaihtoehdot kuin **Kumppanin tyyppi** -kentällä eli "" (tyhjä), *Yritys* ja *Henkilö*. **Intrastat-kumppanin tyyppi** -kenttä on korvannut **Kumppanin tyyppi** -kentän Intrastat-raportoinnissa. **Kumppanin tyyppi** -kenttää käytetään yhtenäisen euromaksualueen (SEPA) määrittämiseen SEPA-suoraveloitusjärjestelmän (Core tai B2B) määrittämiseksi. **Intrastat-kumppanin tyyppiä** -kenttää käytetään vain Intrastat-raportoinnissa. Tällä tavoin voit tarpeen mukaan määrittää eri arvot näille kahdelle kentälle.
>
> Jos **Intrastat-kumppanin tyyppi** -kenttä jätetään tyhjäksi, Intrastat-raportoinnissa käytetään **Kumppanin tyyppi** -kentän arvoa.

**Intrastat-raportin asetuksia**, **Tiedonvaihtomäärityksiä** ja **Intrastat-raportin tarkistusluetteloa** lukuun ottamatta sinun on määritettävä myös muita asetuksia:

| Sivu | Kuvaus |
| ---- | ----------- |
| **Maat/alueet** | Ennen kuin aloitat Intrastat-raporttien käyttämisen, sinun täytyy myös määrittää **maat/alueet**-sivu. Tällä sivulla sinun täytyy lisätä **EU-maa-/aluekoodi** ja **Intrastat-koodi** määritelläksesi sen maan/alueen koodin, jonka kanssa käyt kauppaa, niin kuin se on käytössä Intrastat-raportoinnissa. |
| **Tavaranimikkeet** | Monissa maissa tulli- ja veroviranomaiset määrittävät kahdeksannumeroiset koodit eri nimikkeille. Jotta nimikkeen tapahtumat sisältäisivät tarvittavat tiedot ohjelman tuodessa ne Intrastat-ilmoituksen riville, sinun on syötettävä nimikekoodi **Tavaranimike**-sivulle. Etsi niiden nimikkeiden koodit, joilla yrityksesi käy kauppaa, ja syötä ne **Tavaranimikkeet**-sivulle. |
| **Kuljetusmuodot** | Intrastat-kuljetusmuodoilla on seitsemän yksimerkkistä koodia. **1** tarkoittaa merikuljetusta, **2** rautatiekuljetusta, **3** tiekuljetusta, **4** ilmakuljetusta, **5** postitusta, **7** kiinteää asennusta ja **9** omaa käyttövoimaa (kuten auton kuljettaminen sitä ajamalla). [!INCLUDE[prod_short](includes/prod_short.md)] ei edellytä näitä tiettyjä koodeja, mutta suosituksena on käyttää merkitykseltään vastaavia kuvauksia. |
| **Kauppatapahtumien luonteet** | Mailla ja alueilla on eri koodit Intrastat-tapahtumatyypeille, kuten tavallisille ostoille ja myynneille, palautettujen tavaroiden vaihdolle ja palauttamattomien tavaroiden vaihdolle. Määritä omaa maata tai aluetta koskevat koodit. Näitä koodeja käytetään myynti-ja ostoasiakirjojen **Ulkomaankauppa**-pikavälilehdessä sekä palautusten käsittelyssä. |
| **Tapahtumamääritykset** | Määritä koodit, jotka täydentävät transaktiotyypin kuvauksia. |
  > [!NOTE]
  > Tammikuusta 2022 alkaen Intrastat edellyttää eri tapahtuman luonteen koodeja yksityishenkilöille tai ALV-rekisteröitymättömille yrityksille suunnatuille ja ALV-rekisteröityneille yrityksille osoitetuille toimituksille. Tämän vaatimuksen täyttämiseksi on suositeltavaa tarkistaa tapahtumien luonteiden koodit ja/tai lisätä uusia sellaisia **Tapahtumien tyypit** -sivulle kulloisenkin maan vaatimusten mukaisesti. Lisäksi kannattaa tarkistaa ja päivittää **Intrastat-kumppanin tyyppi**-kenttä muotoon *Henkilö* asianomaisten asiakkaiden eli yksityishenkilöjen ja ALV-rekisteröimättömien yritysten **Asiakas**-sivulla. Jos et ole varma oikeasta Intrastat-kumppani- tai tapahtumatyypistä, suosittelemme, että pyydät samassa maassa tai samalla alueella asuvan asiantuntijan neuvoa.

| **Kenttä** | **Kuvaus** |
| --------- | --------------- |
| **Nettopaino** | Paino on eräs Intrastat-raportointiin liittyvistä peruskokoonpanoista, koska **kokonaispaino** on pakollinen raportoinnissa. Jotta tämä vaatimus olisi valmis, sinun täytyy täyttää myös nimikkeen tai käyttöomaisuuden kortin **nettopaino**-kenttä. |
| **Alkuperämaan koodi** | Käytä kaksikirjaimisia ISO-alfakoodeja nimikkeelle tai käyttöomaisuuskortille sen maan osalta, jossa tuote hankittiin tai tuotettiin. Jos tuotetta on tuotettu useammassa kuin yhdessä maassa, alkuperämaa on viimeinen maa, jossa sitä käsiteltiin merkittävästi. |
| **Tuontijäsenvaltion kumppanitoiminnan harjoittajan ALV-tunnistenumero** | Tämä on tuontijäsenvaltion kumppanitoiminnan harjoittajan ALV-tunnistenumero. ALV-tunnusta käytetään myös EU-maiden välisten vientitietojen vaihdossa jäsenvaltioiden kesken, ja sen avulla jäsenvaltiot voivat jakaa vastaanotetut tiedot oman maansa tuontiyritykselle. Raportointiyksiköiden on ilmoitettava sen yrityksen ALV-tunnus, joka on ilmoittanut unionin sisäisen tuotteiden hankinnan jäsenvaltiossa, johon tuote tuotiin. |

Myös seuraavat voi määrittää:

* **Kauppatavarakoodit**: Tulli- ja veroviranomaiset ovat luoneet nimikkeiden ja palvelujen luokittelua varten numeeriset koodit. Nämä koodit määritetään nimikkeissä.
* **Alueet**: Täydentäviä maita ja alueita koskevia tietoja.
* **Tulo-/ lähtöpaikat**: Määritä tämän vaihtoehdon avulla sijainnit, joissa lähetät nimikkeitä muihin maihin tai vastaanotat nimikkeitä muista maista. Lentoasema on esimerkki tulo- tai lähtöpaikasta. Tulo- tai lähtöpaikat annetaan myynti- ja ostoasiakirjoihin **Ulkomaankauppa**-pikavälilehdessä. Nämä tiedot kopioidaan myös nimiketapahtumista Intrastat-ilmoituksen luomisen yhteydessä.
* **Täydentävä mittayksikkö**: Intrastat-raportoinnissa käytettävä tavaroiden määrä voi olla joko nettopaino (kilogrammoina) tai lisäyksikkö. Jos tarvitaan lisäyksiköitä, ne on määritettävä nimikkeille ja käyttöomaisuudelle.

#### <a name="set-up-transport-methods"></a>Kuljetusmuotojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuljetusmuodot**, valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a>Kauppatapahtuman luonteen koodien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tapahtuman tyypit** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a>Muut asiaan liittyvät määritykset

Ennen kuin käytät Intrastat-raportointiominaisuutta, sinun täytyy määrittää joitain kenttiä nimikkeen, käyttöomaisuuden, asiakkaan ja toimittajan korteille.

#### <a name="item-cards"></a>Nimikekortit

Kaikkien Intrastatiin liittyvien tarvittavien tietojen määrittäminen nimikekortteihin:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet**, valitse sitten vastaava linkki.
2. Valitse kohde, jonka haluat määrittää.
3. Laajenna **Kustannukset & kirjaus** -pikavälilehti ja täytä **tavaranimikenumero**, **Lisämittayksikkö** sekä **Alkuperämaan/-alueen koodi** -kentät.
4. Laajenna **varasto**-pikavälilehti ja syötä desimaaliarvo **nettopaino**-kenttään.

> [!NOTE]
> Voit käyttää lisämittayksikkönä eri mittayksiköitä. Jos tämä ei ole sama kuin **Perusmittayksikkö**, tämä mittayksikkö on määritettävä **Nimikkeen mittayksiköt** -sivulla.

#### <a name="fixed-asset-cards"></a>Käyttöomaisuuden kortti

Kaikkien Intrastatiin liittyvien tarvittavien tietojen määrittäminen käyttöomaisuuskortteihin:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus**, valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jota haluat määrittää.
3. Laajenna **Intrastat**-pikavälilehti ja täytä **Tavaranimikenro**-, **Nettopaino**- ja **Lisämittayksikkö**-kentät.

> [!NOTE]
> Voit käyttää lisämittayksikkönä eri mittayksiköitä. Mutta minkä tahansa **Mittayksikön koodin** valitset, sen **Määrä** Intrastat-raporteissa on aina 1.

#### <a name="vendor-cards"></a>Toimittajan kortit

Ennen kuin voit käyttää toimittajaa Intrastat-raportoinnissa, sinulla täytyy olla oma **Maa-/aluekoodi** ja **ALV-rekisterinro** kullekin niistä sekä lisätietoja **Toimittajan kortti** -sivusta:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat**, valitse sitten vastaava linkki.
2. Valitse toimittaja, jonka haluat määrittää.
3. **Intrastat**-pikavälilehdessä voit määrittää oletusarvot **oletussiirtotyyppi**-, **oletussiirtotyyppi - palautukset** ja **oletuskuljetusmuoto** -kentille.
4. Laajenna **maksut** -pikavälilehti ja valitse **Intrastat-kumppanien tyyppi** -kentässä oleva valinta, jos haluat määrittää, onko toimittaja henkilö vai yritys Intrastat-raportoinnissa.

#### <a name="customer-cards"></a>Asiakaskortit

Ennen kuin voit käyttää asiakasta Intrastat-raportoinnissa, sinulla täytyy olla oma **Maa-/aluekoodi** ja **ALV-rekisterinro** kullekin niistä sekä lisätietoja **Asiakaskortti**-sivusta:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat**, valitse sitten vastaava linkki.
2. Valitse asiakas, jonka haluat määrittää.
3. **Intrastat**-pikavälilehdessä voit määrittää oletusarvot **oletussiirtotyyppi**-, **oletussiirtotyyppi - palautukset** ja **oletuskuljetusmuoto** -kentille.
4. Laajenna **maksut** -pikavälilehti ja valitse **Intrastat-kumppanien tyyppi** -kentässä oleva valinta, jos haluat määrittää, onko toimittaja henkilö vai yritys Intrastat-raportoinnissa.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Nimikkeiden ja käyttöomaisuuden jättäminen pois Intrastat-raportoinnista

Jos tietty nimike tai käyttöomaisuus jätetään pois Intrastat-raportoinnin avulla, kortissa olevaa vaihtoehtoa täytyy muuttaa.

##### <a name="exclude-an-item-from-intrastat-reporting"></a>Sulje nimike pois Intrastat-raportoinnista

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet**, valitse sitten vastaava linkki.
2. Valitse kohde, jonka haluat määrittää.
3. Laajenna **Kustannus & kirjaus** -pikavälilehti ja valitse sitten **Jätä pois Intrastat-raportista** -kenttä.

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Käyttöomaisuuden jättäminen pois Intrastat-raportoinnista

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus**, valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jota haluat määrittää.
3. Laajenna **Intrastat**-pikavälilehti ja valitse sitten **Jätä pois Intrastat-raportista** -kenttä.

## <a name="country-specific-intrastat-setup"></a>Maakohtaiset Intrastat-asetukset

<!-- PM's note: Currently, we will add only the 'Overview' topic; the topic 'Manage Intrastat Country Specifics' and country details will wait until 21.1 when I update with all country-based details -->

Intrastat-vaatimukset ovat samanlaiset kaikissa EU:n jäsenvaltioissa, joskin tärkeitä poikkeuksia on olemassa. Teoriassa sääntöjä olisi sovellettava yhdenmukaisesti kaikissa jäsenvaltioissa. Täytäntöönpanossa on kuitenkin eroja, koska jotkin jäsenvaltiot antavat suuntaviivoja siitä, miten asetuksen yleisiä periaatteita olisi sovellettava erityistilanteissa (esimerkiksi kaupalliset näytteet, tavaroiden palautus jne.). Nämä suuntaviivat voivat johtaa erilaisiin tuloksiin eri tilanteissa EU:n jäsenvaltioissa. Tämän vuoksi joissakin maissa on erillisiä erityistietoja muista maista, ja niillä on myös eri tiedostomuoto raportointia varten.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvästä koulutuksesta on [Microsoft Learnissa](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Katso myös

[Intrastat-raportointi Business Centralissa](finance-how-report-intrastat.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
