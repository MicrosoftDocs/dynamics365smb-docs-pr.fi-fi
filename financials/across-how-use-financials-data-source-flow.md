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
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 277dda7c954380138af1ecabc02d77121f35aac7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="f605d-103">[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen automaattisessa työnkulussa</span><span class="sxs-lookup"><span data-stu-id="f605d-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="f605d-104">Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja työnkulun osana Microsoft Flow'ssa.</span><span class="sxs-lookup"><span data-stu-id="f605d-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="f605d-105">Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Flow-tili.</span><span class="sxs-lookup"><span data-stu-id="f605d-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="f605d-106">[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen Flow'n tietolähteeksi</span><span class="sxs-lookup"><span data-stu-id="f605d-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="f605d-107">Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com/en-us/) ja kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="f605d-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="f605d-108">Valitse sivun yläosan valintanauhassa **Omat Flow't**.</span><span class="sxs-lookup"><span data-stu-id="f605d-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="f605d-109">Valitse **Omat Flow't** -ikkunassa **Luo tyhjästä mallista** -asetus.</span><span class="sxs-lookup"><span data-stu-id="f605d-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="f605d-110">Valitse käytettävien käynnistimien luettelosta jompikumpi kahdesta [!INCLUDE[d365fin](includes/d365fin_md.md)]-käynnistimestä: *Kun tietue on luotu* tai *Kun tietuetta on muutettu*.</span><span class="sxs-lookup"><span data-stu-id="f605d-110">From the list of available triggers, select one of the two [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available: *When a record is created*, or *When a record is modified*.</span></span>
5. <span data-ttu-id="f605d-111">Flow näyttää yhteyssivun, joka kysyy sinulta tietoja, jotka on yhdistettävä [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoihin.</span><span class="sxs-lookup"><span data-stu-id="f605d-111">Flow will display a connection page that prompts you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="f605d-112">Yhteyttä varten on määritettävä yhteyden nimi, ODatan URL-osoite, käyttäjänimi, salasana ja yrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="f605d-112">To connect, you must specify a name for the connection, an OData URL, username, password, and company name.</span></span>

   <span data-ttu-id="f605d-113">Voit kopioida *OData URL* -osoitteeksi minkä tahansa [!INCLUDE[d365fin](includes/d365fin_md.md)]in **WWW-palvelut**-sivulla mainitun verkkopalvelun OData V4 URL-osoitteen, kuten `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.</span><span class="sxs-lookup"><span data-stu-id="f605d-113">For the *OData URL*, you can copy the OData V4 URL of any of the web services that are listed in the **Web Services** page in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.</span></span>  

   <span data-ttu-id="f605d-114">Käytä *yrityksen nimenä* nimeä, joka näkyy [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Oman yrityksen tiedot** -ikkunan **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f605d-114">For the *Company Name*, use the name that is shown in the **Name** field in the **Company Information** window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f605d-115">Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on useita yrityksiä, valitse sopiva yrityksen nimi **Yritykset**-ikkunassa olevasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="f605d-115">If your [!INCLUDE[d365fin](includes/d365fin_md.md)] contains multiple companies, choose the relevant company name from the list in the **Companies** window.</span></span> <span data-ttu-id="f605d-116">Varmista kummassakin tapauksessa, että ohjatussa PowerApps-toiminnossa määrittämäsi nimi on kirjoitettu täsmälleen samoin kuin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Esimerkki: `My Company`.</span><span class="sxs-lookup"><span data-stu-id="f605d-116">In both cases, make sure that the name that you specify in the PowerApps wizard matches exactly the text shown in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as `My Company`.</span></span>

   <span data-ttu-id="f605d-117">Käytä käyttäjänimenä ja salasanana tilille [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Käyttäjät**-ikkunassa määritettyä nimeä ja verkkopalvelun käyttöoikeusavainta.</span><span class="sxs-lookup"><span data-stu-id="f605d-117">For the username and password, use the name and web service access key that are specified for your account in the **Users** window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f605d-118">Käyttäjänimesi on esimerkiksi *JÄRJESTELMÄNVALVOJA* ja salasanana toimiva verkkopalvelun käyttöoikeusavain on *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.</span><span class="sxs-lookup"><span data-stu-id="f605d-118">For example, your username is *ADMIN*, and the web service access key that serves as your password is *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.</span></span> <span data-ttu-id="f605d-119">Lisätietoja on kohdassa [Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="f605d-119">For more information, see [How to: Manage Users and Permissions](ui-how-users-permissions.md).</span></span>
6. <span data-ttu-id="f605d-120">Jatka valitsemalla sivun alareunassa **Luo**-painike.</span><span class="sxs-lookup"><span data-stu-id="f605d-120">Choose the **Create** button at the bottom of the page to continue.</span></span>

   <span data-ttu-id="f605d-121">Flow näyttää luettelon taulukoista, joita voi käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ista.</span><span class="sxs-lookup"><span data-stu-id="f605d-121">Flow will show a list of tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f605d-122">Nämä taulukot tai päätepisteet viittaavat kaikkiin [!INCLUDE[d365fin](includes/d365fin_md.md)]ista julkaistuihin verkkopalveluihin.</span><span class="sxs-lookup"><span data-stu-id="f605d-122">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="f605d-123">Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-sivulla tai avustettua **Määritä raportointi** -asetusopasta tai valitsemalla **Muokkaa Excelissä** -toiminnon missä tahansa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f605d-123">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
7. <span data-ttu-id="f605d-124">Valitse Flow'ssa käytettävät tiedot.</span><span class="sxs-lookup"><span data-stu-id="f605d-124">Choose the data that you want to use for in Flow.</span></span>

<span data-ttu-id="f605d-125">Olet nyt muodostanut yhteyden Dynamics 365 -tietoihin ja olet valmis aloittamaan oman Flow'n luomisen.</span><span class="sxs-lookup"><span data-stu-id="f605d-125">At this point, you have successfully connected to your Dynamics 365 data and are ready to begin building your flow.</span></span> <span data-ttu-id="f605d-126">Lisätietoja on kohdassa [Flow-dokumentaatio](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="f605d-126">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

## <a name="see-also"></a><span data-ttu-id="f605d-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f605d-127">See Also</span></span>
<span data-ttu-id="f605d-128">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="f605d-128">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="f605d-129">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="f605d-129">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="f605d-130">[Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="f605d-130">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="f605d-131">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="f605d-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="f605d-132">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="f605d-132">Finance</span></span>](finance.md)  

