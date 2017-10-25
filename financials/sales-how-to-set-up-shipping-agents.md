---
title: "Kuljetusliikkeiden määrittäminen | Microsoft Docs"
description: "Voit määrittää koodin jokaiselle kuljetusliikkeelle, ja syöttää tietoja niistä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84a5d9eb8757dc82834c17327ffbb510cd15fa1a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shipping-agents"></a>Kuljetusliikkeiden määrittäminen
Voit määrittää koodin jokaiselle kuljetusliikkeelle ja antaa niitä koskevia tietoja.  

Jos syötät Internet-osoitteen kuljetusliikkeen kohdalle, ja jos kuljetusliike tarjoaa kollinseurantapalveluja Internetissä, voit käyttää ohjelman automaattista kollin seuranta -ominaisuutta. Lisätietoja on kohdassa [Toimintaohje: Kollien seuraaminen](sales-how-track-packages.md).

Kun määrität kuljetusliikkeitä myyntitilauksillesi, voit määrittää myös kunkin kuljetusliikkeen tarjoamat palvelut.  
Voit määrittää rajoittamattoman määrän palveluita jokaiselle kuljetusliikkeelle ja voit määrittää toimitusajan jokaiselle palvelulle.  

Kun olet määrittänyt kuljetusliikkeen palvelun myyntitilausriville, palvelun toimitusaika sisällytetään sille riville toimituksen lupaamisen laskentaan. Lisätietoja on kohdassa [Toimintaohje: Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Kuljetusliikkeiden määrittäminen  
1.  Valitse ![Etsiä sivu tai raportti](media/ui-search/search_small.png "Etsiä sivu tai raportti -kuvake") -kuvake, kirjoita **Kuljetusliikkeet** ja valitse sitten aiheeseen liittyvät linkki.  
2.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Valitse **Kuljetusliikkeen palvelut** -toiminto.
4. Täytä tarvittavat **Kuljetusliikkeen palvelut** -kentät.

> [!NOTE]  
>  Jos poistat kuljetusliikkeen tilausriviltä, ohjelma poistaa riviltä myös kuljetusliikkeen palvelukoodin. Ohjelma laskee sen jälkeen uudelleen kenttien tiedot, jotka perustuivat osittain kuljetusliikkeiden palveluihin.  

## <a name="see-also"></a>Katso myös
[Kollien seuraaminen](sales-how-track-packages.md)    
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

