---
title: "Rakennetiedot – kysynnän ja tarjonnan täsmäyttäminen | Microsoft Docs"
description: "Suunnittelujärjestelmän priorisoitujen tavoitteiden ymmärtäminen edellyttää suunnittelujärjestelmän toiminnan ymmärtämistä. Tärkeimmät tavoitteet pyrkivät varmistamaan, että kaikki kysyntä täytetään riittävällä tarjonnalla ja että kaikki tarjonta palvelee tarkoitusta."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: af9569114cfbe2d48be3a7514cc5c2bb48bd48ca
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-balancing-demand-and-supply"></a><span data-ttu-id="ea364-103">Rakennetiedot: kysynnän ja tarjonnan täsmäytys</span><span class="sxs-lookup"><span data-stu-id="ea364-103">Design Details: Balancing Demand and Supply</span></span>
<span data-ttu-id="ea364-104">Suunnittelujärjestelmän priorisoitujen tavoitteiden ymmärtäminen edellyttää suunnittelujärjestelmän toiminnan ymmärtämistä. Tärkeimmät tavoitteet pyrkivät varmistamaan seuraavat seikat:</span><span class="sxs-lookup"><span data-stu-id="ea364-104">To understand how the planning system works, it is necessary to understand the prioritized goals of the planning system, the most important of which are to ensure that:</span></span>  

- <span data-ttu-id="ea364-105">Kaikki kysyntä täytetään riittävällä tarjonnalla.</span><span class="sxs-lookup"><span data-stu-id="ea364-105">Any demand will be met by sufficient supply.</span></span>  
- <span data-ttu-id="ea364-106">Kaikki tarjonta palvelee tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="ea364-106">Any supply serves a purpose.</span></span>  

 <span data-ttu-id="ea364-107">Yleisesti ottaen nämä tavoitteet saavutetaan täsmäyttämällä tarjonta ja kysyntä.</span><span class="sxs-lookup"><span data-stu-id="ea364-107">Generally, these goals are achieved by balancing supply with demand.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="ea364-108">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="ea364-108">In This Section</span></span>  
[<span data-ttu-id="ea364-109">Rakennetiedot: kysyntä ja tarjonta</span><span class="sxs-lookup"><span data-stu-id="ea364-109">Design Details: Demand and Supply</span></span>](design-details-demand-and-supply.md)  
[<span data-ttu-id="ea364-110">Rakennetiedot: täsmäytyksen käsite lyhyesti</span><span class="sxs-lookup"><span data-stu-id="ea364-110">Design Details: The Concept of Balancing in Brief</span></span>](design-details-the-concept-of-balancing-in-brief.md)  
[<span data-ttu-id="ea364-111">Rakennetiedot: tilausten käsittely ennen suunnittelun aloituspäivää</span><span class="sxs-lookup"><span data-stu-id="ea364-111">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>](design-details-dealing-with-orders-before-the-planning-starting-date.md)  
[<span data-ttu-id="ea364-112">Rakennetiedot: varastoprofiilien lataaminen</span><span class="sxs-lookup"><span data-stu-id="ea364-112">Design Details: Loading the Inventory Profiles</span></span>](design-details-loading-the-inventory-profiles.md)  
[<span data-ttu-id="ea364-113">Rakennetiedot: tilausten priorisointi</span><span class="sxs-lookup"><span data-stu-id="ea364-113">Design Details: Prioritizing Orders</span></span>](design-details-prioritizing-orders.md)  
[<span data-ttu-id="ea364-114">Rakennetiedot: tarjonnan täsmäytys kysynnällä</span><span class="sxs-lookup"><span data-stu-id="ea364-114">Design Details: Balancing Supply with Demand</span></span>](design-details-balancing-supply-with-demand.md)  
[<span data-ttu-id="ea364-115">Rakennetiedot: kysynnän ja tarjonnan sulkeminen</span><span class="sxs-lookup"><span data-stu-id="ea364-115">Design Details: Closing Demand and Supply</span></span>](design-details-closing-demand-and-supply.md)  

## <a name="see-also"></a><span data-ttu-id="ea364-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ea364-116">See Also</span></span>  
 <span data-ttu-id="ea364-117">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="ea364-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 <span data-ttu-id="ea364-118">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="ea364-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="ea364-119">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="ea364-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

