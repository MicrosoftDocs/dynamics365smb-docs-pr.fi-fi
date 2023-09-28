---
title: Intrastat-raportoinnin määrittäminen
description: Opi tämän artikkelin avulla määrittämään Intrastat-raportointiominaisuudet ja raportoimaan muiden EU-maissa tai -alueilla toimivien yritysten kanssa käyty kauppa.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Intrastat-raportoinnin määrittäminen

Kaikkien Euroopan unionin (EU) alueen yritysten täytyy raportoida kaupastaan muiden EU-maiden/alueiden kanssa. Yritysten tulee raportoida tavaran liikkuminen kotimaan/-alueen tilastoviranomaisille kuukausittain ja raportti on toimitettava veroviranomaisille. Intrastat on järjestelmä, jolla kerätään kauppatilastoja tavaroista näissä maissa/alueilla. Intrastat-raportin avulla voit suorittaa jaksoittaisen Intrastat-raportoinnin, keräämisen, kirjaamisen ja raportoinnin kauppatavaran paikallisen lainsäädännön mukaisesti.

Intrastat-raportointi perustuu kaikkiin maihin ja alueisiin sovellettaviin EU-perussäädöksiin. Yksittäisten maiden ja alueiden välillä on kuitenkin eroja. Jokaisella maalla ja alueella on omat sääntönsä siitä, mitä ja miten raportoidaan.

