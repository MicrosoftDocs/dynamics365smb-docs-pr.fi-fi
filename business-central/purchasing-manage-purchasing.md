---
title: Ostojen hallintatehtävien yleiskatsaus
description: Ohjeaiheessa kerrotaan osto- tai hankintaprosessien hallinnasta ja selitetään muun muassa ostolaskujen ja -tilausten käyttöä.
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Ostaminen

Voit luoda ostolaskun tai -tilauksen ostojen kustannusten tallentamiseksi ja ostoreskontran seuraamiseksi. Jos haluat hallita varastoa, myös ostolaskuja käytetään varastotasojen dynaamiseen päivittämiseen, jotta voit minimoida varaston kustannukset ja tarjota parempaa asiakaspalvelua. Ostokustannukset, sisältäen palvelukulut ja varastoarvot, jotka aiheutuvat tiliöinnin ostolaskuista, vaikuttavat voittolukuihin ja muihin talouden KPI:hin roolikeskuksessasi.

Ostotilauksia on käytettävä, jos ostoprosessi vaatii tilausmäärän osittaisten vastaanottojen tallentamisen esimerkiksi silloin, kun koko määrä ei ole kerralla toimittajan käytettävissä. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), ostotilauksia on käytettävä. Lisätietoja on kohdassa [Suoratoimitusten tekeminen](sales-how-drop-shipment.md). Kaikilta muilta osin ostotilaukset toimivat samalla tavalla kuin ostolaskut.

Ostolaskut voidaan luoda automaattisesti käyttämällä OCR (Optical Character Recognition) -palvelua toimittajien PDF-laskujen muuntamisessa sähköisiksi asiakirjoiksi, jotka työnkulku puolestaan muuntaa ostolaskuiksi. Voit käyttää tätä toimintoa rekisteröitymällä ensin OCR-palveluun ja määrittämällä sitten asetukset. Lisätietoja on kohdassa [Saapuvat asiakirjat](across-income-documents.md).

Tuotteet voivat olla sekä varastonimikkeitä että palveluita. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

Voit ottaa hyväksymistyönkulun käyttöön kaikissa ostoprosesseissa esimerkiksi silloin, kun pyydät talouspäälliköltä hyväksyntää suurille ostoille. Lisätietoja on kohdassa [Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md).

Seuraavassa osissa kuvataan tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

## Osto-ominaisuuksien käytön aloittaminen

Ennen kuin ostat tavaroita, määritä, miten haluat hallita yrityksesi ostoprosesseja.

|Vastaanottaja...| Katso |
|---|---|
| Määritä säännöt ja arvot, jotka määrittävät yrityksen ostokäytännöt. | [Ostojen määrittäminen](purchasing-setup-purchasing.md) |
| Rekisteröi jokainen toimittaja, jolta ostat toimittajakortin kanssa. | [Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md) |

## Ostoanalyysit

Tässä osassa kuvataan analyysityökaluja, joita voit käyttää, kun haluat saada ostoprosesseja.

| Vastaanottaja... | Katso |
| --- | --- |
| Tutustu ostotietojen analysointimahdollisuuksiin. | [Ostamisen analyysin yleiskatsaus](purchasing-analytics-overview.md) |
| Tee ostotietojen ad-hoc-analyysi suoraan luettelosivuilla ja kyselyissä. | [Ostotietojen ad-hoc-analyysi](ad-hoc-analysis-purchasing.md) |
| Tutki valmiita ostoraportteja. | [Valmiit ostoraportit](purchase-reports.md) |

## Tarjouksesta tilaukseen ja ostolaskuun

Seuraavassa taulukossa kuvataan, miten yksinkertaisia ostoprosesseja käytetään.

| Vastaanottaja | Katso |
| --- | --- |
|Luo toimittajan tarjouspyyntöä vastaava ostotarjous, jonka voit myöhemmin muuntaa ostotilaukseksi.|[Tarjousten pyytäminen](purchasing-how-request-quotes.md)|
| Luo ostolasku kaikille valituille myyntilaskun riveille. |[Nimikkeiden ostaminen myyntiin](purchasing-how-purchase-products-sale.md) |
| Luot ostolasku tallentaaksesi sopimuksesi asiakkaan kanssa tuotteiden ostamisesta tietyillä toimitus- ja maksuehdoilla. |[Ostojen kirjaaminen](purchasing-how-record-purchases.md) |
| Lisätietoja tavasta, jolla [!INCLUDE[prod_short](includes/prod_short.md)] laskee nimikkeen tilausajankohdan, niin että se vastaanotetaan tiettynä päivänä.|[Ostojen päivämäärien laskeminen](purchasing-date-calculation-for-purchases.md)|
|Tietoja siitä, mitä tapahtuu ostoasiakirjoja kirjattaessa.|[Ostojen kirjaaminen](ui-post-purchases.md)|

Jos tarvitset monimutkaisempia ostoprosesseja, seuraavassa taulukossa on luettelo artikkeleista, joissa kerrotaan, miten voit tehdä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmalla.

| Vastaanottaja | Katso |
| --- | --- |
| Suorita toiminto maksamattomalle kirjatulle ostolaskulle hyvityslaskun automaattiseksi luomiseksi ja joko peruuta ostolasku tai luo se uudelleen, jotta voit tehdä korjauksia. |[Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Luo ostohyvityslasku palauttamaan tietty kirjattu ostolasku ilmaisemaan, mitkä tuotteet palautetaan toimittajalle ja mikä maksusumma peritään. |[Ostopalautusten tai -peruutusten käsittely](purchasing-how-process-purchase-returns-cancellations.md) |
|Voit hallita toimittajan suurta määrää koskevaa ostositoumustasi, joka toimitetaan useassa erässä tietyn ajan kuluessa.|[Puiteostotilaukset käyttäminen](sales-how-to-create-blanket-sales-orders.md)|


## Peruutetut tilaukset, hyvitykset ja palautukset

Seuraavassa taulukossa kuvataan, miten ostojen peruutettuja tilauksia, hyvityksiä ja palautuksia käsitellään.

| Vastaanottaja | Katso |
| --- | --- |
|Valmistaudu laskuttamaan kerralla useita vastaanottoja samalta toimittajalta yhdistämällä vastaanotot yhteen laskuun.|[Vastaanottojen yhdistäminen yhteen laskuun](purchasing-how-to-combine-receipts.md)|
|Voit muuntaa esimerkiksi toimittajien sähköiset laskut ostolaskuiksi Business Centralissa.|[Sähköisten asiakirjojen vastaanottaminen ja muuntaminen](purchasing-how-to-receive-and-convert-electronic-documents.md)|


## Muut myyntiprosessit

Seuraavassa taulukossa kuvataan, miten muita ostoprosesseja käytetään.

| Vastaanottaja | Katso |
| --- | --- |
|Ratkaise ristiriita, kun samalla toimittajalla on ainakin tietuetta.|[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)|


## Ulkoisen tiedoston numerot

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Katso myös

[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Ostamisen analyysin yleiskatsaus](purchasing-analytics-overview.md)   
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Yrityksen yleiset toiminnot](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
