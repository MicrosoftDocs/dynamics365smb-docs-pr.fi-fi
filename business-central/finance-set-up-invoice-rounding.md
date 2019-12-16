---
title: Laskun pyöristyksen määrittäminen | Microsoft Docs
description: Voit pyöristää laskujen summat, kun luot laskuja. Paikalliset määräykset tai tavat voivat lisäksi edellyttää laskun pyöristystä tietyllä tavalla (esimerkiksi niin, että summa on jaollinen luvulla 0,05).
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: bb114e6ea550ca5cc453c8319e72da5b11cec6e8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882468"
---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="ab854-104">Laskun pyöristyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ab854-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="ab854-105">Jos laskujen summat on pyöristettävä laskuja luotaessa, voit käyttää automaattista pyöristystoimintoa.</span><span class="sxs-lookup"><span data-stu-id="ab854-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="ab854-106">Kun lasku pyöristetään, lisätään lisärivi, joka sisältää pyöristyssumman ja joka kirjataan muiden laskurivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="ab854-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="ab854-107">Paikalliset määräykset tai tavat saattavat vaatia laskun pyöristystä tietyllä tavalla (esimerkiksi niin, että summa on jaollinen luvulla 0,05).</span><span class="sxs-lookup"><span data-stu-id="ab854-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  

<span data-ttu-id="ab854-108">Jos haluat käyttää automaattista laskun pyöristystä, sinun on</span><span class="sxs-lookup"><span data-stu-id="ab854-108">To use automatic invoice rounding, you must:</span></span>  

* <span data-ttu-id="ab854-109">määritettävä kirjanpitotilit, joille pyöristyserot kirjataan</span><span class="sxs-lookup"><span data-stu-id="ab854-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="ab854-110">määritettävä laskujen pyöristyksen säännöt paikallista valuuttaa ja ulkomaanvaluuttaa varten</span><span class="sxs-lookup"><span data-stu-id="ab854-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="ab854-111">aktivoitava toiminto.</span><span class="sxs-lookup"><span data-stu-id="ab854-111">Activate the function.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ab854-112">Laskun pyöristysominaisuuksien lisäksi laskujen summien pyöristyksessä voi käyttää yksikkösumman ja summan pyöristysominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ab854-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="ab854-113">KP-tilien määrittäminen laskun kohdistuksen pyöristyseroille</span><span class="sxs-lookup"><span data-stu-id="ab854-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="ab854-114">Kun haluat käyttää ohjelman automaattista laskunpyöristystoimintoa, sinun täytyy määrittää se KP-tili (tai ne KP-tilit), joille pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="ab854-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="ab854-115">Sitä ennen sinun täytyy luoda tuotteen ALV-kirjausryhmät.</span><span class="sxs-lookup"><span data-stu-id="ab854-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="ab854-116">Lisätietoja on kohdassa [ALV:n määrittäminen](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="ab854-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="ab854-117">KP-tilien määrittäminen laskun kohdistuksen pyöristyseroille</span><span class="sxs-lookup"><span data-stu-id="ab854-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="ab854-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tilikartta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab854-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab854-119">Määritä tili **Tilikartta**-sivulla ja anna sen nimeksi esimerkiksi **Laskun pyöristys**.</span><span class="sxs-lookup"><span data-stu-id="ab854-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ab854-120">käyttää tätä tilin nimeä pyöristetyissä laskuissa.</span><span class="sxs-lookup"><span data-stu-id="ab854-120">will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="ab854-121">Valitse **Veron ALV-kirjausryhmä**- tai **Tuotteen ALV-kirjausryhmä** -kentässä pyöristettyjen summien kirjausryhmä sen mukaan, onko kyseessä ALV- vai myyntivero.</span><span class="sxs-lookup"><span data-stu-id="ab854-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="ab854-122">Voit halutessasi määrittää uuden ryhmäkoodin laskun pyöristystä varten.</span><span class="sxs-lookup"><span data-stu-id="ab854-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="ab854-123">Jätä **Yleinen kirjaustyyppi**- ja joko **Liiketoiminnan veron kirjausryhmä**- tai **Liiketoiminnan ALV-kirjausryhmä** -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="ab854-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

<span data-ttu-id="ab854-124">Voit nyt määrittää laskun pyöristystilin kirjausryhmille **Toimittajan kirjausryhmät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ab854-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="ab854-125">Ulkomaan valuutan ja paikallisen valuutan pyöristämisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ab854-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="ab854-126">Ulkomaanvaluutan ja paikallisen valuutan pyöristämissäännöt on määritettävä ennen automaattisen pyöristystoiminnon käyttöä.</span><span class="sxs-lookup"><span data-stu-id="ab854-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="ab854-127">Ulkomaan valuuttojen pyöristyssääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ab854-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="ab854-128">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Valuutat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab854-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab854-129">Avaa **Valuutan kortti** valitsemalla **Valuutat**-sivulla ulkomaanvaluutta ja täytä sitten **Summan pyöristystarkkuus**-, **Yksikkösumman pyöristystarkkuus**-, **Laskun pyöristystarkkuus**- ja **Laskun pyöristystyyppi** -kentät.</span><span class="sxs-lookup"><span data-stu-id="ab854-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>

### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="ab854-130">Paikallisen valuutan pyöristyssääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ab854-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="ab854-131">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon määritykset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab854-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab854-132">Täytä **Pääkirjanpidon asetukset** -sivun **Yleiset**-pikavälilehdessä **Laskun pyöristystarkkuus**- ja **Laskun pyöristystyyppi** -kentät.</span><span class="sxs-lookup"><span data-stu-id="ab854-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="ab854-133">Laskun pyöristystoiminnon aktivointi</span><span class="sxs-lookup"><span data-stu-id="ab854-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="ab854-134">Laskun pyöristystoiminto on aktivoitava, jotta voit varmistaa myynti- ja ostolaskujen automaattisen pyöristyksen.</span><span class="sxs-lookup"><span data-stu-id="ab854-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="ab854-135">Voit aktivoida laskunpyöristyksen erikseen myynti- ja ostolaskuille.</span><span class="sxs-lookup"><span data-stu-id="ab854-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="ab854-136">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntien ja myyntisaamisten asetukset** tai **Ostojen ostovelkojen asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab854-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab854-137">Valitse **Yleiset**-pikavälilehdessä **Laskun pyöristys** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="ab854-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ab854-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ab854-138">See Also</span></span>  
[<span data-ttu-id="ab854-139">Myynnin laskutus</span><span class="sxs-lookup"><span data-stu-id="ab854-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="ab854-140">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="ab854-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)
