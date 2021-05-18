---
title: Siirrä pankkivarat
description: Voit siirtää summia pankkitililtä toisille myös muissa valuutoissa kirjaamalla tapahtuman yleiseen päiväkirjaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985385"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="bff83-103">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="bff83-103">Transfer Bank Funds</span></span>

<span data-ttu-id="bff83-104">Joskus on siirrettävä varoja yhdeltä pankkitililtä kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] toiselle.</span><span class="sxs-lookup"><span data-stu-id="bff83-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="bff83-105">Se tehdään kirjaamalla tapahtuma **Yleinen päiväkirja** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="bff83-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="bff83-106">Tehtävä vaihtelee sen mukaan, käytetäänkö pankkitileillä samaa vai eri valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="bff83-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="bff83-107">Siirtojen kirjaaminen pankkitileillä, jotka käyttävät samaa valuuttakoodia</span><span class="sxs-lookup"><span data-stu-id="bff83-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="bff83-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="bff83-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="bff83-109">Täytä päiväkirjan rivillä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.</span><span class="sxs-lookup"><span data-stu-id="bff83-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="bff83-110">Valitse **Tilityyppi**-kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="bff83-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="bff83-111">Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="bff83-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="bff83-112">Syötä siirrettävä summa **Summa**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="bff83-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="bff83-113">Seuraavaksi sinun täytyy määrittää vastatili.</span><span class="sxs-lookup"><span data-stu-id="bff83-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="bff83-114">Jos liittyvät kentät eivät ole näkyvissä, valitse **Näytä lisää sarakkeita** -toiminto, jolloin kaikki käytettävissä olevat kentät tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="bff83-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="bff83-115">Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="bff83-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="bff83-116">Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="bff83-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="bff83-117">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="bff83-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="bff83-118">Siirtojen kirjaaminen pankkitileillä, joilla on eri valuuttakoodit</span><span class="sxs-lookup"><span data-stu-id="bff83-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="bff83-119">Voit siirtää varoja eri valuuttoja käyttävien pankkitilien välillä kirjaamalla kaksi yleisen päiväkirjan riviä.</span><span class="sxs-lookup"><span data-stu-id="bff83-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="bff83-120">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="bff83-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="bff83-121">Luo kaksi päiväkirjan riviä ja täytä **Kirjauspvm**- ja **Asiakirjan nro.** -kentät.</span><span class="sxs-lookup"><span data-stu-id="bff83-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="bff83-122">Valitse **Tyyppi**-kentän ensimmäisellä rivillä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="bff83-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="bff83-123">Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="bff83-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="bff83-124">Syötä **Summa**-kenttään summa pankkitilin valuuttana vähennysmerkin kanssa tai ilman sitä.</span><span class="sxs-lookup"><span data-stu-id="bff83-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="bff83-125">Jos summan edessä ei ole merkkiä, se on debet-summa. Muussa tapauksessa kyseessä on kredit-summa.</span><span class="sxs-lookup"><span data-stu-id="bff83-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bff83-126">Jotkin yritykset siirtävät tilit mieluiten erillisillä päiväkirjariveillä.</span><span class="sxs-lookup"><span data-stu-id="bff83-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="bff83-127">Joissakin yrityksissä kirjataan kaikki yhdelle päiväkirjariville vastatilin avulla.</span><span class="sxs-lookup"><span data-stu-id="bff83-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="bff83-128">Varmista käytäntö tarvittaessa paikalliselta asiantuntijalta.</span><span class="sxs-lookup"><span data-stu-id="bff83-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="bff83-129">Jos yrityksessä halutaan käyttää vastatiliä, määritä **Vastatilin tyyppi** -kentän arvoksi **Pankkitili** ja määritä sitten **Vastatilin nro** -kentän arvoksi se pankkitili, jolle varat halutaan siirtää.</span><span class="sxs-lookup"><span data-stu-id="bff83-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="bff83-130">Siirry sitten vaiheeseen 9 tai 10.</span><span class="sxs-lookup"><span data-stu-id="bff83-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="bff83-131">Jos yrityksessä halutaan käyttää erillistä päiväkirjariviä, siirry seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="bff83-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="bff83-132">Valitse **Tyyppi**-kentän toisella rivillä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="bff83-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="bff83-133">Valitse **Tilinro**-kentässä pankkitili, johon haluat siirtää varat.</span><span class="sxs-lookup"><span data-stu-id="bff83-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="bff83-134">Syötä **Summa**-kenttään summa pankkitilin valuuttana vähennysmerkin kanssa tai ilman sitä.</span><span class="sxs-lookup"><span data-stu-id="bff83-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="bff83-135">Jos summan edessä ei ole merkkiä, se on debet-summa. Muussa tapauksessa kyseessä on kredit-summa.</span><span class="sxs-lookup"><span data-stu-id="bff83-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="bff83-136">Jos päiväkirjassa käytetyt vaihtokurssit eroavat **Valuutan vaihtokurssit** -sivun kursseista, syötä uusi päiväkirjarivi vaihtokurssivoittoa tai -tappiota varten.</span><span class="sxs-lookup"><span data-stu-id="bff83-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="bff83-137">Valitse **KP-tili**-kentässä **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="bff83-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="bff83-138">Syötä **Tilinro**-kenttään valuuttakurssivoittojen ja -tappioiden KP-tilin numero.</span><span class="sxs-lookup"><span data-stu-id="bff83-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="bff83-139">Syötä valuuttakurssin voitto tai tappio **Summa**-kenttään miinusmerkillä kanssa tai ilman sitä.</span><span class="sxs-lookup"><span data-stu-id="bff83-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="bff83-140">Jos summan edessä ei ole merkkiä, se on debet-summa. Muussa tapauksessa kyseessä on kredit-summa.</span><span class="sxs-lookup"><span data-stu-id="bff83-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="bff83-141">Kirjaa päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="bff83-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="bff83-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="bff83-142">See Also</span></span>

[<span data-ttu-id="bff83-143">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="bff83-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="bff83-144">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bff83-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="bff83-145">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="bff83-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="bff83-146">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bff83-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]