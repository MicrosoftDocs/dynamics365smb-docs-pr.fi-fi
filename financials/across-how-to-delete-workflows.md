---
title: "Työnkulkujen poistaminen | Microsoft Docs"
description: "Voit poistaa työnkulun, jos olet varma, ettei sitä enää käytetä. Kaikkien työnkulun osavaiheiden instanssien tilan on oltava **Valmis**."
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
ms.openlocfilehash: d1b7b29735983e2de0bdaf5d382679d9546a6278
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-delete-workflows"></a><span data-ttu-id="811de-104">Toimintaohje: Työnkulkujen poistaminen</span><span class="sxs-lookup"><span data-stu-id="811de-104">How to: Delete Workflows</span></span>
<span data-ttu-id="811de-105">Voit poistaa työnkulun, jos olet varma, ettei sitä enää käytetä.</span><span class="sxs-lookup"><span data-stu-id="811de-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="811de-106">Kaikkien työnkulun osavaiheiden instanssien tilan pitää olla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="811de-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="811de-107">Kun poistat työnkulun, kaikki työnkulun tiedot menetetään.</span><span class="sxs-lookup"><span data-stu-id="811de-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="811de-108">**Työnkulku**-ikkunassa voit luoda työnkulun luetteloimalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="811de-108">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="811de-109">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="811de-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="811de-110">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="811de-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="811de-111">Lisätietoja on kohdassa [Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="811de-111">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="811de-112">Työnkulun poistaminen</span><span class="sxs-lookup"><span data-stu-id="811de-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="811de-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työnkulut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="811de-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="811de-114">Valitse työnkulku, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="811de-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="811de-115">Valitse **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="811de-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="811de-116">Voit myös avata työnkulun, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="811de-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="811de-117">Valitse **Työnkulku**-ikkunassa **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="811de-117">In the **Workflow** window, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="811de-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="811de-118">See Also</span></span>  
 <span data-ttu-id="811de-119">[Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="811de-119">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="811de-120">[Toimintaohje: Työnkulkujen ottaminen käyttöön](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="811de-120">[How to: Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="811de-121">[Toimintaohje: Arkistoitujen työnkulun osavaiheen instanssien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="811de-121">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="811de-122">[Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="811de-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="811de-123">[Työnkulkujen määrittäminen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="811de-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="811de-124">[Työnkulkujen käyttäminen](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="811de-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="811de-125">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="811de-125">Workflow</span></span>](across-workflow.md)   

