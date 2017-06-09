---
title: Ostaminen| Microsoft Docs
description: "Tässä artikkelissa kerrotaan, miten ostoaktiviteetteja hallitaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4ba8ea773fa4024cfcaccd00b80bdbbfe81be8b7
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="purchasing"></a>Ostaminen
Voit luoda ostolaskun tai -tilauksen ostojen kustannusten tallentamiseksi ja ostoreskontran seuraamiseksi. Jos haluat hallita varastoa, myös ostolaskuja käytetään varastotasojen dynaamiseen päivittämiseen, jotta voit minimoida varaston kustannukset ja tarjota parempaa asiakaspalvelua. Ostokustannukset, kuten palvelukulut ja varastoarvot, jotka aiheutuvat tiliöinnin ostolaskuista, vaikuttavat kotisivullasi oleviin voittolukuihin ja muihin talouden avaintunnuslukuihin.

Ostotilauksia on käytettävä, jos ostoprosessi vaatii tilausmäärän osittaisten vastaanottojen tallentamisen esimerkiksi silloin, kun koko määrä ei ole kerralla toimittajan käytettävissä. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), ostotilauksia on käytettävä. Lisätietoja on kohdassa [Toimintaohje: Suoratoimitusten tekeminen](sales-how-drop-shipment.md). Kaikilta muilta osin ostotilaukset toimivat samalla tavalla kuin ostolaskut.

Ostolaskut voidaan luoda automaattisesti käyttämällä OCR (Optical Character Recognition) -palvelua toimittajien PDF-laskujen muuntamisessa sähköisiksi asiakirjoiksi, jotka työnkulku puolestaan muuntaa ostolaskuiksi. Voit käyttää tätä toimintoa rekisteröitymällä ensin OCR-palveluun ja määrittämällä sitten asetukset. Lisätietoja on kohdassa [Toimintaohje: Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).      

Tuotteet voivat olla sekä varastonimikkeitä että palveluita. Lisätietoja on kohdassa [Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

Voit ottaa hyväksymistyönkulun käyttöön kaikissa ostoprosesseissa esimerkiksi silloin, kun pyydät talouspäälliköltä hyväksyntää suurille ostoille. Lisätietoja on kohdassa [Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin. Tehtävät luetellaan järjestyksessä, jossa ne yleensä suoritetaan.

| Toiminta | Katso |
| --- | --- |
| Luot ostolasku tallentaaksesi sopimuksesi asiakkaan kanssa tuotteiden ostamisesta tietyillä toimitus- ja maksuehdoilla. |[Toimintaohje: Ostojen kirjaus](purchasing-how-record-purchases.md) |
| Luo ostolasku kaikille valituille myyntilaskun riveille. |[Toimintaohje: Tuotteiden ostaminen myyntiin](purchasing-how-purchase-products-sale.md) |
| Suorita toiminto maksamattomalle kirjatulle ostolaskulle hyvityslaskun automaattiseksi luomiseksi ja joko peruuta ostolasku tai luo se uudelleen, jotta voit tehdä korjauksia. |[Toimintaohjeet: Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Luo ostohyvityslasku palauttamaan vastaamaan määrätty kirjattu ostolasku heijastamaan sitä, mitä tuotteita palautat toimittajalle ja minkä maksusumman keräät. |[Toimintaohje: Ostopalautuksen tai peruutuksen käsittely](purchasing-how-register-new-vendors.md) |
| Luo toimittajan kortti jokaiselle toimittajalle, jolta ostat. |[Toimintaohje: Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md) |

## <a name="see-also"></a>Katso myös
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Projektien hallinta](projects-manage-projects.md)    
[Toimitusketju](madeira-supply-chain.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
