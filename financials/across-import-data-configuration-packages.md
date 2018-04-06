---
title: Tietojen tuominen Financialsiin Excelin avulla | Microsoft Docs
description: "Voit lisätä asiakastietoja Excelissä oletusmäärityspaketin avulla ja tuoda tiedot takaisin Finance and Operations, Business editioniin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 591d8100100ee717a932d188a87545fe4098a001
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="c1916-103">Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla</span><span class="sxs-lookup"><span data-stu-id="c1916-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="c1916-104">Voit tuoda päätiedot ja joitakin tapahtumatietoja muista rahoitusjärjestelmistä [!INCLUDE[d365fin](includes/d365fin_md.md)]in oletusmäärityspaketin perusteella.</span><span class="sxs-lookup"><span data-stu-id="c1916-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c1916-105">Voit käsitellä tuotavaa pakettia **Määrityspaketit**-ikkunassa, jossa voit myös tarkistaa tiedot ennen paketin käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="c1916-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!NOTE]  
> <span data-ttu-id="c1916-106">Määrityspaketit ovat [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman RapidStart Services -palvelun osa. Ne ovat laajoja työkalupaketteja, joiden avulla määritetään uusia ratkaisuja asiakkaiden liiketoimintavaatimusten ja asetustietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="c1916-106">Configuration packages are part of RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="c1916-107">RapidStart Services sisältää myös vanhojen tietojen tuontitoimintoja.</span><span class="sxs-lookup"><span data-stu-id="c1916-107">RapidStart Services also offers functionality for import of legacy data.</span></span> <span data-ttu-id="c1916-108">Lisätietoja on kohdassa [Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="c1916-108">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

> [!TIP]  
>   <span data-ttu-id="c1916-109">Voit myös käyttää tietojen siirtotoimintoja, jos haluat tuoda tietoja QuickBooksista tai Dynamics GP:stä.</span><span class="sxs-lookup"><span data-stu-id="c1916-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="c1916-110">Lisätietoja on kohdassa [QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md) tai [Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="c1916-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="c1916-111">Tietojen käsittely Excelissä</span><span class="sxs-lookup"><span data-stu-id="c1916-111">Working with Data in Excel</span></span>
<span data-ttu-id="c1916-112">Kun tuot oletusmäärityspaketin Exceliin, luodussa työkirjassa on kutakin paketin taulukkoa vastaava laskentataulukko.</span><span class="sxs-lookup"><span data-stu-id="c1916-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="c1916-113">Yksinkertaistaaksesi tehtäviä voit hyödyntää XML manipulointityökaluja, jotka on sisällytetty Exceliin.</span><span class="sxs-lookup"><span data-stu-id="c1916-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="c1916-114">Voit käyttää myös Excelin valmiita funktioita tietojen muotoilun auttamiseksi ja tiedon asettamiseksi oikeisiin soluihin.</span><span class="sxs-lookup"><span data-stu-id="c1916-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="c1916-115">Lisää esimerkiksi tyhjä laskentataulukko ja kopioi vanhat tiedot siihen.</span><span class="sxs-lookup"><span data-stu-id="c1916-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="c1916-116">Tee sitten Excel-kaava määrittämään muunnostyökirjan tiedot viedyn laskentataulukon kenttien ja vanhojen asiakastietojen välille.</span><span class="sxs-lookup"><span data-stu-id="c1916-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="c1916-117">Kun olet yhdistänyt kaikki tiedot, kopioi tietoalue taulukon työkirjaan.</span><span class="sxs-lookup"><span data-stu-id="c1916-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="c1916-118">Älä muuta sarakkeita työkirjoissa.</span><span class="sxs-lookup"><span data-stu-id="c1916-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="c1916-119">Jos niitä on siirretty, muutettu tai poistettu, laskentataulukkoa ei voi tuoda [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="c1916-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="c1916-120">Oletusmäärityspaketin taulukot</span><span class="sxs-lookup"><span data-stu-id="c1916-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="c1916-121">Oletusmäärityspaketti tukee seuraavia taulukoita:</span><span class="sxs-lookup"><span data-stu-id="c1916-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="c1916-122">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="c1916-122">Payment Terms</span></span>
-   <span data-ttu-id="c1916-123">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="c1916-123">Customer Price Group</span></span>
-   <span data-ttu-id="c1916-124">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="c1916-124">Shipment Method</span></span>
-   <span data-ttu-id="c1916-125">Myyjä/Ostaja</span><span class="sxs-lookup"><span data-stu-id="c1916-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="c1916-126">Sijainti</span><span class="sxs-lookup"><span data-stu-id="c1916-126">Location</span></span>
-   <span data-ttu-id="c1916-127">KP-tili</span><span class="sxs-lookup"><span data-stu-id="c1916-127">GL Account</span></span>
-   <span data-ttu-id="c1916-128">Asiakas</span><span class="sxs-lookup"><span data-stu-id="c1916-128">Customer</span></span>
-   <span data-ttu-id="c1916-129">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="c1916-129">Vendor</span></span>
-   <span data-ttu-id="c1916-130">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="c1916-130">Item</span></span>
-   <span data-ttu-id="c1916-131">Myynnin tunnistetiedot</span><span class="sxs-lookup"><span data-stu-id="c1916-131">Sales Header</span></span>
-   <span data-ttu-id="c1916-132">Myyntirivi</span><span class="sxs-lookup"><span data-stu-id="c1916-132">Sales Line</span></span>
-   <span data-ttu-id="c1916-133">Ostojen tunnistetiedot</span><span class="sxs-lookup"><span data-stu-id="c1916-133">Purchase Header</span></span>
-   <span data-ttu-id="c1916-134">Ostorivi</span><span class="sxs-lookup"><span data-stu-id="c1916-134">Purchase Line</span></span>
-   <span data-ttu-id="c1916-135">Yleisen päiväkirjan rivi</span><span class="sxs-lookup"><span data-stu-id="c1916-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="c1916-136">Nimikepäiväkirjan rivi</span><span class="sxs-lookup"><span data-stu-id="c1916-136">Item Journal Line</span></span>
-   <span data-ttu-id="c1916-137">Asiakkaan kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="c1916-137">Customer Posting Group</span></span>
-   <span data-ttu-id="c1916-138">Toimittajan kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="c1916-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="c1916-139">Varaston kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="c1916-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="c1916-140">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="c1916-140">Unit of Measure</span></span>
-   <span data-ttu-id="c1916-141">Ylein. liiketoim. kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="c1916-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="c1916-142">Yleinen tuotteen kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="c1916-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="c1916-143">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="c1916-143">General Posting Setup</span></span>
-   <span data-ttu-id="c1916-144">Territorio</span><span class="sxs-lookup"><span data-stu-id="c1916-144">Territory</span></span>
-   <span data-ttu-id="c1916-145">Nimikeluokka</span><span class="sxs-lookup"><span data-stu-id="c1916-145">Item Category</span></span>
-   <span data-ttu-id="c1916-146">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="c1916-146">Sales Price</span></span>
-   <span data-ttu-id="c1916-147">Ostohinta</span><span class="sxs-lookup"><span data-stu-id="c1916-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="c1916-148">Asiakastietojen tuominen</span><span class="sxs-lookup"><span data-stu-id="c1916-148">Importing Customer Data</span></span>
<span data-ttu-id="c1916-149">Kun asiakastiedot on annettu Excelissä, tiedot tuodaan [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="c1916-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c1916-150">Tiedot tuodaan **Määrityspaketit**-ikkunassa Excel-tiedostosta. Voit myös tarkistaa tässä ikkunassa, että tiedot ovat yhdenmukaiset [!INCLUDE[d365fin](includes/d365fin_md.md)]in kanssa ennen paketin käyttöä.</span><span class="sxs-lookup"><span data-stu-id="c1916-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1916-151">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c1916-151">See Also</span></span>
[<span data-ttu-id="c1916-152">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="c1916-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="c1916-153">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="c1916-153">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c1916-154">QuickBooks-tietojen siirto</span><span class="sxs-lookup"><span data-stu-id="c1916-154">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="c1916-155">Dynamics GP -tietojen siirto</span><span class="sxs-lookup"><span data-stu-id="c1916-155">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

