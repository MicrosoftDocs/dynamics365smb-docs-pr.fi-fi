---
title: Rakennetiedot – Uusintatilauspisteen rooli | Microsoft Docs
description: Tässä ohjeaiheessa selvitetään uusintatilauspisteen määrityksen merkitystä, sillä sen perusteella osataan tilata lisää varastoa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 836da35166d947de8c37128d9ed8807914594c55
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246080"
---
# <a name="design-details-the-role-of-the-reorder-point"></a>Rakennetiedot: uusintatilauspisteen rooli
Yleisen kysynnän ja tarjonnan täsmäytyksen lisäksi suunnittelujärjestelmän on myös valvottava liittyvien nimikkeiden varastomääriä suhteessa määritettyihin uudelleenjärjestelykäytäntöihin.  
  
Uusintatilauspiste edustaa kysyntää toimitusaikana. Kun oletetun varaston arvo laskee uusintatilauspisteen määrittämän varaston tason alapuolelle, on aika tilata lisää. Tänä aikana varaston arvon oletetaan laskevan asteittain ja saavuttavan mahdollisesti nollan (tai varmuusvaraston tason), kunnes täydennys saapuu.  
  
Näin ollen suunnittelujärjestelmä ehdottaa tulevaa ajastettua toimitustilausta, kun oletettu varasto vähenee uusintatilauspisteen alapuolelle.  
  
Jälkitilauspiste heijastaa tiettyä varaston tasoa. Varastotasot voivat kuitenkin siirtyä aikavälillä huomattavasti, ja tämän vuoksi suunnittelujärjestelmän tulisi valvoa jatkuvasti oletettua saatavilla olevaa varastoa.  
  
## <a name="see-also"></a>Katso myös  
[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md)   
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)