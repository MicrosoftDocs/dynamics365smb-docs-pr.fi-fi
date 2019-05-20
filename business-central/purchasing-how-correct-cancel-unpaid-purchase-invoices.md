---
title: Maksamattomien ostolaskujen korjaaminen tai peruuttaminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten kirjattua lasku korjataan, peruutetaan tai kumotaan ja miten ostohyvityslasku luodaan automaattisesti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 76ef3837801a5841a39228f956db48caba264336
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252571"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="8f263-103">Maksamattomien ostolaskujen korjaaminen tai peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="8f263-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="8f263-104">Voit korjata tai peruuttaa maksamattoman ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="8f263-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="8f263-105">Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai muuttaa ostoa tilausprosessin alkuvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="8f263-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="8f263-106">Jos olet jo maksanut kirjatun ostolaskun tuotteet, et voi korjata tai peruuttaa sitä itse kirjatusta ostolaskusta.</span><span class="sxs-lookup"><span data-stu-id="8f263-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="8f263-107">Sen sijaan sinun on peruutettava osto luomalla ostohyvityslasku, jota voi tarvittaessa hallinta ostopalautustilauksella.</span><span class="sxs-lookup"><span data-stu-id="8f263-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="8f263-108">Lisätietoja on kohdassa [Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="8f263-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="8f263-109">Valitse **Kirjattu ostolasku** -sivulla **Korjaa**- tai **Peruuta**-painike.</span><span class="sxs-lookup"><span data-stu-id="8f263-109">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="8f263-110">Kun korjaat tai peruutat kirjatun ostolaskun, korjaavaa ostohyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen ostolasku kirjattiin.</span><span class="sxs-lookup"><span data-stu-id="8f263-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="8f263-111">Tämä kumoaa kirjatun ostolaskun kirjanpitotietueissa ja jättää korjaavan kirjatun ostohyvityslaskun kirjausketjua varten.</span><span class="sxs-lookup"><span data-stu-id="8f263-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="8f263-112">Alla kerrotaan, miten **Korjaa**- ja **Peruuta**-painikkeita käytetään.</span><span class="sxs-lookup"><span data-stu-id="8f263-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="8f263-113">Kirjatun ostolaskun korjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="8f263-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="8f263-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8f263-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f263-115">Valitse kirjattu ostolasku, jonka haluat korjata.</span><span class="sxs-lookup"><span data-stu-id="8f263-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="8f263-116">Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua ostolaskua, koska se on jo korjattu tai peruutettu.</span><span class="sxs-lookup"><span data-stu-id="8f263-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="8f263-117">Valitse **Kirjattu ostolasku** -sivulla **Korjaa**.</span><span class="sxs-lookup"><span data-stu-id="8f263-117">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="8f263-118">Luodaan samoilla tiedoilla uusi ostolasku, johon voit tehdä korjauksen.</span><span class="sxs-lookup"><span data-stu-id="8f263-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="8f263-119">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="8f263-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="8f263-120">Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8f263-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="8f263-121">Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.</span><span class="sxs-lookup"><span data-stu-id="8f263-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="8f263-122">Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="8f263-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="8f263-123">Kirjatun ostolaskun peruuttamiseksi</span><span class="sxs-lookup"><span data-stu-id="8f263-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="8f263-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8f263-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f263-125">Valitse kirjattu ostolasku, jonka haluat peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="8f263-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="8f263-126">Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua ostolaskua, koska se on jo peruutettu tai korjattu.</span><span class="sxs-lookup"><span data-stu-id="8f263-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="8f263-127">Valitse **Kirjattu ostolasku** -sivulla **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="8f263-127">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="8f263-128">Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.</span><span class="sxs-lookup"><span data-stu-id="8f263-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="8f263-129">Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8f263-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="8f263-130">Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="8f263-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f263-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8f263-131">See Also</span></span>
[<span data-ttu-id="8f263-132">Osto</span><span class="sxs-lookup"><span data-stu-id="8f263-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="8f263-133">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="8f263-133">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="8f263-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f263-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
