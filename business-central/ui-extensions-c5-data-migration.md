---
title: "C5-tietojen siirtolaajennuksen käyttäminen | Microsoft Docs"
description: "Voit käyttää tätä laajennusta asiakkaiden, toimittajien, nimikkeiden ja pääkirjanpidon tilien siirtämiseen Microsoft Dynamics C5 2012:sta Business Centraliin."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5c89d841cdf0e92af4a3dc497cb9c807798e3924
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="74116-103">Tietojen siirron C5-laajennus</span><span class="sxs-lookup"><span data-stu-id="74116-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="74116-104">Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, nimikkeitä ja pääkirjanpidon tilejä Microsoft Dynamcis C5 2012 -versiosta [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="74116-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="74116-105">Voit siirtää myös pääkirjanpidon tilien vanhat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="74116-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="74116-106">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yrityksessä ei saa olla tietoja.</span><span class="sxs-lookup"><span data-stu-id="74116-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="74116-107">Kun siirto on käynnistetty, asiakkaiden, toimittajien, nimikkeiden tai tilien luominen ei ole sallittua. Voit luoda niitä siirron valmistuttua.</span><span class="sxs-lookup"><span data-stu-id="74116-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="74116-108">Mitkä tiedot siirretään?</span><span class="sxs-lookup"><span data-stu-id="74116-108">What Data is Migrated?</span></span>
<span data-ttu-id="74116-109">Seuraavat kunkin objektit tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="74116-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="74116-110">**Asiakkaat**</span><span class="sxs-lookup"><span data-stu-id="74116-110">**Customers**</span></span>
* <span data-ttu-id="74116-111">Kontaktit</span><span class="sxs-lookup"><span data-stu-id="74116-111">Contacts</span></span>  
* <span data-ttu-id="74116-112">Sijainti</span><span class="sxs-lookup"><span data-stu-id="74116-112">Location</span></span>
* <span data-ttu-id="74116-113">Maa</span><span class="sxs-lookup"><span data-stu-id="74116-113">Country</span></span>
* <span data-ttu-id="74116-114">Asiakkaan dimensiota (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="74116-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="74116-115">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="74116-115">Shipment method</span></span>
* <span data-ttu-id="74116-116">Myyjä</span><span class="sxs-lookup"><span data-stu-id="74116-116">Sales Person</span></span>
* <span data-ttu-id="74116-117">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="74116-117">Payment terms</span></span>
* <span data-ttu-id="74116-118">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="74116-118">Payment method</span></span>
* <span data-ttu-id="74116-119">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="74116-119">Customer price group</span></span>
* <span data-ttu-id="74116-120">Asiakkaan laskun alennus</span><span class="sxs-lookup"><span data-stu-id="74116-120">Customer invoice discount</span></span>

<span data-ttu-id="74116-121">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="74116-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="74116-122">Asiakkaan kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="74116-122">Customer posting setup</span></span>
* <span data-ttu-id="74116-123">Yleisen päiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="74116-123">General journal batch</span></span>
* <span data-ttu-id="74116-124">Avoimet tapahtumat (asiakastapahtumat)</span><span class="sxs-lookup"><span data-stu-id="74116-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="74116-125">**Toimittajat**</span><span class="sxs-lookup"><span data-stu-id="74116-125">**Vendors**</span></span>
* <span data-ttu-id="74116-126">Kontaktit</span><span class="sxs-lookup"><span data-stu-id="74116-126">Contacts</span></span>
* <span data-ttu-id="74116-127">Sijainti</span><span class="sxs-lookup"><span data-stu-id="74116-127">Location</span></span>
* <span data-ttu-id="74116-128">Maa</span><span class="sxs-lookup"><span data-stu-id="74116-128">Country</span></span>
* <span data-ttu-id="74116-129">Toimittajan dimensiot (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="74116-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="74116-130">Laskualennus</span><span class="sxs-lookup"><span data-stu-id="74116-130">Invoice discount</span></span>
* <span data-ttu-id="74116-131">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="74116-131">Shipment method</span></span>
* <span data-ttu-id="74116-132">Ostaja</span><span class="sxs-lookup"><span data-stu-id="74116-132">Purchaser</span></span>
* <span data-ttu-id="74116-133">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="74116-133">Payment terms</span></span>
* <span data-ttu-id="74116-134">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="74116-134">Payment method</span></span>
* <span data-ttu-id="74116-135">Toimittajan laskun alennus</span><span class="sxs-lookup"><span data-stu-id="74116-135">Vendor invoice discount</span></span>

<span data-ttu-id="74116-136">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="74116-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="74116-137">Toimittajan kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="74116-137">Vendor posting setup</span></span>
* <span data-ttu-id="74116-138">Yleisen päiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="74116-138">General journal batch</span></span>
* <span data-ttu-id="74116-139">Avoimet tapahtumat (toimittajatapahtumat)</span><span class="sxs-lookup"><span data-stu-id="74116-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="74116-140">**Nimikkeet**</span><span class="sxs-lookup"><span data-stu-id="74116-140">**Items**</span></span>
* <span data-ttu-id="74116-141">Sijainti</span><span class="sxs-lookup"><span data-stu-id="74116-141">Location</span></span>
* <span data-ttu-id="74116-142">Maa</span><span class="sxs-lookup"><span data-stu-id="74116-142">Country</span></span>
* <span data-ttu-id="74116-143">Nimikkeen dimensiot (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="74116-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="74116-144">Myynnin rivialennukset</span><span class="sxs-lookup"><span data-stu-id="74116-144">Sales line discounts</span></span>
* <span data-ttu-id="74116-145">Asiakkaan alennusryhmät</span><span class="sxs-lookup"><span data-stu-id="74116-145">Customer discount groups</span></span>
* <span data-ttu-id="74116-146">Nimikealennusryhmät</span><span class="sxs-lookup"><span data-stu-id="74116-146">Item discount groups</span></span>
* <span data-ttu-id="74116-147">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="74116-147">Sales price</span></span>
* <span data-ttu-id="74116-148">Tavaranimike</span><span class="sxs-lookup"><span data-stu-id="74116-148">Tariff number</span></span>
* <span data-ttu-id="74116-149">Mittayksiköt</span><span class="sxs-lookup"><span data-stu-id="74116-149">Units of measure</span></span>
* <span data-ttu-id="74116-150">Nimikkeen seurantakoodi</span><span class="sxs-lookup"><span data-stu-id="74116-150">Item tracking code</span></span>
* <span data-ttu-id="74116-151">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="74116-151">Customer price group</span></span>
* <span data-ttu-id="74116-152">Kokoonpanon tuoterakenteet</span><span class="sxs-lookup"><span data-stu-id="74116-152">Assembly BOMs</span></span>

<span data-ttu-id="74116-153">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="74116-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="74116-154">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="74116-154">Inventory posting setup</span></span>
* <span data-ttu-id="74116-155">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="74116-155">General posting setup</span></span>
* <span data-ttu-id="74116-156">Nimikepäiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="74116-156">Item journal batch</span></span>
* <span data-ttu-id="74116-157">Avoimet tapahtumat (nimiketapahtumat)</span><span class="sxs-lookup"><span data-stu-id="74116-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="74116-158">Jos avoimissa tapahtumissa käytetään ulkomaanvaluuttoja, myös kyseisten valuuttojen vaihtokurssit siirretään.</span><span class="sxs-lookup"><span data-stu-id="74116-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="74116-159">Muita vaihtokursseja ei siirretä.</span><span class="sxs-lookup"><span data-stu-id="74116-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="74116-160">**Tilikartta**</span><span class="sxs-lookup"><span data-stu-id="74116-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="74116-161">Vakiodimensiot: osasto, kustannupaikka, tarkoitus</span><span class="sxs-lookup"><span data-stu-id="74116-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="74116-162">Historialliset KP-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="74116-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="74116-163">Historialliset KP-tapahtumat, joita käsitellään hieman eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="74116-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="74116-164">Kun siirrät tietoja, määrität **Nykyinen jakso** -parametrin.</span><span class="sxs-lookup"><span data-stu-id="74116-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="74116-165">Tämä parametri määrittää, miten KP-tapahtumia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="74116-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="74116-166">Tämän päivämäärän jälkeen tapahtumat siirretään erikseen.</span><span class="sxs-lookup"><span data-stu-id="74116-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="74116-167">Tapahtumat ennen tätä päivämäärää koostetaan tilikohtaisesti ja siirretään yhtenä summana.</span><span class="sxs-lookup"><span data-stu-id="74116-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="74116-168">Esimerkiksi oletetaan, että tapahtumia on vuosina 2015, 2016, 2017 ja 2018, ja määrität 1. tammikuuta 2017 Nykyinen jakso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="74116-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="74116-169">Kunkin tilin tapahtumien 31.12.2016 tai sitä ennen summat kootaan yhteen yleisen päiväkirjan riviin kullekin KP-tilille.</span><span class="sxs-lookup"><span data-stu-id="74116-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="74116-170">Kaikki tapahtumat tämän päivämäärän jälkeen siirretään yksitellen.</span><span class="sxs-lookup"><span data-stu-id="74116-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="74116-171">Tietojen siirtäminen</span><span class="sxs-lookup"><span data-stu-id="74116-171">To migrate data</span></span>
<span data-ttu-id="74116-172">Tietojen siirtäminen C5:stä ja tuominen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmasta edellyttää vain seuraavien vaiheiden suorittamista:</span><span class="sxs-lookup"><span data-stu-id="74116-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="74116-173">Voit viedä tiedot C5:stä käyttämällä **Vie tietokanta** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="74116-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="74116-174">Pakkaa sitten viennin kansio.</span><span class="sxs-lookup"><span data-stu-id="74116-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="74116-175">Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tietojen siirto** ja valitse **Tietojen siirto**.</span><span class="sxs-lookup"><span data-stu-id="74116-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="74116-176">Suorita asetusten ohjatun määrityksen oppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="74116-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="74116-177">Varmista, että valitset tietolähteeksi **Tuo Microsoft Dynamcis C5 2012 -versiosta** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="74116-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="74116-178">Siirron tilan tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="74116-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="74116-179">Voit valvoa siirron onnistumista **Tietojen siirron yleiskuvaus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="74116-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="74116-180">Sivulla on tietoja esimerkiksi siirrettävien objektien määrästä, siirron tilasta, siirrettyjen nimikkeiden määrästä ja siirron onnistumisesta.</span><span class="sxs-lookup"><span data-stu-id="74116-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="74116-181">Sivulla on tietoja myös virheiden määrästä. Voit tarkastella sivulla virheitä ja mahdollisesti siirtyä sivulta korjaamaan objektin ongelmat.</span><span class="sxs-lookup"><span data-stu-id="74116-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="74116-182">Lisätietoja on tämän aiheen seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="74116-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="74116-183">Päivitä sivu, jotta siirron tulokset näkyvät sivulla.</span><span class="sxs-lookup"><span data-stu-id="74116-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="74116-184">Miten voit välttää kaksinkertaisen kirjauksen</span><span class="sxs-lookup"><span data-stu-id="74116-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="74116-185">Voit välttää kaksinkertaisen kirjaamisen pääkirjanpitoon, käyttämällä seuraavia vastatilejä avoimille tapahtumille:</span><span class="sxs-lookup"><span data-stu-id="74116-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="74116-186">Toimittajia varten käytetään ostoreskontratiliä toimittajan kirjausryhmästä.</span><span class="sxs-lookup"><span data-stu-id="74116-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="74116-187">Asiakkaita varten käytetään myyntireskontratiliä asiakkaan kirjausryhmästä.</span><span class="sxs-lookup"><span data-stu-id="74116-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="74116-188">Nimikkeille luodaan yleinen kirjausasetus, missä oikaisutili on tili, joka on määritetty varastotiliksi varaston kirjausasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="74116-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="74116-189">Virheiden korjaaminen</span><span class="sxs-lookup"><span data-stu-id="74116-189">Correcting Errors</span></span>
<span data-ttu-id="74116-190">Jos siirrossa tapahtuu virheitä, **Tila**-kentän arvoksi tulee **Valmis (löytyi virheitä)**. **Virheiden määrä** -kenttä osoittaa virheiden määrän.</span><span class="sxs-lookup"><span data-stu-id="74116-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="74116-191">Voit tarkastella virheluetteloa, kun avaat **Tietojen siirron virheet** -sivun valitsemalla seuraavat kohdat:</span><span class="sxs-lookup"><span data-stu-id="74116-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="74116-192">Objektin **Virheiden määrä** -kentässä oleva luku.</span><span class="sxs-lookup"><span data-stu-id="74116-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="74116-193">Objekti ja sen jälkeen **Näytä virheet** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="74116-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="74116-194">Voit korjata virheen **Tietojen siirron virheet** -sivulla valitsemalla virhesanoman ja valitsemalla sitten **Muokkaa tietuetta**. Näyttöön avautuu objektin siirretyt tiedot.</span><span class="sxs-lookup"><span data-stu-id="74116-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="74116-195">Jos korjattavia virheitä on paljon, voit muokata luettelossa olevia objekteja **Korjaa virheet joukkotoimintona** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="74116-195">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="74116-196">Jos virheen aiheuttaja on liittyvä merkintä, yksittäiset tietueet on avattava tästä huolimatta.</span><span class="sxs-lookup"><span data-stu-id="74116-196">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="74116-197">Esimerkiksi toimittajaa ei siirretä, jos toimittajan jonkin yhteyshenkilön sähköpostiosoite on virheellisessä muodossa.</span><span class="sxs-lookup"><span data-stu-id="74116-197">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="74116-198">Kun olet korjannut yhden tai useita virheitä, voit siirtää korjaamasi objektit valitsemalla **Siirrä**. Koko siirtoprosessia ei siis tarvitse käynnistää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="74116-198">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="74116-199">Jos olet korjannut useita virheitä, voit valita useita siirrettäviä rivejä valitsemalla **Valitse lisää** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="74116-199">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="74116-200">Jos virheitä ei tarvitse korjata, voit valita ne ja valita sitten **Ohita valinnat**.</span><span class="sxs-lookup"><span data-stu-id="74116-200">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="74116-201">Jos osa nimikkeistä sisältyy tuoterakenteeseen, siirto on ehkä tehtävä useaan kertaan, jos alkuperäistä nimikettä ei luoda ennen siihen viittaavien varianttien luomista.</span><span class="sxs-lookup"><span data-stu-id="74116-201">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="74116-202">Jos nimikevariantti luodaan ensin, alkuperäisen nimikkeen viite voi aiheuttaa virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="74116-202">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="74116-203">Tietojen tarkistaminen siirron jälkeen</span><span class="sxs-lookup"><span data-stu-id="74116-203">Verifying Data After Migrating</span></span>
<span data-ttu-id="74116-204">Yksi tapa tarkistaa, että tiedot on siirretty oikein, on katsoa seuraavia C5:n ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in sivuja.</span><span class="sxs-lookup"><span data-stu-id="74116-204">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="74116-205">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="74116-205">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="74116-206">Käytettävä eräajo</span><span class="sxs-lookup"><span data-stu-id="74116-206">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="74116-207">Asiakastapahtumat</span><span class="sxs-lookup"><span data-stu-id="74116-207">Customer Entries</span></span>| <span data-ttu-id="74116-208">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="74116-208">General Journals</span></span>| <span data-ttu-id="74116-209">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="74116-209">CUSTMIGR</span></span> |
|<span data-ttu-id="74116-210">Toimittajatapahtumat</span><span class="sxs-lookup"><span data-stu-id="74116-210">Vendor Entries</span></span>| <span data-ttu-id="74116-211">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="74116-211">General Journals</span></span>| <span data-ttu-id="74116-212">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="74116-212">VENDMIGR</span></span>|
|<span data-ttu-id="74116-213">Nimiketapahtumat</span><span class="sxs-lookup"><span data-stu-id="74116-213">Item Entries</span></span>| <span data-ttu-id="74116-214">Nimikepäiväkirjat</span><span class="sxs-lookup"><span data-stu-id="74116-214">Item Journals</span></span>| <span data-ttu-id="74116-215">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="74116-215">ITEMMIGR</span></span> |
|<span data-ttu-id="74116-216">KP-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="74116-216">G/L Entries</span></span>| <span data-ttu-id="74116-217">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="74116-217">General Journals</span></span>| <span data-ttu-id="74116-218">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="74116-218">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="74116-219">Tietojen siirron pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="74116-219">Stopping Data Migration</span></span>
<span data-ttu-id="74116-220">Voit pysäyttää tietojen siirron valitsemalla **Pysäytä kaikki siirrot**.</span><span class="sxs-lookup"><span data-stu-id="74116-220">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="74116-221">Jos teet näin, kaikki odottavat siirrot pysäytetään.</span><span class="sxs-lookup"><span data-stu-id="74116-221">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="74116-222">Katso myös</span><span class="sxs-lookup"><span data-stu-id="74116-222">See Also</span></span>
<span data-ttu-id="74116-223">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="74116-223">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="74116-224">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="74116-224">Getting Started</span></span>](product-get-started.md)

