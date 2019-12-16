---
title: Rakennetiedot – kysyntä ja tarjonta | Microsoft Docs
description: Tässä ohjeaiheessa esitellään kysyntä-termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 11/11/2019
ms.author: sgroespe
ms.openlocfilehash: b5434f4f8b5df6a23d01401be442ec08de329d1d
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880518"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="785b5-103">Rakennetiedot: kysyntä tyhjä-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="785b5-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="785b5-104">Kun käyttäjä luo kysyntätapahtuman, kuten myyntitilausrivin, ohjelma sallii käyttäjän joskus määrittää sijaintikoodin, mutta ei aina. Tällöin käytetään tyhjää sijaintia.</span><span class="sxs-lookup"><span data-stu-id="785b5-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="785b5-105">Riippumatta siitä, onko kysynnällä sijaintikoodeja, suunnittelujärjestelmä toimii suoraviivaisesti seuraavien asioiden toteutuessa:</span><span class="sxs-lookup"><span data-stu-id="785b5-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="785b5-106">Kysyntäriveillä on aina sijaintikoodi, ja järjestelmä käyttää varastointiyksiköiden kaikkia ominaisuuksia, myös asiaankuuluvia sijaintiasetuksia.</span><span class="sxs-lookup"><span data-stu-id="785b5-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="785b5-107">Kysyntäriveillä ei missään tilanteessa käytetä sijaintikoodeja, eikä järjestelmä käytä varastointiyksiköitä eikä sijaintiasetuksia (ks. viimeinen tilanne seuraavassa osiossa).</span><span class="sxs-lookup"><span data-stu-id="785b5-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="785b5-108">Jos kysyntätapahtumissa toisinaan on sijaintikoodeja ja toisinaan taas ei, suunnittelujärjestelmä noudattaa asetuksien mukaan tiettyjä sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="785b5-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="785b5-109">Kysyntä sijainnissa</span><span class="sxs-lookup"><span data-stu-id="785b5-109">Demand at Location</span></span>
<span data-ttu-id="785b5-110">Kun suunnittelujärjestelmä havaitsee kysyntää tietyssä sijainnissa, se toimii kolmen keskeisen asetusarvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="785b5-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="785b5-111">Järjestelmä tarkistaa kyseiset kolme arvoa järjestyksessä suunnitteluajon aikana ja toteuttaa suunnitelmat niiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="785b5-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="785b5-112">Onko **Sijainti pakollinen** -kentässä valintamerkki?</span><span class="sxs-lookup"><span data-stu-id="785b5-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="785b5-113">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="785b5-113">If yes, then:</span></span>

2. <span data-ttu-id="785b5-114">Onko nimikkeellä varastointiyksikkö?</span><span class="sxs-lookup"><span data-stu-id="785b5-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="785b5-115">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="785b5-115">If yes, then:</span></span>

    <span data-ttu-id="785b5-116">Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="785b5-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="785b5-117">Toimet, kun vastaus on Ei:</span><span class="sxs-lookup"><span data-stu-id="785b5-117">If no, then:</span></span>

3. <span data-ttu-id="785b5-118">Onko Komponentit sijainnissa -kentässä vaadittu sijaintikoodi?</span><span class="sxs-lookup"><span data-stu-id="785b5-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="785b5-119">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="785b5-119">If yes, then:</span></span>

  <span data-ttu-id="785b5-120">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="785b5-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="785b5-121">Toimet, kun vastaus on Ei:</span><span class="sxs-lookup"><span data-stu-id="785b5-121">If no, then:</span></span>

  <span data-ttu-id="785b5-122">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä, Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit = tyhjä, uusintatilaustapaa käyttävät nimikkeet = Tilaus säilyy käyttäen tilausta muiden asetusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="785b5-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="785b5-123">Poikkeuksellisiin suunnitteluasetuksiin, jotka ovat viimeisen reaktion tulosta vaiheessa 3 yllä, viitataan seuraavassa nimellä "minimivaihtoehto".</span><span class="sxs-lookup"><span data-stu-id="785b5-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="785b5-124">Tämän suunnitteluasetus kattaa vain tarkan kysynnän. Muut suunnitteluparametrit ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="785b5-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="785b5-125">Katso tiedot tämän suunnittelulogiikan variaatioista alla olevasta skenaariot-osiosta.</span><span class="sxs-lookup"><span data-stu-id="785b5-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="785b5-126">Kysyntä tyhjässä sijainnissa</span><span class="sxs-lookup"><span data-stu-id="785b5-126">Demand at Blank Location</span></span>
