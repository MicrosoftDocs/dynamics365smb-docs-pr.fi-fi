---
title: "Suunnittelu sijainteja käyttämällä tai ilman niitä | Microsoft Docs"
description: "Kysyntäriveillä tehtävä sijaintikoodeja käyttävä suunnittelu tai ilman niitä tehtävä suunnittelu on toiminto, jonka ymmärtäminen on tärkeää."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a2043b50e9f398839034c87e8f0fb42f68d8c036
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="a396a-103">Suunnittelu sijainteja käyttämällä tai ilman niitä</span><span class="sxs-lookup"><span data-stu-id="a396a-103">Planning With or Without Locations</span></span>
<span data-ttu-id="a396a-104">Käytetään sijaintikoodeja kysyntäriveillä suunnittelussa tai ei, suunnittelujärjestelmä toimii suoraviivaisesti seuraavien asioiden toteutuessa:</span><span class="sxs-lookup"><span data-stu-id="a396a-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="a396a-105">Kysyntäriveillä on aina sijaintikoodi, ja järjestelmä käyttää varastointiyksiköiden kaikkia ominaisuuksia, myös asiaankuuluvia sijaintiasetuksia.</span><span class="sxs-lookup"><span data-stu-id="a396a-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="a396a-106">Kysyntäriveillä ei missään tilanteessa käytetä sijaintikoodeja, eikä järjestelmä käytä varastointiyksiköitä eikä sijaintiasetuksia (ks. viimein esimerkkitilanne jäljempänä).</span><span class="sxs-lookup"><span data-stu-id="a396a-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="a396a-107">Jos kysyntäriveillä toisinaan on sijaintikoodeja ja toisinaan taas ei, suunnittelujärjestelmä noudattaa asetuksien mukaan tiettyjä sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="a396a-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="a396a-108">Kysyntä sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-108">Demand at Location</span></span>  
<span data-ttu-id="a396a-109">Kun suunnittelujärjestelmä havaitsee kysyntää tietyssä sijainnissa (rivi, jossa on sijaintikoodi), järjestelmä ryhtyy toimimaan. Toimintamalli määräytyy kolmen keskeisen asetusarvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="a396a-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="a396a-110">Järjestelmä tarkistaa kyseiset kolme arvoa järjestyksessä suunnitteluajon aikana ja toteuttaa suunnitelmat niiden mukaan:</span><span class="sxs-lookup"><span data-stu-id="a396a-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="a396a-111">Onko **Sijainti pakollinen** -kentässä valintamerkki?</span><span class="sxs-lookup"><span data-stu-id="a396a-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="a396a-112">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="a396a-112">If yes, then:</span></span>  

2.  <span data-ttu-id="a396a-113">Onko nimikkeellä varastointiyksikkö?</span><span class="sxs-lookup"><span data-stu-id="a396a-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="a396a-114">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="a396a-114">If yes, then:</span></span>  

    <span data-ttu-id="a396a-115">Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a396a-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="a396a-116">Toimet, kun vastaus on Ei:</span><span class="sxs-lookup"><span data-stu-id="a396a-116">If no, then:</span></span>  

3.  <span data-ttu-id="a396a-117">Onko **Komponentit sijainnissa** -kentässä vaadittu sijaintikoodi?</span><span class="sxs-lookup"><span data-stu-id="a396a-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="a396a-118">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="a396a-118">If yes, then:</span></span>  

    <span data-ttu-id="a396a-119">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a396a-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="a396a-120">Toimet, kun vastaus on Ei:</span><span class="sxs-lookup"><span data-stu-id="a396a-120">If no, then:</span></span>  

    <span data-ttu-id="a396a-121">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä*, Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="a396a-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="a396a-122">( *Tilaus*-uusintatilaustapaa käyttävät nimikkeet käyttävät yhä  *Tilaus*-uusintatilaustapaa sekä muita asetuksia.)</span><span class="sxs-lookup"><span data-stu-id="a396a-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a396a-123">Tämä "minimaalinen vaihtoehto" kattaa vain tarkan kysynnän.</span><span class="sxs-lookup"><span data-stu-id="a396a-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="a396a-124">Kaikki määritetyt suunnitteluparametrit ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="a396a-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="a396a-125">Tutustu jäljempänä oleviin esimerkkitilanteisiin.</span><span class="sxs-lookup"><span data-stu-id="a396a-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="a396a-126">Kysyntä "tyhjässä sijainnissa"</span><span class="sxs-lookup"><span data-stu-id="a396a-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="a396a-127">Vaikka **Sijainti pakollinen** -valintaruutu olisi valittu, järjestelmä sallii kysyntärivien luonnin ilman sijaintikoodia. Tätä kutsutaan myös *TYHJÄKSI* sijainniksi.</span><span class="sxs-lookup"><span data-stu-id="a396a-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="a396a-128">Tämä on järjestelmälle poikkeustilanne, koska sijaintien käsittelyä varten on määritetty useita määritysarvoja (esimerkki yllä). Suunnitteluohjelma ei tämän vuoksi luo tällaiselle kysyntäriville suunnitteluriviä.</span><span class="sxs-lookup"><span data-stu-id="a396a-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="a396a-129">Jos **Sijainti pakollinen** -kenttää ei ole valittu mutta käytössä on sijainnin asetusarvoja, kyseessä on poikkeustilanne. Suunnittelujärjestelmä reagoi siihen tuottamalla minimaalisen vaihtoehdon:</span><span class="sxs-lookup"><span data-stu-id="a396a-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="a396a-130">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä *Tilaus)*, Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="a396a-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="a396a-131">Tutustu jäljempänä oleviin määritystilanteisiin.</span><span class="sxs-lookup"><span data-stu-id="a396a-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="a396a-132">Asetukset (1):</span><span class="sxs-lookup"><span data-stu-id="a396a-132">Setup 1:</span></span>  

