---
title: Vastaanottojen yhdistäminen | Microsoft Docs
description: Jos haluat laskuttaa useita ostovastaanottoja kerralla, voit käyttää Vastaanottojen yhdistämistoimintoa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5e1b04cc998319cc835b5dcc1547723c48be6763
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252871"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="55b70-103">Vastaanottojen yhdistäminen yhteen laskuun</span><span class="sxs-lookup"><span data-stu-id="55b70-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="55b70-104">Jos haluat laskuttaa useita ostovastaanottoja kerralla, voit käyttää **Vastaanottojen yhdistämistoimintoa**.</span><span class="sxs-lookup"><span data-stu-id="55b70-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="55b70-105">Yhdistetyn vastaanoton voi luoda vasta, kun vähintään kaksi saman toimittajan ostokuittia on kirjattu samalla valuutalla.</span><span class="sxs-lookup"><span data-stu-id="55b70-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="55b70-106">Toisin sanoen vähintään kaksi ostotilausta täytyy olla täytetty ja kirjattu vastaanotetuiksi (mutta ei laskutetuiksi).</span><span class="sxs-lookup"><span data-stu-id="55b70-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="55b70-107">Kun ostovastaanotot yhdistetään laskuun ja kirjataan, askutetuille riveille luodaan kirjattu ostolasku.</span><span class="sxs-lookup"><span data-stu-id="55b70-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="55b70-108">Alkuperäisen puiteostotilauksen ja/tai ostotilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="55b70-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="55b70-109">Tätä alkuperäistä ostoasiakirjaa ei kuitenkaan ole poistettu, vaikka se on kokonaan vastaanotettu ja laskutettu. Sen vuoksi ostoasiakirja on poistettava.</span><span class="sxs-lookup"><span data-stu-id="55b70-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="55b70-110">Vastaanottojen yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="55b70-110">To combine receipts</span></span>  
1. <span data-ttu-id="55b70-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="55b70-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="55b70-112">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="55b70-112">Choose the **New** action.</span></span> <span data-ttu-id="55b70-113">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="55b70-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="55b70-114">Valitse **Rivit**-pikavälilehdessä **Hae vast.oton rivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="55b70-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="55b70-115">Valitse useat vastaanoton rivit, jotka haluat sisällyttää laskuun:</span><span class="sxs-lookup"><span data-stu-id="55b70-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="55b70-116">Jos valitsit väärän vastaanoton rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa rivit ostolaskusta ja suorittaa **Hae vast.oton rivit** -toiminnon uudelleen.</span><span class="sxs-lookup"><span data-stu-id="55b70-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="55b70-117">Kirjaa lasku valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="55b70-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="55b70-118">Poista avoin ostotilaus yhdistetyn vastaanoton kirjauksen jälkeen</span><span class="sxs-lookup"><span data-stu-id="55b70-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="55b70-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista laskutetut ostotilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="55b70-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="55b70-120">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="55b70-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="55b70-121">.</span><span class="sxs-lookup"><span data-stu-id="55b70-121">.</span></span>
3. <span data-ttu-id="55b70-122">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="55b70-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="55b70-123">Voit myös poistaa manuaalisesti yksittäiset tilaukset.</span><span class="sxs-lookup"><span data-stu-id="55b70-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="55b70-124">Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puiteostotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="55b70-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="55b70-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="55b70-125">See Also</span></span>  
[<span data-ttu-id="55b70-126">Osto</span><span class="sxs-lookup"><span data-stu-id="55b70-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="55b70-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="55b70-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
