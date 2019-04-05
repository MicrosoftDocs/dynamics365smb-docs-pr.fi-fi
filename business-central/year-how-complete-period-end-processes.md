---
title: Jaksojen sulkemisen valinnaiset toiminnot | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan Business Central -sovelluksen kirjanpitojaksojen sulkemisen valinnaisista prosesseista ja toiminnoista.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: ab72d1af179ec543ea358ac957e9b658987f7d53
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795100"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="beafe-103">Kirjanpitojaksojen sulkemistehtävien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="beafe-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="beafe-104">ei pakota päättämään kausia, joskin on monia kauden lopussa (kuukauden lopussa) aktiviteetteja, jotka voit tehdä.</span><span class="sxs-lookup"><span data-stu-id="beafe-104">does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="beafe-105">Tässä ohjeaiheessa on yleiskatsaus kausien päättämiseen liittyvistä valinnaisista prosesseista ja aktiviteeteista.</span><span class="sxs-lookup"><span data-stu-id="beafe-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="beafe-106">Pääkirjanpito</span><span class="sxs-lookup"><span data-stu-id="beafe-106">General Ledger</span></span>
* <span data-ttu-id="beafe-107">Määritä järjestelmänlaajuiset ja käyttäjäkohtaiset kirjausjaksot.</span><span class="sxs-lookup"><span data-stu-id="beafe-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="beafe-108">Tässä määritetään kirjausten sallittu päivämääräväli.</span><span class="sxs-lookup"><span data-stu-id="beafe-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="beafe-109">Liiketoiminnan tarpeiden mukaan voit sallia kirjauksen jakson alussa tai jakson loppupuolella.</span><span class="sxs-lookup"><span data-stu-id="beafe-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="beafe-110">Lisätietoja on kohdassa [Kirjausjaksojen määrittäminen](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="beafe-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="beafe-111">Tee kaikki tarpeelliset KP-muutokset.</span><span class="sxs-lookup"><span data-stu-id="beafe-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="beafe-112">Päivitä ja kirjaa toistuvat päiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="beafe-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="beafe-113">Suorita KP-raporttimallit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="beafe-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="beafe-114">Avaa **KP-raporttimalli**-sivu ja valitse sitten **Tulosta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="beafe-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="beafe-115">Myynnit ja myyntisaamiset</span><span class="sxs-lookup"><span data-stu-id="beafe-115">Sales and Receivables</span></span>
* <span data-ttu-id="beafe-116">Kirjaa kaikki myyntitilaukset, laskut, hyvityslaskut ja palautustilaukset.</span><span class="sxs-lookup"><span data-stu-id="beafe-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="beafe-117">Kirjaa kaikki kassapäiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="beafe-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="beafe-118">Päivitä ja kirjaa myyntiin ja myyntisaamisiin liittyvät toistuvat päiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="beafe-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="beafe-119">Täsmäytä myyntisaatavat pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="beafe-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="beafe-120">Suorita **Poista laskutetut myyntitilaukset** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="beafe-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="beafe-121">Ostot ja ostovelat</span><span class="sxs-lookup"><span data-stu-id="beafe-121">Purchases and Payables</span></span>
* <span data-ttu-id="beafe-122">Kirjaa kaikki ostotilaukset, laskut, hyvityslaskut ja palautustilaukset.</span><span class="sxs-lookup"><span data-stu-id="beafe-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="beafe-123">Kirjaa kaikki maksupäiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="beafe-123">Post all payment journals.</span></span>  
* <span data-ttu-id="beafe-124">Päivitä ja kirjaa ostoihin ja ostovelkoihin liittyvät toistuvat päiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="beafe-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="beafe-125">Suorita **Ostovelkojen tilanne** -raportti ja täsmäytä ostovelat pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="beafe-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="beafe-126">Suorita **Poista laskutetut ostotilaukset** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="beafe-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="beafe-127">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="beafe-127">Fixed Assets</span></span>
* <span data-ttu-id="beafe-128">Kirjaa kaikki kunnossapitokustannukset, jotka on kirjattu käyttöomaisuuspäiväkirjojen tai laskujen kautta.</span><span class="sxs-lookup"><span data-stu-id="beafe-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="beafe-129">Kirjaa muutokset.</span><span class="sxs-lookup"><span data-stu-id="beafe-129">Post adjustments.</span></span>
* <span data-ttu-id="beafe-130">Kirjaa arvonkorotus.</span><span class="sxs-lookup"><span data-stu-id="beafe-130">Post appreciation.</span></span>
* <span data-ttu-id="beafe-131">Kirjaa arvonalennus.</span><span class="sxs-lookup"><span data-stu-id="beafe-131">Post depreciation.</span></span>
* <span data-ttu-id="beafe-132">Päivitä ja kirjaa toistuva käyttöomaisuuspäiväkirja.</span><span class="sxs-lookup"><span data-stu-id="beafe-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="beafe-133">Konserni</span><span class="sxs-lookup"><span data-stu-id="beafe-133">Intercompany</span></span>
* <span data-ttu-id="beafe-134">Konsernin tapahtumien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="beafe-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="beafe-135">Arvonlisäveron laskeminen ja käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="beafe-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="beafe-136">Täytä ALV-ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="beafe-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="beafe-137">Katso myös</span><span class="sxs-lookup"><span data-stu-id="beafe-137">See Also</span></span>
[<span data-ttu-id="beafe-138">Vuosien ja jaksojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="beafe-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="beafe-139">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="beafe-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="beafe-140">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="beafe-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
