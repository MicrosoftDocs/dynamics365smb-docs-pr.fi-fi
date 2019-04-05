---
title: Rakennetiedot – tilausten priorisointi | Microsoft Docs
description: Lisätietoja kysynnän ja tarjonnan vaatimusten priorisoinnista.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 1d58a02bdfe4810d1116d20866d3b435bc7341bc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796371"
---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="25960-103">Rakennetiedot: tilausten priorisointi</span><span class="sxs-lookup"><span data-stu-id="25960-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="25960-104">Pyydetty tai käytettävissä oleva päivämäärä edustaa annetun varastointiyksikön korkeinta prioriteettia. Tämän päivän kysyntä tulee käsitellä ennen seuraavan viikon kysyntää.</span><span class="sxs-lookup"><span data-stu-id="25960-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="25960-105">Mutta tämän kokonaisprioriteetin lisäksi suunnittelujärjestelmä suosittelee myös kysynnän tyyppiä, joka olisi täytettävä ennen toisen kysynnän täyttämistä.</span><span class="sxs-lookup"><span data-stu-id="25960-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="25960-106">Vastaavasti se ehdottaa mitä tarjontalähdettä olisi sovellettava ennen muiden tarjontalähteiden käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="25960-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="25960-107">Tämä tehdään tilauksen prioriteettien mukaan.</span><span class="sxs-lookup"><span data-stu-id="25960-107">This is done according to order priorities.</span></span>  

<span data-ttu-id="25960-108">Ladattu kysyntä ja tarjonta lisätään arvioidun varaston profiiliin seuraavilla prioriteeteilla:</span><span class="sxs-lookup"><span data-stu-id="25960-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  

## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="25960-109">Kysyntäpuolen prioriteetit</span><span class="sxs-lookup"><span data-stu-id="25960-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="25960-110">Jo toimitettu: nimiketapahtuma</span><span class="sxs-lookup"><span data-stu-id="25960-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="25960-111">Ostopalautustilaus</span><span class="sxs-lookup"><span data-stu-id="25960-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="25960-112">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="25960-112">Sales Order</span></span>  
4. <span data-ttu-id="25960-113">Huoltotilaus</span><span class="sxs-lookup"><span data-stu-id="25960-113">Service Order</span></span>  
5. <span data-ttu-id="25960-114">Tuotannon komponenttitarve</span><span class="sxs-lookup"><span data-stu-id="25960-114">Production Component Need</span></span>  
6. <span data-ttu-id="25960-115">Kokoonpanotilauksen rivi</span><span class="sxs-lookup"><span data-stu-id="25960-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="25960-116">Lähtevä siirtotilaus</span><span class="sxs-lookup"><span data-stu-id="25960-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="25960-117">Puitetilaus (jota liittyvä myyntitilaukset eivät ole vielä käyttäneet)</span><span class="sxs-lookup"><span data-stu-id="25960-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="25960-118">Ennuste (jota muut myyntitilaukset eivät ole vielä kuluttaneet)</span><span class="sxs-lookup"><span data-stu-id="25960-118">Forecast (that has not already been consumed by other sales orders)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="25960-119">Ostopalautuksia ei tavallisesti sisällytetä tarjonnan suunnittelun, ne tulisi aina varata erästä,joka aiotaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="25960-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="25960-120">Jos se ei ole varattuna, ostopalautukset vaikuttavat saatavuuteen ja ne priorisoidaan erittäin korkealle, jotta vältetään mahdollisuus, että suunnittelujärjestelmä ehdottaa toimitustilausta vain ostopalautuksen käsittelemiseksi.</span><span class="sxs-lookup"><span data-stu-id="25960-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  

## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="25960-121">Tarjontapuolen prioriteetit</span><span class="sxs-lookup"><span data-stu-id="25960-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="25960-122">Jo varastossa: nimiketapahtuma (suunnittelun joustavuus = ei mitään)</span><span class="sxs-lookup"><span data-stu-id="25960-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="25960-123">Myynnin palautustilaus (suunnittelun joustavuus = ei mitään)</span><span class="sxs-lookup"><span data-stu-id="25960-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="25960-124">Tuleva siirtotilaus</span><span class="sxs-lookup"><span data-stu-id="25960-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="25960-125">Tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="25960-125">Production Order</span></span>  
5. <span data-ttu-id="25960-126">Kokoonpanotilaus</span><span class="sxs-lookup"><span data-stu-id="25960-126">Assembly Order</span></span>  
6. <span data-ttu-id="25960-127">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="25960-127">Purchase Order</span></span>  

## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="25960-128">Kysynnän ja tarjonnan tilaan liittyvä prioriteetti</span><span class="sxs-lookup"><span data-stu-id="25960-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="25960-129">Riippumatta kysynnän ja tarjonnan määrittämistä prioriteeteista, nykyinen tila suoritusprosessissa määrittää myös prioriteetin.</span><span class="sxs-lookup"><span data-stu-id="25960-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="25960-130">Esimerkiksi varastoinnin aktiviteeteilla on vaikutus ja myyntien tila, osto-, siirto-, kokoonpano- ja tuotantotilaukset otetaan huomioon:</span><span class="sxs-lookup"><span data-stu-id="25960-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  

1. <span data-ttu-id="25960-131">Osittain käsitelty (suunnittelun joustavuus = ei mitään)</span><span class="sxs-lookup"><span data-stu-id="25960-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="25960-132">Jo käsittelyssä varastossa (suunnittelun joustavuus = ei mitään)</span><span class="sxs-lookup"><span data-stu-id="25960-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="25960-133">Julkaistu - kaikki tilaustyypit (suunnittelun joustavuus = rajoittamaton)</span><span class="sxs-lookup"><span data-stu-id="25960-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="25960-134">Sitovasti suunniteltu tuotantotilaus (suunnittelun joustavuus = rajoittamaton)</span><span class="sxs-lookup"><span data-stu-id="25960-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="25960-135">Suunniteltu/avoin – kaikki tilaustyypit (suunnittelun joustavuus = rajoittamaton)</span><span class="sxs-lookup"><span data-stu-id="25960-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  

## <a name="see-also"></a><span data-ttu-id="25960-136">Katso myös</span><span class="sxs-lookup"><span data-stu-id="25960-136">See Also</span></span>  
<span data-ttu-id="25960-137">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="25960-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="25960-138">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="25960-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="25960-139">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="25960-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
