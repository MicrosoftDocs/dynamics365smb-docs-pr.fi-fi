---
title: Kirjatun myyntilaskun korjaaminen tai peruuttaminen | Microsoft Docs
description: "Ohjeaiheessa käsitellään, miten kirjattu myyntilasku korjataan, kumotaan tai peruutetaan ja miten myyntihyvityslasku kohdistetaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e8e5a4762564d036ac8c0e7bdaf9e13b448d37f4
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a><span data-ttu-id="da2a8-103">Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="da2a8-103">Correct or Cancel Unpaid Sales Invoices</span></span>
<span data-ttu-id="da2a8-104">Voit korjata tai peruuttaa maksamattoman myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="da2a8-104">You can correct or cancel a posted sales invoice.</span></span> <span data-ttu-id="da2a8-105">Tästä on hyötyä, jos teet virheen tai jos asiakas pyytää muutosta.</span><span class="sxs-lookup"><span data-stu-id="da2a8-105">This is useful if you make a mistake or if the customer requests a change.</span></span>

> [!NOTE]  
>   <span data-ttu-id="da2a8-106">Kun kirjattu myyntilasku on osittain tai kokonaan maksettu, et voi korjata tai peruuttaa sitä itse kirjatusta myyntilaskusta.</span><span class="sxs-lookup"><span data-stu-id="da2a8-106">After a posted sales invoice has been partially or fully paid, you cannot correct or cancel it from the posted sales invoice itself.</span></span> <span data-ttu-id="da2a8-107">Sen sijaan sinun on luotava manuaalisesti myyntihyvityslasku, jolla myynti mitätöidään ja asiakas hyvitetään. Sitä voi haluttaessa hallita myyntipalautustilauksella.</span><span class="sxs-lookup"><span data-stu-id="da2a8-107">Instead, you must manually create a sales credit memo to void the sale and reimburse the customer, optionally managed with a sales return order.</span></span> <span data-ttu-id="da2a8-108">Lisätietoja on kohdassa [Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="da2a8-108">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>

<span data-ttu-id="da2a8-109">Voit valita **Kirjattu myyntilasku** -ikkunassa **Korjaa** - tai **Peruuta**-toiminnon suorittaaksesi toimintoja, jotka on kuvattu seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="da2a8-109">In the **Posted Sales Invoice** window, you can choose the **Correct** action or the **Cancel** action to perform the actions that are described in the following table.</span></span>

| <span data-ttu-id="da2a8-110">Toiminto</span><span class="sxs-lookup"><span data-stu-id="da2a8-110">Action</span></span> | <span data-ttu-id="da2a8-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="da2a8-111">Description</span></span> |
| --- | --- |
| <span data-ttu-id="da2a8-112">**Korjaa**</span><span class="sxs-lookup"><span data-stu-id="da2a8-112">**Correct**</span></span> |<span data-ttu-id="da2a8-113">Kirjattu myyntilaskun peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="da2a8-113">The posted sales invoice is canceled.</span></span> <span data-ttu-id="da2a8-114">Luodaan uusi myyntilasku, jossa on samat tiedot.</span><span class="sxs-lookup"><span data-stu-id="da2a8-114">A new sales invoice with the same information is created.</span></span> <span data-ttu-id="da2a8-115">Voit suorittaa korjauksen ja jatkaa sitten myyntiprosessia.</span><span class="sxs-lookup"><span data-stu-id="da2a8-115">You can make the correction and then continue the sales process.</span></span> <span data-ttu-id="da2a8-116">Uudella myyntilaskulla on eri numero kuin alkuperäisellä myyntilaskulla.</span><span class="sxs-lookup"><span data-stu-id="da2a8-116">The new sales invoice has a different number than the initial sales invoice.</span></span> <span data-ttu-id="da2a8-117">Korjaavat myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="da2a8-117">A corrective sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="da2a8-118">Alkuperäisen kirjatun myyntilaskun Peruutettu- ja Maksettu-valintaruudut ovat valittuina.</span><span class="sxs-lookup"><span data-stu-id="da2a8-118">On the initial posted sales invoice, the Canceled and Paid check boxes are selected.</span></span> |
| <span data-ttu-id="da2a8-119">**Peruuta**</span><span class="sxs-lookup"><span data-stu-id="da2a8-119">**Cancel**</span></span> |<span data-ttu-id="da2a8-120">Kirjattu myyntilaskun peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="da2a8-120">The posted sales invoice is canceled.</span></span> <span data-ttu-id="da2a8-121">Korjaavat myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="da2a8-121">A corrective sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="da2a8-122">Alkuperäisen kirjatun myyntilaskun Peruutettu- ja Maksettu-valintaruudut ovat valittuina.</span><span class="sxs-lookup"><span data-stu-id="da2a8-122">On the initial posted sales invoice, the Canceled and Paid check boxes are selected.</span></span> |

<span data-ttu-id="da2a8-123">Kun korjaat tai peruutat kirjatun myyntilaskun, korjaavaa myyntihyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen myyntilasku kirjattiin.</span><span class="sxs-lookup"><span data-stu-id="da2a8-123">When you correct or cancel a posted sales invoice, the corrective sales credit memo is applied to all general ledger and inventory ledger entries that were created when the initial sales invoice was posted.</span></span> <span data-ttu-id="da2a8-124">Tämä kumoaa kirjatun myyntilaskun kirjanpitotietueissa ja jättää korjaavan kirjatun myyntihyvityslaskun kirjausketjua varten.</span><span class="sxs-lookup"><span data-stu-id="da2a8-124">This reverses the posted sales invoice in your financial records and leaves the corrective posted sales credit memo for your audit trail.</span></span>

## <a name="to-correct-a-posted-sales-invoice"></a><span data-ttu-id="da2a8-125">Kirjatun myyntilaskun korjaaminen</span><span class="sxs-lookup"><span data-stu-id="da2a8-125">To correct a posted sales invoice</span></span>
1. <span data-ttu-id="da2a8-126">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjatut myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="da2a8-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="da2a8-127">Valitse kirjattu myyntilasku, jonka haluat korjata.</span><span class="sxs-lookup"><span data-stu-id="da2a8-127">Select the posted sales invoice that you want to correct.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="da2a8-128">Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua myyntilaskua, koska se on jo korjattu tai peruutettu.</span><span class="sxs-lookup"><span data-stu-id="da2a8-128">If the **Canceled** check box is selected, then you cannot correct the posted sales invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="da2a8-129">Valitse **Kirjattu myyntilasku** -ikkunassa **Korjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="da2a8-129">In the **Posted Sales Invoice** window, choose the **Correct** action.</span></span>  
4. <span data-ttu-id="da2a8-130">Luodaan samoilla tiedoilla uusi myyntilasku, johon voit tehdä korjauksen.</span><span class="sxs-lookup"><span data-stu-id="da2a8-130">A new sales invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="da2a8-131">Alkuperäisen kirjatun myyntilaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="da2a8-131">The **Canceled** field on the initial posted sales invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="da2a8-132">Korjaava myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="da2a8-132">A sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span>
5. <span data-ttu-id="da2a8-133">Valitse **Näytä korjaava hyvityslasku** -toiminto, kun haluat tarkastella kirjattua myyntihyvityslaskua, joka mitätöi alkuperäisen kirjatun myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="da2a8-133">Choose the **Show Corrective Credit Memo** action to view the posted sales credit memo that voids the initial posted sales invoice.</span></span>

## <a name="to-cancel-a-posted-sales-invoice"></a><span data-ttu-id="da2a8-134">Kirjatun myyntilaskun peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="da2a8-134">To cancel a posted sales invoice</span></span>
1. <span data-ttu-id="da2a8-135">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjatut myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="da2a8-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="da2a8-136">Valitse kirjattu myyntilasku, jonka haluat peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="da2a8-136">Select the posted sales invoice that you want to cancel.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="da2a8-137">Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua myyntilaskua, koska se on jo peruutettu tai korjattu.</span><span class="sxs-lookup"><span data-stu-id="da2a8-137">If the **Canceled** check box is selected, then you cannot cancel the posted sales invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="da2a8-138">Valitse **Kirjattu myyntilasku** -ikkunassa **Peruuta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="da2a8-138">In the **Posted Sales Invoice** window, choose the **Cancel** action.</span></span>

    <span data-ttu-id="da2a8-139">Korjaava myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="da2a8-139">A sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="da2a8-140">Alkuperäisen kirjatun myyntilaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="da2a8-140">The **Canceled** field on the initial posted sales invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="da2a8-141">Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua myyntihyvityslaskua, joka mitätöi alkuperäisen kirjatun myyntilaskun.</span><span class="sxs-lookup"><span data-stu-id="da2a8-141">Choose **Show Corrective Credit Memo** to view the posted sales credit memo that voids the initial posted sales invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="da2a8-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="da2a8-142">See Also</span></span>
[<span data-ttu-id="da2a8-143">Myynti</span><span class="sxs-lookup"><span data-stu-id="da2a8-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="da2a8-144">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="da2a8-144">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="da2a8-145">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="da2a8-145">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="da2a8-146">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da2a8-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

