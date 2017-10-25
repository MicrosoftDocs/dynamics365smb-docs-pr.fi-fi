---
title: "Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen | Microsoft Docs"
description: "Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4."
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
ms.openlocfilehash: b48d7f73b640b98d0cdab6e2e7e7486a3bdb39db
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="48708-103">Esimerkkiskenaario: Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="48708-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="48708-104">Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="48708-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="48708-105">Tässä aiheessa kuvataan, miten määrittää kolmen uuden kohdistuskohteen kustannuskohteet TUOT kustannuspaikoille käyttäen vahvistettu-varaus -suhdetta 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="48708-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="48708-106">Kolme kohdekustannuskohdetta ovat LISÄLAITT, MAALIT ja KALUSTO.</span><span class="sxs-lookup"><span data-stu-id="48708-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="48708-107">Esimerkissä käytetään demodataa [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta.</span><span class="sxs-lookup"><span data-stu-id="48708-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="48708-108">Määritä varauksen lähde TUOT kustannuspaikka yleisessä pikavälilehdessä</span><span class="sxs-lookup"><span data-stu-id="48708-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="48708-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannusten kohdistaminen** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="48708-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48708-110">Valitse **Kustannusten kohdistaminen** -ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="48708-110">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="48708-111">Paina **Tunnus**-kentässä Enter tai kirjoita tunnus.</span><span class="sxs-lookup"><span data-stu-id="48708-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="48708-112">Syötä **Taso**-kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="48708-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="48708-113">Syötä arvot **Voimassaolo alkaa**- ja **Voimassaolo päättyy** -kenttiin.</span><span class="sxs-lookup"><span data-stu-id="48708-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="48708-114">Syötä **Kustanuspaikkakoodi**-kenttään **TUOT**.</span><span class="sxs-lookup"><span data-stu-id="48708-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="48708-115">Syötä **Luotto kustannustyyppiin** -kenttään kustannustyyppi **9903**.</span><span class="sxs-lookup"><span data-stu-id="48708-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="48708-116">Määritä kodhistuskohteen kustannus-objektit Rivit-pikavälilehdellä</span><span class="sxs-lookup"><span data-stu-id="48708-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="48708-117">Syötä laskun ensimmäiselle riville **Kohdekustannustyyppi**-kenttään **9903**.</span><span class="sxs-lookup"><span data-stu-id="48708-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="48708-118">Syötä ensimmäiselle riville **Kohdekustannuskohde**-kenttään **LISÄLAITT**.</span><span class="sxs-lookup"><span data-stu-id="48708-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="48708-119">Valitse ensimmäisen rivin **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="48708-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="48708-120">Valitse ensimmäisen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="48708-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="48708-121">Anna ensimmäisen rivin **Jaa**-kentässä varaussuhde **5**.</span><span class="sxs-lookup"><span data-stu-id="48708-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="48708-122">Syötä toiselle riville **Kohdekustannustyyppi**-kenttään **9903**.</span><span class="sxs-lookup"><span data-stu-id="48708-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="48708-123">Syötä toiselle riville **Kohdekustannuskohde**-kenttään **MAALI**.</span><span class="sxs-lookup"><span data-stu-id="48708-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="48708-124">Valitse toiselle riville **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="48708-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="48708-125">Valitse toisen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="48708-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="48708-126">Anna toisen rivin **Jaa**-kentässä varaussuhde **2**.</span><span class="sxs-lookup"><span data-stu-id="48708-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="48708-127">Syötä kolmannelle riville **Kohdekustannustyyppi**-kenttään **9903**.</span><span class="sxs-lookup"><span data-stu-id="48708-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="48708-128">Syötä kolmannelle riville **Kohdekustannuskohde**-kenttään **KALUSTO**.</span><span class="sxs-lookup"><span data-stu-id="48708-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="48708-129">Valitse kolmannen rivin **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="48708-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="48708-130">Valitse kolmannen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="48708-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="48708-131">Anna kolmannen rivin **Jaa**-kentässä varaussuhde **4**.</span><span class="sxs-lookup"><span data-stu-id="48708-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="48708-132"> laskee automaattisesti **Prosentti**-kenttään prosenttiarvon, joka määräytyy kaikkien niiden kolmen kohdistussuhteen mukaan, jotka syötetty **Osuus**-kenttään kaikilla kolmella rivillä.</span><span class="sxs-lookup"><span data-stu-id="48708-132"> automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="48708-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="48708-133">See Also</span></span>  
<span data-ttu-id="48708-134">[Kohdistuksen lähteen ja tavoitteiden määrittäminen](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="48708-134">[How to: Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
<span data-ttu-id="48708-135">[Kustannusten määrittäminen ja kohdistaminen](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="48708-135">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
<span data-ttu-id="48708-136">[Esimerkkiskenaario: Myytyihin nimikkeisiin perustuvien dynaamisten kohdistusten määrittäminen](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span><span class="sxs-lookup"><span data-stu-id="48708-136">[Scenario Example: Defining Dynamic Allocations Based on Items Sold](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span></span>  
[<span data-ttu-id="48708-137">Kustannusten määrittäminen ja kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="48708-137">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)

