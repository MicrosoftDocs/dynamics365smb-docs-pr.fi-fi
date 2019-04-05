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
ms.date: 11/27/2018
ms.author: sgroespe
ms.openlocfilehash: 5932823e2ed18e2e2c61317d2a23a635ee66c609
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795337"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="43414-103">Työntekijöiden kulujen kirjaaminen ja hyvittäminen</span><span class="sxs-lookup"><span data-stu-id="43414-103">Record and Reimburse Employees' Expenses</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="43414-104">tukee työntekijän tapahtumia samalla tavoin kuin toimittajien tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="43414-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="43414-105">Niinpä työntekijän kirjausryhmien avulla voidaan varmistaa, että työntekijätapahtumat kirjataan oikeille yleisen päiväkirjan tileille.</span><span class="sxs-lookup"><span data-stu-id="43414-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="43414-106">Työntekijätapahtumat voidaan kirjata vain paikallisena valuuttana.</span><span class="sxs-lookup"><span data-stu-id="43414-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="43414-107">Työntekijöille tehtävät hyvitysmaksut eivät tue alennuksia ja maksutoleransseja.</span><span class="sxs-lookup"><span data-stu-id="43414-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="43414-108">Jos työntekijät voivat käyttää omia varojaan liiketoiminnoissa, voit kirjata kulun työntekijän tilille.</span><span class="sxs-lookup"><span data-stu-id="43414-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="43414-109">Työntekijälle tehdään sitten hyvitys suorittamalla maksu työntekijän pankkitilille toimittajille tehtävien maksujen tavoin.</span><span class="sxs-lookup"><span data-stu-id="43414-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="43414-110">Työntekijän kulun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="43414-110">To record an employee's expense</span></span>
<span data-ttu-id="43414-111">Voit kirjat työntekijän kulut **Yleinen päiväkirja** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="43414-111">You post employees' expenses on the **General Journal** page.</span></span>
1. <span data-ttu-id="43414-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="43414-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="43414-113">Avaa liittyvä yleisen päiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="43414-113">Open the relevant general journal batch.</span></span> <span data-ttu-id="43414-114">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="43414-114">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="43414-115">Täytä tarvittaessa uuden päiväkirjarivin kentät.</span><span class="sxs-lookup"><span data-stu-id="43414-115">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="43414-116">Toista vaihe 3 kaikissa kuluissa, joita työntekijällä on.</span><span class="sxs-lookup"><span data-stu-id="43414-116">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="43414-117">Jos haluat antaa työntekijän pankkitilille useita kulurivejä yhden vastatilin rivin yläpuolelle, valitse erän rivillä **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="43414-117">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="43414-118">Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan kulujen täsmäyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="43414-118">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="43414-119">Kirjaa kulut työntekijän tilille valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="43414-119">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="43414-120">Hyvityksen tekeminen työntekijälle</span><span class="sxs-lookup"><span data-stu-id="43414-120">To reimburse an employee</span></span>
<span data-ttu-id="43414-121">Hyvitys tehdään työntekijöille kirjaamalla maksut heidän pankkitililleen **Maksupäiväkirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="43414-121">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>
1. <span data-ttu-id="43414-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="43414-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="43414-123">Avaa käsiteltävä maksupäiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="43414-123">Open the relevant payment journal batch.</span></span> <span data-ttu-id="43414-124">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="43414-124">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="43414-125">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="43414-125">Fill in the fields as necessary.</span></span> <span data-ttu-id="43414-126">Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="43414-126">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="43414-127">Vaihtoehtoisesti voit valita **Ehdota työntekijämaksuja**-toiminnon, joka lisää automaattisesti odottavat työntekijän hyvitysten päiväkirjarivit.</span><span class="sxs-lookup"><span data-stu-id="43414-127">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="43414-128">Rekisteröi hyvitys valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="43414-128">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="43414-129">Hyvitysten täsmäyttäminen työntekijätapahtumien kanssa</span><span class="sxs-lookup"><span data-stu-id="43414-129">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="43414-130">Voit kohdistaa työntekijämaksut niiden liittyviin avoimiin työntekijätapahtumiin liittyvien pankkitilitapahtumien perusteella samalla tavoin kuin toimittajan maksut. Voit tehdä tämän esimerkiksi **Maksujen täsmäytyskirjauskansio** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="43414-130">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="43414-131">Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="43414-131">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="43414-132">Vaihtoehtoisesti voit tehdä kohdistuksen manuaalisesti **Työntekijätapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="43414-132">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="43414-133">Lisätietoja on liittyvässä kohdassa [Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista](payables-how-apply-purchase-transactions-manually.md)</span><span class="sxs-lookup"><span data-stu-id="43414-133">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="43414-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="43414-134">See Also</span></span>
[<span data-ttu-id="43414-135">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="43414-135">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="43414-136">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="43414-136">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="43414-137">Kirjausten peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="43414-137">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="43414-138">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="43414-138">Finance</span></span>](finance.md)  
<span data-ttu-id="43414-139">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43414-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
