---
title: Myynnin hallintatehtävien yleiskatsaus
description: 'Lue lisää Business Centralin palveluiden käytöstä asiakkaiden myynnin aktiviteettien hallintaan: esimerkkeinä myyntilaskut, tilaukset ja tarjoukset.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'trade, sell'
ms.search.form: '253,'
ms.date: 01/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="sales"></a>Myynti

Luo myyntilasku tai -tilaus tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla.

Myyntitilauksia on käytettävä, jos myyntiprosessi vaatii tilausmäärän osittaisen toimittamisen esimerkiksi silloin, kun koko määrä ei ole kerralla käytettävissä. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), myyntitilauksia on käytettävä. Kaikilta muilta osin myyntitilaukset toimivat samalla tavalla kuin myyntilaskut. Voit ilmoittaa tietyt toimituspäivät asiakkaille myyntitilauksissa Toimituksen lupaaminen -toiminnon avulla.  

Voit neuvotella asiakkaan kanssa luomalla ensin myyntitarjoukseen, jonka voit muuntaa myyntilaskuksi tai -tilaukseksi, kun hyväksyt myynnin. Kun asiakas on vahvistanut sopimuksen, voit lähettää tilausvahvistuksen ja tallentaa velvollisuutesi toimittaa tuotteet sovitusti.

Voit helposti korjata tai peruuttaa kirjatun myyntilaskun ennen kuin asiakas maksaa sen. Esimerkiksi kirjoitusvirheen korjaamiseksi tai jos asiakas pyytää muutosta tilausprosessin alkuvaiheessa. Jos kirjattu myyntilasku maksetaan, sinun on peruutettava myynti luomalla myyntihyvityslasku tai myyntipalautustilaus.

Tärkeintä hyvissä myynti- ja markkinointikäytännöissä on tehdä oikeita päätöksiä oikeaan aikaan. [!INCLUDE[prod_short](includes/prod_short.md)]in markkinointitoiminnot tarjoavat yhteystietojen yleiskuvauksen tarkasti ja oikea-aikaisesti, mikä tehostaa mahdollisten asiakkaiden palvelemista ja parantaa asiakastyytyväisyyttä. Lisätietoja on kohdassa [Suhteiden hallinta](marketing-relationship-management.md).

Jos käytät Microsoft Dynamics 365 Salesia asiakassuhteissa, voit nauttia saumattomasta integraatiosta liidistä tuottoon -prosessidds käyttämällä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa taustatoiminnoissa. Voit esimerkiksi käsitellä tilauksia, hallita varastoa ja hoitaa raha-asioita. Lue lisätietoja kohdasta [Dynamics 365 Salesin käyttäminen Business Centralista](marketing-integrate-dynamicscrm.md).

Liiketoimintaympäristöissä, joissa asiakkaan on maksettava ennen kuin tuotteet toimitetaan, kuten vähittäismyynti, sinun on odotettava maksukuittia ennen kuin toimitat tuotteet. Useimmissa tapauksissa saapuvia maksuja käsitellään joitakin viikkoja toimituksen jälkeen kohdistamalla maksut niihin liittyviin kirjattuihin ja maksamattomiin myyntilaskuihin. Lue lisätietoja kohdasta [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Myyntiasiakirjat voidaan lähettää sähköpostin liitteenä PDF-tiedostoina. Sähköpostin perusteksti sisältää otteen myyntiasiakirjasta. Ote voi sisältää esimerkiksi tuotteet, kokonaissumman ja PayPal-sivuston linkin. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostilla](ui-how-send-documents-email.md).

Voit sisällyttää hyväksynnän työnkulun kaikkiin myyntiprosesseihin. Hyväksynnän työnkulku voi esimerkiksi vaatia, että johtaja hyväksyy suuren myynnin tietyille asiakkaille. Lisätietoja on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).

Seuraavassa osissa kuvataan tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

## <a name="get-started-with-sales-capabilities"></a>Myyntiominaisuuksien käytön aloittaminen

Ennen kuin myyt, määritä, miten haluat hallita yrityksesi myyntiprosesseja.

|Vastaanottaja...| Katso |
|---|---|
| Luo asiakkaan kortti jokaiselle asiakkaalle, jolle myyt.|[Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md) |
| Määritä, miten myynnit hoidetaan, esimerkiksi hinnat ja alennukset, asiakkaan hinta- ja alennusryhmät, myyjät, toimitusehdot ja agentit. | [Myynnin määrittäminen](sales-setup-sales.md) |

## <a name="sales-analytics"></a>Myynnin analyysi

Tässä osassa kuvataan analyysityökaluja, joita voit käyttää, kun haluat saada myyntitietoja.

| Vastaanottaja... | Katso |
| --- | --- |
| Tutustu myyntitietojen analysointimahdollisuuksiin. | [Myynnin analyysin yleiskatsaus](sales-analytics-overview.md) |
| Tee myyntitietojen ad-hoc-analyysi suoraan luettelosivuilla ja kyselyissä. | [Myynnin analyysiraporttien luominen](bi-how-create-analysis-views-reports.md) |
| Tutustu valmiisiin myyntiraportteihin. | [Valmiit myyntiraportit](sales-reports.md) |

