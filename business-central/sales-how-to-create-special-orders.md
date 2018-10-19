---
title: Erikoistilausten luominen | Microsoft Docs
description: "Erikoistilauksen voi luoda tietylle luettelonimikkeelle, joka toimitetaan tietylle asiakkaalle. Toimittajasi toimittaa nimikkeen fyysiseen varastoosi, ja sen jälkeen voit toimittaa nimikkeen asiakkaallesi joko erikseen tai yhdessä muiden, toisen tilauksen nimikkeiden kanssa."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 36c68048c384f4ccfef6c811ac288b306351ce2f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="create-special-orders"></a><span data-ttu-id="8b329-104">Erikoistilausten luominen</span><span class="sxs-lookup"><span data-stu-id="8b329-104">Create Special Orders</span></span>
<span data-ttu-id="8b329-105">Erikoistilauksen voi luoda tietylle luettelonimikkeelle, joka toimitetaan tietylle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="8b329-105">You can create a special order for a specific catalog item to be shipped to a specific customer.</span></span> <span data-ttu-id="8b329-106">Toimittajasi toimittaa nimikkeen fyysiseen varastoosi, ja sen jälkeen voit toimittaa nimikkeen asiakkaallesi joko erikseen tai yhdessä muiden, toisen tilauksen nimikkeiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="8b329-106">Your vendor ships the item to your warehouse and you can then ship the item on to your customer either independently or together with other items on another order.</span></span>  

<span data-ttu-id="8b329-107">Erikoistilaukset ilmaisevat, että osto- ja myyntitilaus on linkitetty toisiinsa. Näin varmistetaan, että tietty luettelonimike poimitaan ja toimitetaan kyseiselle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="8b329-107">Special orders imply that the purchase and sales order are linked to ensure that the specific catalog item is picked and delivered to the customer.</span></span>  

<span data-ttu-id="8b329-108">Ennen kuin tätä ominaisuutta voi käyttää, tilaukselle tarpeelliset asiakas-, myyjä- ja nimikekortit tulee määrittää.</span><span class="sxs-lookup"><span data-stu-id="8b329-108">Before you can use this feature, you must first set up the customer, vendor, and item cards necessary for the order.</span></span>  

## <a name="to-create-a-special-order"></a><span data-ttu-id="8b329-109">Erikoistilausten luominen</span><span class="sxs-lookup"><span data-stu-id="8b329-109">To create a special order</span></span>  
1.  <span data-ttu-id="8b329-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaus** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8b329-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Order**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8b329-111">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="8b329-111">Choose the **New** action.</span></span> <span data-ttu-id="8b329-112">Luo nimikkeelle  myyntitilaus ja täytä se.</span><span class="sxs-lookup"><span data-stu-id="8b329-112">Create and fill in a  sales order for the item.</span></span> <span data-ttu-id="8b329-113">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="8b329-113">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
3.  <span data-ttu-id="8b329-114">Täytä myyntirivi **Rivit**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="8b329-114">On the **Lines** FastTab, fill in the sales line.</span></span> <span data-ttu-id="8b329-115">Valitse **Ostamisen koodi** -kentässä ostokoodi, jonka **Erikoistilaus**-kenttä on valittuna.</span><span class="sxs-lookup"><span data-stu-id="8b329-115">In the **Purchasing Code** field, select a purchasing code that has the **Special Order** field selected.</span></span>

    <span data-ttu-id="8b329-116">Luo seuraavaksi ostotilaus hankintalistasta.</span><span class="sxs-lookup"><span data-stu-id="8b329-116">You must now create a purchase order from a requisition worksheet.</span></span>  
