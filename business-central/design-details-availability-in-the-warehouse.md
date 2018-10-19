---
title: "Rakennetiedot – Saatavuus varastossa | Microsoft Docs"
description: "Järjestelmän on valvottava varaston nimikkeiden saatavuutta jatkuvasti, jotta lähtevät tilaukset toimitetaan tehokkaasti ja toimitukset saadaan halutussa ajassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 90d25c9c5c5687109387c548a273f4457691e151
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-availability-in-the-warehouse"></a><span data-ttu-id="728a9-103">Rakennetiedot: saatavuus varastossa</span><span class="sxs-lookup"><span data-stu-id="728a9-103">Design Details: Availability in the Warehouse</span></span>
<span data-ttu-id="728a9-104">Järjestelmän on valvottava varaston nimikkeiden saatavuutta jatkuvasti, jotta lähtevät tilaukset toimitetaan tehokkaasti ja toimitukset saadaan halutussa ajassa.</span><span class="sxs-lookup"><span data-stu-id="728a9-104">The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.</span></span>  

 <span data-ttu-id="728a9-105">Saatavuus vaihtelee riippuen varauksista lokerotasolla, kun varastotoiminnot, kuten poiminnat ja liikkeet ilmenevät ja kun varaston varausjärjestelmä asettaa noudatettavat rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="728a9-105">Availability varies depending on allocations at the bin level when warehouse activities such as picks and movements occur and when the inventory reservation system imposes restrictions to comply with.</span></span> <span data-ttu-id="728a9-106">Varsin monimutkainen algoritmi tarkistaa, että kaikki edellytykset täyttyvät ennen kuin poimintojen määrät määritetään lähteville virroille.</span><span class="sxs-lookup"><span data-stu-id="728a9-106">A rather complex algorithm verifies that all conditions are met before allocating quantities to picks for outbound flows.</span></span>  

## <a name="bin-content-and-reservations"></a><span data-ttu-id="728a9-107">Lokeron sisältö ja varaukset</span><span class="sxs-lookup"><span data-stu-id="728a9-107">Bin Content and Reservations</span></span>  
 <span data-ttu-id="728a9-108">Kaikissa varastoinninhallinnan asennuksissa nimikkeen määrät ovat olemassa sekä fyysisen varastoinnin tapahtumina fyysisen varaston sovellusalueella että nimiketapahtumina varaston sovellusalueella.</span><span class="sxs-lookup"><span data-stu-id="728a9-108">In any installation of warehouse management, item quantities exist both as warehouse entries, in the Warehouse application area, and as item ledger entries, in the Inventory application area.</span></span> <span data-ttu-id="728a9-109">Nämä kaksi tapahtumatyyppiä sisältävät eri tiedot nimikkeiden sijainnista ja niiden saatavuudesta.</span><span class="sxs-lookup"><span data-stu-id="728a9-109">These two entry types contain different information about where items exist and whether they are available.</span></span> <span data-ttu-id="728a9-110">Fyysisen varastoinnin tapahtumat määrittävät nimikkeen saatavuuden varastopaikan ja varastopaikan tyypin mukaan. Jälkimmäistä kutsutaan myös varastopaikan sisällöksi.</span><span class="sxs-lookup"><span data-stu-id="728a9-110">Warehouse entries define an item’s availability by bin and bin type, which is called bin content.</span></span> <span data-ttu-id="728a9-111">Nimiketapahtumat määrittävät nimikkeen saatavuuden lähtevien asiakirjojen varauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="728a9-111">Item ledger entries define an item’s availability by its reservation to outbound documents.</span></span>  

 <span data-ttu-id="728a9-112">Erikoistoiminta on olemassa poiminta-algoritmissa ja sen avulla voidaan laskea määrä, joka on käytettävissä poimimiseen, kun säiliön sisältö on yhdistetty varauksiin.</span><span class="sxs-lookup"><span data-stu-id="728a9-112">Special functionality in the picking algorithm exists to calculate the quantity that is available to pick when bin content is coupled with reservations.</span></span>  

