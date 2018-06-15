---
title: "Työnkulku | Microsoft Docs"
description: "Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 05/09/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 128d20233d1750b2b89c3c7e2de6e497bd32b342
ms.contentlocale: fi-fi
ms.lasthandoff: 05/15/2018

---
# <a name="workflow"></a><span data-ttu-id="88951-105">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="88951-105">Workflow</span></span>
<span data-ttu-id="88951-106">Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="88951-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="88951-107">Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat.</span><span class="sxs-lookup"><span data-stu-id="88951-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="88951-108">Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.</span><span class="sxs-lookup"><span data-stu-id="88951-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="88951-109">Voit luoda **Työnkulku**-ikkunassa työnkulun mainitsemalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="88951-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="88951-110">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="88951-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="88951-111">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="88951-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="88951-112">[!INCLUDE[d365fin](includes/d365fin_md.md)]in yleinen versio sisältää useita valmiiksi määritettyjä työnkulkuja ja työnkulkumalleja, joita kopioimalla voit luoda työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="88951-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="88951-113">Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-".</span><span class="sxs-lookup"><span data-stu-id="88951-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="88951-114">Lisätietoja on Työnkulkumallit-ikkunan työnkulkumallien luettelossa.</span><span class="sxs-lookup"><span data-stu-id="88951-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="88951-115">Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei ole tuettu, Microsoft-kumppanin on toteutettava se mukauttamalla sovelluksen koodia.</span><span class="sxs-lookup"><span data-stu-id="88951-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="88951-116">Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Vaihekuvaus: Uusien työnkulun tapahtumien ja vastausten määrittäminen](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses).</span><span class="sxs-lookup"><span data-stu-id="88951-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>

> [!NOTE]  
> <span data-ttu-id="88951-117">Työnkulut voidaan aloittaa myös Microsoft Flow'sta.</span><span class="sxs-lookup"><span data-stu-id="88951-117">Workflows can also be initiated from Microsoft Flow.</span></span> <span data-ttu-id="88951-118">Lisätietoja on kohdassa [Business Centralin käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="88951-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="88951-119">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="88951-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="88951-120">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="88951-120">**To**</span></span>|<span data-ttu-id="88951-121">**Katso**</span><span class="sxs-lookup"><span data-stu-id="88951-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="88951-122">Luo työnkulun käyttäjiä, määriä, kuinka käyttäjät saavat ilmoituksia, ja luo uusia työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="88951-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="88951-123">Jos haluat määrittää uusia työnkulkuja skenaarioille, joita ei tueta, työnkulun elementit on otettava käyttöön mukauttamalla sovelluskoodia.</span><span class="sxs-lookup"><span data-stu-id="88951-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="88951-124">Työnkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="88951-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="88951-125">Ota käyttöön työnkulkuja ja käsittele työnkulun ilmoituksia, joihin kuuluvat myös hyväksyntöjen pyytäminen sekä työnkulun osavaiheen suorituspyyntöjen hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="88951-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="88951-126">Arkistoi ja poista työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="88951-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="88951-127">Työnkulkujen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="88951-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="88951-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="88951-128">See Also</span></span>  
[<span data-ttu-id="88951-129">Myynti</span><span class="sxs-lookup"><span data-stu-id="88951-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="88951-130">Osto</span><span class="sxs-lookup"><span data-stu-id="88951-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="88951-131">Projektien hallinta</span><span class="sxs-lookup"><span data-stu-id="88951-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="88951-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="88951-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

