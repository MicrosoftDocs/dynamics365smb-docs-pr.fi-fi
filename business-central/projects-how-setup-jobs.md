---
title: 'Projektien, hintojen ja projektin kirjausryhmien määrittäminen'
description: Tietoja töiden yleistietojen luomisesta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Projektien, hintojen ja projektin kirjausryhmien määrittäminen

Määrität projektipäällikkönä projektit, jotka määrittävät jokaisen [!INCLUDE[prod_short](includes/prod_short.md)]issa hallittavan projektin. **Töiden asetukset** -sivulla voit määrittää, miten työominaisuuksia käytetään.

Määrittele eri tiedot jokaiselle työlle:

* Projektinimikkeiden hinnat
* Projektiresurssit
* Projektin kirjanpitotilit
* Projektin kirjausryhmät (pakollinen)

## <a name="to-set-general-information-for-jobs"></a>Projektien yleistietojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektienhallinnan asetukset** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> **Käytä käyttölinkkiä oletusarvoisesti** -valinta **Projektimääritys**-sivulla osoittaa, onko projektitapahtumat linkitetty projektin suunnitteluriveihin oletusarvoisesti. Ota tämä asetus käyttöön kaikissa uusissa projekteissa ottamalla vaihto käyttöön. Voit ottaa käyttöön tai poistaa käytöstä projektin käytön seurannan tietylle projektille ottamalla käyttöön tai poistamalla **Käytä käyttölinkkiä** **Työkortti**-sivulla.

### <a name="to-set-up-job-usage-tracking"></a>Projektin käytön seurannan määrittäminen

Kun työskentelet projektin parissa, haluat ehkä tietää, miten käyttöäsi seurataan suunnitelmaasi. Voit tutkia käyttöä luomalla linkin työsuunnittelurivien ja toteutuneen käytön välille. Linkin avulla voit seurata kustannuksia ja selvittää, kuinka paljon työtä on jäljellä. Oletusarvon mukaan työn suunnittelurivin tyyppi on **Budjetti**, mutta käyttämällä rivin tyyppiä **Sekä budjetti että laskutettava** on samanlainen vaikutus.

Kun olet määrität käytön seurannan valitsemalla **Käytä käyttölinkkiä oletusarvoisesti** -valinnan, voit tarkastella tietoja projektin suunnittelurivillä. Voit esimerkiksi määrittää resurssin, nimikkeen tai kirjanpitotilin määrän. Voit myös määrittää projektipäiväkirjaan siirrettävän määrän. Projektin suunnittelurivin **Jäljellä oleva määrä** -kenttä osoittaa projektipäiväkirjaan siirrettävän ja kirjattavan jäljellä olevan määrän.

