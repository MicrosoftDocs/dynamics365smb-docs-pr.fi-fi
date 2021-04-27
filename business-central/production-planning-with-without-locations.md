---
title: Suunnittelu sijainteja käyttämällä tai ilman niitä | Microsoft Docs
description: Kysyntäriveillä tehtävä sijaintikoodeja käyttävä suunnittelu tai ilman niitä tehtävä suunnittelu on toiminto, jonka ymmärtäminen on tärkeää.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b182a66984ea0345e7f33e1292839d1ecfad4bfd
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787550"
---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="ac470-103">Suunnittelu sijainteja käyttämällä tai ilman niitä</span><span class="sxs-lookup"><span data-stu-id="ac470-103">Planning With or Without Locations</span></span>
<span data-ttu-id="ac470-104">Käytetään sijaintikoodeja kysyntäriveillä suunnittelussa tai ei, suunnittelujärjestelmä toimii suoraviivaisesti seuraavien asioiden toteutuessa:</span><span class="sxs-lookup"><span data-stu-id="ac470-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="ac470-105">Kysyntäriveillä on aina sijaintikoodi, ja järjestelmä käyttää varastointiyksiköiden kaikkia ominaisuuksia, myös asiaankuuluvia sijaintiasetuksia.</span><span class="sxs-lookup"><span data-stu-id="ac470-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="ac470-106">Kysyntäriveillä ei missään tilanteessa käytetä sijaintikoodeja, eikä järjestelmä käytä varastointiyksiköitä eikä sijaintiasetuksia (ks. viimein esimerkkitilanne jäljempänä).</span><span class="sxs-lookup"><span data-stu-id="ac470-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="ac470-107">Jos kysyntäriveillä toisinaan on sijaintikoodeja ja toisinaan taas ei, suunnittelujärjestelmä noudattaa asetuksien mukaan tiettyjä sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="ac470-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="ac470-108">Kysyntä sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-108">Demand at Location</span></span>  
<span data-ttu-id="ac470-109">Kun suunnittelujärjestelmä havaitsee kysyntää tietyssä sijainnissa (rivi, jossa on sijaintikoodi), järjestelmä ryhtyy toimimaan. Toimintamalli määräytyy kolmen keskeisen asetusarvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="ac470-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="ac470-110">Järjestelmä tarkistaa kyseiset kolme arvoa järjestyksessä suunnitteluajon aikana ja toteuttaa suunnitelmat niiden mukaan:</span><span class="sxs-lookup"><span data-stu-id="ac470-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="ac470-111">Onko **Sijainti pakollinen** -kentässä valintamerkki?</span><span class="sxs-lookup"><span data-stu-id="ac470-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="ac470-112">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="ac470-112">If yes, then:</span></span>  

2.  <span data-ttu-id="ac470-113">Onko nimikkeellä varastointiyksikkö?</span><span class="sxs-lookup"><span data-stu-id="ac470-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="ac470-114">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="ac470-114">If yes, then:</span></span>  

    <span data-ttu-id="ac470-115">Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ac470-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="ac470-116">Toimet, kun vastaus on Ei:</span><span class="sxs-lookup"><span data-stu-id="ac470-116">If no, then:</span></span>  

3.  <span data-ttu-id="ac470-117">Onko **Komponentit sijainnissa** -kentässä vaadittu sijaintikoodi?</span><span class="sxs-lookup"><span data-stu-id="ac470-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="ac470-118">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="ac470-118">If yes, then:</span></span>  

    <span data-ttu-id="ac470-119">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ac470-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="ac470-120">Toimet, kun vastaus on Ei:</span><span class="sxs-lookup"><span data-stu-id="ac470-120">If no, then:</span></span>  

    <span data-ttu-id="ac470-121">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä*, Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="ac470-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="ac470-122">( *Tilaus*-uusintatilaustapaa käyttävät nimikkeet käyttävät yhä  *Tilaus*-uusintatilaustapaa sekä muita asetuksia.)</span><span class="sxs-lookup"><span data-stu-id="ac470-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ac470-123">Tämä "minimaalinen vaihtoehto" kattaa vain tarkan kysynnän.</span><span class="sxs-lookup"><span data-stu-id="ac470-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="ac470-124">Kaikki määritetyt suunnitteluparametrit ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="ac470-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="ac470-125">Tutustu jäljempänä oleviin esimerkkitilanteisiin.</span><span class="sxs-lookup"><span data-stu-id="ac470-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="ac470-126">Kysyntä "tyhjässä sijainnissa"</span><span class="sxs-lookup"><span data-stu-id="ac470-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="ac470-127">Vaikka **Sijainti pakollinen** -valintaruutu olisi valittu, järjestelmä sallii kysyntärivien luonnin ilman sijaintikoodia. Tätä kutsutaan myös *TYHJÄKSI* sijainniksi.</span><span class="sxs-lookup"><span data-stu-id="ac470-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="ac470-128">Tämä on järjestelmälle poikkeustilanne, koska sijaintien käsittelyä varten on määritetty useita määritysarvoja (esimerkki yllä). Suunnitteluohjelma ei tämän vuoksi luo tällaiselle kysyntäriville suunnitteluriviä.</span><span class="sxs-lookup"><span data-stu-id="ac470-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="ac470-129">Jos **Sijainti pakollinen** -kenttää ei ole valittu mutta käytössä on sijainnin asetusarvoja, kyseessä on poikkeustilanne. Suunnittelujärjestelmä reagoi siihen tuottamalla minimaalisen vaihtoehdon:</span><span class="sxs-lookup"><span data-stu-id="ac470-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="ac470-130">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä *Tilaus)*, Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="ac470-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="ac470-131">Tutustu jäljempänä oleviin määritystilanteisiin.</span><span class="sxs-lookup"><span data-stu-id="ac470-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="ac470-132">Asetukset (1):</span><span class="sxs-lookup"><span data-stu-id="ac470-132">Setup 1:</span></span>  

