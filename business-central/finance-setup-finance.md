---
title: "Talousprosessien määrittäminen| Microsoft Docs"
description: "Lisätietoja tehtävistä, joilla määritetään liiketoiminnan taloushallinto laskentatoimen, tilintarkastuksen tai kirjanpidon tarpeita varten."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 025c00e6013e773204a12abc7d86c09b3dcef3dd
ms.contentlocale: fi-fi
ms.lasthandoff: 06/28/2018

---
# <a name="setting-up-finance"></a><span data-ttu-id="91e8f-103">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-103">Setting Up Finance</span></span>
<span data-ttu-id="91e8f-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää useimpien rahoitusprosessien vakiomääritykset, mikä nopeuttaa käytön aloittamista.</span><span class="sxs-lookup"><span data-stu-id="91e8f-104">To help you get going quickly, [!INCLUDE[d365fin](includes/d365fin_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="91e8f-105">Voit tarvittaessa muuttaa määrityksiä liiketoiminnan tarpeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="91e8f-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="91e8f-106">Voit määrittää esimerkiksi roolikeskuksessa avustetun asennusoppaan avulla sijaintiin sopivan arvonlisäveron.</span><span class="sxs-lookup"><span data-stu-id="91e8f-106">For example, from the Role Center, you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="91e8f-107">Tietyt asiat on kuitenkin määritettävä itse.</span><span class="sxs-lookup"><span data-stu-id="91e8f-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="91e8f-108">Esimerkki: haluat käyttää dimensioita BI-tietojen perustana.</span><span class="sxs-lookup"><span data-stu-id="91e8f-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="91e8f-109">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="91e8f-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="91e8f-110">Toiminta</span><span class="sxs-lookup"><span data-stu-id="91e8f-110">To</span></span> | <span data-ttu-id="91e8f-111">Katso</span><span class="sxs-lookup"><span data-stu-id="91e8f-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="91e8f-112">Valitse, miten maksat toimittajille.</span><span class="sxs-lookup"><span data-stu-id="91e8f-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="91e8f-113">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="91e8f-114">Määritä kirjausryhmät, jotka yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjat, pääkirjanpidon tileille.</span><span class="sxs-lookup"><span data-stu-id="91e8f-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="91e8f-115">Kirjausryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="91e8f-116">Luo KP-raporttimallit ja määritä tililuokat, jos haluat määrittää talouskaavioiden ja -raporttien, kuten tase- ja tuloslaskelmaraporttien, sisällön.</span><span class="sxs-lookup"><span data-stu-id="91e8f-116">Create account schedules and define account categories to define the contents of financial charts and reports, such as the Balance Sheet and Income Statement reports.</span></span>|[<span data-ttu-id="91e8f-117">Talousraportoinnin valmisteleminen KP-raporttimallien ja tililuokkien avulla</span><span class="sxs-lookup"><span data-stu-id="91e8f-117">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>](bi-how-work-account-schedule.md)|
|<span data-ttu-id="91e8f-118">Määritä toleranssi, jonka mukaan järjestelmä sulkee laskun, vaikka maksu ja mahdolliset alennukset eivät täysin vastaa laskun koko summaa.</span><span class="sxs-lookup"><span data-stu-id="91e8f-118">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="91e8f-119">Maksutoleranssien ja maksualennustoleranssien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-119">Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="91e8f-120">Määritä tilikaudet.</span><span class="sxs-lookup"><span data-stu-id="91e8f-120">Set up fiscal periods.</span></span> |[<span data-ttu-id="91e8f-121">Uuden tilikauden avaaminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-121">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="91e8f-122">Määritä, miten myynnistä kerätyt arvonlisäverosummat raportoidaan veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="91e8f-122">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="91e8f-123">ALV:n raportointi veroviranomaisille</span><span class="sxs-lookup"><span data-stu-id="91e8f-123">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="91e8f-124">Määritä myynti- ja ostotoiminnot käsittelemään maksut ulkomaan valuuttana.</span><span class="sxs-lookup"><span data-stu-id="91e8f-124">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="91e8f-125">Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa</span><span class="sxs-lookup"><span data-stu-id="91e8f-125">Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="91e8f-126">Lisää aiemmin luotuun tilikarttaan uusia tilejä.</span><span class="sxs-lookup"><span data-stu-id="91e8f-126">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="91e8f-127">Tilikartan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-127">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="91e8f-128">Määritä BI-kaaviot analysoimaan kassavirtaa.</span><span class="sxs-lookup"><span data-stu-id="91e8f-128">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="91e8f-129">Kassavirta-analyysin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-129">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="91e8f-130">Ota käyttöön sellaisen asiakkaan laskutus, jota ei ole määritetty järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="91e8f-130">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="91e8f-131">Käteisasiakkaiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-131">Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="91e8f-132">Intrastat-raportoinnin määrittäminen ja raportin lähettäminen viranomaisille</span><span class="sxs-lookup"><span data-stu-id="91e8f-132">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="91e8f-133">Intrastat-ilmoituksen määrittäminen ja raportoiminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-133">Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="91e8f-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="91e8f-134">See Also</span></span>
[<span data-ttu-id="91e8f-135">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="91e8f-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="91e8f-136">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="91e8f-136">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="91e8f-137">Dimensioiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-137">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="91e8f-138">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="91e8f-138">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="91e8f-139">Yrityksen kassavirran analysoiminen</span><span class="sxs-lookup"><span data-stu-id="91e8f-139">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="91e8f-140">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="91e8f-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

