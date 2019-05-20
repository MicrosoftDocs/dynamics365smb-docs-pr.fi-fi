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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7a87023445ea10aa19cc0cc4f60d76ce4cf3e365
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251218"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="1086d-103">Suoratoimitusten tekeminen</span><span class="sxs-lookup"><span data-stu-id="1086d-103">Make Drop Shipments</span></span>
<span data-ttu-id="1086d-104">Suoratoimitus on nimikkeen toimitus yhdeltä toimittajistasi suoraan yhdelle asiakkaistasi.</span><span class="sxs-lookup"><span data-stu-id="1086d-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="1086d-105">Kun myyntitilaus merkitään suoratoimitusta varten, ja luot ostotilauksen, jossa asiakas määritetään **Tilausasiakkaan nro**</span><span class="sxs-lookup"><span data-stu-id="1086d-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="1086d-106">-kentässä, voit linkittää nämä kaksi asiakirjaa ja ohjeistaa toimittajaa toimittamaan nimikkeet suoraan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="1086d-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="1086d-107">Myyntitilauksen luominen suoratoimitusta varten</span><span class="sxs-lookup"><span data-stu-id="1086d-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="1086d-108">Voit valmistella suoratoimituksen luomalla nimikkeelle normaalisti myyntitilauksen. Myyntirivillä tulee kuitenkin määrittää, että myynti vaatii suoratoimituksen.</span><span class="sxs-lookup"><span data-stu-id="1086d-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="1086d-109">Luo nimikkeelle myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="1086d-109">Create a sales order for an item.</span></span> <span data-ttu-id="1086d-110">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="1086d-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="1086d-111">Valitse suoratoimituksen myyntitilauksen rivillä **Suoratoimitus**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1086d-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="1086d-112">Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="1086d-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="1086d-113">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="1086d-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="1086d-114">Ostotilauksen luominen suoratoimitukselle</span><span class="sxs-lookup"><span data-stu-id="1086d-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="1086d-115">Myytävän nimikkeen suoratoimitus valmistellaan luomalla ostotilaus normaalisti lukuun ottamatta sitä, että ostotilauksessa on määritettävä, että nimikkeet on toimitettava asiakkaalle, ei ostotilauksen tekijälle.</span><span class="sxs-lookup"><span data-stu-id="1086d-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="1086d-116">Luo ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="1086d-116">Create a purchase order.</span></span> <span data-ttu-id="1086d-117">Älä täytä riveillä olevia kenttiä.</span><span class="sxs-lookup"><span data-stu-id="1086d-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="1086d-118">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="1086d-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="1086d-119">Valitse **Tilausasiakkaan nro**</span><span class="sxs-lookup"><span data-stu-id="1086d-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="1086d-120">-kenttään asiakas, jolle myydään.</span><span class="sxs-lookup"><span data-stu-id="1086d-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="1086d-121">Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1086d-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="1086d-122">Valitse **Myyntiluettelo**-sivulla myyntitilaus, jota valmisteltiin kohdassa [Myyntitilauksen luominen suoratoimitusta varten](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="1086d-122">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="1086d-123">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="1086d-123">Choose the **OK** button.</span></span>

<span data-ttu-id="1086d-124">Myyntitilauksen rivin tiedot lisätään ostotilauksen riville/riveille.</span><span class="sxs-lookup"><span data-stu-id="1086d-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="1086d-125">Voit ohjeistaa toimittajaa toimittamaan nimikkeet asiakkaalle esimerkiksi lähettämällä ostotilauksen PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="1086d-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="1086d-126">Myyntitilauksesta linkitetyn ostotilauksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="1086d-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="1086d-127">Valitse suoratoimituksen myyntitilauksen rivi ja valitse sitten **Tilaa**-toiminto. Valitse **Suoratoimitus**-toiminto ja valitse sitten **Ostotilaus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="1086d-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="1086d-128">Kirjaa suoratoimitus</span><span class="sxs-lookup"><span data-stu-id="1086d-128">To post a drop shipment</span></span>
<span data-ttu-id="1086d-129">Kun toimittaja toimittaa nimikkeet, voit kirjata myyntitilauksen toimitetuksi.</span><span class="sxs-lookup"><span data-stu-id="1086d-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="1086d-130">Voit kirjata myös ostotilauksen, mutta vain **Vastaanotto**-vaihtoehdon kanssa niin kauan, kunnes myyntitilaus on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="1086d-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="1086d-131">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1086d-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="1086d-132">Avaa kohdassa [Myyntitilauksen luominen suoratoimitukselle]() luomasi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="1086d-132">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="1086d-133">Määritä **Toimitettava määrä** -kentässä toimitettava tilausmäärä, joka voi olla koko tai osittainen tilausmäärä.</span><span class="sxs-lookup"><span data-stu-id="1086d-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="1086d-134">Valitse **Kirjaa**- tai **Kirjaa ja lähetä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1086d-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="1086d-135">Valitse **Toimitus**-vaihtoehto, kun haluat laskuttaa myöhemmin, tai **Toimitus ja lasku** -vaihtoehto, kun haluat laskuttaa heti.</span><span class="sxs-lookup"><span data-stu-id="1086d-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="1086d-136">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1086d-136">See Also</span></span>
[<span data-ttu-id="1086d-137">Erikoistilausten luominen</span><span class="sxs-lookup"><span data-stu-id="1086d-137">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="1086d-138">Nimikkeiden ostaminen myyntiin</span><span class="sxs-lookup"><span data-stu-id="1086d-138">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="1086d-139">Tuotteiden myyminen</span><span class="sxs-lookup"><span data-stu-id="1086d-139">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="1086d-140">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="1086d-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="1086d-141">Myynti</span><span class="sxs-lookup"><span data-stu-id="1086d-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="1086d-142">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="1086d-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="1086d-143">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1086d-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