-   <span data-ttu-id="ac470-133">Sijainti pakollinen = *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="ac470-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="ac470-134">Varastointiyksikkö on määritetty kohteeseen  *PUNAINEN*</span><span class="sxs-lookup"><span data-stu-id="ac470-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="ac470-135">Komponentit sijainnissa =  *SININEN*</span><span class="sxs-lookup"><span data-stu-id="ac470-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="ac470-136">Tapaus 1.1: Kysyntää *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="ac470-137">Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti (mahdolliset siirrot mukaan lukien).</span><span class="sxs-lookup"><span data-stu-id="ac470-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="ac470-138">Tapaus 1.2: Kysyntää *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="ac470-139">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ac470-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="ac470-140">Tapaus 1.3: Kysyntää  *VIHREÄ*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="ac470-141">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="ac470-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="ac470-142">Tapaus 1.4: Kysyntää  *TYHJÄ* -sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="ac470-143">Nimikettä ei suunnitella, koska kysyntäriville ei ole määritetty sijaintia.</span><span class="sxs-lookup"><span data-stu-id="ac470-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="ac470-144">Asetukset (2):</span><span class="sxs-lookup"><span data-stu-id="ac470-144">Setup 2:</span></span>  

-   <span data-ttu-id="ac470-145">Sijainti pakollinen = *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="ac470-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="ac470-146">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="ac470-146">No SKU exists</span></span>  
-   <span data-ttu-id="ac470-147">Komponentit sijainnissa =  *SININEN*</span><span class="sxs-lookup"><span data-stu-id="ac470-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="ac470-148">Tapaus 2.1: Kysyntää  *PUNAINEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="ac470-149">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="ac470-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="ac470-150">Tapaus 2.2: Kysyntää *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="ac470-151">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ac470-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="ac470-152">Asetukset (3):</span><span class="sxs-lookup"><span data-stu-id="ac470-152">Setup 3:</span></span>  

-   <span data-ttu-id="ac470-153">Sijainti pakollinen = *Ei*</span><span class="sxs-lookup"><span data-stu-id="ac470-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="ac470-154">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="ac470-154">No SKU exists</span></span>  
-   <span data-ttu-id="ac470-155">Komponentit sijainnissa =  *SININEN*</span><span class="sxs-lookup"><span data-stu-id="ac470-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="ac470-156">Tapaus 3.1: Kysyntää  *PUNAINEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="ac470-157">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="ac470-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="ac470-158">Tapaus 3.2: Kysyntää *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="ac470-159">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ac470-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="ac470-160">Tapaus 3.3: Kysyntää  *TYHJÄ* -sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="ac470-161">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="ac470-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="ac470-162">Asetukset (4):</span><span class="sxs-lookup"><span data-stu-id="ac470-162">Setup 4:</span></span>  

-   <span data-ttu-id="ac470-163">Sijainti pakollinen = *Ei*</span><span class="sxs-lookup"><span data-stu-id="ac470-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="ac470-164">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="ac470-164">No SKU exists</span></span>  
-   <span data-ttu-id="ac470-165">Komponentit sijainnissa =  *TYHJÄ*</span><span class="sxs-lookup"><span data-stu-id="ac470-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="ac470-166">Tapaus 4.1: Kysyntää  *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="ac470-167">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="ac470-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="ac470-168">Tapaus 4.2: Kysyntää  *TYHJÄ* -sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac470-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="ac470-169">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ac470-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="ac470-170">Kuten viimeinen esimerkkitilanne osoittaa, kaikkien sijainteihin liittyvien asetusarvojen poistaminen käytöstä on ainoa tapa saada oikeita tuloksia, kun kysyntärivillä ei ole sijaintikoodia.</span><span class="sxs-lookup"><span data-stu-id="ac470-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="ac470-171">Vastaavasti varastointiyksiköiden käyttäminen on ainoa tapa saada vakaita suunnittelutuloksia sijaintien kysyntään liittyen.</span><span class="sxs-lookup"><span data-stu-id="ac470-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="ac470-172">Jos suunnittelet usein kysyntää sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa ehdottomasti käyttää.</span><span class="sxs-lookup"><span data-stu-id="ac470-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ac470-173">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ac470-173">See Also</span></span>
<span data-ttu-id="ac470-174">[Suunnittelu](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="ac470-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="ac470-175">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ac470-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="ac470-176">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ac470-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="ac470-177">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="ac470-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ac470-178">Osto</span><span class="sxs-lookup"><span data-stu-id="ac470-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ac470-179">[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="ac470-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="ac470-180">Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu</span><span class="sxs-lookup"><span data-stu-id="ac470-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="ac470-181">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ac470-181">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]