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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3d0d1234a6459b153a436ed2dfe9a3a2f667ab89
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192745"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="55190-103">Maksamattomien ostolaskujen korjaaminen tai peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="55190-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="55190-104">Voit korjata tai peruuttaa maksamattoman ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="55190-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="55190-105">Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai muuttaa ostoa tilausprosessin alkuvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="55190-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="55190-106">Jos olet jo maksanut kirjatun ostolaskun tuotteet, et voi korjata tai peruuttaa sitä itse kirjatusta ostolaskusta.</span><span class="sxs-lookup"><span data-stu-id="55190-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="55190-107">Sen sijaan sinun on peruutettava osto luomalla ostohyvityslasku, jota voi tarvittaessa hallinta ostopalautustilauksella.</span><span class="sxs-lookup"><span data-stu-id="55190-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="55190-108">Lisätietoja on kohdassa [Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="55190-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="55190-109">Valitse **Kirjattu ostolasku** -sivulla **Korjaa**- tai **Peruuta**-painike.</span><span class="sxs-lookup"><span data-stu-id="55190-109">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="55190-110">Kun korjaat tai peruutat kirjatun ostolaskun, korjaavaa ostohyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen ostolasku kirjattiin.</span><span class="sxs-lookup"><span data-stu-id="55190-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="55190-111">Tämä kumoaa kirjatun ostolaskun kirjanpitotietueissa ja jättää korjaavan kirjatun ostohyvityslaskun kirjausketjua varten.</span><span class="sxs-lookup"><span data-stu-id="55190-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="55190-112">Alla kerrotaan, miten **Korjaa**- ja **Peruuta**-painikkeita käytetään.</span><span class="sxs-lookup"><span data-stu-id="55190-112">In the following the use of **Correct** and **Cancel** is described.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="55190-113">Kirjatun ostolaskun korjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="55190-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="55190-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="55190-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="55190-115">Valitse kirjattu ostolasku, jonka haluat korjata.</span><span class="sxs-lookup"><span data-stu-id="55190-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="55190-116">Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua ostolaskua, koska se on jo korjattu tai peruutettu.</span><span class="sxs-lookup"><span data-stu-id="55190-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="55190-117">Valitse **Kirjattu ostolasku** -sivulla **Korjaa**.</span><span class="sxs-lookup"><span data-stu-id="55190-117">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="55190-118">Luodaan samoilla tiedoilla uusi ostolasku, johon voit tehdä korjauksen.</span><span class="sxs-lookup"><span data-stu-id="55190-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="55190-119">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="55190-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="55190-120">Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="55190-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="55190-121">Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.</span><span class="sxs-lookup"><span data-stu-id="55190-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="55190-122">Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="55190-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="55190-123">Kirjatun ostolaskun peruuttamiseksi</span><span class="sxs-lookup"><span data-stu-id="55190-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="55190-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="55190-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="55190-125">Valitse kirjattu ostolasku, jonka haluat peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="55190-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="55190-126">Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua ostolaskua, koska se on jo peruutettu tai korjattu.</span><span class="sxs-lookup"><span data-stu-id="55190-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="55190-127">Valitse **Kirjattu ostolasku** -sivulla **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="55190-127">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="55190-128">Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.</span><span class="sxs-lookup"><span data-stu-id="55190-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="55190-129">Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="55190-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="55190-130">Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="55190-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

### <a name="partial-invoice-posting-also-supported"></a><span data-ttu-id="55190-131">Osittaisen laskun kirjausta tuetaan myös</span><span class="sxs-lookup"><span data-stu-id="55190-131">Partial Invoice Posting also Supported</span></span>
<span data-ttu-id="55190-132">Jos peruutus liittyy osittaiseen laskun kirjaukseen, alkuperäinen ostotilausrivi päivitetään peruutetun laskutetun määrän mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="55190-132">If the cancellation is related to a partial invoice posting, then the originating purchase order line is updated to reflect the canceled invoiced quantity.</span></span> <span data-ttu-id="55190-133">**Laskutettava määrä** - ja **Laskutettu määrä** -kentät liittyvässä ostotilauksessa palautetaan arvoihin ennen osittaista kirjausta.</span><span class="sxs-lookup"><span data-stu-id="55190-133">The **Qty. to Invoice** and **Qty. Invoiced** fields on the related purchase order line are reset to the values before the partial posting.</span></span>

## <a name="see-also"></a><span data-ttu-id="55190-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="55190-134">See Also</span></span>
[<span data-ttu-id="55190-135">Osto</span><span class="sxs-lookup"><span data-stu-id="55190-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="55190-136">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="55190-136">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="55190-137">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="55190-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
