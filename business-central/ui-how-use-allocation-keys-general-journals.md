---
title: Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa | Microsoft Docs
description: Lisätietoja kohdistusavaimen käytöstä kirjauskansioissa.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: aa2e553b28825338dadd758f48c5ff43a0494cf4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249236"
---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="0c96e-103">Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa</span><span class="sxs-lookup"><span data-stu-id="0c96e-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="0c96e-104">Voit kohdistaa yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="0c96e-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="0c96e-105">Kohdistus voidaan tehdä määrän, prosentin tai summan mukaan.</span><span class="sxs-lookup"><span data-stu-id="0c96e-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="0c96e-106">Kohdistusavaimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0c96e-106">To set up allocation keys</span></span>
1. <span data-ttu-id="0c96e-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toistuva yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0c96e-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c96e-108">Valitse **Erän nimi** -kenttä, kun haluat avata **Yleisen päiväkirjan erät** -sivun.</span><span class="sxs-lookup"><span data-stu-id="0c96e-108">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="0c96e-109">Voit muokata luettelon olemassa olevan erän kohdistuksia tai luoda uuden erän ja kohdistukset.</span><span class="sxs-lookup"><span data-stu-id="0c96e-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="0c96e-110">Luo uusi erä valitsemalla **Uusi**-toiminto ja siirtymällä seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="0c96e-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="0c96e-111">Voit muuttaa olemassa olevan päiväkirjan kohdistuksia valitsemalla päiväkirjan ja siirtymällä vaiheeseen 7.</span><span class="sxs-lookup"><span data-stu-id="0c96e-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="0c96e-112">Syötä **Nimi**-kenttään erän nimi, esimerkiksi SIIVOUS.</span><span class="sxs-lookup"><span data-stu-id="0c96e-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="0c96e-113">Syötä **Kuvaus**-kenttään kuvaus, esimerkiksi Siivouskulujen päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="0c96e-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="0c96e-114">Kun olet valmis, sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0c96e-114">When you are done, close the page.</span></span> <span data-ttu-id="0c96e-115">Esiin tulee uusi tyhjä toistuva kirjaus.</span><span class="sxs-lookup"><span data-stu-id="0c96e-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="0c96e-116">Täytä rivin kentät.</span><span class="sxs-lookup"><span data-stu-id="0c96e-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="0c96e-117">Valitse **Kohdistukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="0c96e-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="0c96e-118">Lisää rivi jokaista kohdistusta varten.</span><span class="sxs-lookup"><span data-stu-id="0c96e-118">Add a line for each allocation.</span></span> <span data-ttu-id="0c96e-119">Sinun täytyy täyttää jokin seuraavista kentistä: **Kohdistus- %**, **Kohdistettava määrä** tai **Summa**.</span><span class="sxs-lookup"><span data-stu-id="0c96e-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="0c96e-120">Sinun tulee myös täyttää **Tilinro**-kenttä ja, mikäli kohdistat tapahtuman globaaleille dimensioille, globaali dimensio -kentät.</span><span class="sxs-lookup"><span data-stu-id="0c96e-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="0c96e-121">Jos syötät riville prosentin, ohjelma laskee **Summa**-kentän arvon automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0c96e-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="0c96e-122">Näillä summilla on vastakkainen merkki kuin kokonaissummalla toistuvan kirjauksen **Summa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0c96e-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="0c96e-123">Kun olet syöttänyt kohdistusrivit, valitse **OK** palataksesi takaisin **Toistuva yleinen päiväkirja** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="0c96e-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="0c96e-124">**Kohdistettu summa (USD)** -kenttä on täytetty ja vastaa **Summa** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="0c96e-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="0c96e-125">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="0c96e-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="0c96e-126">Aiemmin määritetyn kohdistusavaimen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="0c96e-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="0c96e-127">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Toistuva yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0c96e-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c96e-128">Valitse **Toistuva yleinen päiväkirja** -sivulla päiväkirja, jossa kohdistus on.</span><span class="sxs-lookup"><span data-stu-id="0c96e-128">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="0c96e-129">Valitse ensin kohdistuksen rivi ja sitten **Kohdistukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="0c96e-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="0c96e-130">Vaihda soveltuvat kentät ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="0c96e-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c96e-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0c96e-131">See Also</span></span>
[<span data-ttu-id="0c96e-132">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0c96e-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="0c96e-133">Asiakirjojen ja päiväkirjojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="0c96e-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="0c96e-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c96e-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
