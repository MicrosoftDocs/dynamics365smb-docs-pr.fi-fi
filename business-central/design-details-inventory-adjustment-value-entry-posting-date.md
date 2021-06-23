---
title: Arvotapahtumien kirjauspäivämäärä
description: Lisätietoja siitä, miten Muuta kustannuksia - Nimiketapahtumat -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 918a450ea40676447f872ba95eb489c7cc210211
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215101"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="7d3f3-103">Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="7d3f3-104">Tässä artikkelissa on ohjeita [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen varaston arvostustoimintojen käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="7d3f3-105">Tässä artikkelissa on ohjeita siitä, miten **Muuta kustannuksia - Nimiketapahtumat** -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="7d3f3-106">Ensin tarkistetaan prosessin käsite eli miten eräajo tunnistaa ja määrittää luotavan arvotapahtuman kirjauspäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="7d3f3-107">Tämän jälkeen jaetaan muutamia skenaarioita, joihin tukitiimit tärmäävät silloin tällöin. Lopuksi tutustutaan käsitteiden yhteenvetoon.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="7d3f3-108">Käsite</span><span class="sxs-lookup"><span data-stu-id="7d3f3-108">The Concept</span></span>  
<span data-ttu-id="7d3f3-109">**Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää kirjauspäivämäärän arvotapahtumalle, jonka se luo seuraavien vaiheiden avulla:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-109">The **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="7d3f3-110">Alussa luotavan tapahtuman kirjauspäivämäärä on sama kuin päivämäärän, jota se muuttaa.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="7d3f3-111">Kirjauspäivämäärä vahvistetaan varastokausien ja/tai pääkirjanpidon asetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="7d3f3-112">Kirjauspäivämäärän määritys: jos alkuperäinen kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, eräajo määrittää sallitu kirjauspäivämäärän pääkirjanpidon asetuksista tai varastokausista.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="7d3f3-113">Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, muutoksen arvotapahtumalle määritetään myöhempi näistä kahdesta päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="7d3f3-114">Tarkastellaan tätä prosessia lähemmin.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="7d3f3-115">Oletetaan, että käsittelyssä on myynnin nimiketapahtuma.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="7d3f3-116">Nimike on toimitettu 5.9.2013 ja laskutettu päivää myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-116">The item was shipped on September 5, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="7d3f3-117">![Nimiketapahtumien tila skenaariossa](media/helene/TechArticleAdjustcost1.png "Nimiketapahtumien tila skenaariossa")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="7d3f3-118">Alla oleva ensimmäinen arvotapahtuma (379) edustaa toimitusta. Sen kirjauspäivämäärä on sama kuin päänimiketapahtuman päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="7d3f3-119">Toinen arvotapahtuma (381) edustaa laskua.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="7d3f3-120">Kolmas arvotapahtuma (391) on laskutuksen arvotapahtuman (381) muutos</span><span class="sxs-lookup"><span data-stu-id="7d3f3-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="7d3f3-121">![Arvotapahtumien tila skenaariossa](media/helene/TechArticleAdjustcost2.png "Arvotapahtumien tila skenaariossa")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="7d3f3-122">Vaihe 1: Luotava muutoksen arvotapahtuma on määritetty samaan kirjauspäivämäärään kuin tapahtuma, jota se muuttaa, kuten yläpuolella oleva arvotapahtuma 391 osoittaa.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="7d3f3-123">Vaihe 2: Alussa määritetyn kirjauspäivämäärän tarkistus.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="7d3f3-124">**Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää, kuuluuko muutoksen arvotapahtuman alkuperäinen kirjauspäivämäärä sallittuun kirjauspäivämääräalueeseen varastokausien ja/tai pääkirjanpidon asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="7d3f3-125">Tarkistetaan yllämainittu myynti lisäämällä sallittujen kirjauspäivämääräalueiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="7d3f3-126">Varastokaudet:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-126">Inventory Periods:</span></span>  

