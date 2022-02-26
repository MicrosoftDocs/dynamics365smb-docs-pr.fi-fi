---
title: Kuljetusliikkeiden määrittäminen
description: Lue, miten voit määrittää koodin kullekin kuljetusliikkeelle ja syöttää kuvailevat tiedot kustakin sekä niiden tarjoamista palveluista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 1e74be125909db7f7d1c4301a33da1b12648e70a
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440226"
---
# <a name="set-up-shipping-agents"></a>Kuljetusliikkeiden määrittäminen
Voit määrittää koodin jokaiselle kuljetusliikkeelle, ja syöttää tietoja niistä.  

Jos syötät Internet-osoitteen kuljetusliikkeen kohdalle, ja jos kuljetusliike tarjoaa kollinseurantapalveluja Internetissä, voit käyttää ohjelman automaattista kollin seuranta -ominaisuutta. Lisätietoja on kohdassa [Kollien seuraaminen](sales-how-track-packages.md).

Kun määrität kuljetusliikkeitä myyntitilauksillesi, voit määrittää myös kunkin kuljetusliikkeen tarjoamat palvelut.  
Voit määrittää rajoittamattoman määrän palveluita jokaiselle kuljetusliikkeelle ja voit määrittää toimitusajan jokaiselle palvelulle.  

Kun olet määrittänyt kuljetusliikkeen palvelun myyntitilausriville, palvelun toimitusaika sisällytetään sille riville toimituksen lupaamisen laskentaan. Lisätietoja on kohdassa [Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Kuljetusliikkeiden määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuljetusliikkeet** ja valitse sitten vastaava linkki.  
2.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Valitse **Kuljetusliikkeen palvelut** -toiminto.
4. Täytä tarvittavat **Kuljetusliikkeen palvelut** -kentät.

> [!NOTE]  
>  Jos poistat kuljetusliikkeen tilausriviltä, ohjelma poistaa riviltä myös kuljetusliikkeen palvelukoodin. Ohjelma laskee sen jälkeen uudelleen kenttien tiedot, jotka perustuivat osittain kuljetusliikkeiden palveluihin.  

## <a name="see-also"></a>Katso myös
[Toimitusehtojen määrittäminen](sales-how-set-up-shipment-methods.md)  
[Kollien seuraaminen](sales-how-track-packages.md)    
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]