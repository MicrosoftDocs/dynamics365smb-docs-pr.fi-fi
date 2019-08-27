---
title: Toimitusehtojen määrittäminen | Microsoft Docs
description: Voit määrittää koodin jokaiselle tarjotulle toimitusehdolle, ja syöttää niitä koskevia tietoja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 06/17/2019
ms.author: sgroespe
ms.openlocfilehash: 7248f49e92db98cec047d2035ce82d7caf84799f
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632781"
---
# <a name="set-up-shipment-methods"></a>Toimitusehtojen määrittäminen
Toimitusehdot, joita kutsutaan myös incoterms-toimitusehdoiksi, määräytyvät usein nimikkeiden, asiakkaiden ja toimittajien mukaan. Jos asiakas asuu esimerkiksi saarella, hän voi valita, että nimikkeet toimitetaan aina lentoteitse tai aina meriteitse. Jotkin asiakkaat saattavat haluta toimituksen seuraavana päivänä. Jotkin asiakkaat taas haluavat noutaa tilauksen. Asiakas- ja toimittajakortteihin voit määrittää, kuinka toimitus toteutetaan.

Kullekin toimitusehdolle määritetään kuvaus ja koodi **Toimitusehto**-sivulla. Voit esimerkiksi määrittää koodiksi FOB ja syöttää **Kuvaus**-kenttään Vapaasti aluksessa. Voit syöttää koodin **Toimitusehtokoodi**-kenttään myös muualla järjestelmässä, esimerkiksi asiakaskortissa. Kun tämän jälkeen luot esimerkiksi uusia tilauksia, laskuja ja hyvityslaskuja, järjestelmä syöttää koodin kuvauksen. Voit muuttaa kuvausta tarvittaessa asiakirjassa.

## <a name="to-set-up-a-shipment-code"></a>Toimituskoodin määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **toimitusehdot** ja valitse sitten liittyvä linkki.
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