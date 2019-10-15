---
title: Arvotapahtumien kirjauspäivämäärä
description: Lisätietoja siitä, miten Muuta kustannuksia - Nimiketapahtumat -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 2595efa188aed593bf1d112f984acf411446959b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307130"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="d6633-103">Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d6633-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="d6633-104">Tässä artikkelissa on ohjeita [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen varaston arvostustoimintojen käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="d6633-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d6633-105">Tässä artikkelissa on ohjeita siitä, miten **Muuta kustannuksia - Nimiketapahtumat** -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.</span><span class="sxs-lookup"><span data-stu-id="d6633-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="d6633-106">Ensin tarkistetaan prosessin käsite eli miten eräajo tunnistaa ja määrittää luotavan arvotapahtuman kirjauspäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="d6633-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="d6633-107">Tämän jälkeen jaetaan muutamia skenaarioita, joihin tukitiimit tärmäävät silloin tällöin. Lopuksi tutustutaan versiossa 3.0 käytettävien käsitteiden yhteenvetoon.</span><span class="sxs-lookup"><span data-stu-id="d6633-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="d6633-108">Käsite</span><span class="sxs-lookup"><span data-stu-id="d6633-108">The Concept</span></span>  
<span data-ttu-id="d6633-109">Versiossa 5.0 **Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää kirjauspäivämäärän arvotapahtumalle, jonka se luo seuraavien vaiheiden avulla:</span><span class="sxs-lookup"><span data-stu-id="d6633-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="d6633-110">Alussa luotavan tapahtuman kirjauspäivämäärä on sama kuin päivämäärän, jota se muuttaa.</span><span class="sxs-lookup"><span data-stu-id="d6633-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="d6633-111">Kirjauspäivämäärä vahvistetaan varastokausien ja/tai pääkirjanpidon asetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="d6633-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="d6633-112">Kirjauspäivämäärän määritys: jos alkuperäinen kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, eräajo määrittää sallitu kirjauspäivämäärän pääkirjanpidon asetuksista tai varastokausista.</span><span class="sxs-lookup"><span data-stu-id="d6633-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="d6633-113">Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, muutoksen arvotapahtumalle määritetään myöhempi näistä kahdesta päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="d6633-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="d6633-114">Tarkastellaan tätä prosessia lähemmin.</span><span class="sxs-lookup"><span data-stu-id="d6633-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="d6633-115">Oletetaan, että käsittelyssä on myynnin nimiketapahtuma.</span><span class="sxs-lookup"><span data-stu-id="d6633-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="d6633-116">Nimike on toimitettu 5.9.2013 ja laskutettu päivää myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="d6633-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="d6633-117">![Nimiketapahtumien tila skenaariossa](media/helene/TechArticleAdjustcost1.png "Nimiketapahtumien tila skenaariossa")</span><span class="sxs-lookup"><span data-stu-id="d6633-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="d6633-118">Alla oleva ensimmäinen arvotapahtuma (379) edustaa toimitusta. Sen kirjauspäivämäärä on sama kuin päänimiketapahtuman päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="d6633-119">Toinen arvotapahtuma (381) edustaa laskua.</span><span class="sxs-lookup"><span data-stu-id="d6633-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="d6633-120">Kolmas arvotapahtuma (391) on laskutuksen arvotapahtuman (381) muutos</span><span class="sxs-lookup"><span data-stu-id="d6633-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="d6633-121">![Arvotapahtumien tila skenaariossa](media/helene/TechArticleAdjustcost2.png "Arvotapahtumien tila skenaariossa")</span><span class="sxs-lookup"><span data-stu-id="d6633-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="d6633-122">Vaihe 1: Luotava muutoksen arvotapahtuma on määritetty samaan kirjauspäivämäärään kuin tapahtuma, jota se muuttaa, kuten yläpuolella oleva arvotapahtuma 391 osoittaa.</span><span class="sxs-lookup"><span data-stu-id="d6633-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="d6633-123">Vaihe 2: Alussa määritetyn kirjauspäivämäärän tarkistus.</span><span class="sxs-lookup"><span data-stu-id="d6633-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="d6633-124">**Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää, kuuluuko muutoksen arvotapahtuman alkuperäinen kirjauspäivämäärä sallittuun kirjauspäivämääräalueeseen varastokausien ja/tai pääkirjanpidon asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="d6633-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="d6633-125">Tarkistetaan yllämainittu myynti lisäämällä sallittujen kirjauspäivämääräalueiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="d6633-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="d6633-126">Varastokaudet:</span><span class="sxs-lookup"><span data-stu-id="d6633-126">Inventory Periods:</span></span>  

