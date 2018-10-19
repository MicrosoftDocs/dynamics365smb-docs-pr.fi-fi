---
title: "Työnkulkujen poistaminen | Microsoft Docs"
description: "Voit poistaa työnkulun, jos olet varma, ettei sitä enää käytetä. Kaikkien työnkulun osavaiheiden instanssien tilan pitää olla **Valmis**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 79d4ac247abe75fab8a7c935d31fc236383747cc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="delete-workflows"></a><span data-ttu-id="d2f36-104">Työnkulkujen poistaminen</span><span class="sxs-lookup"><span data-stu-id="d2f36-104">Delete Workflows</span></span>
<span data-ttu-id="d2f36-105">Voit poistaa työnkulun, jos olet varma, ettei sitä enää käytetä.</span><span class="sxs-lookup"><span data-stu-id="d2f36-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="d2f36-106">Kaikkien työnkulun osavaiheiden instanssien tilan pitää olla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="d2f36-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="d2f36-107">Kun poistat työnkulun, kaikki työnkulun tiedot menetetään.</span><span class="sxs-lookup"><span data-stu-id="d2f36-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="d2f36-108">**Työnkulku**-ikkunassa voit luoda työnkulun luetteloimalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="d2f36-108">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="d2f36-109">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d2f36-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="d2f36-110">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="d2f36-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="d2f36-111">Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d2f36-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="d2f36-112">Työnkulun poistaminen</span><span class="sxs-lookup"><span data-stu-id="d2f36-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="d2f36-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d2f36-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d2f36-114">Valitse työnkulku, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="d2f36-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="d2f36-115">Valitse **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d2f36-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="d2f36-116">Voit myös avata työnkulun, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="d2f36-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="d2f36-117">Valitse **Työnkulku**-ikkunassa **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d2f36-117">In the **Workflow** window, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2f36-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d2f36-118">See Also</span></span>  
 <span data-ttu-id="d2f36-119">[Työnkulkujen luominen](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d2f36-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="d2f36-120">[Työnkulkujen ottaminen käyttöön](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d2f36-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="d2f36-121">[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="d2f36-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="d2f36-122">[Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="d2f36-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="d2f36-123">[Työnkulkujen määrittäminen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d2f36-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="d2f36-124">[Työnkulkujen käyttäminen](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d2f36-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="d2f36-125">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="d2f36-125">Workflow</span></span>](across-workflow.md)   

