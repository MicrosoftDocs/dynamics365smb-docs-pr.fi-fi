---
title: "Rakennetiedot – Koodiyksikön 408 dimension hallinta | Microsoft Docs"
description: "Koodiyksikkö 408, dimension hallinta on toimintokirjasto, joka käsittelee yleiset dimensioihin liittyvät tehtävät, kuten kopioinnin taulukosta toiseen tai yhdestä asiakirjasta toiseen."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 32f67c058570f03d4aa1c84d9bb32289b1f07bec
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="782a8-103">Rakennetiedot: koodiyksikön 408 dimension hallinta</span><span class="sxs-lookup"><span data-stu-id="782a8-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="782a8-104">Koodiyksikkö 408, dimension hallinta on toimintokirjasto, joka käsittelee yleiset dimensioihin liittyvät tehtävät, kuten kopioinnin taulukosta toiseen tai yhdestä asiakirjasta toiseen.</span><span class="sxs-lookup"><span data-stu-id="782a8-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="782a8-105">Tässä ohjeaiheessa luetellaan Microsoft Dynamics NAV 2013 Rs:ssa muutetut toiminnot ja määritetään toimintoihin tehdyt muutokset.</span><span class="sxs-lookup"><span data-stu-id="782a8-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="782a8-106">Monet toiminnot on poistettu, koska dimensiotaulukoiden välillä ei tarvitse kopioida.</span><span class="sxs-lookup"><span data-stu-id="782a8-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="782a8-107">Muutetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="782a8-107">Modified Functions</span></span>  

|<span data-ttu-id="782a8-108">Funktion nimi</span><span class="sxs-lookup"><span data-stu-id="782a8-108">Function Name</span></span>|<span data-ttu-id="782a8-109">Muutoksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="782a8-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="782a8-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="782a8-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="782a8-111">Uusi toiminto, joka korvaa muut tarkastustoiminnot ja ottaa dimensioyhdistelmän tunnuksen argumenttina dimensiotaulukon asemasta.</span><span class="sxs-lookup"><span data-stu-id="782a8-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="782a8-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="782a8-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="782a8-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="782a8-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="782a8-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="782a8-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="782a8-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="782a8-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="782a8-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="782a8-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="782a8-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="782a8-117">CheckDimValueComb</span></span>|<span data-ttu-id="782a8-118">Poista.</span><span class="sxs-lookup"><span data-stu-id="782a8-118">Delete.</span></span> <span data-ttu-id="782a8-119">Kaikki käyttö tulisi muuttaa arvoon CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="782a8-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="782a8-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="782a8-120">GetDefaultDim</span></span>|<span data-ttu-id="782a8-121">Muuta palauttamaan dimensioyhdistelmän tunnus kokonaisluku-muodossa tietuejoukon sijasta.</span><span class="sxs-lookup"><span data-stu-id="782a8-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="782a8-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="782a8-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="782a8-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="782a8-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="782a8-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="782a8-126">Muokkaa toimimaan: DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="782a8-127">Poistetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="782a8-127">Deleted Functions</span></span>  
 <span data-ttu-id="782a8-128">Alla luetellaan toiminnot, jotka on poistettu 408-koodiyksikön dimensioyhdistelmän tapahtumat -ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="782a8-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="782a8-129">Kun sovelluksen koodia päivitetään Microsoft Dynamics NAV 2009:stä tai sitä aiemmasta versiosta Microsoft Dynamics NAV 2016:een, seuraavat toiminnot eivät ole käytettävissä Microsoft Dynamics NAV:ssa.</span><span class="sxs-lookup"><span data-stu-id="782a8-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="782a8-130">Jos olet tehnyt mukautuksia, jotka käyttävät yhtä tai useampaa seuraavista toiminnoista, mukautuksesi on päivitettävä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="782a8-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="782a8-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="782a8-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="782a8-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="782a8-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="782a8-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="782a8-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="782a8-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="782a8-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="782a8-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="782a8-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-136">InsertDocDim</span></span>  

 <span data-ttu-id="782a8-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="782a8-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="782a8-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="782a8-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="782a8-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="782a8-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="782a8-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="782a8-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="782a8-141">InsertServContractDim</span></span>  

 <span data-ttu-id="782a8-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="782a8-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="782a8-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="782a8-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="782a8-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-144">GetDocDim</span></span>  

 <span data-ttu-id="782a8-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-145">GetProdDocDim</span></span>  

 <span data-ttu-id="782a8-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="782a8-146">TypeToTableID1</span></span>  

 <span data-ttu-id="782a8-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="782a8-147">TypeToTableID2</span></span>  

 <span data-ttu-id="782a8-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="782a8-148">TypeToTableID3</span></span>  

 <span data-ttu-id="782a8-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="782a8-149">TypeToTableID4</span></span>  

 <span data-ttu-id="782a8-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="782a8-150">TypeToTableID5</span></span>  

 <span data-ttu-id="782a8-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="782a8-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-152">DeleteDocDim</span></span>  

 <span data-ttu-id="782a8-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="782a8-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="782a8-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="782a8-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="782a8-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="782a8-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="782a8-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="782a8-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="782a8-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="782a8-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="782a8-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-160">ShowDocDim</span></span>  

 <span data-ttu-id="782a8-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-161">SaveDocDim</span></span>  

 <span data-ttu-id="782a8-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="782a8-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="782a8-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="782a8-164">ShowTempDim</span></span>  

 <span data-ttu-id="782a8-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="782a8-165">SaveTempDim</span></span>  

 <span data-ttu-id="782a8-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="782a8-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="782a8-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="782a8-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="782a8-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="782a8-168">SaveServContractDim</span></span>  

 <span data-ttu-id="782a8-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="782a8-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="782a8-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="782a8-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="782a8-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="782a8-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="782a8-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="782a8-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="782a8-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="782a8-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="782a8-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="782a8-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="782a8-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="782a8-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="782a8-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="782a8-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="782a8-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="782a8-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="782a8-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="782a8-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="782a8-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="782a8-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="782a8-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="782a8-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="782a8-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="782a8-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="782a8-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="782a8-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="782a8-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="782a8-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="782a8-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="782a8-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="782a8-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="782a8-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="782a8-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="782a8-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="782a8-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="782a8-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="782a8-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="782a8-198">TestDimValue</span></span>  

 <span data-ttu-id="782a8-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="782a8-199">TestNewDimValue</span></span>  

 <span data-ttu-id="782a8-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="782a8-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="782a8-201">(Poista, koska ItemBudgetDim-taulukko poistetaan.)</span><span class="sxs-lookup"><span data-stu-id="782a8-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="782a8-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="782a8-202">GetServContractDim</span></span>  

 <span data-ttu-id="782a8-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="782a8-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="782a8-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="782a8-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="782a8-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="782a8-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="782a8-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="782a8-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="782a8-207">Katso myös</span><span class="sxs-lookup"><span data-stu-id="782a8-207">See Also</span></span>
 <span data-ttu-id="782a8-208">[Rakennetiedot: dimensioyhdistelmä-tapahtumat](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="782a8-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="782a8-209">[Rakennetiedot: Dimensioyhdistelmätapahtumien yleiskatsaus](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="782a8-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="782a8-210">[Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="782a8-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="782a8-211">[Rakennetiedot: taulukkorakenne](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="782a8-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="782a8-212">Rakennetiedot: koodiesimerkkejä muuttuneista kuvioista muutoksissa</span><span class="sxs-lookup"><span data-stu-id="782a8-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

