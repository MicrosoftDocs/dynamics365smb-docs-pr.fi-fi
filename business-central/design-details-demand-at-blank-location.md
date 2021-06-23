---
title: Rakennetiedot – kysyntä ja tarjonta | Microsoft Docs
description: Tässä ohjeaiheessa esitellään kysyntä-termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 62abcd0e37a9871efd6158a898538b7c18b6b47f
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215326"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="b676d-103">Rakennetiedot: kysyntä tyhjä-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="b676d-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="b676d-104">Kun käyttäjä luo kysyntätapahtuman, kuten myyntitilausrivin, ohjelma sallii käyttäjän joskus määrittää sijaintikoodin, mutta ei aina. Tällöin käytetään tyhjää sijaintia.</span><span class="sxs-lookup"><span data-stu-id="b676d-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="b676d-105">Riippumatta siitä, onko kysynnällä sijaintikoodeja, suunnittelujärjestelmä toimii suoraviivaisesti seuraavien asioiden toteutuessa:</span><span class="sxs-lookup"><span data-stu-id="b676d-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="b676d-106">Kysyntäriveillä on aina sijaintikoodi, ja järjestelmä käyttää varastointiyksiköiden kaikkia ominaisuuksia, myös asiaankuuluvia sijaintiasetuksia.</span><span class="sxs-lookup"><span data-stu-id="b676d-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="b676d-107">Kysyntäriveillä ei missään tilanteessa käytetä sijaintikoodeja, eikä järjestelmä käytä varastointiyksiköitä eikä sijaintiasetuksia (ks. viimeinen tilanne seuraavassa osiossa).</span><span class="sxs-lookup"><span data-stu-id="b676d-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="b676d-108">Jos kysyntätapahtumissa toisinaan on sijaintikoodeja ja toisinaan taas ei, suunnittelujärjestelmä noudattaa asetuksien mukaan tiettyjä sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="b676d-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="b676d-109">Kysyntä sijainnissa</span><span class="sxs-lookup"><span data-stu-id="b676d-109">Demand at Location</span></span>
<span data-ttu-id="b676d-110">Kun suunnittelujärjestelmä havaitsee kysyntää tietyssä sijainnissa, se toimii kolmen keskeisen asetusarvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="b676d-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="b676d-111">Järjestelmä tarkistaa kyseiset kolme arvoa järjestyksessä suunnitteluajon aikana ja toteuttaa suunnitelmat niiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="b676d-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="b676d-112">Onko **Sijainti pakollinen** -kentässä valintamerkki?</span><span class="sxs-lookup"><span data-stu-id="b676d-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="b676d-113">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="b676d-113">If yes, then:</span></span>

2. <span data-ttu-id="b676d-114">Onko nimikkeellä varastointiyksikkö?</span><span class="sxs-lookup"><span data-stu-id="b676d-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="b676d-115">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="b676d-115">If yes, then:</span></span>

    <span data-ttu-id="b676d-116">Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b676d-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="b676d-117">Toimet, kun vastaus on Ei:</span><span class="sxs-lookup"><span data-stu-id="b676d-117">If no, then:</span></span>

3. <span data-ttu-id="b676d-118">Onko Komponentit sijainnissa -kentässä vaadittu sijaintikoodi?</span><span class="sxs-lookup"><span data-stu-id="b676d-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="b676d-119">Toimet, kun vastaus on Kyllä:</span><span class="sxs-lookup"><span data-stu-id="b676d-119">If yes, then:</span></span>

  <span data-ttu-id="b676d-120">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b676d-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="b676d-121">Toimet, kun vastaus on Ei:</span><span class="sxs-lookup"><span data-stu-id="b676d-121">If no, then:</span></span>

  <span data-ttu-id="b676d-122">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä, Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit = tyhjä, uusintatilaustapaa käyttävät nimikkeet = Tilaus säilyy käyttäen tilausta muiden asetusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="b676d-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="b676d-123">Poikkeuksellisiin suunnitteluasetuksiin, jotka ovat viimeisen reaktion tulosta vaiheessa 3 yllä, viitataan seuraavassa nimellä "minimivaihtoehto".</span><span class="sxs-lookup"><span data-stu-id="b676d-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="b676d-124">Tämän suunnitteluasetus kattaa vain tarkan kysynnän. Muut suunnitteluparametrit ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="b676d-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="b676d-125">Katso tiedot tämän suunnittelulogiikan variaatioista alla olevasta skenaariot-osiosta.</span><span class="sxs-lookup"><span data-stu-id="b676d-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="b676d-126">Kysyntä tyhjässä sijainnissa</span><span class="sxs-lookup"><span data-stu-id="b676d-126">Demand at Blank Location</span></span>
