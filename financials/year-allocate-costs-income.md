---
title: "Kustannusten ja tulojen kohdistustehtävien yleiskatsaus | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan tehtävistä, joilla voi kohdistaa yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1620e69ce8018256780dcba108c31312c02166cb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-allocate-costs-and-income"></a><span data-ttu-id="634dc-103">Toimintaohje: Kustannusten ja tulojen kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="634dc-103">How to: Allocate Costs and Income</span></span>
<span data-ttu-id="634dc-104">Voit kohdistaa yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="634dc-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="634dc-105">Kohdistamisen voi tehdä kolmella eri tavalla:</span><span class="sxs-lookup"><span data-stu-id="634dc-105">The allocation can be made by three different methods:</span></span>

* <span data-ttu-id="634dc-106">määrä</span><span class="sxs-lookup"><span data-stu-id="634dc-106">Quantity</span></span>
* <span data-ttu-id="634dc-107">prosenttiosuus (%)</span><span class="sxs-lookup"><span data-stu-id="634dc-107">Percentage (%)</span></span>
* <span data-ttu-id="634dc-108">Summa</span><span class="sxs-lookup"><span data-stu-id="634dc-108">Amount</span></span>

<span data-ttu-id="634dc-109">Kohdistustoimintoja voi käyttää toistuvien yleisten päiväkirjojen ja käyttöomaisuuspäiväkirjojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="634dc-109">The allocation features can be used with recurring general journals and in fixed assets journals.</span></span>
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

<span data-ttu-id="634dc-110">Seuraavaksi kerrotaan, miten kustannusten kohdistus valmistellaan toistuvissa yleisessä päiväkirjassa määrittämällä kohdistusavaimet.</span><span class="sxs-lookup"><span data-stu-id="634dc-110">The following procedures describe how to prepare to allocate costs in a recurring general journal by defining allocation keys.</span></span> <span data-ttu-id="634dc-111">Kun kohdistusavaimet on määritetty, voit suorittaa ja kirjata päiväkirjan muiden toistuvien yleisten päiväkirjojen tavoin.</span><span class="sxs-lookup"><span data-stu-id="634dc-111">When allocation keys are defined, you complete and post the journal like any other recurring general journal.</span></span> <span data-ttu-id="634dc-112">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="634dc-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="634dc-113">Kohdistusavaimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="634dc-113">To set up allocation keys</span></span>
<span data-ttu-id="634dc-114">Voit kohdistaa toistuvan yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="634dc-114">You can allocate an entry in a recurring general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="634dc-115">Kohdistus voidaan tehdä määrän, prosentin tai summan mukaan.</span><span class="sxs-lookup"><span data-stu-id="634dc-115">The allocation can be made by quantity, percentage, or amount.</span></span>
1. <span data-ttu-id="634dc-116">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Toistuva yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="634dc-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="634dc-117">Valitse **Erän nimi** -kenttä, kun haluat avata **Yleisen päiväkirjan erät** -ikkunan.</span><span class="sxs-lookup"><span data-stu-id="634dc-117">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="634dc-118">Voit muokata luettelon olemassa olevan erän kohdistuksia tai luoda uuden erän ja kohdistukset.</span><span class="sxs-lookup"><span data-stu-id="634dc-118">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="634dc-119">Luo uusi erä valitsemalla **Uusi**-toiminto ja siirtymällä seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="634dc-119">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="634dc-120">Voit muuttaa olemassa olevan päiväkirjan kohdistuksia valitsemalla päiväkirjan ja siirtymällä vaiheeseen 7.</span><span class="sxs-lookup"><span data-stu-id="634dc-120">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="634dc-121">Syötä **Nimi**-kenttään erän nimi, esimerkiksi SIIVOUS.</span><span class="sxs-lookup"><span data-stu-id="634dc-121">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="634dc-122">Syötä **Kuvaus**-kenttään kuvaus, esimerkiksi Siivouskulujen päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="634dc-122">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="634dc-123">Kun olet valmis, sulje ikkuna.</span><span class="sxs-lookup"><span data-stu-id="634dc-123">When you are done, close the window.</span></span> <span data-ttu-id="634dc-124">Esiin tulee uusi tyhjä toistuva kirjaus.</span><span class="sxs-lookup"><span data-stu-id="634dc-124">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="634dc-125">Täytä rivin kentät.</span><span class="sxs-lookup"><span data-stu-id="634dc-125">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="634dc-126">Valitse **Kohdistukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="634dc-126">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="634dc-127">Lisää rivi jokaista kohdistusta varten.</span><span class="sxs-lookup"><span data-stu-id="634dc-127">Add a line for each allocation.</span></span> <span data-ttu-id="634dc-128">Sinun täytyy täyttää jokin seuraavista kentistä: **Kohdistus- %**, **Kohdistettava määrä** tai **Summa**.</span><span class="sxs-lookup"><span data-stu-id="634dc-128">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="634dc-129">Sinun tulee myös täyttää **Tilinro**-kenttä ja, mikäli kohdistat tapahtuman globaaleille dimensioille, globaali dimensio -kentät.</span><span class="sxs-lookup"><span data-stu-id="634dc-129">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="634dc-130">Jos syötät riville prosentin, ohjelma laskee **Summa**-kentän arvon automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="634dc-130">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="634dc-131">Näillä summilla on vastakkainen merkki kuin kokonaissummalla toistuvan kirjauksen **Summa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="634dc-131">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="634dc-132">Kun olet syöttänyt kohdistusrivit, valitse **OK** palataksesi takaisin **Toistuva yleinen päiväkirja** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="634dc-132">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="634dc-133">**Kohdistettu summa (USD)** -kenttä on täytetty ja vastaa **Summa** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="634dc-133">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="634dc-134">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="634dc-134">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="634dc-135">Aiemmin määritetyn kohdistusavaimen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="634dc-135">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="634dc-136">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Toistuva yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="634dc-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="634dc-137">Valitse **Toistuva yleinen päiväkirja** -ikkunassa päiväkirja, jossa kohdistus on.</span><span class="sxs-lookup"><span data-stu-id="634dc-137">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="634dc-138">Valitse ensin kohdistuksen rivi ja sitten **Kohdistukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="634dc-138">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="634dc-139">Vaihda soveltuvat kentät ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="634dc-139">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="634dc-140">Katso myös</span><span class="sxs-lookup"><span data-stu-id="634dc-140">See Also</span></span>
[<span data-ttu-id="634dc-141">Vuosien ja jaksojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="634dc-141">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="634dc-142">[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="634dc-142">[Working with General Journals](ui-work-general-journals.md)  </span></span>  
<span data-ttu-id="634dc-143">[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="634dc-143">[Posting Documents and Journals](ui-post-documents-journals.md)  </span></span>  
<span data-ttu-id="634dc-144">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="634dc-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

