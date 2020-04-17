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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187890"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="f152b-103">[!INCLUDE [prodlong](includes/prodlong.md)]in käyttö Power BI:n tietolähteenä raportteja luotaessa</span><span class="sxs-lookup"><span data-stu-id="f152b-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="f152b-104">Voit määrittää [!INCLUDE[prodlong](includes/prodlong.md)]in tiedot käytettäviksi Power BI:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.</span><span class="sxs-lookup"><span data-stu-id="f152b-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="f152b-105">Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power BI -tili.</span><span class="sxs-lookup"><span data-stu-id="f152b-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="f152b-106">Lisäksi on ladattava [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span><span class="sxs-lookup"><span data-stu-id="f152b-106">You must also download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="f152b-107">Lisätietoja on kohdassa [Pika-aloitus: Power BI Desktopin tietoihin yhdistäminen](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="f152b-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="f152b-108">[!INCLUDE[prodshort](includes/prodshort.md)]in lisääminen Power BI Desktopin tietolähteeksi</span><span class="sxs-lookup"><span data-stu-id="f152b-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="f152b-109">Valitse Power BI Desktopin vasemmassa siirtymisruudussa **Nouda tiedot**.</span><span class="sxs-lookup"><span data-stu-id="f152b-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="f152b-110">Valitse **Nouda tiedot** -sivulla **Online Services**. Valitse sitten **Microsoft Dynamics 365 Business Central** ja valitse lopuksi **Muodosta yhteys** -painike.</span><span class="sxs-lookup"><span data-stu-id="f152b-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="f152b-111">Power BI avaa ohjatun toiminnon, joka auttaa yhteyden muodostusprosessissa. Tähän kuuluu myös sovellukseen [!INCLUDE [prodshort](includes/prodshort.md)] kirjautuminen.</span><span class="sxs-lookup"><span data-stu-id="f152b-111">Power BI displays a wizard that will guide you through the connection process, including signing into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="f152b-112">Valitse **Kirjaudu sisään**ja valitse sitten haluamasi tili.</span><span class="sxs-lookup"><span data-stu-id="f152b-112">Choose **Sign in**, and then choose the relevant account.</span></span> <span data-ttu-id="f152b-113">Käytä samaa tiliä, jonka avulla kirjaudut sisään sovellukseen [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="f152b-113">Use the same account that you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="f152b-114">Jatka valitsemalla **Muodosta yhteys**.</span><span class="sxs-lookup"><span data-stu-id="f152b-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="f152b-115">Ohjatussa Power BI -toiminnossa on luettelo Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ympäristöistä, yrityksistä ja tietolähteistä.</span><span class="sxs-lookup"><span data-stu-id="f152b-115">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies, and data sources.</span></span> <span data-ttu-id="f152b-116">Nämä tietolähteet viittaavat kaikkiin sovelluksesta [!INCLUDE [prodshort](includes/prodshort.md)] julkaistuihin verkkopalveluihin.</span><span class="sxs-lookup"><span data-stu-id="f152b-116">These data sources represent all the web services that you have published from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

    <span data-ttu-id="f152b-117">Voit myös luoda uuden verkkopalvelun URL-osoitteen sovelluksessa [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="f152b-117">You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead.</span></span> <span data-ttu-id="f152b-118">Valitse yksi seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="f152b-118">Choose one of the following methods:</span></span>

      - <span data-ttu-id="f152b-119">Käytä **Luo tietojoukkoa** -toiminto **Verkkopalvelut**-sivulla</span><span class="sxs-lookup"><span data-stu-id="f152b-119">Use the **Create Data Set** action on the **Web Services** page</span></span>
      - <span data-ttu-id="f152b-120">Käytä **raportoinnin määrityksen** asetusten ohjattua määritysopasta</span><span class="sxs-lookup"><span data-stu-id="f152b-120">Use the **Set Up Reporting** Assisted Setup guide</span></span>
      - <span data-ttu-id="f152b-121">Valitse **Muokkaa Excelissä** -toiminto luetteloista</span><span class="sxs-lookup"><span data-stu-id="f152b-121">Choose the **Edit in Excel** action in any lists</span></span>

5. <span data-ttu-id="f152b-122">Määritä tietomalliin lisättävät tiedot ja valitse sitten **Lataa**-painike.</span><span class="sxs-lookup"><span data-stu-id="f152b-122">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
6. <span data-ttu-id="f152b-123">Lisää uusia [!INCLUDE [prodshort](includes/prodshort.md)]in tai muita tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f152b-123">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="f152b-124">Kun yhteys [!INCLUDE [prodshort](includes/prodshort.md)]iin on muodostettu, sinua ei pyydetä kirjautumaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f152b-124">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="f152b-125">Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa.</span><span class="sxs-lookup"><span data-stu-id="f152b-125">Once the data is loaded, you can see it in the right navigation on the page.</span></span> <span data-ttu-id="f152b-126">Olet muodostanut yhteyden sovelluksen [!INCLUDE [prodshort](includes/prodshort.md)] tietoihin ja voit aloittaa oman Power BI -raportin luomisen.</span><span class="sxs-lookup"><span data-stu-id="f152b-126">You have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data, and you can begin building your Power BI report.</span></span>  

<span data-ttu-id="f152b-127">[!INCLUDE [prodshort](includes/prodshort.md)] -teematiedosto kannattaa tuoda ennen raportin luontia.</span><span class="sxs-lookup"><span data-stu-id="f152b-127">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="f152b-128">Teematiedosto luo värivalikoiman, jonka avulla voit luoda raportteja samalla värityylillä kuin [!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksissa ilman, että kunkin visuaalisen ominaisuuden mukautetut värit on määritettävä erikseen.</span><span class="sxs-lookup"><span data-stu-id="f152b-128">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="f152b-129">Lisätietoja on [Power BI -dokumentaatiossa](/power-bi/consumer/).</span><span class="sxs-lookup"><span data-stu-id="f152b-129">For more information, see the [Power BI documentation](/power-bi/consumer/).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="f152b-130">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="f152b-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="f152b-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f152b-131">See Also</span></span>

[<span data-ttu-id="f152b-132">Yritystietojen ottaminen käyttöön Power BI:tä varten</span><span class="sxs-lookup"><span data-stu-id="f152b-132">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="f152b-133">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="f152b-133">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="f152b-134">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="f152b-134">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="f152b-135">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="f152b-135">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="f152b-136">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="f152b-136">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="f152b-137">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="f152b-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="f152b-138">Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin</span><span class="sxs-lookup"><span data-stu-id="f152b-138">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