## <a name="quantity-available-to-pick"></a><span data-ttu-id="728a9-113">Saatavilla oleva poimintamäärä</span><span class="sxs-lookup"><span data-stu-id="728a9-113">Quantity Available to Pick</span></span>  
 <span data-ttu-id="728a9-114">Jos poiminta-algoritmi ei esimerkiksi ota huomioon nimikkeiden määriä, jotka on varattu odottavalle myyntitilauksen toimitukselle, nämä nimikkeet saatetaan poimia toiselle myyntitilaukselle, joka toimitetaan aiemmin ja tämä estää ensimmäisen myynnin täyttämisen.</span><span class="sxs-lookup"><span data-stu-id="728a9-114">If, for example, the picking algorithm does not consider item quantities that are reserved for a pending sales order shipment, then those items might be picked for another sales order that is shipped earlier, which prevents the first sales from being fulfilled.</span></span> <span data-ttu-id="728a9-115">Tämä tilanne vältetään, kun poiminta-algoritmi vähentää muille lähteville asiakirjoille varatut määrät, olemassa olevien poiminta-asiakirjojen määrät ja määrät, jotka on jo poimittu, mutta joita ei ole vielä toimitettu tai kulutettu.</span><span class="sxs-lookup"><span data-stu-id="728a9-115">To avoid this situation, the picking algorithm subtracts quantities that are reserved for other outbound documents, quantities on existing pick documents, and quantities that are picked but not yet shipped or consumed.</span></span>  

 <span data-ttu-id="728a9-116">Tulos näytetään **Saatav. ol. määrä poimittav.** -kentässä **Poimintatyökirja** -ikkunassa, jossa kenttä lasketaan dynaamisesti.</span><span class="sxs-lookup"><span data-stu-id="728a9-116">The result is displayed in the **Available Qty. to Pick** field in the **Pick Worksheet** window, where the field is calculated dynamically.</span></span> <span data-ttu-id="728a9-117">Arvo lasketaan myös silloin, kun käyttäjä luo fyysisen varastoinnin poiminnat suoraan lähteville asiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="728a9-117">The value is also calculated when users create warehouse picks directly for outbound documents.</span></span> <span data-ttu-id="728a9-118">Tällaiset lähtevät asiakirjat voisivat olla myyntitilauksia, tuotantomenekkiä tai saapuvia siirtoja, joiden tulos näkyy liittyvissä määräkentissä, kuten **Käsiteltävä määrä**.</span><span class="sxs-lookup"><span data-stu-id="728a9-118">Such outbound documents could be sales orders, production consumption, or outbound transfers, where the result is reflected in the related quantity fields, such as **Qty. to Handle**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="728a9-119">Varausten prioriteettiin liittyen varattava määrä vähennetään poimittavissa olevasta määrästä.</span><span class="sxs-lookup"><span data-stu-id="728a9-119">Concerning the priority of reservations, the quantity to reserve is subtracted from the quantity available to pick.</span></span> <span data-ttu-id="728a9-120">Esimerkiksi, jos poimintalokeroissa käytettävissä oleva määrä on 5 yksikköä, mutta 100 yksikköä on hyllytyslokeroissa, ja kun yrität varata enemmän kuin 5 yksikköä toiselle tilaukselle, järjestelmä näyttää virheilmoituksen, koska poimintalokeroissa on oltava tämä lisämäärä.</span><span class="sxs-lookup"><span data-stu-id="728a9-120">For example, if the quantity available in pick bins is 5 units, but 100 units are in put-away bins, then when you try to reserve more than 5 units for another order, an error message is displayed because the additional quantity must be available in pick bins.</span></span>  

### <a name="calculating-the-quantity-available-to-pick"></a><span data-ttu-id="728a9-121">Lasketaan poimittavissa olevaa määrää</span><span class="sxs-lookup"><span data-stu-id="728a9-121">Calculating the Quantity Available to Pick</span></span>  
 <span data-ttu-id="728a9-122">Poimintaan käytettävissä oleva määrä lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="728a9-122">The quantity available to pick is calculated as follows:</span></span>  

 <span data-ttu-id="728a9-123">poimittavissa olevaa määrää = määrä poimintavarastopaikoissa - määrä poiminnoissa ja siirroissa- – (varattu määrä poimintavarastopaikoissa + varattu määrä poiminnoissa ja siirroissa-)</span><span class="sxs-lookup"><span data-stu-id="728a9-123">quantity available to pick = quantity in pick bins - quantity on picks and movements – (reserved quantity in pick bins + reserved quantity on picks and movements)</span></span>  

 <span data-ttu-id="728a9-124">Seuraava kaavio sisältää laskelman eri elementit.</span><span class="sxs-lookup"><span data-stu-id="728a9-124">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="728a9-125">![Poimittavissa, varauksen päällekkäisyys](media/design_details_warehouse_management_availability_2.png "Poimittavissa, varauksen päällekkäisyys")</span><span class="sxs-lookup"><span data-stu-id="728a9-125">![Available to pick with reservation overlap](media/design_details_warehouse_management_availability_2.png "Available to pick with reservation overlap")</span></span>  

