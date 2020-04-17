---
title: Työntekijän liiketoimintaan liittyvien kulujen kirjaaminen ja hyvittäminen | Microsoft Docs
description: Hyvitä liiketoimintaan liittyväkulu kirjaamalla työntekijän kulut ensin yleisessä päiväkirjassa työntekijän tilille ja sitten maksu työntekijän tilille.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 5f943006997e4735d4ec224957442f23e2af1324
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184074"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="2d1f4-103">Työntekijöiden kulujen kirjaaminen ja hyvittäminen</span><span class="sxs-lookup"><span data-stu-id="2d1f4-103">Record and Reimburse Employees' Expenses</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2d1f4-104">tukee työntekijän tapahtumia samalla tavoin kuin toimittajien tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="2d1f4-105">Niinpä työntekijän kirjausryhmien avulla voidaan varmistaa, että työntekijätapahtumat kirjataan oikeille yleisen päiväkirjan tileille.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="2d1f4-106">Työntekijätapahtumat voidaan kirjata vain paikallisena valuuttana.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="2d1f4-107">Työntekijöille tehtävät hyvitysmaksut eivät tue alennuksia ja maksutoleransseja.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="2d1f4-108">Jos työntekijät voivat käyttää omia varojaan liiketoiminnoissa, voit kirjata kulun työntekijän tilille.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="2d1f4-109">Työntekijälle tehdään sitten hyvitys suorittamalla maksu työntekijän pankkitilille toimittajille tehtävien maksujen tavoin.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="2d1f4-110">Työntekijän kulun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="2d1f4-110">To record an employee's expense</span></span>
<span data-ttu-id="2d1f4-111">Voit kirjat työntekijän kulut **Yleinen päiväkirja** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-111">You post employees' expenses on the **General Journal** page.</span></span>
1. <span data-ttu-id="2d1f4-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="2d1f4-113">Avaa liittyvä yleisen päiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-113">Open the relevant general journal batch.</span></span> <span data-ttu-id="2d1f4-114">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="2d1f4-114">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="2d1f4-115">Täytä tarvittaessa uuden päiväkirjarivin kentät.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-115">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="2d1f4-116">Toista vaihe 3 kaikissa kuluissa, joita työntekijällä on.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-116">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="2d1f4-117">Jos haluat antaa työntekijän pankkitilille useita kulurivejä yhden vastatilin rivin yläpuolelle, valitse erän rivillä **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-117">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="2d1f4-118">Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan kulujen täsmäyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-118">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="2d1f4-119">Kirjaa kulut työntekijän tilille valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-119">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="2d1f4-120">Hyvityksen tekeminen työntekijälle</span><span class="sxs-lookup"><span data-stu-id="2d1f4-120">To reimburse an employee</span></span>
<span data-ttu-id="2d1f4-121">Hyvitys tehdään työntekijöille kirjaamalla maksut heidän pankkitililleen **Maksupäiväkirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-121">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>
1. <span data-ttu-id="2d1f4-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="2d1f4-123">Avaa käsiteltävä maksupäiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-123">Open the relevant payment journal batch.</span></span> <span data-ttu-id="2d1f4-124">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="2d1f4-124">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="2d1f4-125">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-125">Fill in the fields as necessary.</span></span> <span data-ttu-id="2d1f4-126">Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="2d1f4-126">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="2d1f4-127">Vaihtoehtoisesti voit valita **Ehdota työntekijämaksuja**-toiminnon, joka lisää automaattisesti odottavat työntekijän hyvitysten päiväkirjarivit.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-127">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="2d1f4-128">Rekisteröi hyvitys valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-128">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="2d1f4-129">Hyvitysten täsmäyttäminen työntekijätapahtumien kanssa</span><span class="sxs-lookup"><span data-stu-id="2d1f4-129">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="2d1f4-130">Voit kohdistaa työntekijämaksut niiden liittyviin avoimiin työntekijätapahtumiin liittyvien pankkitilitapahtumien perusteella samalla tavoin kuin toimittajan maksut. Voit tehdä tämän esimerkiksi **Maksujen täsmäytyskirjauskansio** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-130">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="2d1f4-131">Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="2d1f4-131">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="2d1f4-132">Vaihtoehtoisesti voit tehdä kohdistuksen manuaalisesti **Työntekijätapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="2d1f4-132">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="2d1f4-133">Lisätietoja on liittyvässä kohdassa [Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista](payables-how-apply-purchase-transactions-manually.md)</span><span class="sxs-lookup"><span data-stu-id="2d1f4-133">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d1f4-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2d1f4-134">See Also</span></span>
[<span data-ttu-id="2d1f4-135">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="2d1f4-135">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="2d1f4-136">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2d1f4-136">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="2d1f4-137">Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen</span><span class="sxs-lookup"><span data-stu-id="2d1f4-137">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="2d1f4-138">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="2d1f4-138">Finance</span></span>](finance.md)  
<span data-ttu-id="2d1f4-139">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2d1f4-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
