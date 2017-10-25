---
title: Kustannusbudjettien luominen | Microsoft Docs
description: "Tässä ohjeaiheessa käsitellään yleisesti kustannusbudjettien luontia ja analysointia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5e66e9f915772a6e5f9000ea6fe207e425ee25bb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="creating-cost-budgets"></a><span data-ttu-id="eed7d-103">Kustannusbudjettien luominen</span><span class="sxs-lookup"><span data-stu-id="eed7d-103">Creating Cost Budgets</span></span>
<span data-ttu-id="eed7d-104">Budjetointi kustannuslaskennassa muistuttaa pääkirjanpidon budjetointia.</span><span class="sxs-lookup"><span data-stu-id="eed7d-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="eed7d-105">Kustannusbudjetti luodaan kustannustyyppien perusteella samalla tavalla kuin pääkirjanpidon budjetti  luodaan pääkirjanpitotilien perusteella.</span><span class="sxs-lookup"><span data-stu-id="eed7d-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="eed7d-106">Kustannusbudjetti luodaan tietylle aikajaksolle, esimerkiksi tilikaudelle.</span><span class="sxs-lookup"><span data-stu-id="eed7d-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="eed7d-107">Kustannusbudjetteja voi määrittää niin monta kuin tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="eed7d-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="eed7d-108">Voit luoda uuden kusannusbudjeti manuaalisesti tai tuomalla kustannusbudjetin tai kopioimalla aiemmin luodun kustannusbudjetin talousarvion perustaksi.</span><span class="sxs-lookup"><span data-stu-id="eed7d-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="eed7d-109">Lisätietoja on kohdassa [Budjettien luominen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="eed7d-109">For more information, see [How to: Create Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="eed7d-110">Voit luoda ja analysoida kustannusbudjetteja seuraavissa ikkunoissa.</span><span class="sxs-lookup"><span data-stu-id="eed7d-110">You use the following windows to create and analyze cost budgets.</span></span> <span data-ttu-id="eed7d-111">Etsi ikkuna valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake ja lue sitten kunkin ikkunan työkaluvihje.</span><span class="sxs-lookup"><span data-stu-id="eed7d-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon to find a window, and then read the tooltip for each.</span></span>

|<span data-ttu-id="eed7d-112">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="eed7d-112">To</span></span>|<span data-ttu-id="eed7d-113">Katso</span><span class="sxs-lookup"><span data-stu-id="eed7d-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="eed7d-114">Siirrä budjetit pääkirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="eed7d-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="eed7d-115">**Kopioi KP-budjetti kustannuslaskentaan** -eräajo</span><span class="sxs-lookup"><span data-stu-id="eed7d-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="eed7d-116">Kopioi kustannusbudjetit.</span><span class="sxs-lookup"><span data-stu-id="eed7d-116">Copy cost budgets.</span></span>|<span data-ttu-id="eed7d-117">**Kopioi budjetin kustannukset** -eräajo</span><span class="sxs-lookup"><span data-stu-id="eed7d-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="eed7d-118">Kohdista budjetit.</span><span class="sxs-lookup"><span data-stu-id="eed7d-118">Allocate budgets.</span></span>|<span data-ttu-id="eed7d-119">**Kustannusten kohdistaminen** -sivu</span><span class="sxs-lookup"><span data-stu-id="eed7d-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="eed7d-120">Katso kustannusbudjetin rekisterit ja kustannusbudjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="eed7d-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="eed7d-121">**Kustannusbudjettirekisterit** -sivu</span><span class="sxs-lookup"><span data-stu-id="eed7d-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="eed7d-122">Tulosta kustannusbudjettivertailut eri raporttien avulla.</span><span class="sxs-lookup"><span data-stu-id="eed7d-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="eed7d-123">**Kustannuslaskennan saldo/budjetti** -raportti</span><span class="sxs-lookup"><span data-stu-id="eed7d-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="eed7d-124">**Kustannuslaskelma/budjetti** -raportti</span><span class="sxs-lookup"><span data-stu-id="eed7d-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="eed7d-125">**Kustannusbudjetti kustannuspaikoittain** -raportti</span><span class="sxs-lookup"><span data-stu-id="eed7d-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="eed7d-126">**Kustannusbudjetti kustannuskohteittain** -raportti</span><span class="sxs-lookup"><span data-stu-id="eed7d-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="eed7d-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="eed7d-127">See Also</span></span>  
[<span data-ttu-id="eed7d-128">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="eed7d-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="eed7d-129">Uusien budjettien luominen</span><span class="sxs-lookup"><span data-stu-id="eed7d-129">How to: Create Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="eed7d-130">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="eed7d-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="eed7d-131">Kustannusten määrittäminen ja kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="eed7d-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="eed7d-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eed7d-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

