---
title: Ostotilauksen linkittäminen myyntitilaukseen suoratoimitusta varten | Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten ostotilaukseen linkitetty myyntitilaus luodaan. Näin toimitus voidaan tehdä suoraan toimittajalta asiakkaalle.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 09/06/2019
ms.author: sgroespe
ms.openlocfilehash: 9555aabe515757b71426ddca2f90b37e561f96e2
ms.sourcegitcommit: d3035c32bb79b51179540787b98579ac0c528cc4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/06/2019
ms.locfileid: "1985812"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="f1a81-103">Suoratoimitusten tekeminen</span><span class="sxs-lookup"><span data-stu-id="f1a81-103">Make Drop Shipments</span></span>
<span data-ttu-id="f1a81-104">Suoratoimitus on nimikkeen toimitus yhdeltä toimittajistasi suoraan yhdelle asiakkaistasi.</span><span class="sxs-lookup"><span data-stu-id="f1a81-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="f1a81-105">Kun myyntilaus on merkitty suoratoimitusta varten ja luot ostotilauksen, jossa asiakas määritetään **Toimitusasiakas**-kenttään, **Asiakkaan osoite**, voit linkittää kaksi asiakirjaa ja ohjata toimittajan lähettämään tilaus suoraan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="f1a81-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="f1a81-106">Myyntitilauksen luominen suoratoimitusta varten</span><span class="sxs-lookup"><span data-stu-id="f1a81-106">To create a sales order for drop shipment</span></span>
<span data-ttu-id="f1a81-107">Voit valmistella suoratoimituksen luomalla nimikkeelle normaalisti myyntitilauksen. Myyntirivillä tulee kuitenkin määrittää, että myynti vaatii suoratoimituksen.</span><span class="sxs-lookup"><span data-stu-id="f1a81-107">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="f1a81-108">Luo nimikkeelle myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="f1a81-108">Create a sales order for an item.</span></span> <span data-ttu-id="f1a81-109">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="f1a81-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="f1a81-110">Valitse suoratoimituksen myyntitilauksen rivillä **Suoratoimitus**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f1a81-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="f1a81-111">Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="f1a81-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="f1a81-112">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="f1a81-112">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="f1a81-113">Ostotilauksen luominen suoratoimitukselle</span><span class="sxs-lookup"><span data-stu-id="f1a81-113">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="f1a81-114">Myytävän nimikkeen suoratoimitus valmistellaan luomalla ostotilaus normaalisti lukuun ottamatta sitä, että ostotilauksessa on määritettävä, että nimikkeet on toimitettava asiakkaalle, ei ostotilauksen tekijälle.</span><span class="sxs-lookup"><span data-stu-id="f1a81-114">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="f1a81-115">Luo ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="f1a81-115">Create a purchase order.</span></span> <span data-ttu-id="f1a81-116">Älä täytä riveillä olevia kenttiä.</span><span class="sxs-lookup"><span data-stu-id="f1a81-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="f1a81-117">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="f1a81-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="f1a81-118">Valitse **Toimitusasiakas**-kentässä **Asiakkaan osoite**.</span><span class="sxs-lookup"><span data-stu-id="f1a81-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="f1a81-119">Valitse **Asiakas**-kenttään asiakas, jolle myydään.</span><span class="sxs-lookup"><span data-stu-id="f1a81-119">In the **Customer** field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="f1a81-120">Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f1a81-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="f1a81-121">Valitse **Myyntiluettelo**-sivulla myyntitilaus, jota valmisteltiin kohdassa [Myyntitilauksen luominen suoratoimitusta varten](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="f1a81-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="f1a81-122">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="f1a81-122">Choose the **OK** button.</span></span>

<span data-ttu-id="f1a81-123">Myyntitilauksen rivin tiedot lisätään ostotilauksen riville/riveille.</span><span class="sxs-lookup"><span data-stu-id="f1a81-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="f1a81-124">Voit ohjeistaa toimittajaa toimittamaan nimikkeet asiakkaalle esimerkiksi lähettämällä ostotilauksen PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="f1a81-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="f1a81-125">Myyntitilauksesta linkitetyn ostotilauksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="f1a81-125">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="f1a81-126">Valitse suoratoimituksen myyntitilauksen rivi ja valitse sitten **Tilaa**-toiminto. Valitse **Suoratoimitus**-toiminto ja valitse sitten **Ostotilaus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f1a81-126">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="f1a81-127">Kirjaa suoratoimitus</span><span class="sxs-lookup"><span data-stu-id="f1a81-127">To post a drop shipment</span></span>
<span data-ttu-id="f1a81-128">Kun toimittaja toimittaa nimikkeet, voit kirjata myyntitilauksen toimitetuksi.</span><span class="sxs-lookup"><span data-stu-id="f1a81-128">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="f1a81-129">Voit kirjata myös ostotilauksen, mutta vain **Vastaanotto**-vaihtoehdon kanssa niin kauan, kunnes myyntitilaus on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="f1a81-129">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="f1a81-130">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f1a81-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1a81-131">Avaa kohdassa [Myyntitilauksen luominen suoratoimitukselle]() luomasi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="f1a81-131">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="f1a81-132">Määritä **Toimitettava määrä** -kentässä toimitettava tilausmäärä, joka voi olla koko tai osittainen tilausmäärä.</span><span class="sxs-lookup"><span data-stu-id="f1a81-132">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="f1a81-133">Valitse **Kirjaa**- tai **Kirjaa ja lähetä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f1a81-133">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="f1a81-134">Valitse **Toimitus**-vaihtoehto, kun haluat laskuttaa myöhemmin, tai **Toimitus ja lasku** -vaihtoehto, kun haluat laskuttaa heti.</span><span class="sxs-lookup"><span data-stu-id="f1a81-134">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1a81-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f1a81-135">See Also</span></span>
[<span data-ttu-id="f1a81-136">Erikoistilausten luominen</span><span class="sxs-lookup"><span data-stu-id="f1a81-136">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="f1a81-137">Nimikkeiden ostaminen myyntiin</span><span class="sxs-lookup"><span data-stu-id="f1a81-137">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="f1a81-138">Tuotteiden myyminen</span><span class="sxs-lookup"><span data-stu-id="f1a81-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="f1a81-139">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="f1a81-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="f1a81-140">Myynti</span><span class="sxs-lookup"><span data-stu-id="f1a81-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="f1a81-141">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="f1a81-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f1a81-142">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f1a81-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
