---
title: Sijaintikortin ja siirtoreittien määrittäminen| Microsoft Docs
description: Jokaisille varastoitavalle varastonimikkeelle luodaan sijaintikortti, kuten varasto tai jakelukeskus. Lisäksi sijaintien välille määritetään siirtoreitit.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 805439e0cc50fe0b9dc3132050eb7c7041ffe7a7
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785944"
---
# <a name="set-up-locations"></a>Sijaintien määrittäminen
Jos ostat, varastoit tai myyt nimikkeitä useamman varaston avulla, sijaintikortti ja siirtoreitit on määritettävä jokaiselle sijainnille.

Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen. Lisätietoja on myös kohdassa [Varaston hallinta](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="to-create-a-location-card"></a>Sijaintikortin luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sijainnit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Sijaintikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.

> [!NOTE]  
> Monet sijaintikortin kentät viittaavat saapuvien ja lähtevien varastoprosessien nimikkeiden käsittelyyn. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Siirtoreittien luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Siirtoreitit** ja valitse sitten liittyvä linkki.
2. Voit myös valita **Siirtoreitit**-toiminnon miltä tahansa **Sijaintikortti**-sivulta.
3. Valitse **Uusi**-toiminto.
4. Täytä **Sijaintikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voit nyt siirtää varastonimikkeitä sijaintien välillä. Lisätietoja on kohdassa [Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Katso myös
[Varaston hallinta](inventory-manage-inventory.md)  
[Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)
