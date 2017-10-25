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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 050b0bd997629ca189cfbe035e361de7a252d079
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="fbb6f-104">Kustannusten määrittäminen ja kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="fbb6f-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="fbb6f-105">Kustannusten kohdistukset siirtävät kustannuksia ja tuottoja eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="fbb6f-106">Voit määrittää niin monta kodhistusta kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="fbb6f-107">Jokainen kohdistus koostuu:</span><span class="sxs-lookup"><span data-stu-id="fbb6f-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="fbb6f-108">Kohdistamisen lähde.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-108">An allocation source.</span></span>  
-   <span data-ttu-id="fbb6f-109">Vähintään yksi kohdistuskohde.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-109">One or more allocation targets.</span></span>  

<span data-ttu-id="fbb6f-110">Kohdistuksen lähde määrittää, mitkä kustannukset täytyy kohdistaa sekä kohdistustavoitteet määrittävät, missä kustannukset on kohdistettava.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="fbb6f-111">Esimerkiksi kohdistuksen lähde voi olla Sähkö ja lämmitys -kustannuslajin kustannukset.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="fbb6f-112">Kohdista kaikki sähkö ja lämmityskustannukset kolmeen kustannuspaikkaan: korjaamo, tuotanto ja myynti.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="fbb6f-113">Näihin kustannuspaikkoihin kohdistetaan kohteita.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="fbb6f-114">Määritä jokaiselle kohdistuksen lähteelle kohdistustaso, voimassaoloaika ja variantti ryhmittelyn tunnukseksi.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="fbb6f-115">Erätyön avulla voit määrittää suodattimia valitaksesi kohdistusmääritelmiä ja suorittaaksesi sitten kustannusten kohdistukset automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="fbb6f-116">Määritä jokaiselle kohdistuksen kohteelle kohdistusperuste.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="fbb6f-117">Kohdistusperuste voi olla joko staattinen tai dynaaminen.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="fbb6f-118">Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="fbb6f-119">Dynaaminen kohdistus perustuu muutettaviin arvoihin, kuten työntekijöiden määrään kustannuspaikassa, kustannuskohteen myyntituottoihin tiettynä aikajaksona.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="fbb6f-120">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="fbb6f-121">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="fbb6f-121">To</span></span>|<span data-ttu-id="fbb6f-122">Katso</span><span class="sxs-lookup"><span data-stu-id="fbb6f-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="fbb6f-123">Kohdistuksen lähteen ja sen tavoitteiden määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="fbb6f-124">Kohdistuksen lähteen ja tavoitteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fbb6f-124">How to: Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="fbb6f-125">Määrittää useita suodattimia dynaamisen kohdistuksen perusteille.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="fbb6f-126">Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="fbb6f-127">Esimerkki siitä, miten voit määrittää staattista kohdistamista.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="fbb6f-128">Esimerkkiskenaario: Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fbb6f-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="fbb6f-129">Esimerkki siitä, miten voit määrittää dynaamista kohdistamista.</span><span class="sxs-lookup"><span data-stu-id="fbb6f-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="fbb6f-130">Esimerkkiskenaario: Määrittämällä myytyihin nimikkeisiin perustuvat dynaamiset kohdistamiset</span><span class="sxs-lookup"><span data-stu-id="fbb6f-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="fbb6f-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fbb6f-131">See Also</span></span>  
 <span data-ttu-id="fbb6f-132">[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="fbb6f-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="fbb6f-133">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="fbb6f-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="fbb6f-134">[Kustannuslaskenta](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="fbb6f-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="fbb6f-135">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="fbb6f-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="fbb6f-136">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="fbb6f-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