4. <span data-ttu-id="8b329-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hankintalista** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8b329-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requisition Worksheet**, and then choose the related link.</span></span>  
5. <span data-ttu-id="8b329-118">Valitse ensin **Erikoistilaus**-toiminto ja sitten **Hae myyntitilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="8b329-118">Choose the **Special Order** action, and then choose the **Get Sales Orders** action.</span></span>  
6.  <span data-ttu-id="8b329-119">Näytä **Hae myyntitilaukset** -ikkunassa tulokset, joissa **Asiakirjan nro.** on myyntitilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="8b329-119">In the **Get Sales Orders** window, show results where the **Document No.** is the sales order number.</span></span> <span data-ttu-id="8b329-120">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="8b329-120">Choose the **OK** button.</span></span> <span data-ttu-id="8b329-121">Ohjelma luo nimikkeelle hankintalistan rivin.</span><span class="sxs-lookup"><span data-stu-id="8b329-121">A requisition worksheet line is created for the item.</span></span>  
7.  <span data-ttu-id="8b329-122">Valitse hankintalistarivin  **Toimenpideviesti**-kentässä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8b329-122">On the requisition worksheet line, in the **Action Message** field, select **New**.</span></span>  
8.  <span data-ttu-id="8b329-123">Valitse **Hankintalista**-ikkunassa **Toteuta toimenpideviesti** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="8b329-123">In the **Req. Worksheet** window, choose the **Carry Out Action Message** action.</span></span> <span data-ttu-id="8b329-124">**Toteuta toim.pideviesti - hank** -ikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="8b329-124">The **Carry Out Action Msg. - Req.** window opens.</span></span> <span data-ttu-id="8b329-125">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="8b329-125">Choose the **OK** button.</span></span>  

    <span data-ttu-id="8b329-126">Näyttöön tulee ikkuna, jossa ilmoitetaan, että ostotilaukset on luotu.</span><span class="sxs-lookup"><span data-stu-id="8b329-126">A message appears telling you that the purchase orders have been created.</span></span> <span data-ttu-id="8b329-127">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="8b329-127">Choost the **OK** button.</span></span>  

<span data-ttu-id="8b329-128">Suunnittelujärjestelmä säilyttää myyntitilaukselle erikoistilauksena luodun ostotilauksen, koska se tasapainottaa kysyntää ja tarjontaa.</span><span class="sxs-lookup"><span data-stu-id="8b329-128">A purchase order created as a special order for a sales order is respected by the planning system as it balances demand and supply.</span></span> <span data-ttu-id="8b329-129">Ostotilaus (tarjonta) pysyy linkitettynä myyntitilaukseen (kysyntään), vaikka ostotilauksella voisi toimittaa toisen aiemman kysynnän.</span><span class="sxs-lookup"><span data-stu-id="8b329-129">That is, the purchase order (supply) remains linked to the sales order (demand), even if that purchase order could supply another earlier demand.</span></span> <span data-ttu-id="8b329-130">Lisätietoja on kohdassa [Rakennetiedot: Uusintatilauskäytännöt](design-details-reservation-order-tracking-and-action-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="8b329-130">For more information, see [Design Details: Reordering Policies](design-details-reservation-order-tracking-and-action-messaging.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8b329-131">Et voi käyttää erikoistilauksen toimintoja, jos nimike on jo varattu.</span><span class="sxs-lookup"><span data-stu-id="8b329-131">You cannot use the special order functionality if the item is already reserved.</span></span> <span data-ttu-id="8b329-132">Tämän varmista erikoistilauksina myydyille nimikkeille, että **Varaa**-kenttää nimikkeen kortissa ei ole määritetty arvoon **Aina**.</span><span class="sxs-lookup"><span data-stu-id="8b329-132">Therefore, for items that are sold on special orders, make sure the **Reserve** field on the item card is not set to **Always**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8b329-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8b329-133">See Also</span></span>  
[<span data-ttu-id="8b329-134">Luettelonimikkeiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="8b329-134">Work with Catalog Items</span></span>](inventory-how-work-nonstock-items.md)  
[<span data-ttu-id="8b329-135">Myynti</span><span class="sxs-lookup"><span data-stu-id="8b329-135">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="8b329-136">[Suoratoimitusten tekeminen](sales-how-drop-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="8b329-136">[Make Drop Shipments](sales-how-drop-shipment.md) </span></span>  
[<span data-ttu-id="8b329-137">Rakennetiedot: uusintatilauskäytännöt</span><span class="sxs-lookup"><span data-stu-id="8b329-137">Design Details: Reordering Policies</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="8b329-138">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8b329-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

