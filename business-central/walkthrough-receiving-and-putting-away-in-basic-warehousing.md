---
title: "Vaihekuvaus – Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä | Microsoft Docs"
description: "Business Central -sovelluksessa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 0ba61572a237e177b763b7b8a2e13ca7ec93eea4
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="48ecf-103">Vaihekuvaus: Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä</span><span class="sxs-lookup"><span data-stu-id="48ecf-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>
<span data-ttu-id="48ecf-104">[!INCLUDE[d365fin](includes/d365fin_md.md)]issa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="48ecf-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="48ecf-105">Tapa</span><span class="sxs-lookup"><span data-stu-id="48ecf-105">Method</span></span>|<span data-ttu-id="48ecf-106">Saapuva prosessi</span><span class="sxs-lookup"><span data-stu-id="48ecf-106">Inbound process</span></span>|<span data-ttu-id="48ecf-107">Varastopaikat</span><span class="sxs-lookup"><span data-stu-id="48ecf-107">Bins</span></span>|<span data-ttu-id="48ecf-108">Vastaanotot</span><span class="sxs-lookup"><span data-stu-id="48ecf-108">Receipts</span></span>|<span data-ttu-id="48ecf-109">Hyllytykset</span><span class="sxs-lookup"><span data-stu-id="48ecf-109">Put-aways</span></span>|<span data-ttu-id="48ecf-110">Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="48ecf-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="48ecf-111">L</span><span class="sxs-lookup"><span data-stu-id="48ecf-111">A</span></span>|<span data-ttu-id="48ecf-112">Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä</span><span class="sxs-lookup"><span data-stu-id="48ecf-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="48ecf-113">X</span><span class="sxs-lookup"><span data-stu-id="48ecf-113">X</span></span>|||<span data-ttu-id="48ecf-114">2</span><span class="sxs-lookup"><span data-stu-id="48ecf-114">2</span></span>|  
|<span data-ttu-id="48ecf-115">B</span><span class="sxs-lookup"><span data-stu-id="48ecf-115">B</span></span>|<span data-ttu-id="48ecf-116">Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta</span><span class="sxs-lookup"><span data-stu-id="48ecf-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="48ecf-117">X</span><span class="sxs-lookup"><span data-stu-id="48ecf-117">X</span></span>|<span data-ttu-id="48ecf-118">3</span><span class="sxs-lookup"><span data-stu-id="48ecf-118">3</span></span>|  
|<span data-ttu-id="48ecf-119">N</span><span class="sxs-lookup"><span data-stu-id="48ecf-119">C</span></span>|<span data-ttu-id="48ecf-120">Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta</span><span class="sxs-lookup"><span data-stu-id="48ecf-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="48ecf-121">X</span><span class="sxs-lookup"><span data-stu-id="48ecf-121">X</span></span>||<span data-ttu-id="48ecf-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="48ecf-122">4/5/6</span></span>|  
|<span data-ttu-id="48ecf-123">P</span><span class="sxs-lookup"><span data-stu-id="48ecf-123">D</span></span>|<span data-ttu-id="48ecf-124">Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta</span><span class="sxs-lookup"><span data-stu-id="48ecf-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="48ecf-125">X</span><span class="sxs-lookup"><span data-stu-id="48ecf-125">X</span></span>|<span data-ttu-id="48ecf-126">X</span><span class="sxs-lookup"><span data-stu-id="48ecf-126">X</span></span>|<span data-ttu-id="48ecf-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="48ecf-127">4/5/6</span></span>|  

