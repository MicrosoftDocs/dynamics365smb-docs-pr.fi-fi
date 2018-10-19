---
title: "Laskun pyöristyksen määrittäminen | Microsoft Docs"
description: "Voit pyöristää laskujen summat, kun luot laskuja. Paikalliset määräykset tai tavat voivat lisäksi edellyttää laskun pyöristystä tietyllä tavalla (esimerkiksi niin, että summa on jaollinen luvulla 0,05)."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d21a1b2f199c5d53e3879bf3a0866f39e904b873
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="8a958-104">Laskun pyöristyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8a958-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="8a958-105">Jos laskujen summat on pyöristettävä laskuja luotaessa, voit käyttää automaattista pyöristystoimintoa.</span><span class="sxs-lookup"><span data-stu-id="8a958-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="8a958-106">Kun lasku pyöristetään, lisätään lisärivi, joka sisältää pyöristyssumman ja joka kirjataan muiden laskurivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="8a958-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="8a958-107">Paikalliset määräykset tai tavat saattavat vaatia laskun pyöristystä tietyllä tavalla (esimerkiksi niin, että summa on jaollinen luvulla 0,05).</span><span class="sxs-lookup"><span data-stu-id="8a958-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  

<span data-ttu-id="8a958-108">Jos haluat käyttää automaattista laskun pyöristystä, sinun on</span><span class="sxs-lookup"><span data-stu-id="8a958-108">To use automatic invoice rounding, you must:</span></span>  

* <span data-ttu-id="8a958-109">määritettävä kirjanpitotilit, joille pyöristyserot kirjataan</span><span class="sxs-lookup"><span data-stu-id="8a958-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="8a958-110">määritettävä laskujen pyöristyksen säännöt paikallista valuuttaa ja ulkomaanvaluuttaa varten</span><span class="sxs-lookup"><span data-stu-id="8a958-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="8a958-111">aktivoitava toiminto.</span><span class="sxs-lookup"><span data-stu-id="8a958-111">Activate the function.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8a958-112">Laskun pyöristysominaisuuksien lisäksi laskujen summien pyöristyksessä voi käyttää yksikkösumman ja summan pyöristysominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="8a958-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="8a958-113">KP-tilien määrittäminen laskun kohdistuksen pyöristyseroille</span><span class="sxs-lookup"><span data-stu-id="8a958-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="8a958-114">Kun haluat käyttää ohjelman automaattista laskunpyöristystoimintoa, sinun täytyy määrittää se KP-tili (tai ne KP-tilit), joille pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="8a958-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="8a958-115">Sitä ennen sinun täytyy luoda tuotteen ALV-kirjausryhmät.</span><span class="sxs-lookup"><span data-stu-id="8a958-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="8a958-116">Lisätietoja on kohdassa [ALV:n määrittäminen](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="8a958-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="8a958-117">KP-tilien määrittäminen laskun kohdistuksen pyöristyseroille</span><span class="sxs-lookup"><span data-stu-id="8a958-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="8a958-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8a958-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8a958-119">Luo tili **Tilikartta**-ikkunassa ja anna sen nimeksi esimerkiksi **Laskun pyöristys**.</span><span class="sxs-lookup"><span data-stu-id="8a958-119">In the **Chart of Accounts** window, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8a958-120">käyttää tätä tilin nimeä pyöristetyissä laskuissa.</span><span class="sxs-lookup"><span data-stu-id="8a958-120">will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="8a958-121">Valitse **Veron ALV-kirjausryhmä**- tai **Tuotteen ALV-kirjausryhmä** -kentässä pyöristettyjen summien kirjausryhmä sen mukaan, onko kyseessä ALV- vai myyntivero.</span><span class="sxs-lookup"><span data-stu-id="8a958-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="8a958-122">Voit halutessasi määrittää uuden ryhmäkoodin laskun pyöristystä varten.</span><span class="sxs-lookup"><span data-stu-id="8a958-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="8a958-123">Jätä **Yleinen kirjaustyyppi**- ja joko **Liiketoiminnan veron kirjausryhmä**- tai **Liiketoiminnan ALV-kirjausryhmä** -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="8a958-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

<span data-ttu-id="8a958-124">Voit nyt määrittää laskun pyöristystilin kirjausryhmille **Toimittajan kirjausryhmät** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="8a958-124">Now you can assign the invoice rounding account to posting groups in the **Vendor Posting Groups** window.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="8a958-125">Ulkomaan valuutan ja paikallisen valuutan pyöristämisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8a958-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="8a958-126">Ulkomaanvaluutan ja paikallisen valuutan pyöristämissäännöt on määritettävä ennen automaattisen pyöristystoiminnon käyttöä.</span><span class="sxs-lookup"><span data-stu-id="8a958-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="8a958-127">Ulkomaan valuuttojen pyöristyssääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8a958-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="8a958-128">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8a958-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8a958-129">Avaa **Valuutan kortti** valitsemalla **Valuutat**-ikkunassa ulkomaanvaluutta ja täytä sitten **Summan pyöristystarkkuus**-, **Yksikkösumman pyöristystarkkuus**-, **Laskun pyöristystarkkuus**- ja **Laskun pyöristystyyppi** -kentät.</span><span class="sxs-lookup"><span data-stu-id="8a958-129">In the **Currencies** window, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>

### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="8a958-130">Paikallisen valuutan pyöristyssääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8a958-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="8a958-131">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8a958-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8a958-132">Täytä **Pääkirjanpidon asetukset** -ikkunan **Yleiset**-pikavälilehdessä **Laskun pyöristystarkkuus**- ja **Laskun pyöristystyyppi** -kentät.</span><span class="sxs-lookup"><span data-stu-id="8a958-132">In the **General Ledger Setup** window, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="8a958-133">Laskun pyöristystoiminnon aktivointi</span><span class="sxs-lookup"><span data-stu-id="8a958-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="8a958-134">Laskun pyöristystoiminto on aktivoitava, jotta voit varmistaa myynti- ja ostolaskujen automaattisen pyöristyksen.</span><span class="sxs-lookup"><span data-stu-id="8a958-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="8a958-135">Voit aktivoida laskunpyöristyksen erikseen myynti- ja ostolaskuille.</span><span class="sxs-lookup"><span data-stu-id="8a958-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="8a958-136">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** tai **Ostojen ostovelkojen asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8a958-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8a958-137">Valitse **Yleiset**-pikavälilehdessä **Laskun pyöristys** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="8a958-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8a958-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8a958-138">See Also</span></span>  
[<span data-ttu-id="8a958-139">Myynnin laskutus</span><span class="sxs-lookup"><span data-stu-id="8a958-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="8a958-140">Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="8a958-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)

