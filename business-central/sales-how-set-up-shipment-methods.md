---
title: Toimitusehtojen määrittäminen | Microsoft Docs
description: Voit määrittää koodin jokaiselle tarjotulle toimitusehdolle, ja syöttää niitä koskevia tietoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 75a3e689083e64f446e84b2bc3b1d26961e3d898
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877541"
---
# <a name="set-up-shipment-methods"></a>Toimitusehtojen määrittäminen
Toimitusehdot, joita kutsutaan myös incoterms-toimitusehdoiksi, määräytyvät usein nimikkeiden, asiakkaiden ja toimittajien mukaan. Jos asiakas asuu esimerkiksi saarella, hän voi valita, että nimikkeet toimitetaan aina lentoteitse tai aina meriteitse. Jotkin asiakkaat saattavat haluta toimituksen seuraavana päivänä. Jotkin asiakkaat taas haluavat noutaa tilauksen. Asiakas- ja toimittajakortteihin voit määrittää, kuinka toimitus toteutetaan.

Kullekin toimitusehdolle määritetään kuvaus ja koodi **Toimitusehto**-sivulla. Voit esimerkiksi määrittää koodiksi FOB ja syöttää **Kuvaus**-kenttään Vapaasti aluksessa. Voit syöttää koodin **Toimitusehtokoodi**-kenttään myös muualla järjestelmässä, esimerkiksi asiakaskortissa. Kun tämän jälkeen luot esimerkiksi uusia tilauksia, laskuja ja hyvityslaskuja, järjestelmä syöttää koodin kuvauksen. Voit muuttaa kuvausta tarvittaessa asiakirjassa.

## <a name="to-set-up-a-shipment-code"></a>Toimituskoodin määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimitustavat** ja valitse sitten liittyvä linkki.
2. Valitse **Toimitusehdot**-sivulla **Uusi**-toiminto.
3. Määritä uudella rivillä toimitusehdon koodi ja kuvaus.

## <a name="see-also"></a>Katso myös
[Incoterms-toimituslausekkeet](https://iccwbo.org/resources-for-business/incoterms-rules)  
[Kuljetusliikkeiden määrittäminen](sales-how-to-set-up-shipping-agents.md)  
[Kollien seuraaminen](sales-how-track-packages.md)    
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
