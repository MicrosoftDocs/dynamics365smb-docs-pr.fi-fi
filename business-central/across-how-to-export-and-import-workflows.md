---
title: Työnkulkujen vienti ja tuonti | Microsoft Docs
description: Voit siirtää työnkulkuja muihin Business Central -tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4d11bc57066c0124bcb004894ed6b2c9dc4b812e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754765"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="19581-103">Työnkulkujen vienti ja tuonti</span><span class="sxs-lookup"><span data-stu-id="19581-103">Export and Import Workflows</span></span>
<span data-ttu-id="19581-104">Voit siirtää työnkulkuja muihin [!INCLUDE[prod_short](includes/prod_short.md)] tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="19581-104">To transfer workflows to other [!INCLUDE[prod_short](includes/prod_short.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="19581-105">Toinen tapa luoda nopeasti työnkulut on työnkulkujen luominen työnkulkumalleista.</span><span class="sxs-lookup"><span data-stu-id="19581-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="19581-106">Lisätietoja on kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="19581-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="19581-107">Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="19581-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="19581-108">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="19581-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="19581-109">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="19581-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="19581-110">Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="19581-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="19581-111">Työnkulun vieminen</span><span class="sxs-lookup"><span data-stu-id="19581-111">To export a workflow</span></span>  
1.  <span data-ttu-id="19581-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="19581-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="19581-113">Valitse ensin työnkulku ja sitten **Vie tiedostoon** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="19581-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="19581-114">Valitse **Vie tiedosto** -sivulla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="19581-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="19581-115">Valitse tiedostosijainti **Vie**-sivulla ja valitse sitten **Tallenna**-painike.</span><span class="sxs-lookup"><span data-stu-id="19581-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="19581-116">Työnkulun tuominen</span><span class="sxs-lookup"><span data-stu-id="19581-116">To import a workflow</span></span>  
1.  <span data-ttu-id="19581-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="19581-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="19581-118">Valitse **Tuo tiedostosta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="19581-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="19581-119">Valitse **Tuo**-sivulla XML-tiedosto, joka sisältää työnkulun, ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="19581-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="19581-120">Jos työnkulun koodi on jo tietokannassa, työnkulun osavaiheita korvataan tuodun työnkulun vaiheilla.</span><span class="sxs-lookup"><span data-stu-id="19581-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="19581-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="19581-121">See Also</span></span>  
 <span data-ttu-id="19581-122">[Työnkulkujen luominen](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="19581-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="19581-123">[Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="19581-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="19581-124">[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="19581-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="19581-125">[Työnkulkujen poistaminen](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="19581-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="19581-126">[Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="19581-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="19581-127">[Työnkulkujen määrittäminen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="19581-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="19581-128">[Työnkulkujen käyttäminen](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="19581-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="19581-129">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="19581-129">Workflow</span></span>](across-workflow.md)   
