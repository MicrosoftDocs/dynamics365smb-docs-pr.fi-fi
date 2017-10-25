---
title: Ostotilaukseen linkitetyn myyntitilauksen luominen suoratoimitusta varten | Microsoft Docs
description: "Tässä artikkelissa kerrotaan, miten ostotilaukseen linkitetty myyntitilaus luodaan. Näin toimitus voidaan tehdä suoraan toimittajalta asiakkaalle."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 990867cb428f860b1001177738d1a027f72485bc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="204e5-103">Toimintaohje: Suoratoimitusten tekeminen</span><span class="sxs-lookup"><span data-stu-id="204e5-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="204e5-104">Suoratoimitus on nimikkeen toimitus yhdeltä toimittajistasi suoraan yhdelle asiakkaistasi.</span><span class="sxs-lookup"><span data-stu-id="204e5-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="204e5-105">Kun myyntitilaus merkitään suoratoimitusta varten, ja luot ostotilauksen, jossa asiakas määritetään **Tilausasiakkaan nro**</span><span class="sxs-lookup"><span data-stu-id="204e5-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="204e5-106">-kentässä, voit linkittää nämä kaksi asiakirjaa ja ohjeistaa toimittajaa toimittamaan nimikkeet suoraan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="204e5-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="204e5-107">Myyntitilauksen luominen suoratoimitusta varten</span><span class="sxs-lookup"><span data-stu-id="204e5-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="204e5-108">Voit valmistella suoratoimituksen luomalla nimikkeelle normaalisti myyntitilauksen. Myyntirivillä tulee kuitenkin määrittää, että myynti vaatii suoratoimituksen.</span><span class="sxs-lookup"><span data-stu-id="204e5-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="204e5-109">Luo nimikkeelle myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="204e5-109">Create a sales order for an item.</span></span> <span data-ttu-id="204e5-110">Lisätietoja on kohdassa [Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="204e5-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="204e5-111">Valitse suoratoimituksen myyntitilauksen rivillä **Suoratoimitus**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="204e5-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="204e5-112">Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="204e5-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="204e5-113">Lisätietoja on ohjeaiheessa [Käyttäjän mukautus](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="204e5-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="204e5-114">Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**.</span><span class="sxs-lookup"><span data-stu-id="204e5-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="204e5-115">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="204e5-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="204e5-116">Ostotilauksen luominen suoratoimitukselle</span><span class="sxs-lookup"><span data-stu-id="204e5-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="204e5-117">Myytävän nimikkeen suoratoimitus valmistellaan luomalla ostotilaus normaalisti lukuun ottamatta sitä, että ostotilauksessa on määritettävä, että nimikkeet on toimitettava asiakkaalle, ei ostotilauksen tekijälle.</span><span class="sxs-lookup"><span data-stu-id="204e5-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="204e5-118">Luo ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="204e5-118">Create a purchase order.</span></span> <span data-ttu-id="204e5-119">Älä täytä riveillä olevia kenttiä.</span><span class="sxs-lookup"><span data-stu-id="204e5-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="204e5-120">Lisätietoja on kohdassa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="204e5-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="204e5-121">Valitse **Tilausasiakkaan nro**</span><span class="sxs-lookup"><span data-stu-id="204e5-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="204e5-122">-kenttään asiakas, jolle myydään.</span><span class="sxs-lookup"><span data-stu-id="204e5-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="204e5-123">Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="204e5-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="204e5-124">Valitse **Myyntiluettelo**-ikkunassa myyntitilaus, jota valmisteltiin "Myyntitilauksen luominen suoratoimitusta varten" -osassa.</span><span class="sxs-lookup"><span data-stu-id="204e5-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="204e5-125">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="204e5-125">Choose the **OK** button.</span></span>

<span data-ttu-id="204e5-126">Myyntitilauksen rivin tiedot lisätään ostotilauksen riville/riveille.</span><span class="sxs-lookup"><span data-stu-id="204e5-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="204e5-127">Voit ohjeistaa toimittajaa toimittamaan nimikkeet asiakkaalle esimerkiksi lähettämällä ostotilauksen PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="204e5-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="204e5-128">Myyntitilauksesta linkitetyn ostotilauksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="204e5-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="204e5-129">Valitse suoratoimituksen myyntitilauksen rivi ja valitse sitten **Tilaa**-toiminto. Valitse **Suoratoimitus**-toiminto ja valitse sitten **Ostotilaus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="204e5-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="204e5-130">Kirjaa suoratoimitus</span><span class="sxs-lookup"><span data-stu-id="204e5-130">To post a drop shipment</span></span>
<span data-ttu-id="204e5-131">Kun toimittaja toimittaa nimikkeet, voit kirjata myyntitilauksen toimitetuksi.</span><span class="sxs-lookup"><span data-stu-id="204e5-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="204e5-132">Voit kirjata myös ostotilauksen, mutta vain **Vastaanotto**-vaihtoehdon kanssa niin kauan, kunnes myyntitilaus on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="204e5-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="204e5-133">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="204e5-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="204e5-134">Avaa "Myyntitilauksen luominen suoratoimitukselle" -osassa luomasi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="204e5-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="204e5-135">Määritä **Toimitettava määrä** -kentässä toimitettava tilausmäärä, joka voi olla koko tai osittainen tilausmäärä.</span><span class="sxs-lookup"><span data-stu-id="204e5-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="204e5-136">Valitse **Kirjaa**- tai **Kirjaa ja lähetä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="204e5-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="204e5-137">Valitse **Toimitus**-vaihtoehto, kun haluat laskuttaa myöhemmin, tai **Toimitus ja lasku** -vaihtoehto, kun haluat laskuttaa heti.</span><span class="sxs-lookup"><span data-stu-id="204e5-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="204e5-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="204e5-138">See Also</span></span>
<span data-ttu-id="204e5-139">[Toimintaohje: Erikoistilausten luominen](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="204e5-139">[How to: Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="204e5-140">Toimintaohje: Tuotteiden myyminen</span><span class="sxs-lookup"><span data-stu-id="204e5-140">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="204e5-141">Toimintaohje: Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="204e5-141">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="204e5-142">Myynti</span><span class="sxs-lookup"><span data-stu-id="204e5-142">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="204e5-143">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="204e5-143">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="204e5-144">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="204e5-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

