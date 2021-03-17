---
title: Työnkulku | Microsoft Docs
description: Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 38092f364d1dee1f34d8aa0c0858ac1bc04d829b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378796"
---
# <a name="workflows-in-dynamics-365-business-central"></a><span data-ttu-id="29058-105">Dynamics 365 Business Centralin työnkulut</span><span class="sxs-lookup"><span data-stu-id="29058-105">Workflows in Dynamics 365 Business Central</span></span>

<span data-ttu-id="29058-106">Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="29058-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="29058-107">Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat.</span><span class="sxs-lookup"><span data-stu-id="29058-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="29058-108">Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.</span><span class="sxs-lookup"><span data-stu-id="29058-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="29058-109">Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä.</span><span class="sxs-lookup"><span data-stu-id="29058-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="29058-110">Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="29058-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="29058-111">Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="29058-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="29058-112">[!INCLUDE[prod_short](includes/prod_short.md)]in yleinen versio sisältää useita valmiiksi määritettyjä työnkulkuja ja työnkulkumalleja, joita kopioimalla voit luoda työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="29058-112">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="29058-113">Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-".</span><span class="sxs-lookup"><span data-stu-id="29058-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="29058-114">Lisätietoja on Työnkulkumallit-sivun työnkulkumallien luettelossa.</span><span class="sxs-lookup"><span data-stu-id="29058-114">For more information, see the list of workflow templates in the Workflow Templates page.</span></span>  

 <span data-ttu-id="29058-115">Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei ole tuettu, voit mukauttaa sovelluskoodia Power Automaten avulla tai tekemällä yhteistyöt Microsoft-kumppanin kanssa.</span><span class="sxs-lookup"><span data-stu-id="29058-115">If a business scenario requires a workflow event or response that is not supported, you can either use Power Automate or work with a Microsoft partner to customize the application code.</span></span> <span data-ttu-id="29058-116">Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="29058-116">For more information, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>

<span data-ttu-id="29058-117">Power Automatella luodut työnkulkumallit lisätään [!INCLUDE[prod_short](includes/prod_short.md)]in työkulkumalleihin.</span><span class="sxs-lookup"><span data-stu-id="29058-117">Any workflow template that you create with Power Automate is added to the list of workflow templates within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="29058-118">Lisätietoja on kohdassa [Business Centralin käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="29058-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="29058-119">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="29058-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="29058-120">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="29058-120">**To**</span></span>|<span data-ttu-id="29058-121">**Katso**</span><span class="sxs-lookup"><span data-stu-id="29058-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="29058-122">Luo työnkulun käyttäjiä, määriä, kuinka käyttäjät saavat ilmoituksia, ja luo uusia työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="29058-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="29058-123">Jos haluat määrittää uusia työnkulkuja skenaarioille, joita ei tueta, työnkulun elementit on otettava käyttöön mukauttamalla sovelluskoodia.</span><span class="sxs-lookup"><span data-stu-id="29058-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="29058-124">Työnkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="29058-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="29058-125">Ota käyttöön työnkulkuja ja käsittele työnkulun ilmoituksia, joihin kuuluvat myös hyväksyntöjen pyytäminen sekä työnkulun osavaiheen suorituspyyntöjen hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="29058-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="29058-126">Arkistoi ja poista työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="29058-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="29058-127">Työnkulkujen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="29058-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="29058-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="29058-128">See Also</span></span>

[<span data-ttu-id="29058-129">Myynti</span><span class="sxs-lookup"><span data-stu-id="29058-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="29058-130">Osto</span><span class="sxs-lookup"><span data-stu-id="29058-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="29058-131">Projektien hallinta</span><span class="sxs-lookup"><span data-stu-id="29058-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="29058-132">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="29058-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]