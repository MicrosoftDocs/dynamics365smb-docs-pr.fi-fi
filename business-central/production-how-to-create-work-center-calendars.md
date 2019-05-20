---
title: Tuotantokalenterien määrittäminen | Microsoft Docs
description: 'Tuotantosolun kalenterissa määritetään työpäivät ja -tunnit, työvuorot, lomapäivät sekä poissaolot, jotka määräävät tuotantosolun käytettävissä olevan kokonaiskapasiteetin (ajassa mitattuna) solun tehokkuus- ja kapasiteettiarvojen mukaisesti. Tuotantosolun kalenterin luominen ja käyttöönotto edellyttävät useita valmistelutoimenpiteitä:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0db2bd47c9581e1dc0aa052d03d3170b7796cd39
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253537"
---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="803e9-104">Tuotantokalentereiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="803e9-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="803e9-105">Tuotantosolun tai kuormituskeskuksen kalenterissa määritetään työpäivät ja -tunnit, työvuorot, lomapäivät sekä poissaolot, jotka määräävät tuotantosolun tai kuormituskeskuksen käytettävissä olevan kokonaiskapasiteetin (ajassa mitattuna) tehokkuus- ja kapasiteettiarvojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="803e9-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="803e9-106">Tuotantosolun tai kuormituskeskuksen kalenterin laskemisen perustaksi on ensin määritettävä ainakin yksi yleinen tuotantokalenteri.</span><span class="sxs-lookup"><span data-stu-id="803e9-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="803e9-107">Tuotantokalenteriin määritetään vakiotyöviikon kunkin työpäivän alkamis- ja päättymisajat sekä työvuorot.</span><span class="sxs-lookup"><span data-stu-id="803e9-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="803e9-108">Lisäksi tuotantokalenteriin määritetään kaikki vuoden kiinteät lomapäivät.</span><span class="sxs-lookup"><span data-stu-id="803e9-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="803e9-109">Seuraavaksi käsitellään tuotantosolun kalenterien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="803e9-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="803e9-110">Kuormitusryhmän kalenterit määritetään vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="803e9-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="803e9-111">Työvuorojen luominen</span><span class="sxs-lookup"><span data-stu-id="803e9-111">To create work shifts</span></span>  
1.  <span data-ttu-id="803e9-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työvuorot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="803e9-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="803e9-113">Anna tyhjälle riville **Koodi**-kenttään numero työvuoron tunnisteeksi (esimerkiksi **1**).</span><span class="sxs-lookup"><span data-stu-id="803e9-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="803e9-114">Kirjoita työvuoron kuvaus **Kuvaus**-kenttään, esimerkiksi **1. vuoro**.</span><span class="sxs-lookup"><span data-stu-id="803e9-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="803e9-115">Voit täyttää myös toisen tai kolmannen työvuoron rivit.</span><span class="sxs-lookup"><span data-stu-id="803e9-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="803e9-116">Vaikka tuotantosolussa ei työskenneltäisi eri vuoroissa, syötä ainakin yksi työvuoron koodin.</span><span class="sxs-lookup"><span data-stu-id="803e9-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="803e9-117">Tuotantokalenterin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="803e9-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="803e9-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotantokalenterit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="803e9-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="803e9-119">Anna tyhjälle riville **Koodi**-kenttään numero tuotantokalenterin tunnisteeksi (esimerkiksi 1).</span><span class="sxs-lookup"><span data-stu-id="803e9-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="803e9-120">Kirjoita tuotantokalenterin kuvaus **Kuvaus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="803e9-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="803e9-121">Valitse **Työpäivät**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="803e9-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="803e9-122">Määritä **Tuotantokalenterin työpäivät** -sivulla koko työviikko sekä kunkin päivän alkamis- ja päättymisaika.</span><span class="sxs-lookup"><span data-stu-id="803e9-122">On the **Shop Calendar Working Days** page, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="803e9-123">Valitse **Työvuoron koodi** -kentässä jokin työvuoro, jonka olet määrittänyt aiemmin.</span><span class="sxs-lookup"><span data-stu-id="803e9-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="803e9-124">Lisää rivi jokaiselle työpäivälle ja jokaiselle vuorolle.</span><span class="sxs-lookup"><span data-stu-id="803e9-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="803e9-125">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="803e9-125">For example:</span></span>  

    <span data-ttu-id="803e9-126">Maanantai 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="803e9-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="803e9-127">Tiistai 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="803e9-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="803e9-128">Jos tarvitaan tuotantokalenteri, jossa on kaksi työvuoroa, annetaan tiedot seuraavan esimerkin mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="803e9-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="803e9-129">Maanantai 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="803e9-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="803e9-130">Maanantai 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="803e9-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="803e9-131">Tiistai 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="803e9-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="803e9-132">Tiistai 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="803e9-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="803e9-133">Viikonpäivät, joita ei määritetä tuotantokalenteriin (esimerkiksi lauantai ja sunnuntai) tulkitaan ei-työpäiviksi, ja niiden käytettävissä oleva kapasiteetti on tuotantosolun kalenterissa nolla.</span><span class="sxs-lookup"><span data-stu-id="803e9-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="803e9-134">Kun viikon kaikki työpäivät on määritetty, voit sulkea **Tuotantokalenterin työpäivät** -sivun ja antaa sitten lomapäivät.</span><span class="sxs-lookup"><span data-stu-id="803e9-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** page and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="803e9-135">Valitse **Tuotantokalenterit**-sivulla ensin tuotantokalenteri ja sitten **Lomapäivät**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="803e9-135">On the **Shop Calendars** page, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="803e9-136">Määritä **Tuotantokalenterin lomapäivät** -sivulla vuoden kaikki lomapäivät antamalla kunkin loman alkamispäivämäärä ja -aika sekä päättymispäivämäärä ja -aika omille riveilleen.</span><span class="sxs-lookup"><span data-stu-id="803e9-136">On the **Shop Calendar Holidays** page, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="803e9-137">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="803e9-137">For example:</span></span>  

    <span data-ttu-id="803e9-138">04.07.04 0:00:00 23:59:00 Kesäloma</span><span class="sxs-lookup"><span data-stu-id="803e9-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="803e9-139">05.07.14 0:00:00 23:59:00 Kesäloma</span><span class="sxs-lookup"><span data-stu-id="803e9-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="803e9-140">06.07.14 0:00:00 23:59:00 Kesäloma</span><span class="sxs-lookup"><span data-stu-id="803e9-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="803e9-141">Määritettyinä lomapäivinä tuotantosolun kalenterin käytettävissä oleva kapasiteetti on nolla.</span><span class="sxs-lookup"><span data-stu-id="803e9-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="803e9-142">Tuotantokalenteri voidaan nyt liittää tuotantosoluun, ja tuotantosolun kalenteri voidaan laskea. Tuotantosolun kalenteri ohjaa kaikkien toimintojen aikataulutusta kyseisessä tuotantosolussa.</span><span class="sxs-lookup"><span data-stu-id="803e9-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="803e9-143">Tuotantosolun kalenterin laskeminen</span><span class="sxs-lookup"><span data-stu-id="803e9-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="803e9-144">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työkeskukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="803e9-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="803e9-145">Avaa tuotantosolu, jonka haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="803e9-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="803e9-146">Valitse **Tuotantokalenterin koodi** -kentässä, mitä tuotantokalenteria käytetään tuotantosolun kalenterin pohjana.</span><span class="sxs-lookup"><span data-stu-id="803e9-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="803e9-147">Valitse **Kalenteri**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="803e9-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="803e9-148">Valitse **Tuotantosolun kalenteri** -sivulla **Näytä matriisi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="803e9-148">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="803e9-149">Matriisisivun vasemmassa reunassa on kaikkien määritettyjen tuotantosolujen luettelo.</span><span class="sxs-lookup"><span data-stu-id="803e9-149">The left side of the matrix page lists the work centers that are set up.</span></span> <span data-ttu-id="803e9-150">Oikeassa reunassa on kalenteri, jossa näkyvät käytettävissä olevat kapasiteettiarvot työpäivittäin määritettynä mittayksikkönä, esimerkiksi **480** (minuuttia).</span><span class="sxs-lookup"><span data-stu-id="803e9-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="803e9-151">Kukin rivi edustaa yhden tuotantosolun kalenteria.</span><span class="sxs-lookup"><span data-stu-id="803e9-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="803e9-152">Voit tarkastella myös viikko- tai kuukausikohtaisia kapasiteettiarvoja muuttamalla valintaa **Tuotantosolun kalenteri** -sivun **Näyttöperuste**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="803e9-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field on the **Work Center Calendar** page.</span></span>  

    <span data-ttu-id="803e9-153">Ilmaistaksesi, että uusi tuotantokalenterin rivi on valitussa tuotantosolussa, se on ensin laskettava.</span><span class="sxs-lookup"><span data-stu-id="803e9-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="803e9-154">Valitse **Laske**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="803e9-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="803e9-155">**Tuotantosolu**-pikavälilehdessä voidaan asettaa suodatin niin, että järjestelmä laskee vain yhden tuotantosolun kalenterin.</span><span class="sxs-lookup"><span data-stu-id="803e9-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="803e9-156">Jos laskentaa ei suodateta, järjestelmä laskee kaikki tuotantosolujen kalenterit.</span><span class="sxs-lookup"><span data-stu-id="803e9-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="803e9-157">Määritä laskettavan kalenterijakson alkamis- ja päättymispäivämäärät, esimerkiksi yksi vuosi 1.1.2014-31.12.2014.</span><span class="sxs-lookup"><span data-stu-id="803e9-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="803e9-158">Laske kapasiteetti valitsemalla **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="803e9-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="803e9-159">Järjestelmä luo (tai päivittää) kalenteritapahtumat, joista näkyy käytettävissä oleva päivittäinen (tai muun jakson mukainen) kapasiteetti seuraavan kolmen perustietojoukon mukaan:</span><span class="sxs-lookup"><span data-stu-id="803e9-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="803e9-160">Tuotantokalenterissa määritetyt työpäivät ja -vuorot</span><span class="sxs-lookup"><span data-stu-id="803e9-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="803e9-161">tuotantosolukortin **Kapasiteetti**-kentän arvo</span><span class="sxs-lookup"><span data-stu-id="803e9-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="803e9-162">tuotantosolukortin **Tehokkuus**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="803e9-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="803e9-163">Laskettu tuotantosolun kalenteri määrittelee nyt, milloin ja kuinka paljon kapasiteettia on saatavilla tässä tuotantosolussa.</span><span class="sxs-lookup"><span data-stu-id="803e9-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="803e9-164">Tämä ohjaa tuotantosolussa suoritettavaa toimintojen yksityiskohtaista aikataulutusta.</span><span class="sxs-lookup"><span data-stu-id="803e9-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="803e9-165">Tuotantosolun poissaolojen tallentaminen</span><span class="sxs-lookup"><span data-stu-id="803e9-165">To record work center absence</span></span>  
