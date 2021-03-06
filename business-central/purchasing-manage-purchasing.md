---
title: Ostojen hallintatehtävien yleiskatsaus
description: Ohjeaiheessa kerrotaan osto- tai hankintaprosessien hallinnasta ja selitetään muun muassa ostolaskujen ja -tilausten käyttöä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 929e1d62a091c4a01aa6f5e03dd5fcbdaa5bf7c0
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115788"
---
# <a name="purchasing"></a>Ostaminen
Voit luoda ostolaskun tai -tilauksen ostojen kustannusten tallentamiseksi ja ostoreskontran seuraamiseksi. Jos haluat hallita varastoa, myös ostolaskuja käytetään varastotasojen dynaamiseen päivittämiseen, jotta voit minimoida varaston kustannukset ja tarjota parempaa asiakaspalvelua. Ostokustannukset, sisältäen palvelukulut ja varastoarvot, jotka aiheutuvat tiliöinnin ostolaskuista, vaikuttavat voittolukuihin ja muihin talouden KPI:hin roolikeskuksessasi.

Ostotilauksia on käytettävä, jos ostoprosessi vaatii tilausmäärän osittaisten vastaanottojen tallentamisen esimerkiksi silloin, kun koko määrä ei ole kerralla toimittajan käytettävissä. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), ostotilauksia on käytettävä. Lisätietoja on kohdassa [Suoratoimitusten tekeminen](sales-how-drop-shipment.md). Kaikilta muilta osin ostotilaukset toimivat samalla tavalla kuin ostolaskut.

Ostolaskut voidaan luoda automaattisesti käyttämällä OCR (Optical Character Recognition) -palvelua toimittajien PDF-laskujen muuntamisessa sähköisiksi asiakirjoiksi, jotka työnkulku puolestaan muuntaa ostolaskuiksi. Voit käyttää tätä toimintoa rekisteröitymällä ensin OCR-palveluun ja määrittämällä sitten asetukset. Lisätietoja on kohdassa [Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).      

Tuotteet voivat olla sekä varastonimikkeitä että palveluita. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

Voit ottaa hyväksymistyönkulun käyttöön kaikissa ostoprosesseissa esimerkiksi silloin, kun pyydät talouspäälliköltä hyväksyntää suurille ostoille. Lisätietoja on kohdassa [Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

| Vastaanottaja | Katso |
| --- | --- |
| Luot ostolasku tallentaaksesi sopimuksesi asiakkaan kanssa tuotteiden ostamisesta tietyillä toimitus- ja maksuehdoilla. |[Ostojen kirjaus](purchasing-how-record-purchases.md) |
|Luo toimittajan tarjouspyyntöä vastaava ostotarjous, jonka voit myöhemmin muuntaa ostotilaukseksi.|[Tarjousten pyytäminen](purchasing-how-request-quotes.md)|
| Luo ostolasku kaikille valituille myyntilaskun riveille. |[Nimikkeiden ostaminen myyntiin](purchasing-how-purchase-products-sale.md) |
|Tietoja siitä, mitä tapahtuu ostoasiakirjoja kirjattaessa.|[Ostojen kirjaaminen](ui-post-purchases.md)|
| Suorita toiminto maksamattomalle kirjatulle ostolaskulle hyvityslaskun automaattiseksi luomiseksi ja joko peruuta ostolasku tai luo se uudelleen, jotta voit tehdä korjauksia. |[Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Luo ostohyvityslasku palauttamaan vastaamaan määrätty kirjattu ostolasku heijastamaan sitä, mitä tuotteita palautat toimittajalle ja minkä maksusumman keräät. |[Ostopalautusten tai peruutusten käsittely](purchasing-how-register-new-vendors.md) |
|Valmistaudu laskuttamaan kerralla useita vastaanottoja samalta toimittajalta yhdistämällä vastaanotot yhteen laskuun.|[Vastaanottojen yhdistäminen yhteen laskuun](purchasing-how-to-combine-receipts.md)|
|Voit muuntaa esimerkiksi toimittajien sähköiset laskut ostolaskuiksi Business Centralissa.|[Sähköisten asiakirjojen vastaanottaminen ja muuntaminen](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Lisätietoja tavasta, jolla [!INCLUDE[prod_short](includes/prod_short.md)] laskee nimikkeen tilausajankohdan, niin että se vastaanotetaan tiettynä päivänä.|[Ostojen päivämäärälaskenta](purchasing-date-calculation-for-purchases.md)|
|Ratkaise ristiriita, kun samalla toimittajalla on ainakin tietuetta.|[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)|
|Voit hallita toimittajan suurta määrää koskevaa ostositoumustasi, joka toimitetaan useassa erässä tietyn ajan kuluessa.|[Puiteostotilausten käyttäminen](sales-how-to-create-blanket-sales-orders.md)|

## <a name="external-document-numbers"></a>Ulkoisen tiedoston numerot

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/purchase-items-services-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Projektien hallinta](projects-manage-projects.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]