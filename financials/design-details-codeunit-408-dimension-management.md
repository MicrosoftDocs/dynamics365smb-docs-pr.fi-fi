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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a811c565a8eb0ce774d35d15776e65b6dce6a31a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="00f5f-103">Rakennetiedot: koodiyksikön 408 dimension hallinta</span><span class="sxs-lookup"><span data-stu-id="00f5f-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="00f5f-104">Koodiyksikkö 408, dimension hallinta on toimintokirjasto, joka käsittelee yleiset dimensioihin liittyvät tehtävät, kuten kopioinnin taulukosta toiseen tai yhdestä asiakirjasta toiseen.</span><span class="sxs-lookup"><span data-stu-id="00f5f-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="00f5f-105">Tässä ohjeaiheessa luetellaan Microsoft Dynamics NAV 2013 Rs:ssa muutetut toiminnot ja määritetään toimintoihin tehdyt muutokset.</span><span class="sxs-lookup"><span data-stu-id="00f5f-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="00f5f-106">Monet toiminnot on poistettu, koska dimensiotaulukoiden välillä ei tarvitse kopioida.</span><span class="sxs-lookup"><span data-stu-id="00f5f-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="00f5f-107">Muutetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="00f5f-107">Modified Functions</span></span>  

|<span data-ttu-id="00f5f-108">Funktion nimi</span><span class="sxs-lookup"><span data-stu-id="00f5f-108">Function Name</span></span>|<span data-ttu-id="00f5f-109">Muutoksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="00f5f-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="00f5f-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="00f5f-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="00f5f-111">Uusi toiminto, joka korvaa muut tarkastustoiminnot ja ottaa dimensioyhdistelmän tunnuksen argumenttina dimensiotaulukon asemasta.</span><span class="sxs-lookup"><span data-stu-id="00f5f-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="00f5f-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="00f5f-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="00f5f-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="00f5f-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="00f5f-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="00f5f-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="00f5f-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="00f5f-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="00f5f-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="00f5f-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="00f5f-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="00f5f-117">CheckDimValueComb</span></span>|<span data-ttu-id="00f5f-118">Poista.</span><span class="sxs-lookup"><span data-stu-id="00f5f-118">Delete.</span></span> <span data-ttu-id="00f5f-119">Kaikki käyttö tulisi muuttaa arvoon CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="00f5f-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="00f5f-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-120">GetDefaultDim</span></span>|<span data-ttu-id="00f5f-121">Muuta palauttamaan dimensioyhdistelmän tunnus kokonaisluku-muodossa tietuejoukon sijasta.</span><span class="sxs-lookup"><span data-stu-id="00f5f-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="00f5f-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="00f5f-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="00f5f-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="00f5f-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="00f5f-126">Muokkaa toimimaan: DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="00f5f-127">Poistetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="00f5f-127">Deleted Functions</span></span>  
 <span data-ttu-id="00f5f-128">Alla luetellaan toiminnot, jotka on poistettu 408-koodiyksikön dimensioyhdistelmän tapahtumat -ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="00f5f-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="00f5f-129">Kun sovelluksen koodia päivitetään Microsoft Dynamics NAV 2009:stä tai sitä aiemmasta versiosta Microsoft Dynamics NAV 2016:een, seuraavat toiminnot eivät ole käytettävissä Microsoft Dynamics NAV:ssa.</span><span class="sxs-lookup"><span data-stu-id="00f5f-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="00f5f-130">Jos olet tehnyt mukautuksia, jotka käyttävät yhtä tai useampaa seuraavista toiminnoista, mukautuksesi on päivitettävä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="00f5f-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="00f5f-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="00f5f-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="00f5f-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="00f5f-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="00f5f-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-136">InsertDocDim</span></span>  

 <span data-ttu-id="00f5f-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="00f5f-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="00f5f-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="00f5f-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="00f5f-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-141">InsertServContractDim</span></span>  

 <span data-ttu-id="00f5f-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="00f5f-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="00f5f-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="00f5f-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-144">GetDocDim</span></span>  

 <span data-ttu-id="00f5f-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-145">GetProdDocDim</span></span>  

 <span data-ttu-id="00f5f-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="00f5f-146">TypeToTableID1</span></span>  

 <span data-ttu-id="00f5f-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="00f5f-147">TypeToTableID2</span></span>  

 <span data-ttu-id="00f5f-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="00f5f-148">TypeToTableID3</span></span>  

 <span data-ttu-id="00f5f-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="00f5f-149">TypeToTableID4</span></span>  

 <span data-ttu-id="00f5f-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="00f5f-150">TypeToTableID5</span></span>  

 <span data-ttu-id="00f5f-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-152">DeleteDocDim</span></span>  

 <span data-ttu-id="00f5f-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="00f5f-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="00f5f-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="00f5f-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="00f5f-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="00f5f-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-160">ShowDocDim</span></span>  

 <span data-ttu-id="00f5f-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-161">SaveDocDim</span></span>  

 <span data-ttu-id="00f5f-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="00f5f-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="00f5f-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-164">ShowTempDim</span></span>  

 <span data-ttu-id="00f5f-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-165">SaveTempDim</span></span>  

 <span data-ttu-id="00f5f-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="00f5f-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="00f5f-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-168">SaveServContractDim</span></span>  

 <span data-ttu-id="00f5f-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="00f5f-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="00f5f-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="00f5f-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="00f5f-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="00f5f-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="00f5f-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="00f5f-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="00f5f-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="00f5f-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="00f5f-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="00f5f-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="00f5f-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="00f5f-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="00f5f-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="00f5f-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="00f5f-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="00f5f-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="00f5f-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="00f5f-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="00f5f-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="00f5f-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="00f5f-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="00f5f-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="00f5f-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="00f5f-198">TestDimValue</span></span>  

 <span data-ttu-id="00f5f-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="00f5f-199">TestNewDimValue</span></span>  

 <span data-ttu-id="00f5f-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="00f5f-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="00f5f-201">(Poista, koska ItemBudgetDim-taulukko poistetaan.</span><span class="sxs-lookup"><span data-stu-id="00f5f-201">(Delete because the ItemBudgetDim Table is deleted.</span></span>  

 <span data-ttu-id="00f5f-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-202">GetServContractDim</span></span>  

 <span data-ttu-id="00f5f-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="00f5f-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="00f5f-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="00f5f-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="00f5f-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="00f5f-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="00f5f-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="00f5f-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="00f5f-207">Katso myös</span><span class="sxs-lookup"><span data-stu-id="00f5f-207">See Also</span></span>
 <span data-ttu-id="00f5f-208">[Rakennetiedot: dimensioyhdistelmä-tapahtumat](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="00f5f-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="00f5f-209">[Rakennetiedot: Dimensioyhdistelmätapahtumien yleiskatsaus](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="00f5f-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="00f5f-210">[Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="00f5f-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="00f5f-211">[Rakennetiedot: taulukkorakenne](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="00f5f-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="00f5f-212">Rakennetiedot: koodiesimerkkejä muuttuneista kuvioista muutoksissa</span><span class="sxs-lookup"><span data-stu-id="00f5f-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

