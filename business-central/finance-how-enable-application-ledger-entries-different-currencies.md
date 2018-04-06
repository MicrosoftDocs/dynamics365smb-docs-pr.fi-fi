---
title: Eri valuutoissa olevien tapahtumien kohdistaminen| Microsoft Docs
description: "Jos asiakkaan maksu vastaanotetaan eri valuuttana kuin myytäessä käytetty valuutta, voidaan kirjanpitotapahtumat kohdistaa useana valuuttana."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 960ae581a3f933c6e9c2ed5183944ddf62ca5965
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="06e3c-103">Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa</span><span class="sxs-lookup"><span data-stu-id="06e3c-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="06e3c-104">Jos ostat toimittajalta yhdessä valuutassa ja maksat maksun toisessa valuutassa, maksu voidaan kohdistaa ostoon.</span><span class="sxs-lookup"><span data-stu-id="06e3c-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="06e3c-105">Ja jos asiakkaalle myydään yhdessä valuutassa ja maksu vastaanotetaan toisessa valuutassa, maksu voidaan kohdistaa myyntilaskuun.</span><span class="sxs-lookup"><span data-stu-id="06e3c-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="06e3c-106">Seuraavassa kuvataan, miten tämä määritetään toimittajatapahtumille **Ostojen ja ostovelkojen asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="06e3c-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="06e3c-107">Asetukset tehdään samoin kuin asiakastapahtumille **Myyntien ja myyntisaamisten asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="06e3c-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="06e3c-108">Toimittajatapahtumien kohdistamisen ottaminen käyttöön eri valuutoissa</span><span class="sxs-lookup"><span data-stu-id="06e3c-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="06e3c-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Ostojen ostovelkojen asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="06e3c-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="06e3c-110">Valitse **Valuuttojen välinen kohdistus** -kentässä jokin seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="06e3c-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="06e3c-111">Asetus</span><span class="sxs-lookup"><span data-stu-id="06e3c-111">Option</span></span> | <span data-ttu-id="06e3c-112">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="06e3c-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="06e3c-113">Ei yhtään</span><span class="sxs-lookup"><span data-stu-id="06e3c-113">None</span></span> |<span data-ttu-id="06e3c-114">Valuuttojen välistä kohdistusta ei sallita.</span><span class="sxs-lookup"><span data-stu-id="06e3c-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="06e3c-115">EMU</span><span class="sxs-lookup"><span data-stu-id="06e3c-115">EMU</span></span> |<span data-ttu-id="06e3c-116">EMU-valuuttojen välinen kohdistus sallitaan.</span><span class="sxs-lookup"><span data-stu-id="06e3c-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="06e3c-117">Kaikki</span><span class="sxs-lookup"><span data-stu-id="06e3c-117">All</span></span> |<span data-ttu-id="06e3c-118">Kaikkien valuuttojen välinen kohdistus sallitaan.</span><span class="sxs-lookup"><span data-stu-id="06e3c-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="06e3c-119">KP-tilien määrittäminen valuutan kohdistuksen pyöristyseroille</span><span class="sxs-lookup"><span data-stu-id="06e3c-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="06e3c-120">Jos eri valuutoissa olevia tapahtumia kohdistetaan, täytyy määrittää KP-tilit, jolle haluat kirjata pyöristyserot.</span><span class="sxs-lookup"><span data-stu-id="06e3c-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="06e3c-121">Sinun on määritettävä pääkirjanpidon tilit, ennen kuin viimeistelet tehtävän.</span><span class="sxs-lookup"><span data-stu-id="06e3c-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="06e3c-122">Lisätietoja on kohdassa [Tietoja pääkirjanpidosta ja tilikartasta](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="06e3c-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="06e3c-123">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaan kirjausryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="06e3c-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="06e3c-124">Anna **Debet val. kohd. pyör. tili**- ja **Kredit val. kohd. pyör. tili** -kenttiin asianmukaiset pääkirjanpitotilit, joihin pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="06e3c-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="06e3c-125">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Toimittajan kirjausryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="06e3c-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="06e3c-126">Anna **Debet val. kohd. pyör. tili**- ja **Kredit val. kohd. pyör. tili** -kentissä pääkirjanpitotilit, joihin pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="06e3c-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="06e3c-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="06e3c-127">See Also</span></span>
[<span data-ttu-id="06e3c-128">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="06e3c-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="06e3c-129">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="06e3c-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="06e3c-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="06e3c-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

