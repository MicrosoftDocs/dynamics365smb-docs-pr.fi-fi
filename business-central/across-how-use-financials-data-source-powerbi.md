---
title: Business Centralin käyttäminen Power BI -raporteissa | Microsoft Docs
description: Määritä tiedot käytettäviksi Power BI:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 07/08/2019
ms.author: edupont
ms.openlocfilehash: c86f1c3c40f80ec993d0a3a89154047ddf9e8126
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755239"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="3e3b7-103">[!INCLUDE [prodlong](includes/prodlong.md)]in käyttö Power BI:n tietolähteenä raportteja luotaessa</span><span class="sxs-lookup"><span data-stu-id="3e3b7-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="3e3b7-104">Voit määrittää [!INCLUDE[prodlong](includes/prodlong.md)]in tiedot käytettäviksi Power BI:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="3e3b7-105">Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power BI -tili.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="3e3b7-106">Lisäksi sinun on ladattava [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="3e3b7-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span> <span data-ttu-id="3e3b7-107">Lisätietoja on kohdassa [Pika-aloitus: Power BI Desktopin tietoihin yhdistäminen](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="3e3b7-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="3e3b7-108">[!INCLUDE[prodshort](includes/prodshort.md)]in lisääminen Power BI Desktopin tietolähteeksi</span><span class="sxs-lookup"><span data-stu-id="3e3b7-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="3e3b7-109">Valitse Power BI Desktopin vasemmassa siirtymisruudussa **Nouda tiedot**.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="3e3b7-110">Valitse **Nouda tiedot** -sivulla **Online Services**. Valitse sitten **Microsoft Dynamics 365 Business Central** ja valitse lopuksi **Muodosta yhteys** -painike.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="3e3b7-111">Power BI avaa ohjatun toiminnon, joka auttaa yhteyden muodostusprosessissa.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-111">Power BI displays a wizard that will guide you through the connection process.</span></span> <span data-ttu-id="3e3b7-112">Sinua pyydetään kirjatumaan [!INCLUDE [prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-112">You will be prompted to sign into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3e3b7-113">Valitse ensin **Kirjaudu sisään** ja sitten tili, johon haluat kirjautua.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-113">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="3e3b7-114">Valitse sama tili, jolla kirjaudut [!INCLUDE [prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-114">This should be the same account you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="3e3b7-115">Jatka valitsemalla **Muodosta yhteys**.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-115">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="3e3b7-116">Ohjatussa Power BI -toiminnossa on luettelo Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]in yrityksistä ja tietolähteistä.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-116">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] companies and data sources.</span></span> <span data-ttu-id="3e3b7-117">Nämä tietolähteet viittaavat kaikkiin verkkopalveluihin, jotka on julkaistu kustakin [!INCLUDE [prodshort](includes/prodshort.md)]in yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-117">These data source represent all the web services that you have published from each company in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

  ![powerbi_webservices.png](media/across-how-use-financials-data-source-powerbi/powerbi_webservices.png)

5. <span data-ttu-id="3e3b7-119">Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE [prodshort](includes/prodshort.md)]issa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-sivulla tai asetusten ohjattua **Määritä raportointi** -määritystä tai valitsemalla **Muokkaa Excelissä** -toiminnon jossakin luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-119">Alternatively, create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] by using the **Create Data Set** action on the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="3e3b7-120">Määritä tietomalliin lisättävät tiedot ja valitse sitten **Lataa**-painike.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-120">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="3e3b7-121">Lisää uusia [!INCLUDE [prodshort](includes/prodshort.md)]in tai muita tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-121">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="3e3b7-122">Kun yhteys [!INCLUDE [prodshort](includes/prodshort.md)]iin on muodostettu, sinua ei pyydetä kirjautumaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-122">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="3e3b7-123">Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-123">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="3e3b7-124">Olet nyt muodostanut yhteyden [!INCLUDE [prodshort](includes/prodshort.md)] -tietoihin ja olet valmis aloittamaan oman Power BI -raportin luomisen.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-124">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your Power BI report.</span></span>  

<span data-ttu-id="3e3b7-125">[!INCLUDE [prodshort](includes/prodshort.md)] -teematiedosto kannattaa tuoda ennen raportin luontia.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-125">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="3e3b7-126">Teematiedosto luo värivalikoiman, jonka avulla voit luoda raportteja samalla värityylillä kuin [!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksissa ilman, että kunkin visuaalisen ominaisuuden mukautetut värit on määritettävä erikseen.</span><span class="sxs-lookup"><span data-stu-id="3e3b7-126">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="3e3b7-127">Lisätietoja on [Power BI -dokumentaatiossa](/power-bi/consumer/power-bi-consumer-landing/).</span><span class="sxs-lookup"><span data-stu-id="3e3b7-127">For more information, see the [Power BI documentation](/power-bi/consumer/power-bi-consumer-landing/).</span></span>

## <a name="see-also"></a><span data-ttu-id="3e3b7-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3e3b7-128">See Also</span></span>

[<span data-ttu-id="3e3b7-129">Yritystietojen ottaminen käyttöön Power BI:tä varten</span><span class="sxs-lookup"><span data-stu-id="3e3b7-129">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="3e3b7-130">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="3e3b7-130">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="3e3b7-131">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="3e3b7-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="3e3b7-132">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="3e3b7-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="3e3b7-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="3e3b7-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="3e3b7-134">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="3e3b7-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="3e3b7-135">Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin</span><span class="sxs-lookup"><span data-stu-id="3e3b7-135">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
