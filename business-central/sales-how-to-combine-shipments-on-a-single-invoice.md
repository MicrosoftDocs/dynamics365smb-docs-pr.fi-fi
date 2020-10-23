---
title: Toimitusten yhdistäminen yhteen laskuun | Microsoft Docs
description: Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 19b6cb69d33d76d4263ad75a666eba14deaeeae8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925945"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="6ddc8-103">Toimitusten yhdistäminen yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="6ddc8-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="6ddc8-104">Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

<span data-ttu-id="6ddc8-105">Ennen kuin koontilaskun voi luoda, samalle asiakkaalle täytyy kirjata useita myyntitoimituksia samassa valuutassa.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="6ddc8-106">Toimintoa voi siis käyttää, kun vähintään kaksi myyntitilausta luodaan ja kirjataan toimitetuiksi, mutta ei laskutetuiksi.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-106">In other words, you must have create two or more sales orders and post them as shipped, but not invoiced.</span></span> 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="6ddc8-107">Yhdistä manuaalisesti toimitukset yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="6ddc8-107">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="6ddc8-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6ddc8-109">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-109">Choose the **New** action.</span></span> <span data-ttu-id="6ddc8-110">Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="6ddc8-110">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="6ddc8-111">Valitse **Tilausasiakkaan nro**</span><span class="sxs-lookup"><span data-stu-id="6ddc8-111">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="6ddc8-112">asiakas, jolle toimitettujen nimikkeiden lasku lähetetään.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-112">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="6ddc8-113">Valitse **Rivit**-pikavälilehdessä **Hae toimitusrivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-113">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="6ddc8-114">Valitse laskuun sisällytettävä toimitusrivi:</span><span class="sxs-lookup"><span data-stu-id="6ddc8-114">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="6ddc8-115">Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-115">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="6ddc8-116">Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-116">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="6ddc8-117">Voit käyttää Ctrl-näppäintä valitsemaan useita ei-perättäisiä rivejä.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-117">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="6ddc8-118">Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa laskun rivit ja ajaa **Hae toimitusrivit** -toiminnon uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-118">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="6ddc8-119">Kirjaa lasku valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-119">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="6ddc8-120">Yhdistä automaattisesti toimitukset yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="6ddc8-120">To automatically combine shipments on a single invoice</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6ddc8-121">valitsee vain ne myyntitilaukset, joissa on valittu **koontilasku**.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-121">will select only sales orders where **Combine Shipments** is chosen.</span></span> 

1. <span data-ttu-id="6ddc8-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimitusten yhdistäminen** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="6ddc8-123">Eräajon pyynnön sivu aukeaa.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="6ddc8-124">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="6ddc8-125">Valitse **Kirjaa laskut** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-125">Choose the **Post Invoices** check box.</span></span>  
4. <span data-ttu-id="6ddc8-126">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6ddc8-127">Huomaa, että laskut on kirjattava manuaalisesti, jos eräajon **Kirjaa laskut** -valintaruutua ei ole valittu.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="6ddc8-128">Avoimen myyntitilauksen poistaminen koontilaskun kirjauksen jälkeen</span><span class="sxs-lookup"><span data-stu-id="6ddc8-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="6ddc8-129">Kun koontilasku on tehty ja kirjattu, laskutetuille riveille luodaan kirjattu myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="6ddc8-130">Alkuperäisen puitemyyntitilauksen tai myyntitilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="6ddc8-131">Kun laskutat toimitukset näin, säilyvät tilaukset, joista toimitukset kirjattiin, vaikka ne olisi toimitettu ja laskutettu täysin.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="6ddc8-132">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poista laskutetut myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="6ddc8-133">Määritä **Numero** -kenttään</span><span class="sxs-lookup"><span data-stu-id="6ddc8-133">Specify in the **No.**</span></span> <span data-ttu-id="6ddc8-134">, mitkä myyntitilaukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="6ddc8-135">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="6ddc8-136">Voit myös poistaa manuaalisesti yksittäiset myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="6ddc8-137">Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puitemyyntitilauksissa.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ddc8-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6ddc8-138">See Also</span></span>  
[<span data-ttu-id="6ddc8-139">Myynti</span><span class="sxs-lookup"><span data-stu-id="6ddc8-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="6ddc8-140">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ddc8-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