<span data-ttu-id="d6633-127">![Varastokaudet skenaariossa](media/helene/TechArticleAdjustcost3.png "Varastokaudet skenaariossa")</span><span class="sxs-lookup"><span data-stu-id="d6633-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="d6633-128">Ensimmäinen sallittu kirjauspäivämäärä on ensimmäisen avoimen kauden ensimmäinen päivä.</span><span class="sxs-lookup"><span data-stu-id="d6633-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="d6633-129">1.9.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="d6633-130">Pääkirjanpidon asetukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-130">General Ledger Setup:</span></span>  

<span data-ttu-id="d6633-131">![KP-asetukset skenaariossa](media/helene/TechArticleAdjustcost4.png "KP-asetukset skenaariossa")</span><span class="sxs-lookup"><span data-stu-id="d6633-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="d6633-132">Ensimmäinen sallittu kirjauspäivämäärä on Ensimm. sallittu kirjauspvm -kentässä mainittu päivämäärä: 10.9.2013.</span><span class="sxs-lookup"><span data-stu-id="d6633-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="d6633-133">Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, jälkimmäinen päivämäärä määrittää sallitun kirjauspäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="d6633-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="d6633-134">Vaihe 3: Sallitun kirjauspäivämäärän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d6633-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="d6633-135">Alkuperäinen määritetty kirjauspäivämäärä oli 6.9., kuten vaiheessa 1 kerrottiin.</span><span class="sxs-lookup"><span data-stu-id="d6633-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="d6633-136">Toisessa vaiheessa kuitenkin Muuta kustannuksia - Nimiketapahtumat -eräajo määrittää, että aikaisin sallittu kirjauspäivämäärä on 10.9. ja tämän vuoksi määrittää alla muutoksen arvotapahtumalle päivämäärän 10.9.</span><span class="sxs-lookup"><span data-stu-id="d6633-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="d6633-137">![Arvotapahtumien tila skenaariossa 2](media/helene/TechArticleAdjustcost5.png "Arvotapahtumien tila skenaariossa 2")</span><span class="sxs-lookup"><span data-stu-id="d6633-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="d6633-138">Olemme nyt käyneet läpi kirjauspäivämäärien määrittämisen arvotapahtumille, jotka Muuta kustannuksia - Nimiketapahtumat -eräajo on luonut.</span><span class="sxs-lookup"><span data-stu-id="d6633-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="d6633-139">Jatketaan tutkimalla skenaarioita, joita tukitiimi tapaa ajoittain, kun Muuta kustannuksia - Nimiketapahtumat -eräajon ja liittyvien asetusten määritettyjen kirjauspäivämäärien kohdalla.</span><span class="sxs-lookup"><span data-stu-id="d6633-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="d6633-140">Esimerkkitilanteet</span><span class="sxs-lookup"><span data-stu-id="d6633-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="d6633-141">Skenaario I: Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen...</span><span class="sxs-lookup"><span data-stu-id="d6633-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="d6633-142">Tässä skenaariossa käyttäjä näkee mainitun virhesanoman, kun Muuta kustannuksia - Nimiketapahtumat -eräajo suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="d6633-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="d6633-143">Edellisessä kirjauspäivämäärien määrittämistä koskevassa osassa Muuta kustannuksia - Nimiketapahtumat -eräajon tarkoitus on luoda arvotapahtuma, jonka kirjauspäivämäärä on 10.9.</span><span class="sxs-lookup"><span data-stu-id="d6633-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="d6633-144">![Kirjauspäivämäärää koskeva virhesanoma](media/helene/TechArticleAdjustcost6.png "Kirjauspäivämäärää koskeva virhesanoma")</span><span class="sxs-lookup"><span data-stu-id="d6633-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="d6633-145">Seurataan käyttäjäasetuksia;</span><span class="sxs-lookup"><span data-stu-id="d6633-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="d6633-146">![Käyttäjän sallittujen kirjauspäivämäärien asetukset](media/helene/TechArticleAdjustcost7.png "Käyttäjän sallittujen kirjauspäivämäärien asetukset")</span><span class="sxs-lookup"><span data-stu-id="d6633-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="d6633-147">Tässä tapauksessa käyttäjälle määritetty sallittu kirjauspäivämääräalue on 11.9. - 30.9. Muutoksen arvotapahtuman kirjauspäivämäärä ei siis voi olla 10.9.</span><span class="sxs-lookup"><span data-stu-id="d6633-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="d6633-148">![Asiaankuuluvan kirjauspäivämäärän asetusten yleiskatsaus](media/helene/TechArticleAdjustcost8.png "Asiaankuuluvan kirjauspäivämäärän asetusten yleiskatsaus")</span><span class="sxs-lookup"><span data-stu-id="d6633-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="d6633-149">Knowledge Base -artikkeli [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) sisältää lisää mainittuun virhesanomaan liittyviä skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="d6633-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="d6633-150">Skenaario II: Kirjauspäivämäärään verratun muutoksen arvotapahtuman kirjauspäivämäärän vuoksi muutos voi olla uudelleenarvostus tai nimikekulu.</span><span class="sxs-lookup"><span data-stu-id="d6633-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="d6633-151">Uudelleenarvostusskenaario:</span><span class="sxs-lookup"><span data-stu-id="d6633-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="d6633-152">Vaatimukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-152">Prerequisites:</span></span>  

 <span data-ttu-id="d6633-153">Varastonhallinnan asetukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-153">Inventory setup:</span></span>  

