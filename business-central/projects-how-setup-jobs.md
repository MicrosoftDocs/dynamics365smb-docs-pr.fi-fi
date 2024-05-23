---
title: 'Projektien, hintojen ja projektin kirjausryhmien määrittäminen'
description: Tietoja projektien yleistietojen luomisesta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# Projektien, hintojen ja projektin kirjausryhmien määrittäminen

Projektipäällikkö määrittää projektit, jotka määrittävät jokaisen [!INCLUDE[prod_short](includes/prod_short.md)]issa hallittavan projektin. **Projektiasetukset**-sivulla voidaan määrittää, miten projektiominaisuuksia käytetään.

Kullekin projektille määritetään monenlaisia tietoja:

* Projektinimikkeiden hinnat
* Projektien resurssit
* Projektin kirjanpitotilit
* Projektin kirjausryhmät (pakollinen)

## Projektien yleistietojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektiasetukset** ja valitse sitten sopiva linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> **Käytä käyttölinkkiä oletusarvoisesti** -valinta **Projektiasetukset**-sivulla ilmaisee, onko projektitapahtumat linkitetty projektin suunnitteluriveihin oletusarvoisesti. Tämä asetus otetaan vaihtopainikkeella käyttöön kaikissa uusissa projekteissa. Tietyn projektin projektin käytön seuranta voidaan ottaa käyttöön tai poistaa käytöstä **Projektikortti**-sivun **Käytä käyttölinkkiä** -vaihtopainikkeella.

### Projektin nimikkeiden oletussijainnin määrittäminen

Tietojen syöttämisessä säästyy aikaa, kun projektien oletussijainti ja -varastopaikka määritetään **Projektikortti**-sivulla. Oletussijainti ja -varastopaikka määritetään automaattisesti, kun projektin tehtäviä, projektin suunnittelurivejä ja projektipäiväkirjan rivejä luodaan projektille. Sijaintikoodia ja varastopaikkaa voidaan kuitenkin tarvittaessa muuttaa tehtävissä ja riveillä.

Jos **Projektin valmisteluvarastopaikkakoodiin** määritetään sijainnissa, valmisteluvarastopaikkakoodi täytetään, kun sijaintikoodi valitaan. Jos varastotyönkulku edellyttää varastopoimintoja, nimikkeiden kuluttamista varten voidaan määrittää myös muita varastopaikkoja.

Nämä kentät ovat oletuksia projektitehtäviä luotaessa. Aiemmin luodut projektitehtävät eivät muutu.

Seuraavat seikat on otettava oletussijainteja käytettäessä huomioon:

* Jos projektitehtävissä määritetään **Projektin valmisteluvarastopaikkakoodiin** määritetään sijainnissa, varastopaikkakoodi määritetään, kun sijaintikoodi valitaan. Jos varastotyönkulku edellyttää varastopoimintoja, nimikkeiden kuluttamista varten voidaan määrittää myös muita varastopaikkoja.
* Projektin suunnitteluriveillä **sijaintikoodi** perustuu projektin suunnittelurivillä nimikettä valittaessa valittuun arvoon. Jos projektitehtävälle ei määritetä varastopaikkakoodia, varastopaikka valitaan oletusvarastopaikkasisällöstä. Kumpikin arvo voidaan muuttaa manuaalisesti.
* Projektipäiväkirjan riveillä **sijaintikoodi** perustuu projektipäiväkirjan rivillä nimikettä valittaessa valittuun arvoon. Jos projektitehtävälle ei määritetä varastopaikkakoodia, varastopaikka valitaan oletusvarastopaikkasisällöstä. Kumpikin arvo voidaan muuttaa manuaalisesti.

### Useiden asiakkaiden laskuttaminen projektitehtävien osalta 

