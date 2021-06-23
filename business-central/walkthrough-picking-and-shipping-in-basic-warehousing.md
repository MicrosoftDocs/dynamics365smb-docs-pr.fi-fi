---
title: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä
description: Business Central -sovelluksessa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214651"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="220b3-103">Vaihekuvaus: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä</span><span class="sxs-lookup"><span data-stu-id="220b3-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="220b3-104">[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.</span><span class="sxs-lookup"><span data-stu-id="220b3-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="220b3-105">Tapa</span><span class="sxs-lookup"><span data-stu-id="220b3-105">Method</span></span>|<span data-ttu-id="220b3-106">Saapuva prosessi</span><span class="sxs-lookup"><span data-stu-id="220b3-106">Inbound process</span></span>|<span data-ttu-id="220b3-107">Varastopaikat</span><span class="sxs-lookup"><span data-stu-id="220b3-107">Bins</span></span>|<span data-ttu-id="220b3-108">Poiminnat</span><span class="sxs-lookup"><span data-stu-id="220b3-108">Picks</span></span>|<span data-ttu-id="220b3-109">Toimitukset</span><span class="sxs-lookup"><span data-stu-id="220b3-109">Shipments</span></span>|<span data-ttu-id="220b3-110">Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="220b3-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="220b3-111">L</span><span class="sxs-lookup"><span data-stu-id="220b3-111">A</span></span>|<span data-ttu-id="220b3-112">Poiminnan ja toimituksen kirjaaminen tilausriviltä</span><span class="sxs-lookup"><span data-stu-id="220b3-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="220b3-113">X</span><span class="sxs-lookup"><span data-stu-id="220b3-113">X</span></span>|||<span data-ttu-id="220b3-114">2</span><span class="sxs-lookup"><span data-stu-id="220b3-114">2</span></span>|  
|<span data-ttu-id="220b3-115">B</span><span class="sxs-lookup"><span data-stu-id="220b3-115">B</span></span>|<span data-ttu-id="220b3-116">Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta</span><span class="sxs-lookup"><span data-stu-id="220b3-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="220b3-117">X</span><span class="sxs-lookup"><span data-stu-id="220b3-117">X</span></span>||<span data-ttu-id="220b3-118">3</span><span class="sxs-lookup"><span data-stu-id="220b3-118">3</span></span>|  
|<span data-ttu-id="220b3-119">N</span><span class="sxs-lookup"><span data-stu-id="220b3-119">C</span></span>|<span data-ttu-id="220b3-120">Kirjaa poiminta ja lähetyksen fyysisen varastoinnin toimituksen asiakirjasta</span><span class="sxs-lookup"><span data-stu-id="220b3-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="220b3-121">X</span><span class="sxs-lookup"><span data-stu-id="220b3-121">X</span></span>|<span data-ttu-id="220b3-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="220b3-122">4/5/6</span></span>|  
|<span data-ttu-id="220b3-123">P</span><span class="sxs-lookup"><span data-stu-id="220b3-123">D</span></span>|<span data-ttu-id="220b3-124">Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimituksen asiakirjasta</span><span class="sxs-lookup"><span data-stu-id="220b3-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="220b3-125">X</span><span class="sxs-lookup"><span data-stu-id="220b3-125">X</span></span>|<span data-ttu-id="220b3-126">X</span><span class="sxs-lookup"><span data-stu-id="220b3-126">X</span></span>|<span data-ttu-id="220b3-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="220b3-127">4/5/6</span></span>|  

<span data-ttu-id="220b3-128">Katso lisätietoja kohdasta [Rakennetiedot: lähtevän fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="220b3-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="220b3-129">Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.</span><span class="sxs-lookup"><span data-stu-id="220b3-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="220b3-130">Tietoja tästä vaihekuvauksesta</span><span class="sxs-lookup"><span data-stu-id="220b3-130">About This Walkthrough</span></span>

<span data-ttu-id="220b3-131">Jos sijainnit on määritetty fyysisen varastoinnin perusmäärityksissä edellyttämään poimintakäsittelyä mutta ei toimituskäsittelyä, **Varaston poiminta** -sivua on käytettävä lähtevien lähdeasiakirjojen poiminta- ja toimitustietojen tallennuksessa ja kirjaamisessa.</span><span class="sxs-lookup"><span data-stu-id="220b3-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="220b3-132">Lähtevä lähdeasiakirja voi olla myyntitilaus, ostopalautustilaus, lähtevä siirtotilaus tai tuotantotilaus komponenttitarpeella.</span><span class="sxs-lookup"><span data-stu-id="220b3-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="220b3-133">Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="220b3-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="220b3-134">ETELÄ-sijainnin määrittäminen varastopaikan käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="220b3-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="220b3-135">Myyntitilauksen luominen asiakkaalle 10000 30 Amsterdam-lampusta.</span><span class="sxs-lookup"><span data-stu-id="220b3-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="220b3-136">Myyntitilauksen vapauttaminen varaston käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="220b3-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="220b3-137">Varastopoiminnan julkaistusta lähdeasiakirjasta luominen</span><span class="sxs-lookup"><span data-stu-id="220b3-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="220b3-138">Rekisteröidään fyysisen varastoinnin siirtoa varastosta ja kirjataan samanaikaisesti lähdemyyntitilauksen myyntitoimitusta.</span><span class="sxs-lookup"><span data-stu-id="220b3-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="220b3-139">Roolit</span><span class="sxs-lookup"><span data-stu-id="220b3-139">Roles</span></span>

<span data-ttu-id="220b3-140">Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="220b3-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="220b3-141">Varastopäällikkö</span><span class="sxs-lookup"><span data-stu-id="220b3-141">Warehouse Manager</span></span>  
- <span data-ttu-id="220b3-142">Tilausten käsittelijä</span><span class="sxs-lookup"><span data-stu-id="220b3-142">Order Processor</span></span>  
- <span data-ttu-id="220b3-143">Varastotyöntekijä</span><span class="sxs-lookup"><span data-stu-id="220b3-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="220b3-144">Taustatietoja</span><span class="sxs-lookup"><span data-stu-id="220b3-144">Story</span></span>

<span data-ttu-id="220b3-145">Ellen, CRONUSin varastopäällikkö, määrittää ETELÄ-varaston Basic-poiminnan käsittelyä varten. Sen mukaisesti varastotyöntekijät käsittelevät lähtevät tilaukset erikseen.</span><span class="sxs-lookup"><span data-stu-id="220b3-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="220b3-146">Susanna, tilausten käsittelijä, luo myyntitilauksen 1928-S-nimikkeen 30 yksikön toimituksesta asiakkaalle 10000 ETELÄ-varastosta.</span><span class="sxs-lookup"><span data-stu-id="220b3-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="220b3-147">Johnin, varastotyöntekijän, täytyy varmistaa, että lähetys on valmisteltu ja toimitettu asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="220b3-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="220b3-148">John hallitsee kaikkia **Varaston poiminta** -sivulla olevia tehtäviä, jotka viittaavat automaattisesti varastopaikkoihin, joissa nimikettä 1928-S varastoidaan.</span><span class="sxs-lookup"><span data-stu-id="220b3-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="220b3-149">Varastopaikkakoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="220b3-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="220b3-150">Kun olet määrittänyt sijainnin, sinun täytyy lisätä kaksi varastopaikkaa.</span><span class="sxs-lookup"><span data-stu-id="220b3-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="220b3-151">Varastopaikkakoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="220b3-151">To setup the bin codes</span></span>

1. <span data-ttu-id="220b3-152">Valitse **Varastopaikat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="220b3-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="220b3-153">Luo kaksi varastopaikkaa koodeilla *S-01-0001* ja *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="220b3-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="220b3-154">Varastotyöntekijän tekeminen sijainnissa ETELÄ</span><span class="sxs-lookup"><span data-stu-id="220b3-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="220b3-155">Jotta voisit käyttää tätä toimintoa, sinun on lisättävä itsesi varastotyöntekijäksi tähän sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="220b3-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="220b3-156">Tee itsestäsi varastotyöntekijä</span><span class="sxs-lookup"><span data-stu-id="220b3-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="220b3-157">Valitse ensimmäinen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastotyöntekijät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="220b3-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="220b3-158">Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **F.var. työntekijät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="220b3-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="220b3-159">Valitse **Sijaintikoodi**-kentässä ETELÄ.</span><span class="sxs-lookup"><span data-stu-id="220b3-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="220b3-160">Valitse **Oletus**-kenttä ja sitten **Kyllä**-painike..</span><span class="sxs-lookup"><span data-stu-id="220b3-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="220b3-161">Nimikkeen 1928-S tekeminen saatavaksi</span><span class="sxs-lookup"><span data-stu-id="220b3-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="220b3-162">Tehdäksesi nimikkeen 1928-S saatavaksi ETELÄ-sijainnissa noudata seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="220b3-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="220b3-163">Valitse toinen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="220b3-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="220b3-164">Avaa oletuspäiväkirja ja luo kaksi nimikepäiväkirjan riviä seuraavilla käsittelypäivämäärän tiedoilla (23. tammikuuta).</span><span class="sxs-lookup"><span data-stu-id="220b3-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="220b3-165">Tapahtuman tyyppi</span><span class="sxs-lookup"><span data-stu-id="220b3-165">Entry Type</span></span>|<span data-ttu-id="220b3-166">Nimikenumero</span><span class="sxs-lookup"><span data-stu-id="220b3-166">Item Number</span></span>|<span data-ttu-id="220b3-167">Sijaintikoodi </span><span class="sxs-lookup"><span data-stu-id="220b3-167">Location Code</span></span>|<span data-ttu-id="220b3-168">Varastopaikan koodi</span><span class="sxs-lookup"><span data-stu-id="220b3-168">Bin Code</span></span>|<span data-ttu-id="220b3-169">määrä</span><span class="sxs-lookup"><span data-stu-id="220b3-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="220b3-170">Posit. muutos</span><span class="sxs-lookup"><span data-stu-id="220b3-170">Positive Adjmt.</span></span>|<span data-ttu-id="220b3-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="220b3-171">1928-S</span></span>|<span data-ttu-id="220b3-172">ETELÄ</span><span class="sxs-lookup"><span data-stu-id="220b3-172">SOUTH</span></span>|<span data-ttu-id="220b3-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="220b3-173">S-01-0001</span></span>|<span data-ttu-id="220b3-174">20</span><span class="sxs-lookup"><span data-stu-id="220b3-174">20</span></span>|  
        |<span data-ttu-id="220b3-175">Posit. muutos</span><span class="sxs-lookup"><span data-stu-id="220b3-175">Positive Adjmt.</span></span>|<span data-ttu-id="220b3-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="220b3-176">1928-S</span></span>|<span data-ttu-id="220b3-177">ETELÄ</span><span class="sxs-lookup"><span data-stu-id="220b3-177">SOUTH</span></span>|<span data-ttu-id="220b3-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="220b3-178">S-01-0002</span></span>|<span data-ttu-id="220b3-179">20</span><span class="sxs-lookup"><span data-stu-id="220b3-179">20</span></span>|  

        <span data-ttu-id="220b3-180">Oletusarvoisesti myyntirivien **Varastopaikan koodi** -kentät on piilotettu, joten ne on tuotava näkyviin.</span><span class="sxs-lookup"><span data-stu-id="220b3-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="220b3-181">Sen tehdäksesi sinun on muokattava sivua.</span><span class="sxs-lookup"><span data-stu-id="220b3-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="220b3-182">Lisätietoja on kohdassa, jossa [Sivun mukauttaminen mukautusvalintanauhan avulla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="220b3-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="220b3-183">Valitse **Toiminnot**, sitten **Kirjaus** ja valitse sitten **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="220b3-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="220b3-184">Valitse **Kyllä**-painike.</span><span class="sxs-lookup"><span data-stu-id="220b3-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="220b3-185">Myyntitilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="220b3-185">Creating the Sales Order</span></span>

<span data-ttu-id="220b3-186">Myyntitilaukset ovat yleisin lähtevien lähdeasiakirjojen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="220b3-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="220b3-187">Myyntitilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="220b3-187">To create the sales order</span></span>

1. <span data-ttu-id="220b3-188">Valitse kolmas ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="220b3-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="220b3-189">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="220b3-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="220b3-190">Luo myyntitilaus asiakkaalle 10000 (23.1.) käsittelypäivämääränä seuraavien myyntitilausrivin kanssa.</span><span class="sxs-lookup"><span data-stu-id="220b3-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="220b3-191">Nimike</span><span class="sxs-lookup"><span data-stu-id="220b3-191">Item</span></span>|<span data-ttu-id="220b3-192">Sijaintikoodi </span><span class="sxs-lookup"><span data-stu-id="220b3-192">Location Code</span></span>|<span data-ttu-id="220b3-193">määrä</span><span class="sxs-lookup"><span data-stu-id="220b3-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="220b3-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="220b3-194">1928-S</span></span>|<span data-ttu-id="220b3-195">ETELÄ</span><span class="sxs-lookup"><span data-stu-id="220b3-195">SOUTH</span></span>|<span data-ttu-id="220b3-196">30</span><span class="sxs-lookup"><span data-stu-id="220b3-196">30</span></span>|  

     <span data-ttu-id="220b3-197">Siirry ja ilmoita varastolle, että myyntitilaus on valmis varaston käsittelyyn, kun toimitus saapuu.</span><span class="sxs-lookup"><span data-stu-id="220b3-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="220b3-198">Valitse **Vapauta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="220b3-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="220b3-199">John etenee nimikkeiden poimintaan ja toimitukseen.</span><span class="sxs-lookup"><span data-stu-id="220b3-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="220b3-200">Nimikkeiden poiminta ja toimitus</span><span class="sxs-lookup"><span data-stu-id="220b3-200">Picking and Shipping Items</span></span>

<span data-ttu-id="220b3-201">**Varaston poiminta** -sivulla voit hallita kaikkia tietyn lähdeasiakirjan lähteviä varastointiaktiviteetteja, kuten myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="220b3-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="220b3-202">Nimikkeiden poiminta ja lähettäminen</span><span class="sxs-lookup"><span data-stu-id="220b3-202">To pick and ship items</span></span>

1. <span data-ttu-id="220b3-203">Valitse neljäs ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varaston poiminnat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="220b3-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="220b3-204">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="220b3-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="220b3-205">Varmista, että **Nro**-kenttä</span><span class="sxs-lookup"><span data-stu-id="220b3-205">Make sure that the **No.**</span></span> <span data-ttu-id="220b3-206">täytetään **Yleinen**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="220b3-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="220b3-207">Valitse **Lähdeasiakirja**-kenttä ja sitten **Myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="220b3-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="220b3-208">Valitse **Lähdenro**-kentässä asiakkaalle 10000 tehdyn myynnin rivi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="220b3-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="220b3-209">Vaihtoehtoisesti voit valita ensin **Hae lähdeasiakirja** -toiminnon ja sitten myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="220b3-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="220b3-210">Valitse **Täytä autom. käsitelt. määrä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="220b3-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="220b3-211">Syötä vaihtoehtoisesti **Käsiteltävä määrä** -kentässä vastaavasti 10 ja 20 kahdelle varastonpoimintariville.</span><span class="sxs-lookup"><span data-stu-id="220b3-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="220b3-212">Valita ensin **Kirjaa**-toiminto, sitten **Toimitus** ja lopuksi **OK**.</span><span class="sxs-lookup"><span data-stu-id="220b3-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="220b3-213">30 Amsterdam-lamppua on nyt rekisteröity poimituiksi varastopaikoista S-01-0001- ja S-01-0002, ja luodaan negatiivinen nimiketapahtuma, joka heijastaa kirjattua myyntitoimitusta.</span><span class="sxs-lookup"><span data-stu-id="220b3-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="220b3-214">Katso myös</span><span class="sxs-lookup"><span data-stu-id="220b3-214">See Also</span></span>

[<span data-ttu-id="220b3-215">Nimikkeiden poiminta varastopoiminnalla</span><span class="sxs-lookup"><span data-stu-id="220b3-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="220b3-216">Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten</span><span class="sxs-lookup"><span data-stu-id="220b3-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="220b3-217">Fyysisten perusvarastojen ja toimintoalueiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="220b3-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="220b3-218">Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä</span><span class="sxs-lookup"><span data-stu-id="220b3-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="220b3-219">Poiminta tuotantoon tai kokoonpanoon</span><span class="sxs-lookup"><span data-stu-id="220b3-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="220b3-220">Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä</span><span class="sxs-lookup"><span data-stu-id="220b3-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="220b3-221">Rakennetiedot: lähtevän fyysisen varastoinnin virta</span><span class="sxs-lookup"><span data-stu-id="220b3-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="220b3-222">Liiketoimintaprosessien vaihekuvaukset</span><span class="sxs-lookup"><span data-stu-id="220b3-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="220b3-223">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="220b3-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
