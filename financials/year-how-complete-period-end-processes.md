---
title: Jaksojen sulkemisen valinnaiset toiminnot | Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan Financialsin kirjanpitojaksojen sulkemisen valinnaisista prosesseista ja toiminnoista."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 678cebc065594ed0ed6fea897676f109ff2c1dce
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="57238-103">Kirjanpitojaksojen sulkemistehtävien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="57238-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="57238-104"> ei pakota päättämään kausia, joskin on monia kauden lopussa (kuukauden lopussa) aktiviteetteja, jotka voit tehdä.</span><span class="sxs-lookup"><span data-stu-id="57238-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="57238-105">Tässä ohjeaiheessa on yleiskatsaus kausien päättämiseen liittyvistä valinnaisista prosesseista ja aktiviteeteista.</span><span class="sxs-lookup"><span data-stu-id="57238-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="57238-106">Pääkirjanpito</span><span class="sxs-lookup"><span data-stu-id="57238-106">General Ledger</span></span>
* <span data-ttu-id="57238-107">Määritä järjestelmänlaajuiset ja käyttäjäkohtaiset kirjausjaksot.</span><span class="sxs-lookup"><span data-stu-id="57238-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="57238-108">Tässä määritetään kirjausten sallittu päivämääräväli.</span><span class="sxs-lookup"><span data-stu-id="57238-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="57238-109">Liiketoiminnan tarpeiden mukaan voit sallia kirjauksen jakson alussa tai jakson loppupuolella.</span><span class="sxs-lookup"><span data-stu-id="57238-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="57238-110">Lisätietoja on kohdassa [Toimintaohje: Kirjausjaksojen määrittäminen](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="57238-110">For more information, see [How to: Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="57238-111">Tee kaikki tarpeelliset KP-muutokset.</span><span class="sxs-lookup"><span data-stu-id="57238-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="57238-112">Päivitä ja kirjaa toistuvat päiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="57238-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="57238-113">Suorita KP-raporttimallit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="57238-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="57238-114">Avaa **KP-raporttimalli**-ikkuna ja valitse sitten **Tulosta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="57238-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="57238-115">Myynnit ja myyntisaamiset</span><span class="sxs-lookup"><span data-stu-id="57238-115">Sales and Receivables</span></span>
* <span data-ttu-id="57238-116">Kirjaa kaikki myyntitilaukset, laskut, hyvityslaskut ja palautustilaukset.</span><span class="sxs-lookup"><span data-stu-id="57238-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="57238-117">Kirjaa kaikki kassapäiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="57238-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="57238-118">Päivitä ja kirjaa myyntiin ja myyntisaamisiin liittyvät toistuvat päiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="57238-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="57238-119">Täsmäytä myyntisaatavat pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="57238-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="57238-120">Suorita **Poista laskutetut myyntitilaukset** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="57238-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="57238-121">Ostot ja ostovelat</span><span class="sxs-lookup"><span data-stu-id="57238-121">Purchases and Payables</span></span>
* <span data-ttu-id="57238-122">Kirjaa kaikki ostotilaukset, laskut, hyvityslaskut ja palautustilaukset.</span><span class="sxs-lookup"><span data-stu-id="57238-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="57238-123">Kirjaa kaikki maksupäiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="57238-123">Post all payment journals.</span></span>  
* <span data-ttu-id="57238-124">Päivitä ja kirjaa ostoihin ja ostovelkoihin liittyvät toistuvat päiväkirjat.</span><span class="sxs-lookup"><span data-stu-id="57238-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="57238-125">Suorita **Ostovelkojen tilanne** -raportti ja täsmäytä ostovelat pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="57238-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="57238-126">Suorita **Poista laskutetut ostotilaukset** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="57238-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="57238-127">Arvonlisäveron laskeminen ja käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="57238-127">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="57238-128">Täytä ALV-ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="57238-128">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="57238-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="57238-129">See Also</span></span>
[<span data-ttu-id="57238-130">Vuosien ja jaksojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="57238-130">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="57238-131">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="57238-131">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="57238-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="57238-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

