---
title: "Toimitusten yhdistäminen yhteen laskuun | Microsoft Docs"
description: "Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c9f2464014f2078f2a86f2e7d8a72873fa4015a8
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="85ebe-103">Toimitusten yhdistäminen yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="85ebe-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="85ebe-104">Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="85ebe-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="85ebe-105">Ennen kuin koontilaskun voi luoda, samalle asiakkaalle täytyy kirjata useita myyntitoimituksia samassa valuutassa.</span><span class="sxs-lookup"><span data-stu-id="85ebe-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="85ebe-106">Toimintoa voi siis käyttää, kun vähintään kaksi myyntitilausta on täytetty ja kirjattu toimitetuiksi (muttei laskutetuiksi).</span><span class="sxs-lookup"><span data-stu-id="85ebe-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="85ebe-107">**Asiakaskortin** **Toimitus**-pikavälilehden **Tee koontilasku** -valintaruutu on valittava, jotta palautustoimituksia voidaan yhdistää.</span><span class="sxs-lookup"><span data-stu-id="85ebe-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="85ebe-108">Yhdistä manuaalisesti toimitukset yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="85ebe-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="85ebe-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="85ebe-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="85ebe-110">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="85ebe-110">Choose the **New** action.</span></span> <span data-ttu-id="85ebe-111">Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="85ebe-111">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="85ebe-112">Valitse **Tilausasiakkaan nro**</span><span class="sxs-lookup"><span data-stu-id="85ebe-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="85ebe-113">asiakas, jolle toimitettujen nimikkeiden lasku lähetetään.</span><span class="sxs-lookup"><span data-stu-id="85ebe-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="85ebe-114">Valitse **Rivit**-pikavälilehdessä **Hae toimitusrivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="85ebe-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="85ebe-115">Valitse laskuun sisällytettävä toimitusrivi:</span><span class="sxs-lookup"><span data-stu-id="85ebe-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="85ebe-116">Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="85ebe-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="85ebe-117">Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="85ebe-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="85ebe-118">Voit käyttää Ctrl-näppäintä valitsemaan useita ei-perättäisiä rivejä.</span><span class="sxs-lookup"><span data-stu-id="85ebe-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="85ebe-119">Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa laskun rivit ja ajaa **Hae toimitusrivit** -toiminnon uudelleen.</span><span class="sxs-lookup"><span data-stu-id="85ebe-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="85ebe-120">Kirjaa lasku valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="85ebe-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="85ebe-121">Yhdistä automaattisesti toimitukset yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="85ebe-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="85ebe-122">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tee koontilasku** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="85ebe-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="85ebe-123">Eräajon pyynnön ikkuna aukeaa.</span><span class="sxs-lookup"><span data-stu-id="85ebe-123">The batch job request window opens.</span></span>  
2. <span data-ttu-id="85ebe-124">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="85ebe-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="85ebe-125">Valitse **Kirjaa laskut** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="85ebe-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="85ebe-126">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="85ebe-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="85ebe-127">Huomaa, että laskut on kirjattava manuaalisesti, jos eräajon **Kirjaa laskut** -valintaruutua ei ole valittu.</span><span class="sxs-lookup"><span data-stu-id="85ebe-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="85ebe-128">Avoimen myyntitilauksen poistaminen koontilaskun kirjauksen jälkeen</span><span class="sxs-lookup"><span data-stu-id="85ebe-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="85ebe-129">Kun koontilasku on tehty ja kirjattu, laskutetuille riveille luodaan kirjattu myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="85ebe-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="85ebe-130">Alkuperäisen puitemyyntitilauksen tai myyntitilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="85ebe-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="85ebe-131">Kun laskutat toimitukset näin, säilyvät tilaukset, joista toimitukset kirjattiin, vaikka ne olisi toimitettu ja laskutettu täysin.</span><span class="sxs-lookup"><span data-stu-id="85ebe-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="85ebe-132">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista laskutetut myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="85ebe-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="85ebe-133">Määritä **Numero** -kenttään</span><span class="sxs-lookup"><span data-stu-id="85ebe-133">Specify in the **No.**</span></span> <span data-ttu-id="85ebe-134">, mitkä myyntitilaukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="85ebe-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="85ebe-135">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="85ebe-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="85ebe-136">Voit myös poistaa manuaalisesti yksittäiset myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="85ebe-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="85ebe-137">Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puitemyyntitilauksissa.</span><span class="sxs-lookup"><span data-stu-id="85ebe-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="85ebe-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="85ebe-138">See Also</span></span>  
[<span data-ttu-id="85ebe-139">Myynti</span><span class="sxs-lookup"><span data-stu-id="85ebe-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="85ebe-140">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="85ebe-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

