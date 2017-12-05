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
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a><span data-ttu-id="55f8b-103">Dynamics 365 for Finance and Operations, Business editionin C5-tietojen siirtolaajennukset</span><span class="sxs-lookup"><span data-stu-id="55f8b-103">The C5 Data Migration Extension for Dynamics 365 for Finance and Operations, Business Edition</span></span>
<span data-ttu-id="55f8b-104">Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, nimikkeitä ja pääkirjanpidon tilejä Microsoft Dynamcis C5 2012 -versiosta [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="55f8b-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
> [!Note] 
> <span data-ttu-id="55f8b-105">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yrityksessä ei saa olla tietoja.</span><span class="sxs-lookup"><span data-stu-id="55f8b-105">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="55f8b-106">Kun siirto on käynnistetty, asiakkaiden, toimittajien, nimikkeiden tai tilien luominen ei ole sallittua. Voit luoda niitä siirron valmistuttua.</span><span class="sxs-lookup"><span data-stu-id="55f8b-106">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="55f8b-107">Tietojen siirtäminen</span><span class="sxs-lookup"><span data-stu-id="55f8b-107">To migrate data</span></span>
<span data-ttu-id="55f8b-108">Tietojen siirtäminen C5:stä ja tuominen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmasta edellyttää vain seuraavien vaiheiden suorittamista:</span><span class="sxs-lookup"><span data-stu-id="55f8b-108">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  
  
1. <span data-ttu-id="55f8b-109">Voit viedä tiedot C5:stä käyttämällä **Vie tietokanta** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="55f8b-109">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="55f8b-110">Pakkaa sitten viennin kansio.</span><span class="sxs-lookup"><span data-stu-id="55f8b-110">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="55f8b-111">Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake. Valitse **Tietojen siirto** ja valitse sitten **Tietojen siirto**.</span><span class="sxs-lookup"><span data-stu-id="55f8b-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="55f8b-112">Suorita asetusten ohjatun määrityksen oppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="55f8b-112">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="55f8b-113">Varmista, että valitset tietolähteeksi **Tuo Microsoft Dynamcis C5 2012 -versiosta** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="55f8b-113">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note] 
> <span data-ttu-id="55f8b-114">Yritykset lisäävät usein kenttiä, joiden avulla C5 voidaan mukauttaa toimialan vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="55f8b-114">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="55f8b-115"> ei siirrä mukautettujen kenttien tietoja.</span><span class="sxs-lookup"><span data-stu-id="55f8b-115"> does not migrate data from custom fields.</span></span> <span data-ttu-id="55f8b-116">Siirto epäonnistuu myös, jos mukautettuja kenttiä on enemmän kuin 10.</span><span class="sxs-lookup"><span data-stu-id="55f8b-116">Also, migration will fail if you have more than 10 custom fields.</span></span> 

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="55f8b-117">Siirron tilan tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="55f8b-117">Viewing the Status of the Migration</span></span>
<span data-ttu-id="55f8b-118">Voit valvoa siirron onnistumista **Tietojen siirron yleiskuvaus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="55f8b-118">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="55f8b-119">Sivulla on tietoja esimerkiksi siirrettävien objektien määrästä, siirron tilasta, siirrettyjen nimikkeiden määrästä ja siirron onnistumisesta.</span><span class="sxs-lookup"><span data-stu-id="55f8b-119">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="55f8b-120">Sivulla on tietoja myös virheiden määrästä. Voit tarkastella sivulla virheitä ja mahdollisesti siirtyä sivulta korjaamaan objektin ongelmat.</span><span class="sxs-lookup"><span data-stu-id="55f8b-120">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="55f8b-121">Lisätietoja on tämän aiheen seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="55f8b-121">For more information, see the next section in this topic.</span></span> 

> [!Note] 
> <span data-ttu-id="55f8b-122">Päivitä sivu, jotta siirron tulokset näkyvät sivulla.</span><span class="sxs-lookup"><span data-stu-id="55f8b-122">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="55f8b-123">Virheiden korjaaminen</span><span class="sxs-lookup"><span data-stu-id="55f8b-123">Correcting Errors</span></span>
<span data-ttu-id="55f8b-124">Jos siirrossa tapahtuu virheitä, **Tila**-kentän arvoksi tulee **Valmis (löytyi virheitä)**. **Virheiden määrä** -kenttä osoittaa virheiden määrän.</span><span class="sxs-lookup"><span data-stu-id="55f8b-124">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="55f8b-125">Voit tarkastella virheluetteloa, kun avaat **Tietojen siirron virheet** -sivun valitsemalla seuraavat kohdat:</span><span class="sxs-lookup"><span data-stu-id="55f8b-125">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>

* <span data-ttu-id="55f8b-126">Objektin **Virheiden määrä** -kentässä oleva luku.</span><span class="sxs-lookup"><span data-stu-id="55f8b-126">The number in the **Error Count** field for the entity.</span></span> 
* <span data-ttu-id="55f8b-127">Objekti ja sen jälkeen **Näytä virheet** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="55f8b-127">The entity, and then the **Show Errors** action.</span></span> 

<span data-ttu-id="55f8b-128">Voit korjata virheen **Tietojen siirron virheet** -sivulla valitsemalla virhesanoman ja valitsemalla sitten **Muokkaa tietuetta**. Näyttöön avautuu sivu, joka sisältää objektin siirretyt tiedot.</span><span class="sxs-lookup"><span data-stu-id="55f8b-128">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="55f8b-129">Kun olet korjannut yhden tai useita virheitä, voit siirtää korjaamasi objektit valitsemalla **Siirrä**. Koko siirtoprosessia ei siis tarvitse käynnistää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="55f8b-129">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="55f8b-130">Jos olet korjannut useita virheitä, voit valita useita siirrettäviä rivejä valitsemalla **Valitse lisää** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="55f8b-130">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="55f8b-131">Jos virheitä ei tarvitse korjata, voit valita ne ja valita sitten **Ohita valinnat**.</span><span class="sxs-lookup"><span data-stu-id="55f8b-131">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="55f8b-132">Jos osa nimikkeistä sisältyy tuoterakenteeseen, siirto on ehkä tehtävä useaan kertaan, jos alkuperäistä nimikettä ei luoda ennen siihen viittaavien varianttien luomista.</span><span class="sxs-lookup"><span data-stu-id="55f8b-132">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="55f8b-133">Jos nimikevariantti luodaan ensin, alkuperäisen nimikkeen viite voi aiheuttaa virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="55f8b-133">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="55f8b-134">Tietojen tarkistaminen siirron jälkeen</span><span class="sxs-lookup"><span data-stu-id="55f8b-134">Verifying Data After Migrating</span></span> 
<span data-ttu-id="55f8b-135">Jos haluat tarkistaa, että tiedot on siirretty oikein, voit katsoa seuraavia C5:n ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman sivuja.</span><span class="sxs-lookup"><span data-stu-id="55f8b-135">If you want to verify that your data migrated correctly, you can look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="55f8b-136">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="55f8b-136">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="55f8b-137">Asiakastapahtumat</span><span class="sxs-lookup"><span data-stu-id="55f8b-137">Customer Entries</span></span>| <span data-ttu-id="55f8b-138">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="55f8b-138">General Journals</span></span>|
|<span data-ttu-id="55f8b-139">Toimittajatapahtumat</span><span class="sxs-lookup"><span data-stu-id="55f8b-139">Vendor Entries</span></span>| <span data-ttu-id="55f8b-140">Yleiset päiväkirjat</span><span class="sxs-lookup"><span data-stu-id="55f8b-140">General Journals</span></span>|
|<span data-ttu-id="55f8b-141">Nimiketapahtumat</span><span class="sxs-lookup"><span data-stu-id="55f8b-141">Item Entries</span></span>| <span data-ttu-id="55f8b-142">Nimikepäiväkirjat</span><span class="sxs-lookup"><span data-stu-id="55f8b-142">Item Journals</span></span>|

<span data-ttu-id="55f8b-143">Siirrettyjen tietojen erän nimeksi annetaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="55f8b-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span> 

## <a name="stopping-data-migration"></a><span data-ttu-id="55f8b-144">Tietojen siirron pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="55f8b-144">Stopping Data Migration</span></span>
<span data-ttu-id="55f8b-145">Voit pysäyttää tietojen siirron valitsemalla **Pysäytä kaikki siirrot**.</span><span class="sxs-lookup"><span data-stu-id="55f8b-145">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="55f8b-146">Jos teet näin, kaikki odottavat siirrot pysäytetään.</span><span class="sxs-lookup"><span data-stu-id="55f8b-146">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="55f8b-147">Katso myös</span><span class="sxs-lookup"><span data-stu-id="55f8b-147">See Also</span></span>
<span data-ttu-id="55f8b-148">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="55f8b-148">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="55f8b-149">[Tervetuloa [!INCLUDE[d365fin](includes/d365fin_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="55f8b-149">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

