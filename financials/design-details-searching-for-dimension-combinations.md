---
title: "Rakennetiedot – Dimensioyhdistelmien etsiminen | Microsoft Docs"
description: "Kun suljet ikkunan dimensioyhdistelmän muokkaamisen jälkeen, Finance and Operations, Business edition arvioi, onko muokattu dimensiojoukko olemassa. Jos yhdistelmää ei ole olemassa, järjestelmän luo uuden ja palauttaa dimensioyhdistelmän tunnuksen."
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
ms.openlocfilehash: 821ddebee02d1ea922c0c13a181ae0e29e4eb40e
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="27bc9-104">Rakennetiedot: dimensioyhdistelmien etsiminen</span><span class="sxs-lookup"><span data-stu-id="27bc9-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="27bc9-105">Kun suljet ikkunan dimensioyhdistelmän muokkaamisen jälkeen, [!INCLUDE[d365fin](includes/d365fin_md.md)] arvioi, onko muokattu dimensiojoukko olemassa.</span><span class="sxs-lookup"><span data-stu-id="27bc9-105">When you close a window after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="27bc9-106">Jos yhdistelmää ei ole olemassa, järjestelmän luo uuden ja palauttaa dimensioyhdistelmän tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="27bc9-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="27bc9-107">Rakennetaan hakupuuta</span><span class="sxs-lookup"><span data-stu-id="27bc9-107">Building Search Tree</span></span>  
 <span data-ttu-id="27bc9-108">Taulukkoa 481 **Dimensionasetuksen puusolmu** käytetään, kun [!INCLUDE[d365fin](includes/d365fin_md.md)] arvioi onko dimensiosarja jo olemassa taulukossa 480 **Dimensionasetuskirjaus**.</span><span class="sxs-lookup"><span data-stu-id="27bc9-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="27bc9-109">Arviointi suoritetaan kulkemalla hakupuu läpi rekursiivisesti aloittaen ylätason numerosta 0.</span><span class="sxs-lookup"><span data-stu-id="27bc9-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="27bc9-110">Ylätason 0 edustaa dimensiosarjaa, jossa ei ole dimensiosarjan kirjauksia.</span><span class="sxs-lookup"><span data-stu-id="27bc9-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="27bc9-111">Tämän dimensiosarjan jälkeläiset edustavat dimensiosarjoja, joilla on vain yksi dimensiosarjan kirjaus.</span><span class="sxs-lookup"><span data-stu-id="27bc9-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="27bc9-112">Näiden dimensiosarjojen jälkeläiset edustavat dimensiosarjoja, joilla on kaksi jälkeläistä jne.</span><span class="sxs-lookup"><span data-stu-id="27bc9-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="27bc9-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="27bc9-113">Example 1</span></span>  
 <span data-ttu-id="27bc9-114">Seuraava kaavio esittelee hakupuun ja kuusi dimensiosarjaa.</span><span class="sxs-lookup"><span data-stu-id="27bc9-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="27bc9-115">Kaaviossa näkyy vain erottava dimensioyhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="27bc9-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="27bc9-116">![Dimension puurakenne](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")</span><span class="sxs-lookup"><span data-stu-id="27bc9-116">![Dimension tree structure](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")</span></span>  

 <span data-ttu-id="27bc9-117">Seuraavassa taulukossa kuvataan koko dimensiosarjan kirjausten luettelo, joka muodostaa kunkin dimensiosarjan.</span><span class="sxs-lookup"><span data-stu-id="27bc9-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="27bc9-118">Dimensioyhdistelmät</span><span class="sxs-lookup"><span data-stu-id="27bc9-118">Dimension Sets</span></span>|<span data-ttu-id="27bc9-119">Dimensioyhdistelmän tapahtumat</span><span class="sxs-lookup"><span data-stu-id="27bc9-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="27bc9-120">Aseta 0</span><span class="sxs-lookup"><span data-stu-id="27bc9-120">Set 0</span></span>|<span data-ttu-id="27bc9-121">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="27bc9-121">None</span></span>|  
