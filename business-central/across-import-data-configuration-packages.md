---
title: Tietojen tuominen Business Central -ohjelmaan Excelin avulla
description: Voit lisätä asiakastietoja Excelissä oletusmäärityspaketin avulla ja tuoda tiedot takaisin Business Central -sovellukseen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3885d9e07a6ea417bf2dc7de5881e6d3278ca10
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379246"
---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="68fef-103">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="68fef-103">Importing Business Data from Other Finance Systems</span></span>

<span data-ttu-id="68fef-104">Kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)]iin, voit luoda tyhjän yrityksen, ladata siihen omat tietosi ja testata uuden [!INCLUDE[prod_short](includes/prod_short.md)]-yrityksesi.</span><span class="sxs-lookup"><span data-stu-id="68fef-104">When you sign up for [!INCLUDE[prod_short](includes/prod_short.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[prod_short](includes/prod_short.md)] company.</span></span> <span data-ttu-id="68fef-105">Yrityksen tällä hetkellä käytössä olevan rahoitusratkaisun mukaan voit siirtää tietoja asiakkaista, toimittajista, varastosta ja pankkitileistä.</span><span class="sxs-lookup"><span data-stu-id="68fef-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="68fef-106">Roolikeskuksen avustetun asennusoppaan avulla voit siirtää liiketoimintatiedot Excel-tiedostosta tai muista muodoista.</span><span class="sxs-lookup"><span data-stu-id="68fef-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="68fef-107">Ladattavissa olevien tiedostojen tyyppi riippuu käytettävissä olevista laajennuksista.</span><span class="sxs-lookup"><span data-stu-id="68fef-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="68fef-108">Voit esimerkiksi siirtää tietoja QuickBooks-ohjelmasta, koska [!INCLUDE[prod_short](includes/prod_short.md)] sisältää laajennuksen, joka käsittelee QuickBooks-tietojen muunnoksen.</span><span class="sxs-lookup"><span data-stu-id="68fef-108">For example, you can migrate data from QuickBooks because [!INCLUDE[prod_short](includes/prod_short.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="68fef-109">Jos haluat siirtää tietoja muista rahoitusratkaisuista, tarkista, onko kyseiselle ratkaisulle saatavana laajennus, tai tuo tiedot Excelistä.</span><span class="sxs-lookup"><span data-stu-id="68fef-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="68fef-110">sisältää malleja tileille, asiakkaille, toimittajille ja varastonimikkeille, joita voit kohdistaa tietojen tuomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="68fef-110">includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="68fef-111">Voit tuoda päätiedot ja joitakin tapahtumatietoja muista rahoitusjärjestelmistä [!INCLUDE[prod_short](includes/prod_short.md)]in oletusmäärityspaketin perusteella.</span><span class="sxs-lookup"><span data-stu-id="68fef-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="68fef-112">Voit käsitellä tuotavaa pakettia **Määrityspaketit**-sivulla, jossa voit myös tarkistaa tiedot ennen paketin käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="68fef-112">On the **Configuration Packages** page, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="68fef-113">Suosittelemme, että käytät tietojen siirtotoimintoja, jos haluat tuoda tietoja Dynamics GP:stä, Dynamics NAVista tai QuickBooksista.</span><span class="sxs-lookup"><span data-stu-id="68fef-113">We recommend that you use data migration wizards to import data from Dynamics GP, Dynamics NAV, or QuickBooks.</span></span> <span data-ttu-id="68fef-114">Lisätietoja on kohdassa [Paikallisten tietojen siirtäminen Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) -ohjelmaan hallintasisällössä tai [QuickBooks-tiedonsiirto-ohjelmassa](ui-extensions-quickbooks-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="68fef-114">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content, or [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="68fef-115">Jos kyseessä on suuri toteutustyö, voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in RapidStart Servicesia. Se koostuu työkalupaketista, jonka avulla määritetään uusia ratkaisuja asiakkaiden liiketoimintavaatimusten ja asetustietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="68fef-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="68fef-116">RapidStart Services sisältää myös liiketoimintatietojen tuontitoimintoja.</span><span class="sxs-lookup"><span data-stu-id="68fef-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="68fef-117">Lisätietoja on kohdassa [Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="68fef-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

<span data-ttu-id="68fef-118">Voit tuoda nimikekuvat **Varastonhallinnan asetukset** -sivulla olevalla toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="68fef-118">To import item pictures, you can use a dedicated function on the **Inventory Setup** page.</span></span> <span data-ttu-id="68fef-119">Lisätietoja on kohdassa [Useiden nimikekuvien tuominen](inventory-how-import-item-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="68fef-119">For more information, see [Import Multiple Item Pictures](inventory-how-import-item-pictures.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="68fef-120">Tietojen tuominen määrityspaketeista</span><span class="sxs-lookup"><span data-stu-id="68fef-120">Importing Data from Configuration Packages</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="68fef-121">sisältää määrityspaketin, jonka voit viedä Exceliin tietojen määrittämiseksi siellä.</span><span class="sxs-lookup"><span data-stu-id="68fef-121">includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="68fef-122">Tämän jälkeen voit tuoda tiedot uudelleen Excelistä.</span><span class="sxs-lookup"><span data-stu-id="68fef-122">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="68fef-123">Paketissa on 27 taulukkoa, mukaan lukien päätiedot, kuten asiakkaat, toimittajat, nimikkeet ja tilit, muita perusasetustaulukkoja, kuten toimitustavat, ja tapahtumataulukot, kuten myyntiotsikko ja rivit.</span><span class="sxs-lookup"><span data-stu-id="68fef-123">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="68fef-124">Määrityspakettien käyttäminen on lisätoiminto ja onkin suositeltavaa keskustella sen käytöstä järjestelmänvalvojan kanssa.</span><span class="sxs-lookup"><span data-stu-id="68fef-124">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="68fef-125">Lisätietoja on kohdassa [Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="68fef-125">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="68fef-126">Tietojen käsittely Excelissä</span><span class="sxs-lookup"><span data-stu-id="68fef-126">Working with Data in Excel</span></span>
<span data-ttu-id="68fef-127">Kun tuot oletusmäärityspaketin Exceliin, luodussa työkirjassa on kutakin paketin taulukkoa vastaava laskentataulukko.</span><span class="sxs-lookup"><span data-stu-id="68fef-127">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="68fef-128">Yksinkertaistaaksesi tehtäviä voit hyödyntää XML manipulointityökaluja, jotka on sisällytetty Exceliin.</span><span class="sxs-lookup"><span data-stu-id="68fef-128">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="68fef-129">Voit käyttää myös Excelin valmiita funktioita tietojen muotoilun auttamiseksi ja tiedon asettamiseksi oikeisiin soluihin.</span><span class="sxs-lookup"><span data-stu-id="68fef-129">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="68fef-130">Lisää esimerkiksi tyhjä laskentataulukko ja kopioi vanhat tiedot siihen.</span><span class="sxs-lookup"><span data-stu-id="68fef-130">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="68fef-131">Tee sitten Excel-kaava määrittämään muunnostyökirjan tiedot viedyn laskentataulukon kenttien ja vanhojen asiakastietojen välille.</span><span class="sxs-lookup"><span data-stu-id="68fef-131">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="68fef-132">Kun olet yhdistänyt kaikki tiedot, kopioi tietoalue taulukon työkirjaan.</span><span class="sxs-lookup"><span data-stu-id="68fef-132">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="68fef-133">Älä muuta sarakkeita työkirjoissa.</span><span class="sxs-lookup"><span data-stu-id="68fef-133">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="68fef-134">Jos niitä on siirretty, muutettu tai poistettu, laskentataulukkoa ei voi tuoda [!INCLUDE[prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="68fef-134">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="68fef-135">BLOB-tyypin kenttiä ei voi viedä tai tuoda Excelin avulla.</span><span class="sxs-lookup"><span data-stu-id="68fef-135">Fields of type Blob cannot be exported/imported using Excel.</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="68fef-136">Oletusmäärityspaketin taulukot</span><span class="sxs-lookup"><span data-stu-id="68fef-136">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="68fef-137">Oletusmäärityspaketti tukee seuraavia taulukoita:</span><span class="sxs-lookup"><span data-stu-id="68fef-137">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="68fef-138">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="68fef-138">Payment Terms</span></span>
-   <span data-ttu-id="68fef-139">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="68fef-139">Customer Price Group</span></span>
-   <span data-ttu-id="68fef-140">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="68fef-140">Shipment Method</span></span>
-   <span data-ttu-id="68fef-141">Myyjä/Ostaja</span><span class="sxs-lookup"><span data-stu-id="68fef-141">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="68fef-142">Sijainti</span><span class="sxs-lookup"><span data-stu-id="68fef-142">Location</span></span>
-   <span data-ttu-id="68fef-143">KP-tili</span><span class="sxs-lookup"><span data-stu-id="68fef-143">GL Account</span></span>
-   <span data-ttu-id="68fef-144">Asiakas</span><span class="sxs-lookup"><span data-stu-id="68fef-144">Customer</span></span>
-   <span data-ttu-id="68fef-145">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="68fef-145">Vendor</span></span>
-   <span data-ttu-id="68fef-146">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="68fef-146">Item</span></span>
-   <span data-ttu-id="68fef-147">Myynnin tunnistetiedot</span><span class="sxs-lookup"><span data-stu-id="68fef-147">Sales Header</span></span>
-   <span data-ttu-id="68fef-148">Myyntirivi</span><span class="sxs-lookup"><span data-stu-id="68fef-148">Sales Line</span></span>
-   <span data-ttu-id="68fef-149">Ostojen tunnistetiedot</span><span class="sxs-lookup"><span data-stu-id="68fef-149">Purchase Header</span></span>
-   <span data-ttu-id="68fef-150">Ostorivi</span><span class="sxs-lookup"><span data-stu-id="68fef-150">Purchase Line</span></span>
-   <span data-ttu-id="68fef-151">Yl.</span><span class="sxs-lookup"><span data-stu-id="68fef-151">Gen.</span></span> <span data-ttu-id="68fef-152">päiväkirjan rivi</span><span class="sxs-lookup"><span data-stu-id="68fef-152">Journal Line</span></span>
-   <span data-ttu-id="68fef-153">Nimikepäiväkirjan rivi</span><span class="sxs-lookup"><span data-stu-id="68fef-153">Item Journal Line</span></span>
-   <span data-ttu-id="68fef-154">Asiakkaan kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="68fef-154">Customer Posting Group</span></span>
-   <span data-ttu-id="68fef-155">Toimittajan kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="68fef-155">Vendor Posting Group</span></span>
-   <span data-ttu-id="68fef-156">Varaston kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="68fef-156">Inventory Posting Group</span></span>
-   <span data-ttu-id="68fef-157">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="68fef-157">Unit of Measure</span></span>
-   <span data-ttu-id="68fef-158">Yl.</span><span class="sxs-lookup"><span data-stu-id="68fef-158">Gen.</span></span> <span data-ttu-id="68fef-159">liiketoim. kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="68fef-159">Business Posting Group</span></span>
-   <span data-ttu-id="68fef-160">Yl.</span><span class="sxs-lookup"><span data-stu-id="68fef-160">Gen.</span></span> <span data-ttu-id="68fef-161">Tuotteen kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="68fef-161">Product Posting Group</span></span>
-   <span data-ttu-id="68fef-162">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="68fef-162">General Posting Setup</span></span>
-   <span data-ttu-id="68fef-163">Territorio</span><span class="sxs-lookup"><span data-stu-id="68fef-163">Territory</span></span>
-   <span data-ttu-id="68fef-164">Nimikeluokka</span><span class="sxs-lookup"><span data-stu-id="68fef-164">Item Category</span></span>
-   <span data-ttu-id="68fef-165">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="68fef-165">Sales Price</span></span>
-   <span data-ttu-id="68fef-166">Ostohinta</span><span class="sxs-lookup"><span data-stu-id="68fef-166">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="68fef-167">Katso myös</span><span class="sxs-lookup"><span data-stu-id="68fef-167">See Also</span></span>
[<span data-ttu-id="68fef-168">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="68fef-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="68fef-169">Paikallisten tietojen siirtäminen Business Central Onlineen</span><span class="sxs-lookup"><span data-stu-id="68fef-169">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[<span data-ttu-id="68fef-170">QuickBooks-tietojen siirto</span><span class="sxs-lookup"><span data-stu-id="68fef-170">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="68fef-171">Useiden nimikekuvien tuominen</span><span class="sxs-lookup"><span data-stu-id="68fef-171">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]