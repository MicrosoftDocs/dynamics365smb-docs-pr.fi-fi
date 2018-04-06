---
title: "Talousprosessien määrittäminen| Microsoft Docs"
description: "Lisätietoja tehtävistä, joilla määritetään liiketoiminnan taloushallinto laskentatoimen, tilintarkastuksen tai kirjanpidon tarpeita varten."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 08/10/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5ec4748db61410128b7a61336e52ea6f066fae34
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-finance"></a><span data-ttu-id="ecd6e-103">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-103">Setting Up Finance</span></span>
<span data-ttu-id="ecd6e-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää useimpien rahoitusprosessien vakiomääritykset, mikä nopeuttaa käytön aloittamista.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-104">To help you get going quickly, [!INCLUDE[d365fin](includes/d365fin_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="ecd6e-105">Voit tarvittaessa muuttaa määrityksiä liiketoiminnan tarpeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="ecd6e-106">Voit määrittää esimerkiksi roolikeskuksessa avustetun asennusoppaan avulla sijaintiin sopivan arvonlisäveron.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-106">For example, from the Role Center, you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="ecd6e-107">Tietyt asiat on kuitenkin määritettävä itse.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="ecd6e-108">Esimerkki: haluat käyttää dimensioita BI-tietojen perustana.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="ecd6e-109">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="ecd6e-110">Toiminta</span><span class="sxs-lookup"><span data-stu-id="ecd6e-110">To</span></span> | <span data-ttu-id="ecd6e-111">Katso</span><span class="sxs-lookup"><span data-stu-id="ecd6e-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="ecd6e-112">Valitse, miten maksat toimittajille.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="ecd6e-113">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="ecd6e-114">Määritä kirjausryhmät, jotka yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjat, pääkirjanpidon tileille.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="ecd6e-115">Kirjausryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="ecd6e-116">Määritä toleranssi, jonka mukaan järjestelmä sulkee laskun, vaikka maksu ja mahdolliset alennukset eivät täysin vastaa laskun koko summaa.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-116">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="ecd6e-117">Maksutoleranssien ja maksualennustoleranssien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-117">Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="ecd6e-118">Määritä tilikaudet.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-118">Set up fiscal periods.</span></span> |[<span data-ttu-id="ecd6e-119">Uuden tilikauden avaaminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-119">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="ecd6e-120">Määritä, miten myynnistä kerätyt arvonlisäverosummat raportoidaan veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-120">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="ecd6e-121">ALV:n raportointi veroviranomaisille</span><span class="sxs-lookup"><span data-stu-id="ecd6e-121">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="ecd6e-122">Määritä myynti- ja ostotoiminnot käsittelemään maksut ulkomaan valuuttana.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-122">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="ecd6e-123">Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa</span><span class="sxs-lookup"><span data-stu-id="ecd6e-123">Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="ecd6e-124">Lisää aiemmin luotuun tilikarttaan uusia tilejä.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-124">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="ecd6e-125">Tilikartan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-125">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="ecd6e-126">Määritä BI-kaaviot analysoimaan kassavirtaa.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-126">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="ecd6e-127">Kassavirta-analyysin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-127">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="ecd6e-128">Ota käyttöön sellaisen asiakkaan laskutus, jota ei ole määritetty järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="ecd6e-128">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="ecd6e-129">Käteisasiakkaiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-129">Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="ecd6e-130">Intrastat-raportoinnin määrittäminen ja raportin lähettäminen viranomaisille</span><span class="sxs-lookup"><span data-stu-id="ecd6e-130">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="ecd6e-131">Intrastat-ilmoituksen määrittäminen ja raportoiminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-131">Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="ecd6e-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ecd6e-132">See Also</span></span>
[<span data-ttu-id="ecd6e-133">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="ecd6e-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="ecd6e-134">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="ecd6e-134">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="ecd6e-135">Dimensioiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-135">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="ecd6e-136">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="ecd6e-136">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="ecd6e-137">Yrityksen kassavirran analysoiminen</span><span class="sxs-lookup"><span data-stu-id="ecd6e-137">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="ecd6e-138">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ecd6e-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