<span data-ttu-id="7d3f3-127">![Varastokaudet skenaariossa](media/helene/TechArticleAdjustcost3.png "Varastokaudet skenaariossa")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="7d3f3-128">Ensimmäinen sallittu kirjauspäivämäärä on ensimmäisen avoimen kauden ensimmäinen päivä.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="7d3f3-129">1. syyskuuta 2013.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-129">September 1, 2013.</span></span>  

 <span data-ttu-id="7d3f3-130">Pääkirjanpidon asetukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-130">General Ledger Setup:</span></span>  

<span data-ttu-id="7d3f3-131">![Pääkirjanpidon asetukset skenaariossa](media/helene/TechArticleAdjustcost4.png "Pääkirjanpidon asetukset skenaariossa")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="7d3f3-132">Ensimmäinen sallittu kirjauspäivämäärä on Ensimm. sallittu kirjauspvm -kentässä mainittu päivämäärä: 10.9.2013.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-132">First allowed posting date is the date stated in field Allow Posting From: September 10, 2013.</span></span>  

 <span data-ttu-id="7d3f3-133">Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, jälkimmäinen päivämäärä määrittää sallitun kirjauspäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="7d3f3-134">Vaihe 3: Sallitun kirjauspäivämäärän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d3f3-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="7d3f3-135">Alkuperäinen määritetty kirjauspäivämäärä oli 6.9., kuten vaiheessa 1 kerrottiin.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-135">The initial assigned Posting Date was September 6 as illustrated in step 1.</span></span> <span data-ttu-id="7d3f3-136">Toisessa vaiheessa kuitenkin Muuta kustannuksia - Nimiketapahtumat -eräajo määrittää, että aikaisin sallittu kirjauspäivämäärä on 10.9. ja tämän vuoksi määrittää alla muutoksen arvotapahtumalle päivämäärän 10.9.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-136">However, in the second step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10 and thereby assigns September 10 to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="7d3f3-137">![Arvotapahtumien tila skenaariossa 2](media/helene/TechArticleAdjustcost5.png "Arvotapahtumien tila skenaariossa 2")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="7d3f3-138">Olemme nyt käyneet läpi kirjauspäivämäärien määrittämisen arvotapahtumille, jotka Muuta kustannuksia - Nimiketapahtumat -eräajo on luonut.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="7d3f3-139">Jatketaan tutkimalla skenaarioita, joita tukitiimi tapaa ajoittain, kun Muuta kustannuksia - Nimiketapahtumat -eräajon ja liittyvien asetusten määritettyjen kirjauspäivämäärien kohdalla.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="7d3f3-140">Esimerkkitilanteet</span><span class="sxs-lookup"><span data-stu-id="7d3f3-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="7d3f3-141">Skenaario I: Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen...</span><span class="sxs-lookup"><span data-stu-id="7d3f3-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="7d3f3-142">Tässä skenaariossa käyttäjä näkee mainitun virhesanoman, kun Muuta kustannuksia - Nimiketapahtumat -eräajo suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="7d3f3-143">Edellisessä kirjauspäivämäärien määrittämistä koskevassa osassa Muuta kustannuksia - Nimiketapahtumat -eräajon tarkoitus on luoda arvotapahtuma, jonka kirjauspäivämäärä on 10.9.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="7d3f3-144">![Kirjauspäivämäärää koskeva virhesanoma](media/helene/TechArticleAdjustcost6.png "Kirjauspäivämäärää koskeva virhesanoma")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="7d3f3-145">Seurataan käyttäjäasetuksia;</span><span class="sxs-lookup"><span data-stu-id="7d3f3-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="7d3f3-146">![Käyttäjän sallittujen kirjauspäivämäärien asetus](media/helene/TechArticleAdjustcost7.png "Käyttäjän sallittujen kirjauspäivämäärien asetus")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="7d3f3-147">Tässä tapauksessa käyttäjälle määritetty sallittu kirjauspäivämääräalue on 11.9.–30.9. Muutoksen arvotapahtuman kirjauspäivämäärä ei siis voi olla 10.9.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-147">The user in this case has an allowed posting date range from September 11 to September 30 and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="7d3f3-148">![Asiaankuuluvan kirjauspäivämäärän asetuksen yleiskuvaus](media/helene/TechArticleAdjustcost8.png "Asiaankuuluvan kirjauspäivämäärän asetuksen yleiskuvaus")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="7d3f3-149">Knowledge Base -artikkeli [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) sisältää lisää mainittuun virhesanomaan liittyviä skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses more scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="7d3f3-150">Skenaario II: Kirjauspäivämäärään verratun muutoksen arvotapahtuman kirjauspäivämäärän vuoksi muutos voi olla uudelleenarvostus tai nimikekulu.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="7d3f3-151">Uudelleenarvostusskenaario:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="7d3f3-152">Vaatimukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-152">Prerequisites:</span></span>  

 <span data-ttu-id="7d3f3-153">Varastonhallinnan asetukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-153">Inventory setup:</span></span>  

