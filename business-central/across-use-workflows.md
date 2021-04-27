---
title: Työnkulkujen käyttäminen
description: Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. Tietoja eri vaiheista, jotka työnkulkujen käytön aloittaminen vaatii.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92b32957bb7b20dda304be8a99bb17c5c5947498
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787005"
---
# <a name="using-workflows"></a><span data-ttu-id="6de2c-104">Työnkulkujen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6de2c-104">Using Workflows</span></span>
<span data-ttu-id="6de2c-105">Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="6de2c-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="6de2c-106">Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat.</span><span class="sxs-lookup"><span data-stu-id="6de2c-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="6de2c-107">Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.</span><span class="sxs-lookup"><span data-stu-id="6de2c-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="6de2c-108">Ennen kuin voit aloittaa työnkulkujen käyttämisen, sinun on määritettävä työnkulun käyttäjät, luotava työnkulut ja tehtävä mahdolliset koodin mukautukset, ja määritettävä miten käyttäjät saavat ilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="6de2c-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="6de2c-109">Lisätietoja on kohdassa [Työnkulkujen määrittäminen](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="6de2c-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6de2c-110">Tavalliset työnkulun osavaiheet liittyvät käyttäjiin, jotka pyytävät hyväksyntää tehtäville, ja hyväksyjiin, jotka hyväksyvät tai hylkäävät pyynnöt.</span><span class="sxs-lookup"><span data-stu-id="6de2c-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="6de2c-111">Tämän vuoksi monet työnkulkuihin liittyvät ohjeaiheet liittyvät hyväksyntään.</span><span class="sxs-lookup"><span data-stu-id="6de2c-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="6de2c-112">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="6de2c-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="6de2c-113">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="6de2c-113">**To**</span></span>|<span data-ttu-id="6de2c-114">**Katso**</span><span class="sxs-lookup"><span data-stu-id="6de2c-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="6de2c-115">Määritä työnkulku alkamaan, kun ensimmäinen merkitsevä tapahtuma toteutuu.</span><span class="sxs-lookup"><span data-stu-id="6de2c-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="6de2c-116">Työnkulkujen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="6de2c-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="6de2c-117">Pyydä tehtävän hyväksyntää, ja hyväksyjänä voit hyväksyä, hylätä tai delegoida hyväksyntöjä sekä lähettää tai tarkastella hyväksyntäilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="6de2c-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="6de2c-118">Hyväksymistyönkulkujen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6de2c-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="6de2c-119">Luo työnkulun vaiheet, jotka rajoittavat tiettyjen tietuetyyppien käyttöä ennen kuin tietty tapahtuma tapahtuu, esimerkiksi, että tietue on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="6de2c-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="6de2c-120">Tietueen käytön rajoittaminen ja salliminen</span><span class="sxs-lookup"><span data-stu-id="6de2c-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="6de2c-121">Tarkastele Valmis-tilassa olevia työnkulun osavaiheita.</span><span class="sxs-lookup"><span data-stu-id="6de2c-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="6de2c-122">Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="6de2c-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="6de2c-123">Poista työnkulku, joka ei ole enää käytössä.</span><span class="sxs-lookup"><span data-stu-id="6de2c-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="6de2c-124">Työnkulkujen poistaminen</span><span class="sxs-lookup"><span data-stu-id="6de2c-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="6de2c-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6de2c-125">See Also</span></span>  
<span data-ttu-id="6de2c-126">[Työnkulkujen määrittäminen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="6de2c-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="6de2c-127">[Työnkulku](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="6de2c-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="6de2c-128">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6de2c-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]