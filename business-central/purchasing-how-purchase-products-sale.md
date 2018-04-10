---
title: Nimikkeiden ostaminen myyntiin ostolaskuja luomalla | Microsoft Docs
description: Voit ostaa tuotteita luomalla toimittajan ostolaskun myyntilaskusta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: d5ae63043a6f296de22f71c401a5686f970ad3a0
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="purchase-items-for-a-sale"></a><span data-ttu-id="4055f-103">Nimikkeiden ostaminen myyntiin</span><span class="sxs-lookup"><span data-stu-id="4055f-103">Purchase Items for a Sale</span></span>
<span data-ttu-id="4055f-104">Voit luoda myyntitilausten ja myyntilaskujen toiminnoilla nopeasti ostoasiakirjoja myynnin edellyttämille puuttuville nimikemäärille.</span><span class="sxs-lookup"><span data-stu-id="4055f-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="4055f-105">Voit käyttää asiakirjan tyypin mukaan kahta eri toimintoa.</span><span class="sxs-lookup"><span data-stu-id="4055f-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="4055f-106">Toiminto</span><span class="sxs-lookup"><span data-stu-id="4055f-106">Function</span></span>|<span data-ttu-id="4055f-107">Description</span><span class="sxs-lookup"><span data-stu-id="4055f-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="4055f-108">**Luo ostotilaukset**</span><span class="sxs-lookup"><span data-stu-id="4055f-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="4055f-109">Tällä toiminnolla voi luoda myyntitilauksesta ostotilauksen kullekin myyntitilauksessa olevan nimikkeen toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="4055f-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="4055f-110">Voit muokata ostomäärää ennen ostotilausten luontia.</span><span class="sxs-lookup"><span data-stu-id="4055f-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="4055f-111">Vain myyntimääriä, jotka eivät ole käytettävissä, ehdotetaan.</span><span class="sxs-lookup"><span data-stu-id="4055f-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="4055f-112">**Luo ostolasku**</span><span class="sxs-lookup"><span data-stu-id="4055f-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="4055f-113">Tällä toiminnolla voi luoda myyntitilauksesta ja myyntilaskusta ostolaskun myyntiasiakirjasta valitun toimittajan kaikille tai valituille riveille.</span><span class="sxs-lookup"><span data-stu-id="4055f-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="4055f-114">Ehdotuksena on myynnin täysi määrä.</span><span class="sxs-lookup"><span data-stu-id="4055f-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="4055f-115">Vähintään yhden ostotilauksen luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="4055f-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="4055f-116">Voit luoda ostotilauksen kullekin myyntitilauksen nimikkeen määrälle, joka ei ole käytettävissä **Luo ostotilauksia** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="4055f-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span>

1. <span data-ttu-id="4055f-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4055f-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="4055f-118">Avaa myyntitilaus, johon haluat ostaa nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="4055f-118">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="4055f-119">Valitse **Luo ostotilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="4055f-119">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="4055f-120">Avautuvassa **Luo ostotilauksia** -ikkunassa näkyy rivi kullekin myyntitilauksen nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="4055f-120">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="4055f-121">Oletusarvoisesti näkyvissä on kokonaan saatavana olevien myyntimäärien rivit sekä niiden myyntimäärien rivit, jotka eivät ole saatavana (näkyvät harmaana).</span><span class="sxs-lookup"><span data-stu-id="4055f-121">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="4055f-122">Voit valita **Näytä ne, jotka eivät ole saatavilla** -toiminnon, jos haluat nähdä vain niiden myyntimäärien rivit, jotka eivät ole saatavilla.</span><span class="sxs-lookup"><span data-stu-id="4055f-122">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="4055f-123">**Ostojen määrä** -kenttä sisältää oletusarvoisesti myyntimäärän, joka ei ole saatavilla.</span><span class="sxs-lookup"><span data-stu-id="4055f-123">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="4055f-124">Voit ostaa jonkin muun määrän kuin ei saatavilla olevan myyntimäärän muokkaamalla **Ostettava määrä** -kentän arvon.</span><span class="sxs-lookup"><span data-stu-id="4055f-124">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="4055f-125">Voit muuttaa myös harmaana näkyvien rivien **Ostettava määrä** -kenttää, vaikka ne ilmaisevatkin kokonaan saatavilla olevat myyntimäärät.</span><span class="sxs-lookup"><span data-stu-id="4055f-125">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="4055f-126">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="4055f-126">Choose the **OK** button.</span></span>

    <span data-ttu-id="4055f-127">Kullekin myyntitilauksen nimikkeiden toimittajalle luodaan ostotilaus, mukaan lukien **Luo ostotilaukset** -ikkunassa mahdollisesti tehdyt määrän muutokset.</span><span class="sxs-lookup"><span data-stu-id="4055f-127">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="4055f-128">Siirry käsittelemään ostotilauksia esimerkiksi muokkaamalla tai lisäämällä ostotilausrivejä.</span><span class="sxs-lookup"><span data-stu-id="4055f-128">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="4055f-129">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="4055f-129">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="4055f-130">Ostolaskun luominen myyntitilauksesta tai myyntilaskusta</span><span class="sxs-lookup"><span data-stu-id="4055f-130">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="4055f-131">Voit luoda yhden ostolaskun yhdelle tai usealle myyntiasiakirjan riville valitsemalla ensin toimittajan, jolta nimike ostetaan, käyttämällä **Luo ostotilaus** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="4055f-131">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4055f-132">Tällä toiminnolla luodaan ostolasku täsmälleen valitussa myyntiasiakirjassa olevalle nimikemäärälle.</span><span class="sxs-lookup"><span data-stu-id="4055f-132">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="4055f-133">Voit muuttaa oston määrää muokkaamalla ostolasku sen jälkeen, kun se on luotu.</span><span class="sxs-lookup"><span data-stu-id="4055f-133">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="4055f-134">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4055f-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="4055f-135">Avaa myyntilasku, johon haluat ostaa nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="4055f-135">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="4055f-136">Valitse yksi tai useampi myyntilaskun rivi, joita haluat käyttää ostolaskuun.</span><span class="sxs-lookup"><span data-stu-id="4055f-136">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="4055f-137">Voit käyttää kaikkia myyntilaskurivejä valitsemalla kaikki rivit tai jättämällä kaikki rivit valitsematta.</span><span class="sxs-lookup"><span data-stu-id="4055f-137">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="4055f-138">Valitse **Luo ostolasku** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="4055f-138">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="4055f-139">Valitse joko **Kaikki rivit** tai **Valitut rivit** ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="4055f-139">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="4055f-140">Valitse avautuvasta toimittajaluettelosta toimittaja, jolta haluat ostaa kaikki nimikkeet, ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="4055f-140">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="4055f-141">Luotavassa ostolaskussa on yksi myyntilaskun rivi, useita myyntilaskun rivejä tai kaikki myyntilaskun rivit.</span><span class="sxs-lookup"><span data-stu-id="4055f-141">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="4055f-142">Siirry käsittelemään ostolasku, esimerkiksi lisäämällä ostolaskurivit tai muokkaamalla niitä.</span><span class="sxs-lookup"><span data-stu-id="4055f-142">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="4055f-143">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="4055f-143">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4055f-144">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4055f-144">See Also</span></span>
[<span data-ttu-id="4055f-145">Osto</span><span class="sxs-lookup"><span data-stu-id="4055f-145">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="4055f-146">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="4055f-146">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="4055f-147">Myynnin laskutus</span><span class="sxs-lookup"><span data-stu-id="4055f-147">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="4055f-148">Uusien toimittajien rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="4055f-148">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="4055f-149">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4055f-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