-   <span data-ttu-id="7d3f3-154">Automaattinen kustannusten kirjaus = Kyllä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="7d3f3-155">Automaattinen kustannusten muuttaminen = Aina</span><span class="sxs-lookup"><span data-stu-id="7d3f3-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="7d3f3-156">Keskim. kust. laskentatyyppi = Nimike</span><span class="sxs-lookup"><span data-stu-id="7d3f3-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="7d3f3-157">Keskimääräisen kustannuksen jakso = Päivä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="7d3f3-158">Pääkirjanpidon asetukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="7d3f3-159">Ensimm. sallittu kirjauspvm = 1.1.2014</span><span class="sxs-lookup"><span data-stu-id="7d3f3-159">Allow Posting From = January 1, 2014</span></span>  

-   <span data-ttu-id="7d3f3-160">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="7d3f3-161">Käyttäjäasetukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-161">User Setup:</span></span>  

-   <span data-ttu-id="7d3f3-162">Ensimm. sallittu kirjauspvm = 1.12.2013</span><span class="sxs-lookup"><span data-stu-id="7d3f3-162">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="7d3f3-163">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="7d3f3-164">Skenaarion testaaminen</span><span class="sxs-lookup"><span data-stu-id="7d3f3-164">To test the scenario</span></span>  

