---
title: Työnkulkujen käyttäminen | Microsoft Docs
description: Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 517c29549274430f6f851f88d0737bdb9aaf4faa
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785769"
---
# <a name="using-workflows"></a><span data-ttu-id="73204-105">Työnkulkujen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="73204-105">Using Workflows</span></span>
<span data-ttu-id="73204-106">Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="73204-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="73204-107">Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat.</span><span class="sxs-lookup"><span data-stu-id="73204-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="73204-108">Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.</span><span class="sxs-lookup"><span data-stu-id="73204-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="73204-109">Ennen kuin voit aloittaa työnkulkujen käyttämisen, sinun on määritettävä työnkulun käyttäjät, luotava työnkulut ja tehtävä mahdolliset koodin mukautukset, ja määritettävä miten käyttäjät saavat ilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="73204-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="73204-110">Lisätietoja on kohdassa [Työnkulkujen määrittäminen](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="73204-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="73204-111">Tavalliset työnkulun osavaiheet liittyvät käyttäjiin, jotka pyytävät hyväksyntää tehtäville, ja hyväksyjiin, jotka hyväksyvät tai hylkäävät pyynnöt.</span><span class="sxs-lookup"><span data-stu-id="73204-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="73204-112">Tämän vuoksi monet työnkulkuihin liittyvät ohjeaiheet liittyvät hyväksyntään.</span><span class="sxs-lookup"><span data-stu-id="73204-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="73204-113">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="73204-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="73204-114">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="73204-114">**To**</span></span>|<span data-ttu-id="73204-115">**Katso**</span><span class="sxs-lookup"><span data-stu-id="73204-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="73204-116">Määritä työnkulku alkamaan, kun ensimmäinen merkitsevä tapahtuma toteutuu.</span><span class="sxs-lookup"><span data-stu-id="73204-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="73204-117">Työnkulkujen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="73204-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="73204-118">Pyydä tehtävän hyväksyntää, ja hyväksyjänä voit hyväksyä, hylätä tai delegoida hyväksyntöjä sekä lähettää tai tarkastella hyväksyntäilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="73204-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="73204-119">Hyväksymistyönkulkujen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="73204-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="73204-120">Luo työnkulun vaiheet, jotka rajoittavat tiettyjen tietuetyyppien käyttöä ennen kuin tietty tapahtuma tapahtuu, esimerkiksi, että tietue on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="73204-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="73204-121">Tietueen käytön rajoittaminen ja salliminen</span><span class="sxs-lookup"><span data-stu-id="73204-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="73204-122">Tarkastele Valmis-tilassa olevia työnkulun osavaiheita.</span><span class="sxs-lookup"><span data-stu-id="73204-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="73204-123">Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="73204-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="73204-124">Poista työnkulku, joka ei ole enää käytössä.</span><span class="sxs-lookup"><span data-stu-id="73204-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="73204-125">Työnkulkujen poistaminen</span><span class="sxs-lookup"><span data-stu-id="73204-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="73204-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="73204-126">See Also</span></span>  
<span data-ttu-id="73204-127">[Työnkulkujen määrittäminen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="73204-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="73204-128">[Työnkulku](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="73204-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="73204-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="73204-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
