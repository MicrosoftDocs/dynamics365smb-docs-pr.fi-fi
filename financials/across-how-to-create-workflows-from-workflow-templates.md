---
title: "Työnkulkujen luominen työnkulkumalleista | Microsoft Docs"
description: "Voit säästää aikaa uusien työnkulkujen luomisessa luomalla työnkulut työnkulkumalleista."
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
ms.openlocfilehash: dcf6f5f5b0364ebcaefdcbc43fdbd7471cb6079e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-workflows-from-workflow-templates"></a><span data-ttu-id="0b8ac-103">Ohje: Työnkulkujen luominen työnkulkumalleista</span><span class="sxs-lookup"><span data-stu-id="0b8ac-103">How to: Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="0b8ac-104">Voit säästää aikaa uusien työnkulkujen luomisessa luomalla työnkulut työnkulkumalleista.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="0b8ac-105">Työnkulkumallit ovat yleisen [!INCLUDE[d365fin](includes/d365fin_md.md)] -version työnkulkuja, joita ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0b8ac-106">Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-".</span><span class="sxs-lookup"><span data-stu-id="0b8ac-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="0b8ac-107">Työnkulun voi nopeasti myös tuomalla aiemmin luodun työnkulun, joka on [!INCLUDE[d365fin](includes/d365fin_md.md)]in ulkopuolisessa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0b8ac-108">Lisätietoja on kohdassa [Toimintaohje: Työnkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="0b8ac-108">For more information, see [How to: Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="0b8ac-109">**Työnkulku**-ikkunassa voit luoda työnkulun luetteloimalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="0b8ac-110">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="0b8ac-111">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="0b8ac-112">Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="0b8ac-112">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="0b8ac-113">Työnkulun luominen työnkulkumallista</span><span class="sxs-lookup"><span data-stu-id="0b8ac-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="0b8ac-114">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työnkulut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0b8ac-115">Valitse **Luo työnkulku mallista** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="0b8ac-116">**Työnkulkumallit**-ikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="0b8ac-117">Valitse työnkulkumalli ja sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="0b8ac-118">Uuden työnkulun avautuvassa **Työnkulku**-ikkunassa on kaikki valitun mallin tiedot.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="0b8ac-119">**Koodi**-kentän arvoon liitetään esimerkiksi ”-01”, joka osoittaa, että kyseessä on ensimmäinen työnkulkumallista luotu työnkulku.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="0b8ac-120">Jatka työnkulun luontia muokkaamalla työnkulun vaiheita tai lisäämällä uusia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="0b8ac-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="0b8ac-121">Lisätietoja on kohdassa [Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="0b8ac-121">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b8ac-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0b8ac-122">See Also</span></span>  
 <span data-ttu-id="0b8ac-123">[Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0b8ac-123">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="0b8ac-124">[Toimintaohje: työnkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0b8ac-124">[How to: Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="0b8ac-125">[Toimintaohje: Arkistoitujen työnkulun osavaiheen instanssien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="0b8ac-125">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="0b8ac-126">[Toimintaohje: Työnkulkujen poistaminen](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0b8ac-126">[How to: Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="0b8ac-127">[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="0b8ac-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="0b8ac-128">[Työnkulkujen määrittäminen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0b8ac-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="0b8ac-129">[Työnkulkujen käyttäminen](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0b8ac-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="0b8ac-130">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="0b8ac-130">Workflow</span></span>](across-workflow.md)   

