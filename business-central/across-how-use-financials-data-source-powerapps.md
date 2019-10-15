---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot PowerAppsin avulla yrityssovelluksen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305019"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a><span data-ttu-id="fdfe1-103">Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten PowerAppsin avulla</span><span class="sxs-lookup"><span data-stu-id="fdfe1-103">Connecting to Your Business Central Data to Build a Business App Using PowerApps</span></span>
<span data-ttu-id="fdfe1-104">Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietoja PowerAppsin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in PowerApps.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="fdfe1-105">Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja PowerApps -tili.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with PowerApps.</span></span>  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a><span data-ttu-id="fdfe1-106">[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen PowerAppsin tietolähteeksi</span><span class="sxs-lookup"><span data-stu-id="fdfe1-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in PowerApps</span></span>
1. <span data-ttu-id="fdfe1-107">Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) ja kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="fdfe1-108">Luo uusi kaaviosovellus valitsemalla aloitussivulla **Sovellukset**, **Luo sovellus** ja **Kangas**.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="fdfe1-109">Tämä sovellus suunnitellaan mobiililaitekäyttöön, mutta voit valita myös toisenlaisen mallin.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="fdfe1-110">PowerApp-sovelluksen luonnin seuraavana vaiheena on tietojen valinta.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-110">The next step to create a PowerApp is to select your data.</span></span> <span data-ttu-id="fdfe1-111">Valitse sivun vasemmassa yläosassa ensin nuolikuvake ja sitten **Uusi yhteys** -asetus.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="fdfe1-112">Tarjolla olevien yhteyksien joukosta, valitse **Business Central**, ja valitse sitten **Luo** nappula.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="fdfe1-113">PowerApps muodostaa [!INCLUDE [prodshort](includes/prodshort.md)] -yhteyden niillä käyttäjätiedoilla, joilla olet kirjautunut sisään.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-113">PowerApps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="fdfe1-114">Jos et ole järjestelmänvalvoja [!INCLUDE [prodshort](includes/prodshort.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4.  <span data-ttu-id="fdfe1-115">PowerApps näyttää luettelon *ympäristöistä ja yrityksistä*, jotka ovat käytettävissä [!INCLUDE [prodshort](includes/prodshort.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-115">PowerApps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="fdfe1-116">Valitse ne tiedot sisältävä ympäristö ja yritys, joihin haluat muodostaa yhteyden.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="fdfe1-117">Seuraavaksi näyttöön tulee ohjelmointirajapintaluettelo.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="fdfe1-118">Valitse **Ohjelmointirajapinta**, johon haluat muodostaa yhteyden.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="fdfe1-119">Nämä niin kutsutut taulukot ovat osa [!INCLUDE [prodshort](includes/prodshort.md)] API:a.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="fdfe1-120">Sinun ei tarvitse määrittää päätepisteitä itse – [!INCLUDE [prodshort](includes/prodshort.md)]in PowerApps-yhdistin tekee sen puolestasi.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for PowerApps does it for you.</span></span>  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

<span data-ttu-id="fdfe1-121">Tässä kohtaa olet yhdistänyt [!INCLUDE [prodshort](includes/prodshort.md)] dataasi ja olet valmis aloittamaan PowerAppisi rakentamisen.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-121">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="fdfe1-122">Voit luoda lisää ruutuja ja yhdistää lisädataan [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="fdfe1-122">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="fdfe1-123">Lisätietoja on kohdassa [Kaaviosovelluksen luominen PowerAppsin mallista](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="fdfe1-123">For more information, see [Create a canvas app from a template in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="fdfe1-124">Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="fdfe1-125">Lisätietoja on kohdassa [Kaaviosovelluksen tallentaminen julkaiseminen PowerAppsissa](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="fdfe1-125">For more information, see [Save and publish a canvas app in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="fdfe1-126">Jos haluat yhdistää [!INCLUDE [prodshort](includes/prodshort.md)]iin paikallisesti, sinun täytyy valita  **Business Central (paikallinen)** yhdistin vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-126">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fdfe1-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fdfe1-127">See Also</span></span>

[<span data-ttu-id="fdfe1-128">Kaaviosovelluksen luominen PowerAppsin mallista</span><span class="sxs-lookup"><span data-stu-id="fdfe1-128">Create a canvas app from a template in PowerApps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="fdfe1-129">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="fdfe1-129">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="fdfe1-130">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="fdfe1-130">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="fdfe1-131">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="fdfe1-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="fdfe1-132">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="fdfe1-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="fdfe1-133">Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="fdfe1-133">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
