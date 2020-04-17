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
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 2c6600ac7fe9f6e0aa44554883209039faabbd99
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187506"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="5ba85-103">Näyttäminen ja muokkaaminen Excelissä Business Centralista</span><span class="sxs-lookup"><span data-stu-id="5ba85-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="5ba85-104">Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit katsoa tietueita myös Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="5ba85-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="5ba85-105">Sen voi tehdä kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="5ba85-105">To do this, you have two options.</span></span> <span data-ttu-id="5ba85-106">Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="5ba85-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="5ba85-107">Toimintojen erot ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="5ba85-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="5ba85-108">Avaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="5ba85-108">Open in Excel</span></span>

- <span data-ttu-id="5ba85-109">Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat suodattimia.</span><span class="sxs-lookup"><span data-stu-id="5ba85-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="5ba85-110">Niinpä Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prodshort](includes/prodshort.md)]in sivulla.</span><span class="sxs-lookup"><span data-stu-id="5ba85-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="5ba85-111">Voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista näitä muutoksia takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="5ba85-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="5ba85-112">Voit ainoastaan tallentaa muutokset Excel-tiedostoon omassa tietokoneessa.</span><span class="sxs-lookup"><span data-stu-id="5ba85-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="5ba85-113">Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="5ba85-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="5ba85-114">Paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)]:ssa **Avaa Excelissä** -toiminto on oletusarvoisesti käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5ba85-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="5ba85-115">Jos kuitenkin [!INCLUDE [prodshort](includes/prodshort.md)] määrität paikallisesti muokkausta varten tietoja Excelissä, **Avaa Excelissä-toiminnon** korvaa **Muokkaa Excelissä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="5ba85-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="5ba85-116">Muokkaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="5ba85-116">Edit in Excel</span></span>

- <span data-ttu-id="5ba85-117">Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat useimpia suodattimia.</span><span class="sxs-lookup"><span data-stu-id="5ba85-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="5ba85-118">Niinpä Excel-työkirjassa on lähes samat tietueet ja sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="5ba85-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="5ba85-119">**Muokkaa Excelissä** -toiminnon etuna on, että voit tehdä muutoksia tietueisiin Excelissä ja julkaista sitten muutokset takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="5ba85-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="5ba85-120">Toimintoa voi käyttää vain Windowsissa eikä se toimi Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="5ba85-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="5ba85-121">Voit vaihtaa käytössä olevaa yritystä.</span><span class="sxs-lookup"><span data-stu-id="5ba85-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="5ba85-122">Se tehdään valitsemalla **Asetukset**-kuvake ![Excel-apuohjelman asetukset](media/cogwheel.png "Excel-apuohjelman asetukset") Excel-apuohjelma-ruudussa ja valitsemalla sitten yritys **Yritys**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5ba85-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="5ba85-123">Kun vaihdat yritystä, varmista, että **Ympäristö**-kenttä ei ole tyhjä.</span><span class="sxs-lookup"><span data-stu-id="5ba85-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="5ba85-124">Jos kenttä on tyhjä, määritä siihen jokin käytettävissä olevista asetuksista. Muussa tapauksessa apuohjelma ei toimi oikein.</span><span class="sxs-lookup"><span data-stu-id="5ba85-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="5ba85-125">Excel-apuohjelmaa parannettiin vuoden 2019 julkaisuaallossa 2.</span><span class="sxs-lookup"><span data-stu-id="5ba85-125">The Excel Add-in was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="5ba85-126">Lisätietoja on kohdassa [Excel-integroinnin parannukset](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="5ba85-126">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="5ba85-127">**Muokkaa Excelissä** -toiminto on käytettävissä paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)] -versiossa vain, jos järjestelmänvalvoja on määrittänyt Excel-apuohjelman. Se on käytettävissä vain WWW-asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="5ba85-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="5ba85-128">Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="5ba85-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span> <span data-ttu-id="5ba85-129">Paikallinen [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5ba85-129">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="5ba85-130">Vaihtoehtojen välisiin eroihin tutustuminen</span><span class="sxs-lookup"><span data-stu-id="5ba85-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="5ba85-131">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="5ba85-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="5ba85-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5ba85-132">See Also</span></span>
[<span data-ttu-id="5ba85-133">Business Centralin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="5ba85-133">Working with Business Central</span></span>](ui-work-product.md)  