-   <span data-ttu-id="d6633-154">Automaattinen kustannusten kirjaus = Kyllä</span><span class="sxs-lookup"><span data-stu-id="d6633-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="d6633-155">Automaattinen kustannusten muuttaminen = Aina</span><span class="sxs-lookup"><span data-stu-id="d6633-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="d6633-156">Keskim. kust. laskentatyyppi = Nimike</span><span class="sxs-lookup"><span data-stu-id="d6633-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="d6633-157">Keskimääräisen kustannuksen jakso = Päivä</span><span class="sxs-lookup"><span data-stu-id="d6633-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="d6633-158">Pääkirjanpidon asetukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="d6633-159">Ensimm. sallittu kirjauspvm = 1.1.2014</span><span class="sxs-lookup"><span data-stu-id="d6633-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="d6633-160">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="d6633-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="d6633-161">Käyttäjäasetukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-161">User Setup:</span></span>  

-   <span data-ttu-id="d6633-162">Ensimm. sallittu kirjauspvm = 1.12.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="d6633-163">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="d6633-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="d6633-164">Skenaarion testaaminen</span><span class="sxs-lookup"><span data-stu-id="d6633-164">To test the scenario</span></span>  

1.  <span data-ttu-id="d6633-165">Luo TESTI-nimike:</span><span class="sxs-lookup"><span data-stu-id="d6633-165">Create item TEST:</span></span>  

     <span data-ttu-id="d6633-166">Perusmittayksikkö = Kpl</span><span class="sxs-lookup"><span data-stu-id="d6633-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="d6633-167">Arvostusmenetelmä = Keskiarvo</span><span class="sxs-lookup"><span data-stu-id="d6633-167">Costing Method = Average</span></span>  

     <span data-ttu-id="d6633-168">Valitse vaihtoehtoiset kirjausryhmät.</span><span class="sxs-lookup"><span data-stu-id="d6633-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="d6633-169">Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d6633-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="d6633-170">Kirjauspäivämäärä = 15.12.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="d6633-171">Nimike = TESTI</span><span class="sxs-lookup"><span data-stu-id="d6633-171">Item = TEST</span></span>  

     <span data-ttu-id="d6633-172">Tapahtuman tyyppi = Osto</span><span class="sxs-lookup"><span data-stu-id="d6633-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="d6633-173">Määrä = 100</span><span class="sxs-lookup"><span data-stu-id="d6633-173">Quantity = 100</span></span>  

     <span data-ttu-id="d6633-174">Yksikkösumma = 10</span><span class="sxs-lookup"><span data-stu-id="d6633-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="d6633-175">Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d6633-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="d6633-176">Päivämäärä = 20.12.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="d6633-177">Nimike = TESTI</span><span class="sxs-lookup"><span data-stu-id="d6633-177">Item = TEST</span></span>  

     <span data-ttu-id="d6633-178">Tapahtuman tyyppi = Negatiivinen muutos</span><span class="sxs-lookup"><span data-stu-id="d6633-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="d6633-179">Määrä = 2</span><span class="sxs-lookup"><span data-stu-id="d6633-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="d6633-180">Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d6633-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="d6633-181">Päivämäärä = 15.1.2014</span><span class="sxs-lookup"><span data-stu-id="d6633-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="d6633-182">Nimike = TESTI</span><span class="sxs-lookup"><span data-stu-id="d6633-182">Item = TEST</span></span>  

     <span data-ttu-id="d6633-183">Tapahtuman tyyppi = Negatiivinen muutos</span><span class="sxs-lookup"><span data-stu-id="d6633-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="d6633-184">Määrä = 3</span><span class="sxs-lookup"><span data-stu-id="d6633-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="d6633-185">Avaa uudelleenarvostuspäiväkirja ja luo ja kirjaa rivit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d6633-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="d6633-186">Nimike = TESTI</span><span class="sxs-lookup"><span data-stu-id="d6633-186">Item = TEST</span></span>  

     <span data-ttu-id="d6633-187">Kohdistetaan tapahtumaan = valitse vaiheessa 2 kirjattu ostotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="d6633-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="d6633-188">Uudelleenarvostuksen kirjauspäivämäärä on sama kuin tapahtuman, jota se muuttaa.</span><span class="sxs-lookup"><span data-stu-id="d6633-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="d6633-189">Uudelleenarvostettu yksikkökustannus = 40</span><span class="sxs-lookup"><span data-stu-id="d6633-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="d6633-190">Seuraavat nimikekirjaukset ja arvotapahtumat on kirjattu:</span><span class="sxs-lookup"><span data-stu-id="d6633-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="d6633-191">![Nimike- ja arvotapahtumien 1 yleiskatsaus](media/helene/TechArticleAdjustcost9.png "Nimike- ja arvotapahtumien 1 yleiskatsaus")</span><span class="sxs-lookup"><span data-stu-id="d6633-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="d6633-192">![Nimike- ja arvotapahtumien 2 yleiskatsaus](media/helene/TechArticleAdjustcost10.png "Nimike- ja arvotapahtumien 2 yleiskatsaus")</span><span class="sxs-lookup"><span data-stu-id="d6633-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="d6633-193">Muuta kustannuksia - Nimiketapahtumat -eräajo on tunnistavut muutokset kustannuksissa ja muuttanut negatiivisia muutoksia.</span><span class="sxs-lookup"><span data-stu-id="d6633-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="d6633-194">**Luotujen muutoksen arvotapahtumien kirjauspäivämäärien tarkistaminen:** Muuta kustannuksia - Nimiketapahtumat -eräajon aikaisin sallittu kirjauspäivämäärä on 1.1.2014 pääkirjanpidon asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="d6633-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="d6633-195">**Negatiivinen muutos vaiheessa 3:** määritetty kirjauspäivämäärä on 1.1. pääkirjanpidon asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="d6633-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="d6633-196">Muutoksen arvotapahtuman kirjauspäivämäärä on 20.12.2013.</span><span class="sxs-lookup"><span data-stu-id="d6633-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="d6633-197">Pääkirjanpidon asetusten mukaan päivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen.</span><span class="sxs-lookup"><span data-stu-id="d6633-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="d6633-198">Tämän vuoksi muutoksen arvotapahtumalle on määritetty pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="d6633-199">**Negatiivinen muutos vaiheessa 4:** määritetty kirjauspäivämäärä on 15.1.</span><span class="sxs-lookup"><span data-stu-id="d6633-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="d6633-200">Muutoksen arvotapahtuman kirjauspäivämäärä on 15.1., joka kuuluu sallittuun kirjauspäivämääräalueeseen pääkirjanpidon asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="d6633-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="d6633-201">Negatiiviseen muutokseen vaiheessa 3 tehty muutos aiheuttaa keskustelua.</span><span class="sxs-lookup"><span data-stu-id="d6633-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="d6633-202">Muutoksen arvotapahtuman suositeltu kirjauspäivämäärä olisi ollut 20.12. tai jokin muu joulukuun päivämäärä, koska myytyjen tuotteiden kustannusten muutoksen aiheuttanut uudelleenarvostus kirjattiin joulukuussa.</span><span class="sxs-lookup"><span data-stu-id="d6633-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="d6633-203">Jotta negatiiviseen muutokseen voidaan tehdä muutos joulukuussa vaiheessa 3, pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärän on oltava joulukuussa.</span><span class="sxs-lookup"><span data-stu-id="d6633-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="d6633-204">**Yhteenveto.**</span><span class="sxs-lookup"><span data-stu-id="d6633-204">**Conclusion:**</span></span>  

 <span data-ttu-id="d6633-205">Tämän skenaarion kokemusten perusteella yritykselle parhaiten sopivin sallitun kirjauspäivämääräalueen asetus voisi olla noudattaa seuraavia periaatteita: niin kauan kuin varastoarvon muutokset voidaan kirjata kauden aikana, tässä tapauksessa joulukuussa, yrityksen sallitun kirjauspäivämääräalueen asetus tulee määrittää tämän mukaan.</span><span class="sxs-lookup"><span data-stu-id="d6633-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="d6633-206">Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kenttä, johon on määritetty 1.12., sallii joulukuussa tehdyn uudelleenarvostuksen ohjauksen edelleen saman kauden muuttuneisiin lähteviin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="d6633-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="d6633-207">Tässä skenaariossa ollut asetus, jonka mukaan käyttäjäryhmät, jotka eivät voi tehdä kirjauksia joulukuussa, voivat tehdä niitä tammikuussa, kannattaa määrittää käyttäjäasetuksissa pääkirjanpidon asetusten sijaan.</span><span class="sxs-lookup"><span data-stu-id="d6633-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="d6633-208">Nimikekulujen skenaario:</span><span class="sxs-lookup"><span data-stu-id="d6633-208">Item charge scenario:</span></span>  
 <span data-ttu-id="d6633-209">Vaatimukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-209">Prerequisites:</span></span>  

 <span data-ttu-id="d6633-210">Varastonhallinnan asetukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-210">Inventory setup:</span></span>  

