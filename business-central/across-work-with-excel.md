---
title: Näyttäminen ja muokkaaminen Excelissä Business Centralista
description: Lisätietoja sivujen avaamisesta Microsoft Excelissä, jotta tietoja voi analysoida paremmin Business Centralissa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786930"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="afba2-103">Näyttäminen ja muokkaaminen Excelissä Business Centralista</span><span class="sxs-lookup"><span data-stu-id="afba2-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="afba2-104">Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit katsoa tietueita myös Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="afba2-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="afba2-105">Sen voi tehdä kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="afba2-105">To do this, you have two options.</span></span> <span data-ttu-id="afba2-106">Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="afba2-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="afba2-107">Toimintojen erot ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="afba2-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="afba2-108">Avaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="afba2-108">Open in Excel</span></span>

- <span data-ttu-id="afba2-109">Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat suodattimia.</span><span class="sxs-lookup"><span data-stu-id="afba2-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="afba2-110">Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prod_short](includes/prod_short.md)]in sivulla.</span><span class="sxs-lookup"><span data-stu-id="afba2-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="afba2-111">Voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista näitä muutoksia takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="afba2-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="afba2-112">Voit ainoastaan tallentaa muutokset Excel-tiedostoon omassa tietokoneessa.</span><span class="sxs-lookup"><span data-stu-id="afba2-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="afba2-113">Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="afba2-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="afba2-114">Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)]:ssa **Avaa Excelissä** -toiminto on oletusarvoisesti käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="afba2-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="afba2-115">Jos kuitenkin [!INCLUDE[prod_short](includes/prod_short.md)] määrität paikallisesti muokkausta varten tietoja Excelissä, **Avaa Excelissä-toiminnon** korvaa **Muokkaa Excelissä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="afba2-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="afba2-116">Muokkaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="afba2-116">Edit in Excel</span></span>

- <span data-ttu-id="afba2-117">Tämän toiminnon avulla Excel ottaa huomioon useimmat sivun suodattimet, jotka rajoittavat näytettäviä tietueita, joten Excel-työkirja sisältää lähes samat tietueet ja sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="afba2-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="afba2-118">**Muokkaa Excelissä** -toiminnon etuna on, että voit tehdä muutoksia tietueisiin Excelissä ja julkaista sitten muutokset takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="afba2-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="afba2-119">Toimintoa voi käyttää vain Windowsissa eikä se toimi Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="afba2-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="afba2-120">Voit vaihtaa käytössä olevaa yritystä.</span><span class="sxs-lookup"><span data-stu-id="afba2-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="afba2-121">Voit vaihtaa yritystä valitsemalla **Asetukset**-kuvakkeen ![Excel-apuohjelman asetukset](media/cogwheel.png "Excel-apuohjelman asetukset") Excel-apuohjelma-ruudussa ja valitsemalla sitten yritys **Yritys**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="afba2-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="afba2-122">Kun vaihdat yritystä, varmista, että **Ympäristö**-kenttä ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="afba2-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="afba2-123">Jos kenttä on tyhjä, määritä siihen jokin käytettävissä olevista asetuksista. Muussa tapauksessa apuohjelma ei toimi oikein.</span><span class="sxs-lookup"><span data-stu-id="afba2-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="afba2-124">Jos apuohjelmaan tehdään muutoksia, yhteyden päivittäminen edellyttää sen lataamista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="afba2-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="afba2-125">Lataamiseen käytetään ![Excelin apuohjelmavalikko](media/excel-addin-menu.png "Excel-apuohjelmavalikko") -valikko apuohjelman oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="afba2-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="afba2-126">Jos et voi ladata apuohjelmaa, keskustele järjestelmänvalvojan kanssa.</span><span class="sxs-lookup"><span data-stu-id="afba2-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="afba2-127">Jos olet järjestelmänvalvoja, katso lisätietoja kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="afba2-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="afba2-128">**Muokkaa Excelissä** -toiminto on käytettävissä paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa vain, jos järjestelmänvalvoja on määrittänyt Excel-apuohjelman. Se on käytettävissä vain WWW-asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="afba2-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="afba2-129">Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="afba2-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="afba2-130">Vaihtoehtojen välisiin eroihin tutustuminen</span><span class="sxs-lookup"><span data-stu-id="afba2-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="afba2-131">Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="afba2-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="afba2-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="afba2-132">See Also</span></span>

[<span data-ttu-id="afba2-133">Rahoituslaskelmien analysointi Microsoft Excel:issä</span><span class="sxs-lookup"><span data-stu-id="afba2-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="afba2-134">Business Centralin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="afba2-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="afba2-135">Excel-integraation parannukset vuoden 2019 2. julkaisuaallossa</span><span class="sxs-lookup"><span data-stu-id="afba2-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]