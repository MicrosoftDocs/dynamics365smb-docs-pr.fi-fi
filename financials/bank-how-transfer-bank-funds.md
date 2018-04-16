---
title: "Pankkivarojen siirtäminen| Microsoft Docs"
description: "Voit siirtää summia pankkitililtä toisille myös muissa valuutoissa kirjaamalla tapahtuman yleiseen päiväkirjaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: f19fbdd0f0059e62080d0076bdc419712560d4f2
ms.contentlocale: fi-fi
ms.lasthandoff: 04/16/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="b85be-103">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="b85be-103">Transfer Bank Funds</span></span>
<span data-ttu-id="b85be-104">Joskus on siirrettävä varoja yhdeltä pankkitililtä toiselle.</span><span class="sxs-lookup"><span data-stu-id="b85be-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="b85be-105">Se tehdään kirjaamalla tapahtuma yleiseen päiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="b85be-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="b85be-106">Tehtävä vaihtelee sen mukaan, käytetäänkö pankkitileillä samaa vai eri valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="b85be-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="b85be-107">Siirtojen kirjaaminen pankkitileillä, jotka käyttävät samaa valuuttakoodia</span><span class="sxs-lookup"><span data-stu-id="b85be-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="b85be-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b85be-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="b85be-109">Täytä päiväkirjan rivillä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.</span><span class="sxs-lookup"><span data-stu-id="b85be-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="b85be-110">Valitse **Tilityyppi**-kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="b85be-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="b85be-111">Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="b85be-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="b85be-112">Syötä siirrettävä summa **Summa**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b85be-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="b85be-113">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="b85be-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="b85be-114">Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="b85be-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="b85be-115">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="b85be-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="b85be-116">Siirtojen kirjaaminen pankkitileillä, joilla on eri valuuttakoodit</span><span class="sxs-lookup"><span data-stu-id="b85be-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="b85be-117">Voit siirtää varoja eri valuuttoja käyttävien pankkitilien välillä kirjaamalla kaksi yleisen päiväkirjan riviä.</span><span class="sxs-lookup"><span data-stu-id="b85be-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="b85be-118">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b85be-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="b85be-119">Luo kaksi päiväkirjan riviä ja täytä **Kirjauspvm**- ja **Asiakirjan nro.** -kentät.</span><span class="sxs-lookup"><span data-stu-id="b85be-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="b85be-120">Valitse **Tyyppi**-kentän ensimmäisellä rivillä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="b85be-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="b85be-121">Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="b85be-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="b85be-122">Syötä **Summa**-kenttään summa pankkitilin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="b85be-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="b85be-123">Anna kredit-summat miinusmerkkisinä.</span><span class="sxs-lookup"><span data-stu-id="b85be-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="b85be-124">Anna debet-summat ilman miinusmerkkiä.</span><span class="sxs-lookup"><span data-stu-id="b85be-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="b85be-125">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="b85be-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="b85be-126">Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="b85be-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="b85be-127">Valitse **Tyyppi**-kentän toisella rivillä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="b85be-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="b85be-128">Valitse **Tilinro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="b85be-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="b85be-129">Syötä **Summa**-kenttään summa pankkitilin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="b85be-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="b85be-130">Anna kredit-summat miinusmerkkisinä.</span><span class="sxs-lookup"><span data-stu-id="b85be-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="b85be-131">Anna debet-summat ilman miinusmerkkiä.</span><span class="sxs-lookup"><span data-stu-id="b85be-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="b85be-132">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="b85be-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="b85be-133">Valitse **Vastatilin nro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="b85be-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="b85be-134">Jos päiväkirjassa käytetyt vaihtokurssit eroavat **Valuutan vaihtokurssit** -ikkunan kursseista, syötä kolmas rivi vaihtokurssivoittoa tai -tappiota varten.</span><span class="sxs-lookup"><span data-stu-id="b85be-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="b85be-135">Valitse **KP-tili**-kentässä**Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="b85be-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="b85be-136">Syötä **Tilinro**-kenttään valuuttakurssivoittojen ja -tappioiden KP-tilin numero.</span><span class="sxs-lookup"><span data-stu-id="b85be-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="b85be-137">Syötä valuuttakurssivoitto tai -tappio **Summa**-kenttään. Syötä summa miinusmerkin kanssa, jos kyseessä on kredit, ja ilman miinusmerkkiä, jos kyseessä on debet.</span><span class="sxs-lookup"><span data-stu-id="b85be-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="b85be-138">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="b85be-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="b85be-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b85be-139">See Also</span></span>
[<span data-ttu-id="b85be-140">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="b85be-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="b85be-141">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b85be-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="b85be-142">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="b85be-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="b85be-143">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b85be-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

