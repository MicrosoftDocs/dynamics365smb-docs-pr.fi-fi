---
title: "Kustannusten määrittäminen ja kohdistaminen | Microsoft Docs"
description: "Kustannusten kohdistukset siirtävät kustannukset ja tuotot eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä. Voit määrittää niin monta kodhistusta kuin on tarpeen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7bdddcadf3fb7dceb762354e8fa527158782b676
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="d7d94-104">Kustannusten määrittäminen ja kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="d7d94-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="d7d94-105">Kustannusten kohdistukset siirtävät kustannuksia ja tuottoja eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä.</span><span class="sxs-lookup"><span data-stu-id="d7d94-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="d7d94-106">Voit määrittää niin monta kodhistusta kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="d7d94-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="d7d94-107">Jokainen kohdistus koostuu:</span><span class="sxs-lookup"><span data-stu-id="d7d94-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="d7d94-108">Kohdistamisen lähde.</span><span class="sxs-lookup"><span data-stu-id="d7d94-108">An allocation source.</span></span>  
-   <span data-ttu-id="d7d94-109">Vähintään yksi kohdistuskohde.</span><span class="sxs-lookup"><span data-stu-id="d7d94-109">One or more allocation targets.</span></span>  

<span data-ttu-id="d7d94-110">Kohdistuksen lähde määrittää, mitkä kustannukset täytyy kohdistaa sekä kohdistustavoitteet määrittävät, missä kustannukset on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="d7d94-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="d7d94-111">Esimerkiksi kohdistuksen lähde voi olla Sähkö ja lämmitys -kustannuslajin kustannukset.</span><span class="sxs-lookup"><span data-stu-id="d7d94-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="d7d94-112">Kohdista kaikki sähkö ja lämmityskustannukset kolmeen kustannuspaikkaan: korjaamo, tuotanto ja myynti.</span><span class="sxs-lookup"><span data-stu-id="d7d94-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="d7d94-113">Näihin kustannuspaikkoihin kohdistetaan kohteita.</span><span class="sxs-lookup"><span data-stu-id="d7d94-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="d7d94-114">Määritä jokaiselle kohdistuksen lähteelle kohdistustaso, voimassaoloaika ja variantti ryhmittelyn tunnukseksi.</span><span class="sxs-lookup"><span data-stu-id="d7d94-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="d7d94-115">Erätyön avulla voit määrittää suodattimia valitaksesi kohdistusmääritelmiä ja suorittaaksesi sitten kustannusten kohdistukset automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d7d94-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="d7d94-116">Määritä jokaiselle kohdistuksen kohteelle kohdistusperuste.</span><span class="sxs-lookup"><span data-stu-id="d7d94-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="d7d94-117">Kohdistusperuste voi olla joko staattinen tai dynaaminen.</span><span class="sxs-lookup"><span data-stu-id="d7d94-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="d7d94-118">Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="d7d94-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="d7d94-119">Dynaaminen kohdistus perustuu muutettaviin arvoihin, kuten työntekijöiden määrään kustannuspaikassa, kustannuskohteen myyntituottoihin tiettynä aikajaksona.</span><span class="sxs-lookup"><span data-stu-id="d7d94-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="d7d94-120">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="d7d94-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="d7d94-121">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="d7d94-121">To</span></span>|<span data-ttu-id="d7d94-122">Katso</span><span class="sxs-lookup"><span data-stu-id="d7d94-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="d7d94-123">Kohdistuksen lähteen ja sen tavoitteiden määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="d7d94-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="d7d94-124">Kohdistuksen lähteen ja sen tavoitteiden määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="d7d94-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="d7d94-125">Määrittää useita suodattimia dynaamisen kohdistuksen perusteille.</span><span class="sxs-lookup"><span data-stu-id="d7d94-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="d7d94-126">Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.</span><span class="sxs-lookup"><span data-stu-id="d7d94-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="d7d94-127">Esimerkki siitä, miten voit määrittää staattista kohdistamista.</span><span class="sxs-lookup"><span data-stu-id="d7d94-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="d7d94-128">Esimerkkiskenaario: Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d7d94-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="d7d94-129">Esimerkki siitä, miten voit määrittää dynaamista kohdistamista.</span><span class="sxs-lookup"><span data-stu-id="d7d94-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="d7d94-130">Esimerkkiskenaario: Määrittämällä myytyihin nimikkeisiin perustuvat dynaamiset kohdistamiset</span><span class="sxs-lookup"><span data-stu-id="d7d94-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="d7d94-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d7d94-131">See Also</span></span>  
 <span data-ttu-id="d7d94-132">[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="d7d94-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="d7d94-133">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d7d94-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="d7d94-134">[Kustannuslaskenta](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="d7d94-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="d7d94-135">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="d7d94-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="d7d94-136">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="d7d94-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

