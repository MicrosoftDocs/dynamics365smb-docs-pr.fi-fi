---
title: Rakennetiedot – Koodiyksikön 408 dimension hallinta | Microsoft Docs
description: Koodiyksikkö 408, dimension hallinta on toimintokirjasto, joka käsittelee yleiset dimensioihin liittyvät tehtävät, kuten kopioinnin taulukosta toiseen tai yhdestä asiakirjasta toiseen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-dimension-set-entries
ms.openlocfilehash: f725e5baea27b47399a50d041757fde83657673c
ms.sourcegitcommit: 1fa3d33db7bc71e3a27c826308a80ff24a436a72
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/30/2019
ms.locfileid: "1970968"
---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="ead4a-103">Rakennetiedot: koodiyksikön 408 dimension hallinta</span><span class="sxs-lookup"><span data-stu-id="ead4a-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="ead4a-104">Koodiyksikkö 408, dimension hallinta on toimintokirjasto, joka käsittelee yleiset dimensioihin liittyvät tehtävät, kuten kopioinnin taulukosta toiseen tai yhdestä asiakirjasta toiseen.</span><span class="sxs-lookup"><span data-stu-id="ead4a-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="ead4a-105">Tässä ohjeaiheessa luetellaan Microsoft Dynamics NAV 2013 Rs:ssa muutetut toiminnot ja määritetään toimintoihin tehdyt muutokset.</span><span class="sxs-lookup"><span data-stu-id="ead4a-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="ead4a-106">Monet toiminnot on poistettu, koska dimensiotaulukoiden välillä ei tarvitse kopioida.</span><span class="sxs-lookup"><span data-stu-id="ead4a-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="ead4a-107">Muutetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="ead4a-107">Modified Functions</span></span>  

|<span data-ttu-id="ead4a-108">Funktion nimi</span><span class="sxs-lookup"><span data-stu-id="ead4a-108">Function Name</span></span>|<span data-ttu-id="ead4a-109">Muutoksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="ead4a-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="ead4a-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="ead4a-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="ead4a-111">Uusi toiminto, joka korvaa muut tarkastustoiminnot ja ottaa dimensioyhdistelmän tunnuksen argumenttina dimensiotaulukon asemasta.</span><span class="sxs-lookup"><span data-stu-id="ead4a-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="ead4a-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="ead4a-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="ead4a-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="ead4a-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="ead4a-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="ead4a-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="ead4a-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="ead4a-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="ead4a-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="ead4a-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="ead4a-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="ead4a-117">CheckDimValueComb</span></span>|<span data-ttu-id="ead4a-118">Poista.</span><span class="sxs-lookup"><span data-stu-id="ead4a-118">Delete.</span></span> <span data-ttu-id="ead4a-119">Kaikki käyttö tulisi muuttaa arvoon CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="ead4a-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="ead4a-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-120">GetDefaultDim</span></span>|<span data-ttu-id="ead4a-121">Muuta palauttamaan dimensioyhdistelmän tunnus kokonaisluku-muodossa tietuejoukon sijasta.</span><span class="sxs-lookup"><span data-stu-id="ead4a-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="ead4a-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="ead4a-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="ead4a-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="ead4a-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="ead4a-126">Muokkaa toimimaan: DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="ead4a-127">Poistetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="ead4a-127">Deleted Functions</span></span>  
 <span data-ttu-id="ead4a-128">Alla luetellaan toiminnot, jotka on poistettu 408-koodiyksikön dimensioyhdistelmän tapahtumat -ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="ead4a-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="ead4a-129">Kun sovelluksen koodia päivitetään Microsoft Dynamics NAV 2009:stä tai sitä aiemmasta versiosta Microsoft Dynamics NAV 2016:een, seuraavat toiminnot eivät ole käytettävissä Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="ead4a-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="ead4a-130">Jos olet tehnyt mukautuksia, jotka käyttävät yhtä tai useampaa seuraavista toiminnoista, mukautuksesi on päivitettävä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="ead4a-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="ead4a-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="ead4a-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="ead4a-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="ead4a-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="ead4a-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-136">InsertDocDim</span></span>  

 <span data-ttu-id="ead4a-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="ead4a-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="ead4a-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="ead4a-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="ead4a-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-141">InsertServContractDim</span></span>  

 <span data-ttu-id="ead4a-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="ead4a-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="ead4a-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="ead4a-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-144">GetDocDim</span></span>  

 <span data-ttu-id="ead4a-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-145">GetProdDocDim</span></span>  

 <span data-ttu-id="ead4a-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="ead4a-146">TypeToTableID1</span></span>  

 <span data-ttu-id="ead4a-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="ead4a-147">TypeToTableID2</span></span>  

 <span data-ttu-id="ead4a-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="ead4a-148">TypeToTableID3</span></span>  

 <span data-ttu-id="ead4a-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="ead4a-149">TypeToTableID4</span></span>  

 <span data-ttu-id="ead4a-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="ead4a-150">TypeToTableID5</span></span>  

 <span data-ttu-id="ead4a-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-152">DeleteDocDim</span></span>  

 <span data-ttu-id="ead4a-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="ead4a-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="ead4a-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="ead4a-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="ead4a-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="ead4a-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-160">ShowDocDim</span></span>  

 <span data-ttu-id="ead4a-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-161">SaveDocDim</span></span>  

 <span data-ttu-id="ead4a-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="ead4a-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="ead4a-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-164">ShowTempDim</span></span>  

 <span data-ttu-id="ead4a-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-165">SaveTempDim</span></span>  

 <span data-ttu-id="ead4a-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="ead4a-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="ead4a-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-168">SaveServContractDim</span></span>  

 <span data-ttu-id="ead4a-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ead4a-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ead4a-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ead4a-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="ead4a-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="ead4a-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="ead4a-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="ead4a-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ead4a-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="ead4a-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="ead4a-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ead4a-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="ead4a-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="ead4a-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="ead4a-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="ead4a-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="ead4a-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="ead4a-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="ead4a-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ead4a-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="ead4a-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="ead4a-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="ead4a-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="ead4a-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="ead4a-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="ead4a-198">TestDimValue</span></span>  

 <span data-ttu-id="ead4a-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="ead4a-199">TestNewDimValue</span></span>  

 <span data-ttu-id="ead4a-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="ead4a-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="ead4a-201">(Poista, koska ItemBudgetDim-taulukko poistetaan.)</span><span class="sxs-lookup"><span data-stu-id="ead4a-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="ead4a-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-202">GetServContractDim</span></span>  

 <span data-ttu-id="ead4a-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="ead4a-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="ead4a-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="ead4a-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="ead4a-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="ead4a-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="ead4a-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="ead4a-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="ead4a-207">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ead4a-207">See Also</span></span>
 <span data-ttu-id="ead4a-208">[Rakennetiedot: dimensioyhdistelmä-tapahtumat](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ead4a-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="ead4a-209">[Rakennetiedot: Dimensioyhdistelmätapahtumien yleiskatsaus](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="ead4a-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="ead4a-210">[Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="ead4a-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 [<span data-ttu-id="ead4a-211">Rakennetiedot: taulukkorakenne</span><span class="sxs-lookup"><span data-stu-id="ead4a-211">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 