<span data-ttu-id="785b5-127">Vaikka **Sijainti pakollinen** -kenttä on valittu, ohjelma sallii kysyntärivien luonnin ilman sijaintikoodia. Tätä kutsutaan myös tyhjäksi sijainniksi.</span><span class="sxs-lookup"><span data-stu-id="785b5-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="785b5-128">Tämä on järjestelmälle poikkeustilanne, koska sijaintien käsittelyä varten on määritetty useita määritysarvoja (esimerkki yllä). Suunnitteluohjelma ei tämän vuoksi luo tällaiselle kysyntäriville suunnitteluriviä.</span><span class="sxs-lookup"><span data-stu-id="785b5-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="785b5-129">Jos **Sijainti pakollinen** -kenttää ei ole valittu, mutta mikä tahansa sijainnin asetusarvoista on olemassa, se katsotaan myös poikkeamaksi ja suunnittelujärjestelmä reagoi siihen käyttämällä "minimaalinen vaihtoehto"-ominaisuutta: nimike suunnitellaan seuraavien parametrien mukaan: uusintatilaustapa = erä-erästä (tilaus on edelleen tilaus), sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit = tyhjä.</span><span class="sxs-lookup"><span data-stu-id="785b5-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="785b5-130">Esimerkkitilanteet</span><span class="sxs-lookup"><span data-stu-id="785b5-130">Scenarios</span></span>
<span data-ttu-id="785b5-131">Seuraavat skenaariot kuvaavat tyhjän paikan kysynnän variaatioita ja kuinka suunnittelujärjestelmä ratkaisee "minimivaihtoehdon".</span><span class="sxs-lookup"><span data-stu-id="785b5-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="785b5-132">Asetukset (1):</span><span class="sxs-lookup"><span data-stu-id="785b5-132">Setup 1:</span></span>
<span data-ttu-id="785b5-133">Sijainti pakollinen = Kyllä</span><span class="sxs-lookup"><span data-stu-id="785b5-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="785b5-134">Varastointiyksikkö on määritetty kohteeseen PUNAINEN</span><span class="sxs-lookup"><span data-stu-id="785b5-134">SKU is set up for RED</span></span>

<span data-ttu-id="785b5-135">Komponentit sijainnissa = SININEN</span><span class="sxs-lookup"><span data-stu-id="785b5-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="785b5-136">Tapaus 1.1: Kysyntä on sijainnissa PUNAINEN</span><span class="sxs-lookup"><span data-stu-id="785b5-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="785b5-137">Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="785b5-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="785b5-138">Tapaus 1.2: Kysyntä on sijainnissa SININEN</span><span class="sxs-lookup"><span data-stu-id="785b5-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="785b5-139">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="785b5-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="785b5-140">Tapaus 1.3: Kysyntä on sijainnissa VIHREÄ</span><span class="sxs-lookup"><span data-stu-id="785b5-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="785b5-141">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="785b5-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="785b5-142">Tapaus 1.4: Kysyntä on sijainnissa TYHJÄ</span><span class="sxs-lookup"><span data-stu-id="785b5-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="785b5-143">Nimikettä ei suunnitella, koska kysyntäriville ei ole määritetty sijaintia.</span><span class="sxs-lookup"><span data-stu-id="785b5-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="785b5-144">Asetukset (2):</span><span class="sxs-lookup"><span data-stu-id="785b5-144">Setup 2:</span></span>
<span data-ttu-id="785b5-145">Sijainti pakollinen = Kyllä</span><span class="sxs-lookup"><span data-stu-id="785b5-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="785b5-146">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="785b5-146">No SKU exists</span></span>

