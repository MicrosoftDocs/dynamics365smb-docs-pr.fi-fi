---
title: Työnkulkujen luominen työnkulkumalleista | Microsoft Docs
description: Voit säästää aikaa uusien työnkulkujen luomisessa luomalla työnkulut työnkulkumalleista.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b2ee2dcba364f7b89bae49c3f15f098c51d2c5a3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913544"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="049b9-103">Työnkulkujen luominen työnkulkumalleista</span><span class="sxs-lookup"><span data-stu-id="049b9-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="049b9-104">Voit säästää aikaa uusien työnkulkujen luomisessa luomalla työnkulut työnkulkumalleista.</span><span class="sxs-lookup"><span data-stu-id="049b9-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="049b9-105">Työnkulkumallit ovat yleisen [!INCLUDE[d365fin](includes/d365fin_md.md)] -version työnkulkuja, joita ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="049b9-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="049b9-106">Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-".</span><span class="sxs-lookup"><span data-stu-id="049b9-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="049b9-107">Työnkulun voi nopeasti myös tuomalla aiemmin luodun työnkulun, joka on [!INCLUDE[d365fin](includes/d365fin_md.md)]in ulkopuolisessa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="049b9-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="049b9-108">Lisätietoja on kohdassa [Työnkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="049b9-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="049b9-109">Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="049b9-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="049b9-110">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="049b9-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="049b9-111">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="049b9-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="049b9-112">Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="049b9-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="049b9-113">Työnkulun luominen työnkulkumallista</span><span class="sxs-lookup"><span data-stu-id="049b9-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="049b9-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="049b9-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="049b9-115">Valitse **Luo työnkulku mallista** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="049b9-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="049b9-116">**Työnkulkumallit**-sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="049b9-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="049b9-117">Valitse työnkulkumalli ja sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="049b9-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="049b9-118">Uuden työnkulun avautuvalla **Työnkulku**-sivulla on kaikki valitun mallin tiedot.</span><span class="sxs-lookup"><span data-stu-id="049b9-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="049b9-119">**Koodi**-kentän arvoon liitetään esimerkiksi ”-01”, joka osoittaa, että kyseessä on ensimmäinen työnkulkumallista luotu työnkulku.</span><span class="sxs-lookup"><span data-stu-id="049b9-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="049b9-120">Jatka työnkulun luontia muokkaamalla työnkulun vaiheita tai lisäämällä uusia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="049b9-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="049b9-121">Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="049b9-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="049b9-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="049b9-122">See Also</span></span>  
 <span data-ttu-id="049b9-123">[Työnkulkujen luominen](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="049b9-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="049b9-124">[Työnkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="049b9-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="049b9-125">[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="049b9-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="049b9-126">[Työnkulkujen poistaminen](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="049b9-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="049b9-127">[Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="049b9-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="049b9-128">[Työnkulkujen määrittäminen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="049b9-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="049b9-129">[Työnkulkujen käyttäminen](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="049b9-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="049b9-130">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="049b9-130">Workflow</span></span>](across-workflow.md)   