<span data-ttu-id="b676d-127">Vaikka **Sijainti pakollinen** -kenttä on valittu, ohjelma sallii kysyntärivien luonnin ilman sijaintikoodia. Tätä kutsutaan myös tyhjäksi sijainniksi.</span><span class="sxs-lookup"><span data-stu-id="b676d-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="b676d-128">Tämä on järjestelmälle poikkeustilanne, koska sijaintien käsittelyä varten on määritetty useita määritysarvoja (esimerkki yllä). Suunnitteluohjelma ei tämän vuoksi luo tällaiselle kysyntäriville suunnitteluriviä.</span><span class="sxs-lookup"><span data-stu-id="b676d-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="b676d-129">Jos **Sijainti pakollinen** -kenttää ei ole valittu, mutta mikä tahansa sijainnin asetusarvoista on olemassa, se katsotaan myös poikkeamaksi ja suunnittelujärjestelmä reagoi siihen käyttämällä "minimaalinen vaihtoehto"-ominaisuutta: nimike suunnitellaan seuraavien parametrien mukaan: uusintatilaustapa = erä-erästä (tilaus on edelleen tilaus), sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit = tyhjä.</span><span class="sxs-lookup"><span data-stu-id="b676d-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="b676d-130">Esimerkkitilanteet</span><span class="sxs-lookup"><span data-stu-id="b676d-130">Scenarios</span></span>
<span data-ttu-id="b676d-131">Seuraavat skenaariot kuvaavat tyhjän paikan kysynnän variaatioita ja kuinka suunnittelujärjestelmä ratkaisee "minimivaihtoehdon".</span><span class="sxs-lookup"><span data-stu-id="b676d-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="b676d-132">Asetukset (1):</span><span class="sxs-lookup"><span data-stu-id="b676d-132">Setup 1:</span></span>
<span data-ttu-id="b676d-133">Sijainti pakollinen = Kyllä</span><span class="sxs-lookup"><span data-stu-id="b676d-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="b676d-134">Varastointiyksikkö on määritetty kohteeseen PUNAINEN</span><span class="sxs-lookup"><span data-stu-id="b676d-134">SKU is set up for RED</span></span>

<span data-ttu-id="b676d-135">Komponentit sijainnissa = SININEN</span><span class="sxs-lookup"><span data-stu-id="b676d-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="b676d-136">Tapaus 1.1: Kysyntä on sijainnissa PUNAINEN</span><span class="sxs-lookup"><span data-stu-id="b676d-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="b676d-137">Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b676d-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="b676d-138">Tapaus 1.2: Kysyntä on sijainnissa SININEN</span><span class="sxs-lookup"><span data-stu-id="b676d-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="b676d-139">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="b676d-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="b676d-140">Tapaus 1.3: Kysyntä on sijainnissa VIHREÄ</span><span class="sxs-lookup"><span data-stu-id="b676d-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="b676d-141">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="b676d-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="b676d-142">Tapaus 1.4: Kysyntä on sijainnissa TYHJÄ</span><span class="sxs-lookup"><span data-stu-id="b676d-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="b676d-143">Nimikettä ei suunnitella, koska kysyntäriville ei ole määritetty sijaintia.</span><span class="sxs-lookup"><span data-stu-id="b676d-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="b676d-144">Asetukset (2):</span><span class="sxs-lookup"><span data-stu-id="b676d-144">Setup 2:</span></span>
<span data-ttu-id="b676d-145">Sijainti pakollinen = Kyllä</span><span class="sxs-lookup"><span data-stu-id="b676d-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="b676d-146">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="b676d-146">No SKU exists</span></span>