## <a name="quote-to-order-to-sales-invoice"></a>Tarjouksesta tilaukseen ja myyntilaskuun

Seuraavassa taulukossa kuvataan, miten yksinkertaisia myyntiprosesseja käytetään.

|Vastaanottaja...| Katso |
|---|---|
| Luo myyntitarjous, jos tarjoat tuotteita siirtokelpoisilla ehdoilla ennen tarjouksen muuntamista myyntilaskuksi. |[Myyntitarjousten tekeminen](sales-how-make-offers.md) |
| Käsittele myyntitilaus (ehkä osittaisella toimituksella tai suoratoimituksella.) |[Tuotteiden myyminen](sales-how-sell-products.md) |
| Luot myyntilaskun tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla. |[Lasku – myynti](sales-how-invoice-sales.md) |
|Tietoja siitä, mitä tapahtuu myyntiasiakirjoja kirjattaessa.|[Myynnin kirjaaminen](ui-post-sales.md)|

Jos tarvitset monimutkaisempia myyntiprosesseja, seuraavassa taulukossa on luettelo artikkeleista, joissa kerrotaan, miten voit tehdä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmalla.

|Vastaanottaja...| Katso |
|---|---|
| Toteuta myyntitilaus, jossa on useita osittaisia toimituksia. | [Osittaisten toimitusten prosessointi](sales-how-send-partial-shipments.md) |
| Määritä vakiomyynti- tai -ostorivit, jotka voit lisätä nopeasti asiakirjoihin, kuten toistuviin täydennystilauksiin.|[Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md)|  
|Voit hallita asiakkaan suurta määrää koskevaa ostositoumusta, joka toimitetaan useassa erässä tietyn ajan kuluessa.|[Puitemyyntitilausten käyttäminen](sales-how-to-create-blanket-sales-orders.md)|
|Laskuta asiakasta vain kerran yhdistämällä useiden toimitusten toimitukset yhteen laskuun.|[Toimitusten yhdistäminen yhteen laskuun](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Sellaiset kokoonpanon nimikkeet, jotka eivät ole tällä hetkellä saatavana, myydään luomalla linkitetty kokoonpanotilaus. Kokoonpanotilaus voi toimittaa myyntitilauksen koko tai osittaisen määrän.|[Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md)|

## <a name="pick-and-ship"></a>Poiminta ja lähettäminen

Seuraavassa taulukossa kuvataan, miten myyntitilauksen nimikkeitä poimitaan ja toimitetaan asiakkaalle.

| Vastaanottaja | Katso |
| --- | --- |
|Valmistaudu poimimaan lähetettäviä nimikkeitä.|[Poimintaluettelon tulostaminen](sales-how-print-picking-list.md)|
| Linkitä myyntitilaus ostotilaukseen, jotta voit myydä suoratoimituksen nimikkeen, joka toimitetaan suoraan toimittajaltasi asiakkaallesi. |[Suoratoimitusten tekeminen](sales-how-drop-shipment.md) |
|Luettelonimike on toimitettava toimittajalta fyysiseen varastoon, jotta voit toimittaa nimikkeen asiakkaallesi.|[Erikoistilausten luominen](sales-how-to-create-special-orders.md)|
|Ilmoitta tilauksen toimiaika asiakkaille laskemalla joko mahdollinen luvattavaksi- tai luvattavissa -päivämäärä.|[Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)|
| Tutustu, miten kollia seurataan kirjatusta myyntitoimituksesta. | [Pakettien seuraaminen](sales-how-track-packages.md) |

## <a name="canceled-orders-refunds-and-returns"></a>Peruutetut tilaukset, hyvitykset ja palautukset

Seuraavassa taulukossa kuvataan, miten peruutettuja tilauksia, hyvityksiä ja palautuksia käsitellään.

| Vastaanottaja | Katso |
| --- | --- |
| Suorita toiminto maksamattomalle kirjatulle myyntilaskulle hyvityslaskun automaattiseksi luomiseksi ja joko peruuta myyntilasku tai luo se uudelleen, jotta voit tehdä korjauksia. |[Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md) |
| Luo myyntihyvityslasku palauttamaan tietty kirjattu myyntilasku siten, että vastaa asiakaspalautuksen tuotteita ja hyvitettävää summaa. |[Myyntipalautusten tai -peruutusten käsittely](sales-how-process-sales-returns-cancellations.md) |

## <a name="other-processes-in-sales"></a>Muut myyntiprosessit

Seuraavassa taulukossa kuvataan, miten muita myyntiprosesseja käytetään.

| Vastaanottaja | Katso |
| --- | --- |
|Ratkaise ristiriita, kun samalla asiakkaalla on ainakin kaksi tietuetta.|[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)|

## <a name="see-also"></a>Katso myös

[Myynnin määrittäminen](sales-setup-sales.md)  
[Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md)  
[Myynnin analyysin yleiskatsaus](sales-analytics-overview.md)   
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Yrityksen yleiset toiminnot](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
