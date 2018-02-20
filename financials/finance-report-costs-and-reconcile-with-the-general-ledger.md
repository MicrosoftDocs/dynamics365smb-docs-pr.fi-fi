---
title: "Kustannukset raportointi ja täsmäyttäminen pääkirjanpidon kanssa | Microsoft Docs"
description: "Kirjanpitojaksojen lopussa (kuukausittain, vuosittain tai muulla aikavälillä) suoritetaan joukko kustannustenhallinta- ja auditointitehtäviä, joiden avulla saadaan oikea ja saldoltaan täsmällinen varaston arvo raportoitavaksi taloushallinto-osastolle. Tilintarkastajat ja kustannusten seurantahenkilöstö vastaavat näistä liiketoiminnan kannalta kriittisistä tehtävistä, ja yksittäisiä nimikkeen arvotapahtumia erityisille kirjanpitotileille siirtävän kirjausrutiinin lisäksi heidän käytettävissään on useita raportteja, jäljitystoimintoja ja erityinen täsmäytystyökalu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45afc7249e921b483d9fcb6860401528746f554a
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a><span data-ttu-id="8b45e-104">Kustannukset raportointi ja täsmäyttäminen pääkirjanpidon kanssa</span><span class="sxs-lookup"><span data-stu-id="8b45e-104">Reporting Costs and Reconciling with the General Ledger</span></span>
<span data-ttu-id="8b45e-105">Kirjanpitojaksojen lopussa (kuukausittain, vuosittain tai muulla aikavälillä) suoritetaan joukko kustannustenhallinta- ja auditointitehtäviä, joiden avulla saadaan oikea ja saldoltaan täsmällinen varaston arvo raportoitavaksi taloushallinto-osastolle.</span><span class="sxs-lookup"><span data-stu-id="8b45e-105">At the end of accounting periods, monthly, yearly or other, a sequence of cost control and auditing tasks must be performed to report a correct and balanced inventory value to the finance department.</span></span> <span data-ttu-id="8b45e-106">Tilintarkastajat ja kustannusten seurantahenkilöstö vastaavat näistä liiketoiminnan kannalta kriittisistä tehtävistä, ja yksittäisiä nimikkeen arvotapahtumia erityisille kirjanpitotileille siirtävän kirjausrutiinin lisäksi heidän käytettävissään on useita raportteja, jäljitystoimintoja ja erityinen täsmäytystyökalu.</span><span class="sxs-lookup"><span data-stu-id="8b45e-106">Apart from the posting routine that transfers the individual item value entries to dedicated general ledger accounts, several reports, tracing functions, and a special reconciliation tool are available to the auditor or controller responsible for this business-critical work.</span></span>  

 <span data-ttu-id="8b45e-107">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="8b45e-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="8b45e-108">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="8b45e-108">**To**</span></span>|<span data-ttu-id="8b45e-109">**Katso**</span><span class="sxs-lookup"><span data-stu-id="8b45e-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="8b45e-110">Valittujen nimikkeiden varaston arvon tarkastelu. Tietoihin sisältyvät varaston lisäysten ja vähennysten määrät ja arvot valittuna aikana.</span><span class="sxs-lookup"><span data-stu-id="8b45e-110">View the inventory value of selected items, including information about the quantities and values of increases and decreases in inventory over a selected period.</span></span>|<span data-ttu-id="8b45e-111">**Varaston arvostus** -raportti</span><span class="sxs-lookup"><span data-stu-id="8b45e-111">**Inventory Valuation** report</span></span>|  
|<span data-ttu-id="8b45e-112">Valittujen KET-varaston tuotantotilausten varaston arvon tarkastelu. Tietoihin sisältyvät kulutuksen määrät ja arvot, kapasiteetin käyttö sekä meneillään olevien tuotantotilausten tuotto.</span><span class="sxs-lookup"><span data-stu-id="8b45e-112">View the inventory value of selected production orders in your WIP (work in process) inventory, such as the quantities and values of consumption, capacity usage, and output in ongoing production orders.</span></span>|<span data-ttu-id="8b45e-113">**Varaston arvostus - KET** -raportti</span><span class="sxs-lookup"><span data-stu-id="8b45e-113">**Inventory Valuation - WIP** report</span></span>|  
|<span data-ttu-id="8b45e-114">Valittujen nimikkeiden varaston arvon tarkastelu, mukaan lukien todellinen ja oletettu kustannus määritettynä päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="8b45e-114">View the inventory value of selected items, including their actual and expected cost on the date specified.</span></span>|<span data-ttu-id="8b45e-115">**Varaston arvostus - Kust. määr.** -raportti</span><span class="sxs-lookup"><span data-stu-id="8b45e-115">**Invt. Valuation - Cost Spec.** report</span></span>|  
|<span data-ttu-id="8b45e-116">Raportin käyttäminen kustannusvarianssien analysoimiseksi tai myytyjen tuotteiden kustannusosuuksien selvittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="8b45e-116">Use a report to analyze the reasons for cost variances or to gain insight into the cost shares of sold items (COGS).</span></span>|<span data-ttu-id="8b45e-117">**Kustannusjakaumien erittely** -raportti</span><span class="sxs-lookup"><span data-stu-id="8b45e-117">**Cost Shares Breakdown** report</span></span>|  
|<span data-ttu-id="8b45e-118">Nimiketapahtumiin liittyvien arvotapahtumien kausittainen kirjaaminen varastotapahtumista niihin liittyville pääkirjanpidon tileille näiden kahden kirjanpidon täsmäyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="8b45e-118">Periodically post the value entries of item transactions from the inventory ledger to the related G/L accounts to reconcile the two ledgers.</span></span>|[<span data-ttu-id="8b45e-119">Varaston kustannusten täsmäyttäminen pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="8b45e-119">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="8b45e-120">Varastotapahtumien ja pääkirjanpidon välisen täsmäytyksen tarkistaminen yhdessä ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="8b45e-120">Use one window to audit the reconciliation between the inventory ledger and the general ledger.</span></span>|[<span data-ttu-id="8b45e-121">Varaston kustannusten täsmäyttäminen pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="8b45e-121">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="8b45e-122">Tasetileille kirjattavan KET-summan määrittäminen kauden lopussa suoritettavaa raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="8b45e-122">Determine the WIP amount that needs to be posted to balance sheet accounts for period-end reporting.</span></span>|[<span data-ttu-id="8b45e-123">Projektin edistymisen ja suorituskyvyn valvonta</span><span class="sxs-lookup"><span data-stu-id="8b45e-123">Monitor Job Progress and Performance</span></span>](projects-how-monitor-progress-performance.md)|

## <a name="see-also"></a><span data-ttu-id="8b45e-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8b45e-124">See Also</span></span>  
[<span data-ttu-id="8b45e-125">Varastonarvostuksen ja kustannuslaskennan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8b45e-125">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="8b45e-126">Varaston kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="8b45e-126">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="8b45e-127">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="8b45e-127">Finance</span></span>](finance.md)  
<span data-ttu-id="8b45e-128">[Vaihto-omaisuus](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="8b45e-128">[Inventory](inventory-manage-inventory.md) </span></span>  
<span data-ttu-id="8b45e-129">[Myynti](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="8b45e-129">[Sales](sales-manage-sales.md) </span></span>  
[<span data-ttu-id="8b45e-130">Osto</span><span class="sxs-lookup"><span data-stu-id="8b45e-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8b45e-131">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8b45e-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

