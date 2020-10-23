---
title: Eri valuutoissa olevien tapahtumien kohdistaminen| Microsoft Docs
description: Jos asiakkaan maksu vastaanotetaan eri valuuttana kuin myytäessä käytetty valuutta, voidaan kirjanpitotapahtumat kohdistaa useana valuuttana.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c11939306e56299347a5f80d9ccfbc35c22fe5aa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917024"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="a2637-103">Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa</span><span class="sxs-lookup"><span data-stu-id="a2637-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="a2637-104">Jos ostat toimittajalta yhdessä valuutassa ja maksat maksun toisessa valuutassa, maksu voidaan kohdistaa ostoon.</span><span class="sxs-lookup"><span data-stu-id="a2637-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="a2637-105">Ja jos asiakkaalle myydään yhdessä valuutassa ja maksu vastaanotetaan toisessa valuutassa, maksu voidaan kohdistaa myyntilaskuun.</span><span class="sxs-lookup"><span data-stu-id="a2637-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="a2637-106">Seuraavassa kuvataan, miten tämä määritetään toimittajatapahtumille **Ostojen ja ostovelkojen asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a2637-106">The following procedure describes how to set this up for vendor ledger entries on the **Purchases & Payables Setup** page.</span></span> <span data-ttu-id="a2637-107">Asetukset tehdään samoin kuin asiakastapahtumille **Myyntien ja myyntisaamisten asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a2637-107">The setup is similar for customer ledger entries on the **Sales & Receivables Setup** page.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="a2637-108">Toimittajatapahtumien kohdistamisen ottaminen käyttöön eri valuutoissa</span><span class="sxs-lookup"><span data-stu-id="a2637-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="a2637-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostojen ja ostovelkojen asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a2637-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="a2637-110">Valitse **Valuuttojen välinen kohdistus** -kentässä jokin seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="a2637-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="a2637-111">Asetus</span><span class="sxs-lookup"><span data-stu-id="a2637-111">Option</span></span> | <span data-ttu-id="a2637-112">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a2637-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="a2637-113">Ei yhtään</span><span class="sxs-lookup"><span data-stu-id="a2637-113">None</span></span> |<span data-ttu-id="a2637-114">Valuuttojen välistä kohdistusta ei sallita.</span><span class="sxs-lookup"><span data-stu-id="a2637-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="a2637-115">EMU</span><span class="sxs-lookup"><span data-stu-id="a2637-115">EMU</span></span> |<span data-ttu-id="a2637-116">EMU-valuuttojen välinen kohdistus sallitaan.</span><span class="sxs-lookup"><span data-stu-id="a2637-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="a2637-117">Kaikki</span><span class="sxs-lookup"><span data-stu-id="a2637-117">All</span></span> |<span data-ttu-id="a2637-118">Kaikkien valuuttojen välinen kohdistus sallitaan.</span><span class="sxs-lookup"><span data-stu-id="a2637-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="a2637-119">KP-tilien määrittäminen valuutan kohdistuksen pyöristyseroille</span><span class="sxs-lookup"><span data-stu-id="a2637-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="a2637-120">Jos eri valuutoissa olevia tapahtumia kohdistetaan, täytyy määrittää KP-tilit, jolle haluat kirjata pyöristyserot.</span><span class="sxs-lookup"><span data-stu-id="a2637-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a2637-121">Sinun on määritettävä pääkirjanpidon tilit, ennen kuin viimeistelet tehtävän.</span><span class="sxs-lookup"><span data-stu-id="a2637-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="a2637-122">Lisätietoja on kohdassa [Tietoja pääkirjanpidosta ja tilikartasta](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="a2637-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="a2637-123">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaan kirjausryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a2637-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a2637-124">Anna **Debet val. kohd. pyör. tili**- ja **Kredit val. kohd. pyör. tili** -kenttiin asianmukaiset pääkirjanpitotilit, joihin pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a2637-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="a2637-125">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajan kirjausryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a2637-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="a2637-126">Anna **Debet val. kohd. pyör. tili**- ja **Kredit val. kohd. pyör. tili** -kentissä pääkirjanpitotilit, joihin pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a2637-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a2637-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a2637-127">See Also</span></span>
[<span data-ttu-id="a2637-128">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="a2637-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="a2637-129">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="a2637-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="a2637-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a2637-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
