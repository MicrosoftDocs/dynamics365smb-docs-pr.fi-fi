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
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: fi-fi
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="1cf61-103">C5-tietojen siirron laajennus Business Central -sovellusta varten</span><span class="sxs-lookup"><span data-stu-id="1cf61-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="1cf61-104">Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, nimikkeitä ja pääkirjanpidon tilejä Microsoft Dynamcis C5 2012 -versiosta [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="1cf61-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1cf61-105">Voit siirtää myös pääkirjanpidon tilien vanhat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="1cf61-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="1cf61-106">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yrityksessä ei saa olla tietoja.</span><span class="sxs-lookup"><span data-stu-id="1cf61-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="1cf61-107">Kun siirto on käynnistetty, asiakkaiden, toimittajien, nimikkeiden tai tilien luominen ei ole sallittua. Voit luoda niitä siirron valmistuttua.</span><span class="sxs-lookup"><span data-stu-id="1cf61-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="1cf61-108">Mitkä tiedot siirretään?</span><span class="sxs-lookup"><span data-stu-id="1cf61-108">What Data is Migrated?</span></span>
<span data-ttu-id="1cf61-109">Seuraavat kunkin objektit tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="1cf61-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="1cf61-110">**Asiakkaat**</span><span class="sxs-lookup"><span data-stu-id="1cf61-110">**Customers**</span></span>
* <span data-ttu-id="1cf61-111">Sijainti</span><span class="sxs-lookup"><span data-stu-id="1cf61-111">Location</span></span>
* <span data-ttu-id="1cf61-112">Maa</span><span class="sxs-lookup"><span data-stu-id="1cf61-112">Country</span></span>
* <span data-ttu-id="1cf61-113">Asiakkaan dimensiota (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="1cf61-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1cf61-114">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="1cf61-114">Shipment method</span></span>
* <span data-ttu-id="1cf61-115">Myyjä</span><span class="sxs-lookup"><span data-stu-id="1cf61-115">Sales Person</span></span>
* <span data-ttu-id="1cf61-116">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="1cf61-116">Payment terms</span></span>
* <span data-ttu-id="1cf61-117">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="1cf61-117">Payment method</span></span>
* <span data-ttu-id="1cf61-118">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="1cf61-118">Customer price group</span></span>
* <span data-ttu-id="1cf61-119">Asiakkaan laskun alennus</span><span class="sxs-lookup"><span data-stu-id="1cf61-119">Customer invoice discount</span></span>

<span data-ttu-id="1cf61-120">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="1cf61-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1cf61-121">Asiakkaan kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="1cf61-121">Customer posting setup</span></span>
* <span data-ttu-id="1cf61-122">Yleisen päiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="1cf61-122">General journal batch</span></span>
* <span data-ttu-id="1cf61-123">Avoimet tapahtumat (asiakastapahtumat)</span><span class="sxs-lookup"><span data-stu-id="1cf61-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="1cf61-124">**Toimittajat**</span><span class="sxs-lookup"><span data-stu-id="1cf61-124">**Vendors**</span></span>
* <span data-ttu-id="1cf61-125">Sijainti</span><span class="sxs-lookup"><span data-stu-id="1cf61-125">Location</span></span>
* <span data-ttu-id="1cf61-126">Maa</span><span class="sxs-lookup"><span data-stu-id="1cf61-126">Country</span></span>
* <span data-ttu-id="1cf61-127">Toimittajan dimensiot (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="1cf61-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1cf61-128">Laskualennus</span><span class="sxs-lookup"><span data-stu-id="1cf61-128">Invoice discount</span></span>
* <span data-ttu-id="1cf61-129">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="1cf61-129">Shipment method</span></span>
* <span data-ttu-id="1cf61-130">Ostaja</span><span class="sxs-lookup"><span data-stu-id="1cf61-130">Purchaser</span></span>
* <span data-ttu-id="1cf61-131">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="1cf61-131">Payment terms</span></span>
* <span data-ttu-id="1cf61-132">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="1cf61-132">Payment method</span></span>
* <span data-ttu-id="1cf61-133">Toimittajan laskun alennus</span><span class="sxs-lookup"><span data-stu-id="1cf61-133">Vendor invoice discount</span></span>

<span data-ttu-id="1cf61-134">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="1cf61-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1cf61-135">Toimittajan kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="1cf61-135">Vendor posting setup</span></span>
* <span data-ttu-id="1cf61-136">Yleisen päiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="1cf61-136">General journal batch</span></span>
* <span data-ttu-id="1cf61-137">Avoimet tapahtumat (toimittajatapahtumat)</span><span class="sxs-lookup"><span data-stu-id="1cf61-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="1cf61-138">**Nimikkeet**</span><span class="sxs-lookup"><span data-stu-id="1cf61-138">**Items**</span></span>
* <span data-ttu-id="1cf61-139">Sijainti</span><span class="sxs-lookup"><span data-stu-id="1cf61-139">Location</span></span>
* <span data-ttu-id="1cf61-140">Maa</span><span class="sxs-lookup"><span data-stu-id="1cf61-140">Country</span></span>
* <span data-ttu-id="1cf61-141">Nimikkeen dimensiot (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="1cf61-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1cf61-142">Myynnin rivialennukset</span><span class="sxs-lookup"><span data-stu-id="1cf61-142">Sales line discounts</span></span>
* <span data-ttu-id="1cf61-143">Asiakkaan alennusryhmät</span><span class="sxs-lookup"><span data-stu-id="1cf61-143">Customer discount groups</span></span>
* <span data-ttu-id="1cf61-144">Nimikealennusryhmät</span><span class="sxs-lookup"><span data-stu-id="1cf61-144">Item discount groups</span></span>
* <span data-ttu-id="1cf61-145">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="1cf61-145">Sales price</span></span>
* <span data-ttu-id="1cf61-146">Tavaranimike</span><span class="sxs-lookup"><span data-stu-id="1cf61-146">Tariff number</span></span>
* <span data-ttu-id="1cf61-147">Mittayksiköt</span><span class="sxs-lookup"><span data-stu-id="1cf61-147">Units of measure</span></span>
* <span data-ttu-id="1cf61-148">Nimikkeen seurantakoodi</span><span class="sxs-lookup"><span data-stu-id="1cf61-148">Item tracking code</span></span>
* <span data-ttu-id="1cf61-149">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="1cf61-149">Customer price group</span></span>

<span data-ttu-id="1cf61-150">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="1cf61-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1cf61-151">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="1cf61-151">Inventory posting setup</span></span>
* <span data-ttu-id="1cf61-152">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="1cf61-152">General posting setup</span></span>
* <span data-ttu-id="1cf61-153">Nimikepäiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="1cf61-153">Item journal batch</span></span>
* <span data-ttu-id="1cf61-154">Avoimet tapahtumat (nimiketapahtumat)</span><span class="sxs-lookup"><span data-stu-id="1cf61-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="1cf61-155">Jos avoimissa tapahtumissa käytetään ulkomaanvaluuttoja, myös kyseisten valuuttojen vaihtokurssit siirretään.</span><span class="sxs-lookup"><span data-stu-id="1cf61-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="1cf61-156">Muita vaihtokursseja ei siirretä.</span><span class="sxs-lookup"><span data-stu-id="1cf61-156">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="1cf61-157">**Tilikartta**</span><span class="sxs-lookup"><span data-stu-id="1cf61-157">**Chart of Accounts**</span></span>  
* <span data-ttu-id="1cf61-158">Vakiodimensiot: osasto, kustannupaikka, tarkoitus</span><span class="sxs-lookup"><span data-stu-id="1cf61-158">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="1cf61-159">Historialliset KP-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="1cf61-159">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="1cf61-160">Historialliset KP-tapahtumat, joita käsitellään hieman eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="1cf61-160">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="1cf61-161">Kun siirrät tietoja, määrität **Nykyinen jakso** -parametrin.</span><span class="sxs-lookup"><span data-stu-id="1cf61-161">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="1cf61-162">Tämä parametri määrittää, miten KP-tapahtumia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="1cf61-162">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="1cf61-163">Tämän päivämäärän jälkeen tapahtumat siirretään erikseen.</span><span class="sxs-lookup"><span data-stu-id="1cf61-163">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="1cf61-164">Tapahtumat ennen tätä päivämäärää koostetaan tilikohtaisesti ja siirretään yhtenä summana.</span><span class="sxs-lookup"><span data-stu-id="1cf61-164">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="1cf61-165">Esimerkiksi oletetaan, että tapahtumia on vuosina 2015, 2016, 2017 ja 2018, ja määrität 1. tammikuuta 2017 Nykyinen jakso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="1cf61-165">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="1cf61-166">Kunkin tilin tapahtumien 31.12.2016 tai sitä ennen summat kootaan yhteen yleisen päiväkirjan riviin kullekin KP-tilille.</span><span class="sxs-lookup"><span data-stu-id="1cf61-166">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="1cf61-167">Kaikki tapahtumat tämän päivämäärän jälkeen siirretään yksitellen.</span><span class="sxs-lookup"><span data-stu-id="1cf61-167">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="1cf61-168">Tietojen siirtäminen</span><span class="sxs-lookup"><span data-stu-id="1cf61-168">To migrate data</span></span>
<span data-ttu-id="1cf61-169">Tietojen siirtäminen C5:stä ja tuominen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmasta edellyttää vain seuraavien vaiheiden suorittamista:</span><span class="sxs-lookup"><span data-stu-id="1cf61-169">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="1cf61-170">Voit viedä tiedot C5:stä käyttämällä **Vie tietokanta** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="1cf61-170">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="1cf61-171">Pakkaa sitten viennin kansio.</span><span class="sxs-lookup"><span data-stu-id="1cf61-171">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="1cf61-172">Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake. Valitse **Tietojen siirto** ja valitse sitten **Tietojen siirto**.</span><span class="sxs-lookup"><span data-stu-id="1cf61-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="1cf61-173">Suorita asetusten ohjatun määrityksen oppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="1cf61-173">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="1cf61-174">Varmista, että valitset tietolähteeksi **Tuo Microsoft Dynamcis C5 2012 -versiosta** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="1cf61-174">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="1cf61-175">Yritykset lisäävät usein kenttiä, joiden avulla C5 voidaan mukauttaa toimialan vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="1cf61-175">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="1cf61-176"> ei siirrä mukautettujen kenttien tietoja.</span><span class="sxs-lookup"><span data-stu-id="1cf61-176"> does not migrate data from custom fields.</span></span> <span data-ttu-id="1cf61-177">Siirto epäonnistuu myös, jos mukautettuja kenttiä on enemmän kuin 10.</span><span class="sxs-lookup"><span data-stu-id="1cf61-177">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="1cf61-178">Siirron tilan tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="1cf61-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="1cf61-179">Voit valvoa siirron onnistumista **Tietojen siirron yleiskuvaus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1cf61-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="1cf61-180">Sivulla on tietoja esimerkiksi siirrettävien objektien määrästä, siirron tilasta, siirrettyjen nimikkeiden määrästä ja siirron onnistumisesta.</span><span class="sxs-lookup"><span data-stu-id="1cf61-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="1cf61-181">Sivulla on tietoja myös virheiden määrästä. Voit tarkastella sivulla virheitä ja mahdollisesti siirtyä sivulta korjaamaan objektin ongelmat.</span><span class="sxs-lookup"><span data-stu-id="1cf61-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="1cf61-182">Lisätietoja on tämän aiheen seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="1cf61-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="1cf61-183">Päivitä sivu, jotta siirron tulokset näkyvät sivulla.</span><span class="sxs-lookup"><span data-stu-id="1cf61-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="1cf61-184">Miten voit välttää kaksinkertaisen kirjauksen</span><span class="sxs-lookup"><span data-stu-id="1cf61-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="1cf61-185">Voit välttää kaksinkertaisen kirjaamisen pääkirjanpitoon, käyttämällä seuraavia vastatilejä avoimille tapahtumille:</span><span class="sxs-lookup"><span data-stu-id="1cf61-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  
  
* <span data-ttu-id="1cf61-186">Toimittajia varten käytetään ostoreskontratiliä toimittajan kirjausryhmästä.</span><span class="sxs-lookup"><span data-stu-id="1cf61-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="1cf61-187">Asiakkaita varten käytetään myyntireskontratiliä asiakkaan kirjausryhmästä.</span><span class="sxs-lookup"><span data-stu-id="1cf61-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="1cf61-188">Nimikkeille luodaan yleinen kirjausasetus, missä oikaisutili on tili, joka on määritetty varastotiliksi varaston kirjausasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="1cf61-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="1cf61-189">Virheiden korjaaminen</span><span class="sxs-lookup"><span data-stu-id="1cf61-189">Correcting Errors</span></span>
<span data-ttu-id="1cf61-190">Jos siirrossa tapahtuu virheitä, **Tila**-kentän arvoksi tulee **Valmis (löytyi virheitä)**. **Virheiden määrä** -kenttä osoittaa virheiden määrän.</span><span class="sxs-lookup"><span data-stu-id="1cf61-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="1cf61-191">Voit tarkastella virheluetteloa, kun avaat **Tietojen siirron virheet** -sivun valitsemalla seuraavat kohdat:</span><span class="sxs-lookup"><span data-stu-id="1cf61-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="1cf61-192">Objektin **Virheiden määrä** -kentässä oleva luku.</span><span class="sxs-lookup"><span data-stu-id="1cf61-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="1cf61-193">Objekti ja sen jälkeen **Näytä virheet** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1cf61-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="1cf61-194">Voit korjata virheen **Tietojen siirron virheet** -sivulla valitsemalla virhesanoman ja valitsemalla sitten **Muokkaa tietuetta**. Näyttöön avautuu sivu, joka sisältää objektin siirretyt tiedot.</span><span class="sxs-lookup"><span data-stu-id="1cf61-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="1cf61-195">Kun olet korjannut yhden tai useita virheitä, voit siirtää korjaamasi objektit valitsemalla **Siirrä**. Koko siirtoprosessia ei siis tarvitse käynnistää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="1cf61-195">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="1cf61-196">Jos olet korjannut useita virheitä, voit valita useita siirrettäviä rivejä valitsemalla **Valitse lisää** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="1cf61-196">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="1cf61-197">Jos virheitä ei tarvitse korjata, voit valita ne ja valita sitten **Ohita valinnat**.</span><span class="sxs-lookup"><span data-stu-id="1cf61-197">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="1cf61-198">Jos osa nimikkeistä sisältyy tuoterakenteeseen, siirto on ehkä tehtävä useaan kertaan, jos alkuperäistä nimikettä ei luoda ennen siihen viittaavien varianttien luomista.</span><span class="sxs-lookup"><span data-stu-id="1cf61-198">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="1cf61-199">Jos nimikevariantti luodaan ensin, alkuperäisen nimikkeen viite voi aiheuttaa virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="1cf61-199">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="1cf61-200">Tietojen tarkistaminen siirron jälkeen</span><span class="sxs-lookup"><span data-stu-id="1cf61-200">Verifying Data After Migrating</span></span>
<span data-ttu-id="1cf61-201">Yksi tapa tarkistaa, että tiedot on siirretty oikein, on katsoa seuraavia C5:n ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in sivuja.</span><span class="sxs-lookup"><span data-stu-id="1cf61-201">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="1cf61-202">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="1cf61-202">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="1cf61-203">Käytettävä eräajo</span><span class="sxs-lookup"><span data-stu-id="1cf61-203">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="1cf61-204">Asiakastapahtumat</span><span class="sxs-lookup"><span data-stu-id="1cf61-204">Customer Entries</span></span>| <span data-ttu-id="1cf61-205">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="1cf61-205">General Journals</span></span>| <span data-ttu-id="1cf61-206">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="1cf61-206">CUSTMIGR</span></span> |
|<span data-ttu-id="1cf61-207">Toimittajatapahtumat</span><span class="sxs-lookup"><span data-stu-id="1cf61-207">Vendor Entries</span></span>| <span data-ttu-id="1cf61-208">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="1cf61-208">General Journals</span></span>| <span data-ttu-id="1cf61-209">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="1cf61-209">VENDMIGR</span></span>|
|<span data-ttu-id="1cf61-210">Nimiketapahtumat</span><span class="sxs-lookup"><span data-stu-id="1cf61-210">Item Entries</span></span>| <span data-ttu-id="1cf61-211">Nimikepäiväkirjat</span><span class="sxs-lookup"><span data-stu-id="1cf61-211">Item Journals</span></span>| <span data-ttu-id="1cf61-212">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="1cf61-212">ITEMMIGR</span></span> |
|<span data-ttu-id="1cf61-213">KP-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="1cf61-213">G/L Entries</span></span>| <span data-ttu-id="1cf61-214">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="1cf61-214">General Journals</span></span>| <span data-ttu-id="1cf61-215">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="1cf61-215">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="1cf61-216">Tietojen siirron pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="1cf61-216">Stopping Data Migration</span></span>
<span data-ttu-id="1cf61-217">Voit pysäyttää tietojen siirron valitsemalla **Pysäytä kaikki siirrot**.</span><span class="sxs-lookup"><span data-stu-id="1cf61-217">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="1cf61-218">Jos teet näin, kaikki odottavat siirrot pysäytetään.</span><span class="sxs-lookup"><span data-stu-id="1cf61-218">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cf61-219">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1cf61-219">See Also</span></span>
<span data-ttu-id="1cf61-220">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1cf61-220">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="1cf61-221">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="1cf61-221">Getting Started</span></span>](product-get-started.md) 

