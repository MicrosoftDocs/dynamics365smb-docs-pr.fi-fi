---
title: Rakennetiedot – Sallitun ylityksen alapuolella pysytteleminen | Microsoft Docs
description: Kun käytössä on Enimmäismäärä ja Kiinteä uusintatil. määrä suunnittelujärjestelmä keskittyy oletettuun varastoon vain annetulla aikavälillä. Tämä tarkoittaa sitä, että suunnittelujärjestelmä voi ehdottaa tarpeetonta tarjontaa, kun annetun aikavälin ulkopuolella tapahtuu negatiivisia tai positiivisia tarjonnan muutoksia.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 250de9bf843dac7bfca08d8f3a9dcd4ea44586df
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240048"
---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="df1bf-104">Rakennetiedot: sallitun ylityksen alapuolella pysytteleminen</span><span class="sxs-lookup"><span data-stu-id="df1bf-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="df1bf-105">Kun Enimmäismäärä- ja Kiinteä uusintatil. määrä -käytäntöjä käytetään, suunnittelujärjestelmä keskittyy oletettuun varastoon vain annetulla aikavälillä.</span><span class="sxs-lookup"><span data-stu-id="df1bf-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="df1bf-106">Tämä tarkoittaa sitä, että suunnittelujärjestelmä voi ehdottaa tarpeetonta tarjontaa, kun annetun aikavälin ulkopuolella tapahtuu negatiivisia tai positiivisia tarjonnan muutoksia.</span><span class="sxs-lookup"><span data-stu-id="df1bf-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="df1bf-107">Jos tästä syystä ehdotetaan tarpeetonta tarjontaa, suunnittelujärjestelmä laskee mihin määrään tarjonta tulee vähentää (tai poistaa) tarpeettoman tarjonnan välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="df1bf-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="df1bf-108">Tätä määrää kutsutaan ylivuototasoksi.</span><span class="sxs-lookup"><span data-stu-id="df1bf-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="df1bf-109">Ylitys ilmoitetaan suunnittelurivinä, jossa on **Muuta määrä (vähennys)**- tai **Peruuta**-toiminto, ja seuraava varoitusviesti:</span><span class="sxs-lookup"><span data-stu-id="df1bf-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="df1bf-110">*Huomio: arvioitu varastomäärä [xx] on korkeampi kuin sallittu ylitys [xx] [xx] eräpäivänä [xx].*</span><span class="sxs-lookup"><span data-stu-id="df1bf-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="df1bf-111">![Varaston ylivuototaso](media/supplyplanning_2_overflow1_new.png "Varaston ylivuototaso")</span><span class="sxs-lookup"><span data-stu-id="df1bf-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "Inventory overflow level")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="df1bf-112">Lasketaan sallittua ylitystä</span><span class="sxs-lookup"><span data-stu-id="df1bf-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="df1bf-113">Ylitystaso lasketaan eri tavoin riippuen suunnitteluasetuksista.</span><span class="sxs-lookup"><span data-stu-id="df1bf-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="df1bf-114">Enimmäismäärä-uusintatilaustapa</span><span class="sxs-lookup"><span data-stu-id="df1bf-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="df1bf-115">Sallittu ylitys = enimmäisvarasto</span><span class="sxs-lookup"><span data-stu-id="df1bf-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="df1bf-116">Jos vähimmäistilausmäärä on olemassa, se lisätään seuraavasti: sallittu ylitys = enimmäisvarasto + vähimmäistilausmäärä.</span><span class="sxs-lookup"><span data-stu-id="df1bf-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="df1bf-117">Kiinteän uusintatilausmäärän uusintatilaustapa</span><span class="sxs-lookup"><span data-stu-id="df1bf-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="df1bf-118">Sallittu ylitys = uusintatilausmäärä + uusintatilauspiste</span><span class="sxs-lookup"><span data-stu-id="df1bf-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="df1bf-119">Jos vähimmäistilausmäärä on korkeampi kuin uusintatilauspiste, se korvaa seuraavasti: sallittu ylitys = uusintatilausmäärä + vähimmäistilausmäärä</span><span class="sxs-lookup"><span data-stu-id="df1bf-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="df1bf-120">Tilauskerrannainen</span><span class="sxs-lookup"><span data-stu-id="df1bf-120">Order Multiple</span></span>  
<span data-ttu-id="df1bf-121">Jos tilauskerrannainen on olemassa, se säätää sekä enimmäismäärän että kiinteän uusintatilaustavan sallittua ylitystä.</span><span class="sxs-lookup"><span data-stu-id="df1bf-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="df1bf-122">Suunnittelurivin luominen ylitys-varoituksella</span><span class="sxs-lookup"><span data-stu-id="df1bf-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="df1bf-123">Suunnittelurivi luodaan, kun oletettu varasto on aikavälin lopussa suurempi kuin sallittu ylitys olemassa olevan tarjonnan vuoksi.</span><span class="sxs-lookup"><span data-stu-id="df1bf-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="df1bf-124">Kun mahdollisesta tarpeettomasta tarjonnasta varoitetaan, suunnittelurivillä on varoitusviesti, **Hyväksy toimenpideviesti** -kenttää ei ole valittu ja toimenpideviesti on Peruuta tai Muuta määrä.</span><span class="sxs-lookup"><span data-stu-id="df1bf-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="df1bf-125">Lasketaan suunnittelurivin määrää</span><span class="sxs-lookup"><span data-stu-id="df1bf-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="df1bf-126">Suunnittelurivin määrä = nykyisen tarjonnan määrä (oletettu varasto – sallittu ylitys)</span><span class="sxs-lookup"><span data-stu-id="df1bf-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="df1bf-127">Kuten kaikkien varoitusrivien kohdalla, kaikki tilauksen enimmäis-/vähimmäismäärät ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="df1bf-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="df1bf-128">Toimintoviestin tyypin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="df1bf-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="df1bf-129">Jos suunnittelurivin määrä on suurempi kuin 0, toimenpideviesti on Muuta määrä</span><span class="sxs-lookup"><span data-stu-id="df1bf-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="df1bf-130">Jos suunnittelurivin määrä on yhtä suuri tai pienempi kuin 0, toimenpideviesti on Peruuta</span><span class="sxs-lookup"><span data-stu-id="df1bf-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="df1bf-131">Varoitusviestin luonti</span><span class="sxs-lookup"><span data-stu-id="df1bf-131">Composing the Warning Message</span></span>  
<span data-ttu-id="df1bf-132">Ylivuodon tapauksessa **Ei-seuratut suunnitteluelementit** -sivulla on varoitusviesti, jossa on seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="df1bf-132">In case of overflow, the **Untracked Planning Elements** page displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="df1bf-133">Käsitelty varastotaso, joka laukaisi varoituksen</span><span class="sxs-lookup"><span data-stu-id="df1bf-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="df1bf-134">Laskettu ylitystaso</span><span class="sxs-lookup"><span data-stu-id="df1bf-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="df1bf-135">Tarjontatapahtuman eräpäivä.</span><span class="sxs-lookup"><span data-stu-id="df1bf-135">The due date of the supply event.</span></span>  

