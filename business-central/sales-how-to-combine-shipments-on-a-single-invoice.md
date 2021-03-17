---
title: Toimitusten yhdistäminen yhteen laskuun | Microsoft Docs
description: Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 802cb7e6d7b7bb56f994eaf2b45df9c9f9cb43d3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383073"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="7d664-103">Toimitusten yhdistäminen yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="7d664-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="7d664-104">Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="7d664-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

<span data-ttu-id="7d664-105">Ennen kuin koontilaskun voi luoda, samalle asiakkaalle täytyy kirjata useita myyntitoimituksia samassa valuutassa.</span><span class="sxs-lookup"><span data-stu-id="7d664-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="7d664-106">Toimintoa voi siis käyttää, kun vähintään kaksi myyntitilausta luodaan ja kirjataan toimitetuiksi, mutta ei laskutetuiksi.</span><span class="sxs-lookup"><span data-stu-id="7d664-106">In other words, you must have create two or more sales orders and post them as shipped, but not invoiced.</span></span> 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="7d664-107">Yhdistä manuaalisesti toimitukset yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="7d664-107">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="7d664-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d664-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7d664-109">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="7d664-109">Choose the **New** action.</span></span> <span data-ttu-id="7d664-110">Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="7d664-110">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="7d664-111">Valitse **Tilausasiakkaan nro**</span><span class="sxs-lookup"><span data-stu-id="7d664-111">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="7d664-112">asiakas, jolle toimitettujen nimikkeiden lasku lähetetään.</span><span class="sxs-lookup"><span data-stu-id="7d664-112">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="7d664-113">Valitse **Rivit**-pikavälilehdessä **Hae toimitusrivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="7d664-113">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="7d664-114">Valitse laskuun sisällytettävä toimitusrivi:</span><span class="sxs-lookup"><span data-stu-id="7d664-114">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="7d664-115">Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d664-115">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="7d664-116">Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d664-116">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="7d664-117">Voit käyttää Ctrl-näppäintä valitsemaan useita ei-perättäisiä rivejä.</span><span class="sxs-lookup"><span data-stu-id="7d664-117">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="7d664-118">Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa laskun rivit ja ajaa **Hae toimitusrivit** -toiminnon uudelleen.</span><span class="sxs-lookup"><span data-stu-id="7d664-118">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="7d664-119">Kirjaa lasku valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="7d664-119">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="7d664-120">Yhdistä automaattisesti toimitukset yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="7d664-120">To automatically combine shipments on a single invoice</span></span>  
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="7d664-121">valitsee vain ne myyntitilaukset, joissa on valittu **koontilasku**.</span><span class="sxs-lookup"><span data-stu-id="7d664-121">will select only sales orders where **Combine Shipments** is chosen.</span></span> 

1. <span data-ttu-id="7d664-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimitusten yhdistäminen** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d664-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="7d664-123">Eräajon pyynnön sivu aukeaa.</span><span class="sxs-lookup"><span data-stu-id="7d664-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="7d664-124">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="7d664-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="7d664-125">Valitse **Kirjaa laskut** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7d664-125">Choose the **Post Invoices** check box.</span></span>  
4. <span data-ttu-id="7d664-126">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="7d664-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7d664-127">Huomaa, että laskut on kirjattava manuaalisesti, jos eräajon **Kirjaa laskut** -valintaruutua ei ole valittu.</span><span class="sxs-lookup"><span data-stu-id="7d664-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="7d664-128">Avoimen myyntitilauksen poistaminen koontilaskun kirjauksen jälkeen</span><span class="sxs-lookup"><span data-stu-id="7d664-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="7d664-129">Kun koontilasku on tehty ja kirjattu, laskutetuille riveille luodaan kirjattu myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="7d664-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="7d664-130">Alkuperäisen puitemyyntitilauksen tai myyntitilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="7d664-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="7d664-131">Kun laskutat toimitukset näin, säilyvät tilaukset, joista toimitukset kirjattiin, vaikka ne olisi toimitettu ja laskutettu täysin.</span><span class="sxs-lookup"><span data-stu-id="7d664-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="7d664-132">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poista laskutetut myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d664-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="7d664-133">Määritä **Numero** -kenttään</span><span class="sxs-lookup"><span data-stu-id="7d664-133">Specify in the **No.**</span></span> <span data-ttu-id="7d664-134">, mitkä myyntitilaukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="7d664-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="7d664-135">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="7d664-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="7d664-136">Voit myös poistaa manuaalisesti yksittäiset myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="7d664-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="7d664-137">Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puitemyyntitilauksissa.</span><span class="sxs-lookup"><span data-stu-id="7d664-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d664-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7d664-138">See Also</span></span>  
[<span data-ttu-id="7d664-139">Myynti</span><span class="sxs-lookup"><span data-stu-id="7d664-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="7d664-140">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d664-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]