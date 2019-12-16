---
title: Kustannusbudjettien luominen | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään yleisesti kustannusbudjettien luontia ja analysointia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 33999778898c671a87638ef5868103ea34875ff8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879822"
---
# <a name="creating-cost-budgets"></a><span data-ttu-id="2df33-103">Kustannusbudjettien luominen</span><span class="sxs-lookup"><span data-stu-id="2df33-103">Creating Cost Budgets</span></span>
<span data-ttu-id="2df33-104">Budjetointi kustannuslaskennassa muistuttaa pääkirjanpidon budjetointia.</span><span class="sxs-lookup"><span data-stu-id="2df33-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="2df33-105">Kustannusbudjetti luodaan kustannustyyppien perusteella samalla tavalla kuin pääkirjanpidon budjetti luodaan pääkirjanpitotilien perusteella.</span><span class="sxs-lookup"><span data-stu-id="2df33-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="2df33-106">Kustannusbudjetti luodaan tietylle aikajaksolle, esimerkiksi tilikaudelle.</span><span class="sxs-lookup"><span data-stu-id="2df33-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="2df33-107">Kustannusbudjetteja voi määrittää niin monta kuin tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="2df33-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="2df33-108">Voit luoda uuden kusannusbudjeti manuaalisesti tai tuomalla kustannusbudjetin tai kopioimalla aiemmin luodun kustannusbudjetin talousarvion perustaksi.</span><span class="sxs-lookup"><span data-stu-id="2df33-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="2df33-109">Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="2df33-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="2df33-110">Voit luoda ja analysoida kustannusbudjetteja seuraavilla sivuilla.</span><span class="sxs-lookup"><span data-stu-id="2df33-110">You use the following pages to create and analyze cost budgets.</span></span> <span data-ttu-id="2df33-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen ja etsi sivu. Lue sitten kunkin sivun työkaluvihje.</span><span class="sxs-lookup"><span data-stu-id="2df33-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon to find a page, and then read the tooltip for each.</span></span>

|<span data-ttu-id="2df33-112">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="2df33-112">To</span></span>|<span data-ttu-id="2df33-113">Katso</span><span class="sxs-lookup"><span data-stu-id="2df33-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="2df33-114">Siirrä budjetit pääkirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="2df33-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="2df33-115">**Kopioi KP-budjetti kustannuslaskentaan** -eräajo</span><span class="sxs-lookup"><span data-stu-id="2df33-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="2df33-116">Kopioi kustannusbudjetit.</span><span class="sxs-lookup"><span data-stu-id="2df33-116">Copy cost budgets.</span></span>|<span data-ttu-id="2df33-117">**Kopioi budjetin kustannukset** -eräajo</span><span class="sxs-lookup"><span data-stu-id="2df33-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="2df33-118">Kohdista budjetit.</span><span class="sxs-lookup"><span data-stu-id="2df33-118">Allocate budgets.</span></span>|<span data-ttu-id="2df33-119">**Kustannusten kohdistaminen** -sivu</span><span class="sxs-lookup"><span data-stu-id="2df33-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="2df33-120">Katso kustannusbudjetin rekisterit ja kustannusbudjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="2df33-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="2df33-121">**Kustannusbudjettirekisterit** -sivu</span><span class="sxs-lookup"><span data-stu-id="2df33-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="2df33-122">Tulosta kustannusbudjettivertailut eri raporttien avulla.</span><span class="sxs-lookup"><span data-stu-id="2df33-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="2df33-123">**Kustannuslaskennan saldo/budjetti** -raportti</span><span class="sxs-lookup"><span data-stu-id="2df33-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="2df33-124">**Kustannuslaskelma/budjetti** -raportti</span><span class="sxs-lookup"><span data-stu-id="2df33-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="2df33-125">**Kustannusbudjetti kustannuspaikoittain** -raportti</span><span class="sxs-lookup"><span data-stu-id="2df33-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="2df33-126">**Kustannusbudjetti kustannuskohteittain** -raportti</span><span class="sxs-lookup"><span data-stu-id="2df33-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="2df33-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2df33-127">See Also</span></span>  
[<span data-ttu-id="2df33-128">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="2df33-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="2df33-129">KP-budjettien luominen</span><span class="sxs-lookup"><span data-stu-id="2df33-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="2df33-130">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="2df33-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="2df33-131">Kustannusten määrittäminen ja kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="2df33-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="2df33-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2df33-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