Jos projekteissa on useita asiakkaita, oikean tehtävän laskuttaminen oikealta asiakkaalta voi olla haastavaa. [!INCLUDE [prod_short](includes/prod_short.md)] yksinkertaistaa laskutusta mahdollistamalla laskutus- ja tilausasiakkaiden määrittämisen kullakin projektitehtävärivillä, joten laskut voidaan luoda automaattisesti oikeille asiakkaille. Lisätietoja useiden asiakkaiden laskuttamisesta on kohdassa [Projektitehtävien laskuttaminen yhdeltä tai usealta asiakkaalta](projects-how-create-jobs.md#invoice-one-or-more-customers-for-project-tasks).

### Projektin käytön seurannan määrittäminen

Kun työskentelet projektin parissa, haluat ehkä tietää, miten käyttöäsi seurataan suunnitelman perusteella. Käyttöön voi perehtyä luomalla linkki projektin suunnittelurivien ja toteutuneen käytön välille. Linkin avulla voit seurata kustannuksia ja selvittää, kuinka paljon työtä on jäljellä. Oletusarvoisesti projektin suunnittelurivin tyyppi on **Budjetti**, mutta rivintyypin **Sekä budjetti että laskutettava** käytöllä on samanlainen vaikutus.

Kun käytön seuranta on määritetty ottamalla **Käytä käyttölinkkiä oletusarvoisesti** käyttöön vaihtopainikkeella, tietoja voi tarkastella projektin suunnittelurivillä. Voit esimerkiksi määrittää resurssin, nimikkeen tai kirjanpitotilin määrän. Voit myös määrittää projektipäiväkirjaan siirrettävän määrän. Projektin suunnittelurivin **Jäljellä oleva määrä** -kenttä ilmaisee projektipäiväkirjaan siirrettävän ja kirjattavan jäljellä olevan määrän.

>[!NOTE]
> Jos projektin **Käytä käyttölinkkiä** -valintaruutu on valittu ja projektipäiväkirjarivin **Rivityyppi**-kenttä tai ostorivi on **Laskutettava**, **Sekä budjetti että laskutettava** -tyyppiset projektin uudet suunnittelurivit luodaan projektipäiväkirjan tai ostoasiakirjan kirjaamisen yhteydessä.  
>
> Lisätietoja on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md) ja [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Jos projektipäiväkirjarivin tai ostorivin **Rivityyppi**-kentän arvoa ei määritetä, projektin suunnittelurivejä ei luoda, kun projektipäiväkirja tai ostoasiakirja kirjataan.

## Hintojen määrittäminen töiden projekteille, resursseille ja KP-tileille

> [!NOTE]
> Vuoden 2020 julkaisuaallossa 2 julkaisimme uudet prosessit hintojen ja alennusten määritykseen ja hallintaan. Jos olet uusi asiakas, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttöokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

Hinnat voidaan määrittää projektiin liittyville nimikkeille, resursseille ja KP-tileille. 

#### [Nykyinen kokemus](#tab/current-experience)

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Valitse projekti ja valitse sitten **Resurssi**- **Nimike**- tai **KP-tili**-toiminto.
3. Täytä **Projektiresurssien hinnat**-, **Projektinimikkeiden hinnat**- tai **Projektin kirjanpitotilin hinnat** -sivulla tarvittavat kentät.

Kun projektille valitaan resurssi, nimike tai kirjanpitotili, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää projektin suunnitelmarivien ja projektipäiväkirjojen valinnaisten kenttien tietoja. Seuraavassa taulukossa kuvataan, miten.

|Sarake1  |Sarake2  |
|---------|---------|
|**Projektin resurssit**|**Projektitehtävän nro**-, **Työtyyppi**-, **Valuuttakoodi**-, **Rivialennus-%**- ja **Yksikkökustannustekijä**-kentät. Resurssin **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun resurssi tai resurssiryhmään liitetty resurssi määritetään. Tämä hinta ohittaa **Resurssihinta / resurssiryhmän hinta** -sivulla määritetyt hinnat.|
|**Projektinimikkeet**|**Projektitehtävän nro**-, **Valuuttakoodi**- ja **Rivialennus-%**-kentät. Nimikkeen **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa tämän nimikkeen syöttämisen yhteydessä. Tämä hinta ohittaa nimikkeiden normaalin asiakashinnan (parhaan hinnan mekanismi). Jos haluat käyttää tavallista asiakashintaa, älä määritä projektin projektinimikkeiden hintoja.|
|**Kirjanpitotilit**|**Projektitehtävän nro**-, **Valuutan koodi**-, **Rivialennus-%**-, **Yksikkökustannustekijä**- ja **Yksikkökustannus**-kentän tietoja käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun tämä kirjapitotili syötetään ja lisätään projektiin. Kun valitset pääkirjanpitotilin, projektin suunnittelurivit ja projektipäiväkirjat käyttävät **Yksikköhinta**-kentän arvoa pääkirjapidon projektikuluina.|

#### [Uusi kokemus](#tab/new-experience)

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Valitse soveltuva projekti ja valitse sitten **Myyntihinnastot**-toiminto.

---

## Projektin kirjausryhmien määrittäminen

Yksi osa projektien suunnittelua on sen päättäminen, mitä kirjaustilejä projektin kustannuslaskentaan käytetään. Projektien kirjaus edellyttää, että määrität kullekin projektin kirjausryhmälle tilit kirjausta varten. Kirjausryhmä ilmaisee projektin ja sen kirjanpitokäsittelyn välisen linkin. Kun projekti luodaan, kirjausryhmä määritetään ja oletusarvoisesti kunkin projektiin luotava tehtävä liitetään kyseiseen kirjausryhmään. Voit kuitenkin ohittaa oletusarvon tehtävien luonnin yhteydessä ja valita sopivamman kirjausryhmän.  

> [!NOTE]  
> Sinun tulee määrittää tilit tilikartassa ennen kirjausryhmien määrittämistä. Lisätietoja on kohdassa [Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md).  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin kirjausryhmät** ja valitse sitten sopiva linkki.  
2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

| Summakentät | Kuvaus | Käytetty KET-tyypissä |
| --- | --- |  --- |
| **Koodi** |Tunniste kirjausryhmää varten. Voit kirjoittaa enintään 10 merkkiä (välilyönnit mukaan lukien). | |
| **KET-kustannusten tili** |Projektin keskeneräisen työn laskettujen kustannusten KET-tili, joka on käyttöomaisuuden tasetili. | Sovellettu kustannus, kirjatut kustannukset|
| **Kertyneiden KET-kustannusten tili** |KET-laskennan kustannusarvon tai myynnin kustannusten tili. Tämä tili kattaa taseesi kertyneet siirtovelat. Kun KET-oikaisu edellyttää, että lisäät tuloslaskelmaan kirjattavia käyttökustannuksia, kirjaat tälle tilille. | Kertyneet kustannukset|
| **Projektin kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. Käytetään, kun **käytetty KET-kirjaustapa** on *Projekti* . | Sovelletut kustannukset, kirjatut kustannukset|
| **Nimikkeiden kohdistettujen kustannusten tili** |Sama kuin **Projektin kohdistettujen kustannusten tili** mutta käytetään, kun **Käytetty KET-kirjausmenetelmä** -arvoksi on määritetty *Projektitapahtuma*.| |
| **Resurssien kohdistettujen kustannusten tili** |Sama kuin **Projektin kohdistettujen kustannusten tili** mutta käytetään, kun **Käytetty KET-kirjausmenetelmä** -arvoksi on määritetty *Projektitapahtuma*.| |
| **KP-kustannusten kohdistettujen kustannusten tili** |Sama kuin **Projektin kohdistettujen kustannusten tili** mutta käytetään, kun **Käytetty KET-kirjausmenetelmä** -arvoksi on määritetty *Projektitapahtuma*.| |
| **Projektin hinnan muutostili** |Kertyneiden KET-kustannusten tilin vastatili, joka on kustannustili. | Kertyneet kustannukset|
| **Kirjanpidon kustannustili (budjetti)** |Tässä kentässä on myyntitili, jota käytetään tämän kirjausryhmän projektitehtävien kirjanpitokustannuksille. Jos kenttä on tyhjä, projektin suunnitteluriville syötettyä kirjanpitotiliä käytetään. | |
| **Kertyneen KET-myynnin tili** |Keskeneräisen työn lasketun myyntiarvon KET-tili, joka on taseen kertyneen tuoton tili. Kun KET-oikaisu edellyttää kirjattujen tulojen lisäämistä, kirjaat tälle tilille. | Kertyneet myynnit, kirjatut myynnit|
| **Laskutetun KET-myynnin tili** |Keskeneräisen työn sen laskutetun myyntiarvon tili, jota ei voi tulouttaa. Tämä on taseen ansaitsemattoman tuoton tili. | Kirjatut myynnit, sovelletut myynnit|
| **Projektin kohdistettujen myyntien tili** |Laskutetun KET-myynnin tilin vastatili, joka on tuottotilin vastatili. | Sovelletut myynnit, kirjatut myynnit|
| **Projektin myynnin muutostili** |KET-projektin myyntitilin vastatili, joka on tuottotili. | Kertynyt myynti|
| **Tuloutettujen kustannusten tili** |Kustannustili, joka sisältää projektin tuloutetut kustannukset. Yleensä tili on debetkustannustili. | Tuloutetut kustannukset|
| **Tuloutetun myynnin tili** |Tulotili, joka sisältää projektin tuloutetut tuotot. Yleensä tili on kredittulotili. | Tuloutettu myynti|

## Katso myös

[Projektienhallinnan määrittäminen](projects-setup-projects.md)  
[Video: Projektin luonti Dynamics 365 Business Centralissa](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projektien hallinta](projects-manage-projects.md)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
