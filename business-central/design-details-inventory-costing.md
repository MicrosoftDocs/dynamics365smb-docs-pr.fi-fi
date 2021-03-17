---
title: Rakennetiedot – Varaston arvostus | Microsoft Docs
description: Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja Business Central -sovelluksen varaston arvostuksen toiminnoissa käytettävistä konsepteista ja periaatteista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a14c2a81a6aa36ce57384decb9342660297f9a84
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389922"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="e5532-103">Rakennetiedot: varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="e5532-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="e5532-104">Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman varaston arvostuksen toiminnoissa käytettävistä konsepteista ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="e5532-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="e5532-105">Varaston arvostus, jota kutsutaan myös kustannuslaskennaksi, käsittelee liiketoiminnan toimintokustannusten tallennusta ja raportointia.</span><span class="sxs-lookup"><span data-stu-id="e5532-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="e5532-106">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="e5532-106">In This Section</span></span>  
[<span data-ttu-id="e5532-107">Rakennetiedot: Arvostusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="e5532-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="e5532-108">Rakennetiedot: Nimikkeen kohdistus</span><span class="sxs-lookup"><span data-stu-id="e5532-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="e5532-109">Rakennetiedot: Nimikkeen kohdistuksen tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="e5532-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="e5532-110">Rakennetiedot: Kustannuksen muutos</span><span class="sxs-lookup"><span data-stu-id="e5532-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="e5532-111">Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="e5532-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="e5532-112">Rakennetiedot: Oletetun kustannuksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="e5532-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="e5532-113">Rakennetiedot: Keskimääräinen kustannus</span><span class="sxs-lookup"><span data-stu-id="e5532-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="e5532-114">Rakennetiedot: varianssi</span><span class="sxs-lookup"><span data-stu-id="e5532-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="e5532-115">Rakennetiedot: pyöristys</span><span class="sxs-lookup"><span data-stu-id="e5532-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="e5532-116">Rakennetiedot: kustannuskomponentit</span><span class="sxs-lookup"><span data-stu-id="e5532-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="e5532-117">Rakennetiedot: varastokausi</span><span class="sxs-lookup"><span data-stu-id="e5532-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="e5532-118">Rakennetiedot: varaston kirjaus</span><span class="sxs-lookup"><span data-stu-id="e5532-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="e5532-119">Rakennetiedot: tuotantotilauksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="e5532-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="e5532-120">Rakennetiedot: Kokoonpanotilauksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="e5532-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="e5532-121">Rakennetiedot: täsmäytys pääkirjanpidon kanssa</span><span class="sxs-lookup"><span data-stu-id="e5532-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="e5532-122">Rakennetiedot: pääkirjanpidon tilit</span><span class="sxs-lookup"><span data-stu-id="e5532-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="e5532-123">Rakennetiedot: varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="e5532-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="e5532-124">Rakennetiedot: uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="e5532-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]