<span data-ttu-id="785b5-147">Komponentit sijainnissa = SININEN</span><span class="sxs-lookup"><span data-stu-id="785b5-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="785b5-148">Tapaus 2.1: Kysyntä on sijainnissa PUNAINEN</span><span class="sxs-lookup"><span data-stu-id="785b5-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="785b5-149">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="785b5-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="785b5-150">Tapaus 2.2: Kysyntä on sijainnissa SININEN</span><span class="sxs-lookup"><span data-stu-id="785b5-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="785b5-151">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="785b5-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="785b5-152">Asetukset (3):</span><span class="sxs-lookup"><span data-stu-id="785b5-152">Setup 3:</span></span>
<span data-ttu-id="785b5-153">Sijainti pakollinen = Ei</span><span class="sxs-lookup"><span data-stu-id="785b5-153">Location Mandatory = No</span></span>

<span data-ttu-id="785b5-154">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="785b5-154">No SKU exists</span></span>

<span data-ttu-id="785b5-155">Komponentit sijainnissa = SININEN</span><span class="sxs-lookup"><span data-stu-id="785b5-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="785b5-156">Tapaus 3.1: Kysyntä on sijainnissa PUNAINEN</span><span class="sxs-lookup"><span data-stu-id="785b5-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="785b5-157">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="785b5-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="785b5-158">Tapaus 3.2: Kysyntä on sijainnissa SININEN</span><span class="sxs-lookup"><span data-stu-id="785b5-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="785b5-159">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="785b5-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="785b5-160">Tapaus 3.3: Kysyntä on sijainnissa TYHJÄ</span><span class="sxs-lookup"><span data-stu-id="785b5-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="785b5-161">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="785b5-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="785b5-162">Asetukset (4):</span><span class="sxs-lookup"><span data-stu-id="785b5-162">Setup 4:</span></span>
<span data-ttu-id="785b5-163">Sijainti pakollinen = Ei</span><span class="sxs-lookup"><span data-stu-id="785b5-163">Location Mandatory = No</span></span>

<span data-ttu-id="785b5-164">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="785b5-164">No SKU exists</span></span>

<span data-ttu-id="785b5-165">Komponentit sijainnissa = TYHJÄ</span><span class="sxs-lookup"><span data-stu-id="785b5-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="785b5-166">Tapaus 4.1: Kysyntä on sijainnissa SININEN</span><span class="sxs-lookup"><span data-stu-id="785b5-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="785b5-167">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="785b5-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="785b5-168">Tapaus 4.2: Kysyntä on sijainnissa TYHJÄ</span><span class="sxs-lookup"><span data-stu-id="785b5-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="785b5-169">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="785b5-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="785b5-170">Kuten edellisessä esimerkkitilanteessa kuvataan, kaikkien sijainteihin liittyvien asetusarvojen poistaminen käytöstä on ainoa tapa saada oikeita tuloksia, kun kysyntärivillä ei ole sijaintikoodia.</span><span class="sxs-lookup"><span data-stu-id="785b5-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="785b5-171">Vastaavasti varastointiyksiköiden käyttäminen on ainoa tapa saada vakaita suunnittelutuloksia sijaintien kysyntään liittyen.</span><span class="sxs-lookup"><span data-stu-id="785b5-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="785b5-172">Jos yritykset suunnittelevat usein kysyntää sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa ehdottomasti käyttää.</span><span class="sxs-lookup"><span data-stu-id="785b5-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="785b5-173">Katso myös</span><span class="sxs-lookup"><span data-stu-id="785b5-173">See Also</span></span>  
<span data-ttu-id="785b5-174">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="785b5-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="785b5-175">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="785b5-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="785b5-176">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="785b5-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
