---
title: Toimitusehtojen määrittäminen
description: Voit määrittää koodin jokaiselle tarjotulle toimitusehdolle, ja syöttää niitä koskevia tietoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9ee6cdceb716331e2d8338e178def4b8b1e5cfe8
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436699"
---
# <a name="set-up-shipment-methods"></a>Toimitusehtojen määrittäminen

Toimitusehdot määräytyvät usein nimikkeiden, asiakkaiden ja toimittajien mukaan. Jos asiakas asuu esimerkiksi saarella, hän voi valita, että nimikkeet toimitetaan aina lentoteitse tai aina meriteitse. Jotkin asiakkaat saattavat haluta toimituksen seuraavana päivänä. Jotkin asiakkaat taas haluavat noutaa tilauksen. Asiakas- ja toimittajakortteihin voit määrittää, kuinka toimitus toteutetaan.

Kullekin toimitusehdolle määritetään kuvaus ja koodi **Toimitusehto**-sivulla. Voit esimerkiksi määrittää koodiksi FOB ja syöttää **Kuvaus**-kenttään Vapaasti aluksessa. Voit syöttää koodin **Toimitusehtokoodi**-kenttään myös muualla järjestelmässä, esimerkiksi asiakaskortissa. Kun tämän jälkeen luot esimerkiksi uusia tilauksia, laskuja ja hyvityslaskuja, järjestelmä syöttää koodin kuvauksen. Voit muuttaa kuvausta tarvittaessa asiakirjassa.

## <a name="to-set-up-a-shipment-method"></a>Toimitustapojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimitusmuodot** ja valitse sitten vastaava linkki.
2. Valitse **Toimitusehdot**-sivulla **Uusi**-toiminto.
3. Määritä uudella rivillä toimitusehdon koodi ja kuvaus.

> [!TIP]
> Jos käytät Incotermsiä, määritä toimitustavat edustamaan asianmukaisia Incoterms-sääntöjä.  

## <a name="see-also"></a>Katso myös

[Kuljetusliikkeiden määrittäminen](sales-how-to-set-up-shipping-agents.md)  
[Kollien seuraaminen](sales-how-track-packages.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Incoterms osoitteessa iccwbo.org](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]