<span data-ttu-id="df1bf-136">Esimerkki: Suunniteltu varasto 120 on suurempi kuin sallittu ylitys 60 kohteessa 28-01-11.</span><span class="sxs-lookup"><span data-stu-id="df1bf-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="df1bf-137">Esimerkkitilanne</span><span class="sxs-lookup"><span data-stu-id="df1bf-137">Scenario</span></span>  
<span data-ttu-id="df1bf-138">Tässä tilanteessa asiakas muuttaa myyntitilauksen arvosta 70 kappaletta arvoksi 40 kappaletta suunnitteluajojen välillä.</span><span class="sxs-lookup"><span data-stu-id="df1bf-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="df1bf-139">Ylitystoiminto alkaa vähentämään tilausta, jota ehdotettiin alkuperäiselle myyntimäärälle.</span><span class="sxs-lookup"><span data-stu-id="df1bf-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="df1bf-140">Nimikkeen asetus</span><span class="sxs-lookup"><span data-stu-id="df1bf-140">Item setup</span></span>  

|<span data-ttu-id="df1bf-141">Uusintatilaustapa</span><span class="sxs-lookup"><span data-stu-id="df1bf-141">Reordering Policy</span></span>|<span data-ttu-id="df1bf-142">Enimmäismäärä</span><span class="sxs-lookup"><span data-stu-id="df1bf-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="df1bf-143">Enimmäistilausmäärä</span><span class="sxs-lookup"><span data-stu-id="df1bf-143">Maximum Order Quantity</span></span>|<span data-ttu-id="df1bf-144">100</span><span class="sxs-lookup"><span data-stu-id="df1bf-144">100</span></span>|  
|<span data-ttu-id="df1bf-145">Uusintatilauspiste</span><span class="sxs-lookup"><span data-stu-id="df1bf-145">Reorder Point</span></span>|<span data-ttu-id="df1bf-146">50</span><span class="sxs-lookup"><span data-stu-id="df1bf-146">50</span></span>|  
|<span data-ttu-id="df1bf-147">Varasto</span><span class="sxs-lookup"><span data-stu-id="df1bf-147">Inventory</span></span>|<span data-ttu-id="df1bf-148">80</span><span class="sxs-lookup"><span data-stu-id="df1bf-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="df1bf-149">Tilanne ennen myynnin vähenemistä</span><span class="sxs-lookup"><span data-stu-id="df1bf-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="df1bf-150">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="df1bf-150">Event</span></span>|<span data-ttu-id="df1bf-151">Muuta määrä</span><span class="sxs-lookup"><span data-stu-id="df1bf-151">Change Qty.</span></span>|<span data-ttu-id="df1bf-152">Suunniteltu varasto</span><span class="sxs-lookup"><span data-stu-id="df1bf-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="df1bf-153">Yksi päivä</span><span class="sxs-lookup"><span data-stu-id="df1bf-153">Day one</span></span>|<span data-ttu-id="df1bf-154">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="df1bf-154">None</span></span>|<span data-ttu-id="df1bf-155">80</span><span class="sxs-lookup"><span data-stu-id="df1bf-155">80</span></span>|  
|<span data-ttu-id="df1bf-156">Myynti</span><span class="sxs-lookup"><span data-stu-id="df1bf-156">Sale</span></span>|<span data-ttu-id="df1bf-157">-70</span><span class="sxs-lookup"><span data-stu-id="df1bf-157">-70</span></span>|<span data-ttu-id="df1bf-158">10</span><span class="sxs-lookup"><span data-stu-id="df1bf-158">10</span></span>|  
|<span data-ttu-id="df1bf-159">Aikavälin loppu</span><span class="sxs-lookup"><span data-stu-id="df1bf-159">End of time bucket</span></span>|<span data-ttu-id="df1bf-160">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="df1bf-160">None</span></span>|<span data-ttu-id="df1bf-161">10</span><span class="sxs-lookup"><span data-stu-id="df1bf-161">10</span></span>|  
|<span data-ttu-id="df1bf-162">Ehdota uutta ostopalautustilausta</span><span class="sxs-lookup"><span data-stu-id="df1bf-162">Suggest new purchase order</span></span>|<span data-ttu-id="df1bf-163">+90</span><span class="sxs-lookup"><span data-stu-id="df1bf-163">+90</span></span>|<span data-ttu-id="df1bf-164">100</span><span class="sxs-lookup"><span data-stu-id="df1bf-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="df1bf-165">Tilanne myynnin vähenemisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="df1bf-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="df1bf-166">Vaihtoraha</span><span class="sxs-lookup"><span data-stu-id="df1bf-166">Change</span></span>|<span data-ttu-id="df1bf-167">Muuta määrä</span><span class="sxs-lookup"><span data-stu-id="df1bf-167">Change Qty.</span></span>|<span data-ttu-id="df1bf-168">Suunniteltu varasto</span><span class="sxs-lookup"><span data-stu-id="df1bf-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="df1bf-169">Yksi päivä</span><span class="sxs-lookup"><span data-stu-id="df1bf-169">Day one</span></span>|<span data-ttu-id="df1bf-170">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="df1bf-170">None</span></span>|<span data-ttu-id="df1bf-171">80</span><span class="sxs-lookup"><span data-stu-id="df1bf-171">80</span></span>|  
|<span data-ttu-id="df1bf-172">Myynti</span><span class="sxs-lookup"><span data-stu-id="df1bf-172">Sale</span></span>|<span data-ttu-id="df1bf-173">-40</span><span class="sxs-lookup"><span data-stu-id="df1bf-173">-40</span></span>|<span data-ttu-id="df1bf-174">40</span><span class="sxs-lookup"><span data-stu-id="df1bf-174">40</span></span>|  
|<span data-ttu-id="df1bf-175">Osto</span><span class="sxs-lookup"><span data-stu-id="df1bf-175">Purchase</span></span>|<span data-ttu-id="df1bf-176">+90</span><span class="sxs-lookup"><span data-stu-id="df1bf-176">+90</span></span>|<span data-ttu-id="df1bf-177">130</span><span class="sxs-lookup"><span data-stu-id="df1bf-177">130</span></span>|  
|<span data-ttu-id="df1bf-178">Aikavälin loppu</span><span class="sxs-lookup"><span data-stu-id="df1bf-178">End of time bucket</span></span>|<span data-ttu-id="df1bf-179">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="df1bf-179">None</span></span>|<span data-ttu-id="df1bf-180">130</span><span class="sxs-lookup"><span data-stu-id="df1bf-180">130</span></span>|  
|<span data-ttu-id="df1bf-181">Ehdotus tilauksen pienentämiseksi</span><span class="sxs-lookup"><span data-stu-id="df1bf-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="df1bf-182">tilaus arvosta 90 arvoon 60</span><span class="sxs-lookup"><span data-stu-id="df1bf-182">order from 90 to 60</span></span>|<span data-ttu-id="df1bf-183">-30</span><span class="sxs-lookup"><span data-stu-id="df1bf-183">-30</span></span>|<span data-ttu-id="df1bf-184">100</span><span class="sxs-lookup"><span data-stu-id="df1bf-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="df1bf-185">Tuloksena suunnittelurivit</span><span class="sxs-lookup"><span data-stu-id="df1bf-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="df1bf-186">Järjestelmä luo yhden suunnittelurivin (varoitus) oston vähentämiseksi 30 yksiköllä 90 yksiköstä 60 yksikköön, jotta arvioitu varasto on 100 sallitun ylityksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="df1bf-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="df1bf-187">![Suunnittelu ylivuototason mukaisesti](media/nav_app_supply_planning_2_overflow2.png "Suunnittelu ylivuototason mukaisesti")</span><span class="sxs-lookup"><span data-stu-id="df1bf-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "Plan according to overflow level")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="df1bf-188">Ilman ylivuototoimintoa varoitusta ei luoda, jos oletetun varaston taso ylittää enimmäisvaraston.</span><span class="sxs-lookup"><span data-stu-id="df1bf-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="df1bf-189">Tämä voi aiheuttaa tarpeettoman tarjonnan, joka on 30.</span><span class="sxs-lookup"><span data-stu-id="df1bf-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="df1bf-190">Katso myös</span><span class="sxs-lookup"><span data-stu-id="df1bf-190">See Also</span></span>  
<span data-ttu-id="df1bf-191">[Rakennetiedot: Uusintatilauskäytännöt](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="df1bf-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="df1bf-192">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="df1bf-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="df1bf-193">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="df1bf-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="df1bf-194">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="df1bf-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
