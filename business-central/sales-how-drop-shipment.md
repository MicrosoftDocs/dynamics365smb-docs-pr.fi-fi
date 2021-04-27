---
title: Ostotilauksen linkittäminen myyntitilaukseen suoratoimitusta varten | Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten ostotilaukseen linkitetty myyntitilaus luodaan. Näin toimitus voidaan tehdä suoraan toimittajalta asiakkaalle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: beb78a3526b95af228ab313b67174633902e7bd7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778820"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="3ae95-103">Suoratoimitusten tekeminen</span><span class="sxs-lookup"><span data-stu-id="3ae95-103">Make Drop Shipments</span></span>

<span data-ttu-id="3ae95-104">Suoratoimitus on nimikkeen toimitus yhdeltä toimittajistasi suoraan yhdelle asiakkaistasi.</span><span class="sxs-lookup"><span data-stu-id="3ae95-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="3ae95-105">Kun myyntilaus on merkitty suoratoimitusta varten ja luot ostotilauksen, jossa asiakas määritetään **Toimitusasiakas**-kenttään, **Asiakkaan osoite**, voit linkittää kaksi asiakirjaa ja ohjata toimittajan lähettämään tilaus suoraan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="3ae95-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="3ae95-106">Myyntitilauksen luominen suoratoimitusta varten</span><span class="sxs-lookup"><span data-stu-id="3ae95-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="3ae95-107">Voit valmistella suoratoimituksen luomalla nimikkeelle myyntitilauksen. Myyntirivillä tulee määrittää, että myynti vaatii suoratoimituksen.</span><span class="sxs-lookup"><span data-stu-id="3ae95-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="3ae95-108">Luo nimikkeelle myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="3ae95-108">Create a sales order for an item.</span></span> <span data-ttu-id="3ae95-109">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="3ae95-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="3ae95-110">Valitse suoratoimituksen myyntitilauksen rivillä **Suoratoimitus**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="3ae95-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="3ae95-111">Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="3ae95-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="3ae95-112">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="3ae95-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="3ae95-113">Ostotilauksen luominen suoratoimitukselle</span><span class="sxs-lookup"><span data-stu-id="3ae95-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="3ae95-114">Voit valmistella suoran toimituksen määrittämällä ostotilaukseen, että se täytyy toimittaa asiakkaalle, ei itsellesi.</span><span class="sxs-lookup"><span data-stu-id="3ae95-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="3ae95-115">Luo ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="3ae95-115">Create a purchase order.</span></span> <span data-ttu-id="3ae95-116">Älä täytä riveillä olevia kenttiä.</span><span class="sxs-lookup"><span data-stu-id="3ae95-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="3ae95-117">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="3ae95-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="3ae95-118">Valitse **Toimitusasiakas**-kentässä **Asiakkaan osoite**.</span><span class="sxs-lookup"><span data-stu-id="3ae95-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="3ae95-119">Valitse **Asiakas**-kenttään asiakas, jolle myydään.</span><span class="sxs-lookup"><span data-stu-id="3ae95-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="3ae95-120">Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3ae95-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="3ae95-121">Valitse **Myyntiluettelo**-sivulla myyntitilaus, jota valmisteltiin kohdassa [Myyntitilauksen luominen suoratoimitusta varten](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="3ae95-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="3ae95-122">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="3ae95-122">Choose the **OK** button.</span></span>

<span data-ttu-id="3ae95-123">Myyntitilauksen rivin tiedot lisätään ostotilauksen riville/riveille.</span><span class="sxs-lookup"><span data-stu-id="3ae95-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="3ae95-124">Voit ohjeistaa toimittajaa toimittamaan nimikkeet asiakkaalle esimerkiksi lähettämällä ostotilauksen PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="3ae95-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="3ae95-125">Useiden ostotilausten luominen suoratoimituksille</span><span class="sxs-lookup"><span data-stu-id="3ae95-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="3ae95-126">Voit myös käyttää hankintatyökirjaa luodaksesi ostotilauksen toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="3ae95-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="3ae95-127">Hankintatyökirjan käyttämisen etuna on se, että se voi luoda ostotilauksia kaikille avoimille suoratoimituksille, joten sinun ei tarvitse luoda jokaista erikseen.</span><span class="sxs-lookup"><span data-stu-id="3ae95-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="3ae95-128">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hankintalistat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3ae95-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="3ae95-129">Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3ae95-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="3ae95-130">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="3ae95-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="3ae95-131">Tarkista ostotilausrivit ja valitse **Toimittajan nro** -kentässä toimittaja, joka toimittaa vaadittuja tavaroita.</span><span class="sxs-lookup"><span data-stu-id="3ae95-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="3ae95-132">Valitse **Toteuta toimenpideviesti** -toiminto, jos haluat muuntaa tarkistetut rivit ostotilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="3ae95-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="3ae95-133">Myyntitilauksesta linkitetyn ostotilauksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="3ae95-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="3ae95-134">Valitse suoratoimituksen myyntitilauksen rivi ja valitse sitten **Tilaa**-toiminto. Valitse **Suoratoimitus**-toiminto ja valitse sitten **Ostotilaus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="3ae95-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="3ae95-135">Kirjaa suoratoimitus</span><span class="sxs-lookup"><span data-stu-id="3ae95-135">To post a drop shipment</span></span>

<span data-ttu-id="3ae95-136">Kun toimittaja toimittaa nimikkeet, voit kirjata myyntitilauksen toimitetuksi.</span><span class="sxs-lookup"><span data-stu-id="3ae95-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="3ae95-137">Voit kirjata myös ostotilauksen, mutta vain **Vastaanotto**-vaihtoehdon kanssa niin kauan, kunnes myyntitilaus on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="3ae95-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="3ae95-138">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3ae95-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="3ae95-139">Avaa myyntitilaus, joka luotiin kohdassa [Myyntitilauksen luominen suoratoimitukselle](#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="3ae95-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="3ae95-140">Määritä **Toimitettava määrä** -kentässä toimitettava tilausmäärä, joka voi olla koko tai osittainen tilausmäärä.</span><span class="sxs-lookup"><span data-stu-id="3ae95-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="3ae95-141">Valitse **Kirjaa**- tai **Kirjaa ja lähetä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3ae95-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="3ae95-142">Valitse **Toimitus**-vaihtoehto, kun haluat laskuttaa myöhemmin, tai **Toimitus ja lasku** -vaihtoehto, kun haluat laskuttaa heti.</span><span class="sxs-lookup"><span data-stu-id="3ae95-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ae95-143">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3ae95-143">See Also</span></span>

[<span data-ttu-id="3ae95-144">Erikoistilausten luominen</span><span class="sxs-lookup"><span data-stu-id="3ae95-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="3ae95-145">Nimikkeiden ostaminen myyntiin</span><span class="sxs-lookup"><span data-stu-id="3ae95-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="3ae95-146">Tuotteiden myyminen</span><span class="sxs-lookup"><span data-stu-id="3ae95-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="3ae95-147">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="3ae95-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="3ae95-148">Myynti</span><span class="sxs-lookup"><span data-stu-id="3ae95-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="3ae95-149">Varasto</span><span class="sxs-lookup"><span data-stu-id="3ae95-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="3ae95-150">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3ae95-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]