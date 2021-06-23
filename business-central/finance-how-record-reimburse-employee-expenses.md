---
title: Työntekijän liiketoimintaan liittyvien kulujen kirjaaminen ja hyvittäminen
description: Hyvitä liiketoimintaan liittyväkulu kirjaamalla työntekijän kulut ensin yleisessä päiväkirjassa työntekijän tilille ja sitten maksu työntekijän tilille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184397"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="d02cb-103">Työntekijöiden kulujen kirjaaminen ja hyvittäminen</span><span class="sxs-lookup"><span data-stu-id="d02cb-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d02cb-104">tukee työntekijöiden tapahtumia samalla tavoin kuin toimittajien tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="d02cb-104">supports transactions for employees in a similar way as for vendors.</span></span> <span data-ttu-id="d02cb-105">Niinpä työntekijän kirjausryhmien avulla voidaan varmistaa, että työntekijätapahtumat kirjataan oikeille yleisen päiväkirjan tileille.</span><span class="sxs-lookup"><span data-stu-id="d02cb-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="d02cb-106">Työntekijätapahtumat voidaan kirjata vain paikallisena valuuttana.</span><span class="sxs-lookup"><span data-stu-id="d02cb-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="d02cb-107">Työntekijöille tehtävät hyvitysmaksut eivät tue alennuksia ja maksutoleransseja.</span><span class="sxs-lookup"><span data-stu-id="d02cb-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="d02cb-108">Jos työntekijät voivat käyttää omia varojaan liiketoiminnoissa, voit kirjata kulun työntekijän tilille.</span><span class="sxs-lookup"><span data-stu-id="d02cb-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="d02cb-109">Työntekijälle tehdään sitten hyvitys suorittamalla maksu työntekijän pankkitilille toimittajille tehtävien maksujen tavoin.</span><span class="sxs-lookup"><span data-stu-id="d02cb-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="d02cb-110">Tässä artikkelissa käsitellään kulujen kirjaamista kirjoihin ja niiden hyvittämistä työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="d02cb-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="d02cb-111">Organisaatiossa voi olla portaali tai sovellus, jossa työntekijät voivat lähettää kuluraportit.</span><span class="sxs-lookup"><span data-stu-id="d02cb-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

<span data-ttu-id="d02cb-112">Joustavana [!INCLUDE [prod_short](includes/prod_short.md)] sopii moniin erilaisiin käytäntöihin.</span><span class="sxs-lookup"><span data-stu-id="d02cb-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexible enough to suit many different practices.</span></span> <span data-ttu-id="d02cb-113">Käytettävät tilinumerot määräytyvät organisaation määritysten ja prosessien mukaan.</span><span class="sxs-lookup"><span data-stu-id="d02cb-113">The exact account numbers to use depends on your organization's configuration and processes.</span></span>  

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="d02cb-114">Työntekijän kulun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="d02cb-114">To record an employee's expense</span></span>

<span data-ttu-id="d02cb-115">Voit kirjat työntekijän kulut **Yleinen päiväkirja** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d02cb-115">You post employees' expenses on the **General Journal** page.</span></span>

1. <span data-ttu-id="d02cb-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d02cb-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d02cb-117">Avaa liittyvä yleisen päiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="d02cb-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="d02cb-118">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="d02cb-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="d02cb-119">Täytä tarvittaessa uuden päiväkirjarivin kentät.</span><span class="sxs-lookup"><span data-stu-id="d02cb-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="d02cb-120">Toista vaihe 3 kaikissa kuluissa, joita työntekijällä on.</span><span class="sxs-lookup"><span data-stu-id="d02cb-120">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="d02cb-121">Jos haluat antaa työntekijän pankkitilille useita kulurivejä yhden vastatilin rivin yläpuolelle, valitse erän rivillä **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d02cb-121">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="d02cb-122">Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan kulujen täsmäyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="d02cb-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="d02cb-123">Kirjaa kulut työntekijän tilille valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d02cb-123">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="d02cb-124">Hyvityksen tekeminen työntekijälle</span><span class="sxs-lookup"><span data-stu-id="d02cb-124">To reimburse an employee</span></span>

<span data-ttu-id="d02cb-125">Hyvitys tehdään työntekijöille kirjaamalla maksut heidän pankkitililleen **Maksupäiväkirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d02cb-125">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>  

1. <span data-ttu-id="d02cb-126">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d02cb-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="d02cb-127">Avaa käsiteltävä maksupäiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="d02cb-127">Open the relevant payment journal batch.</span></span> <span data-ttu-id="d02cb-128">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="d02cb-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="d02cb-129">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="d02cb-129">Fill in the fields as necessary.</span></span> <span data-ttu-id="d02cb-130">Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="d02cb-130">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="d02cb-131">Vaihtoehtoisesti voit valita **Ehdota työntekijämaksuja**-toiminnon, joka lisää automaattisesti odottavat työntekijän hyvitysten päiväkirjarivit.</span><span class="sxs-lookup"><span data-stu-id="d02cb-131">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="d02cb-132">Rekisteröi hyvitys valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d02cb-132">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="d02cb-133">Hyvitysten täsmäyttäminen työntekijätapahtumien kanssa</span><span class="sxs-lookup"><span data-stu-id="d02cb-133">To reconcile reimbursements with employee ledger entries</span></span>

<span data-ttu-id="d02cb-134">Voit kohdistaa työntekijämaksut niiden liittyviin avoimiin työntekijätapahtumiin liittyvien pankkitilitapahtumien perusteella samalla tavoin kuin toimittajan maksut. Voit tehdä tämän esimerkiksi **Maksujen täsmäytyskirjauskansio** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d02cb-134">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="d02cb-135">Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="d02cb-135">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="d02cb-136">Vaihtoehtoisesti voit tehdä kohdistuksen manuaalisesti **Työntekijätapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d02cb-136">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="d02cb-137">Lisätietoja on liittyvässä kohdassa [Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista](payables-how-apply-purchase-transactions-manually.md)</span><span class="sxs-lookup"><span data-stu-id="d02cb-137">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d02cb-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d02cb-138">See Also</span></span>

[<span data-ttu-id="d02cb-139">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="d02cb-139">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="d02cb-140">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="d02cb-140">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="d02cb-141">Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen</span><span class="sxs-lookup"><span data-stu-id="d02cb-141">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="d02cb-142">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="d02cb-142">Finance</span></span>](finance.md)  
<span data-ttu-id="d02cb-143">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d02cb-143">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]