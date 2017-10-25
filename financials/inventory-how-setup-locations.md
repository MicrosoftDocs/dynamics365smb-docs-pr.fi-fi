---
title: "Sijaintikortin ja siirtoreittien määrittäminen| Microsoft Docs"
description: "Jokaisille varastoitavalle varastonimikkeelle luodaan sijaintikortti, kuten varasto tai jakelukeskus. Lisäksi sijaintien välille määritetään siirtoreitit."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7d82b1c63bb1da367736f8dd044640b583493af8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-locations"></a>Sijaintien määrittäminen
Jos ostat, varastoit tai myyt nimikkeitä useamman varaston avulla, sijaintikortti ja siirtoreitit on määritettävä jokaiselle sijainnille.

Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen. Lisätietoja on myös kohdassa [Varaston hallinta](inventory-manage-inventory.md).

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-create-a-location-card"></a>Sijaintikortin luominen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Sijaintikortti**-ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.

> [!NOTE]  
> Monet sijaintikortin kentät viittaavat saapuvien ja lähtevien varastoprosessien nimikkeiden käsittelyyn. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md). 

## <a name="to-create-a-transfer-route"></a>Siirtoreittien luominen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.
2. Voit myös valita **Siirtoreitit**-toiminnon mistä tahansa **Sijaintikortti**-ikkunasta.
3. Valitse **Uusi**-toiminto.
4. Täytä **Sijaintikortti**-ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voit nyt siirtää varastonimikkeitä sijaintien välillä. Lisätietoja on kohdassa [Toimintaohje: Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Katso myös
[Varaston hallinta](inventory-manage-inventory.md)  
[Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

