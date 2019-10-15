---
title: Kuljetusliikkeiden määrittäminen | Microsoft Docs
description: Voit määrittää koodin jokaiselle kuljetusliikkeelle, ja syöttää tietoja niistä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 27b362c9c9aabec842e28e631ca2b93c1515f2fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311978"
---
# <a name="set-up-shipping-agents"></a>Kuljetusliikkeiden määrittäminen
Voit määrittää koodin jokaiselle kuljetusliikkeelle, ja syöttää tietoja niistä.  

Jos syötät Internet-osoitteen kuljetusliikkeen kohdalle, ja jos kuljetusliike tarjoaa kollinseurantapalveluja Internetissä, voit käyttää ohjelman automaattista kollin seuranta -ominaisuutta. Lisätietoja on kohdassa [Kollien seuraaminen](sales-how-track-packages.md).

Kun määrität kuljetusliikkeitä myyntitilauksillesi, voit määrittää myös kunkin kuljetusliikkeen tarjoamat palvelut.  
Voit määrittää rajoittamattoman määrän palveluita jokaiselle kuljetusliikkeelle ja voit määrittää toimitusajan jokaiselle palvelulle.  

Kun olet määrittänyt kuljetusliikkeen palvelun myyntitilausriville, palvelun toimitusaika sisällytetään sille riville toimituksen lupaamisen laskentaan. Lisätietoja on kohdassa [Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Kuljetusliikkeiden määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuljetusliikkeet** ja valitse sitten liittyvä linkki.  
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
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
