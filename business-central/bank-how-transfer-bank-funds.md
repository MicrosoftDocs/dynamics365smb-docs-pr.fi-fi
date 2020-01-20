---
title: Pankkivarojen siirtäminen| Microsoft Docs
description: Voit siirtää summia pankkitililtä toisille myös muissa valuutoissa kirjaamalla tapahtuman yleiseen päiväkirjaan.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 12/13/2019
ms.author: sgroespe
ms.openlocfilehash: 3618ad87377ebc47f183292207d2f25dc6c3ed34
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910418"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="42e15-103">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="42e15-103">Transfer Bank Funds</span></span>
<span data-ttu-id="42e15-104">Joskus on siirrettävä varoja yhdeltä pankkitililtä kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)] toiselle.</span><span class="sxs-lookup"><span data-stu-id="42e15-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to another.</span></span> <span data-ttu-id="42e15-105">Se tehdään kirjaamalla tapahtuma **Yleinen päiväkirja** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="42e15-105">To do this, you must post the a transaction on the **General Journal** page.</span></span> <span data-ttu-id="42e15-106">Tehtävä vaihtelee sen mukaan, käytetäänkö pankkitileillä samaa vai eri valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="42e15-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="42e15-107">Siirtojen kirjaaminen pankkitileillä, jotka käyttävät samaa valuuttakoodia</span><span class="sxs-lookup"><span data-stu-id="42e15-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="42e15-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="42e15-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="42e15-109">Täytä päiväkirjan rivillä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.</span><span class="sxs-lookup"><span data-stu-id="42e15-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="42e15-110">Valitse **Tilityyppi**-kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="42e15-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="42e15-111">Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="42e15-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="42e15-112">Syötä siirrettävä summa **Summa**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="42e15-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="42e15-113">Näytä kaikki käytettävissä olevat kentät valitsemalla **Näytä enemmän sarakkeita** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="42e15-113">Choose the **Show More Columns** action to view all available fields.</span></span>
7. <span data-ttu-id="42e15-114">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="42e15-114">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
8. <span data-ttu-id="42e15-115">Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="42e15-115">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
9. <span data-ttu-id="42e15-116">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="42e15-116">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="42e15-117">Siirtojen kirjaaminen pankkitileillä, joilla on eri valuuttakoodit</span><span class="sxs-lookup"><span data-stu-id="42e15-117">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="42e15-118">Voit siirtää varoja eri valuuttoja käyttävien pankkitilien välillä kirjaamalla kaksi yleisen päiväkirjan riviä.</span><span class="sxs-lookup"><span data-stu-id="42e15-118">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="42e15-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="42e15-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="42e15-120">Luo kaksi päiväkirjan riviä ja täytä **Kirjauspvm**- ja **Asiakirjan nro.** -kentät.</span><span class="sxs-lookup"><span data-stu-id="42e15-120">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="42e15-121">Valitse **Tyyppi**-kentän ensimmäisellä rivillä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="42e15-121">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="42e15-122">Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="42e15-122">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="42e15-123">Syötä **Summa**-kenttään summa pankkitilin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="42e15-123">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="42e15-124">Anna kredit-summat miinusmerkkisinä.</span><span class="sxs-lookup"><span data-stu-id="42e15-124">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="42e15-125">Anna debet-summat ilman miinusmerkkiä.</span><span class="sxs-lookup"><span data-stu-id="42e15-125">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="42e15-126">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="42e15-126">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="42e15-127">Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="42e15-127">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="42e15-128">Valitse **Tyyppi**-kentän toisella rivillä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="42e15-128">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="42e15-129">Valitse **Tilinro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="42e15-129">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="42e15-130">Syötä **Summa**-kenttään summa pankkitilin valuuttana.</span><span class="sxs-lookup"><span data-stu-id="42e15-130">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="42e15-131">Anna kredit-summat miinusmerkkisinä.</span><span class="sxs-lookup"><span data-stu-id="42e15-131">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="42e15-132">Anna debet-summat ilman miinusmerkkiä.</span><span class="sxs-lookup"><span data-stu-id="42e15-132">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="42e15-133">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="42e15-133">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="42e15-134">Valitse **Vastatilin nro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="42e15-134">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="42e15-135">Jos päiväkirjassa käytetyt vaihtokurssit eroavat **Valuutan vaihtokurssit** -sivun kursseista, syötä kolmas rivi vaihtokurssivoittoa tai -tappiota varten.</span><span class="sxs-lookup"><span data-stu-id="42e15-135">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="42e15-136">Valitse **KP-tili**-kentässä**Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="42e15-136">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="42e15-137">Syötä **Tilinro**-kenttään valuuttakurssivoittojen ja -tappioiden KP-tilin numero.</span><span class="sxs-lookup"><span data-stu-id="42e15-137">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="42e15-138">Syötä valuuttakurssivoitto tai -tappio **Summa**-kenttään. Syötä summa miinusmerkin kanssa, jos kyseessä on kredit, ja ilman miinusmerkkiä, jos kyseessä on debet.</span><span class="sxs-lookup"><span data-stu-id="42e15-138">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="42e15-139">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="42e15-139">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="42e15-140">Katso myös</span><span class="sxs-lookup"><span data-stu-id="42e15-140">See Also</span></span>
[<span data-ttu-id="42e15-141">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="42e15-141">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="42e15-142">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="42e15-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="42e15-143">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="42e15-143">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="42e15-144">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="42e15-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
