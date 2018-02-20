---
title: "Rakennetiedot – Uusintatilauspisteen rooli | Microsoft Docs"
description: "Tässä ohjeaiheessa selvitetään uusintatilauspisteen määrityksen merkitystä, sillä sen perusteella osataan tilata lisää varastoa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5b5e3cec4bc5af8188470ea1d711422c0130677e
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="44cee-103">Rakennetiedot: uusintatilauspisteen rooli</span><span class="sxs-lookup"><span data-stu-id="44cee-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="44cee-104">Yleisen kysynnän ja tarjonnan täsmäytyksen lisäksi suunnittelujärjestelmän on myös valvottava liittyvien nimikkeiden varastomääriä suhteessa määritettyihin uudelleenjärjestelykäytäntöihin.</span><span class="sxs-lookup"><span data-stu-id="44cee-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  
  
<span data-ttu-id="44cee-105">Uusintatilauspiste edustaa kysyntää toimitusaikana.</span><span class="sxs-lookup"><span data-stu-id="44cee-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="44cee-106">Kun oletetun varaston arvo laskee uusintatilauspisteen määrittämän varaston tason alapuolelle, on aika tilata lisää.</span><span class="sxs-lookup"><span data-stu-id="44cee-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="44cee-107">Tänä aikana varaston arvon oletetaan laskevan asteittain ja saavuttavan mahdollisesti nollan (tai varmuusvaraston tason), kunnes täydennys saapuu.</span><span class="sxs-lookup"><span data-stu-id="44cee-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  
  
<span data-ttu-id="44cee-108">Näin ollen suunnittelujärjestelmä ehdottaa tulevaa ajastettua toimitustilausta, kun oletettu varasto vähenee uusintatilauspisteen alapuolelle.</span><span class="sxs-lookup"><span data-stu-id="44cee-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  
  
<span data-ttu-id="44cee-109">Jälkitilauspiste heijastaa tiettyä varaston tasoa.</span><span class="sxs-lookup"><span data-stu-id="44cee-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="44cee-110">Varastotasot voivat kuitenkin siirtyä aikavälillä huomattavasti, ja tämän vuoksi suunnittelujärjestelmän tulisi valvoa jatkuvasti oletettua saatavilla olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="44cee-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44cee-111">Katso myös</span><span class="sxs-lookup"><span data-stu-id="44cee-111">See Also</span></span>  
<span data-ttu-id="44cee-112">[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="44cee-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="44cee-113">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="44cee-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="44cee-114">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="44cee-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="44cee-115">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="44cee-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
