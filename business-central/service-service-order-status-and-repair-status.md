---
title: Huoltotilauksen tila ja korjauksen tila
description: Huoltotilaus-sivun Tila-kentällä (huoltotilauksen tilalla) ja Huoltotilaus-sivun Korjauksen tilakoodi -kentällä on tietty yhteys huoltohallinnon kohdistusalueella. Huoltotilauksen tila kuvastaa kaikkien huoltotilauksessa olevien huoltonimikkeiden korjauksen tilaa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: b9095cbfd1b8a55f525f0a3c4dcfad6cf56fc449
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386822"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="584f8-104">Huoltotilauksen tila ja korjauksen tila</span><span class="sxs-lookup"><span data-stu-id="584f8-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="584f8-105">**Huoltotilaus**-sivun **Tila**-kentällä (huoltotilauksen tilalla) ja **Huoltotilaus**-sivun **Korjauksen tilakoodi** -kentällä on tietty yhteys huoltohallinnon kohdistusalueella.</span><span class="sxs-lookup"><span data-stu-id="584f8-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="584f8-106">Huoltotilauksen tila kuvastaa kaikkien huoltotilauksessa olevien huoltonimikkeiden korjauksen tilaa.</span><span class="sxs-lookup"><span data-stu-id="584f8-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="584f8-107">Nämä kaksi tilakenttää eivät liity huoltotilausotsikon **Vapautustila**-kenttään, joka määrittää sen, miten fyysinen varasto käsittelee huoltonimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="584f8-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="584f8-108">Kun huoltotilauksessa olevan huoltonimikkeen korjauksen tilaa muutetaan, ohjelma päivittää huoltotilauksen tilan.</span><span class="sxs-lookup"><span data-stu-id="584f8-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="584f8-109">Jotta ohjelma voisi näyttää tilan, joka kuvastaa yksittäisten huoltonimikkeiden korjauksen kokonaistilaa, seuraavat tulee määritellä:</span><span class="sxs-lookup"><span data-stu-id="584f8-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="584f8-110">Huoltotilauksen tila, johon kukin korjauksen tila on linkitetty.</span><span class="sxs-lookup"><span data-stu-id="584f8-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="584f8-111">Kunkin huoltotilauksen tilavaihtoehdon prioriteettitaso.</span><span class="sxs-lookup"><span data-stu-id="584f8-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="584f8-112">Kun huoltotarjous muunnetaan huoltotilaukseksi, ohjelma muuttaa jokaisen tilauksessa olevan huoltonimikkeen korjauksen tilaksi **Alku** ja huoltotilauksen tilaksi **Odottava**.</span><span class="sxs-lookup"><span data-stu-id="584f8-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="584f8-113">Ennen kuin voit luoda huoltotilauksia, sinun on asetettava korjauksen tilat ja huollon tilojen prioriteetit.</span><span class="sxs-lookup"><span data-stu-id="584f8-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="584f8-114">Lisätietoja on kohdassa [Huoltotilausten ja korjausten tilojen määrittäminen](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="584f8-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="584f8-115">Huoltotilauksen tilan määrittäminen korjauksen tilaa varten</span><span class="sxs-lookup"><span data-stu-id="584f8-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="584f8-116">Jokainen korjauksen tila on linkitetty tiettyyn huoltotilauksen tilaan.</span><span class="sxs-lookup"><span data-stu-id="584f8-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="584f8-117">Huoltotilauksen tilan vaihtoehdot ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="584f8-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="584f8-118">**Odottava**</span><span class="sxs-lookup"><span data-stu-id="584f8-118">**Pending**</span></span>
* <span data-ttu-id="584f8-119">**Työn alla**</span><span class="sxs-lookup"><span data-stu-id="584f8-119">**In Process**</span></span>
* <span data-ttu-id="584f8-120">**Estossa**</span><span class="sxs-lookup"><span data-stu-id="584f8-120">**On Hold**</span></span>
* <span data-ttu-id="584f8-121">**Valmis**</span><span class="sxs-lookup"><span data-stu-id="584f8-121">**Finished**</span></span>

<span data-ttu-id="584f8-122">Korjauksen tilojen vaihtoehdot ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="584f8-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="584f8-123">**Alku**</span><span class="sxs-lookup"><span data-stu-id="584f8-123">**Initial**</span></span>
* <span data-ttu-id="584f8-124">**Työn alla**</span><span class="sxs-lookup"><span data-stu-id="584f8-124">**In Process**</span></span>
* <span data-ttu-id="584f8-125">**Lykätty**</span><span class="sxs-lookup"><span data-stu-id="584f8-125">**Referred**</span></span>
* <span data-ttu-id="584f8-126">**Osittain huollettu**</span><span class="sxs-lookup"><span data-stu-id="584f8-126">**Partly Serviced**</span></span>
* <span data-ttu-id="584f8-127">**Tarjous valmis**</span><span class="sxs-lookup"><span data-stu-id="584f8-127">**Quote Finished**</span></span>
* <span data-ttu-id="584f8-128">**Odotetaan asiakasta**</span><span class="sxs-lookup"><span data-stu-id="584f8-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="584f8-129">**Varaosa tilattu**</span><span class="sxs-lookup"><span data-stu-id="584f8-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="584f8-130">**Varaosa vastaanotettu**</span><span class="sxs-lookup"><span data-stu-id="584f8-130">**Spare Part Received**</span></span>
* <span data-ttu-id="584f8-131">**Valmis**</span><span class="sxs-lookup"><span data-stu-id="584f8-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="584f8-132">Odottava</span><span class="sxs-lookup"><span data-stu-id="584f8-132">Pending</span></span>

