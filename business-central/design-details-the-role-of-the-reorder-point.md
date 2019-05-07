---
title: Rakennetiedot – Uusintatilauspisteen rooli | Microsoft Docs
description: Tässä ohjeaiheessa selvitetään uusintatilauspisteen määrityksen merkitystä, sillä sen perusteella osataan tilata lisää varastoa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 836da35166d947de8c37128d9ed8807914594c55
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "924185"
---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="5247f-103">Rakennetiedot: uusintatilauspisteen rooli</span><span class="sxs-lookup"><span data-stu-id="5247f-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="5247f-104">Yleisen kysynnän ja tarjonnan täsmäytyksen lisäksi suunnittelujärjestelmän on myös valvottava liittyvien nimikkeiden varastomääriä suhteessa määritettyihin uudelleenjärjestelykäytäntöihin.</span><span class="sxs-lookup"><span data-stu-id="5247f-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  

<span data-ttu-id="5247f-105">Uusintatilauspiste edustaa kysyntää toimitusaikana.</span><span class="sxs-lookup"><span data-stu-id="5247f-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="5247f-106">Kun oletetun varaston arvo laskee uusintatilauspisteen määrittämän varaston tason alapuolelle, on aika tilata lisää.</span><span class="sxs-lookup"><span data-stu-id="5247f-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="5247f-107">Tänä aikana varaston arvon oletetaan laskevan asteittain ja saavuttavan mahdollisesti nollan (tai varmuusvaraston tason), kunnes täydennys saapuu.</span><span class="sxs-lookup"><span data-stu-id="5247f-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  

<span data-ttu-id="5247f-108">Näin ollen suunnittelujärjestelmä ehdottaa tulevaa ajastettua toimitustilausta, kun oletettu varasto vähenee uusintatilauspisteen alapuolelle.</span><span class="sxs-lookup"><span data-stu-id="5247f-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  

<span data-ttu-id="5247f-109">Jälkitilauspiste heijastaa tiettyä varaston tasoa.</span><span class="sxs-lookup"><span data-stu-id="5247f-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="5247f-110">Varastotasot voivat kuitenkin siirtyä aikavälillä huomattavasti, ja tämän vuoksi suunnittelujärjestelmän tulisi valvoa jatkuvasti oletettua saatavilla olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="5247f-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5247f-111">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5247f-111">See Also</span></span>  
<span data-ttu-id="5247f-112">[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="5247f-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="5247f-113">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="5247f-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="5247f-114">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="5247f-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="5247f-115">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="5247f-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
