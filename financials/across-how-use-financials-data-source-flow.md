---
title: "Tietojen yhdistäminen Flow'hun| Microsoft Docs"
description: "Voit tehdä Financials-tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="d0e95-103">[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen automaattisessa työnkulussa</span><span class="sxs-lookup"><span data-stu-id="d0e95-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="d0e95-104">Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja työnkulun osana Microsoft Flow'ssa.</span><span class="sxs-lookup"><span data-stu-id="d0e95-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d0e95-105">Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Flow-tili.</span><span class="sxs-lookup"><span data-stu-id="d0e95-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="d0e95-106">[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen Flow'n tietolähteeksi</span><span class="sxs-lookup"><span data-stu-id="d0e95-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="d0e95-107">Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com/en-us/) ja kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="d0e95-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="d0e95-108">Valitse sivun yläosan valintanauhassa **Omat Flow't**.</span><span class="sxs-lookup"><span data-stu-id="d0e95-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="d0e95-109">Valitse **Omat Flow't** -ikkunassa **Luo tyhjästä mallista** -asetus.</span><span class="sxs-lookup"><span data-stu-id="d0e95-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="d0e95-110">Valitse käytettävissä olevien käynnistimien luettelosta jokin [!INCLUDE[d365fin](includes/d365fin_md.md)] -käynnistin:</span><span class="sxs-lookup"><span data-stu-id="d0e95-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="d0e95-111">*Kun tietue on luotu*</span><span class="sxs-lookup"><span data-stu-id="d0e95-111">*When a record is created*,</span></span>  
    <span data-ttu-id="d0e95-112">*Kun tietue poistetaan*</span><span class="sxs-lookup"><span data-stu-id="d0e95-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="d0e95-113">*Kun tietuetta muokataan*</span><span class="sxs-lookup"><span data-stu-id="d0e95-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="d0e95-114">*Kun asiakkaan hyväksyntää on pyydetty*</span><span class="sxs-lookup"><span data-stu-id="d0e95-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="d0e95-115">*Kun yleisen päiväkirjan erän hyväksymistä on pyydetty*</span><span class="sxs-lookup"><span data-stu-id="d0e95-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="d0e95-116">*Kun yleisen päiväkirjan rivin hyväksymistä on pyydetty*</span><span class="sxs-lookup"><span data-stu-id="d0e95-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="d0e95-117">*Kun nimikkeen hyväksyntää on pyydetty*</span><span class="sxs-lookup"><span data-stu-id="d0e95-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="d0e95-118">*Kun ostoasiakirjan hyväksyntää on pyydetty*</span><span class="sxs-lookup"><span data-stu-id="d0e95-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="d0e95-119">*Kun myyntiasiakirjan hyväksyntää on pyydetty* tai</span><span class="sxs-lookup"><span data-stu-id="d0e95-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="d0e95-120">*Kun toimittajan hyväksyntää on pyydetty*.</span><span class="sxs-lookup"><span data-stu-id="d0e95-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="d0e95-121">Flow joka kysyy sinulta tietoja, joita tarvitaan [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen yhdistämistä varten.</span><span class="sxs-lookup"><span data-stu-id="d0e95-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="d0e95-122">Yrityksen nimi ja taulukon nimi on valittava, jos valitsit jonkin seuraavista käynnistimistä: *Kun tietue luodaan*, *Kun tietuetta muokataan* tai *Kun tietue poistetaan*.</span><span class="sxs-lookup"><span data-stu-id="d0e95-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="d0e95-123">Muissa käynnistimissä vain yrityksen nimi on yhdistettävä.</span><span class="sxs-lookup"><span data-stu-id="d0e95-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="d0e95-124">Flow näyttää luettelon yrityksistä taulukoista, joita voi käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ista.</span><span class="sxs-lookup"><span data-stu-id="d0e95-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d0e95-125">Nämä taulukot tai päätepisteet viittaavat kaikkiin [!INCLUDE[d365fin](includes/d365fin_md.md)]ista julkaistuihin verkkopalveluihin.</span><span class="sxs-lookup"><span data-stu-id="d0e95-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="d0e95-126">Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-sivulla tai avustettua **Määritä raportointi** -asetusopasta tai valitsemalla **Muokkaa Excelissä** -toiminnon missä tahansa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d0e95-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="d0e95-127">Olet nyt muodostanut yhteyden Finance and Operations, Business editionin tietoihin ja olet valmis aloittamaan oman työnkulun luomisen.</span><span class="sxs-lookup"><span data-stu-id="d0e95-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="d0e95-128">Lisätietoja on kohdassa [Flow-dokumentaatio](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="d0e95-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="d0e95-129">Lisätietoja Microsoft Flow'n vianmäärityksestä on kohdassa [Microsoft Flow -integroinnin vianmääritys](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="d0e95-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d0e95-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d0e95-130">See Also</span></span>
<span data-ttu-id="d0e95-131">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="d0e95-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="d0e95-132">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="d0e95-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="d0e95-133">[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="d0e95-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="d0e95-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="d0e95-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="d0e95-135">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="d0e95-135">Finance</span></span>](finance.md)  

