---
title: "C5-tietojen siirtolaajennuksen käyttäminen | Microsoft Docs"
description: "Voit käyttää tätä laajennusta asiakkaiden, toimittajien, nimikkeiden ja pääkirjanpidon tilien siirtämiseen Microsoft Dynamics C5 2012:sta Financialsiin."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d3b8d3d01ce75da59c1cce873077955776963ce9
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="0f996-103">Finance and Operations, Business editionin C5-tietojen siirtolaajennukset</span><span class="sxs-lookup"><span data-stu-id="0f996-103">The C5 Data Migration Extension for Finance and Operations, Business edition</span></span>
<span data-ttu-id="0f996-104">Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, nimikkeitä ja pääkirjanpidon tilejä Microsoft Dynamcis C5 2012 -versiosta [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="0f996-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0f996-105">Voit siirtää myös pääkirjanpidon tilien vanhat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="0f996-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="0f996-106">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yrityksessä ei saa olla tietoja.</span><span class="sxs-lookup"><span data-stu-id="0f996-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="0f996-107">Kun siirto on käynnistetty, asiakkaiden, toimittajien, nimikkeiden tai tilien luominen ei ole sallittua. Voit luoda niitä siirron valmistuttua.</span><span class="sxs-lookup"><span data-stu-id="0f996-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="0f996-108">Mitkä tiedot siirretään?</span><span class="sxs-lookup"><span data-stu-id="0f996-108">What Data is Migrated?</span></span>
<span data-ttu-id="0f996-109">Seuraavat kunkin objektit tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="0f996-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="0f996-110">**Asiakkaat**</span><span class="sxs-lookup"><span data-stu-id="0f996-110">**Customers**</span></span>
* <span data-ttu-id="0f996-111">Sijainti</span><span class="sxs-lookup"><span data-stu-id="0f996-111">Location</span></span>
* <span data-ttu-id="0f996-112">Maa</span><span class="sxs-lookup"><span data-stu-id="0f996-112">Country</span></span>
* <span data-ttu-id="0f996-113">Asiakkaan dimensiota (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="0f996-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="0f996-114">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="0f996-114">Shipment method</span></span>
* <span data-ttu-id="0f996-115">Myyjä</span><span class="sxs-lookup"><span data-stu-id="0f996-115">Sales Person</span></span>
* <span data-ttu-id="0f996-116">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="0f996-116">Payment terms</span></span>
* <span data-ttu-id="0f996-117">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="0f996-117">Payment method</span></span>
* <span data-ttu-id="0f996-118">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="0f996-118">Customer price group</span></span>
* <span data-ttu-id="0f996-119">Asiakkaan laskun alennus</span><span class="sxs-lookup"><span data-stu-id="0f996-119">Customer invoice discount</span></span>

<span data-ttu-id="0f996-120">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="0f996-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="0f996-121">Asiakkaan kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="0f996-121">Customer posting setup</span></span>
* <span data-ttu-id="0f996-122">Yleisen päiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="0f996-122">General journal batch</span></span>
* <span data-ttu-id="0f996-123">Avoimet tapahtumat (asiakastapahtumat)</span><span class="sxs-lookup"><span data-stu-id="0f996-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="0f996-124">**Toimittajat**</span><span class="sxs-lookup"><span data-stu-id="0f996-124">**Vendors**</span></span>
* <span data-ttu-id="0f996-125">Sijainti</span><span class="sxs-lookup"><span data-stu-id="0f996-125">Location</span></span>
* <span data-ttu-id="0f996-126">Maa</span><span class="sxs-lookup"><span data-stu-id="0f996-126">Country</span></span>
* <span data-ttu-id="0f996-127">Toimittajan dimensiot (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="0f996-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="0f996-128">Laskualennus</span><span class="sxs-lookup"><span data-stu-id="0f996-128">Invoice discount</span></span>
* <span data-ttu-id="0f996-129">Toimitusehto</span><span class="sxs-lookup"><span data-stu-id="0f996-129">Shipment method</span></span>
* <span data-ttu-id="0f996-130">Ostaja</span><span class="sxs-lookup"><span data-stu-id="0f996-130">Purchaser</span></span>
* <span data-ttu-id="0f996-131">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="0f996-131">Payment terms</span></span>
* <span data-ttu-id="0f996-132">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="0f996-132">Payment method</span></span>
* <span data-ttu-id="0f996-133">Toimittajan laskun alennus</span><span class="sxs-lookup"><span data-stu-id="0f996-133">Vendor invoice discount</span></span>

<span data-ttu-id="0f996-134">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="0f996-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="0f996-135">Toimittajan kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="0f996-135">Vendor posting setup</span></span>
* <span data-ttu-id="0f996-136">Yleisen päiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="0f996-136">General journal batch</span></span>
* <span data-ttu-id="0f996-137">Avoimet tapahtumat (toimittajatapahtumat)</span><span class="sxs-lookup"><span data-stu-id="0f996-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="0f996-138">**Nimikkeet**</span><span class="sxs-lookup"><span data-stu-id="0f996-138">**Items**</span></span>
* <span data-ttu-id="0f996-139">Sijainti</span><span class="sxs-lookup"><span data-stu-id="0f996-139">Location</span></span>
* <span data-ttu-id="0f996-140">Maa</span><span class="sxs-lookup"><span data-stu-id="0f996-140">Country</span></span>
* <span data-ttu-id="0f996-141">Nimikkeen dimensiot (osasto, tuotantosolu, tarkoitus)</span><span class="sxs-lookup"><span data-stu-id="0f996-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="0f996-142">Myynnin rivialennukset</span><span class="sxs-lookup"><span data-stu-id="0f996-142">Sales line discounts</span></span>
* <span data-ttu-id="0f996-143">Asiakkaan alennusryhmät</span><span class="sxs-lookup"><span data-stu-id="0f996-143">Customer discount groups</span></span>
* <span data-ttu-id="0f996-144">Nimikealennusryhmät</span><span class="sxs-lookup"><span data-stu-id="0f996-144">Item discount groups</span></span>
* <span data-ttu-id="0f996-145">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="0f996-145">Sales price</span></span>
* <span data-ttu-id="0f996-146">Tavaranimike</span><span class="sxs-lookup"><span data-stu-id="0f996-146">Tariff number</span></span>
* <span data-ttu-id="0f996-147">Mittayksiköt</span><span class="sxs-lookup"><span data-stu-id="0f996-147">Units of measure</span></span>
* <span data-ttu-id="0f996-148">Nimikkeen seurantakoodi</span><span class="sxs-lookup"><span data-stu-id="0f996-148">Item tracking code</span></span>
* <span data-ttu-id="0f996-149">Asiakkaan hintaryhmä</span><span class="sxs-lookup"><span data-stu-id="0f996-149">Customer price group</span></span>

<span data-ttu-id="0f996-150">Jos siirrät tilit, myös seuraavat tiedot siirretään:</span><span class="sxs-lookup"><span data-stu-id="0f996-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="0f996-151">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="0f996-151">Inventory posting setup</span></span>
* <span data-ttu-id="0f996-152">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="0f996-152">General posting setup</span></span>
* <span data-ttu-id="0f996-153">Nimikepäiväkirjan erä</span><span class="sxs-lookup"><span data-stu-id="0f996-153">Item journal batch</span></span>
* <span data-ttu-id="0f996-154">Avoimet tapahtumat (nimiketapahtumat)</span><span class="sxs-lookup"><span data-stu-id="0f996-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="0f996-155">Jos avoimissa tapahtumissa käytetään ulkomaanvaluuttoja, myös kyseisten valuuttojen vaihtokurssit siirretään.</span><span class="sxs-lookup"><span data-stu-id="0f996-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="0f996-156">Muita vaihtokursseja ei siirretä.</span><span class="sxs-lookup"><span data-stu-id="0f996-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="0f996-157">Tietojen siirtäminen</span><span class="sxs-lookup"><span data-stu-id="0f996-157">To migrate data</span></span>
<span data-ttu-id="0f996-158">Tietojen siirtäminen C5:stä ja tuominen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmasta edellyttää vain seuraavien vaiheiden suorittamista:</span><span class="sxs-lookup"><span data-stu-id="0f996-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="0f996-159">Voit viedä tiedot C5:stä käyttämällä **Vie tietokanta** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="0f996-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="0f996-160">Pakkaa sitten viennin kansio.</span><span class="sxs-lookup"><span data-stu-id="0f996-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="0f996-161">Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake. Valitse **Tietojen siirto** ja valitse sitten **Tietojen siirto**.</span><span class="sxs-lookup"><span data-stu-id="0f996-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="0f996-162">Suorita asetusten ohjatun määrityksen oppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="0f996-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="0f996-163">Varmista, että valitset tietolähteeksi **Tuo Microsoft Dynamcis C5 2012 -versiosta** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="0f996-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="0f996-164">Yritykset lisäävät usein kenttiä, joiden avulla C5 voidaan mukauttaa toimialan vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="0f996-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0f996-165"> ei siirrä mukautettujen kenttien tietoja.</span><span class="sxs-lookup"><span data-stu-id="0f996-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="0f996-166">Siirto epäonnistuu myös, jos mukautettuja kenttiä on enemmän kuin 10.</span><span class="sxs-lookup"><span data-stu-id="0f996-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="0f996-167">Siirron tilan tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="0f996-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="0f996-168">Voit valvoa siirron onnistumista **Tietojen siirron yleiskuvaus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0f996-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="0f996-169">Sivulla on tietoja esimerkiksi siirrettävien objektien määrästä, siirron tilasta, siirrettyjen nimikkeiden määrästä ja siirron onnistumisesta.</span><span class="sxs-lookup"><span data-stu-id="0f996-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="0f996-170">Sivulla on tietoja myös virheiden määrästä. Voit tarkastella sivulla virheitä ja mahdollisesti siirtyä sivulta korjaamaan objektin ongelmat.</span><span class="sxs-lookup"><span data-stu-id="0f996-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="0f996-171">Lisätietoja on tämän aiheen seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="0f996-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="0f996-172">Päivitä sivu, jotta siirron tulokset näkyvät sivulla.</span><span class="sxs-lookup"><span data-stu-id="0f996-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="0f996-173">Virheiden korjaaminen</span><span class="sxs-lookup"><span data-stu-id="0f996-173">Correcting Errors</span></span>
<span data-ttu-id="0f996-174">Jos siirrossa tapahtuu virheitä, **Tila**-kentän arvoksi tulee **Valmis (löytyi virheitä)**. **Virheiden määrä** -kenttä osoittaa virheiden määrän.</span><span class="sxs-lookup"><span data-stu-id="0f996-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="0f996-175">Voit tarkastella virheluetteloa, kun avaat **Tietojen siirron virheet** -sivun valitsemalla seuraavat kohdat:</span><span class="sxs-lookup"><span data-stu-id="0f996-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="0f996-176">Objektin **Virheiden määrä** -kentässä oleva luku.</span><span class="sxs-lookup"><span data-stu-id="0f996-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="0f996-177">Objekti ja sen jälkeen **Näytä virheet** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="0f996-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="0f996-178">Voit korjata virheen **Tietojen siirron virheet** -sivulla valitsemalla virhesanoman ja valitsemalla sitten **Muokkaa tietuetta**. Näyttöön avautuu sivu, joka sisältää objektin siirretyt tiedot.</span><span class="sxs-lookup"><span data-stu-id="0f996-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="0f996-179">Kun olet korjannut yhden tai useita virheitä, voit siirtää korjaamasi objektit valitsemalla **Siirrä**. Koko siirtoprosessia ei siis tarvitse käynnistää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="0f996-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="0f996-180">Jos olet korjannut useita virheitä, voit valita useita siirrettäviä rivejä valitsemalla **Valitse lisää** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="0f996-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="0f996-181">Jos virheitä ei tarvitse korjata, voit valita ne ja valita sitten **Ohita valinnat**.</span><span class="sxs-lookup"><span data-stu-id="0f996-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="0f996-182">Jos osa nimikkeistä sisältyy tuoterakenteeseen, siirto on ehkä tehtävä useaan kertaan, jos alkuperäistä nimikettä ei luoda ennen siihen viittaavien varianttien luomista.</span><span class="sxs-lookup"><span data-stu-id="0f996-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="0f996-183">Jos nimikevariantti luodaan ensin, alkuperäisen nimikkeen viite voi aiheuttaa virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="0f996-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="0f996-184">Tietojen tarkistaminen siirron jälkeen</span><span class="sxs-lookup"><span data-stu-id="0f996-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="0f996-185">Yksi tapa tarkistaa, että tiedot on siirretty oikein, on katsoa seuraavia C5:n ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in sivuja.</span><span class="sxs-lookup"><span data-stu-id="0f996-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="0f996-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="0f996-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="0f996-187">Asiakastapahtumat</span><span class="sxs-lookup"><span data-stu-id="0f996-187">Customer Entries</span></span>| <span data-ttu-id="0f996-188">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="0f996-188">General Journals</span></span>|
|<span data-ttu-id="0f996-189">Toimittajatapahtumat</span><span class="sxs-lookup"><span data-stu-id="0f996-189">Vendor Entries</span></span>| <span data-ttu-id="0f996-190">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="0f996-190">General Journals</span></span>|
|<span data-ttu-id="0f996-191">Nimiketapahtumat</span><span class="sxs-lookup"><span data-stu-id="0f996-191">Item Entries</span></span>| <span data-ttu-id="0f996-192">Nimikepäiväkirjat</span><span class="sxs-lookup"><span data-stu-id="0f996-192">Item Journals</span></span>|

<span data-ttu-id="0f996-193">Siirrettyjen tietojen erän nimeksi annetaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="0f996-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="0f996-194">Tietojen siirron pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="0f996-194">Stopping Data Migration</span></span>
<span data-ttu-id="0f996-195">Voit pysäyttää tietojen siirron valitsemalla **Pysäytä kaikki siirrot**.</span><span class="sxs-lookup"><span data-stu-id="0f996-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="0f996-196">Jos teet näin, kaikki odottavat siirrot pysäytetään.</span><span class="sxs-lookup"><span data-stu-id="0f996-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f996-197">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0f996-197">See Also</span></span>
<span data-ttu-id="0f996-198">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="0f996-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="0f996-199">[Tervetuloa [!INCLUDE[d365fin](includes/d365fin_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="0f996-199">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

