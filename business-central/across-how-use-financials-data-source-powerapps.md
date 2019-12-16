---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot Power Apps -sovelluksen avulla yrityssovelluksen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 11/20/2019
ms.author: edupont
ms.openlocfilehash: 9cf587dca8224e742ecbde30bcabc35697bb6f2a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880998"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="a98cb-103">Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten Power Apps -sovellusten avulla</span><span class="sxs-lookup"><span data-stu-id="a98cb-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="a98cb-104">Voit käyttää [!INCLUDE[prodshort](includes/prodshort.md)]-tietoja Power Appsin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="a98cb-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="a98cb-105">Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power Apps -tili.</span><span class="sxs-lookup"><span data-stu-id="a98cb-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps"></a><span data-ttu-id="a98cb-106">[!INCLUDE[prodshort](includes/prodshort.md)]in lisääminen Power Appsin tietolähteeksi</span><span class="sxs-lookup"><span data-stu-id="a98cb-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="a98cb-107">Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/) ja kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="a98cb-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="a98cb-108">Luo uusi kaaviosovellus valitsemalla aloitussivulla **Sovellukset**, **Luo sovellus** ja **Kangas**.</span><span class="sxs-lookup"><span data-stu-id="a98cb-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="a98cb-109">Tämä sovellus suunnitellaan mobiililaitekäyttöön, mutta voit valita myös toisenlaisen mallin.</span><span class="sxs-lookup"><span data-stu-id="a98cb-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="a98cb-110">Power App -sovelluksen luonnin seuraavana vaiheena on tietojen valinta.</span><span class="sxs-lookup"><span data-stu-id="a98cb-110">The next step to create a Power App is to select your data.</span></span> <span data-ttu-id="a98cb-111">Valitse sivun vasemmassa yläosassa ensin nuolikuvake ja sitten **Uusi yhteys** -asetus.</span><span class="sxs-lookup"><span data-stu-id="a98cb-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="a98cb-112">Tarjolla olevien yhteyksien joukosta, valitse **Business Central**, ja valitse sitten **Luo** nappula.</span><span class="sxs-lookup"><span data-stu-id="a98cb-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="a98cb-113">Power Apps yhdistyy [!INCLUDE [prodshort](includes/prodshort.md)]in kanssa niillä tunnuksilla, joilla olet tällä hetkellä kirjautuneena sisään.</span><span class="sxs-lookup"><span data-stu-id="a98cb-113">Power Apps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="a98cb-114">Jos et ole järjestelmänvalvoja [!INCLUDE [prodshort](includes/prodshort.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.</span><span class="sxs-lookup"><span data-stu-id="a98cb-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="a98cb-115">Power Apps näyttää luettelon *ympäristöistä ja yrityksistä*, jotka ovat käytettävissä [!INCLUDE [prodshort](includes/prodshort.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="a98cb-115">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="a98cb-116">Valitse ne tiedot sisältävä ympäristö ja yritys, joihin haluat muodostaa yhteyden.</span><span class="sxs-lookup"><span data-stu-id="a98cb-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="a98cb-117">Seuraavaksi näyttöön tulee ohjelmointirajapintaluettelo.</span><span class="sxs-lookup"><span data-stu-id="a98cb-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="a98cb-118">Valitse **Ohjelmointirajapinta**, johon haluat muodostaa yhteyden.</span><span class="sxs-lookup"><span data-stu-id="a98cb-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="a98cb-119">Nämä niin kutsutut taulukot ovat osa [!INCLUDE [prodshort](includes/prodshort.md)] API:a.</span><span class="sxs-lookup"><span data-stu-id="a98cb-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="a98cb-120">Sinun ei tarvitse itse määrittää päätepisteitä - [!INCLUDE [prodshort](includes/prodshort.md)] yhdistäjä Power Appsille tekee sen puolestasi.</span><span class="sxs-lookup"><span data-stu-id="a98cb-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for Power Apps does it for you.</span></span>  

> [!NOTE]
> <span data-ttu-id="a98cb-121">Jos haluat sisällyttää muiden taulukoiden dataa [!INCLUDE [prodshort](includes/prodshort.md)] sovelluksessasi, sinun tulee työskennellä kehittäjän kanssa, jotta voitte määrittää mukautetun API:n [!INCLUDE [prodshort](includes/prodshort.md)]ille ja käyttää tätä mukautettua API:a mukautetun yhdistimen kautta Power Appsissa.</span><span class="sxs-lookup"><span data-stu-id="a98cb-121">If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="a98cb-122">Lisätietoja, katso [Mukautetun yhdistimen luominen tyhjästä](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="a98cb-122">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="a98cb-123">Tässä kohtaa olet yhdistänyt [!INCLUDE [prodshort](includes/prodshort.md)] dataasi ja olet valmis aloittamaan PowerAppisi rakentamisen.</span><span class="sxs-lookup"><span data-stu-id="a98cb-123">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="a98cb-124">Voit luoda lisää ruutuja ja yhdistää lisädataan [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="a98cb-124">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="a98cb-125">Lisätietoja, katso [Luo kaaviosovellus mallista Power Appsissa](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="a98cb-125">For more information, see [Create a canvas app from a template in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="a98cb-126">Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="a98cb-126">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="a98cb-127">Lisätietoja, katso [Tallenna ja julkaise kaaviosovelluksia Power Appsissa](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="a98cb-127">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="a98cb-128">Jos haluat yhdistää [!INCLUDE [prodshort](includes/prodshort.md)]iin paikallisesti, sinun täytyy valita  **Business Central (paikallinen)** yhdistin vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="a98cb-128">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a98cb-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a98cb-129">See Also</span></span>

<span data-ttu-id="a98cb-130">[Luo kaaviosovellus mallista Power Appsissa](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="a98cb-130">[Create a canvas app from a template in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)</span></span>  
[<span data-ttu-id="a98cb-131">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="a98cb-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="a98cb-132">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="a98cb-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="a98cb-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="a98cb-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="a98cb-134">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="a98cb-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="a98cb-135">Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="a98cb-135">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
