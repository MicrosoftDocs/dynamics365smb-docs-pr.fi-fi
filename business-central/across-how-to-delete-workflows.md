---
title: Työnkulkujen poistaminen | Microsoft Docs
description: Voit poistaa työnkulun, jos olet varma, ettei sitä enää käytetä. Kaikkien työnkulun osavaiheiden instanssien tilan pitää olla **Valmis**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 97cd7c2f74875317a3d4559c15d0bd22367e6df7
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778090"
---
# <a name="delete-workflows"></a><span data-ttu-id="5d557-104">Työnkulkujen poistaminen</span><span class="sxs-lookup"><span data-stu-id="5d557-104">Delete Workflows</span></span>
<span data-ttu-id="5d557-105">Voit poistaa työnkulun, jos olet varma, ettei sitä enää käytetä.</span><span class="sxs-lookup"><span data-stu-id="5d557-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="5d557-106">Kaikkien työnkulun osavaiheiden instanssien tilan pitää olla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="5d557-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="5d557-107">Kun poistat työnkulun, kaikki työnkulun tiedot menetetään.</span><span class="sxs-lookup"><span data-stu-id="5d557-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="5d557-108">Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="5d557-108">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="5d557-109">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="5d557-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="5d557-110">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="5d557-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="5d557-111">Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="5d557-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="5d557-112">Työnkulun poistaminen</span><span class="sxs-lookup"><span data-stu-id="5d557-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="5d557-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5d557-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5d557-114">Valitse työnkulku, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="5d557-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="5d557-115">Valitse **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="5d557-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="5d557-116">Voit myös avata työnkulun, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="5d557-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="5d557-117">Valitse **Työnkulku**-sivulla **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="5d557-117">On the **Workflow** page, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5d557-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5d557-118">See Also</span></span>  
 <span data-ttu-id="5d557-119">[Työnkulkujen luominen](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="5d557-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="5d557-120">[Työnkulkujen ottaminen käyttöön](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="5d557-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="5d557-121">[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="5d557-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="5d557-122">[Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="5d557-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="5d557-123">[Työnkulkujen määrittäminen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="5d557-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="5d557-124">[Työnkulkujen käyttäminen](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="5d557-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="5d557-125">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="5d557-125">Workflow</span></span>](across-workflow.md)   