<span data-ttu-id="b676d-147">Komponentit sijainnissa = SININEN</span><span class="sxs-lookup"><span data-stu-id="b676d-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="b676d-148">Tapaus 2.1: Kysyntä on sijainnissa PUNAINEN</span><span class="sxs-lookup"><span data-stu-id="b676d-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="b676d-149">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="b676d-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="b676d-150">Tapaus 2.2: Kysyntä on sijainnissa SININEN</span><span class="sxs-lookup"><span data-stu-id="b676d-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="b676d-151">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b676d-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="b676d-152">Asetukset (3):</span><span class="sxs-lookup"><span data-stu-id="b676d-152">Setup 3:</span></span>
<span data-ttu-id="b676d-153">Sijainti pakollinen = Ei</span><span class="sxs-lookup"><span data-stu-id="b676d-153">Location Mandatory = No</span></span>

<span data-ttu-id="b676d-154">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="b676d-154">No SKU exists</span></span>

<span data-ttu-id="b676d-155">Komponentit sijainnissa = SININEN</span><span class="sxs-lookup"><span data-stu-id="b676d-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="b676d-156">Tapaus 3.1: Kysyntä on sijainnissa PUNAINEN</span><span class="sxs-lookup"><span data-stu-id="b676d-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="b676d-157">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="b676d-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="b676d-158">Tapaus 3.2: Kysyntä on sijainnissa SININEN</span><span class="sxs-lookup"><span data-stu-id="b676d-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="b676d-159">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b676d-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="b676d-160">Tapaus 3.3: Kysyntä on sijainnissa TYHJÄ</span><span class="sxs-lookup"><span data-stu-id="b676d-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="b676d-161">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="b676d-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="b676d-162">Asetukset (4):</span><span class="sxs-lookup"><span data-stu-id="b676d-162">Setup 4:</span></span>
<span data-ttu-id="b676d-163">Sijainti pakollinen = Ei</span><span class="sxs-lookup"><span data-stu-id="b676d-163">Location Mandatory = No</span></span>

<span data-ttu-id="b676d-164">Ei varastointiyksikköä</span><span class="sxs-lookup"><span data-stu-id="b676d-164">No SKU exists</span></span>

<span data-ttu-id="b676d-165">Komponentit sijainnissa = TYHJÄ</span><span class="sxs-lookup"><span data-stu-id="b676d-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="b676d-166">Tapaus 4.1: Kysyntä on sijainnissa SININEN</span><span class="sxs-lookup"><span data-stu-id="b676d-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="b676d-167">Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="b676d-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="b676d-168">Tapaus 4.2: Kysyntä on sijainnissa TYHJÄ</span><span class="sxs-lookup"><span data-stu-id="b676d-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="b676d-169">Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b676d-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="b676d-170">Kuten edellisessä esimerkkitilanteessa kuvataan, kaikkien sijainteihin liittyvien asetusarvojen poistaminen käytöstä on ainoa tapa saada oikeita tuloksia, kun kysyntärivillä ei ole sijaintikoodia.</span><span class="sxs-lookup"><span data-stu-id="b676d-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="b676d-171">Vastaavasti varastointiyksiköiden käyttäminen on ainoa tapa saada vakaita suunnittelutuloksia sijaintien kysyntään liittyen.</span><span class="sxs-lookup"><span data-stu-id="b676d-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="b676d-172">Jos yritykset suunnittelevat usein kysyntää sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa ehdottomasti käyttää.</span><span class="sxs-lookup"><span data-stu-id="b676d-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="b676d-173">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b676d-173">See Also</span></span>  
<span data-ttu-id="b676d-174">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="b676d-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="b676d-175">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="b676d-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="b676d-176">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="b676d-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]