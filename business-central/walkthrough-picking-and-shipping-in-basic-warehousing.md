---
title: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä | Microsoft Docs
description: Business Central -sovelluksessa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3815e0e928041ca9fcef09b1c7410e45ebb57a1
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035754"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="811e9-103">Vaihekuvaus: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä</span><span class="sxs-lookup"><span data-stu-id="811e9-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="811e9-104">[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.</span><span class="sxs-lookup"><span data-stu-id="811e9-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="811e9-105">Tapa</span><span class="sxs-lookup"><span data-stu-id="811e9-105">Method</span></span>|<span data-ttu-id="811e9-106">Saapuva prosessi</span><span class="sxs-lookup"><span data-stu-id="811e9-106">Inbound process</span></span>|<span data-ttu-id="811e9-107">Varastopaikat</span><span class="sxs-lookup"><span data-stu-id="811e9-107">Bins</span></span>|<span data-ttu-id="811e9-108">Poiminnat</span><span class="sxs-lookup"><span data-stu-id="811e9-108">Picks</span></span>|<span data-ttu-id="811e9-109">Toimitukset</span><span class="sxs-lookup"><span data-stu-id="811e9-109">Shipments</span></span>|<span data-ttu-id="811e9-110">Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="811e9-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="811e9-111">L</span><span class="sxs-lookup"><span data-stu-id="811e9-111">A</span></span>|<span data-ttu-id="811e9-112">Poiminnan ja toimituksen kirjaaminen tilausriviltä</span><span class="sxs-lookup"><span data-stu-id="811e9-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="811e9-113">X</span><span class="sxs-lookup"><span data-stu-id="811e9-113">X</span></span>|||<span data-ttu-id="811e9-114">2</span><span class="sxs-lookup"><span data-stu-id="811e9-114">2</span></span>|  
|<span data-ttu-id="811e9-115">B</span><span class="sxs-lookup"><span data-stu-id="811e9-115">B</span></span>|<span data-ttu-id="811e9-116">Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta</span><span class="sxs-lookup"><span data-stu-id="811e9-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="811e9-117">X</span><span class="sxs-lookup"><span data-stu-id="811e9-117">X</span></span>||<span data-ttu-id="811e9-118">3</span><span class="sxs-lookup"><span data-stu-id="811e9-118">3</span></span>|  
|<span data-ttu-id="811e9-119">N</span><span class="sxs-lookup"><span data-stu-id="811e9-119">C</span></span>|<span data-ttu-id="811e9-120">Kirjaa poiminta ja lähetyksen fyysisen varastoinnin toimituksen asiakirjasta</span><span class="sxs-lookup"><span data-stu-id="811e9-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="811e9-121">X</span><span class="sxs-lookup"><span data-stu-id="811e9-121">X</span></span>|<span data-ttu-id="811e9-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="811e9-122">4/5/6</span></span>|  
|<span data-ttu-id="811e9-123">P</span><span class="sxs-lookup"><span data-stu-id="811e9-123">D</span></span>|<span data-ttu-id="811e9-124">Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimituksen asiakirjasta</span><span class="sxs-lookup"><span data-stu-id="811e9-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="811e9-125">X</span><span class="sxs-lookup"><span data-stu-id="811e9-125">X</span></span>|<span data-ttu-id="811e9-126">X</span><span class="sxs-lookup"><span data-stu-id="811e9-126">X</span></span>|<span data-ttu-id="811e9-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="811e9-127">4/5/6</span></span>|  

<span data-ttu-id="811e9-128">Katso lisätietoja kohdasta [Rakennetiedot: lähtevän fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="811e9-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="811e9-129">Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.</span><span class="sxs-lookup"><span data-stu-id="811e9-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="about-this-walkthrough"></a><span data-ttu-id="811e9-130">Tietoja tästä vaihekuvauksesta</span><span class="sxs-lookup"><span data-stu-id="811e9-130">About This Walkthrough</span></span>

<span data-ttu-id="811e9-131">Jos sijainnit on määritetty fyysisen varastoinnin perusmäärityksissä edellyttämään poimintakäsittelyä mutta ei toimituskäsittelyä, **Varaston poiminta** -sivua on käytettävä lähtevien lähdeasiakirjojen poiminta- ja toimitustietojen tallennuksessa ja kirjaamisessa.</span><span class="sxs-lookup"><span data-stu-id="811e9-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="811e9-132">Lähtevä lähdeasiakirja voi olla myyntitilaus, ostopalautustilaus, lähtevä siirtotilaus tai tuotantotilaus komponenttitarpeella.</span><span class="sxs-lookup"><span data-stu-id="811e9-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="811e9-133">Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="811e9-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="811e9-134">HOPEA-sijainnin määrittäminen varastopaikan käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="811e9-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="811e9-135">Luo myyntitilaus asiakkaalle 10000 30 kaiuttimesta.</span><span class="sxs-lookup"><span data-stu-id="811e9-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="811e9-136">Myyntitilauksen vapauttaminen varaston käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="811e9-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="811e9-137">Varastopoiminnan julkaistusta lähdeasiakirjasta luominen</span><span class="sxs-lookup"><span data-stu-id="811e9-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="811e9-138">Rekisteröidään fyysisen varastoinnin siirtoa varastosta ja kirjataan samanaikaisesti lähdemyyntitilauksen myyntitoimitusta.</span><span class="sxs-lookup"><span data-stu-id="811e9-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a><span data-ttu-id="811e9-139">Roolit</span><span class="sxs-lookup"><span data-stu-id="811e9-139">Roles</span></span>

<span data-ttu-id="811e9-140">Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="811e9-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="811e9-141">Varastopäällikkö</span><span class="sxs-lookup"><span data-stu-id="811e9-141">Warehouse Manager</span></span>  
- <span data-ttu-id="811e9-142">Tilausten käsittelijä</span><span class="sxs-lookup"><span data-stu-id="811e9-142">Order Processor</span></span>  
- <span data-ttu-id="811e9-143">Varastotyöntekijä</span><span class="sxs-lookup"><span data-stu-id="811e9-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="811e9-144">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="811e9-144">Prerequisites</span></span>

<span data-ttu-id="811e9-145">Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:</span><span class="sxs-lookup"><span data-stu-id="811e9-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="811e9-146">[!INCLUDE[prod_short](includes/prod_short.md)] online: yritys perustuu eristysympäristön **Laajennettu arviointi - Kaikki mallitiedot** -vaihtoehtoon.</span><span class="sxs-lookup"><span data-stu-id="811e9-146">For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="811e9-147">[!INCLUDE[prod_short](includes/prod_short.md)] on-premises: CRONUS International Ltd. asennetaan.</span><span class="sxs-lookup"><span data-stu-id="811e9-147">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="811e9-148">Tee itsestäsi fyysisen varaston työntekijä sijainnissa HOPEA seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="811e9-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="811e9-149">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastotyöntekijät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="811e9-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="811e9-150">Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="811e9-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="811e9-151">Kirjoita **Sijaintikoodi**-kenttään HOPEA.</span><span class="sxs-lookup"><span data-stu-id="811e9-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="811e9-152">Valitse **Oletus**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="811e9-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="811e9-153">Valmistusnimike LS-81 saatavilla HOPEA-sijaintiin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="811e9-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="811e9-154">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikepäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="811e9-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="811e9-155">Avaa oletuspäiväkirja ja luo kaksi nimikepäiväkirjan riviä seuraavilla käsittelypäivämäärän tiedoilla (23. tammikuuta).</span><span class="sxs-lookup"><span data-stu-id="811e9-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="811e9-156">Tapahtuman tyyppi</span><span class="sxs-lookup"><span data-stu-id="811e9-156">Entry Type</span></span>|<span data-ttu-id="811e9-157">Nimikenumero</span><span class="sxs-lookup"><span data-stu-id="811e9-157">Item Number</span></span>|<span data-ttu-id="811e9-158">Sijaintikoodi </span><span class="sxs-lookup"><span data-stu-id="811e9-158">Location Code</span></span>|<span data-ttu-id="811e9-159">Varastopaikan koodi</span><span class="sxs-lookup"><span data-stu-id="811e9-159">Bin Code</span></span>|<span data-ttu-id="811e9-160">määrä</span><span class="sxs-lookup"><span data-stu-id="811e9-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="811e9-161">Posit. muutos</span><span class="sxs-lookup"><span data-stu-id="811e9-161">Positive Adjmt.</span></span>|<span data-ttu-id="811e9-162">LS_81</span><span class="sxs-lookup"><span data-stu-id="811e9-162">LS-81</span></span>|<span data-ttu-id="811e9-163">HOPEINEN</span><span class="sxs-lookup"><span data-stu-id="811e9-163">SILVER</span></span>|<span data-ttu-id="811e9-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="811e9-164">S-01-0001</span></span>|<span data-ttu-id="811e9-165">20</span><span class="sxs-lookup"><span data-stu-id="811e9-165">20</span></span>|  
        |<span data-ttu-id="811e9-166">Posit. muutos</span><span class="sxs-lookup"><span data-stu-id="811e9-166">Positive Adjmt.</span></span>|<span data-ttu-id="811e9-167">LS_81</span><span class="sxs-lookup"><span data-stu-id="811e9-167">LS-81</span></span>|<span data-ttu-id="811e9-168">HOPEINEN</span><span class="sxs-lookup"><span data-stu-id="811e9-168">SILVER</span></span>|<span data-ttu-id="811e9-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="811e9-169">S-01-0002</span></span>|<span data-ttu-id="811e9-170">20</span><span class="sxs-lookup"><span data-stu-id="811e9-170">20</span></span>|  

  3. <span data-ttu-id="811e9-171">Valitse ensin **Kirjaa** -toiminto ja sitten **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="811e9-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="811e9-172">Taustatietoja</span><span class="sxs-lookup"><span data-stu-id="811e9-172">Story</span></span>

<span data-ttu-id="811e9-173">Ellen, CRONUS:n varastopäällikkö, määrittää HOPEISEN varaston Basic-poiminnan käsittelyä varten,jossa varastotyöntekijät käsittelevät lähtevät tilaukset erikseen.</span><span class="sxs-lookup"><span data-stu-id="811e9-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="811e9-174">Susanna, tilausten käsittelijä luo myyntitilauksen LS-81-nimikkeen 30 yksikön toimituksesta asiakkaalle 10000 HOPEISESTA varastosta.</span><span class="sxs-lookup"><span data-stu-id="811e9-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="811e9-175">Johnin, varastotyöntekijän, täytyy varmistaa, että lähetys on valmisteltu ja toimitettu asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="811e9-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="811e9-176">John hallitsee kaikkia **Varaston poiminta** -sivulla olevia tehtäviä, jotka viittaavat automaattisesti varastopaikkoihin, joissa LS-81 on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="811e9-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="811e9-177">Sijainnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="811e9-177">Setting Up the Location</span></span>

<span data-ttu-id="811e9-178">**Sijaintikortti**-sivun asetuksissa määritellään yrityksen varaston työnkulut.</span><span class="sxs-lookup"><span data-stu-id="811e9-178">The setup of the **Location Card** page defines the company's warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="811e9-179">Sijainnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="811e9-179">To set up the location</span></span>

1. <span data-ttu-id="811e9-180">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sijainnit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="811e9-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2. <span data-ttu-id="811e9-181">Avaa asianmukaisen HOPEA sijainnin kortti.</span><span class="sxs-lookup"><span data-stu-id="811e9-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="811e9-182">Valitse **Fyysinen varasto** -pikavälilehdessä **Vaadi poiminta** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="811e9-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="811e9-183">Myyntitilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="811e9-183">Creating the Sales Order</span></span>

<span data-ttu-id="811e9-184">Myyntitilaukset ovat yleisin lähtevien lähdeasiakirjojen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="811e9-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="811e9-185">Myyntitilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="811e9-185">To create the sales order</span></span>

1. <span data-ttu-id="811e9-186">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="811e9-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="811e9-187">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="811e9-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="811e9-188">Luo myyntitilaus asiakkaalle 10000 (23.1.) käsittelypäivämääränä seuraavien myyntitilausrivin kanssa.</span><span class="sxs-lookup"><span data-stu-id="811e9-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="811e9-189">Nimike</span><span class="sxs-lookup"><span data-stu-id="811e9-189">Item</span></span>|<span data-ttu-id="811e9-190">Sijaintikoodi </span><span class="sxs-lookup"><span data-stu-id="811e9-190">Location Code</span></span>|<span data-ttu-id="811e9-191">määrä.</span><span class="sxs-lookup"><span data-stu-id="811e9-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="811e9-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="811e9-192">LS_81</span></span>|<span data-ttu-id="811e9-193">HOPEINEN</span><span class="sxs-lookup"><span data-stu-id="811e9-193">SILVER</span></span>|<span data-ttu-id="811e9-194">30</span><span class="sxs-lookup"><span data-stu-id="811e9-194">30</span></span>|  

     <span data-ttu-id="811e9-195">Siirry ja ilmoita varastolle, että myyntitilaus on valmis varaston käsittelyyn, kun toimitus saapuu.</span><span class="sxs-lookup"><span data-stu-id="811e9-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="811e9-196">Valitse **Vapauta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="811e9-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="811e9-197">John etenee nimikkeiden poimintaan ja toimitukseen.</span><span class="sxs-lookup"><span data-stu-id="811e9-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="811e9-198">Nimikkeiden poiminta ja toimitus</span><span class="sxs-lookup"><span data-stu-id="811e9-198">Picking and Shipping Items</span></span>

<span data-ttu-id="811e9-199">**Varaston poiminta** -sivulla voit hallita kaikkia tietyn lähdeasiakirjan lähteviä varastointiaktiviteetteja, kuten myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="811e9-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="811e9-200">Nimikkeiden poiminta ja lähettäminen</span><span class="sxs-lookup"><span data-stu-id="811e9-200">To pick and ship items</span></span>

1. <span data-ttu-id="811e9-201">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varaston poiminnat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="811e9-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="811e9-202">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="811e9-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="811e9-203">Varmista, että **Nro**-kenttä</span><span class="sxs-lookup"><span data-stu-id="811e9-203">Make sure that the **No.**</span></span> <span data-ttu-id="811e9-204">täytetään **Yleinen**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="811e9-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="811e9-205">Valitse **Lähdeasiakirja**-kenttä ja sitten **Myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="811e9-205">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="811e9-206">Valitse **Lähdenro**-kentässä asiakkaalle 10000 tehdyn myynnin rivi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="811e9-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="811e9-207">Vaihtoehtoisesti voit valita ensin **Hae lähdeasiakirja** -toiminnon ja sitten myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="811e9-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="811e9-208">Valitse **Täytä autom. käsitelt. määrä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="811e9-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="811e9-209">Syötä vaihtoehtoisesti **Käsiteltävä määrä** -kentässä vastaavasti 10 ja 20 kahdelle varastonpoimintariville.</span><span class="sxs-lookup"><span data-stu-id="811e9-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="811e9-210">Valita ensin **Kirjaa**-toiminto, sitten **Toimitus** ja lopuksi **OK**.</span><span class="sxs-lookup"><span data-stu-id="811e9-210">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="811e9-211">30 kaiutinta on nyt rekisteröity poimituiksi varastopaikoista S-01-0001- ja S-01-0002, ja luodaan negatiivinen nimiketapahtuma, joka heijastaa kirjattua myyntitoimitusta.</span><span class="sxs-lookup"><span data-stu-id="811e9-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="811e9-212">Katso myös</span><span class="sxs-lookup"><span data-stu-id="811e9-212">See Also</span></span>

[<span data-ttu-id="811e9-213">Nimikkeiden poiminta varastopoiminnalla</span><span class="sxs-lookup"><span data-stu-id="811e9-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="811e9-214">Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten</span><span class="sxs-lookup"><span data-stu-id="811e9-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="811e9-215">Fyysisten perusvarastojen ja toimintoalueiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="811e9-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="811e9-216">Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä</span><span class="sxs-lookup"><span data-stu-id="811e9-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="811e9-217">Poiminta tuotantoon tai kokoonpanoon</span><span class="sxs-lookup"><span data-stu-id="811e9-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="811e9-218">Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä</span><span class="sxs-lookup"><span data-stu-id="811e9-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="811e9-219">Rakennetiedot: lähtevän fyysisen varastoinnin virta</span><span class="sxs-lookup"><span data-stu-id="811e9-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="811e9-220">Liiketoimintaprosessien vaihekuvaukset</span><span class="sxs-lookup"><span data-stu-id="811e9-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="811e9-221">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="811e9-221">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
