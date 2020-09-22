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
ms.date: 07/02/2020
ms.author: edupont
ms.openlocfilehash: 3badffb854323a385123e86066f14de5a2b75b28
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783122"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="ab6a8-103">Maksamattomien ostolaskujen korjaaminen tai peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="ab6a8-103">Correct or Cancel Unpaid Purchase Invoices</span></span>

<span data-ttu-id="ab6a8-104">Voit korjata tai peruuttaa maksamattoman ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="ab6a8-105">Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai muuttaa ostoa tilausprosessin alkuvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="ab6a8-106">Jos olet jo maksanut kirjatun ostolaskun tuotteet, et voi korjata tai peruuttaa sitä itse kirjatusta ostolaskusta.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="ab6a8-107">Sen sijaan sinun on peruutettava osto luomalla ostohyvityslasku, jota voi tarvittaessa hallinta ostopalautustilauksella.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="ab6a8-108">Samaa koskee tilannetta, jossa halutaan muokata yhdistettyihin ostovastaanottoihin perustuvaa ostolaskua.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-108">The same applies if you want to modify a posted purchase invoice that was based on combined purchase receipts.</span></span> <span data-ttu-id="ab6a8-109">Lisätietoja on kohdassa [Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="ab6a8-109">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="ab6a8-110">Valitse **Kirjattu ostolasku** -sivulla **Korjaa**- tai **Peruuta**-painike.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-110">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="ab6a8-111">Kun korjaat tai peruutat kirjatun ostolaskun, korjaavaa ostohyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen ostolasku kirjattiin.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-111">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="ab6a8-112">Tämä kumoaa kirjatun ostolaskun kirjanpitotietueissa ja jättää korjaavan kirjatun ostohyvityslaskun kirjausketjua varten.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-112">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="ab6a8-113">Alla kerrotaan, miten **Korjaa**- ja **Peruuta**-painikkeita käytetään.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-113">In the following the use of **Correct** and **Cancel** is described.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="ab6a8-114">Kirjatun ostolaskun korjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="ab6a8-114">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="ab6a8-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab6a8-116">Valitse kirjattu ostolasku, jonka haluat korjata.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-116">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="ab6a8-117">Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua ostolaskua, koska se on jo korjattu tai peruutettu.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-117">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="ab6a8-118">Valitse **Kirjattu ostolasku** -sivulla **Korjaa**.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-118">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="ab6a8-119">Luodaan samoilla tiedoilla uusi ostolasku, johon voit tehdä korjauksen.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-119">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="ab6a8-120">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="ab6a8-120">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="ab6a8-121">Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-121">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="ab6a8-122">Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-122">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="ab6a8-123">Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-123">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="ab6a8-124">Kirjatun ostolaskun peruuttamiseksi</span><span class="sxs-lookup"><span data-stu-id="ab6a8-124">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="ab6a8-125">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab6a8-126">Valitse kirjattu ostolasku, jonka haluat peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-126">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="ab6a8-127">Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua ostolaskua, koska se on jo peruutettu tai korjattu.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-127">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="ab6a8-128">Valitse **Kirjattu ostolasku** -sivulla **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-128">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="ab6a8-129">Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-129">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="ab6a8-130">Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-130">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="ab6a8-131">Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-131">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

### <a name="partial-invoice-posting-also-supported"></a><span data-ttu-id="ab6a8-132">Osittaisen laskun kirjausta tuetaan myös</span><span class="sxs-lookup"><span data-stu-id="ab6a8-132">Partial Invoice Posting also Supported</span></span>
<span data-ttu-id="ab6a8-133">Jos peruutus liittyy osittaiseen laskun kirjaukseen, alkuperäinen ostotilausrivi päivitetään peruutetun laskutetun määrän mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-133">If the cancellation is related to a partial invoice posting, then the originating purchase order line is updated to reflect the canceled invoiced quantity.</span></span> <span data-ttu-id="ab6a8-134">**Laskutettava määrä** - ja **Laskutettu määrä** -kentät liittyvässä ostotilauksessa palautetaan arvoihin ennen osittaista kirjausta.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-134">The **Qty. to Invoice** and **Qty. Invoiced** fields on the related purchase order line are reset to the values before the partial posting.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab6a8-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ab6a8-135">See Also</span></span>
[<span data-ttu-id="ab6a8-136">Osto</span><span class="sxs-lookup"><span data-stu-id="ab6a8-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="ab6a8-137">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="ab6a8-137">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="ab6a8-138">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ab6a8-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
