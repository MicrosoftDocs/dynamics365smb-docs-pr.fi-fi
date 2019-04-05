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
ms.date: 12/07/2018
ms.author: jswymer
ms.openlocfilehash: 27c137ea6309d40cddc94bc676ec7ea27d5c01fa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795542"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="2b7bb-103">Näyttäminen ja muokkaaminen Excelissä Business Centralista</span><span class="sxs-lookup"><span data-stu-id="2b7bb-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="2b7bb-104">Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit katsoa tietueita myös Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="2b7bb-105">Sen voi tehdä kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-105">To do this, you have two options.</span></span> <span data-ttu-id="2b7bb-106">Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="2b7bb-107">Toimintojen erot ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="2b7bb-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="2b7bb-108">Avaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="2b7bb-108">Open in Excel</span></span>

-    <span data-ttu-id="2b7bb-109">Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita rajoittavia suodattimia.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="2b7bb-110">Niinpä Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prodshort](includes/prodshort.md)]in sivulla.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="2b7bb-111">Voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista näitä muutoksia takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="2b7bb-112">Voit ainoastaan tallentaa muutokset Excel-tiedostoon omassa tietokoneessa.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="2b7bb-113">Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="2b7bb-114">Paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)] -versiossa **Avaa Excelissä** -toiminto ei ole käytettävissä, jos **Muokkaa Excelissä** -toiminto on.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="2b7bb-115">Muokkaa Excelissä</span><span class="sxs-lookup"><span data-stu-id="2b7bb-115">Edit in Excel</span></span>

-    <span data-ttu-id="2b7bb-116">Tätä toimintoa käytettäessä Excel-työkirja ei noudata sivulla olevia näytettäviä tietueita rajoittavia suodattimia.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="2b7bb-117">Tämän vuoksi Excel-työkirja sisältää kaikki käytettävissä olevat tietueet ja sarakkeet riippumatta siitä, mitä näkyy sivulla.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="2b7bb-118">**Muokkaa Excelissä** -toiminnon etuna on, että voit tehdä muutoksia tietueisiin Excelissä ja julkaista sitten muutokset takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="2b7bb-119">Toimintoa voi käyttää vain Windowsissa eikä se toimi Mac-käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="2b7bb-120">**Muokkaa Excelissä** on käytettävissä paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)] -versiossa vain, jos järjestelmänvalvoja on asentanut Excel-apuohjelman.</span><span class="sxs-lookup"><span data-stu-id="2b7bb-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="2b7bb-121">Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="2b7bb-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

## <a name="see-also"></a><span data-ttu-id="2b7bb-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2b7bb-122">See Also</span></span>

[<span data-ttu-id="2b7bb-123">Business Central -sovelluksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2b7bb-123">Working with Business Central</span></span>](ui-work-product.md)  