1.  <span data-ttu-id="7d3f3-165">Luo TESTI-nimike:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-165">Create item TEST:</span></span>  

     <span data-ttu-id="7d3f3-166">Perusmittayksikkö = Kpl</span><span class="sxs-lookup"><span data-stu-id="7d3f3-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="7d3f3-167">Arvostusmenetelmä = Keskiarvo</span><span class="sxs-lookup"><span data-stu-id="7d3f3-167">Costing Method = Average</span></span>  

     <span data-ttu-id="7d3f3-168">Valitse vaihtoehtoiset kirjausryhmät.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="7d3f3-169">Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-169">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="7d3f3-170">Kirjauspäivämäärä = 15.12.2013</span><span class="sxs-lookup"><span data-stu-id="7d3f3-170">Posting Date = December 15, 2013</span></span>  

     <span data-ttu-id="7d3f3-171">Nimike = TESTI</span><span class="sxs-lookup"><span data-stu-id="7d3f3-171">Item = TEST</span></span>  

     <span data-ttu-id="7d3f3-172">Tapahtuman tyyppi = Osto</span><span class="sxs-lookup"><span data-stu-id="7d3f3-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="7d3f3-173">Määrä = 100</span><span class="sxs-lookup"><span data-stu-id="7d3f3-173">Quantity = 100</span></span>  

     <span data-ttu-id="7d3f3-174">Yksikkösumma = 10</span><span class="sxs-lookup"><span data-stu-id="7d3f3-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="7d3f3-175">Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-175">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="7d3f3-176">Päivämäärä = 20.12.2013</span><span class="sxs-lookup"><span data-stu-id="7d3f3-176">Date = December 20, 2013</span></span>  

     <span data-ttu-id="7d3f3-177">Nimike = TESTI</span><span class="sxs-lookup"><span data-stu-id="7d3f3-177">Item = TEST</span></span>  

     <span data-ttu-id="7d3f3-178">Tapahtuman tyyppi = Negatiivinen muutos</span><span class="sxs-lookup"><span data-stu-id="7d3f3-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="7d3f3-179">Määrä = 2</span><span class="sxs-lookup"><span data-stu-id="7d3f3-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="7d3f3-180">Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-180">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="7d3f3-181">Päivämäärä = 15.1.2014</span><span class="sxs-lookup"><span data-stu-id="7d3f3-181">Date = January 15, 2014</span></span>  

     <span data-ttu-id="7d3f3-182">Nimike = TESTI</span><span class="sxs-lookup"><span data-stu-id="7d3f3-182">Item = TEST</span></span>  

     <span data-ttu-id="7d3f3-183">Tapahtuman tyyppi = Negatiivinen muutos</span><span class="sxs-lookup"><span data-stu-id="7d3f3-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="7d3f3-184">Määrä = 3</span><span class="sxs-lookup"><span data-stu-id="7d3f3-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="7d3f3-185">Avaa uudelleenarvostuspäiväkirja ja luo ja kirjaa rivit seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-185">Open Revaluation Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="7d3f3-186">Nimike = TESTI</span><span class="sxs-lookup"><span data-stu-id="7d3f3-186">Item = TEST</span></span>  

     <span data-ttu-id="7d3f3-187">Kohdistetaan tapahtumaan = valitse vaiheessa 2 kirjattu ostotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="7d3f3-188">Uudelleenarvostuksen kirjauspäivämäärä on sama kuin tapahtuman, jota se muuttaa.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="7d3f3-189">Uudelleenarvostettu yksikkökustannus = 40</span><span class="sxs-lookup"><span data-stu-id="7d3f3-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="7d3f3-190">Seuraavat nimikekirjaukset ja arvotapahtumat on kirjattu:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="7d3f3-191">![Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 1](media/helene/TechArticleAdjustcost9.png "Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 1")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="7d3f3-192">![Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 2](media/helene/TechArticleAdjustcost10.png "Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 2")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="7d3f3-193">Muuta kustannuksia - Nimiketapahtumat -eräajo on tunnistavut muutokset kustannuksissa ja muuttanut negatiivisia muutoksia.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="7d3f3-194">**Luotujen muutoksen arvotapahtumien kirjauspäivämäärien tarkistaminen:** Muuta kustannuksia - Nimiketapahtumat -eräajon aikaisin sallittu kirjauspäivämäärä on 1.1.2014 pääkirjanpidon asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="7d3f3-195">**Negatiivinen muutos vaiheessa 3:** määritetty kirjauspäivämäärä on 1.1. pääkirjanpidon asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1, provided by General Ledger Setup.</span></span> <span data-ttu-id="7d3f3-196">Muutoksen arvotapahtuman kirjauspäivämäärä on 20.12.2013.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="7d3f3-197">Pääkirjanpidon asetusten mukaan päivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-197">According to General Ledger Setup, the date is not within allowed posting date range.</span></span> <span data-ttu-id="7d3f3-198">Tämän vuoksi muutoksen arvotapahtumalle on määritetty pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="7d3f3-199">**Negatiivinen muutos vaiheessa 4:** määritetty kirjauspäivämäärä on 15.1.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15.</span></span> <span data-ttu-id="7d3f3-200">Muutoksen arvotapahtuman kirjauspäivämäärä on 15.1., joka kuuluu sallittuun kirjauspäivämääräalueeseen pääkirjanpidon asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-200">The Value Entry in scope of adjustment has Posting Date January 15, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="7d3f3-201">Negatiiviseen muutokseen vaiheessa 3 tehty muutos aiheuttaa keskustelua.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="7d3f3-202">Muutoksen arvotapahtuman suositeltu kirjauspäivämäärä olisi ollut 20.12. tai jokin muu joulukuun päivämäärä, koska myytyjen tuotteiden kustannusten muutoksen aiheuttanut uudelleenarvostus kirjattiin joulukuussa.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20 or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="7d3f3-203">Jotta negatiiviseen muutokseen voidaan tehdä muutos joulukuussa vaiheessa 3, pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärän on oltava joulukuussa.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="7d3f3-204">**Yhteenveto.**</span><span class="sxs-lookup"><span data-stu-id="7d3f3-204">**Conclusion:**</span></span>  

 <span data-ttu-id="7d3f3-205">Tämän skenaarion kokemusten perusteella yritykselle parhaiten sopivin sallitun kirjauspäivämääräalueen asetus voisi olla noudattaa seuraavia periaatteita: niin kauan kuin varastoarvon muutokset voidaan kirjata kauden aikana, tässä tapauksessa joulukuussa, yrityksen sallitun kirjauspäivämääräalueen asetus tulee määrittää tämän mukaan.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, you might want to consider the following information: As long as you allow changes in inventory value to be posted in a period, December in this case, the setup that the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="7d3f3-206">Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kenttä, johon on määritetty 1.12., sallii joulukuussa tehdyn uudelleenarvostuksen ohjauksen edelleen saman kauden muuttuneisiin lähteviin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-206">The Allow Posting From in the General Ledger Setup, stating December 1, would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="7d3f3-207">Tässä skenaariossa ollut asetus, jonka mukaan käyttäjäryhmät, jotka eivät voi tehdä kirjauksia joulukuussa, voivat tehdä niitä tammikuussa, kannattaa määrittää käyttäjäasetuksissa pääkirjanpidon asetusten sijaan.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="7d3f3-208">Nimikekulujen skenaario:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-208">Item charge scenario:</span></span>  
 <span data-ttu-id="7d3f3-209">Vaatimukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-209">Prerequisites:</span></span>  

 <span data-ttu-id="7d3f3-210">Varastonhallinnan asetukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-210">Inventory setup:</span></span>  