> [!NOTE]
> Intrastat-tietoja ei sovelleta maiden ja alueiden välisten palvelujen siirtoon. Tiedot koskevat sen sijaan vain tavaroita, esimerkiksi nimikkeitä ja käyttöomaisuutta. Jos hallinto vaatii rekisteröimään palvelujen liikkumisen maiden ja alueiden välillä, se voidaan tehdä käyttämällä **Palveluilmoitus**-toimintoa.
>
> Tämä ominaisuus on saatavilla sovelluksena, jonka voit ladata [AppSourcesta](https://go.microsoft.com/fwlink/?linkid=2081646). Jos haluat käyttää tätä toimintoa, sinun on asennettava se **Laajennuksen hallinta** -sivulla.

> [!IMPORTANT]
> Tämä artikkeli kattaa uuden Intrastat-kokemuksen, joka on saatavilla [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman versiosta 21 lähtien. Ota yhteyttä järjestelmänvalvojaan ja ota selvää, mitä versiota yrityksesi käyttää ja pitääkö uudet toiminnot ottaa käyttöön.
>
> Lue edellisen version Intrastat-asetukset- ja käyttö-artikkeli kohdassa [Määritä ja raportoi Intrastat](finance-how-setup-report-intrastat-v20.md).

## Ota käyttöön uusi Intrastat-käyttökokemus

Vuoden 2022 2. julkaisuaallossa [!INCLUDE[prod_short](includes/prod_short.md)] sisältää uudelleensuunnitellun Intrastat-kokemuksen ja laajennettuja ominaisuuksia. Jos uusi Intrastat-toiminto ei ole käytössä ympäristössäsi, järjestelmänvalvoja voi ottaa sen käyttöön **Ominaisuuksien hallinta** -sivulla.

> [!IMPORTANT]
> Vanhaa ja uutta käyttökokemusta ei voi käyttää rinnakkain. Tämä ominaisuus kannattaa ottaa käyttöön ja testata eristysympäristössä tuotantotietojen kopiolla ennen laajennuksen aktivoimista tuotantoympäristössä. Kun uusi käyttäjäkokemus on aktivoitu tuotantoympäristössä, et voi palata takaisin vanhaan Intrastat-toimintoon.

1. Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false":::-kuvake, avaa **Ominaisuuksien hallinta** ja valitse sitten vastaava linkki.
2. Valitse **Ominaisuuksien hallinta** -sivulla **Ominaisuuspäivitys: Korvaa aiemmat Intrastat-toiminnot uudella Intrastat-laajennuksella** -rivi. Lisätietoja ominaisuuksien hallinnasta on kohdassa [Tulevien ominaisuuksien käyttöönotto etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).
3. Valitse **Ota käyttöön** -sarakkeessa **Kaikki käyttäjät**.
4. Lue selitys siitä, miten järjestelmä päivitetään, ja valitse **Kyllä** antaaksesi suostumuksesi.
5. Valitse **Seuraava**. Saat Intrastatin perusasetukset. Lue lisää Intrastat-asetuksista [Intrastat-määritys](#intrastat-configuration)-osiossa myöhemmin tässä artikkelissa.
6. Kun asetukset on määritetty, aloita uuden Intrastat-kokemuksen käyttö valitsemalla **Valmis**.

    > [!NOTE]
    > Yrityksen sijainnista riippuen yllä kuvatun ominaisuuden ottaminen käyttöön on riittävää. Jos mailla ja alueilla on erityistoimintoja Intrastat-raportointia varten, ota käyttöön päälaajennuksen lisäksi maa- tai aluekohtaiset Intrastat-sovellukset.

## Intrastatin määritys

Ennen kuin Intrastat-raportteja voi käyttää, on määritettävä useita konfiguraatioita.

### Intrastat-raportoinnin määrittäminen

**Intrastat-raportoinnin asetukset** -sivua käytetään Intrastat-raportoinnin käyttöönottoon ja sen oletustoiminnallisuuden määrittelyyn. Voit määrittää sen, tarvitseeko sinun raportoida Intrastat lähetyksistä (toimitukset), vastaanotoista (saapuvat) vai molemmista, riippuen paikallisten säädöksien rajoista. Voit myös määrittää oletusasetukset tapahtumatyypeille tavallisia ja palautusdokumentteja koskien, joita käytetään maksuliikenteen raportointiin.

Intrastat-raportoinnin määritys tehdään seuraavasti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-raportoinnin asetukset** ja valitse sitten vastaava linkki.
2. Valitse tai kirjoita **Yleiset**-pikavälilehden kenttien tiedot tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Seuraavassa taulukossa on kuvattu joitakin tärkeitä kenttiä.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Raportoi vastaanotot** | Määrittää, että vastaanotettujen tavaroiden saapuminen sisällytetään Intrastat-raportteihin. |
   | **Raportoi toimitukset** | Määrittää, että lähetettyjen nimikkeiden toimitukset sisällytetään Intrastat-raportteihin. |
   | **Sisällytä suoratoimitukset** | Määrittää, sisällytetäänkö suoratoimitustapahtumat Intrastat-raportteihin. Lisätietoja on kohdassa [Intrastat-raportoinnin käsitteleminen](finance-how-report-intrastat.md).  |  
   | **Lähetykset, joiden peruste on**  | Määrittää, minkä maakoodin perusteella Intrastat-raportin rivit määritetään.  |
   | **ALV-numero, jonka perusteena on** | Määrittää, minkä asiakas- tai toimittajakoodin perusteella Intrastat-raportin ALV-numero määritetään.  |
   | **Järjestelmään tallennettu yrityksen ALV-numero** | Määrittää, miten yrityksen ALV-rekisterinumero viedään Intrastat-tiedostoon.  |
   | **Järjestelmään tallennettu toimittajan ALV-numero** | Määrittää, miten toimittajan ALV-rekisterinumero viedään Intrastat-tiedostoon.  |
   | **Järjestelmään tallennettu asiakkaan ALV-numero** | Määrittää, miten asiakkaan ALV-rekisterinumero viedään Intrastat-tiedostoon.  |
   | **Hanki kumppanin ALV-tunnus** | Määrittää sen Intrastat-raportin rivin tyypin, josta kumppanin ALV-rekisterinumero päivitetään. Paikallisista vaatimuksista riippuen voit valita vain vastaanottorivit, vain toimitusrivit tai molemmat rivityypit. |

4. Valitse tai kirjoita **Oletustapahtumat**-pikavälilehden kenttien tiedot tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Seuraavassa taulukossa on kuvattu joitakin tärkeitä kenttiä.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Oletustapahtumatyyppi** | Määrittää säännöllisten myyntitoimitusten, huoltotoimitusten ja ostovastaanottojen oletustapahtumatyypin. |
   | **Oletustapahtumatyyppi – Palautukset** | Määrittää myyntipalautusten, huoltopalautusten ja ostopalautusten oletustapahtumatyypin. |
   | **Oletusarvoinen yksityishenkilön ALV-numero** | Määrittää yksityisen henkilön ALV-numeron, jos yksityishenkilöllä on oltava oma ALV-numero Intrastat-raportissa. |
   | **Oletusarvoinen kolmikantakaupan ALV-numero** | Määrittää oletusarvoisen kolmikantakaupan ALV-numeron siinä tapauksessa, että sinulla ei ole ALV-numeroa. |
   | **Oletusarvoinen tuntemattoman tilan ALV** | Määrittää oletusarvoisen ALV-numeron tuntemattomalle tilalle. |
   | **Oletusarvoinen maa-/aluekoodi** | Määrittää oletusarvoisen vastaanottomaan koodin. |

5. Valitse tai kirjoita **Raportointi**-pikavälilehden kenttien tiedot tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Seuraavassa taulukossa on kuvattu joitakin tärkeitä kenttiä.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Tiedonsiirtomäärityksen koodi** | Määrittää Intrastat-tiedoston luontiin käytettävän tiedonsiirtomäärityksen koodin. Tämä kenttä on käytettävissä vain, jos **Jaettujen vastaanottojen/toimitusten tiedostot** -kentän arvona on **Ei**. |
   | **Jaa Vastaanotot-/Toimitukset-tiedostot** | Määrittää, raportoidaanko vastaanotot ja toimitukset kahdessa erillisessä tiedostossa. |
   | **Zip-tiedostot** | Määrittää, lisätäänkö raporttitiedostot zip-tiedostoon. |
   | **Tiedonsiirtomäärityksen koodi – Vastaanotto** | Määrittää vastaanotettujen tavaroiden Intrastat-tiedoston luontiin käytettävän tiedonsiirtomäärityksen koodin. Tämä kenttä on käytettävissä vain, jos **Jaettujen vastaanottojen/toimitusten tiedostot** -kentän arvona on **Kyllä**. |
   | **Tiedonsiirtomäärityksen koodi – Toimitus** | Määrittää toimitettujen tavaroiden Intrastat-tiedoston luontiin käytettävän tiedonsiirtomäärityksen koodin. Tämä kenttä on käytettävissä vain, jos **Jaettujen vastaanottojen/toimitusten tiedostot** -kentän arvona on **Kyllä**. |

6. Määritä arvo **Numerointi**-pikavälilehdessä **Intrastat-nrot**-kenttään.

### Määritä raportointitiedosto

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Tiedonsiirtomääritykset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi** ja anna sitten **Yleiset**-pikavälilehdellä tiedonsiirron määritelmä, datatiedostotyyppi, sarake-erotin, liittyvät koodiyksiköt, XMLport ja muut kentät tarpeen mukaan.
3. Kuvaile **Rivimääritykset**-pikavälilehdessä datatiedoston rivien muotoilua täyttämällä kentät **Rivityyppi**-kenttään ja missä sinun täytyy määrittää tämän rivin sarakkeiden määrä.
4. Täytä **Sarakemääritykset**-pikavälilehden kunkin suunniteltujen sarakkeiden rivi. Voit määrittää sarakkeiden nimet, tietotyypit (kuten teksti, päivämäärä tai desimaaliluku), sarakkeen sisältävän kiinteäleveyksisen rivin pituuden, jos tiedoston tyyppi on *vakioteksti* ja joitakin muita parametreja.
5. Valitse **Rivimääritykset**-pikavälilehdessä **Kenttien linkitys**.
6. Luo uusi tapahtuma **Kentän linkitys** -sivulla. 
7. Valitse **Yleiset**-pikavälilehdessä **taulukon tunnuksen** arvo (valitse **Intrastat-raportin rivi** -kohdalle **4812**) ja lisää seuraavat kenttätiedot:

   1. Määritä avainindeksi, jota käytetään lähdetietueiden lajittelussa ennen vientiä, **Avainindeksi**-kentässä.
   2. Valitse arvo **Vastaava Codeunit** -kentässä.

8. Lisää **Kenttien vastaavuus** -pikavälilehdessä sarakkeet, jotka määritit aiemmin **Sarakemääritykset**-pikavälilehdessä, ja lisää sitten seuraavat kenttätiedot:

   1. Määritä kunkin sarakkeen **Kenttätunnus**-arvo.
   2. Määritä **Muunnossääntö**-arvo jokaiselle sarakkeelle tarvittaessa. Arvo määrittää säännön, joka muuntaa tuodun tekstin tuetuksi arvoksi ennen kuin se voidaan yhdistää määritettyyn kenttään [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Kun valitset arvon tässä kentässä, täsmälleen sama arvo syötetään **Muunnossääntö**-kenttään **tiedonvaihto-kentän kartoituspuskuri** taulukko. (Kun tarkka arvo syötetään **Muunnossääntö**-kenttään **tiedonvaihto-kentän vastaavuuspuskuri** -taulukossa, arvo valitaan tässä kentässä.)

9. Jos sinun täytyy ryhmitellä tapahtumia tiettyjen sarakkeiden perusteella, valitse **Kenttien ryhmittely** -pikavälilehdessä kentät, joita haluat käyttää ryhmittelemiseen.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] sisältää kaikkien lokalisoitujen maiden ja alueiden Intrastatin esimääritetyn tiedonvaihtomäärityksen. Lisätietoja uuden tiedonsiirtomäärityksen luomisesta tai muuttamisesta on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).

### Pakollisten kenttien määrittäminen Intrastat-raportin tarkistusluettelon avulla

Joissakin maissa ja joillakin alueilla viranomaiset vaativat Intrastat-raportteihin esimerkiksi ostojen toimitustavan tai joitakin arvoja myynnin ylittäessä tietyn raja-arvon.

Pakollisten kenttien tai arvojen määrittäminen **Intrastat-raportti**-sivulla tapahtuu seuraavasti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-raportoinnin asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Intrastat-raportin tarkistusluettelo**.
3. Lisää tarvittavat rivit tarkistusta varten noudattamalla seuraavia ohjeita:
   1. Määritä **Kentän nro** -kenttä kenttään, jonka arvon on oltava jokin muu kuin tyhjä.
   2. Täytä **Suodatinlauseke**-kenttään tarvittaessa arvo seuraavien sääntöjen perusteella:

        1. Kun avaat **Suodatinsivun**, valitse suodatin, jota haluat käyttää tarkistuksessa.
        2. Valitse arvo, joka liittyy valittuun suodattimeen.
        3. Jos sinun täytyy täyttää lisää suodattimia valitulle kentälle, lisää toinen suodatin toistamalla edelliset kaksi vaihetta.
        4. Kun olet määrittänyt valitun kentän suodattimet, valitse **OK**.

   3. Valitse **Käänteinen suodatinlauseke** -valintaruutu määrittääksesi, että kenttien tarkistus suoritetaan vain riveillä, jotka eivät vastaa suodatinlauseketta. Jos riviä ei ole suodatettu, tämä kenttä ohitetaan.

> [!NOTE]
> Kun avaat **suodatinsivun** **suodatinlauseke**-riviltä, voit käyttää kaikkia vakiosuodatuslausekkeita, jotka liittyvät suodatettavaan kenttään.
>
> Ole varovainen määrittäessäsi oikeellisuustarkistusääntöjä, koska ne voivat vaihdella maittain ja alueittain.

## Käytä mukautettuja codeunitseja Intrastat-raporteissa

Jos haluat muuttaa tapaa, jolla Intrastat toimii ja oletuskonfiguraatio ei riitä, voit mukauttaa järjestelmää laajentamalla vakio-ominaisuuksia. Jos sinun on muutettava Intrastat-käyttäytymistä, voit kehittää omia codeunitseja. Kun luot codeunitseja, sinun täytyy tehdä lisää muutoksia niiden käyttöön. Järjestelmän määrittäminen käyttämään omia objekteja tapahtuu seuraavasti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-raporttien määritys** ja valitse sitten liittyvä linkki.
2. Lisää uusi rivi **ALV-raporttien määritys** -sivulla.
3. Valitse **ALV-raportin tyyppi** -kentässä **Intrastat-raportti**.
4. **ALV-raportin versio** -kentässä määritetään raportin versio.
5. Lisää koodiyksiköt seuraaville vaihtoehdoille:
   1. Määrittele **Ehdota rivejä codeunit-tunnukseen** -kentässä uusi codeunit Intrastat-raporttirivien ehdottamista varten.
   2. Määritä **Sisällön codeunitin tunnus** -kentässä uusi codeunit tietojen viemistä varten tiedonsiirtomääritystä käyttämällä.
   3. Määrittele **Validoi codeunit-tunnus** -kentässä uusi codeunit Intrastat-raporttirivien ehdottamista varten.

> [!IMPORTANT]
> Tämän rivin on oltava tyhjä, jos käytät vakiocodeuniteja. Luo rivi ja määritä se vain, jos olet kehittänyt mukautettuja codeunitseja.

## Muut Intrastatin määritykset

Asiakas- ja toimittajakortit sisältävät **Intrastat-kumppanin tyyppi** -kentän, jolla on samat arvovaihtoehdot kuin **Kumppanin tyyppi** -kentällä: 

- "" (tyhjä)
- *Oma yritys*
- *Henkilö*
    
**Intrastat-kumppanin tyyppi** -kenttä on korvannut **Kumppanin tyyppi** -kentän Intrastat-raportoinnissa. **Kumppanin tyyppi** -kenttää käytetään yhtenäisen euromaksualueen (SEPA) määrittämiseen SEPA-suoraveloitusjärjestelmän (Core tai B2B) määrittämiseksi. **Intrastat-kumppanin tyyppiä** -kenttää käytetään vain Intrastat-raportoinnissa. Siksi voit tarpeen mukaan määrittää eri arvot näille kahdelle kentälle.

Jos **Intrastat-kumppanin tyyppi** -kenttä jätetään tyhjäksi, Intrastat-raportoinnissa käytetään **Kumppanin tyyppi** -kentän arvoa.

**Intrastat-raportin määritys**-, **Tiedonvaihtomääritykset**- ja **Intrastat-raportin tarkistusluettelo** -asetuksien lisäksi on määritettävä myös seuraavat asetukset.

| Sivu | Kuvaus |
| ---- | ----------- |
| **Maat/alueet** | **Maat/alueet**-sivulla sinun täytyy lisätä **EU-maa-/aluekoodi** ja **Intrastat-koodi**-tiedot määritelläksesi sen maan/alueen koodin, jonka kanssa käyt kauppaa. Näitä tietoja käytetään Intrastat-raportoinnissa. |
| **Tariffinumerot** | Monissa maissa ja monilla alueilla tulli- ja veroviranomaiset määrittävät kahdeksannumeroiset koodit eri nimikkeille. Jotta nimikkeen tapahtumat sisältäisivät tarvittavat tiedot ohjelman tuodessa ne Intrastat-ilmoituksen riville, sinun on syötettävä nimikekoodi **Tavaranimike**-sivulle. Etsi niiden nimikkeiden koodit, joilla yrityksesi käy kauppaa, ja syötä ne **Tavaranimikkeet**-sivulle. |
| **Kuljetusmuodot** | Intrastat-kuljetusmuodoilla on seitsemän yksimerkkistä koodia: **1** tarkoittaa merikuljetusta, **2** rautatiekuljetusta, **3** tiekuljetusta, **4** ilmakuljetusta, **5** postitusta, **7** kiinteää asennusta ja **9** omaa käyttövoimaa (kuten auton kuljettaminen sitä ajamalla). [!INCLUDE[prod_short](includes/prod_short.md)] ei vaadi näitä erityisiä koodeja. Suosituksena on kuitenkin käyttää merkitykseltään vastaavia kuvauksia. |
| **Kauppatapahtumien luonteet** | Mailla ja alueilla on eri koodit Intrastat-tapahtumatyypeille, kuten tavallisille ostoille ja myynneille, palautettujen tavaroiden vaihdolle ja palauttamattomien tavaroiden vaihdolle. Määritä omaa maata tai aluetta koskevat koodit. Näitä koodeja käytetään myynti-ja ostoasiakirjojen **Ulkomaankauppa**-pikavälilehdessä sekä palautusten käsittelyssä. |
| **Tapahtumamääritykset** | Määritä koodit, jotka täydentävät transaktiotyypin kuvauksia. |
  
> [!NOTE]
> Tammikuusta 2022 alkaen Intrastat edellyttää eri tapahtuman luonteen koodeja yksityishenkilöille tai ALV-rekisteröitymättömille yrityksille suunnatuille ja ALV-rekisteröityneille yrityksille osoitetuille toimituksille. Tämän vaatimuksen täyttämiseksi on suositeltavaa tarkistaa tapahtumien luonteiden koodit tai lisätä uusia sellaisia **Tapahtumien tyypit** -sivulle kulloisenkin maan vaatimusten mukaisesti. Lisäksi kannattaa tarkistaa ja päivittää **Intrastat-kumppanin tyyppi**-kenttä muotoon *Henkilö* asianomaisten asiakkaiden eli yksityishenkilöjen ja ALV-rekisteröimättömien yritysten **Asiakas**-sivulla. Jos et ole varma oikeasta Intrastat-kumppani- tai tapahtumatyypistä, suosittelemme, että pyydät samassa maassa tai samalla alueella asuvan asiantuntijan neuvoa.

|   Kenttä   |   Kuvaus   |
| --------- | --------------- |
| **Nettopaino** | Paino on eräs Intrastat-raportointiin liittyvistä perusmäärityksistä, koska kokonaispaino on pakollinen raportoinnissa. Jotta olisit valmis tämän vaatimuksen täyttämiseen, sinun täytyy täyttää nimikkeen tai käyttöomaisuuden kortin **Nettopaino**-kenttä. |
| **Alkuperämaan koodi** | Käytä kaksikirjaimisia ISO-alfakoodeja nimikkeelle tai käyttöomaisuuskortille sen maan tai alueen osalta, jossa tuote hankittiin tai tuotettiin. Jos tuotetta on tuotettu useammassa kuin yhdessä maassa tai yhdellä alueella, alkuperämaa- tai -alue on viimeinen merkittävän käsittelyn maa/alue. |
| **Tuontijäsenvaltion kumppanitoiminnan harjoittajan ALV-tunnistenumero** | Tämä on tuontijäsenvaltion kumppanitoiminnan harjoittajan ALV-tunnistenumero. ALV-tunnusta käytetään myös EU-maiden välisten vientitietojen vaihdossa jäsenvaltioiden kesken, ja sen avulla jäsenvaltiot voivat jakaa vastaanotetut tiedot oman maansa tai alueensa tuontiyritykselle. Raportointiyksiköiden on ilmoitettava sen yrityksen ALV-tunnus, joka on ilmoittanut unionin sisäisen tuotteiden hankinnan jäsenvaltiossa, johon tuote tuotiin. |

Myös seuraavat voi määrittää:

* **Kauppatavarakoodit**: Tulli- ja veroviranomaiset ovat luoneet nimikkeiden ja palvelujen luokittelua varten numeeriset koodit. Nämä koodit voidaan määrittää nimikkeissä.
* **Alueet**: Täydentäviä maita ja alueita koskevia tietoja.
* **Tulo-/ lähtöpaikat**: Määritä tämän vaihtoehdon avulla sijainnit, joissa lähetät nimikkeitä muihin maihin tai muille alueille tai vastaanotat nimikkeitä muista maista tai muilta alueilta. Lentoasema on esimerkki tulo- tai lähtöpaikasta. Tulo- tai lähtöpaikat annetaan myynti- ja ostoasiakirjoihin **Ulkomaankauppa**-pikavälilehdessä. Nämä tiedot kopioidaan nimiketapahtumista Intrastat-ilmoituksen luomisen yhteydessä.
* **Täydentävä mittayksikkö**: Intrastat-raportoinnissa käytettävä tavaroiden määrä voi olla joko nettopaino (kilogrammoina) tai lisäyksikkö. Jos tarvitaan lisäyksiköitä, ne on määritettävä nimikkeille ja käyttöomaisuudelle.

#### Kuljetusmuotojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuljetusmuodot** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kenttätiedot. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Kauppatapahtuman luonteen koodien määrittäminen

1. valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Tapahtumatyypit** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kenttätiedot. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Muut asiaan liittyvät määritykset

Ennen kuin käytät Intrastat-raportointiominaisuutta, sinun täytyy määrittää kentät nimikkeen, käyttöomaisuuden, asiakkaan ja toimittajan korteille.

#### Nimikekortit

Kaikkien Intrastatiin liittyvien tarvittavien tietojen määrittäminen nimikekortteihin tapahtuu seuraavasti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse kohde, jonka haluat määrittää.
3. Avaa **Kustannukset & kirjaus** -pikavälilehti ja täytä arvo **tavaranimikenumero**, **Lisämittayksikkö** sekä **Alkuperämaan/-alueen koodi** -kenttiin.

    > [!NOTE]
    > Jos haluat käyttää jotain mittayksikköä perusmittayksikön lisäksi, tämä lisämittayksikkö on määritettävä **Nimikkeen mittayksiköt** -sivulla.

4. Syötä **Varasto**-pikavälilehdellä desimaaliarvo **Nettopaino**-kenttään.

> [!NOTE]
> Kun lisäät tavaranumeron mittayksikölle, joka on määritelty nimikkeelle,  [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelma täyttää automaattisesti **Lisämittayksikkö**-kentän tavaranumerokonfiguraation perusteella. **Lisämittayksikkö**-kentän arvoa voi muuttaa tarpeen mukaan.

#### Määritä käyttöomaisuus Intrastatia varten

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jota haluat määrittää.
3. Täytä **Intrastat**-pikavälilehdellä **Tavaranimikenro**-, **Nettopaino**- ja **Lisämittayksikkö**-kentät.

> [!NOTE]
> Voit käyttää lisämittayksikkönä eri mittayksiköitä. Mutta minkä tahansa **Mittayksikön koodin** valitset, sen **Määrä** Intrastat-raporteissa on aina 1.

#### Toimittajien määrittäminen Intrastatia varten

Ennen kuin voit sisällyttää toimittajan Intrastat-raportointiin, syötä toimittajan tiedot  **Toimittajakortti**-sivulle. Voit esimerkiksi määrittää **Maa-/aluekoodi**-arvon ja **ALV-rekisterinumero**-arvon.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.
2. Valitse toimittaja, jonka haluat määrittää.
3. **Intrastat**-pikavälilehdessä voit määrittää oletusarvot **oletussiirtotyyppi**-, **oletussiirtotyyppi - palautukset** ja **oletuskuljetusmuoto** -kentille.
4. Valitse **maksut** -pikavälilehdellä **Intrastat-kumppanien tyyppi** -kentässä oleva valinta, jos haluat määrittää, onko toimittaja henkilö vai yritys Intrastat-raportoinnissa.

#### Asiakkaiden määritys Intrastatia varten

Ennen kuin voit sisällyttää asiakkaan Intrastat-raportointiin, syötä toimittajan tiedot **Asiakaskortti**-sivulle. Voit esimerkiksi määrittää **Maa-/aluekoodi**-arvon ja **ALV-rekisterinumero**-arvon.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas, jonka haluat määrittää.
3. **Intrastat**-pikavälilehdessä voit määrittää oletusarvot **oletussiirtotyyppi**-, **oletussiirtotyyppi - palautukset** ja **oletuskuljetusmuoto** -kentille.
4. Valitse **maksut** -pikavälilehdellä **Intrastat-kumppanien tyyppi** -kentässä oleva valinta, jos haluat määrittää, onko toimittaja henkilö vai yritys Intrastat-raportoinnissa.

#### Nimikkeiden ja käyttöomaisuuden jättäminen pois Intrastat-raportoinnista

Jos tietty nimike tai käyttöomaisuus jätetään pois Intrastat-raportoinnista, muuta kortissa olevaa asetusta merkitsemällä **Sulje pois Intrastat-raportista** -kenttä. Käytä tätä kenttää **Nimikemalli**-kortilla, kun haluat luoda lisää Intrastat-raportoinnin ulkopuolelle jääneitä nimikkeitä. 

##### Sulje nimike pois Intrastat-raportoinnista

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse nimike, jonka haluat määrittää, ja valitse sitten **Kustannus & kirjaus** -pikavälilehdessä **Poista Intrastat-raportista** -valintaruutu.

##### Käyttöomaisuuden jättäminen pois Intrastat-raportoinnista

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jota haluat määrittää.
3. Valitse **Intrastat**-pikavälilehdellä **Jätä pois Intrastat-raportista** -valintaruutu.

#### Tavaranimikkeiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tavaranimikkeet** ja valitse sitten vastaava linkki.  
2. Täytä **Tavaranimikkeet**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.

    | Kenttä | Kuvaus |  
    |-------|-------------|
    | **Nro** | Määrittää tavaranimikkeen. |
    | **Kuvaus** | Määrittää liittyvän tavaranimikkeen kuvauksen. |
    | **Lisäyksiköt** | Määrittää, edellyttävätkö tulli- ja veroviranomaiset tietoja tämän nimikkeen määrästä ja mittayksiköstä. |
    | **Muuntokerroin** | Määrittää tavaranimikkeen muuntokertoimen. |
    | **Mittayksikkö** | Määrittää tavaranimikkeen mittayksikön. |

> [!NOTE]
> Jos lisäät lisämittayksikön, [!INCLUDE [prod_short](includes/prod_short.md)] kysyy haluatko päivittää liittyvät nimikkeet. Jos päätät päivittää liittyvät nimikkeet, **Nimikkeen mittayksiköt** -sivun **Mittayksikkö**-arvo päivitetään kaikkien niiden nimikkeiden osalta, joilla on sama tavaranumero.
> 
> Kun lisäät nimikkeelle tavaranimikkeen, jonka **Mittayksikkö**-arvo on määritelty, [!INCLUDE [prod_short](includes/prod_short.md)] lisää uuden mittayksikön automaattisesti **Nimikkeen mittayksiköt** -arvoihin. **Määrä mittayksikköä kohti** -arvo perustuu **Määrän pyöristystarkkuus** -kenttään.

## Määritä maa- tai aluekohtaiset Intrastat-asetukset

Intrastat-vaatimukset ovat samanlaiset kaikissa EU:n jäsenvaltioissa, joskin tärkeitä poikkeuksia on olemassa. Teoriassa sääntöjä olisi sovellettava yhdenmukaisesti kaikissa jäsenvaltioissa. Täytäntöönpanossa on kuitenkin eroja, koska jotkin jäsenvaltiot antavat suuntaviivoja siitä, miten asetuksen periaatteita olisi sovellettava erityistilanteissa (esimerkiksi kaupalliset näytteet, tavaroiden palautus). Nämä suuntaviivat voivat johtaa erilaisiin tuloksiin eri tilanteissa. Sen vuoksi tiedot, jotka maiden tai alueiden on syötettävä, voivat vaihdella, kuten myös ne tiedostomuodot, joita niiden on käytettävä raportoinnissa.

### Itävalta

Itävallan Intrastat-raportointiin tarvitaan kaksi eri tiedostoa vastaanotoille ja toimituksille. Voit varmistaa, että asetukset ovat oikein, toimimalla seuraavasti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-raportoinnin asetukset** ja valitse sitten vastaava linkki.  
2. Tarkista **Raportointi**-pikavälilehdellä onko **jaettujen vastaanottojen/toimitusten tiedostot** valittuna. Jo se on, löydät kaksi erillistä **Tiedonsiirtomäärityksen koodi** -arvoa määritettynä. 
3. Tarkista, että **zip-tiedosto(-t)** -kenttä on valittuna sen varmistamiseksi, että raporttitiedostot lisätään zip-tiedostoon.

Intrastat-raporttien käsittelyprosessi on sama kuin yleisessä ominaisuudessa.

<!-- ### Belgium-->

### Tšekin tasavalta

Uusi Intrastat-raporttikokemus Tšekin tasavallalle on saatavilla 2023 julkaisuaalto 1 -versiossa. Tällä välin voit jatkaa **Intrastat-ilmoitus**-ominaisuuden käyttöä.

### Suomi

Intrastatin määrittämisessä on Suomessa muutamia lisävaiheita. Suomen Intrastat-raportointiin tarvitaan kaksi eri tiedostoa vastaanotoille ja toimituksille. Löydät myös kaksi erillistä **Tiedonsiirtomäärityksen koodi** -arvoa määritettynä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-raportoinnin asetukset** ja valitse sitten vastaava linkki.  
2. Täytä **Intrastat-ilmoituksen asetukset** -sivun **Tiedostojen asetukset** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.

    |                 Kenttä              |            Kuvaus                |  
    |------------------------------------|---------------------------------------|
    | **Tullikoodi** | Määrittää Intrastat-tiedoston määritystietojen mukautetun koodin. |
    | **Yrityksen sarjanro** | Määrittää Intrastat-tiedoston määritystietojen yrityksen sarjanumeron. |

3. Tarkista **Raportointi**-pikavälilehdellä onko **jaettujen vastaanottojen/toimitusten tiedostot** valittuna.

Intrastat-raporttien käsittelyprosessi on sama kuin yleisessä ominaisuudessa.

<!-- ### Germany-->

### Italia

Italian uusi Intrastat-raporttikokemus on saatavilla helmikuusta 2023 alkaen. Tällä välin voit jatkaa **Intrastat-ilmoitus**-ominaisuuden käyttöä.

<!-- ### France-->

### Ruotsi

Ruotsin Intrastat-raportointiin tarvitaan kaksi eri tiedostoa vastaanotoille ja toimituksille. Voit varmistaa, että asetukset ovat oikein, toimimalla seuraavasti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-raportoinnin asetukset** ja valitse sitten vastaava linkki.  
2. Tarkista **Raportointi**-pikavälilehdellä, että **Jaettujen vastaanottojen/toimitusten tiedostot** on valittuna. Jo se on, löydät kaksi erillistä **Tiedonsiirtomäärityksen koodi** -arvoa määritettynä.

Intrastat-raporttien käsittelyprosessi on sama kuin yleisessä ominaisuudessa.

<!-- ### United Kingdom-->

## Katso myös

[Intrastat-raportointi Business Centralissa](finance-how-report-intrastat.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
