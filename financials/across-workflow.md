---
title: "Työnkulku | Microsoft Docs"
description: "Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita."
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
ms.openlocfilehash: f65c0e577e839928809f7afda3dbdb4c9b7702c8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="workflow"></a><span data-ttu-id="82629-105">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="82629-105">Workflow</span></span>
<span data-ttu-id="82629-106">Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="82629-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="82629-107">Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat.</span><span class="sxs-lookup"><span data-stu-id="82629-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="82629-108">Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.</span><span class="sxs-lookup"><span data-stu-id="82629-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="82629-109">Voit luoda **Työnkulku**-ikkunassa työnkulun mainitsemalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="82629-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="82629-110">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="82629-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="82629-111">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="82629-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="82629-112">[!INCLUDE[d365fin](includes/d365fin_md.md)]in yleinen versio sisältää useita valmiiksi määritettyjä työnkulkuja ja työnkulkumalleja, joita kopioimalla voit luoda työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="82629-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="82629-113">Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-".</span><span class="sxs-lookup"><span data-stu-id="82629-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="82629-114">Lisätietoja on Työnkulkumallit-ikkunan työnkulkumallien luettelossa.</span><span class="sxs-lookup"><span data-stu-id="82629-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="82629-115">Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei ole tuettu, Microsoft-kumppanin on toteutettava se mukauttamalla sovelluksen koodia.</span><span class="sxs-lookup"><span data-stu-id="82629-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="82629-116">Lisätietoja on MSDN:n artikkelissa [Vaihekuvaus: Uusien työnkulun tapahtumien ja vastausten määrittäminen](https://msdn.microsoft.com/en-us/library/mt574349.aspx).</span><span class="sxs-lookup"><span data-stu-id="82629-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](https://msdn.microsoft.com/en-us/library/mt574349.aspx) on MSDN.</span></span>  

 <span data-ttu-id="82629-117">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="82629-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="82629-118">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="82629-118">**To**</span></span>|<span data-ttu-id="82629-119">**Katso**</span><span class="sxs-lookup"><span data-stu-id="82629-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="82629-120">Luo työnkulun käyttäjiä, määriä, kuinka käyttäjät saavat ilmoituksia, ja luo uusia työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="82629-120">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="82629-121">Jos haluat määrittää uusia työnkulkuja skenaarioille, joita ei tueta, työnkulun elementit on otettava käyttöön mukauttamalla sovelluskoodia.</span><span class="sxs-lookup"><span data-stu-id="82629-121">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="82629-122">Työnkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="82629-122">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="82629-123">Ota käyttöön työnkulkuja ja käsittele työnkulun ilmoituksia, joihin kuuluvat myös hyväksyntöjen pyytäminen sekä työnkulun osavaiheen suorituspyyntöjen hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="82629-123">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="82629-124">Arkistoi ja poista työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="82629-124">Archive and delete workflows.</span></span>|[<span data-ttu-id="82629-125">Työnkulkujen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="82629-125">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="82629-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="82629-126">See Also</span></span>  
[<span data-ttu-id="82629-127">Myynti</span><span class="sxs-lookup"><span data-stu-id="82629-127">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="82629-128">Osto</span><span class="sxs-lookup"><span data-stu-id="82629-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="82629-129">Projektien hallinta</span><span class="sxs-lookup"><span data-stu-id="82629-129">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="82629-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82629-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

