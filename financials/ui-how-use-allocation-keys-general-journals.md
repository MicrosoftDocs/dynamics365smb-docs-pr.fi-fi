---
title: "Toimintaohje: Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa | Microsoft Docs"
description: "Lisätietoja kohdistusavaimen käytöstä kirjauskansioissa."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bbacf9b5634d51478dd4d54ac4b587ea9bfaaf99
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-use-allocation-keys-in-general-journals"></a><span data-ttu-id="39d4d-103">Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa</span><span class="sxs-lookup"><span data-stu-id="39d4d-103">How to: Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="39d4d-104">Voit kohdistaa yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="39d4d-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="39d4d-105">Kohdistus voidaan tehdä määrän, prosentin tai summan mukaan.</span><span class="sxs-lookup"><span data-stu-id="39d4d-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="39d4d-106">Kohdistustunnusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="39d4d-106">To set up allocation keys</span></span>
1. <span data-ttu-id="39d4d-107">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Toistuva yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="39d4d-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="39d4d-108">Valitse **Erän nimi** -kenttä, kun haluat avata **Yleisen päiväkirjan erät** -ikkunan.</span><span class="sxs-lookup"><span data-stu-id="39d4d-108">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="39d4d-109">Voit muokata luettelon olemassa olevan erän kohdistuksia tai luoda uuden erän ja kohdistukset.</span><span class="sxs-lookup"><span data-stu-id="39d4d-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="39d4d-110">Luo uusi erä valitsemalla **Uusi**-toiminto ja siirtymällä seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="39d4d-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="39d4d-111">Voit muuttaa olemassa olevan päiväkirjan kohdistuksia valitsemalla päiväkirjan ja siirtymällä vaiheeseen 7.</span><span class="sxs-lookup"><span data-stu-id="39d4d-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="39d4d-112">Syötä **Nimi**-kenttään erän nimi, esimerkiksi SIIVOUS.</span><span class="sxs-lookup"><span data-stu-id="39d4d-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="39d4d-113">Syötä **Kuvaus**-kenttään kuvaus, esimerkiksi Siivouskulujen päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="39d4d-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="39d4d-114">Kun olet valmis, sulje ikkuna.</span><span class="sxs-lookup"><span data-stu-id="39d4d-114">When you are done, close the window.</span></span> <span data-ttu-id="39d4d-115">Esiin tulee uusi tyhjä toistuva kirjaus.</span><span class="sxs-lookup"><span data-stu-id="39d4d-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="39d4d-116">Täytä rivin kentät.</span><span class="sxs-lookup"><span data-stu-id="39d4d-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="39d4d-117">Valitse **Kohdistukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="39d4d-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="39d4d-118">Lisää rivi jokaista kohdistusta varten.</span><span class="sxs-lookup"><span data-stu-id="39d4d-118">Add a line for each allocation.</span></span> <span data-ttu-id="39d4d-119">Sinun täytyy täyttää jokin seuraavista kentistä: **Kohdistus- %**, **Kohdistettava määrä** tai **Summa**.</span><span class="sxs-lookup"><span data-stu-id="39d4d-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="39d4d-120">Sinun tulee täyttää myös **Tilinro**-kenttä</span><span class="sxs-lookup"><span data-stu-id="39d4d-120">You must also fill in the **Account No.**</span></span> <span data-ttu-id="39d4d-121">ja, mikäli kohdistat tapahtuman globaaleille dimensioille, globaalin dimension kentät.</span><span class="sxs-lookup"><span data-stu-id="39d4d-121">field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="39d4d-122">Jos syötät riville prosentin, ohjelma laskee **Summa**-kentän arvon automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="39d4d-122">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="39d4d-123">Näillä summilla on vastakkainen merkki kuin kokonaissummalla toistuvan kirjauksen **Summa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="39d4d-123">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="39d4d-124">Kun olet syöttänyt kohdistusrivit, valitse **OK** palataksesi takaisin **Toistuva yleinen päiväkirja** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="39d4d-124">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="39d4d-125">**Kohdistettu summa (USD)** -kenttä on täytetty ja vastaa **Summa** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="39d4d-125">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="39d4d-126">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="39d4d-126">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="39d4d-127">Aiemmin määritetyn kohdistusavaimen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="39d4d-127">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="39d4d-128">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Toistuva yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="39d4d-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="39d4d-129">Valitse **Toistuva yleinen päiväkirja** -ikkunassa päiväkirja, jossa kohdistus on.</span><span class="sxs-lookup"><span data-stu-id="39d4d-129">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="39d4d-130">Valitse kohdistuksen rivi ja valitse sitten **Kohdistukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="39d4d-130">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="39d4d-131">Vaihda soveltuvat kentät ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="39d4d-131">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="39d4d-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="39d4d-132">See Also</span></span>
[<span data-ttu-id="39d4d-133">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="39d4d-133">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="39d4d-134">Asiakirjojen ja päiväkirjojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="39d4d-134">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="39d4d-135">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39d4d-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

