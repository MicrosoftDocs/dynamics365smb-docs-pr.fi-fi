---
title: Rakennetiedot – Varaston arvostus | Microsoft Docs
description: Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja Business Central -sovelluksen varaston arvostuksen toiminnoissa käytettävistä konsepteista ja periaatteista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 11/25/2019
ms.author: sgroespe
ms.openlocfilehash: 667adfcc9c470a9d4dbf26923fe5e6edfc7ed85a
ms.sourcegitcommit: e97e1df1f5d7b1d8af477580960a8737fcea4d16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832189"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="6f48d-103">Rakennetiedot: varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="6f48d-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="6f48d-104">Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman varaston arvostuksen toiminnoissa käytettävistä konsepteista ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="6f48d-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="6f48d-105">Varaston arvostus, jota kutsutaan myös kustannuslaskennaksi, käsittelee liiketoiminnan toimintokustannusten tallennusta ja raportointia.</span><span class="sxs-lookup"><span data-stu-id="6f48d-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="6f48d-106">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="6f48d-106">In This Section</span></span>  
[<span data-ttu-id="6f48d-107">Rakennetiedot: Arvostusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="6f48d-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="6f48d-108">Rakennetiedot: Nimikkeen kohdistus</span><span class="sxs-lookup"><span data-stu-id="6f48d-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="6f48d-109">Rakennetiedot: Nimikkeen kohdistuksen tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="6f48d-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="6f48d-110">Rakennetiedot: Kustannuksen muutos</span><span class="sxs-lookup"><span data-stu-id="6f48d-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="6f48d-111">Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="6f48d-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="6f48d-112">Rakennetiedot: Oletetun kustannuksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="6f48d-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="6f48d-113">Rakennetiedot: Keskimääräinen kustannus</span><span class="sxs-lookup"><span data-stu-id="6f48d-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="6f48d-114">Rakennetiedot: varianssi</span><span class="sxs-lookup"><span data-stu-id="6f48d-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="6f48d-115">Rakennetiedot: pyöristys</span><span class="sxs-lookup"><span data-stu-id="6f48d-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="6f48d-116">Rakennetiedot: kustannuskomponentit</span><span class="sxs-lookup"><span data-stu-id="6f48d-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="6f48d-117">Rakennetiedot: varastokausi</span><span class="sxs-lookup"><span data-stu-id="6f48d-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="6f48d-118">Rakennetiedot: varaston kirjaus</span><span class="sxs-lookup"><span data-stu-id="6f48d-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="6f48d-119">Rakennetiedot: tuotantotilauksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="6f48d-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="6f48d-120">Rakennetiedot: Kokoonpanotilauksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="6f48d-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="6f48d-121">Rakennetiedot: täsmäytys pääkirjanpidon kanssa</span><span class="sxs-lookup"><span data-stu-id="6f48d-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="6f48d-122">Rakennetiedot: pääkirjanpidon tilit</span><span class="sxs-lookup"><span data-stu-id="6f48d-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="6f48d-123">Rakennetiedot: varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="6f48d-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="6f48d-124">Rakennetiedot: uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="6f48d-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)
