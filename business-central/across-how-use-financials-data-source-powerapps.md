---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot Power Appsin avulla yrityssovelluksen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 718d4378a897b187ba3073449869184fef5cec98
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924826"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="12d73-103">Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten Power Appsin avulla</span><span class="sxs-lookup"><span data-stu-id="12d73-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="12d73-104">Voit käyttää [!INCLUDE[prodshort](includes/prodshort.md)] -tietoja Power Appsin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="12d73-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="12d73-105">Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power Apps -tili.</span><span class="sxs-lookup"><span data-stu-id="12d73-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="12d73-106">[!INCLUDE[prodshort](includes/prodshort.md)]in lisääminen Power Appsin tietolähteeksi</span><span class="sxs-lookup"><span data-stu-id="12d73-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="12d73-107">Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/) ja kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="12d73-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="12d73-108">Valitse aloitussivun **Aloita tiedoista** -osassa **Muut tietolähteet** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="12d73-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="12d73-109">Power Apps Studio avautuu.</span><span class="sxs-lookup"><span data-stu-id="12d73-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="12d73-110">Ensimmäisellä kertaa kirjauduttaessa on määritettävä maa tai alue.</span><span class="sxs-lookup"><span data-stu-id="12d73-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="12d73-111">Tarjolla olevien yhteyksien joukosta, valitse **Business Central**, ja valitse sitten **Luo** nappula.</span><span class="sxs-lookup"><span data-stu-id="12d73-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="12d73-112">Power Apps muodostaa [!INCLUDE[prodshort](includes/prodshort.md)] -yhteyden niillä käyttäjätiedoilla, joilla olet kirjautunut sisään.</span><span class="sxs-lookup"><span data-stu-id="12d73-112">Power Apps will connect to your [!INCLUDE[prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="12d73-113">Jos et ole järjestelmänvalvoja [!INCLUDE[prodshort](includes/prodshort.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.</span><span class="sxs-lookup"><span data-stu-id="12d73-113">If you are not an administrator of your [!INCLUDE[prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="12d73-114">Power Apps näyttää luettelon *ympäristöistä ja yrityksistä*, jotka ovat käytettävissä [!INCLUDE[prodshort](includes/prodshort.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="12d73-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="12d73-115">Valitse ne tiedot sisältävä ympäristö ja yritys, joihin haluat muodostaa yhteyden, kuten *TUOTANTO – oma yritys*.</span><span class="sxs-lookup"><span data-stu-id="12d73-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="12d73-116">Seuraavaksi näkyviin tulee taulukkoluettelo, jotka näkyvät ympäristön ohjelmointirajapinnan osana.</span><span class="sxs-lookup"><span data-stu-id="12d73-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="12d73-117">Valitse taulukko, johon haluat muodostaa yhteyden ja valitse sitten **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="12d73-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="12d73-118">Power Appsin [!INCLUDE[prodshort](includes/prodshort.md)] -yhdistin näyttää nämä niin kutsutut taulukot päätepisteinä.</span><span class="sxs-lookup"><span data-stu-id="12d73-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prodshort](includes/prodshort.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="12d73-119">Jos haluat sisällyttää muiden taulukoiden dataa sovelluksessa [!INCLUDE[prodshort](includes/prodshort.md)], sinun tulee työskennellä kehittäjän kanssa, jotta voitte määrittää mukautetun API:n sovelluksessa [!INCLUDE[prodshort](includes/prodshort.md)] ja käyttää tätä mukautettua API:a mukautetun yhdistimen kautta Power Appsissa.</span><span class="sxs-lookup"><span data-stu-id="12d73-119">If you want to include data from other tables in [!INCLUDE[prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="12d73-120">Lisätietoja, katso [Mukautetun yhdistimen luominen tyhjästä](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="12d73-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="12d73-121">Tässä kohtaa olet yhdistänyt [!INCLUDE[prodshort](includes/prodshort.md)] dataasi ja olet valmis aloittamaan PowerAppisi rakentamisen.</span><span class="sxs-lookup"><span data-stu-id="12d73-121">At this point, you have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="12d73-122">Voit luoda lisää ruutuja ja yhdistää lisädataan [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="12d73-122">You can add additional screens and connect to additional data from your [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="12d73-123">Lisätietoja on kohdassa [Kaaviosovelluksen luominen Power Appsin mallista](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="12d73-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="12d73-124">Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="12d73-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="12d73-125">Lisätietoja on kohdassa [Kaaviosovelluksen tallentaminen julkaiseminen Power Appsissa](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="12d73-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="12d73-126">Jos haluat yhdistää [!INCLUDE[prodshort](includes/prodshort.md)]iin paikallisesti, sinun täytyy valita  **Business Central (paikallinen)** yhdistin vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="12d73-126">If you want to connect to [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="12d73-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="12d73-127">See Also</span></span>

[<span data-ttu-id="12d73-128">Kaaviosovelluksen luominen Power Appsin mallista</span><span class="sxs-lookup"><span data-stu-id="12d73-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="12d73-129">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="12d73-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="12d73-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="12d73-130">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="12d73-131">Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="12d73-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
