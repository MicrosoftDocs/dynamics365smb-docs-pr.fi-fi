---
title: "Rakennetiedot – tilausten käsittely ennen suunnittelun aloituspäivää | Microsoft Docs"
description: "Tässä ohjeaiheessa käsitellään sääntöjä, joita suunnittelu käyttää jäädytetyn alueen tilauksiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5545fe1c2c8833eb1c97765f261777cbb1781098
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a><span data-ttu-id="dabd1-103">Rakennetiedot: tilausten käsittely ennen suunnittelun aloituspäivää</span><span class="sxs-lookup"><span data-stu-id="dabd1-103">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>
<span data-ttu-id="dabd1-104">Voit estää mahdottomien ja sen vuoksi hyödyttömien ehdotusten näkymisen toimitussuunnitelmassa niin, että suunnittelujärjestelmä pitää suunnittelun alkupäivämäärää aiemman jakson jäädytetyksi alueeksi, joka ei sisällä suunnitelmia.</span><span class="sxs-lookup"><span data-stu-id="dabd1-104">To avoid that a supply plan shows impossible and therefore useless suggestions, the planning system regards the period up until the planning starting date a frozen zone where nothing is planned for.</span></span> <span data-ttu-id="dabd1-105">Seuraava sääntö pätee jäädytettyyn alueeseen:</span><span class="sxs-lookup"><span data-stu-id="dabd1-105">The following rule applies to the frozen zone:</span></span>  
  
<span data-ttu-id="dabd1-106">Kaikki kysyntä ja tarjonta ennen suunnittelujakson aloituspäivämäärää katsotaan osaksi varastoa tai toimitetuksi.</span><span class="sxs-lookup"><span data-stu-id="dabd1-106">All supply and demand before the starting date of the planning period will be considered a part of inventory or shipped.</span></span>  
  
<span data-ttu-id="dabd1-107">Näin ollen suunnittelujärjestelmä ei muutamia poikkeuksia lukuun ottamatta ehdota mitään muutoksia toimitustilauksiksi jäädytetyllä alueella ja tilauksen seurantalinkkejä ei luoda tai ylläpidetä tämän ajanjakson osalta.</span><span class="sxs-lookup"><span data-stu-id="dabd1-107">Accordingly, the planning system will not, with a few exceptions, suggest any changes to supply orders in the frozen zone, and no order tracking links are created or maintained for that period.</span></span>  
  
<span data-ttu-id="dabd1-108">Poikkeukset tähän sääntöön ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="dabd1-108">The exceptions to this rule are as follows:</span></span>  
  
* <span data-ttu-id="dabd1-109">Jos oletettu saatavilla oleva varasto, mukaan lukien kysynnän ja tarjonnan summa jäädytetyllä alueella, on nollan alapuolella.</span><span class="sxs-lookup"><span data-stu-id="dabd1-109">If the projected available inventory, including the sum of supply and demand in the frozen zone, is below zero.</span></span>  
* <span data-ttu-id="dabd1-110">Jos takautuvissa tilauksissa vaaditaan sarja-/eränumerot.</span><span class="sxs-lookup"><span data-stu-id="dabd1-110">If serial/lot numbers are required on the backdated order(s).</span></span>  
* <span data-ttu-id="dabd1-111">Jos tarjonta-kysyntä-yhdistelmä on linkitetty tilausten välisellä käytännöllä.</span><span class="sxs-lookup"><span data-stu-id="dabd1-111">If the supply-demand set is linked by an order-to-order policy.</span></span>  
  
<span data-ttu-id="dabd1-112">Jos ensimmäinen käytettävissä oleva varasto on alle nollan, suunnittelujärjestelmä ehdottaa puuttuvan määrän kattamiseksi hätätoimitustilausta suunnittelujaksoa edeltävänä päivänä.</span><span class="sxs-lookup"><span data-stu-id="dabd1-112">If the initial available inventory is below zero, the planning system suggests an emergency supply order on the day before the planning period to cover the missing quantity.</span></span> <span data-ttu-id="dabd1-113">Näin ollen suunnitellun ja käytettävissä olevan varaston on oltava aina vähintään nolla, kun tulevan kauden suunnittelu alkaa.</span><span class="sxs-lookup"><span data-stu-id="dabd1-113">Consequently, the projected and available inventory will always be at least zero when planning for the future period begins.</span></span> <span data-ttu-id="dabd1-114">Tämän toimitustilauksen suunnittelurivillä näytetään Hätävaroituskuvake ja lisätietoa annetaan sitä haettaessa.</span><span class="sxs-lookup"><span data-stu-id="dabd1-114">The planning line for this supply order will display an Emergency warning icon and additional information is provided upon lookup.</span></span>  
  
## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a><span data-ttu-id="dabd1-115">Sarja-/eränumerot ja Tilauksesta tilaukseen -linkit on vapautettu jäädytetyltä alueelta</span><span class="sxs-lookup"><span data-stu-id="dabd1-115">Serial/Lot Numbers and Order-to-Order Links are Exempt from the Frozen Zone</span></span>  
<span data-ttu-id="dabd1-116">Jos sarja-/eränumerot vaaditaan tai tilausten välinen linkki on olemassa, suunnittelujärjestelmä jättää huomioimatta jäädytetyn vyöhykkeen ja sisällyttää nämä takautuvat määrät aloituspäivämäärästä alkaen ja ehdottaa mahdollisesti korjaavia toimenpiteitä, jos kysyntää ja tarjontaa ei synkronoida.</span><span class="sxs-lookup"><span data-stu-id="dabd1-116">If serial/lot numbers are required or an order-to-order link exists, the planning system will disregard the frozen zone and incorporate such quantities that are back-dated from the starting date and potentially suggest corrective actions if demand and supply is not synchronized.</span></span> <span data-ttu-id="dabd1-117">Liiketoimintasyy tälle periaatteelle on se, että tällaisten erityisten kysyntä-tarjonta-asetusten täytyy vastata toisiaan, jotta varmistetaan että tämä erityiskysyntä täyttyy.</span><span class="sxs-lookup"><span data-stu-id="dabd1-117">The business reason for this principle is that such specific demand-supply sets must match to ensure that this specific demand is fulfilled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dabd1-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="dabd1-118">See Also</span></span>  
<span data-ttu-id="dabd1-119">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="dabd1-119">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="dabd1-120">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="dabd1-120">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="dabd1-121">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="dabd1-121">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
