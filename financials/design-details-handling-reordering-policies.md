---
title: "Rakennetiedot – uusintatilauskäytäntöjen käsittely | Microsoft Docs"
description: "Yleiskatsaus tehtävistä, joilla määritetään tuotantosuunnittelun uusintatilauskäytäntö."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="f7fdf-103">Rakennetiedot: uusintatilauskäytäntöjen käsittely</span><span class="sxs-lookup"><span data-stu-id="f7fdf-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="f7fdf-104">Uusintatilausväli on määritettävä, jotta nimike voi osallistua tarjonnan suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="f7fdf-105">Seuraavat neljä jälkitilausohjetta on olemassa:</span><span class="sxs-lookup"><span data-stu-id="f7fdf-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="f7fdf-106">Kiinteä uusintatil. määrä</span><span class="sxs-lookup"><span data-stu-id="f7fdf-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="f7fdf-107">Enimmäismäärä</span><span class="sxs-lookup"><span data-stu-id="f7fdf-107">Maximum Qty.</span></span>  
* <span data-ttu-id="f7fdf-108">Tilaus</span><span class="sxs-lookup"><span data-stu-id="f7fdf-108">Order</span></span>  
* <span data-ttu-id="f7fdf-109">Erä-erästä</span><span class="sxs-lookup"><span data-stu-id="f7fdf-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="f7fdf-110">Kiinteä uusintatil. määrä- ja enimmäismäärä-käytännöt liittyvät varaston suunnittelu.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="f7fdf-111">Vaikka varaston suunnittelu on teknisesti helpompaa kuin täsmäytys, näiden käytäntöjen tulee toimia yhdessä tarjonnan vaiheittaiseksi täsmäyttämiseksi ja tilausten seuraamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="f7fdf-112">Jotta näiden kahden välisen integroinnin valvonta ja Käytetyn suunnittelulogiikan näkyvyyden määritys onnistuu, uudelleentilausmenetelmiä käsitellään tiukkojen periaatteiden avulla.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f7fdf-113">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="f7fdf-113">In This Section</span></span>  
[<span data-ttu-id="f7fdf-114">Rakennetiedot: uusintatilauspisteen rooli</span><span class="sxs-lookup"><span data-stu-id="f7fdf-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="f7fdf-115">Rakennetiedot: arvioidun varastotason ja uusintatilauspisteen valvonta</span><span class="sxs-lookup"><span data-stu-id="f7fdf-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="f7fdf-116">Rakennetiedot: aikavälin rooli</span><span class="sxs-lookup"><span data-stu-id="f7fdf-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="f7fdf-117">Rakennetiedot: sallitun ylityksen alapuolella pysytteleminen</span><span class="sxs-lookup"><span data-stu-id="f7fdf-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="f7fdf-118">Rakennetiedot: suunnitellun negatiivisen varaston käsittely</span><span class="sxs-lookup"><span data-stu-id="f7fdf-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="f7fdf-119">Rakennetiedot: uusintatilauskäytännöt</span><span class="sxs-lookup"><span data-stu-id="f7fdf-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="f7fdf-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f7fdf-120">See Also</span></span>  
<span data-ttu-id="f7fdf-121">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="f7fdf-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="f7fdf-122">[Rakennetiedot: suunnittelun kohdistustaulukko](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="f7fdf-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="f7fdf-123">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="f7fdf-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="f7fdf-124">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="f7fdf-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="f7fdf-125">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="f7fdf-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
