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
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 99fe339426b755b70983d8ec9345858357043347
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808743"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="c51db-103">Näyttäminen ja muokkaaminen Excelissä Business Centralista</span><span class="sxs-lookup"><span data-stu-id="c51db-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="c51db-104">Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit katsoa tietueita myös Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="c51db-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="c51db-105">Sen voi tehdä kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="c51db-105">To do this, you have two options.</span></span> <span data-ttu-id="c51db-106">Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="c51db-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="c51db-107">Toimintojen erot ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="c51db-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="c51db-108">Avaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="c51db-108">Open in Excel</span></span>

- <span data-ttu-id="c51db-109">Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat suodattimia.</span><span class="sxs-lookup"><span data-stu-id="c51db-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="c51db-110">Niinpä Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prodshort](includes/prodshort.md)]in sivulla.</span><span class="sxs-lookup"><span data-stu-id="c51db-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="c51db-111">Voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista näitä muutoksia takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="c51db-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="c51db-112">Voit ainoastaan tallentaa muutokset Excel-tiedostoon omassa tietokoneessa.</span><span class="sxs-lookup"><span data-stu-id="c51db-112">You can only save the changes to Excel file on your computer.</span></span> 

- <span data-ttu-id="c51db-113">Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="c51db-113">This action works on both on Windows and macOS.</span></span> 

> [!NOTE]
> <span data-ttu-id="c51db-114">Paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)]:ssa **Avaa Excelissä** -toiminto on oletusarvoisesti käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="c51db-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="c51db-115">Jos kuitenkin [!INCLUDE [prodshort](includes/prodshort.md)] määrität paikallisesti muokkausta varten tietoja Excelissä, **Avaa Excelissä-toiminnon** korvaa **Muokkaa Excelissä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c51db-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="c51db-116">Muokkaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="c51db-116">Edit in Excel</span></span>

- <span data-ttu-id="c51db-117">Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat useimpia suodattimia.</span><span class="sxs-lookup"><span data-stu-id="c51db-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="c51db-118">Niinpä Excel-työkirjassa on lähes samat tietueet ja sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="c51db-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="c51db-119">**Muokkaa Excelissä** -toiminnon etuna on, että voit tehdä muutoksia tietueisiin Excelissä ja julkaista sitten muutokset takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="c51db-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="c51db-120">Toimintoa voi käyttää vain Windowsissa eikä se toimi Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="c51db-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="c51db-121">Tätä tehostettiin 2019 Release Wave 2 -versiossa.</span><span class="sxs-lookup"><span data-stu-id="c51db-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="c51db-122">Lisätietoja on kohdassa [Excel-integroinnin parannukset](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="c51db-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="c51db-123">**Muokkaa Excelissä** on käytettävissä paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)] -versiossa vain, jos järjestelmänvalvoja on määrittänyt Excel-apuohjelman.</span><span class="sxs-lookup"><span data-stu-id="c51db-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="c51db-124">Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="c51db-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="c51db-125">[!INCLUDE[prodshort](includes/prodshort.md)]:lle paikallisesti, tämä ominaisuus on käytettävissä vain web-asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="c51db-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="c51db-126">Vaihtoehtojen välisiin eroihin tutustuminen</span><span class="sxs-lookup"><span data-stu-id="c51db-126">See the differences between the options</span></span> 
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="c51db-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c51db-127">See Also</span></span>
[<span data-ttu-id="c51db-128">Business Centralin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="c51db-128">Working with Business Central</span></span>](ui-work-product.md)  