-   <span data-ttu-id="7d3f3-211">Automaattinen kustannusten kirjaus = Kyllä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="7d3f3-212">Automaattinen kustannusten muuttaminen = Aina</span><span class="sxs-lookup"><span data-stu-id="7d3f3-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="7d3f3-213">Keskim. kust. laskentatyyppi = Nimike</span><span class="sxs-lookup"><span data-stu-id="7d3f3-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="7d3f3-214">Keskimääräisen kustannuksen jakso = Päivä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="7d3f3-215">Pääkirjanpidon asetukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="7d3f3-216">Ensimm. sallittu kirjauspvm = 1.12.2013</span><span class="sxs-lookup"><span data-stu-id="7d3f3-216">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="7d3f3-217">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="7d3f3-218">Käyttäjäasetukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-218">User Setup:</span></span>  

-   <span data-ttu-id="7d3f3-219">Ensimm. sallittu kirjauspvm = 1.12.2013</span><span class="sxs-lookup"><span data-stu-id="7d3f3-219">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="7d3f3-220">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="7d3f3-221">Skenaarion testaaminen</span><span class="sxs-lookup"><span data-stu-id="7d3f3-221">To test the scenario</span></span>  

1.  <span data-ttu-id="7d3f3-222">Luo nimikekulu:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-222">Create item charge:</span></span>  

     <span data-ttu-id="7d3f3-223">Perusmittayksikkö = Kpl</span><span class="sxs-lookup"><span data-stu-id="7d3f3-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="7d3f3-224">Arvostusmenetelmä = Keskiarvo</span><span class="sxs-lookup"><span data-stu-id="7d3f3-224">Costing Method = Average</span></span>  

     <span data-ttu-id="7d3f3-225">Valitse vaihtoehtoiset kirjausryhmät.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="7d3f3-226">Luo uusi ostotilaus</span><span class="sxs-lookup"><span data-stu-id="7d3f3-226">Create new purchase order</span></span>  

     <span data-ttu-id="7d3f3-227">Tavarantoimittajan nro: 10 000</span><span class="sxs-lookup"><span data-stu-id="7d3f3-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="7d3f3-228">Kirjauspäivämäärä = 15.12.2013</span><span class="sxs-lookup"><span data-stu-id="7d3f3-228">Posting Date = December 15, 2013</span></span>  

     <span data-ttu-id="7d3f3-229">Toimittajan laskunro: 1 234</span><span class="sxs-lookup"><span data-stu-id="7d3f3-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="7d3f3-230">Ostotilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-230">On the purchase order line:</span></span>  

     <span data-ttu-id="7d3f3-231">Nimike = KULU</span><span class="sxs-lookup"><span data-stu-id="7d3f3-231">Item = CHARGE</span></span>  

     <span data-ttu-id="7d3f3-232">Määrä = 1</span><span class="sxs-lookup"><span data-stu-id="7d3f3-232">Quantity = 1</span></span>  

     <span data-ttu-id="7d3f3-233">Välitön yksikkökustannus = 100</span><span class="sxs-lookup"><span data-stu-id="7d3f3-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="7d3f3-234">Kirjaa vastaanottaminen ja lasku.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="7d3f3-235">Luo uusi myyntitilaus:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-235">Create new sales order:</span></span>  

     <span data-ttu-id="7d3f3-236">Tilausasiakkaan nro: 10000</span><span class="sxs-lookup"><span data-stu-id="7d3f3-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="7d3f3-237">Kirjauspäivämäärä = 16.12.2013</span><span class="sxs-lookup"><span data-stu-id="7d3f3-237">Posting Date = December 16, 2013</span></span>  

     <span data-ttu-id="7d3f3-238">Myytitilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-238">On the sales order line:</span></span>  

     <span data-ttu-id="7d3f3-239">Nimike = KULU</span><span class="sxs-lookup"><span data-stu-id="7d3f3-239">Item = CHARGE</span></span>  

     <span data-ttu-id="7d3f3-240">Määrä = 1</span><span class="sxs-lookup"><span data-stu-id="7d3f3-240">Quantity = 1</span></span>  

     <span data-ttu-id="7d3f3-241">Yksikköhinta = 135</span><span class="sxs-lookup"><span data-stu-id="7d3f3-241">Unit Price = 135</span></span>  

     <span data-ttu-id="7d3f3-242">Kirjaa toimitus ja lasku.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="7d3f3-243">Pääkirjanpidon asetukset:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="7d3f3-244">Ensimm. sallittu kirjauspvm = 1.1.2014</span><span class="sxs-lookup"><span data-stu-id="7d3f3-244">Allow Posting From = January 1, 2014</span></span>  

     <span data-ttu-id="7d3f3-245">Viimeinen sallittu kirjauspvm = tyhjä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="7d3f3-246">Luo uusi ostotilaus:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-246">Create new purchase order:</span></span>  

     <span data-ttu-id="7d3f3-247">Tavarantoimittajan nro: 10 000</span><span class="sxs-lookup"><span data-stu-id="7d3f3-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="7d3f3-248">Kirjauspäivämäärä = 2.1.2014</span><span class="sxs-lookup"><span data-stu-id="7d3f3-248">Posting Date = January 2, 2014</span></span>  

     <span data-ttu-id="7d3f3-249">Toimittajan laskunro: 2 345</span><span class="sxs-lookup"><span data-stu-id="7d3f3-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="7d3f3-250">Ostotilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-250">On the purchase order line:</span></span>  

     <span data-ttu-id="7d3f3-251">Nimikekulu = JB-RAHTI</span><span class="sxs-lookup"><span data-stu-id="7d3f3-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="7d3f3-252">Määrä = 1</span><span class="sxs-lookup"><span data-stu-id="7d3f3-252">Quantity = 1</span></span>  

     <span data-ttu-id="7d3f3-253">Välitön yksikkökustannus = 3</span><span class="sxs-lookup"><span data-stu-id="7d3f3-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="7d3f3-254">Määritä nimikekuluksi ostovastaanotto vaiheesta 2.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="7d3f3-255">Kirjaa vastaanotto ja lasku.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="7d3f3-256">![Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 3](media/helene/TechArticleAdjustcost11.png "Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 3")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="7d3f3-257">Ostolasku saapuu käsittelypäivänä 3.1. Ostolasku sisältää vaiheessa 2 ostoon tehdyn lisäkulun.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-257">On work date January 3, a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="7d3f3-258">Tämän laskun asiakirjan päivämäärä on 30.12. Tämän vuoksi sen kirjauspäivämääräksi tulee 30.12.2013.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-258">This invoice has document date December 30 and is therefore posted with Posting Date December 30, 2013.</span></span>  

     <span data-ttu-id="7d3f3-259">Luo uusi ostotilaus:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-259">Create new purchase order:</span></span>  

     <span data-ttu-id="7d3f3-260">Tavarantoimittajan nro: 10 000</span><span class="sxs-lookup"><span data-stu-id="7d3f3-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="7d3f3-261">Kirjauspäivämäärä = 30.12.2013</span><span class="sxs-lookup"><span data-stu-id="7d3f3-261">Posting Date = December 30, 2013</span></span>  

     <span data-ttu-id="7d3f3-262">Toimittajan laskunro: 3 456</span><span class="sxs-lookup"><span data-stu-id="7d3f3-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="7d3f3-263">Ostotilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-263">On the purchase order line:</span></span>  

     <span data-ttu-id="7d3f3-264">Nimikekulu = JB-RAHTI</span><span class="sxs-lookup"><span data-stu-id="7d3f3-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="7d3f3-265">Määrä = 1</span><span class="sxs-lookup"><span data-stu-id="7d3f3-265">Quantity = 1</span></span>  

     <span data-ttu-id="7d3f3-266">Välitön yksikkökustannus = 2</span><span class="sxs-lookup"><span data-stu-id="7d3f3-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="7d3f3-267">Määritä nimikekuluksi ostovastaanotto vaiheesta 2</span><span class="sxs-lookup"><span data-stu-id="7d3f3-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="7d3f3-268">Kirjaa vastaanotto ja lasku.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="7d3f3-269">![Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 4](media/helene/TechArticleAdjustcost12.png "Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 4")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="7d3f3-270">Varaston arvostus -raportti tulostetaan 31.12.2013.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-270">Inventory Valuation report is printed as of Date December 31 , 2013</span></span>  

