---
title: "Rakennetiedot – Varaston arvostus | Microsoft Docs"
description: "Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja Business Central -sovelluksen varaston arvostuksen toiminnoissa käytettävistä konsepteista ja periaatteista."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 830c14eb96557f8852d0a4758922503fe0179b58
ms.contentlocale: fi-fi
ms.lasthandoff: 11/29/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="1a760-103">Rakennetiedot: varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="1a760-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="1a760-104">Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman varaston arvostuksen toiminnoissa käytettävistä konsepteista ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="1a760-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="1a760-105">Varaston arvostus, jota kutsutaan myös kustannuslaskennaksi, käsittelee liiketoiminnan toimintokustannusten tallennusta ja raportointia.</span><span class="sxs-lookup"><span data-stu-id="1a760-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="1a760-106">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="1a760-106">In This Section</span></span>  
[<span data-ttu-id="1a760-107">Rakennetiedot: Arvostusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="1a760-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="1a760-108">Rakennetiedot: Nimikkeen kohdistus</span><span class="sxs-lookup"><span data-stu-id="1a760-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="1a760-109">Rakennetiedot: Nimikkeen kohdistuksen tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="1a760-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="1a760-110">Rakennetiedot: Kustannuksen muutos</span><span class="sxs-lookup"><span data-stu-id="1a760-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="1a760-111">Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="1a760-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="1a760-112">Rakennetiedot: Oletetun kustannuksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="1a760-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="1a760-113">Rakennetiedot: Keskimääräinen kustannus</span><span class="sxs-lookup"><span data-stu-id="1a760-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="1a760-114">Rakennetiedot: varianssi</span><span class="sxs-lookup"><span data-stu-id="1a760-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="1a760-115">Rakennetiedot: pyöristys</span><span class="sxs-lookup"><span data-stu-id="1a760-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="1a760-116">Rakennetiedot: kustannuskomponentit</span><span class="sxs-lookup"><span data-stu-id="1a760-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="1a760-117">Rakennetiedot: varastokausi</span><span class="sxs-lookup"><span data-stu-id="1a760-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="1a760-118">Rakennetiedot: varaston kirjaus</span><span class="sxs-lookup"><span data-stu-id="1a760-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="1a760-119">Rakennetiedot: tuotantotilauksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="1a760-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="1a760-120">Rakennetiedot: Kokoonpanotilauksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="1a760-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="1a760-121">Rakennetiedot: täsmäytys pääkirjanpidon kanssa</span><span class="sxs-lookup"><span data-stu-id="1a760-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
<span data-ttu-id="1a760-122">[Rakennetiedot: pääkirjanpidon tilit](design-details-accounts-in-the-general-ledger.md)
[Rakennetiedot: varaston arvostus](design-details-inventory-valuation.md)</span><span class="sxs-lookup"><span data-stu-id="1a760-122">[Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md)
[Design Details: Inventory Valuation](design-details-inventory-valuation.md)</span></span>  
[<span data-ttu-id="1a760-123">Rakennetiedot: uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="1a760-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)

