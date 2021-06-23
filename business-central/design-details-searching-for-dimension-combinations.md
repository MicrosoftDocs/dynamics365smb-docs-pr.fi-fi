---
title: Rakennetiedot – Dimensioyhdistelmien etsiminen | Microsoft Docs
description: Kun suljet sivun dimensioyhdistelmän muokkaamisen jälkeen, Business Central arvioi, onko muokattu dimensiojoukko olemassa. Jos yhdistelmää ei ole olemassa, järjestelmän luo uuden ja palauttaa dimensioyhdistelmän tunnuksen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 544cb3a1844aaf85ab937031a23d6d00506ffa74
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215751"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="5ead0-104">Rakennetiedot: dimensioyhdistelmien etsiminen</span><span class="sxs-lookup"><span data-stu-id="5ead0-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="5ead0-105">Kun suljet sivun dimensioyhdistelmän muokkaamisen jälkeen, [!INCLUDE[prod_short](includes/prod_short.md)] arvioi, onko muokattu dimensiojoukko olemassa.</span><span class="sxs-lookup"><span data-stu-id="5ead0-105">When you close a page after you edit a set of dimensions, [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="5ead0-106">Jos yhdistelmää ei ole olemassa, järjestelmän luo uuden ja palauttaa dimensioyhdistelmän tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="5ead0-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="5ead0-107">Rakennetaan hakupuuta</span><span class="sxs-lookup"><span data-stu-id="5ead0-107">Building Search Tree</span></span>  
 <span data-ttu-id="5ead0-108">Taulukkoa 481 **Dimensionasetuksen puusolmu** käytetään, kun [!INCLUDE[prod_short](includes/prod_short.md)] arvioi onko dimensiosarja jo olemassa taulukossa 480 **Dimensionasetuskirjaus**.</span><span class="sxs-lookup"><span data-stu-id="5ead0-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="5ead0-109">Arviointi suoritetaan kulkemalla hakupuu läpi rekursiivisesti aloittaen ylätason numerosta 0.</span><span class="sxs-lookup"><span data-stu-id="5ead0-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="5ead0-110">Ylätason 0 edustaa dimensiosarjaa, jossa ei ole dimensiosarjan kirjauksia.</span><span class="sxs-lookup"><span data-stu-id="5ead0-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="5ead0-111">Tämän dimensiosarjan jälkeläiset edustavat dimensiosarjoja, joilla on vain yksi dimensiosarjan kirjaus.</span><span class="sxs-lookup"><span data-stu-id="5ead0-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="5ead0-112">Näiden dimensiosarjojen jälkeläiset edustavat dimensiosarjoja, joilla on kaksi jälkeläistä jne.</span><span class="sxs-lookup"><span data-stu-id="5ead0-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="5ead0-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="5ead0-113">Example 1</span></span>  
 <span data-ttu-id="5ead0-114">Seuraava kaavio esittelee hakupuun ja kuusi dimensiosarjaa.</span><span class="sxs-lookup"><span data-stu-id="5ead0-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="5ead0-115">Kaaviossa näkyy vain erottava dimensioyhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="5ead0-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="5ead0-116">![Esimerkki dimension puurakenteesta](media/nav2013_dimension_tree.png "Esimerkki dimension puurakenteesta")</span><span class="sxs-lookup"><span data-stu-id="5ead0-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="5ead0-117">Seuraavassa taulukossa kuvataan koko dimensiosarjan kirjausten luettelo, joka muodostaa kunkin dimensiosarjan.</span><span class="sxs-lookup"><span data-stu-id="5ead0-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="5ead0-118">Dimensioyhdistelmät</span><span class="sxs-lookup"><span data-stu-id="5ead0-118">Dimension Sets</span></span>|<span data-ttu-id="5ead0-119">Dimensioyhdistelmän tapahtumat</span><span class="sxs-lookup"><span data-stu-id="5ead0-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="5ead0-120">Aseta 0</span><span class="sxs-lookup"><span data-stu-id="5ead0-120">Set 0</span></span>|<span data-ttu-id="5ead0-121">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="5ead0-121">None</span></span>|  
|<span data-ttu-id="5ead0-122">Aseta 1</span><span class="sxs-lookup"><span data-stu-id="5ead0-122">Set 1</span></span>|<span data-ttu-id="5ead0-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="5ead0-123">AREA 30</span></span>|  
|<span data-ttu-id="5ead0-124">Aseta 2</span><span class="sxs-lookup"><span data-stu-id="5ead0-124">Set 2</span></span>|<span data-ttu-id="5ead0-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="5ead0-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="5ead0-126">Aseta 3</span><span class="sxs-lookup"><span data-stu-id="5ead0-126">Set 3</span></span>|<span data-ttu-id="5ead0-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="5ead0-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="5ead0-128">Aseta 4</span><span class="sxs-lookup"><span data-stu-id="5ead0-128">Set 4</span></span>|<span data-ttu-id="5ead0-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="5ead0-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="5ead0-130">Aseta 5</span><span class="sxs-lookup"><span data-stu-id="5ead0-130">Set 5</span></span>|<span data-ttu-id="5ead0-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="5ead0-131">AREA 40</span></span>|  
|<span data-ttu-id="5ead0-132">Aseta 6</span><span class="sxs-lookup"><span data-stu-id="5ead0-132">Set 6</span></span>|<span data-ttu-id="5ead0-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="5ead0-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="5ead0-134">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="5ead0-134">Example 2</span></span>  
 <span data-ttu-id="5ead0-135">Tämä esimerkki osoittaa, miten [!INCLUDE[prod_short](includes/prod_short.md)] arvioi, onko dimensioyhdistelmän tapahtumat AREA 40 ja DEPT PROD sisältävä dimensioyhdistelmä olemassa.</span><span class="sxs-lookup"><span data-stu-id="5ead0-135">This example shows how [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="5ead0-136">[!INCLUDE[prod_short](includes/prod_short.md)] varmistaa ensin päivittämällä **Dimensioyhdistelmän puusolmu** -taulukon, että hakupuu näyttää samalta kuin seuraavassa kaaviossa.</span><span class="sxs-lookup"><span data-stu-id="5ead0-136">First, [!INCLUDE[prod_short](includes/prod_short.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="5ead0-137">Dimensioyhdistelmästä 7 tulee dimensioyhdistelmän 5 alitaso.</span><span class="sxs-lookup"><span data-stu-id="5ead0-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="5ead0-138">![Esimerkki dimension puurakenteesta NAV 2013 -sovelluksessa](media/nav2013_dimension_tree_example2.png "Esimerkki dimension puurakenteesta NAV 2013 -sovelluksessa")</span><span class="sxs-lookup"><span data-stu-id="5ead0-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="5ead0-139">Dimensioyhdistelmän tunnuksen etsiminen</span><span class="sxs-lookup"><span data-stu-id="5ead0-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="5ead0-140">Käsitteellisellä tasolla hakupuun **Päätunnus**, **Dimensio** ja **Dimensioarvo** yhdistetään ja niitä käytetään perusavaimena, koska [!INCLUDE[prod_short](includes/prod_short.md)] kulkee puussa samassa järjestyksessä kuin dimensiotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="5ead0-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[prod_short](includes/prod_short.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="5ead0-141">GET-toimintoa (tietue) käytetään etsimään dimensiosarjan tunnusta.</span><span class="sxs-lookup"><span data-stu-id="5ead0-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="5ead0-142">Seuraava koodiesimerkki osoittaa, kuinka löydetään dimensiosarjan tunnus, kun dimensioarvoja on kolme.</span><span class="sxs-lookup"><span data-stu-id="5ead0-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="5ead0-143">Jotta [!INCLUDE[prod_short](includes/prod_short.md)] voisi kuitenkin edelleen nimetä sekä dimension että dimensioarvon uudelleen, taulukkoa 349, **Dimensioarvo**, laajennetaan **Dimensioarvon tunnus** -kokonaislukukentällä.</span><span class="sxs-lookup"><span data-stu-id="5ead0-143">However, to preserve the ability of [!INCLUDE[prod_short](includes/prod_short.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="5ead0-144">Tämä taulukko muuntaa kenttäparin **Dimensio** ja **Dimension arvo** kokonaislukuarvoksi.</span><span class="sxs-lookup"><span data-stu-id="5ead0-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="5ead0-145">Kun nimeät dimension ja dimension arvon, kokonaislukuarvoa ei muuteta.</span><span class="sxs-lookup"><span data-stu-id="5ead0-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="5ead0-146">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5ead0-146">See Also</span></span>
    
 <span data-ttu-id="5ead0-147">[Rakennetiedot: dimensioyhdistelmä-tapahtumat](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="5ead0-147">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="5ead0-148">[Dimensioyhdistelmätapahtumien yleiskuva](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="5ead0-148">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 [<span data-ttu-id="5ead0-149">Rakennetiedot: taulukkorakenne</span><span class="sxs-lookup"><span data-stu-id="5ead0-149">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]