<span data-ttu-id="7d3f3-271">![Varaston arvostusraportin sisältö](media/helene/TechArticleAdjustcost13.png "Varaston arvostusraportin sisältö")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="7d3f3-272">**Skenaarion yhteenveto:**</span><span class="sxs-lookup"><span data-stu-id="7d3f3-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="7d3f3-273">Kuvattu skenaario loppuu Varaston arvostus -raporttiin, jossa määrä = 0 ja arvo = 2.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="7d3f3-274">Vaiheessa 11 kirjattu nimikekulu on osa varaston arvon nousua joulukuussa. Saman kauden varaston arvon lasku ei ole muuttunut.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="7d3f3-275">Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvo 1.1. on sopiva ensimmäiselle nimikekululle.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-275">Having the General Ledger Setup stating Allow Posting From January 1 was a good thing for the first Item charge.</span></span> <span data-ttu-id="7d3f3-276">Varaston arvon nousun ja laskun kustannukset tallennettiin samaan kauteen.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="7d3f3-277">Pääkirjanpidon asetusten vuoksi toinen nimikekulu aiheuttaa kuitenkin muutoksen myytyjen tuotteiden kustannuksessa. Muutos otetaan huomioon seuraavan kauden aikana.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="7d3f3-278">**Yhteenveto.**</span><span class="sxs-lookup"><span data-stu-id="7d3f3-278">**Conclusion:**</span></span>  

 <span data-ttu-id="7d3f3-279">On haastavaa, kun Varaston arvostus -raportissa määritetään, että määrä = 0 samalla, kun arvo <> 0.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="7d3f3-280">Tässä tapauksessa on vaikeaa kertoa optimaaliset asetukset, koska ostolaskut saapuvat samana päivänä mutta ne koskevat eri kausia tai jopa eri tilivuosia.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="7d3f3-281">Uuteen tilivuoteen siirtäminen vaatii yleensä suunnittelua. Muuta kustannuksia - Nimiketapahtumat -prosessin on myös otettava huomioon myytyjen tuotteiden kustannukset.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="7d3f3-282">Tässä skenaariossa eräs vaihtoehto olisi ollut määrittää pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvoksi muutamaa päivää aikaisempi joulukuun päivämäärä ja kirjata ensimmäinen nimikekulu viiveellä, jolloin edellisen kauden/tilivuoden kaikki kustannukset tuloutettaisiin kaudelle, jolle ne alussa kuuluivat. Tämän jälkeen suoritettaisiin Muuta kustannuksia - Nimiketapahtumat -eräajo ja siirrettäisiin sallittu kirjauspäivämäärä seuraavaan kauteen\/tilivuoteen.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="7d3f3-283">Kirjatuksi olisi tullut ensimmäinen nimikekulu, jonka kirjauspäivämäärä on 2.1.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-283">The first item charge with posting date January 2 could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="7d3f3-284">Muuta kustannuksia - Nimiketapahtumat -eräajon historia</span><span class="sxs-lookup"><span data-stu-id="7d3f3-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="7d3f3-285">Alla on Muuta kustannuksia - Nimiketapahtumat -eräajon muutoksen arvotapahtumien kirjauspäivämäärien määrittämisen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job.</span></span>  