>[!NOTE]
> Jos projektin **Käytä käyttölinkkiä** -valintaruutu on valittu ja päiväkirjarivin **Rivityyppi**-kenttä tai ostorivi on **Laskutettava**, **sekä budjetti että laskutettava**-tyyppiset projektin uudet suunnittelurivit luodaan projektipäiväkirjan tai ostoasiakirjan kirjaamisen yhteydessä.  
>
> Lisätietoja on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md) ja [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Jos et määritä projektipäiväkirjarivin tai ostorivin **Rivityyppi**-kentän arvoa, projektin suunnittelurivejä ei luoda, kun projektipäiväkirja tai ostoasiakirja kirjataan.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>Hintojen määrittäminen töiden nimikkeille, resursseille ja KP-tileille

> [!NOTE]
> Vuoden 2020 julkaisuaallossa 2 julkaisimme uudet prosessit hintojen ja alennusten määritykseen ja hallintaan. Jos olet uusi asiakas, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttöokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

Voit määrittää hintoja työhön liittyville nimikkeille, resursseille ja KP-tileille. 

#### [Nykyinen kokemus](#tab/current-experience)

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse projekti ja valitse sitten **Resurssi**- **Nimike**- tai **KP-tili**-toiminto.
3. Täytä **Projektiresurssien hinnat**-, **Projektinimikkeiden hinnat**- tai **Projektin kirjanpitotilin hinnat** -sivulla tarvittavat kentät.

Kun projektille valitaan resurssi, nimike tai kirjanpitotili, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää projektin suunnitelmarivien ja projektipäiväkirjojen valinnaisten kenttien tietoja. Seuraavassa taulukossa kuvataan, miten.

|Sarake1  |Sarake2  |
|---------|---------|
|**Projektiresurssit**|**Projektitehtävänro**-, **Työtyyppi**-, **Valuuttakoodi**-, **Rivialennus-%**- ja **Yksikkökustannustekijä**-kentät. Resurssin **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun resurssi tai resurssiryhmään liitetty resurssi määritetään. Tämä hinta ohittaa **Resurssihinta / resurssiryhmän hinta** -sivulla määritetyt hinnat.|
|**Projektinimikkeet**|**Projektitehtävänro**-, **Valuuttakoodi**- ja **Rivialennus-%**-kentät. Nimikkeen **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa tämän nimikkeen syöttämisen yhteydessä. Tämä hinta ohittaa nimikkeiden normaalin asiakashinnan (parhaan hinnan mekanismi). Jos haluat käyttää tavallista asiakashintaa, älä määrittele projektin projektinimikkeiden hintoja.|
|**Kirjanpitotilit**|**Projektitehtävän nro**-, **Valuutan koodi**-, **Rivialennus-%**-, **Yksikkökustannustekijä**- ja **Yksikkökustannus**-kentän tietoja käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun tämä kirjapitotili syötetään ja lisätään projektiin. Kun valitset pääkirjanpitotilin, projektin suunnittelurivit ja projektipäiväkirjat käyttävät **Yksikköhinta**-kentän arvoa pääkirjan työkuluille.|

#### [Uusi kokemus](#tab/new-experience)

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse soveltuva projekti ja valitse sitten **Myyntihinnastot**-toiminto.

---

## <a name="to-set-up-job-posting-groups"></a>Projektin kirjausryhmien määrittäminen

Yksi näkökulma projektien suunnittelussa on sen päättäminen, mitä kirjaustilejä projektin kustannuslaskentaan käytetään. Projektien kirjaus edellyttää, että määrität kullekin projektin kirjausryhmälle tilit kirjausta varten. Kirjausryhmä edustaa linkkiä työn ja sen kirjanpitokäsittelyn välillä. Kun luot työn, määrität kirjausryhmän ja oletusarvon mukaan jokainen tehtävä, jonka luot työlle, liittyy kyseiseen kirjausryhmään. Voit kuitenkin ohittaa oletusarvon tehtävien luonnin yhteydessä ja valita sopivamman kirjausryhmän.  

> [!NOTE]  
> Sinun tulee määrittää tilit tilikartassa ennen kirjausryhmien määrittämistä. Lisätietoja on kohdassa [Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

| Summakentät | Kuvaus |
| --- | --- |
| **Koodi** |Tunniste kirjausryhmää varten. Voit kirjoittaa enintään 10 merkkiä (välilyönnit mukaan lukien). |
| **KET-kustannusten tili** |Projektin keskeneräisen työn laskettujen kustannusten KET-tili, joka on käyttöomaisuuden tasetili. |
| **Kertyneiden KET-kustannusten tili** |KET-laskennan kustannusarvon tai myynnin kustannusten tili. Tämä tili kattaa taseesi kertyneet siirtovelat. Kun KET-oikaisu edellyttää, että lisäät tuloslaskelmaan kirjattavia käyttökustannuksia, kirjaat tälle tilille. |
| **Projektin kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. |
| **Nimikkeiden kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. |
| **Resurssien kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. |
| **Kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. |
| **Projektin kustannusten muutostili** |Kertyneiden KET-kustannusten tilin vastatili, joka on kustannustili. |
| **Kirjanpidon kustannustili (budjetti)** |Tässä kentässä on myyntitili, jota käytetään tämän kirjausryhmän projektitehtävien kirjanpitokustannuksille. Jos kenttä on tyhjä, ohjelma käyttää projektin suunnittelurivillä määritettyä kirjanpitotiliä. |
| **Kertyneen KET-myynnin tili** |Keskeneräisen työn lasketun myyntiarvon KET-tili, joka on taseen kertyneen tuoton tili. Kun KET-oikaisu edellyttää kirjattujen tulojen lisäämistä, kirjaat tälle tilille. |
| **Laskutetun KET-myynnin tili** |Keskeneräisen työn sen laskutetun myyntiarvon tili, jota ei voi tulouttaa. Tämä on taseen ansaitsemattoman tuoton tili. |
| **Projektin myynnin kohdistuksen tili** |Laskutetun KET-myynnin tilin vastatili, joka on tuottotilin vastatili. |
| **Projektin myynnin muutostili** |KET-myyntitilin vastatili, joka on tuottotili. |
| **Tuloutettujen kustannusten tili** |Kustannustili, joka sisältää projektin tuloutetut kustannukset. Yleensä tili on debetkustannustili. |
| **Tuloutetun myynnin tili** |Tulotili, joka sisältää projektin tuloutetut tuotot. Yleensä tili on kredittulotili. |

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/set-up-jobs-resources/)

## <a name="see-also"></a>Katso myös

[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Video: Projektin luonti Dynamics 365 Business Centralissa](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projektien hallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
