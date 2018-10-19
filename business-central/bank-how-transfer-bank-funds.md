---
title: "Pankkivarojen siirtäminen| Microsoft Docs"
description: "Voit siirtää summia pankkitililtä toisille myös muissa valuutoissa kirjaamalla tapahtuman yleiseen päiväkirjaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 758833e146c03cde3f892ec24d43143bcdce655c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="61296-103">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="61296-103">Transfer Bank Funds</span></span>
<span data-ttu-id="61296-104">Joskus on siirrettävä varoja yhdeltä pankkitililtä toiselle.</span><span class="sxs-lookup"><span data-stu-id="61296-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="61296-105">Se tehdään kirjaamalla tapahtuma yleiseen päiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="61296-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="61296-106">Tehtävä vaihtelee sen mukaan, käytetäänkö pankkitileillä samaa vai eri valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="61296-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="61296-107">Siirtojen kirjaaminen pankkitileillä, jotka käyttävät samaa valuuttakoodia</span><span class="sxs-lookup"><span data-stu-id="61296-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="61296-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="61296-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="61296-109">Täytä päiväkirjan rivillä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.</span><span class="sxs-lookup"><span data-stu-id="61296-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="61296-110">Valitse **Tilityyppi**-kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="61296-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="61296-111">Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="61296-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="61296-112">Syötä siirrettävä summa **Summa**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="61296-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="61296-113">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="61296-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="61296-114">Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="61296-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="61296-115">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="61296-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="61296-116">Siirtojen kirjaaminen pankkitileillä, joilla on eri valuuttakoodit</span><span class="sxs-lookup"><span data-stu-id="61296-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="61296-117">Voit siirtää varoja eri valuuttoja käyttävien pankkitilien välillä kirjaamalla kaksi yleisen päiväkirjan riviä.</span><span class="sxs-lookup"><span data-stu-id="61296-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="61296-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="61296-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="61296-119">Luo kaksi päiväkirjan riviä ja täytä **Kirjauspvm**- ja **Asiakirjan nro.** -kentät.</span><span class="sxs-lookup"><span data-stu-id="61296-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="61296-120">Valitse **Tyyppi**-kentän ensimmäisellä rivillä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="61296-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="61296-121">Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="61296-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="61296-122">Syötä **Summa**-kenttään summa pankkitilin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="61296-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="61296-123">Anna kredit-summat miinusmerkkisinä.</span><span class="sxs-lookup"><span data-stu-id="61296-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="61296-124">Anna debet-summat ilman miinusmerkkiä.</span><span class="sxs-lookup"><span data-stu-id="61296-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="61296-125">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="61296-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="61296-126">Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="61296-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="61296-127">Valitse **Tyyppi**-kentän toisella rivillä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="61296-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="61296-128">Valitse **Tilinro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="61296-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="61296-129">Syötä **Summa**-kenttään summa pankkitilin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="61296-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="61296-130">Anna kredit-summat miinusmerkkisinä.</span><span class="sxs-lookup"><span data-stu-id="61296-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="61296-131">Anna debet-summat ilman miinusmerkkiä.</span><span class="sxs-lookup"><span data-stu-id="61296-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="61296-132">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="61296-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="61296-133">Valitse **Vastatilin nro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="61296-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="61296-134">Jos päiväkirjassa käytetyt vaihtokurssit eroavat **Valuutan vaihtokurssit** -ikkunan kursseista, syötä kolmas rivi vaihtokurssivoittoa tai -tappiota varten.</span><span class="sxs-lookup"><span data-stu-id="61296-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="61296-135">Valitse **KP-tili**-kentässä**Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="61296-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="61296-136">Syötä **Tilinro**-kenttään valuuttakurssivoittojen ja -tappioiden KP-tilin numero.</span><span class="sxs-lookup"><span data-stu-id="61296-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="61296-137">Syötä valuuttakurssivoitto tai -tappio **Summa**-kenttään. Syötä summa miinusmerkin kanssa, jos kyseessä on kredit, ja ilman miinusmerkkiä, jos kyseessä on debet.</span><span class="sxs-lookup"><span data-stu-id="61296-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="61296-138">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="61296-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="61296-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="61296-139">See Also</span></span>
[<span data-ttu-id="61296-140">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="61296-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="61296-141">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="61296-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="61296-142">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="61296-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="61296-143">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61296-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

