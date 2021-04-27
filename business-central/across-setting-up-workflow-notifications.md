---
title: Työnkulun ilmoitukset
description: Useat työnkulun vastaukset ilmoittavat käyttäjälle toimia vaativista tapahtumista. Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena on toinen ilmoitus, joka lähetetään käyttäjälle 2 eli hyväksyjälle. Seuraavassa työnkulun osavaiheessa tapahtuma voi olla esimerkiksi se, että käyttäjä 2 hyväksyy tietueen. Vastauksena on ilmoitus, joka lähetetään käyttäjälle 3 hyväksyttyyn tietueeseen liittyvän käsittelyn aloittamiseksi. Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d72c3ba220c98d0c77806466f467ab233b3db65c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787044"
---
# <a name="workflow-notifications"></a><span data-ttu-id="c2d2f-106">Työnkulun ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="c2d2f-106">Workflow Notifications</span></span>

<span data-ttu-id="c2d2f-107">Määritä työnkulut ilmoittamaan käyttäjille automaattisesti, kun työnkulun vaihe vaatii heidän huomionsa.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-107">Set up your workflows to automatically notify users when their attention is required for a step in that workflow.</span></span> <span data-ttu-id="c2d2f-108">Useat työnkulun vastaukset ilmoittavat käyttäjälle toimia vaativista tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-108">Many workflow responses are about notifying a user that an event has occurred that they must act on.</span></span> <span data-ttu-id="c2d2f-109">Työnkulun osavaiheen tapahtuma voi olla esimerkiksi se, että käyttäjä 1 pyytää uuden tietueen hyväksymistä. Vastauksena on toinen ilmoitus, joka lähetetään käyttäjälle 2 eli hyväksyjälle.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-109">For example, on one workflow step, the event can be that User 1 requests approval of a new record, and the response is that a notification is sent to User 2, the approver.</span></span> <span data-ttu-id="c2d2f-110">Seuraavassa työnkulun osavaiheessa tapahtuma voi olla esimerkiksi se, että käyttäjä 2 hyväksyy tietueen. Vastauksena on ilmoitus, joka lähetetään käyttäjälle 3 hyväksyttyyn tietueeseen liittyvän käsittelyn aloittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-110">On the next workflow step, the event can be that User 2 approves the record, and the response is that a notification is sent to User 3 to start a related processing of the approved record.</span></span> <span data-ttu-id="c2d2f-111">Hyväksyntään liittyvien työnkulun osavaiheiden ilmoitukset ovat sidoksissa hyväksyntämerkintään.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-111">For workflow steps that are about approval, each notification is tied to an approval entry.</span></span> <span data-ttu-id="c2d2f-112">Lisätietoja on kohdassa [Työnkulku](across-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c2d2f-112">For more information, see [Workflow](across-workflow.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="c2d2f-113">[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleinen versio tukee ilmoituksia sähköpostina ja sisäisinä muistiinpanoina.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-113">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports notifications as email and as internal notes.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="c2d2f-114">Kaikki työnkulun ilmoitukset lähetetään työjonon kautta.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-114">All workflow notifications are sent through a job queue.</span></span> <span data-ttu-id="c2d2f-115">Varmista, että asennuksen työjono on määritetty käsittelemään työnkulun ilmoituksia ja että **Käynnistä automaattisesti palvelimelta** -valintaruutu on valittu.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-115">Make sure that the job queue in your installation is set up to handle workflow notifications, and that the **Start Automatically From Server** check box is selected.</span></span> <span data-ttu-id="c2d2f-116">Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="c2d2f-116">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="set-up-notifications"></a><span data-ttu-id="c2d2f-117">Ilmoitusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-117">Set up notifications</span></span>

<span data-ttu-id="c2d2f-118">Työnkulun ilmoitusten osatekijöitä määritetään seuraavissa paikoissa:</span><span class="sxs-lookup"><span data-stu-id="c2d2f-118">You set up different aspects of workflow notifications in the following places:</span></span>  

* <span data-ttu-id="c2d2f-119">Hyväksyjän ilmoitus</span><span class="sxs-lookup"><span data-stu-id="c2d2f-119">Approver notification</span></span>

    <span data-ttu-id="c2d2f-120">Hyväksynnän työnkulkujen ilmoitusten vastaanottajat määritetään täyttämällä rivi **Hyväksynnän käyttäjäasetukset** -sivulla kullekin työnkulkuun osallistuvalle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-120">For approval workflows, you set up the recipients of workflow notifications by filling a line on the **Approval User Setup** page for each user that takes part in the workflow.</span></span>  

    <span data-ttu-id="c2d2f-121">Jos esimerkiksi käyttäjä 2 on määritetty **Hyväksyjän tunnus** -kentän Käyttäjä 1 -rivillä, hyväksyntäpyyntöilmoitus lähetetään käyttäjälle 1.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-121">For example, if User 2 is specified in the **Approver ID** field on the line for User 1, then the approval request notification is sent to User 1.</span></span> <span data-ttu-id="c2d2f-122">Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="c2d2f-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  
* <span data-ttu-id="c2d2f-123">Ilmoitusaikataulut</span><span class="sxs-lookup"><span data-stu-id="c2d2f-123">Notification schedules</span></span>

    <span data-ttu-id="c2d2f-124">Täyttämällä **Ilmoitusaikataulu**-sivu kullekin työnkulun käyttäjälle määritetään se, milloin ja miten käyttäjät saavat työnkulun ilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-124">You set up when and how users receive workflow notifications by filling the **Notification Schedule** page for each workflow user.</span></span> <span data-ttu-id="c2d2f-125">Lisätietoja on kohdassa [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c2d2f-125">For more information, see [Specify When and How to Receive Notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).</span></span>  
* <span data-ttu-id="c2d2f-126">Sähköposti-ilmoitusten mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-126">Customize the email notifications</span></span>

    <span data-ttu-id="c2d2f-127">Voit halutessasi mukauttaa sähköposti-ilmoituksen sisältöä muokkaamalla raportin 1320 sähköposti-ilmoitusta.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-127">If you want, you can customize the content of the email notification by modifying report 1320, Notification Email.</span></span> <span data-ttu-id="c2d2f-128">Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="c2d2f-128">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>  
* <span data-ttu-id="c2d2f-129">Vastausvaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="c2d2f-129">Response options</span></span>

    <span data-ttu-id="c2d2f-130">Työnkulun ilmoituksen erityinen sisältö ja säännöt määritetään silloin, kun luot kyseistä työnkulkua.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-130">You set up specific content and rules of a workflow notification when you create the workflow in question.</span></span> <span data-ttu-id="c2d2f-131">Se tehdään valitsemalla **Työnkulun vastausvaihtoehdot** -sivulla asetuksia ilmoitusta edustavalle työnkulun vastaukselle.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-131">You do this by selecting options on the **Workflow Response Options** page for the workflow response that represents the notification.</span></span> <span data-ttu-id="c2d2f-132">Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md) vaiheessa 9.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-132">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

* <span data-ttu-id="c2d2f-133">Ilmoita lähettäjälle</span><span class="sxs-lookup"><span data-stu-id="c2d2f-133">Notify sender</span></span>

    <span data-ttu-id="c2d2f-134">Hyväksymistyönkuluille voit lisätä työnkulun vastausvaiheen, joka ilmoittaa lähettäjälle, kun heidän pyyntönsä on hyväksytty tai hylätty.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-134">For approval workflows, add a workflow response step to notify the sender when the request has been approved or rejected.</span></span> <span data-ttu-id="c2d2f-135">Lisätietoja on kohdan [Työnkulkujen luominen](across-how-to-create-workflows.md) vaiheessa 9.</span><span class="sxs-lookup"><span data-stu-id="c2d2f-135">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2d2f-136">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c2d2f-136">See Also</span></span>

[<span data-ttu-id="c2d2f-137">Hyväksynnän käyttäjien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-137">Set Up Approval Users</span></span>](across-how-to-set-up-approval-users.md)  
[<span data-ttu-id="c2d2f-138">Työnkulun käyttäjien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-138">Set Up Workflow Users</span></span>](across-how-to-set-up-workflow-users.md)  
[<span data-ttu-id="c2d2f-139">Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-139">Specify When and How to Receive Notifications</span></span>](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[<span data-ttu-id="c2d2f-140">Työnkulkujen luominen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-140">Create Workflows</span></span>](across-how-to-create-workflows.md)  
[<span data-ttu-id="c2d2f-141">Raporttien mukautettujen asettelujen luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-141">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="c2d2f-142">Työjonojen käyttäminen ajoitustehtäviin</span><span class="sxs-lookup"><span data-stu-id="c2d2f-142">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="c2d2f-143">Sähköpostin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-143">Set up Email</span></span>](admin-how-setup-email.md)  
[<span data-ttu-id="c2d2f-144">Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="c2d2f-144">Walkthrough: Setting Up and Using a Purchase Approval Workflow</span></span>](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[<span data-ttu-id="c2d2f-145">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="c2d2f-145">Workflow</span></span>](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]