<span data-ttu-id="48ecf-128">Lisätietoja on kohdassa [Rakennetiedot: Saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="48ecf-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="48ecf-129">Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.</span><span class="sxs-lookup"><span data-stu-id="48ecf-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="48ecf-130">Tietoja tästä vaihekuvauksesta</span><span class="sxs-lookup"><span data-stu-id="48ecf-130">About This Walkthrough</span></span>  
<span data-ttu-id="48ecf-131">Jos fyysisen varastoinnin perusmääritykset määrittävät sijainnin edellyttämään hyllytyksen muttei vastaanoton käsittelyä, saapuvien lähdeasiakirjojen hyllytys- ja vastaanottotiedot tallennetaan ja kirjataan **Varastohyllytys**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="48ecf-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="48ecf-132">Saapuva lähdeasiakirja voi olla ostotilaus, myyntipalautustilaus, saapuva siirtotilaus tai tuotantotilaus jonka tuotos odottaa hyllytystä.</span><span class="sxs-lookup"><span data-stu-id="48ecf-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="48ecf-133">Vaikka asetusten nimenä on **Vaadi poiminta** ja **Vaadi hyllytys**, voit silti kirjata vastaanottoja ja toimituksia suoraan lähdeasiakirjoista sijainneissa, joissa olet valinnut nämä valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="48ecf-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="48ecf-134">Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="48ecf-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="48ecf-135">HOPEA-sijainnin määrittäminen varastopaikan hyllytykseen.</span><span class="sxs-lookup"><span data-stu-id="48ecf-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="48ecf-136">HOPEA-sijainnin määrittäminen varastopaikan käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="48ecf-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="48ecf-137">Oletusvarastopaikan määrittäminen nimikkeelle LS-81.</span><span class="sxs-lookup"><span data-stu-id="48ecf-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="48ecf-138">(LS-75 on jo määritetty CRONUSISSA.)</span><span class="sxs-lookup"><span data-stu-id="48ecf-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="48ecf-139">Luo ostotilaus toimittajalle 10000 40 kaiuttimesta.</span><span class="sxs-lookup"><span data-stu-id="48ecf-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="48ecf-140">Tarkistetaan, että hyllytyksen varastopaikat määritetään ennalta asetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="48ecf-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="48ecf-141">Ostotilauksen vapauttaminen varaston käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="48ecf-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="48ecf-142">Varastohyllytyksen julkaistusta lähdeasiakirjasta luominen</span><span class="sxs-lookup"><span data-stu-id="48ecf-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="48ecf-143">Tarkistetaan, että hyllytyksen varastopaikat peritään ostotilauksesta.</span><span class="sxs-lookup"><span data-stu-id="48ecf-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="48ecf-144">Rekisteröidään fyysisen varastoinnin siirtoa varastoon ja kirjataan samanaikaisesti lähdeostotilauksen ostokuittia.</span><span class="sxs-lookup"><span data-stu-id="48ecf-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="48ecf-145">Roolit</span><span class="sxs-lookup"><span data-stu-id="48ecf-145">Roles</span></span>  
<span data-ttu-id="48ecf-146">Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="48ecf-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="48ecf-147">Varastopäällikkö</span><span class="sxs-lookup"><span data-stu-id="48ecf-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="48ecf-148">Ostaja</span><span class="sxs-lookup"><span data-stu-id="48ecf-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="48ecf-149">Varastotyöntekijä</span><span class="sxs-lookup"><span data-stu-id="48ecf-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="48ecf-150">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="48ecf-150">Prerequisites</span></span>  
<span data-ttu-id="48ecf-151">Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:</span><span class="sxs-lookup"><span data-stu-id="48ecf-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="48ecf-152">CRONUS Finland Oy on asennettu.</span><span class="sxs-lookup"><span data-stu-id="48ecf-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="48ecf-153">Tee itsestäsi fyysisen varaston työntekijä HOPEISESSA sijainnissa tekemällä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="48ecf-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="48ecf-154">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Varaston työntekijät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="48ecf-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="48ecf-155">Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="48ecf-155">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="48ecf-156">Kirjoita **Sijaintikoodi**-kenttään HOPEA.</span><span class="sxs-lookup"><span data-stu-id="48ecf-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="48ecf-157">Valitse **Oletus**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="48ecf-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="48ecf-158">Taustatietoja</span><span class="sxs-lookup"><span data-stu-id="48ecf-158">Story</span></span>  
<span data-ttu-id="48ecf-159">Ellen on CRONUS Finland Oy:n varastopäällikkö ja hän luo ostotilauksen, jossa on 10 yksikköä LS-75-nimikettä ja 30 yksikköä LS-81-nimikettä, toimittajalta 10000 toimitettavaksi HOPEISEEN varastoon.</span><span class="sxs-lookup"><span data-stu-id="48ecf-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="48ecf-160">Kun toimitus saapuu varastoon, varastotyöntekijä Joakim hyllyttää nimikkeitä niille määritettyihin oletusvarastopaikkoihin.</span><span class="sxs-lookup"><span data-stu-id="48ecf-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="48ecf-161">Kun Joakim kirjaa hyllytyksen, nimikkeet kirjataan vastaanotetuksi varastoon, ja ne ovat käytettävissä myyntiä tai muita kysyntää varten.</span><span class="sxs-lookup"><span data-stu-id="48ecf-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="48ecf-162">Sijainnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="48ecf-162">Setting up the Location</span></span>  
 <span data-ttu-id="48ecf-163">**Sijaintikortti**-sivun asetuksissa määritellään yrityksen varaston työnkulut.</span><span class="sxs-lookup"><span data-stu-id="48ecf-163">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="48ecf-164">Sijainnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="48ecf-164">To set up the location</span></span>  

1.  <span data-ttu-id="48ecf-165">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="48ecf-165">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48ecf-166">Avaa asianmukaisen HOPEA sijainnin kortti.</span><span class="sxs-lookup"><span data-stu-id="48ecf-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="48ecf-167">Valitse **Vaadi hyllytys** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="48ecf-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="48ecf-168">Siirry määrittämään oletusvarastopaikka kahdelle nimikenumerolla, jotka valvovat, missä ne on hyllytetty.</span><span class="sxs-lookup"><span data-stu-id="48ecf-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="48ecf-169">Valitse **Varastopaikat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="48ecf-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="48ecf-170">Valitse varastopaikan S-01-0001 ensimmäinen rivi ja valitse sitten **Sisältö**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="48ecf-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="48ecf-171">Huomaa **Varastopaikan sisältö** -sivulla, että nimike LS-75 on jo määritetty sisällöksi varastopaikassa S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="48ecf-171">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="48ecf-172">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="48ecf-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="48ecf-173">Valitse **Kiinteä**- ja **Oletus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="48ecf-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="48ecf-174">Anna **Nimikenro**-kentässä LS-81.</span><span class="sxs-lookup"><span data-stu-id="48ecf-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="48ecf-175">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="48ecf-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="48ecf-176">Ostotilaukset ovat yleisin saapuvien lähdeasiakirjojen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="48ecf-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="48ecf-177">Ostotilausten luominen</span><span class="sxs-lookup"><span data-stu-id="48ecf-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="48ecf-178">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="48ecf-178">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48ecf-179">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="48ecf-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="48ecf-180">Luo ostotilaus toimittajalle 10000 (23.1.) käsittelypäivämääränä seuraavien ostontilausrivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="48ecf-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="48ecf-181">Nimike</span><span class="sxs-lookup"><span data-stu-id="48ecf-181">Item</span></span>|<span data-ttu-id="48ecf-182">Sijaintikoodi</span><span class="sxs-lookup"><span data-stu-id="48ecf-182">Location code</span></span>|<span data-ttu-id="48ecf-183">Varastopaikan koodi</span><span class="sxs-lookup"><span data-stu-id="48ecf-183">Bin code</span></span>|<span data-ttu-id="48ecf-184">määrä.</span><span class="sxs-lookup"><span data-stu-id="48ecf-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="48ecf-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="48ecf-185">LS_75</span></span>|<span data-ttu-id="48ecf-186">HOPEINEN</span><span class="sxs-lookup"><span data-stu-id="48ecf-186">SILVER</span></span>|<span data-ttu-id="48ecf-187">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="48ecf-187">S-01-0001</span></span>|<span data-ttu-id="48ecf-188">10</span><span class="sxs-lookup"><span data-stu-id="48ecf-188">10</span></span>|  
    |<span data-ttu-id="48ecf-189">LS_81</span><span class="sxs-lookup"><span data-stu-id="48ecf-189">LS-81</span></span>|<span data-ttu-id="48ecf-190">HOPEINEN</span><span class="sxs-lookup"><span data-stu-id="48ecf-190">SILVER</span></span>|<span data-ttu-id="48ecf-191">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="48ecf-191">S-01-0001</span></span>|<span data-ttu-id="48ecf-192">30</span><span class="sxs-lookup"><span data-stu-id="48ecf-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="48ecf-193">Varastopaikkakoodi lisätään automaattisesti "Sijainnin määrittäminen" -osassa suorittamiesi määritysten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="48ecf-193">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="48ecf-194">Siirry ja ilmoita varastolle, että ostotilaus on valmis varaston käsittelyyn, kun toimitus saapuu.</span><span class="sxs-lookup"><span data-stu-id="48ecf-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="48ecf-195">Valitse **Vapauta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="48ecf-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="48ecf-196">Kaiuttimien toimitus toimittajalta 10000 on saapunut HOPEISEEN varastoon, ja John ryhtyy hyllyttämään niitä.</span><span class="sxs-lookup"><span data-stu-id="48ecf-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="48ecf-197">Nimikkeiden vastaanottaminen ja hyllyttäminen</span><span class="sxs-lookup"><span data-stu-id="48ecf-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="48ecf-198">Voit hallita **Varastohyllytys**-sivulla kaikkia tietyn lähdeasiakirjan saapuvia varastotoimintoja, kuten ostotilausta.</span><span class="sxs-lookup"><span data-stu-id="48ecf-198">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="48ecf-199">Nimikkeiden vastaanottaminen ja hyllyttäminen</span><span class="sxs-lookup"><span data-stu-id="48ecf-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="48ecf-200">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston hyllytykset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="48ecf-200">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48ecf-201">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="48ecf-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="48ecf-202">Valitse ensin **Lähdeasiakirja**-kenttä ja sitten **Ostotilaus**.</span><span class="sxs-lookup"><span data-stu-id="48ecf-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="48ecf-203">Valitse **Lähteen nro** -kentässä toimittajalta 10000 tehdyn oston rivi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="48ecf-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="48ecf-204">Valitse vaihtoehtoisesti **Toiminnot**-välilehden **Funktiot**-ryhmässä **Hae lähdeasiakirja**, ja valitse ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="48ecf-204">Alternatively, on the **Actions** tab, in the **Functions** group, choose **Get Source Document**, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="48ecf-205">Valitse **Täytä autom. käsitelt. määrä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="48ecf-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="48ecf-206">Vaihtoehtoisesti voit antaa **Käsiteltävä määrä** -kentässä 10 ja 30 kahdelle varastohyllytysriville.</span><span class="sxs-lookup"><span data-stu-id="48ecf-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="48ecf-207">Valitse ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-toiminto ja lopuksi **OK**.</span><span class="sxs-lookup"><span data-stu-id="48ecf-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="48ecf-208">40 kaiutinta on nyt rekisteröity hyllytetyiksi varastopaikasta S-01-0001, ja luodaan positiivinen nimiketapahtuma, joka heijastaa kirjattua ostotoimitusta.</span><span class="sxs-lookup"><span data-stu-id="48ecf-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="48ecf-209">Katso myös</span><span class="sxs-lookup"><span data-stu-id="48ecf-209">See Also</span></span>  
 <span data-ttu-id="48ecf-210">[Nimikkeiden hyllyttäminen varastohyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="48ecf-210">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="48ecf-211">[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="48ecf-211">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="48ecf-212">[Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="48ecf-212">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="48ecf-213">[Poiminta tuotantoon tai kokoonpanoon](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="48ecf-213">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="48ecf-214">[Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="48ecf-214">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="48ecf-215">[Rakennetiedot: saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="48ecf-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="48ecf-216">Liiketoimintaprosessien vaihekuvaukset</span><span class="sxs-lookup"><span data-stu-id="48ecf-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="48ecf-217">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="48ecf-217">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

