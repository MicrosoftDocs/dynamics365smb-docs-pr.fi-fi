---
title: Näyttäminen ja muokkaaminen Excelissä Business Centralista | Microsoft Docs
description: Lisätietoja sivujen avaamisesta Microsoft Excelissä, jotta tietoja voi analysoida paremmin Business Centralissa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 07/03/2020
ms.author: jswymer
ms.openlocfilehash: f782b3ce19baa29d9268f3fdf742d2aa6112957f
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534587"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="318f0-103">Näyttäminen ja muokkaaminen Excelissä Business Centralista</span><span class="sxs-lookup"><span data-stu-id="318f0-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="318f0-104">Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit katsoa tietueita myös Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="318f0-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="318f0-105">Sen voi tehdä kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="318f0-105">To do this, you have two options.</span></span> <span data-ttu-id="318f0-106">Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="318f0-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="318f0-107">Toimintojen erot ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="318f0-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="318f0-108">Avaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="318f0-108">Open in Excel</span></span>

- <span data-ttu-id="318f0-109">Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat suodattimia.</span><span class="sxs-lookup"><span data-stu-id="318f0-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="318f0-110">Niinpä Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prodshort](includes/prodshort.md)]in sivulla.</span><span class="sxs-lookup"><span data-stu-id="318f0-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="318f0-111">Voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista näitä muutoksia takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="318f0-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="318f0-112">Voit ainoastaan tallentaa muutokset Excel-tiedostoon omassa tietokoneessa.</span><span class="sxs-lookup"><span data-stu-id="318f0-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="318f0-113">Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="318f0-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="318f0-114">Paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)]:ssa **Avaa Excelissä** -toiminto on oletusarvoisesti käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="318f0-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="318f0-115">Jos kuitenkin [!INCLUDE[prodshort](includes/prodshort.md)] määrität paikallisesti muokkausta varten tietoja Excelissä, **Avaa Excelissä-toiminnon** korvaa **Muokkaa Excelissä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="318f0-115">However, if you set up [!INCLUDE[prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="318f0-116">Muokkaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="318f0-116">Edit in Excel</span></span>

- <span data-ttu-id="318f0-117">Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat useimpia suodattimia.</span><span class="sxs-lookup"><span data-stu-id="318f0-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="318f0-118">Niinpä Excel-työkirjassa on lähes samat tietueet ja sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="318f0-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="318f0-119">**Muokkaa Excelissä** -toiminnon etuna on, että voit tehdä muutoksia tietueisiin Excelissä ja julkaista sitten muutokset takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="318f0-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="318f0-120">Toimintoa voi käyttää vain Windowsissa eikä se toimi Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="318f0-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="318f0-121">Voit vaihtaa käytössä olevaa yritystä.</span><span class="sxs-lookup"><span data-stu-id="318f0-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="318f0-122">Se tehdään valitsemalla **Asetukset**-kuvake ![Excel-apuohjelman asetukset](media/cogwheel.png "Excel-apuohjelman asetukset") Excel-apuohjelma-ruudussa ja valitsemalla sitten yritys **Yritys**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="318f0-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="318f0-123">Kun vaihdat yritystä, varmista, että **Ympäristö**-kenttä ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="318f0-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="318f0-124">Jos kenttä on tyhjä, määritä siihen jokin käytettävissä olevista asetuksista. Muussa tapauksessa apuohjelma ei toimi oikein.</span><span class="sxs-lookup"><span data-stu-id="318f0-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="318f0-125">Jos apuohjelmaan tehdään muutoksia, yhteyden päivittäminen edellyttää sen lataamista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="318f0-125">If you make changes to the add-in, you must reload it in order to update the connection.</span></span> <span data-ttu-id="318f0-126">Lataamiseen käytetään ![Excelin apuohjelmavalikko](media/excel-addin-menu.png "Excel-apuohjelmavalikko") -valikko apuohjelman oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="318f0-126">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span>

> [!NOTE]
> <span data-ttu-id="318f0-127">**Muokkaa Excelissä** -toiminto on käytettävissä paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)] -versiossa vain, jos järjestelmänvalvoja on määrittänyt Excel-apuohjelman. Se on käytettävissä vain WWW-asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="318f0-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="318f0-128">Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="318f0-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="318f0-129">Vaihtoehtojen välisiin eroihin tutustuminen</span><span class="sxs-lookup"><span data-stu-id="318f0-129">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="318f0-130">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="318f0-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="318f0-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="318f0-131">See Also</span></span>

[<span data-ttu-id="318f0-132">Business Centralin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="318f0-132">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="318f0-133">Excel-integraation parannukset vuoden 2019 2. julkaisuaallossa</span><span class="sxs-lookup"><span data-stu-id="318f0-133">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