## <a name="quantity-available-to-reserve"></a><span data-ttu-id="728a9-126">Varattavissa oleva määrä</span><span class="sxs-lookup"><span data-stu-id="728a9-126">Quantity Available to Reserve</span></span>  
 <span data-ttu-id="728a9-127">Koska lokeron sisältö ja varaus ovat olemassa, varattavien nimikkeiden määrä tulee kohdistaa varauksilla lähtevän fyysisen varastoinnin asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="728a9-127">Because the concepts of bin content and reservation co-exist, the quantity of items that are available to reserve must be aligned with allocations to outbound warehouse documents.</span></span>  

 <span data-ttu-id="728a9-128">Kaikkien varastossa olevien nimikkeiden varaamisen tulisi olla mahdollista, lähtevien käsittelyssä olevia nimikkeitä lukuun ottamatta.</span><span class="sxs-lookup"><span data-stu-id="728a9-128">It should be possible to reserve all items in inventory, except those that have started outbound processing.</span></span> <span data-ttu-id="728a9-129">Näin ollen varattavissa oleva määrä määritetään kaikissa asiakirjoissa ja kaikissa lokerotyypeissä olevana määränä, lukuun ottamatta seuraavia lähteviä määriä:</span><span class="sxs-lookup"><span data-stu-id="728a9-129">Accordingly, the quantity that is available to reserve is defined as the quantity on all documents and all bin types, except the following outbound quantities:</span></span>  

-   <span data-ttu-id="728a9-130">Määrä rekisteröimättömissä poiminta-asiakirjoissa</span><span class="sxs-lookup"><span data-stu-id="728a9-130">Quantity on unregistered pick documents</span></span>  
-   <span data-ttu-id="728a9-131">Varastopaikoissa oleva määrä</span><span class="sxs-lookup"><span data-stu-id="728a9-131">Quantity in shipment bins</span></span>  
-   <span data-ttu-id="728a9-132">Määrä tuotannon valmisteluvarastopaikoissa</span><span class="sxs-lookup"><span data-stu-id="728a9-132">Quantity in to-production bins</span></span>  
-   <span data-ttu-id="728a9-133">Määrä avoimissa tuotannon varastopaikoissa</span><span class="sxs-lookup"><span data-stu-id="728a9-133">Quantity in open shop floor bins</span></span>  
-   <span data-ttu-id="728a9-134">Määrä kokoonpanon valmisteluvarastopaikoissa</span><span class="sxs-lookup"><span data-stu-id="728a9-134">Quantity in to-assembly bins</span></span>  
-   <span data-ttu-id="728a9-135">Muutosvarastopaikoissa oleva määrä</span><span class="sxs-lookup"><span data-stu-id="728a9-135">Quantity in adjustment bins</span></span>  

 <span data-ttu-id="728a9-136">Tulos näkyy **Saatavilla oleva kokonaismäärä** -kenttään **Varaus**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="728a9-136">The result is displayed in the **Total Available Quantity** field in the **Reservation** window.</span></span>  

 <span data-ttu-id="728a9-137">Varausrivillä oleva määrä, jota ei ole mahdollista varata, koska se on varattu varastossa, näytetään **F.var. kohdistettu määrä** -kentässä **Varaus** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="728a9-137">On a reservation line, the quantity that cannot be reserved, because it is allocated in the warehouse, is displayed in the **Qty. Allocated in Warehouse** field in the **Reservation** window.</span></span>  

### <a name="calculating-the-quantity-available-to-reserve"></a><span data-ttu-id="728a9-138">Lasketaan varattavissa olevaa määrää</span><span class="sxs-lookup"><span data-stu-id="728a9-138">Calculating the Quantity Available to Reserve</span></span>  
 <span data-ttu-id="728a9-139">Varattava määrä lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="728a9-139">The quantity available to reserve is calculated as follows:</span></span>  

 <span data-ttu-id="728a9-140">varattavissa oleva määrää = kokonaismäärä varastossa - määrä poiminnoissa ja siirroissa lähdeasiakirjoille - varattu määrä - määrä lähtevien varastopaikoissa</span><span class="sxs-lookup"><span data-stu-id="728a9-140">quantity available to reserve = total quantity in inventory - quantity on picks and movements for source documents - reserved quantity - quantity in outbound bins</span></span>  

 <span data-ttu-id="728a9-141">Seuraava kaavio sisältää laskelman eri elementit.</span><span class="sxs-lookup"><span data-stu-id="728a9-141">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="728a9-142">![Varattavissa varaston kohdistusten mukaisesti](media/design_details_warehouse_management_availability_3.png "Varattavissa varaston kohdistusten mukaisesti")</span><span class="sxs-lookup"><span data-stu-id="728a9-142">![Avaliable to reserve per warehouse allocation](media/design_details_warehouse_management_availability_3.png "Avaliable to reserve per warehouse allocation")</span></span>  

## <a name="see-also"></a><span data-ttu-id="728a9-143">Katso myös</span><span class="sxs-lookup"><span data-stu-id="728a9-143">See Also</span></span>  
 [<span data-ttu-id="728a9-144">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="728a9-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