### <a name="about-the-request-form-posting-date"></a><span data-ttu-id="7d3f3-286">Tietoja pyyntölomakkeen kirjauspäivämäärästä:</span><span class="sxs-lookup"><span data-stu-id="7d3f3-286">About the request form posting date:</span></span>  
 <span data-ttu-id="7d3f3-287">Muuta kustannuksia - Nimiketapahtumat -eräajon pyyntölomakkeessa ei ole enää ilmoitettavaa kirjauspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-287">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="7d3f3-288">Eräajo käy läpi kaikki pakolliset muutokset ja luo arvotapahtumat, joilla on sen arvotapahtuman kirjauspäivämäärä, jonka eräajo muuttaa.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-288">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="7d3f3-289">Jos kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, käytetään pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä tai mahdollisesti käytössä olevien varastokausien kirjauspäivämäärää sen mukaan, kumpi on myöhempi.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-289">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="7d3f3-290">Katso edellä kuvattua käsitettä.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-290">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="7d3f3-291">Kirjaa varaston kustannukset kirjanpitoon -eräajon historia</span><span class="sxs-lookup"><span data-stu-id="7d3f3-291">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="7d3f3-292">Kirjaa varaston kustannukset kirjanpitoon -eräajo liittyy läheisesti Muuta kustannuksia - Nimiketapahtumat -eräajoon. Tämän vuoksi kyseisen eräajon historiasta tehdään yhteenveto, joka jaetaan myös täällä.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-292">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  
 
