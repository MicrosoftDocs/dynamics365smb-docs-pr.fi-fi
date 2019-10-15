---
title: Rakennetiedot – täsmäytys lyhyesti | Microsoft Docs
description: Yrityksen asiakkaat antavat kysynnän. Yritys voi luoda ja poistaa tarjontaa luodakseen tasapainon. Suunnittelujärjestelmä aloittaa riippumattomasta kysynnästä ja jäljittää sitten taaksepäin tarjontaan.
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
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: af63bf59def37fe873cb66366864855db52bd245
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302954"
---
# <a name="design-details-the-concept-of-balancing-in-brief"></a><span data-ttu-id="1aef9-105">Rakennetiedot: täsmäytyksen käsite lyhyesti</span><span class="sxs-lookup"><span data-stu-id="1aef9-105">Design Details: The Concept of Balancing in Brief</span></span>
<span data-ttu-id="1aef9-106">Yrityksen asiakkaat muodostavat kysynnän.</span><span class="sxs-lookup"><span data-stu-id="1aef9-106">Demand is given by a company’s customers.</span></span> <span data-ttu-id="1aef9-107">Yritys voi luoda ja poistaa tarjontaa luodakseen tasapainon.</span><span class="sxs-lookup"><span data-stu-id="1aef9-107">Supply is what the company can create and remove to establish balance.</span></span> <span data-ttu-id="1aef9-108">Suunnittelujärjestelmä aloittaa riippumattomasta kysynnästä ja jäljittää sitten taaksepäin tarjontaan.</span><span class="sxs-lookup"><span data-stu-id="1aef9-108">The planning system starts with the independent demand and then tracks backwards to the supply.</span></span>  

 <span data-ttu-id="1aef9-109">Varastoprofiileja käytetään sisältämään tietoa kysynnästä ja tarjonnasta, määristä ja ajoituksista.</span><span class="sxs-lookup"><span data-stu-id="1aef9-109">The inventory profiles are used to contain information about the demands and supplies, quantities, and timing.</span></span> <span data-ttu-id="1aef9-110">Nämä profiilit muodostavat käytännössä täsmäytysasteikon kaksi eri puolta.</span><span class="sxs-lookup"><span data-stu-id="1aef9-110">These profiles essentially make up the two sides of the balancing scale.</span></span>  

 <span data-ttu-id="1aef9-111">Suunnittelumekanismin päämäärä on tasapainottaa nimikkeen kysyntää ja tarjontaa, jolloin varmistetaan se, että tarjonta vastaa kysyntää toteuttamiskelpoisella tavalla, kuten määritetty suunnitteluparametreissa ja säännöissä.</span><span class="sxs-lookup"><span data-stu-id="1aef9-111">The objective of the planning mechanism is to counterbalance the demand and supply of an item to ensure that supply will match demand in a feasible way as defined by the planning parameters and rules.</span></span>  

 <span data-ttu-id="1aef9-112">![Kysynnän ja tarjonnan täsmäytyksen yleiskatsaus](media/nav_app_supply_planning_2_balancing.png "Kysynnän ja tarjonnan täsmäytyksen yleiskatsaus")</span><span class="sxs-lookup"><span data-stu-id="1aef9-112">![Overview of supply-demand balancing](media/nav_app_supply_planning_2_balancing.png "Overview of supply-demand balancing")</span></span>  

## <a name="see-also"></a><span data-ttu-id="1aef9-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1aef9-113">See Also</span></span>  
 <span data-ttu-id="1aef9-114">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="1aef9-114">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="1aef9-115">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="1aef9-115">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="1aef9-116">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="1aef9-116">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
