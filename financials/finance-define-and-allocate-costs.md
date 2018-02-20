---
title: "Kustannusten määrittäminen ja kohdistaminen | Microsoft Docs"
description: "Kustannusten kohdistukset siirtävät kustannukset ja tuotot eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä. Voit määrittää niin monta kodhistusta kuin on tarpeen."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="891bb-104">Kustannusten määrittäminen ja kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="891bb-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="891bb-105">Kustannusten kohdistukset siirtävät kustannuksia ja tuottoja eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä.</span><span class="sxs-lookup"><span data-stu-id="891bb-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="891bb-106">Voit määrittää niin monta kodhistusta kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="891bb-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="891bb-107">Jokainen kohdistus koostuu:</span><span class="sxs-lookup"><span data-stu-id="891bb-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="891bb-108">Kohdistamisen lähde.</span><span class="sxs-lookup"><span data-stu-id="891bb-108">An allocation source.</span></span>  
-   <span data-ttu-id="891bb-109">Vähintään yksi kohdistuskohde.</span><span class="sxs-lookup"><span data-stu-id="891bb-109">One or more allocation targets.</span></span>  

<span data-ttu-id="891bb-110">Kohdistuksen lähde määrittää, mitkä kustannukset täytyy kohdistaa sekä kohdistustavoitteet määrittävät, missä kustannukset on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="891bb-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="891bb-111">Esimerkiksi kohdistuksen lähde voi olla Sähkö ja lämmitys -kustannuslajin kustannukset.</span><span class="sxs-lookup"><span data-stu-id="891bb-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="891bb-112">Kohdista kaikki sähkö ja lämmityskustannukset kolmeen kustannuspaikkaan: korjaamo, tuotanto ja myynti.</span><span class="sxs-lookup"><span data-stu-id="891bb-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="891bb-113">Näihin kustannuspaikkoihin kohdistetaan kohteita.</span><span class="sxs-lookup"><span data-stu-id="891bb-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="891bb-114">Määritä jokaiselle kohdistuksen lähteelle kohdistustaso, voimassaoloaika ja variantti ryhmittelyn tunnukseksi.</span><span class="sxs-lookup"><span data-stu-id="891bb-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="891bb-115">Erätyön avulla voit määrittää suodattimia valitaksesi kohdistusmääritelmiä ja suorittaaksesi sitten kustannusten kohdistukset automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="891bb-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="891bb-116">Määritä jokaiselle kohdistuksen kohteelle kohdistusperuste.</span><span class="sxs-lookup"><span data-stu-id="891bb-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="891bb-117">Kohdistusperuste voi olla joko staattinen tai dynaaminen.</span><span class="sxs-lookup"><span data-stu-id="891bb-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="891bb-118">Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="891bb-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="891bb-119">Dynaaminen kohdistus perustuu muutettaviin arvoihin, kuten työntekijöiden määrään kustannuspaikassa, kustannuskohteen myyntituottoihin tiettynä aikajaksona.</span><span class="sxs-lookup"><span data-stu-id="891bb-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="891bb-120">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="891bb-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="891bb-121">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="891bb-121">To</span></span>|<span data-ttu-id="891bb-122">Katso</span><span class="sxs-lookup"><span data-stu-id="891bb-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="891bb-123">Kohdistuksen lähteen ja sen tavoitteiden määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="891bb-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="891bb-124">Kohdistuksen lähteen ja sen tavoitteiden määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="891bb-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="891bb-125">Määrittää useita suodattimia dynaamisen kohdistuksen perusteille.</span><span class="sxs-lookup"><span data-stu-id="891bb-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="891bb-126">Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.</span><span class="sxs-lookup"><span data-stu-id="891bb-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="891bb-127">Esimerkki siitä, miten voit määrittää staattista kohdistamista.</span><span class="sxs-lookup"><span data-stu-id="891bb-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="891bb-128">Esimerkkiskenaario: Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="891bb-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="891bb-129">Esimerkki siitä, miten voit määrittää dynaamista kohdistamista.</span><span class="sxs-lookup"><span data-stu-id="891bb-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="891bb-130">Esimerkkiskenaario: Määrittämällä myytyihin nimikkeisiin perustuvat dynaamiset kohdistamiset</span><span class="sxs-lookup"><span data-stu-id="891bb-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="891bb-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="891bb-131">See Also</span></span>  
 <span data-ttu-id="891bb-132">[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="891bb-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="891bb-133">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="891bb-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="891bb-134">[Kustannuslaskenta](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="891bb-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="891bb-135">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="891bb-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="891bb-136">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="891bb-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