<span data-ttu-id="7d3f3-293">![Todelliset kustannukset vs. oletetut kustannukset](media/helene/TechArticleAdjustcost14.png "Todelliset kustannukset vs. oletetut kustannukset")</span><span class="sxs-lookup"><span data-stu-id="7d3f3-293">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="about-the-posting-date"></a><span data-ttu-id="7d3f3-294">Tietoja kirjauspäivämäärästä</span><span class="sxs-lookup"><span data-stu-id="7d3f3-294">About the posting date</span></span>
 <span data-ttu-id="7d3f3-295">Kirjaa varaston kustannukset kirjanpitoon -eräajon pyyntölomakkeessa ei ole enää ilmoitettavaa kirjauspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-295">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="7d3f3-296">Luodaan KP-tapahtuma, jolla on sama kirjauspäivämäärä kuin liittyvällä arvotapahtumalla.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-296">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="7d3f3-297">Jotta eräajo voidaan suorittaa, sallitun kirjauspäivämääräalueen on sallittava luodun KP-tapahtuman kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-297">In order to complete the batch job, the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="7d3f3-298">Muussa tapauksessa sallittu kirjauspäivämääräalue on avattava uudelleen tilapäisesti joko muuttamalla päivämääriä tai poistamalla niitä pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm- ja Viimeinen sallittu kirjauspvm -kentissä.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-298">If not, the allowed posting date range must be temporarily reopened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="7d3f3-299">Vältät täsmäytysongelmat, kun KP-tapahtuman kirjauspäivämäärä vastaa arvotapahtuman kirjauspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-299">To avoid reconciliation issues, it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="7d3f3-300">Kirjaa arvotapahtuma kirjanpitoon -eräajo skannaa taulukon 5811 ja tunnistaa alueeseen kuuluvat arvotapahtumat pääkirjanpitoon kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-300">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="7d3f3-301">Kun eräajo on suoritettu, taulukko tyhjennetään.</span><span class="sxs-lookup"><span data-stu-id="7d3f3-301">After a successful run, the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d3f3-302">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7d3f3-302">See Also</span></span>  
[<span data-ttu-id="7d3f3-303">Rakennetiedot: Varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="7d3f3-303">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="7d3f3-304">Rakennetiedot: Nimikkeen kohdistus</span><span class="sxs-lookup"><span data-stu-id="7d3f3-304">Design Details: Item Application</span></span>](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