|<span data-ttu-id="27bc9-122">Aseta 1</span><span class="sxs-lookup"><span data-stu-id="27bc9-122">Set 1</span></span>|<span data-ttu-id="27bc9-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="27bc9-123">AREA 30</span></span>|  
|<span data-ttu-id="27bc9-124">Aseta 2</span><span class="sxs-lookup"><span data-stu-id="27bc9-124">Set 2</span></span>|<span data-ttu-id="27bc9-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="27bc9-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="27bc9-126">Aseta 3</span><span class="sxs-lookup"><span data-stu-id="27bc9-126">Set 3</span></span>|<span data-ttu-id="27bc9-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="27bc9-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="27bc9-128">Aseta 4</span><span class="sxs-lookup"><span data-stu-id="27bc9-128">Set 4</span></span>|<span data-ttu-id="27bc9-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="27bc9-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="27bc9-130">Aseta 5</span><span class="sxs-lookup"><span data-stu-id="27bc9-130">Set 5</span></span>|<span data-ttu-id="27bc9-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="27bc9-131">AREA 40</span></span>|  
|<span data-ttu-id="27bc9-132">Aseta 6</span><span class="sxs-lookup"><span data-stu-id="27bc9-132">Set 6</span></span>|<span data-ttu-id="27bc9-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="27bc9-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="27bc9-134">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="27bc9-134">Example 2</span></span>  
 <span data-ttu-id="27bc9-135">Tämä esimerkki osoittaa, miten [!INCLUDE[d365fin](includes/d365fin_md.md)] arvioi, onko dimensioyhdistelmän tapahtumat AREA 40 ja DEPT PROD sisältävä dimensioyhdistelmä olemassa.</span><span class="sxs-lookup"><span data-stu-id="27bc9-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="27bc9-136">[!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa ensin päivittämällä **Dimensioyhdistelmän puusolmu** -taulukon, että hakupuu näyttää samalta kuin seuraavassa kaaviossa.</span><span class="sxs-lookup"><span data-stu-id="27bc9-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="27bc9-137">Dimensioyhdistelmästä 7 tulee dimensioyhdistelmän 5 alitaso.</span><span class="sxs-lookup"><span data-stu-id="27bc9-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="27bc9-138">![NAV2013-dimensiopuu, esimerkki 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")</span><span class="sxs-lookup"><span data-stu-id="27bc9-138">![NAV2013&#95;Dimension&#95;Tree&#95;Example 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="27bc9-139">Dimensioyhdistelmän tunnuksen etsiminen</span><span class="sxs-lookup"><span data-stu-id="27bc9-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="27bc9-140">Käsitteellisellä tasolla hakupuun **Päätunnus**, **Dimensio** ja **Dimensioarvo** yhdistetään ja niitä käytetään perusavaimena, koska [!INCLUDE[d365fin](includes/d365fin_md.md)] kulkee puussa samassa järjestyksessä kuin dimensiotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="27bc9-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="27bc9-141">GET-toimintoa (tietue) käytetään etsimään dimensiosarjan tunnusta.</span><span class="sxs-lookup"><span data-stu-id="27bc9-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="27bc9-142">Seuraava koodiesimerkki osoittaa, kuinka löydetään dimensiosarjan tunnus, kun dimensioarvoja on kolme.</span><span class="sxs-lookup"><span data-stu-id="27bc9-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

 <span data-ttu-id="27bc9-143">Jotta [!INCLUDE[d365fin](includes/d365fin_md.md)] voisi kuitenkin edelleen nimetä dimension ja dimensioarvon uudelleen, taulukkoa 348 **Dimensioarvo** laajennetaan **Dimensioarvon tunnus** -kokonaisluku-kentällä.</span><span class="sxs-lookup"><span data-stu-id="27bc9-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename a dimension and dimension value, table 348 **Dimension Value** is extended with an integer field of **Dimension Value ID**.</span></span> <span data-ttu-id="27bc9-144">Tämä taulukko muuntaa kenttäparin **Dimensio** ja **Dimension arvo** kokonaislukuarvoksi.</span><span class="sxs-lookup"><span data-stu-id="27bc9-144">This table converts the field pair **Dimension** and **Dimension Value** to an integer value.</span></span> <span data-ttu-id="27bc9-145">Kun nimeät dimension ja dimension arvon, kokonaislukuarvoa ei muuteta.</span><span class="sxs-lookup"><span data-stu-id="27bc9-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="27bc9-146">Katso myös</span><span class="sxs-lookup"><span data-stu-id="27bc9-146">See Also</span></span>  
 <span data-ttu-id="27bc9-147">[GET-funktio (tietue)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="27bc9-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="27bc9-148">[Rakennetiedot: Dimensioyhdistelmätapahtumat](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="27bc9-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="27bc9-149">[Dimensioyhdistelmätapahtumien yleiskuva](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="27bc9-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="27bc9-150">[Rakennetiedot: taulukkorakenne](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="27bc9-150">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 <span data-ttu-id="27bc9-151">[Rakennetiedot: Koodiyksikön 408 dimension hallinta](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="27bc9-151">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
 [<span data-ttu-id="27bc9-152">Rakennetiedot: koodiesimerkkejä muuttuneista kuvioista muutoksissa</span><span class="sxs-lookup"><span data-stu-id="27bc9-152">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

