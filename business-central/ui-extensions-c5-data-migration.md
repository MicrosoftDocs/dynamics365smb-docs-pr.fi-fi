---
title: C5-tietojen siirtolaajennuksen käyttäminen | Microsoft Docs
description: Voit käyttää tätä laajennusta asiakkaiden, toimittajien, nimikkeiden ja pääkirjanpidon tilien siirtämiseen Microsoft Dynamics C5 2012:sta Business Centraliin.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 0f257b81f1e36e86e40e67ca8ba07169ec22d938
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747591"
---
# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="8fc2e-103">Tietojen siirron C5-laajennus</span><span class="sxs-lookup"><span data-stu-id="8fc2e-103">The C5 Data Migration Extension</span></span>

<span data-ttu-id="8fc2e-104">Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, nimikkeitä ja pääkirjanpidon tilejä Microsoft Dynamics C5 2012 -versiosta [!INCLUDE[prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamics C5 2012 to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8fc2e-105">Voit siirtää myös pääkirjanpidon tilien vanhat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="8fc2e-106">[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yrityksessä ei saa olla tietoja.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-106">The company in [!INCLUDE[prod_short](includes/prod_short.md)] must not contain any data.</span></span> <span data-ttu-id="8fc2e-107">Kun siirto on käynnistetty, asiakkaiden, toimittajien, nimikkeiden tai tilien luominen ei ole sallittua. Voit luoda niitä siirron valmistuttua.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="8fc2e-108">Mitkä tiedot siirretään?</span><span class="sxs-lookup"><span data-stu-id="8fc2e-108">What Data is Migrated?</span></span>
<span data-ttu-id="8fc2e-109">Seuraavat kunkin objektit tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="8fc2e-109">The following data is migrated for each entity:</span></span>

### <a name="customers"></a><span data-ttu-id="8fc2e-110">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-110">Customers</span></span>

* <span data-ttu-id="8fc2e-111">Kontaktit</span><span class="sxs-lookup"><span data-stu-id="8fc2e-111">Contacts</span></span>  
* <span data-ttu-id="8fc2e-112">Sijainti</span><span class="sxs-lookup"><span data-stu-id="8fc2e-112">Location</span></span>
* <span data-ttu-id="8fc2e-113">Maa</span><span class="sxs-lookup"><span data-stu-id="8fc2e-113">Country</span></span>
* <span data-ttu-id="8fc2e-114">Asiakkaan dimensiota (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="8fc2e-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="8fc2e-115">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="8fc2e-115">Shipment method</span></span>
* <span data-ttu-id="8fc2e-116">Myyjä</span><span class="sxs-lookup"><span data-stu-id="8fc2e-116">Sales Person</span></span>
* <span data-ttu-id="8fc2e-117">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="8fc2e-117">Payment terms</span></span>
* <span data-ttu-id="8fc2e-118">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="8fc2e-118">Payment method</span></span>
* <span data-ttu-id="8fc2e-119">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="8fc2e-119">Customer price group</span></span>
* <span data-ttu-id="8fc2e-120">Asiakkaan laskun alennus</span><span class="sxs-lookup"><span data-stu-id="8fc2e-120">Customer invoice discount</span></span>

<span data-ttu-id="8fc2e-121">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="8fc2e-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="8fc2e-122">Asiakkaan kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="8fc2e-122">Customer posting setup</span></span>
* <span data-ttu-id="8fc2e-123">Yleisen päiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="8fc2e-123">General journal batch</span></span>
* <span data-ttu-id="8fc2e-124">Avoimet tapahtumat (asiakastapahtumat)</span><span class="sxs-lookup"><span data-stu-id="8fc2e-124">Open transactions (customer ledger entries)</span></span>

### <a name="vendors"></a><span data-ttu-id="8fc2e-125">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-125">Vendors</span></span>

* <span data-ttu-id="8fc2e-126">Kontaktit</span><span class="sxs-lookup"><span data-stu-id="8fc2e-126">Contacts</span></span>
* <span data-ttu-id="8fc2e-127">Sijainti</span><span class="sxs-lookup"><span data-stu-id="8fc2e-127">Location</span></span>
* <span data-ttu-id="8fc2e-128">Maa</span><span class="sxs-lookup"><span data-stu-id="8fc2e-128">Country</span></span>
* <span data-ttu-id="8fc2e-129">Toimittajan dimensiot (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="8fc2e-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="8fc2e-130">Laskualennus</span><span class="sxs-lookup"><span data-stu-id="8fc2e-130">Invoice discount</span></span>
* <span data-ttu-id="8fc2e-131">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="8fc2e-131">Shipment method</span></span>
* <span data-ttu-id="8fc2e-132">Ostaja</span><span class="sxs-lookup"><span data-stu-id="8fc2e-132">Purchaser</span></span>
* <span data-ttu-id="8fc2e-133">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="8fc2e-133">Payment terms</span></span>
* <span data-ttu-id="8fc2e-134">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="8fc2e-134">Payment method</span></span>
* <span data-ttu-id="8fc2e-135">Toimittajan laskun alennus</span><span class="sxs-lookup"><span data-stu-id="8fc2e-135">Vendor invoice discount</span></span>

<span data-ttu-id="8fc2e-136">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="8fc2e-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="8fc2e-137">Toimittajan kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="8fc2e-137">Vendor posting setup</span></span>
* <span data-ttu-id="8fc2e-138">Yleisen päiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="8fc2e-138">General journal batch</span></span>
* <span data-ttu-id="8fc2e-139">Avoimet tapahtumat (toimittajatapahtumat)</span><span class="sxs-lookup"><span data-stu-id="8fc2e-139">Open transactions (vendor ledger entries)</span></span>

### <a name="items"></a><span data-ttu-id="8fc2e-140">Nimikkeet</span><span class="sxs-lookup"><span data-stu-id="8fc2e-140">Items</span></span>

* <span data-ttu-id="8fc2e-141">Sijainti</span><span class="sxs-lookup"><span data-stu-id="8fc2e-141">Location</span></span>
* <span data-ttu-id="8fc2e-142">Maa</span><span class="sxs-lookup"><span data-stu-id="8fc2e-142">Country</span></span>
* <span data-ttu-id="8fc2e-143">Nimikkeen dimensiot (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="8fc2e-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="8fc2e-144">Myynnin rivialennukset</span><span class="sxs-lookup"><span data-stu-id="8fc2e-144">Sales line discounts</span></span>
* <span data-ttu-id="8fc2e-145">Asiakkaan alennusryhmät</span><span class="sxs-lookup"><span data-stu-id="8fc2e-145">Customer discount groups</span></span>
* <span data-ttu-id="8fc2e-146">Nimikealennusryhmät</span><span class="sxs-lookup"><span data-stu-id="8fc2e-146">Item discount groups</span></span>
* <span data-ttu-id="8fc2e-147">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="8fc2e-147">Sales price</span></span>
* <span data-ttu-id="8fc2e-148">Tavaranimike</span><span class="sxs-lookup"><span data-stu-id="8fc2e-148">Tariff number</span></span>
* <span data-ttu-id="8fc2e-149">Mittayksiköt</span><span class="sxs-lookup"><span data-stu-id="8fc2e-149">Units of measure</span></span>
* <span data-ttu-id="8fc2e-150">Nimikkeen seurantakoodi</span><span class="sxs-lookup"><span data-stu-id="8fc2e-150">Item tracking code</span></span>
* <span data-ttu-id="8fc2e-151">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="8fc2e-151">Customer price group</span></span>
* <span data-ttu-id="8fc2e-152">Kokoonpanon tuoterakenteet</span><span class="sxs-lookup"><span data-stu-id="8fc2e-152">Assembly BOMs</span></span>

<span data-ttu-id="8fc2e-153">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="8fc2e-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="8fc2e-154">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="8fc2e-154">Inventory posting setup</span></span>
* <span data-ttu-id="8fc2e-155">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="8fc2e-155">General posting setup</span></span>
* <span data-ttu-id="8fc2e-156">Nimikepäiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="8fc2e-156">Item journal batch</span></span>
* <span data-ttu-id="8fc2e-157">Avoimet tapahtumat (nimiketapahtumat)</span><span class="sxs-lookup"><span data-stu-id="8fc2e-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="8fc2e-158">Jos avoimissa tapahtumissa käytetään ulkomaanvaluuttoja, myös kyseisten valuuttojen vaihtokurssit siirretään.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="8fc2e-159">Muita vaihtokursseja ei siirretä.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-159">Other exchange rates are not migrated.</span></span>

### <a name="chart-of-accounts"></a><span data-ttu-id="8fc2e-160">Tilikartta</span><span class="sxs-lookup"><span data-stu-id="8fc2e-160">Chart of Accounts</span></span>

* <span data-ttu-id="8fc2e-161">Vakiodimensiot: osasto, kustannupaikka, tarkoitus</span><span class="sxs-lookup"><span data-stu-id="8fc2e-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="8fc2e-162">Historialliset KP-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="8fc2e-163">Historialliset KP-tapahtumat, joita käsitellään hieman eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="8fc2e-164">Kun siirrät tietoja, määrität **Nykyinen jakso** -parametrin.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="8fc2e-165">Tämä parametri määrittää, miten KP-tapahtumia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="8fc2e-166">Tämän päivämäärän jälkeen tapahtumat siirretään erikseen.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="8fc2e-167">Tapahtumat ennen tätä päivämäärää koostetaan tilikohtaisesti ja siirretään yhtenä summana.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="8fc2e-168">Esimerkiksi oletetaan, että tapahtumia on vuosina 2015, 2016, 2017 ja 2018, ja määrität 1. tammikuuta 2017 Nykyinen jakso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="8fc2e-169">Kunkin tilin tapahtumien 31.12.2016 tai sitä ennen summat kootaan yhteen yleisen päiväkirjan riviin kullekin KP-tilille.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="8fc2e-170">Kaikki tapahtumat tämän päivämäärän jälkeen siirretään yksitellen.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-170">All transactions after this date will be migrated individually.</span></span>

## <a name="file-size-requirements"></a><span data-ttu-id="8fc2e-171">Tiedoston kokovaatimukset</span><span class="sxs-lookup"><span data-stu-id="8fc2e-171">File Size Requirements</span></span>

<span data-ttu-id="8fc2e-172">[!INCLUDE[prod_short](includes/prod_short.md)]iin ladattava tiedoston koko saa olla enintään 150 Mt.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-172">The largest file size you can upload to [!INCLUDE[prod_short](includes/prod_short.md)] is 150 MB.</span></span> <span data-ttu-id="8fc2e-173">Jos C5:stä vietävä tiedosto on tätä suurempi, harkitse tietojen siirtämistä useina tiedostoina.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-173">If the file you export from C5 is larger than that, consider migrating data in multiple files.</span></span> <span data-ttu-id="8fc2e-174">Vie C5:stä yhden tai kahden tyyppiset objektit, kuten asiakkaat ja toimittajat, yhteen tiedostoon, nimikkeet toiseen tiedostoon ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-174">For example, export one or two types of entities from C5, such as customers and vendors, to a file, and then export items to another file, and so on.</span></span> <span data-ttu-id="8fc2e-175">Voit tuoda tiedostot yksitellen [!INCLUDE[prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-175">You can import files individually in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="8fc2e-176">Tietojen siirtäminen</span><span class="sxs-lookup"><span data-stu-id="8fc2e-176">To migrate data</span></span>

<span data-ttu-id="8fc2e-177">Tietojen siirtäminen C5:stä ja tuominen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta edellyttää vain seuraavien vaiheiden suorittamista:</span><span class="sxs-lookup"><span data-stu-id="8fc2e-177">There are just a few steps to export data from C5, and import it in [!INCLUDE[prod_short](includes/prod_short.md)]:</span></span>  

1. <span data-ttu-id="8fc2e-178">Voit viedä tiedot C5:stä käyttämällä **Vie tietokanta** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-178">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="8fc2e-179">Pakkaa sitten viennin kansio.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-179">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="8fc2e-180">Valitse [!INCLUDE[prod_short](includes/prod_short.md)]:ssä ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tietojen siirto** ja valitse **Tietojen siirto**.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-180">In [!INCLUDE[prod_short](includes/prod_short.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="8fc2e-181">Suorita asetusten ohjatun määrityksen oppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-181">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="8fc2e-182">Varmista, että valitset tietolähteeksi **Tuo Microsoft Dynamcis C5 2012 -versiosta** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-182">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="8fc2e-183">Siirron tilan tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="8fc2e-183">Viewing the Status of the Migration</span></span>

<span data-ttu-id="8fc2e-184">Voit valvoa siirron onnistumista **Tietojen siirron yleiskuvaus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-184">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="8fc2e-185">Sivulla on tietoja esimerkiksi siirrettävien objektien määrästä, siirron tilasta, siirrettyjen nimikkeiden määrästä ja siirron onnistumisesta.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-185">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="8fc2e-186">Sivulla on tietoja myös virheiden määrästä. Voit tarkastella sivulla virheitä ja mahdollisesti siirtyä sivulta korjaamaan objektin ongelmat.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-186">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="8fc2e-187">Lisätietoja on tämän aiheen seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-187">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="8fc2e-188">Päivitä sivu, jotta siirron tulokset näkyvät sivulla.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-188">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="8fc2e-189">Miten voit välttää kaksinkertaisen kirjauksen</span><span class="sxs-lookup"><span data-stu-id="8fc2e-189">How to Avoid Double-Posting</span></span>

<span data-ttu-id="8fc2e-190">Voit välttää kaksinkertaisen kirjaamisen pääkirjanpitoon, käyttämällä seuraavia vastatilejä avoimille tapahtumille:</span><span class="sxs-lookup"><span data-stu-id="8fc2e-190">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="8fc2e-191">Toimittajia varten käytetään ostoreskontratiliä toimittajan kirjausryhmästä.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-191">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="8fc2e-192">Asiakkaita varten käytetään myyntireskontratiliä asiakkaan kirjausryhmästä.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-192">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="8fc2e-193">Nimikkeille luodaan yleinen kirjausasetus, missä oikaisutili on tili, joka on määritetty varastotiliksi varaston kirjausasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-193">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="8fc2e-194">Virheiden korjaaminen</span><span class="sxs-lookup"><span data-stu-id="8fc2e-194">Correcting Errors</span></span>

<span data-ttu-id="8fc2e-195">Jos siirrossa tapahtuu virheitä, **Tila**-kentän arvoksi tulee **Valmis (löytyi virheitä)**. **Virheiden määrä** -kenttä osoittaa virheiden määrän.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-195">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="8fc2e-196">Voit tarkastella virheluetteloa, kun avaat **Tietojen siirron virheet** -sivun valitsemalla seuraavat kohdat:</span><span class="sxs-lookup"><span data-stu-id="8fc2e-196">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="8fc2e-197">Objektin **Virheiden määrä** -kentässä oleva luku.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-197">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="8fc2e-198">Objekti ja sen jälkeen **Näytä virheet** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-198">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="8fc2e-199">Voit korjata virheen **Tietojen siirron virheet** -sivulla valitsemalla virhesanoman ja valitsemalla sitten **Muokkaa tietuetta**. Näyttöön avautuu objektin siirretyt tiedot.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-199">On the **Data Migration Errors** page, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="8fc2e-200">Jos korjattavia virheitä on paljon, voit muokata luettelossa olevia objekteja **Korjaa virheet joukkotoimintona** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-200">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="8fc2e-201">Jos virheen aiheuttaja on liittyvä merkintä, yksittäiset tietueet on avattava tästä huolimatta.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-201">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="8fc2e-202">Esimerkiksi toimittajaa ei siirretä, jos toimittajan jonkin yhteyshenkilön sähköpostiosoite on virheellisessä muodossa.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-202">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="8fc2e-203">Kun olet korjannut yhden tai useita virheitä, voit siirtää korjaamasi objektit valitsemalla **Siirrä**. Koko siirtoprosessia ei siis tarvitse käynnistää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-203">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="8fc2e-204">Jos olet korjannut useita virheitä, voit valita useita siirrettäviä rivejä valitsemalla **Valitse lisää** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-204">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="8fc2e-205">Jos virheitä ei tarvitse korjata, voit valita ne ja valita sitten **Ohita valinnat**.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-205">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="8fc2e-206">Jos osa nimikkeistä sisältyy tuoterakenteeseen, siirto on ehkä tehtävä useaan kertaan, jos alkuperäistä nimikettä ei luoda ennen siihen viittaavien varianttien luomista.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-206">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="8fc2e-207">Jos nimikevariantti luodaan ensin, alkuperäisen nimikkeen viite voi aiheuttaa virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-207">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="8fc2e-208">Tietojen tarkistaminen siirron jälkeen</span><span class="sxs-lookup"><span data-stu-id="8fc2e-208">Verifying Data After Migrating</span></span>

<span data-ttu-id="8fc2e-209">Yksi tapa tarkistaa, että tiedot on siirretty oikein, on katsoa seuraavia C5:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in sivuja.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-209">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

|<span data-ttu-id="8fc2e-210">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="8fc2e-210">Microsoft Dynamics C5 2012</span></span> | <span data-ttu-id="8fc2e-211">Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="8fc2e-211">Dynamics 365 Business Central</span></span>| <span data-ttu-id="8fc2e-212">Käytettävä eräajo</span><span class="sxs-lookup"><span data-stu-id="8fc2e-212">Batch Job to Use</span></span> |
|---------------------------|------------------------------|------------------|
|<span data-ttu-id="8fc2e-213">Asiakastapahtumat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-213">Customer Entries</span></span>| <span data-ttu-id="8fc2e-214">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-214">General Journals</span></span>| <span data-ttu-id="8fc2e-215">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="8fc2e-215">CUSTMIGR</span></span> |
|<span data-ttu-id="8fc2e-216">Toimittajatapahtumat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-216">Vendor Entries</span></span>| <span data-ttu-id="8fc2e-217">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-217">General Journals</span></span>| <span data-ttu-id="8fc2e-218">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="8fc2e-218">VENDMIGR</span></span>|
|<span data-ttu-id="8fc2e-219">Nimiketapahtumat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-219">Item Entries</span></span>| <span data-ttu-id="8fc2e-220">Nimikepäiväkirjat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-220">Item Journals</span></span>| <span data-ttu-id="8fc2e-221">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="8fc2e-221">ITEMMIGR</span></span> |
|<span data-ttu-id="8fc2e-222">KP-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-222">G/L Entries</span></span>| <span data-ttu-id="8fc2e-223">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="8fc2e-223">General Journals</span></span>| <span data-ttu-id="8fc2e-224">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="8fc2e-224">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="8fc2e-225">Tietojen siirron pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="8fc2e-225">Stopping Data Migration</span></span>

<span data-ttu-id="8fc2e-226">Voit pysäyttää tietojen siirron valitsemalla **Pysäytä kaikki siirrot**.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-226">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="8fc2e-227">Jos teet näin, kaikki odottavat siirrot pysäytetään.</span><span class="sxs-lookup"><span data-stu-id="8fc2e-227">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fc2e-228">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8fc2e-228">See Also</span></span>

<span data-ttu-id="8fc2e-229">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="8fc2e-229">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="8fc2e-230">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="8fc2e-230">Getting Started</span></span>](product-get-started.md)  
