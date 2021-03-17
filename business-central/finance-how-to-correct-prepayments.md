---
title: Ennakkomaksujen korjaaminen | Microsoft Docs
description: Joskus sinun on korjattava tilausta ennakkomaksulaskun kirjaamisen jälkeen. Voit lisätä tilaukseen uusia rivejä ennakkomaksun lähettämisen jälkeen ja voit kirjata uuden ennakkomaksulaskun, mutta et voi poistaa riviä tilauksesta sen jälkeen, kun rivin ennakkomaksu on laskutettu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6888db488114c306276a95fcedb4a1722637f48d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387422"
---
# <a name="correct-prepayments"></a><span data-ttu-id="914a2-104">Ennakkomaksujen korjaaminen</span><span class="sxs-lookup"><span data-stu-id="914a2-104">Correct Prepayments</span></span>

<span data-ttu-id="914a2-105">Joskus sinun on korjattava tilausta ennakkomaksulaskun kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="914a2-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="914a2-106">Voit lisätä tilaukseen uusia rivejä ennakkomaksun lähettämisen jälkeen ja voit kirjata uuden ennakkomaksulaskun, mutta et voi poistaa riviä tilauksesta sen jälkeen, kun rivin ennakkomaksu on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="914a2-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

> [!TIP]
> <span data-ttu-id="914a2-107">Jos myyntilaskun ennakkomaksulasku on kirjattu ja sitä sitten korjataan tai se peruutetaan, myös ennakkomaksu on korjattava tai peruutettava.</span><span class="sxs-lookup"><span data-stu-id="914a2-107">If you have posted a prepayment invoice for a sales invoice that you then correct or cancel, you must correct or cancel the prepayment as well.</span></span>

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="914a2-108">Ennakkomaksujen korjaaminen</span><span class="sxs-lookup"><span data-stu-id="914a2-108">To correct a prepayment</span></span>

<span data-ttu-id="914a2-109">Seuraavaksi kerrotaan, miten kaikki myyntitilauksen laskutetut ennakkomaksut peruutetaan luomalla ennakkomaksun hyvityslasku.</span><span class="sxs-lookup"><span data-stu-id="914a2-109">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  

1. <span data-ttu-id="914a2-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="914a2-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="914a2-111">Avaa asianomainen myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="914a2-111">Open the relevant sales order.</span></span>
3. <span data-ttu-id="914a2-112">Valitse ensin **Ennakkomaksu**-toiminto, sitten **Kirjaa ennakkomaksun hyvityslasku**- tai **Kirjaa ja tulosta ennakkomaksun hyvityslasku** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="914a2-112">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="914a2-113">Siirry **Myyntihyvityslasku**-sivulle korjaamaan kyseiset tapahtumat samalla tavoin kuin muissakin myyntihyvityslaskussa.</span><span class="sxs-lookup"><span data-stu-id="914a2-113">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="914a2-114">Lisätietoja on kohdassa [Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="914a2-114">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="914a2-115">**Rivisumma**-kentän summaa voi vähentää kasvattamalla ensin rivin ennakkomaksuprosenttia, jotta **Ennakkomaksun rivisumma** -kentän arvo ei ole pienempi kuin **Laskutettu ennakkomaksun summa** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="914a2-115">To reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="914a2-116">Tee ennakkomaksu myyntihyvityslaskun uusille riveille valitsemalla **Ennakkomaksu**-toiminto ja valitsemalla sitten **Kirjaa ennakkomaksulasku**- tai **Kirjaa ja tulosta ennakkomaksulasku** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="914a2-116">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="914a2-117">Voit luoda ylimääräisen ennakkomaksulaskun nostamalla vähintään yhden rivin ennakkomaksua ja kirjaamalla ennakkomaksulaskun.</span><span class="sxs-lookup"><span data-stu-id="914a2-117">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="914a2-118">Uusi lasku luodaan ennakkomaksun laskutettujen summien ja uusien ennakkomaksun summien välisen eron vuoksi.</span><span class="sxs-lookup"><span data-stu-id="914a2-118">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="914a2-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="914a2-119">See Also</span></span>

[<span data-ttu-id="914a2-120">Ennakkomaksujen laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="914a2-120">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="914a2-121">Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="914a2-121">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="914a2-122">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="914a2-122">Finance</span></span>](finance.md)  
<span data-ttu-id="914a2-123">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="914a2-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]