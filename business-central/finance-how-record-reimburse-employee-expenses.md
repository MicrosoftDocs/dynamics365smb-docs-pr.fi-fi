---
title: "Työntekijän liiketoimintaan liittyvien kulujen kirjaaminen ja hyvittäminen | Microsoft Docs"
description: "Hyvitä liiketoimintaan liittyväkulu kirjaamalla työntekijän kulut ensin yleisessä päiväkirjassa työntekijän tilille ja sitten maksu työntekijän tilille."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 604b8ee545269707ebcabd3712aee0d4daf253a8
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="78193-103">Työntekijöiden kulujen kirjaaminen ja hyvittäminen</span><span class="sxs-lookup"><span data-stu-id="78193-103">Record and Reimburse Employees' Expenses</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="78193-104"> tukee työntekijän tapahtumia samalla tavoin kuin toimittajien tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="78193-104"> supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="78193-105">Niinpä työntekijän kirjausryhmien avulla voidaan varmistaa, että työntekijätapahtumat kirjataan oikeille yleisen päiväkirjan tileille.</span><span class="sxs-lookup"><span data-stu-id="78193-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="78193-106">Työntekijätapahtumat voidaan kirjata vain paikallisena valuuttana.</span><span class="sxs-lookup"><span data-stu-id="78193-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="78193-107">Työntekijöille tehtävät hyvitysmaksut eivät tue alennuksia ja maksutoleransseja.</span><span class="sxs-lookup"><span data-stu-id="78193-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="78193-108">Jos työntekijät voivat käyttää omia varojaan liiketoiminnoissa, voit kirjata kulun työntekijän tilille.</span><span class="sxs-lookup"><span data-stu-id="78193-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="78193-109">Työntekijälle tehdään sitten hyvitys suorittamalla maksu työntekijän pankkitilille toimittajille tehtävien maksujen tavoin.</span><span class="sxs-lookup"><span data-stu-id="78193-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="78193-110">Työntekijän kulun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="78193-110">To record an employee's expense</span></span>
<span data-ttu-id="78193-111">Voit kirjat työntekijän kulut **Yleinen päiväkirja** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="78193-111">You post employees' expenses in the **General Journal** window.</span></span>
1. <span data-ttu-id="78193-112">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="78193-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="78193-113">Avaa liittyvä yleisen päiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="78193-113">Open the relevant general journal batch.</span></span> <span data-ttu-id="78193-114">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="78193-114">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="78193-115">Täytä tarvittaessa uuden päiväkirjarivin kentät.</span><span class="sxs-lookup"><span data-stu-id="78193-115">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="78193-116">Toista vaihe 3 kaikissa kuluissa, joita työntekijällä on.</span><span class="sxs-lookup"><span data-stu-id="78193-116">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="78193-117">Jos haluat antaa työntekijän pankkitilille useita kulurivejä yhden vastatilin rivin yläpuolelle, valitse erän rivillä **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="78193-117">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="78193-118">Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan kulujen täsmäyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="78193-118">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="78193-119">Kirjaa kulut työntekijän tilille valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="78193-119">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="78193-120">Hyvityksen tekeminen työntekijälle</span><span class="sxs-lookup"><span data-stu-id="78193-120">To reimburse an employee</span></span>
<span data-ttu-id="78193-121">Hyvitys tehdään työntekijöille kirjaamalla maksut heidän pankkitililleen **Maksupäiväkirja**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="78193-121">You reimburse employees by posting payments to their bank account in the **Payment Journal** window.</span></span>
1. <span data-ttu-id="78193-122">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="78193-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="78193-123">Avaa käsiteltävä maksupäiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="78193-123">Open the relevant payment journal batch.</span></span> <span data-ttu-id="78193-124">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="78193-124">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="78193-125">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="78193-125">Fill in the fields as necessary.</span></span> <span data-ttu-id="78193-126">Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="78193-126">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="78193-127">Vaihtoehtoisesti voit valita **Ehdota työntekijämaksuja**-toiminnon, joka lisää automaattisesti odottavat työntekijän hyvitysten päiväkirjarivit.</span><span class="sxs-lookup"><span data-stu-id="78193-127">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="78193-128">Rekisteröi hyvitys valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="78193-128">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="78193-129">Hyvitysten täsmäyttäminen työntekijätapahtumien kanssa</span><span class="sxs-lookup"><span data-stu-id="78193-129">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="78193-130">Voit kohdistaa työntekijämaksut niiden liittyviin avoimiin työntekijätapahtumiin liittyvien pankkitilitapahtumien perusteella samalla tavoin kuin toimittajan maksut. Voit tehdä tämän esimerkiksi **Maksujen täsmäytyskirjauskansio** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="78193-130">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example in the **Payment Reconciliation Journal** window, based on the related bank statement entries.</span></span> <span data-ttu-id="78193-131">Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="78193-131">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="78193-132">Vaihtoehtoisesti voit tehdä kohdistuksen manuaalisesti **Työntekijätapahtumat**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="78193-132">Alternatively, you can apply manually in the **Employee Ledger Entries** window.</span></span> <span data-ttu-id="78193-133">Lisätietoja on liittyvässä ohjeartikkelissa [Toimittajamaksujen täsmäyttäminen manuaalisesti](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="78193-133">For more information, see the related [Reconcile Vendor Payments Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="78193-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="78193-134">See Also</span></span>
[<span data-ttu-id="78193-135">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="78193-135">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="78193-136">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="78193-136">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="78193-137">Kirjausten peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="78193-137">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="78193-138">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="78193-138">Finance</span></span>](finance.md)  
<span data-ttu-id="78193-139">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="78193-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