<span data-ttu-id="584f8-133">Huoltotilauksen tila **Odottava** tarkoittaa sitä, että huolto voi alkaa tai jatkua milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="584f8-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="584f8-134">Tämän vuoksi korjauksen tilan vaihtoehdot **Alku**, **Lykätty**, **Osittain huollettu** ja **Varaosa vastaanotettu** voidaan kaikki linkittää kyseiseen huoltotilauksen tilaan.</span><span class="sxs-lookup"><span data-stu-id="584f8-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="584f8-135">Työn alla</span><span class="sxs-lookup"><span data-stu-id="584f8-135">In Process</span></span>

<span data-ttu-id="584f8-136">Huoltotilauksen tila **Työn alla** tarkoittaa sitä, että huolto on käynnissä.</span><span class="sxs-lookup"><span data-stu-id="584f8-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="584f8-137">Tämän vuoksi korjauksen tilan vaihtoehdot **Työn alla** ja **Varaosa tilattu** voidaan molemmat linkittää kyseiseen huoltotilauksen tilaan.</span><span class="sxs-lookup"><span data-stu-id="584f8-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="584f8-138">Jos **Varaosa tilattu** -tila linkitetään huoltotilauksen **Työn alla** -tilaan, myös **Varaosa vastaanotettu** -tila tulee linkittää tähän huoltotilauksen tilaan.</span><span class="sxs-lookup"><span data-stu-id="584f8-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="584f8-139">Estossa</span><span class="sxs-lookup"><span data-stu-id="584f8-139">On Hold</span></span>

<span data-ttu-id="584f8-140">Huoltotilauksen tila **Estossa** tarkoittaa sitä, että huolto on tällä hetkellä estossa, koska ennen huollon aloittamista täytyy odottaa asiakkaan vastausta tai varaosia.</span><span class="sxs-lookup"><span data-stu-id="584f8-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="584f8-141">Tämän vuoksi korjauksen tilan vaihtoehdot **Tarjous valmis**, **Varaosa tilattu** ja **Odotetaan asiakasta** voidaan kaikki linkittää kyseiseen huoltotilauksen tilaan.</span><span class="sxs-lookup"><span data-stu-id="584f8-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="584f8-142">Valmis</span><span class="sxs-lookup"><span data-stu-id="584f8-142">Finished</span></span>

<span data-ttu-id="584f8-143">Huoltotilauksen tila **Valmis** tarkoittaa sitä, että huolto on suoritettu loppuun.</span><span class="sxs-lookup"><span data-stu-id="584f8-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="584f8-144">Tämän vuoksi korjauksen tila **Valmis** on linkitetty kyseiseen tilaan.</span><span class="sxs-lookup"><span data-stu-id="584f8-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="584f8-145">Prioriteetin määritteleminen huoltotilauksen tilalle</span><span class="sxs-lookup"><span data-stu-id="584f8-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="584f8-146">Kun muutat (tai ohjelma muuttaa) huoltonimikkeen korjauksen tilaa, ohjelma etsii huoltotilauksen tilan vaihtoehdot, jotka on linkitetty kaikkien tilauksessa olevien huoltonimikkeiden eri korjauksen tilan vaihtoehtoihin.</span><span class="sxs-lookup"><span data-stu-id="584f8-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="584f8-147">Jos huoltonimikkeet on linkitetty kahteen tai useampaan huoltotilauksen tilan vaihtoehtoon, ohjelma valitsee huoltotilauksen tilan, jolla on korkein prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="584f8-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="584f8-148">Sinun täytyy päättää, mikä huoltotilauksen tila sisältää tärkeimmät tiedot huoltotilauksen tilasta, ja määritellä kyseiselle tilalle korkein prioriteetti ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="584f8-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="584f8-149">Kun luot uuden huoltotilauksen ja lisäät siihen huoltonimikkeitä, huoltotilauksen otsikon **Prioriteetti**-kenttä päivitetään huoltonimikkeiden prioriteettien perusteella.</span><span class="sxs-lookup"><span data-stu-id="584f8-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="584f8-150">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="584f8-150">Example</span></span>

<span data-ttu-id="584f8-151">Tavallinen prioriteettitason määrittely voisi olla seuraavanlainen:</span><span class="sxs-lookup"><span data-stu-id="584f8-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="584f8-152">Työn alla - Korkea</span><span class="sxs-lookup"><span data-stu-id="584f8-152">In Process - High</span></span>  
* <span data-ttu-id="584f8-153">Odottava - Melko korkea</span><span class="sxs-lookup"><span data-stu-id="584f8-153">Pending - Medium high</span></span>  
* <span data-ttu-id="584f8-154">Estossa - Melko matala</span><span class="sxs-lookup"><span data-stu-id="584f8-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="584f8-155">Valmis - Matala</span><span class="sxs-lookup"><span data-stu-id="584f8-155">Finished - Low</span></span>  

<span data-ttu-id="584f8-156">Esimerkiksi jos yhdellä huoltonimikkeellä on korjauksen tilana **Alku** (joka on linkitetty huoltotilauksen tilaan **Odottava**), toisella tilana on **Työn alla** (joka on linkitetty huoltotilauksen tilaan **Työn alla**) ja kolmannella **Varaosa tilattu** (joka on linkitetty huoltotilauksen tilaan **Estossa**), seurauksena syntyvä huoltotilauksen tila on **Työn alla**, koska sillä on korkein prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="584f8-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="584f8-157">Katso myös</span><span class="sxs-lookup"><span data-stu-id="584f8-157">See Also</span></span>

[<span data-ttu-id="584f8-158">Huoltotilausten ja -korjausten tilan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="584f8-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="584f8-159">Huoltohallinnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="584f8-159">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]