---
title: Tietojen tuominen Financialsiin Excelin avulla | Microsoft Docs
description: "Voit lisätä asiakastietoja Excelissä oletusmäärityspaketin avulla ja tuoda tiedot takaisin Business Central -sovellukseen."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 05/17/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 379cfd2731bba2df6f5e31d2b8de2d72e2064ebb
ms.contentlocale: fi-fi
ms.lasthandoff: 05/17/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="b22d7-103">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="b22d7-103">Importing Business Data from Other Finance Systems</span></span>
<span data-ttu-id="b22d7-104">Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, voit luoda tyhjän yrityksen, ladata siihen omat tietosi ja testata uuden [!INCLUDE[d365fin](includes/d365fin_md.md)]-yrityksesi.</span><span class="sxs-lookup"><span data-stu-id="b22d7-104">When you sign up for [!INCLUDE[d365fin](includes/d365fin_md.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="b22d7-105">Yrityksen tällä hetkellä käytössä olevan rahoitusratkaisun mukaan voit siirtää tietoja asiakkaista, toimittajista, varastosta ja pankkitileistä.</span><span class="sxs-lookup"><span data-stu-id="b22d7-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="b22d7-106">Roolikeskuksen avustetun asennusoppaan avulla voit siirtää liiketoimintatiedot Excel-tiedostosta tai muista muodoista.</span><span class="sxs-lookup"><span data-stu-id="b22d7-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="b22d7-107">Ladattavissa olevien tiedostojen tyyppi riippuu käytettävissä olevista laajennuksista.</span><span class="sxs-lookup"><span data-stu-id="b22d7-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="b22d7-108">Voit esimerkiksi siirtää tietoja QuickBooks-ohjelmasta, koska [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää laajennuksen, joka käsittelee QuickBooks-tietojen muunnoksen.</span><span class="sxs-lookup"><span data-stu-id="b22d7-108">For example, you can migrate data from QuickBooks because [!INCLUDE[d365fin](includes/d365fin_md.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="b22d7-109">Jos haluat siirtää tietoja muista rahoitusratkaisuista, tarkista, onko kyseiselle ratkaisulle saatavana laajennus, tai tuo tiedot Excelistä.</span><span class="sxs-lookup"><span data-stu-id="b22d7-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b22d7-110"> sisältää malleja tileille, asiakkaille, toimittajille ja varastonimikkeille, joita voit kohdistaa tietojen tuomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b22d7-110"> includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="b22d7-111">Voit tuoda päätiedot ja joitakin tapahtumatietoja muista rahoitusjärjestelmistä [!INCLUDE[d365fin](includes/d365fin_md.md)]in oletusmäärityspaketin perusteella.</span><span class="sxs-lookup"><span data-stu-id="b22d7-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b22d7-112">Voit käsitellä tuotavaa pakettia **Määrityspaketit**-ikkunassa, jossa voit myös tarkistaa tiedot ennen paketin käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="b22d7-112">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="b22d7-113">Voit myös käyttää tietojen siirtotoimintoja, jos haluat tuoda tietoja QuickBooksista tai Dynamics GP:stä.</span><span class="sxs-lookup"><span data-stu-id="b22d7-113">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="b22d7-114">Lisätietoja on kohdassa [QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md) tai [Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="b22d7-114">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="b22d7-115">Jos kyseessä on suuri toteutustyö, voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman RapidStart Services -palvelua. Se koostuu työkalupaketista, jonka avulla määritetään uusia ratkaisuja asiakkaiden liiketoimintavaatimusten ja asetustietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="b22d7-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="b22d7-116">RapidStart Services sisältää myös liiketoimintatietojen tuontitoimintoja.</span><span class="sxs-lookup"><span data-stu-id="b22d7-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="b22d7-117">Lisätietoja on kohdassa [Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="b22d7-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="b22d7-118">Tietojen tuominen määrityspaketeista</span><span class="sxs-lookup"><span data-stu-id="b22d7-118">Importing Data from Configuration Packages</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b22d7-119"> sisältää määrityspaketin, jonka voit viedä Exceliin tietojen määrittämiseksi siellä.</span><span class="sxs-lookup"><span data-stu-id="b22d7-119"> includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="b22d7-120">Tämän jälkeen voit tuoda tiedot uudelleen Excelistä.</span><span class="sxs-lookup"><span data-stu-id="b22d7-120">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="b22d7-121">Paketissa on 27 taulukkoa, mukaan lukien päätiedot, kuten asiakkaat, toimittajat, nimikkeet ja tilit, muita perusasetustaulukkoja, kuten toimitustavat, ja tapahtumataulukot, kuten myyntiotsikko ja rivit.</span><span class="sxs-lookup"><span data-stu-id="b22d7-121">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="b22d7-122">Määrityspakettien käyttäminen on lisätoiminto ja onkin suositeltavaa keskustella sen käytöstä järjestelmänvalvojan kanssa.</span><span class="sxs-lookup"><span data-stu-id="b22d7-122">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="b22d7-123">Lisätietoja on kohdassa [Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="b22d7-123">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="b22d7-124">Tietojen käsittely Excelissä</span><span class="sxs-lookup"><span data-stu-id="b22d7-124">Working with Data in Excel</span></span>
<span data-ttu-id="b22d7-125">Kun tuot oletusmäärityspaketin Exceliin, luodussa työkirjassa on kutakin paketin taulukkoa vastaava laskentataulukko.</span><span class="sxs-lookup"><span data-stu-id="b22d7-125">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="b22d7-126">Yksinkertaistaaksesi tehtäviä voit hyödyntää XML manipulointityökaluja, jotka on sisällytetty Exceliin.</span><span class="sxs-lookup"><span data-stu-id="b22d7-126">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="b22d7-127">Voit käyttää myös Excelin valmiita funktioita tietojen muotoilun auttamiseksi ja tiedon asettamiseksi oikeisiin soluihin.</span><span class="sxs-lookup"><span data-stu-id="b22d7-127">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="b22d7-128">Lisää esimerkiksi tyhjä laskentataulukko ja kopioi vanhat tiedot siihen.</span><span class="sxs-lookup"><span data-stu-id="b22d7-128">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="b22d7-129">Tee sitten Excel-kaava määrittämään muunnostyökirjan tiedot viedyn laskentataulukon kenttien ja vanhojen asiakastietojen välille.</span><span class="sxs-lookup"><span data-stu-id="b22d7-129">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="b22d7-130">Kun olet yhdistänyt kaikki tiedot, kopioi tietoalue taulukon työkirjaan.</span><span class="sxs-lookup"><span data-stu-id="b22d7-130">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="b22d7-131">Älä muuta sarakkeita työkirjoissa.</span><span class="sxs-lookup"><span data-stu-id="b22d7-131">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="b22d7-132">Jos niitä on siirretty, muutettu tai poistettu, laskentataulukkoa ei voi tuoda [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="b22d7-132">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="b22d7-133">Oletusmäärityspaketin taulukot</span><span class="sxs-lookup"><span data-stu-id="b22d7-133">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="b22d7-134">Oletusmäärityspaketti tukee seuraavia taulukoita:</span><span class="sxs-lookup"><span data-stu-id="b22d7-134">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="b22d7-135">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="b22d7-135">Payment Terms</span></span>
-   <span data-ttu-id="b22d7-136">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="b22d7-136">Customer Price Group</span></span>
-   <span data-ttu-id="b22d7-137">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="b22d7-137">Shipment Method</span></span>
-   <span data-ttu-id="b22d7-138">Myyjä/Ostaja</span><span class="sxs-lookup"><span data-stu-id="b22d7-138">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="b22d7-139">Sijainti</span><span class="sxs-lookup"><span data-stu-id="b22d7-139">Location</span></span>
-   <span data-ttu-id="b22d7-140">KP-tili</span><span class="sxs-lookup"><span data-stu-id="b22d7-140">GL Account</span></span>
-   <span data-ttu-id="b22d7-141">Asiakas</span><span class="sxs-lookup"><span data-stu-id="b22d7-141">Customer</span></span>
-   <span data-ttu-id="b22d7-142">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="b22d7-142">Vendor</span></span>
-   <span data-ttu-id="b22d7-143">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="b22d7-143">Item</span></span>
-   <span data-ttu-id="b22d7-144">Myynnin tunnistetiedot</span><span class="sxs-lookup"><span data-stu-id="b22d7-144">Sales Header</span></span>
-   <span data-ttu-id="b22d7-145">Myyntirivi</span><span class="sxs-lookup"><span data-stu-id="b22d7-145">Sales Line</span></span>
-   <span data-ttu-id="b22d7-146">Ostojen tunnistetiedot</span><span class="sxs-lookup"><span data-stu-id="b22d7-146">Purchase Header</span></span>
-   <span data-ttu-id="b22d7-147">Ostorivi</span><span class="sxs-lookup"><span data-stu-id="b22d7-147">Purchase Line</span></span>
-   <span data-ttu-id="b22d7-148">Yleisen päiväkirjan rivi</span><span class="sxs-lookup"><span data-stu-id="b22d7-148">Gen. Journal Line</span></span>
-   <span data-ttu-id="b22d7-149">Nimikepäiväkirjan rivi</span><span class="sxs-lookup"><span data-stu-id="b22d7-149">Item Journal Line</span></span>
-   <span data-ttu-id="b22d7-150">Asiakkaan kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="b22d7-150">Customer Posting Group</span></span>
-   <span data-ttu-id="b22d7-151">Toimittajan kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="b22d7-151">Vendor Posting Group</span></span>
-   <span data-ttu-id="b22d7-152">Varaston kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="b22d7-152">Inventory Posting Group</span></span>
-   <span data-ttu-id="b22d7-153">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="b22d7-153">Unit of Measure</span></span>
-   <span data-ttu-id="b22d7-154">Ylein. liiketoim. kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="b22d7-154">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="b22d7-155">Yleinen tuotteen kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="b22d7-155">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="b22d7-156">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="b22d7-156">General Posting Setup</span></span>
-   <span data-ttu-id="b22d7-157">Territorio</span><span class="sxs-lookup"><span data-stu-id="b22d7-157">Territory</span></span>
-   <span data-ttu-id="b22d7-158">Nimikeluokka</span><span class="sxs-lookup"><span data-stu-id="b22d7-158">Item Category</span></span>
-   <span data-ttu-id="b22d7-159">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="b22d7-159">Sales Price</span></span>
-   <span data-ttu-id="b22d7-160">Ostohinta</span><span class="sxs-lookup"><span data-stu-id="b22d7-160">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="b22d7-161">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b22d7-161">See Also</span></span>
[<span data-ttu-id="b22d7-162">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="b22d7-162">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="b22d7-163">QuickBooks-tietojen siirto</span><span class="sxs-lookup"><span data-stu-id="b22d7-163">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="b22d7-164">Dynamics GP -tietojen siirto</span><span class="sxs-lookup"><span data-stu-id="b22d7-164">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