-   <span data-ttu-id="d6633-211">Automaattinen kustannusten kirjaus = Kyllä</span><span class="sxs-lookup"><span data-stu-id="d6633-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="d6633-212">Automaattinen kustannusten muuttaminen = Aina</span><span class="sxs-lookup"><span data-stu-id="d6633-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="d6633-213">Keskim. kust. laskentatyyppi = Nimike</span><span class="sxs-lookup"><span data-stu-id="d6633-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="d6633-214">Keskimääräisen kustannuksen jakso = Päivä</span><span class="sxs-lookup"><span data-stu-id="d6633-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="d6633-215">Pääkirjanpidon asetukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="d6633-216">Ensimm. sallittu kirjauspvm = 1.12.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="d6633-217">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="d6633-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="d6633-218">Käyttäjäasetukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-218">User Setup:</span></span>  

-   <span data-ttu-id="d6633-219">Ensimm. sallittu kirjauspvm = 1.12.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="d6633-220">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="d6633-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="d6633-221">Skenaarion testaaminen</span><span class="sxs-lookup"><span data-stu-id="d6633-221">To test the scenario</span></span>  

1.  <span data-ttu-id="d6633-222">Luo nimikekulu:</span><span class="sxs-lookup"><span data-stu-id="d6633-222">Create item charge:</span></span>  

     <span data-ttu-id="d6633-223">Perusmittayksikkö = Kpl</span><span class="sxs-lookup"><span data-stu-id="d6633-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="d6633-224">Arvostusmenetelmä = Keskiarvo</span><span class="sxs-lookup"><span data-stu-id="d6633-224">Costing Method = Average</span></span>  

     <span data-ttu-id="d6633-225">Valitse vaihtoehtoiset kirjausryhmät.</span><span class="sxs-lookup"><span data-stu-id="d6633-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="d6633-226">Luo uusi ostotilaus</span><span class="sxs-lookup"><span data-stu-id="d6633-226">Create new purchase order</span></span>  

     <span data-ttu-id="d6633-227">Tavarantoimittajan nro: 10 000</span><span class="sxs-lookup"><span data-stu-id="d6633-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="d6633-228">Kirjauspäivämäärä = 15.12.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="d6633-229">Toimittajan laskunro: 1 234</span><span class="sxs-lookup"><span data-stu-id="d6633-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="d6633-230">Ostotilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="d6633-230">On the purchase order line:</span></span>  

     <span data-ttu-id="d6633-231">Nimike = KULU</span><span class="sxs-lookup"><span data-stu-id="d6633-231">Item = CHARGE</span></span>  

     <span data-ttu-id="d6633-232">Määrä = 1</span><span class="sxs-lookup"><span data-stu-id="d6633-232">Quantity = 1</span></span>  

     <span data-ttu-id="d6633-233">Välitön yksikkökustannus = 100</span><span class="sxs-lookup"><span data-stu-id="d6633-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="d6633-234">Kirjaa vastaanottaminen ja lasku.</span><span class="sxs-lookup"><span data-stu-id="d6633-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="d6633-235">Luo uusi myyntitilaus:</span><span class="sxs-lookup"><span data-stu-id="d6633-235">Create new sales order:</span></span>  

     <span data-ttu-id="d6633-236">Tilausasiakkaan nro: 10000</span><span class="sxs-lookup"><span data-stu-id="d6633-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="d6633-237">Kirjauspäivämäärä = 16.12.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="d6633-238">Myytitilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="d6633-238">On the sales order line:</span></span>  

     <span data-ttu-id="d6633-239">Nimike = KULU</span><span class="sxs-lookup"><span data-stu-id="d6633-239">Item = CHARGE</span></span>  

     <span data-ttu-id="d6633-240">Määrä = 1</span><span class="sxs-lookup"><span data-stu-id="d6633-240">Quantity = 1</span></span>  

     <span data-ttu-id="d6633-241">Yksikköhinta = 135</span><span class="sxs-lookup"><span data-stu-id="d6633-241">Unit Price = 135</span></span>  

     <span data-ttu-id="d6633-242">Kirjaa toimitus ja lasku.</span><span class="sxs-lookup"><span data-stu-id="d6633-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="d6633-243">Pääkirjanpidon asetukset:</span><span class="sxs-lookup"><span data-stu-id="d6633-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="d6633-244">Ensimm. sallittu kirjauspvm = 1.1.2014</span><span class="sxs-lookup"><span data-stu-id="d6633-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="d6633-245">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="d6633-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="d6633-246">Luo uusi ostotilaus:</span><span class="sxs-lookup"><span data-stu-id="d6633-246">Create new purchase order:</span></span>  

     <span data-ttu-id="d6633-247">Tavarantoimittajan nro: 10 000</span><span class="sxs-lookup"><span data-stu-id="d6633-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="d6633-248">Kirjauspäivämäärä = 2.1.2014</span><span class="sxs-lookup"><span data-stu-id="d6633-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="d6633-249">Toimittajan laskunro: 2 345</span><span class="sxs-lookup"><span data-stu-id="d6633-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="d6633-250">Ostotilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="d6633-250">On the purchase order line:</span></span>  

     <span data-ttu-id="d6633-251">Nimikekulu = JB-RAHTI</span><span class="sxs-lookup"><span data-stu-id="d6633-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="d6633-252">Määrä = 1</span><span class="sxs-lookup"><span data-stu-id="d6633-252">Quantity = 1</span></span>  

     <span data-ttu-id="d6633-253">Välitön yksikkökustannus = 3</span><span class="sxs-lookup"><span data-stu-id="d6633-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="d6633-254">Määritä nimikekuluksi ostovastaanotto vaiheesta 2.</span><span class="sxs-lookup"><span data-stu-id="d6633-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="d6633-255">Kirjaa vastaanotto ja lasku.</span><span class="sxs-lookup"><span data-stu-id="d6633-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="d6633-256">![Nimike- ja arvotapahtumien 3 yleiskatsaus](media/helene/TechArticleAdjustcost11.png "Nimike- ja arvotapahtumien 3 yleiskatsaus")</span><span class="sxs-lookup"><span data-stu-id="d6633-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="d6633-257">Ostolasku saapuu käsittelypäivänä 3.1. Ostolasku sisältää vaiheessa 2 ostoon tehdyn lisäkulun.</span><span class="sxs-lookup"><span data-stu-id="d6633-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="d6633-258">Tämän laskun asiakirjan päivämäärä on 30.12. Tämän vuoksi sen kirjauspäivämääräksi tulee 30.12.2013.</span><span class="sxs-lookup"><span data-stu-id="d6633-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="d6633-259">Luo uusi ostotilaus:</span><span class="sxs-lookup"><span data-stu-id="d6633-259">Create new purchase order:</span></span>  

     <span data-ttu-id="d6633-260">Tavarantoimittajan nro: 10 000</span><span class="sxs-lookup"><span data-stu-id="d6633-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="d6633-261">Kirjauspäivämäärä = 30.12.2013</span><span class="sxs-lookup"><span data-stu-id="d6633-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="d6633-262">Toimittajan laskunro: 3 456</span><span class="sxs-lookup"><span data-stu-id="d6633-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="d6633-263">Ostotilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="d6633-263">On the purchase order line:</span></span>  

     <span data-ttu-id="d6633-264">Nimikekulu = JB-RAHTI</span><span class="sxs-lookup"><span data-stu-id="d6633-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="d6633-265">Määrä = 1</span><span class="sxs-lookup"><span data-stu-id="d6633-265">Quantity = 1</span></span>  

     <span data-ttu-id="d6633-266">Välitön yksikkökustannus = 2</span><span class="sxs-lookup"><span data-stu-id="d6633-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="d6633-267">Määritä nimikekuluksi ostovastaanotto vaiheesta 2</span><span class="sxs-lookup"><span data-stu-id="d6633-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="d6633-268">Kirjaa vastaanotto ja lasku.</span><span class="sxs-lookup"><span data-stu-id="d6633-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="d6633-269">![Nimike- ja arvotapahtumien 4 yleiskatsaus](media/helene/TechArticleAdjustcost12.png "Nimike- ja arvotapahtumien 4 yleiskatsaus")</span><span class="sxs-lookup"><span data-stu-id="d6633-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="d6633-270">Varaston arvostus -raportti tulostetaan 31.12.2013.</span><span class="sxs-lookup"><span data-stu-id="d6633-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="d6633-271">![Varaston arvostusraportin sisältö](media/helene/TechArticleAdjustcost13.png "Varaston arvostusraportin sisältö")</span><span class="sxs-lookup"><span data-stu-id="d6633-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="d6633-272">**Skenaarion yhteenveto:**</span><span class="sxs-lookup"><span data-stu-id="d6633-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="d6633-273">Kuvattu skenaario loppuu Varaston arvostus -raporttiin, jossa määrä = 0 ja arvo = 2.</span><span class="sxs-lookup"><span data-stu-id="d6633-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="d6633-274">Vaiheessa 11 kirjattu nimikekulu on osa varaston arvon nousua joulukuussa. Saman kauden varaston arvon lasku ei ole muuttunut.</span><span class="sxs-lookup"><span data-stu-id="d6633-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="d6633-275">Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvo 1.1. on sopiva ensimmäiselle nimikekululle.</span><span class="sxs-lookup"><span data-stu-id="d6633-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="d6633-276">Varaston arvon nousun ja laskun kustannukset tallennettiin samaan kauteen.</span><span class="sxs-lookup"><span data-stu-id="d6633-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="d6633-277">Pääkirjanpidon asetusten vuoksi toinen nimikekulu aiheuttaa kuitenkin muutoksen myytyjen tuotteiden kustannuksessa. Muutos otetaan huomioon seuraavan kauden aikana.</span><span class="sxs-lookup"><span data-stu-id="d6633-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="d6633-278">**Yhteenveto.**</span><span class="sxs-lookup"><span data-stu-id="d6633-278">**Conclusion:**</span></span>  

 <span data-ttu-id="d6633-279">On haastavaa, kun Varaston arvostus -raportissa määritetään, että määrä = 0 samalla, kun arvo <> 0.</span><span class="sxs-lookup"><span data-stu-id="d6633-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="d6633-280">Tässä tapauksessa on vaikeaa kertoa optimaaliset asetukset, koska ostolaskut saapuvat samana päivänä mutta ne koskevat eri kausia tai jopa eri tilivuosia.</span><span class="sxs-lookup"><span data-stu-id="d6633-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="d6633-281">Uuteen tilivuoteen siirtäminen vaatii yleensä suunnittelua. Muuta kustannuksia - Nimiketapahtumat -prosessin on myös otettava huomioon myytyjen tuotteiden kustannukset.</span><span class="sxs-lookup"><span data-stu-id="d6633-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="d6633-282">Tässä skenaariossa eräs vaihtoehto olisi ollut määrittää pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvoksi muutamaa päivää aikaisempi joulukuun päivämäärä ja kirjata ensimmäinen nimikekulu viiveellä, jolloin edellisen kauden/tilivuoden kaikki kustannukset tuloutettaisiin kaudelle, jolle ne alussa kuuluivat. Tämän jälkeen suoritettaisiin Muuta kustannuksia - Nimiketapahtumat -eräajo ja siirrettäisiin sallittu kirjauspäivämäärä seuraavaan kauteen\/tilivuoteen.</span><span class="sxs-lookup"><span data-stu-id="d6633-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="d6633-283">Kirjatuksi olisi tullut ensimmäinen nimikekulu, jonka kirjauspäivämäärä on 2.1.</span><span class="sxs-lookup"><span data-stu-id="d6633-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="d6633-284">Muuta kustannuksia - Nimiketapahtumat -eräajon historia</span><span class="sxs-lookup"><span data-stu-id="d6633-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="d6633-285">Alla on Muuta kustannuksia - Nimiketapahtumat -eräajon muutoksen arvotapahtumien kirjauspäivämäärien määrittämisen yhteenveto versiosta 3.0 lähtien.</span><span class="sxs-lookup"><span data-stu-id="d6633-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="d6633-286">Versiosta 3.0..3.70.A lähtien</span><span class="sxs-lookup"><span data-stu-id="d6633-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="d6633-287">Muuta kustannuksia - Nimiketapahtumat -eräajon pyyntölomakkeessa on käyttäjän antama kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="d6633-288">Eräajo käy läpi kaikki pakolliset muutokset ja luo arvotapahtumat, joille annetaan pyyntölomakkeen kirjauspäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="d6633-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="d6633-289">Ehdotettu kirjauspäivämäärä on tämän päivän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="d6633-290">Versio 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="d6633-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="d6633-291">Muuta kustannuksia - Nimiketapahtumat -eräajon pyyntölomakkeessa on käyttäjän antama suljetun kauden tapahtuman kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="d6633-292">Eräajo käy läpi kaikki tarvittavat muutokset ja luo arvotapahtumat ja päänimikkeen tapahtuman kirjauspäivämäärän (sen myynnin toimituspäivämäärä, jota muutos koskee).</span><span class="sxs-lookup"><span data-stu-id="d6633-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="d6633-293">Jos päänimikkeen tapahtuma ei kuulu sallittuun kirjauspäivämääräalueeseen, suljetun kauden tapahtuman kirjauspäivämääränä ilmoitetulle kirjauspäivämäärälle määritetää muutoksen arvotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="d6633-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="d6633-294">Päivämäärä on suljetulla kaudella, kun se on aikaisempi kuin pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="d6633-295">Versiosta 5.0 lähtien:</span><span class="sxs-lookup"><span data-stu-id="d6633-295">From version 5.0:</span></span>  
 <span data-ttu-id="d6633-296">Muuta kustannuksia - Nimiketapahtumat -eräajon pyyntölomakkeessa ei ole enää ilmoitettavaa kirjauspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="d6633-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="d6633-297">Eräajo käy läpi kaikki pakolliset muutokset ja luo arvotapahtumat, joilla on sen arvotapahtuman kirjauspäivämäärä, jonka eräajo muuttaa.</span><span class="sxs-lookup"><span data-stu-id="d6633-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="d6633-298">Jos kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, käytetään pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä tai mahdollisesti käytössä olevien varastokausien kirjauspäivämäärää sen mukaan, kumpi on myöhempi.</span><span class="sxs-lookup"><span data-stu-id="d6633-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="d6633-299">Katso edellä kuvattua käsitettä.</span><span class="sxs-lookup"><span data-stu-id="d6633-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="d6633-300">Kirjaa varaston kustannukset kirjanpitoon -eräajon historia</span><span class="sxs-lookup"><span data-stu-id="d6633-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="d6633-301">Kirjaa varaston kustannukset kirjanpitoon -eräajo liittyy läheisesti Muuta kustannuksia - Nimiketapahtumat -eräajoon. Tämän vuoksi kyseisen eräajon historiasta tehdään yhteenveto, joka jaetaan myös täällä.</span><span class="sxs-lookup"><span data-stu-id="d6633-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="d6633-302">Versiosta 3.0..3.70.A lähtien</span><span class="sxs-lookup"><span data-stu-id="d6633-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="d6633-303">Kirjaa varaston kustannukset kirjanpitoon -eräajon pyyntölomakkeessa on käyttäjän antama kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="d6633-304">Eräajo käy läpi kaikki suodattimen mahdolliset arvotapahtumat ja luo pääkirjanpidon tapahtumat, joille annetaan pyyntölomakkeen kirjauspäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="d6633-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="d6633-305">Versio 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="d6633-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="d6633-306">Kirjaa varaston kustannukset kirjanpitoon -eräajon pyyntölomakkeessa on käytettävissä Suljetun kauden tapahtuman kirjauspäivämäärä -kenttä.</span><span class="sxs-lookup"><span data-stu-id="d6633-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="d6633-307">Sovellus käyttää tähän kenttään annettua päivämäärää niiden pääkirjanpidon tapahtumien kirjauspäivämääränä, jotka se luo arvotapahtumille, joiden kirjauspäivämäärät ovat suljetuilla tilikausilla.</span><span class="sxs-lookup"><span data-stu-id="d6633-307">The application uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="d6633-308">Muussa tapauksessa pääkirjanpidon tapahtumilla on samat kirjauspäivämäärät kuin alkuperäisillä arvotapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="d6633-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="d6633-309">Päivämäärä on suljetulla kaudella, kun se on aikaisempi kuin pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="d6633-310">Jos kirjaus tehdään kirjanpitoon kirjausryhmän mukaan, pääkirjanpidon tapahtumien kirjauspäivämäärä on pyyntölomakkeen Kirjauspäivämäärä-kentässä määritetty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="d6633-311">Versioissa 3 ja 4 eräajo skannaa kaikki arvotapahtumat ja määrittää, löytyykö arvotapahtumia, joiden kustannussumma (todellinen) on eri kuin kirjanpitoon kirjattu kustannus.</span><span class="sxs-lookup"><span data-stu-id="d6633-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="d6633-312">Jos eroja löytyy, eroava summa kirjataan KP-tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="d6633-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="d6633-313">Jos käytössä on oletettujen kustannusten kirjaus, vastaavat kentät käsitellään samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="d6633-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="d6633-314">![Todellinen kustannus verrattuna odotettuun kustannukseen](media/helene/TechArticleAdjustcost14.png "Todellinen kustannus verrattuna odotettuun kustannukseen")</span><span class="sxs-lookup"><span data-stu-id="d6633-314">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="d6633-315">Versiosta 5.0 lähtien:</span><span class="sxs-lookup"><span data-stu-id="d6633-315">From version 5.0:</span></span>  
 <span data-ttu-id="d6633-316">Kirjaa varaston kustannukset kirjanpitoon -eräajon pyyntölomakkeessa ei ole enää ilmoitettavaa kirjauspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="d6633-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="d6633-317">Luodaan KP-tapahtuma, jolla on sama kirjauspäivämäärä kuin liittyvällä arvotapahtumalla.</span><span class="sxs-lookup"><span data-stu-id="d6633-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="d6633-318">Jotta eräajo voidaan suorittaa, sallitun kirjauspäivämääräalueen on sallittava luodun KP-tapahtuman kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d6633-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="d6633-319">Muussa tapauksessa sallittu kirjauspäivämääräalue on avattava uudelleen tilapäisesti joko muuttamalla päivämääriä tai poistamalla niitä pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm- ja Viimeinen sallittu kirjauspvm -kentissä.</span><span class="sxs-lookup"><span data-stu-id="d6633-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="d6633-320">Vältät täsmäytysongelmat, kun KP-tapahtuman kirjauspäivämäärä vastaa arvotapahtuman kirjauspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="d6633-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="d6633-321">Kirjaa arvotapahtuma kirjanpitoon -eräajo skannaa taulukon 5811 ja tunnistaa alueeseen kuuluvat arvotapahtumat pääkirjanpitoon kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="d6633-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="d6633-322">Kun eräajo on suoritettu, taulukko tyhjennetään.</span><span class="sxs-lookup"><span data-stu-id="d6633-322">After successful run the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6633-323">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d6633-323">See Also</span></span>  
[<span data-ttu-id="d6633-324">Rakennetiedot: Varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="d6633-324">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="d6633-325">Rakennetiedot: Nimikkeen kohdistus</span><span class="sxs-lookup"><span data-stu-id="d6633-325">Design Details: Item Application</span></span>](design-details-item-application.md)  
