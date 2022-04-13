---
title: Kuljetusliikkeiden määrittäminen
description: Lue, miten voit määrittää koodin kullekin kuljetusliikkeelle ja syöttää kuvailevat tiedot kustakin sekä niiden tarjoamista palveluista.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 012fe136161d891cb4adde6ace120040f7da909a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513677"
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
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]