1.  <span data-ttu-id="803e9-166">Valitse **Tuotantosolun kalenteri** -sivulla **Näytä matriisi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="803e9-166">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="803e9-167">Valitse **Tuotantosolun kalenterimatriisi** -sivulla tuotantosolu ja kalenteripäivä, jolle poissaolo halutaan merkitä, ja valitse sitten **Poissaolo**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="803e9-167">On the **Work Center Calendar Matrix** page, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="803e9-168">Määritä **Poissaolo**-sivulla poissaolon alkamis- ja päättymisaika kyseisenä päivänä sekä poissaolon kuvaus esimerkiksi seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="803e9-168">On the **Absence** page, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="803e9-169">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="803e9-169">For example:</span></span>  

    <span data-ttu-id="803e9-170">25.01.01 08:00 10:00 Huolto</span><span class="sxs-lookup"><span data-stu-id="803e9-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="803e9-171">Valitse ensin **Päivitä**-toiminto ja sulje sitten **Poissaolo**-sivu.</span><span class="sxs-lookup"><span data-stu-id="803e9-171">Choose the **Update** action, and then close the **Absence** page.</span></span>  

<span data-ttu-id="803e9-172">Valitun päivän kapasiteetti on nyt pienentynyt kalenteriin merkityn poissaoloajan verran.</span><span class="sxs-lookup"><span data-stu-id="803e9-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="803e9-173">Katso myös</span><span class="sxs-lookup"><span data-stu-id="803e9-173">See Also</span></span>  
[<span data-ttu-id="803e9-174">Peruskalenterien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="803e9-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="803e9-175">Tuotantosolujen ja kuormituskeskusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="803e9-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="803e9-176">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="803e9-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="803e9-177">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="803e9-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="803e9-178">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="803e9-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