-   <span data-ttu-id="a396a-133">Sijainti pakollinen = *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="a396a-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="a396a-134">Varastointiyksikkö on määritetty kohteeseen  *PUNAINEN*</span><span class="sxs-lookup"><span data-stu-id="a396a-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="a396a-135">Komponentit sijainnissa =  *SININEN*</span><span class="sxs-lookup"><span data-stu-id="a396a-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="a396a-136">Tapaus 1.1: Kysyntää *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="a396a-137">Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti (mahdolliset siirrot mukaan lukien).</span><span class="sxs-lookup"><span data-stu-id="a396a-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="a396a-138">Tapaus 1.2: Kysyntää *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="a396a-139">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a396a-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="a396a-140">Tapaus 1.3: Kysyntää  *VIHREÄ*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="a396a-141">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="a396a-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="a396a-142">Tapaus 1.4: Kysyntää  *TYHJÄ* -sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="a396a-143">Nimikettä ei suunnitella, koska kysyntäriville ei ole määritetty sijaintia.</span><span class="sxs-lookup"><span data-stu-id="a396a-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="a396a-144">Asetukset (2):</span><span class="sxs-lookup"><span data-stu-id="a396a-144">Setup 2:</span></span>  

-   <span data-ttu-id="a396a-145">Sijainti pakollinen = *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="a396a-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="a396a-146">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="a396a-146">No SKU exists</span></span>  
-   <span data-ttu-id="a396a-147">Komponentit sijainnissa =  *SININEN*</span><span class="sxs-lookup"><span data-stu-id="a396a-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="a396a-148">Tapaus 2.1: Kysyntää  *PUNAINEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="a396a-149">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="a396a-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="a396a-150">Tapaus 2.2: Kysyntää *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="a396a-151">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a396a-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="a396a-152">Asetukset (3):</span><span class="sxs-lookup"><span data-stu-id="a396a-152">Setup 3:</span></span>  

-   <span data-ttu-id="a396a-153">Sijainti pakollinen = *Ei*</span><span class="sxs-lookup"><span data-stu-id="a396a-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="a396a-154">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="a396a-154">No SKU exists</span></span>  
-   <span data-ttu-id="a396a-155">Komponentit sijainnissa =  *SININEN*</span><span class="sxs-lookup"><span data-stu-id="a396a-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="a396a-156">Tapaus 3.1: Kysyntää  *PUNAINEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="a396a-157">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="a396a-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="a396a-158">Tapaus 3.2: Kysyntää *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="a396a-159">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a396a-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="a396a-160">Tapaus 3.3: Kysyntää  *TYHJÄ* -sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="a396a-161">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="a396a-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="a396a-162">Asetukset (4):</span><span class="sxs-lookup"><span data-stu-id="a396a-162">Setup 4:</span></span>  

-   <span data-ttu-id="a396a-163">Sijainti pakollinen = *Ei*</span><span class="sxs-lookup"><span data-stu-id="a396a-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="a396a-164">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="a396a-164">No SKU exists</span></span>  
-   <span data-ttu-id="a396a-165">Komponentit sijainnissa =  *TYHJÄ*</span><span class="sxs-lookup"><span data-stu-id="a396a-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="a396a-166">Tapaus 4.1: Kysyntää  *SININEN*-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="a396a-167">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="a396a-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="a396a-168">Tapaus 4.2: Kysyntää  *TYHJÄ* -sijainnissa</span><span class="sxs-lookup"><span data-stu-id="a396a-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="a396a-169">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a396a-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="a396a-170">Kuten viimeinen esimerkkitilanne osoittaa, kaikkien sijainteihin liittyvien asetusarvojen poistaminen käytöstä on ainoa tapa saada oikeita tuloksia, kun kysyntärivillä ei ole sijaintikoodia.</span><span class="sxs-lookup"><span data-stu-id="a396a-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="a396a-171">Vastaavasti varastointiyksiköiden käyttäminen on ainoa tapa saada vakaita suunnittelutuloksia sijaintien kysyntään liittyen.</span><span class="sxs-lookup"><span data-stu-id="a396a-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="a396a-172">Jos suunnittelet usein kysyntää sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa ehdottomasti käyttää.</span><span class="sxs-lookup"><span data-stu-id="a396a-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a396a-173">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a396a-173">See Also</span></span>
<span data-ttu-id="a396a-174">[Suunnittelu](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="a396a-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="a396a-175">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a396a-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a396a-176">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a396a-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a396a-177">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="a396a-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a396a-178">Osto</span><span class="sxs-lookup"><span data-stu-id="a396a-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a396a-179">[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a396a-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="a396a-180">Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu</span><span class="sxs-lookup"><span data-stu-id="a396a-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="a396a-181">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a396a-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

