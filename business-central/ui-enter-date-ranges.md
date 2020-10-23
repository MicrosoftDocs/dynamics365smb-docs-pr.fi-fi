---
title: Päivämäärien ja aikojen syöttäminen Business Central -sovelluksessa | Microsoft Docs
description: Tietoja päivämäärien ja aikojen syöttämisestä sekä erilaisista tuottavuutta lisäävistä vihjeistä, jotka liittyvät esimerkiksi pikakirjoitukseen, lausekkeisiin ja alueisiin. Suodata luettelot tai raportit tiettyyn päivämäärään tai tiettyihin ajanjaksoihin.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f658764eafa6f9aa35e33cf8098ca77799fb1e0c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912469"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="0337a-104">Kalenterin päivämäärien ja aikojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="0337a-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="0337a-105">sisältää useita tapoja päivämäärien ja aikojen syöttämiseen sekä tehokkaita toimintoja, jotka nopeuttavat tietojen syöttämistä ja helpottavat monimutkaisten kalenterilausekkeiden kirjoittamista.</span><span class="sxs-lookup"><span data-stu-id="0337a-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="0337a-106">Sovelluksessa on useita kohtia, joissa voi syöttää päivämääriä ja aikoja kenttiin.</span><span class="sxs-lookup"><span data-stu-id="0337a-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="0337a-107">Esimerkiksi myyntitilauksessa voi määrittää lähetyspäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="0337a-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="0337a-108">Voit syöttää päivämäärät ja ajat luetteloiden tai raportin tietojen suodattamisen yhteydessä ja etsiä vain tiedot, joista olet kiinnostunut.</span><span class="sxs-lookup"><span data-stu-id="0337a-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="0337a-109">Alueen ja kielen asetusten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="0337a-109">Check your region and language settings</span></span>
<span data-ttu-id="0337a-110">**Omat asetukset** -sivulla määritetään sovelluksessa käytettävä **alue** ja **kieli**.</span><span class="sxs-lookup"><span data-stu-id="0337a-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="0337a-111">Nämä asetukset vaikuttavat päivämäärien ja aikojen syöttötapaan.</span><span class="sxs-lookup"><span data-stu-id="0337a-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="0337a-112">**Alue**-asetus määrittää, miten päivämäärät, ajat, luvut ja valuutat näkyvät tai miten ne on muotoiltu.</span><span class="sxs-lookup"><span data-stu-id="0337a-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="0337a-113">Jos päivämäärämallit sisältävät sanoja, sanojen kielen on oltava **Kieli**-asetuksessa määritetty kieli.</span><span class="sxs-lookup"><span data-stu-id="0337a-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="0337a-114">käyttää gregoriaanista kalenterijärjestelmää.</span><span class="sxs-lookup"><span data-stu-id="0337a-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="0337a-115">Päivämäärien syöttäminen</span><span class="sxs-lookup"><span data-stu-id="0337a-115">Entering Dates</span></span>

<span data-ttu-id="0337a-116">Voit syöttää päivämääräkenttään päivämäärän alueasetuksen vakiomuodossa.</span><span class="sxs-lookup"><span data-stu-id="0337a-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="0337a-117">Eri alueilla voidaan käyttää päivien, kuukausien ja vuosien välillä erilaisia erottimia.</span><span class="sxs-lookup"><span data-stu-id="0337a-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="0337a-118">Esimerkiksi joillakin alueilla käytetään ajatusviivoja (kk-pp-vvvv) ja toisilla alueilla vinoviivoja (kk/pp/vvvv).</span><span class="sxs-lookup"><span data-stu-id="0337a-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="0337a-119">Voit kuitenkin käyttää mitä tahansa erottimia, jopa välilyöntiä. Päivämäärää muutetaan automaattisesti niin, että se sisältää aluettasi vastaavat erottimet.</span><span class="sxs-lookup"><span data-stu-id="0337a-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="0337a-120">Huomaa, että oma alueasetuksesi ei vaikuta päivämäärän näyttömuotoon tulostetuissa raporteissa ja sähköpostitse lähetetyissä asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="0337a-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="0337a-121">Seuraavissa osissa esiteltyjen menetelmien ja muotojen avulla voit käyttää päivämääriä ja aikoja tuottavammin.</span><span class="sxs-lookup"><span data-stu-id="0337a-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="0337a-122">Päivämäärien valitseminen kalenterista</span><span class="sxs-lookup"><span data-stu-id="0337a-122">Picking dates from the calendar</span></span>

<span data-ttu-id="0337a-123">Mitä tahansa kalenterikuvakkeen sisältävä kenttä voidaan määrittää kalenterin päivämäärän valitsimen avulla.</span><span class="sxs-lookup"><span data-stu-id="0337a-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="0337a-124">Voit näyttää kalenterin päivämäärän valitsimen aktivoimalla kalenterikuvakkeen tai painamalla kentässä pikanäppäimiä Ctrl + Home.</span><span class="sxs-lookup"><span data-stu-id="0337a-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="0337a-125">![Pvm-kentät](media/ui-date-field.png "Esimerkki päivämääräkentästä")</span><span class="sxs-lookup"><span data-stu-id="0337a-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="0337a-126">Katso myös [Kalenterin päivämäärän valitsimen pikanäppäimet](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="0337a-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="0337a-127">Päivä\-viikko\-vuosi-malli</span><span class="sxs-lookup"><span data-stu-id="0337a-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="0337a-128">Voit syöttää päivämäärän viikonpäivänä, jonka jälkeen tulee viikon numero ja halutessasi vuosi.</span><span class="sxs-lookup"><span data-stu-id="0337a-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="0337a-129">Esimerkiksi Ma25 tai ma25 tarkoittaa viikon 25 maanantaita.</span><span class="sxs-lookup"><span data-stu-id="0337a-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="0337a-130">Jos et syötä vuotta, käytetään käsittelypäivämäärän vuotta.</span><span class="sxs-lookup"><span data-stu-id="0337a-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="0337a-131">Sen sijaan, että syötät koko sanan viikonpäivää varten, voit syöttää sanan alkuosan.</span><span class="sxs-lookup"><span data-stu-id="0337a-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="0337a-132">Ristiriitatilanteissa, esimerkiksi kun s voi tarkoittaa sekä lauantaita (Saturday) tai sunnuntaita (Sunday), päivät arvioidaan alueasetuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0337a-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="0337a-133">Syöte arvioidaan ensin käsittelypäivämäärä- ja tänään-määritteiden avulla. Pidä tämä mielessä, kun lyhennät sanoja.</span><span class="sxs-lookup"><span data-stu-id="0337a-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="0337a-134">Esimerkiksi t merkitsee jo tämän päivän päivämäärää, joten se ei voi tarkoittaa tiistaita tai torstaita.</span><span class="sxs-lookup"><span data-stu-id="0337a-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="0337a-135">Viikon numeromalli on aina ISO 8601, jossa viikko 1 on viikko, joka sisältää tammikuun 4. päivän tai vuoden ensimmäisen torstain.</span><span class="sxs-lookup"><span data-stu-id="0337a-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="0337a-136">Numeromallit</span><span class="sxs-lookup"><span data-stu-id="0337a-136">Digit patterns</span></span>

<span data-ttu-id="0337a-137">Päivämäärä-kenttään voi syöttää kaksi, neljä, kuusi tai kahdeksan numeroa:</span><span class="sxs-lookup"><span data-stu-id="0337a-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="0337a-138">Jos syötät vain kaksi numeroa, ohjelma tulkitsee ne kuukaudeksi ja vuodeksi ja lisää käsittelypäivämäärän vuoden.</span><span class="sxs-lookup"><span data-stu-id="0337a-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="0337a-139">Jos syötät neljä numeroa, ohjelma tulkitsee ne päiväksi ja kuukaudeksi ja lisää käsittelypäivämäärän vuoden.</span><span class="sxs-lookup"><span data-stu-id="0337a-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="0337a-140">Päivän ja kuukauden järjestys riippuu alueasetuksista.</span><span class="sxs-lookup"><span data-stu-id="0337a-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="0337a-141">Vaikka alueasetuksissa olisi vuosi ennen päivää ja kuukautta, neljä lukua tulkitaan päiväksi ja kuukaudeksi.</span><span class="sxs-lookup"><span data-stu-id="0337a-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="0337a-142">Jos päivämäärä, jonka haluat syöttää, on välillä 1.1.1930 ja 31.12.2029, voit syöttää vuoden kaksinumeroisena. Muutoin vuosi täytyy syöttää nelinumeroisena.</span><span class="sxs-lookup"><span data-stu-id="0337a-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="0337a-143">Tänään</span><span class="sxs-lookup"><span data-stu-id="0337a-143">Today</span></span>

<span data-ttu-id="0337a-144">Syötä sana today-määritteelle **Kieli**-asetuksen määrittämällä kielellä. Tällöin päivämääräksi tulee nykyinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="0337a-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="0337a-145">Sen sijaan, että syöttäisit koko sanan, voit syöttää sanan alkuosan, kuten t tai tän (sanasta tänään), jos mikään toinen sana ei ala samoilla kirjaimilla.</span><span class="sxs-lookup"><span data-stu-id="0337a-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="0337a-146">Jakso</span><span class="sxs-lookup"><span data-stu-id="0337a-146">Period</span></span>

<span data-ttu-id="0337a-147">Voit suodattaa tietyn kirjanpitojakson antamalla päivämääräkentässä kirjaimen j tai sanan jakso ja lisäämällä sen perään luvun, joka yksilöi kirjanpitojakson, kuten j2 tai jakso4.</span><span class="sxs-lookup"><span data-stu-id="0337a-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="0337a-148">Kirjapitojakso liittyy roolikeskuksessa määritetyn kuluvan käsittelypäivän tilikauteen.</span><span class="sxs-lookup"><span data-stu-id="0337a-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="0337a-149">Jos esimerkiksi käsittelypäivämäärä on **21.3.20**, j1 tai vain j suodattaa tilikauden 2020 ensimmäisen kirjanpitojakson (kuten 01.01.20-31.1.20).</span><span class="sxs-lookup"><span data-stu-id="0337a-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="0337a-150">j15 suodattaa 15:nnen kirjanpitojakson tilikauden 2020 alusta (kuten 1.3.31-31.3.21).</span><span class="sxs-lookup"><span data-stu-id="0337a-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="0337a-151">Kirjanpitojaksot määritetään **Kirjanpitojaksot**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0337a-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="0337a-152">Voit tarkastella tai muuttaa kirjanpitojaksoja avaamalla sivun [täällä](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="0337a-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="0337a-153">Nykyinen käsittelypvm</span><span class="sxs-lookup"><span data-stu-id="0337a-153">Current work date</span></span>

<span data-ttu-id="0337a-154">Käsittelypäivämäärän toiminnon avulla voit tallentaa käännökset muun kuin nykyisen päivämäärän avulla.</span><span class="sxs-lookup"><span data-stu-id="0337a-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="0337a-155">Käsittelypäivämäärä-sana **Kieli**-asetuksen määrittämällä kielellä määrittää nykyisen käsittelypäivämäärän, joka on määritetty **Omat asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0337a-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="0337a-156">Sen sijaan, että syötät koko sanan, voit syöttää sanan alkuosan, esimerkiksi k, kun sana on käsittely.</span><span class="sxs-lookup"><span data-stu-id="0337a-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="0337a-157">Jos et ole määrittänyt käsittelypäivämäärää, nykyistä päivämäärää käytetään käsittelypäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="0337a-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="0337a-158">Haluat ehkä käyttää käsittelypäivämäärää, jos sellaisia tapahtumia on paljon, joissa on jokin muu kuin tämän päivän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="0337a-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="0337a-159">Katso myös [Perusasetusten, kuten käsittelypäivämäärän, muuttaminen](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="0337a-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="0337a-160">Sulkemispvm</span><span class="sxs-lookup"><span data-stu-id="0337a-160">Closing Date</span></span>

<span data-ttu-id="0337a-161">Kun suljet tilikauden, voit käyttää sulkemispäivämääriä osoittaaksesi, että tapahtuma on tilinpäätöstapahtuma.</span><span class="sxs-lookup"><span data-stu-id="0337a-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="0337a-162">Sulkemispäivämäärä sijoittuu teknisesti kahden päivämäärän väliin, esimerkiksi joulukuun 31. päivän ja tammikuun 1. päivän väliin.</span><span class="sxs-lookup"><span data-stu-id="0337a-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="0337a-163">Jos haluat määrittää, että päivämäärä on sulkemispäivämäärä, kirjoita N päivämäärän edelle , esimerkiksi N31.12.01.</span><span class="sxs-lookup"><span data-stu-id="0337a-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="0337a-164">Tätä voidaan käyttää kaikkien päivämäärämallien kanssa.</span><span class="sxs-lookup"><span data-stu-id="0337a-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="0337a-165">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="0337a-165">Examples</span></span>

<span data-ttu-id="0337a-166">Seuraavassa taulukossa on esimerkkejä kaikkia muotoja käyttävistä päivämääristä.</span><span class="sxs-lookup"><span data-stu-id="0337a-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="0337a-167">Oletetaan, että alueasetukset muotoilevat päivämäärät näin: **vuosi.kuukausi.päivä.**, viikko alkaa maanantaista ja kieli on englanti.</span><span class="sxs-lookup"><span data-stu-id="0337a-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="0337a-168">**Tapahtuma**</span><span class="sxs-lookup"><span data-stu-id="0337a-168">**Entry**</span></span>      |<span data-ttu-id="0337a-169">**Tulkinta**</span><span class="sxs-lookup"><span data-stu-id="0337a-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="0337a-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="0337a-170">2018.12.31.</span></span>|<span data-ttu-id="0337a-171">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="0337a-171">2018.12.31.</span></span>|
|<span data-ttu-id="0337a-172">31.12.18</span><span class="sxs-lookup"><span data-stu-id="0337a-172">181231</span></span>|<span data-ttu-id="0337a-173">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="0337a-173">2018.12.31.</span></span>|
|<span data-ttu-id="0337a-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="0337a-174">18.12.31.</span></span>|<span data-ttu-id="0337a-175">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="0337a-175">2018.12.31.</span></span>|
|<span data-ttu-id="0337a-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="0337a-176">18.12.31.</span></span>|<span data-ttu-id="0337a-177">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="0337a-177">2018.12.31.</span></span>|
|<span data-ttu-id="0337a-178">20181231</span><span class="sxs-lookup"><span data-stu-id="0337a-178">20181231</span></span>|<span data-ttu-id="0337a-179">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="0337a-179">2018.12.31.</span></span>|
|<span data-ttu-id="0337a-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="0337a-180">18/12,31</span></span>|<span data-ttu-id="0337a-181">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="0337a-181">2018.12.31.</span></span>|
|<span data-ttu-id="0337a-182">11</span><span class="sxs-lookup"><span data-stu-id="0337a-182">11</span></span>|<span data-ttu-id="0337a-183">käsittelypvm:n vuosi.käsittelypvm:n kuukausi.11.</span><span class="sxs-lookup"><span data-stu-id="0337a-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="0337a-184">11.12</span><span class="sxs-lookup"><span data-stu-id="0337a-184">1112</span></span>|<span data-ttu-id="0337a-185">käsittelypvm:n vuosi.11.12.</span><span class="sxs-lookup"><span data-stu-id="0337a-185">work date year.11.12.</span></span>|
|<span data-ttu-id="0337a-186">t tai tänään</span><span class="sxs-lookup"><span data-stu-id="0337a-186">t or today</span></span>|<span data-ttu-id="0337a-187">tämän päivän päivämäärä</span><span class="sxs-lookup"><span data-stu-id="0337a-187">today's date</span></span>|
|<span data-ttu-id="0337a-188">j4</span><span class="sxs-lookup"><span data-stu-id="0337a-188">p4</span></span>|<span data-ttu-id="0337a-189">päivämääräalue, joka sisältää neljännen kirjanpitojakson, kuten 1.4.20-30.4.20</span><span class="sxs-lookup"><span data-stu-id="0337a-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="0337a-190">k tai käsittelypvm</span><span class="sxs-lookup"><span data-stu-id="0337a-190">w or workdate</span></span>|<span data-ttu-id="0337a-191">käsittelypvm</span><span class="sxs-lookup"><span data-stu-id="0337a-191">the working date</span></span>|
|<span data-ttu-id="0337a-192">ma tai maanantai</span><span class="sxs-lookup"><span data-stu-id="0337a-192">m or Monday</span></span>|<span data-ttu-id="0337a-193">Käsittelypvm:n viikon maanantai</span><span class="sxs-lookup"><span data-stu-id="0337a-193">Monday of the work date week</span></span>|
|<span data-ttu-id="0337a-194">ti tai tiistai</span><span class="sxs-lookup"><span data-stu-id="0337a-194">tu or Tuesday</span></span>|<span data-ttu-id="0337a-195">Käsittelypvm:n viikon tiistai</span><span class="sxs-lookup"><span data-stu-id="0337a-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="0337a-196">la tai lauantai</span><span class="sxs-lookup"><span data-stu-id="0337a-196">sa or Saturday</span></span>|<span data-ttu-id="0337a-197">Käsittelypvm:n viikon lauantai</span><span class="sxs-lookup"><span data-stu-id="0337a-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="0337a-198">su tai sunnuntai</span><span class="sxs-lookup"><span data-stu-id="0337a-198">s or Sunday</span></span>|<span data-ttu-id="0337a-199">Käsittelypvm:n viikon sunnuntai</span><span class="sxs-lookup"><span data-stu-id="0337a-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="0337a-200">t23</span><span class="sxs-lookup"><span data-stu-id="0337a-200">t23</span></span>|<span data-ttu-id="0337a-201">Käsittelypvm:n vuoden viikon 23 tiistai</span><span class="sxs-lookup"><span data-stu-id="0337a-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="0337a-202">t 23</span><span class="sxs-lookup"><span data-stu-id="0337a-202">t 23</span></span>|<span data-ttu-id="0337a-203">Käsittelypvm:n vuoden viikon 23 tiistai</span><span class="sxs-lookup"><span data-stu-id="0337a-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="0337a-204">t-1</span><span class="sxs-lookup"><span data-stu-id="0337a-204">t-1</span></span>|<span data-ttu-id="0337a-205">Käsittelypvm:n vuoden viikon 1 tiistai</span><span class="sxs-lookup"><span data-stu-id="0337a-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="0337a-206">Alueiden asettaminen</span><span class="sxs-lookup"><span data-stu-id="0337a-206">Setting Ranges</span></span>

<span data-ttu-id="0337a-207">Luetteloissa, kokonaissummissa ja raporteissa voi määrittää suodattimia päivämäärille, ajoille sekä päivämäärille ja ajoille, joilla on aloitusarvo ja vaihtoehtoisesti lopetusarvo, jolloin näytetään vain kyseisen alueen tiedot.</span><span class="sxs-lookup"><span data-stu-id="0337a-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="0337a-208">Päivämääräalueiden määrittämisessä käytetään vakiosääntöjä.</span><span class="sxs-lookup"><span data-stu-id="0337a-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="0337a-209">**Merkitys**</span><span class="sxs-lookup"><span data-stu-id="0337a-209">**Meaning**</span></span>|<span data-ttu-id="0337a-210">**Esimerkkilauseke (pvm)**</span><span class="sxs-lookup"><span data-stu-id="0337a-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="0337a-211">**Suodatukseen sisällytettävät tiedot**</span><span class="sxs-lookup"><span data-stu-id="0337a-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="0337a-212">Väli</span><span class="sxs-lookup"><span data-stu-id="0337a-212">Interval</span></span>|<span data-ttu-id="0337a-213">15.12.00-15.1.01</span><span class="sxs-lookup"><span data-stu-id="0337a-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="0337a-214">-15.12.00</span><span class="sxs-lookup"><span data-stu-id="0337a-214">..12 15 00</span></span><br /><br /><span data-ttu-id="0337a-215">j1-j4</span><span class="sxs-lookup"><span data-stu-id="0337a-215">p1..p4</span></span>|<span data-ttu-id="0337a-216">Tietueet, joiden päivämäärät ovat välillä 15.12.00 ja 15.1.01 kyseiset päivät mukaan lukien.</span><span class="sxs-lookup"><span data-stu-id="0337a-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="0337a-217">Tietueet, joiden päivämäärä on 15.12.00 tai aiempi.</span><span class="sxs-lookup"><span data-stu-id="0337a-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="0337a-218">Päivämääräalue, joka sisältää toisen, kolmannen ja neljännen kirjanpitojakson, kuten 1.1.20-30.4.20.</span><span class="sxs-lookup"><span data-stu-id="0337a-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="0337a-219">Joko/tai</span><span class="sxs-lookup"><span data-stu-id="0337a-219">Either/or</span></span>|<span data-ttu-id="0337a-220">12 15 00\|12 16 00</span><span class="sxs-lookup"><span data-stu-id="0337a-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="0337a-221">Tietueet, joiden päivämäärät ovat 15.12.00 tai 16.12.00.</span><span class="sxs-lookup"><span data-stu-id="0337a-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="0337a-222">Myös tietueet, joilla on molemmat päivämäärät, näytetään.</span><span class="sxs-lookup"><span data-stu-id="0337a-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="0337a-223">Yhdistelmä</span><span class="sxs-lookup"><span data-stu-id="0337a-223">Combination</span></span>|<span data-ttu-id="0337a-224">12 15 00\|12 01 00..12 10 00</span><span class="sxs-lookup"><span data-stu-id="0337a-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="0337a-225">..12 14 00\|12 30 00..</span><span class="sxs-lookup"><span data-stu-id="0337a-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="0337a-226">Tietueet, joiden päivämäärät ovat 15.12.00 tai 01.12.00 ja 10.12.00 sekä niiden välisenä aikana.</span><span class="sxs-lookup"><span data-stu-id="0337a-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="0337a-227">Tietueet, joiden päivämäärä on 12 14 00 tai sitä aiempi, tai 12 30 00 tai sitä myöhempi. Toisin sanoen kaikki tietueet paitsi ne, joiden päivämäärä sijoittuu välille 12 15 00 ja 12 29 00 kyseiset päivät mukaan lukien.</span><span class="sxs-lookup"><span data-stu-id="0337a-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="0337a-228">Voit käyttää päivämääräalueiden suodattimissa mitä tahansa sallittua muotoa.</span><span class="sxs-lookup"><span data-stu-id="0337a-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="0337a-229">Jos esimerkiksi päivämäärän ja ajan kentässä käytetään arvoa ma14 3..t 4j, tuloksena on suodatin, joka käsittää aikavälin kuluvan käsittelypäivämäärän vuoden viikon 14 maanantaista kello 3:00 kuluvaan päivään kello 16:00 kyseiset ajankohdat mukaan lukien.</span><span class="sxs-lookup"><span data-stu-id="0337a-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="0337a-230">Päivämäärän kaavojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0337a-230">Using Date Formulas</span></span>
<span data-ttu-id="0337a-231">Päivämäärän kaava on lyhyt kirjain- ja numeroyhdistelmä, joka kertoo ohjelmalle, miten päivämäärät lasketaan.</span><span class="sxs-lookup"><span data-stu-id="0337a-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="0337a-232">Voit syöttää päivämääräkaavat erilaisiin päivämäärien laskentakenttiin ja suodattimiin.</span><span class="sxs-lookup"><span data-stu-id="0337a-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="0337a-233">Kaikissa tietokaavakentissä yksi päivä sisällytetään automaattisesti edustamaan kuluvaa päivää kauden alkupäivänä.</span><span class="sxs-lookup"><span data-stu-id="0337a-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="0337a-234">Jos siis syötät arvoksi esimerkiksi 1K, kausi on kahdeksan päivää, koska tämä päivä lasketaan mukaan.</span><span class="sxs-lookup"><span data-stu-id="0337a-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="0337a-235">Määritä seitsemän päivän kausi \(yksi kokonainen viikko\) sisältäen alkamispäivämäärän ja syötä sitten 6P tai 1K-1P.</span><span class="sxs-lookup"><span data-stu-id="0337a-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="0337a-236">Seuraavassa on joitakin esimerkkejä päivämäärän kaavojen käytöstä:</span><span class="sxs-lookup"><span data-stu-id="0337a-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="0337a-237">Toistuvien päiväkirjojen toistotiheys-kentän päivämäärän kaava määrittää, kuinka usein päiväkirjan rivin tapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="0337a-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="0337a-238">**Ylityskausi**-kentän tietyn tason muistutusta koskeva päivämäärän kaava määrittelee ajanjakson, joka täytyy kulua eräpäivästä \(tai edellisen muistutuksen päivämäärästä\), ennen kuin muistutus voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="0337a-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="0337a-239">**Eräpäivän laskenta** -kentän kaava määrittää, miten ohjelma laskee muistutuksen eräpäivän.</span><span class="sxs-lookup"><span data-stu-id="0337a-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="0337a-240">Päivämäärän kaavassa voi olla enintään 20 merkkiä, sekä numeroita että kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="0337a-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="0337a-241">Voit käyttää seuraavia kirjaimia, jotka ovat kalenteriyksiköiden lyhenteitä:</span><span class="sxs-lookup"><span data-stu-id="0337a-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="0337a-242">Kirjain</span><span class="sxs-lookup"><span data-stu-id="0337a-242">Letter</span></span>  |  <span data-ttu-id="0337a-243">Merkitys</span><span class="sxs-lookup"><span data-stu-id="0337a-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="0337a-244">N</span><span class="sxs-lookup"><span data-stu-id="0337a-244">C</span></span>|<span data-ttu-id="0337a-245">Nykyinen</span><span class="sxs-lookup"><span data-stu-id="0337a-245">Current</span></span>|
|<span data-ttu-id="0337a-246">P</span><span class="sxs-lookup"><span data-stu-id="0337a-246">D</span></span>|<span data-ttu-id="0337a-247">Päivä\(päivät\)</span><span class="sxs-lookup"><span data-stu-id="0337a-247">Day\(s\)</span></span>|
|<span data-ttu-id="0337a-248">VI</span><span class="sxs-lookup"><span data-stu-id="0337a-248">W</span></span>|<span data-ttu-id="0337a-249">Viikko\(viikot\)</span><span class="sxs-lookup"><span data-stu-id="0337a-249">Week\(s\)</span></span>|
|<span data-ttu-id="0337a-250">K</span><span class="sxs-lookup"><span data-stu-id="0337a-250">M</span></span>|<span data-ttu-id="0337a-251">Kuukausi\(kuukaudet\)</span><span class="sxs-lookup"><span data-stu-id="0337a-251">Month\(s\)</span></span>|
|<span data-ttu-id="0337a-252">Q </span><span class="sxs-lookup"><span data-stu-id="0337a-252">Q</span></span>|<span data-ttu-id="0337a-253">Vuosineljännes\(vuosineljännekset\)</span><span class="sxs-lookup"><span data-stu-id="0337a-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="0337a-254">V</span><span class="sxs-lookup"><span data-stu-id="0337a-254">Y</span></span>|<span data-ttu-id="0337a-255">Vuosi\(vuodet\)</span><span class="sxs-lookup"><span data-stu-id="0337a-255">Year\(s\)</span></span>|

<span data-ttu-id="0337a-256">Voit rakentaa päivämääräkaavan kolmella eri tavalla:</span><span class="sxs-lookup"><span data-stu-id="0337a-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="0337a-257">Seuraava esimerkki näyttää, miten käytetään kirjainta N (nykyinen) ja aikayksikköä.</span><span class="sxs-lookup"><span data-stu-id="0337a-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="0337a-258">Lauseke</span><span class="sxs-lookup"><span data-stu-id="0337a-258">Expression</span></span>  |  <span data-ttu-id="0337a-259">Merkitys</span><span class="sxs-lookup"><span data-stu-id="0337a-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0337a-260">NVI</span><span class="sxs-lookup"><span data-stu-id="0337a-260">CW</span></span>|<span data-ttu-id="0337a-261">Nykyinen viikko</span><span class="sxs-lookup"><span data-stu-id="0337a-261">Current week</span></span>|
|<span data-ttu-id="0337a-262">NK</span><span class="sxs-lookup"><span data-stu-id="0337a-262">CM</span></span>|<span data-ttu-id="0337a-263">Nykyinen kuukausi</span><span class="sxs-lookup"><span data-stu-id="0337a-263">Current month</span></span>|

<span data-ttu-id="0337a-264">Seuraava esimerkki näyttää, miten käytetään numeroa ja aikayksikköä.</span><span class="sxs-lookup"><span data-stu-id="0337a-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="0337a-265">Numero ei voi olla suurempi kuin 9999.</span><span class="sxs-lookup"><span data-stu-id="0337a-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="0337a-266">Lauseke</span><span class="sxs-lookup"><span data-stu-id="0337a-266">Expression</span></span>  |  <span data-ttu-id="0337a-267">Merkitys</span><span class="sxs-lookup"><span data-stu-id="0337a-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0337a-268">10P</span><span class="sxs-lookup"><span data-stu-id="0337a-268">10D</span></span>|<span data-ttu-id="0337a-269">10 päivää tästä päivästä</span><span class="sxs-lookup"><span data-stu-id="0337a-269">10 days from today</span></span>|
|<span data-ttu-id="0337a-270">2VI</span><span class="sxs-lookup"><span data-stu-id="0337a-270">2W</span></span>|<span data-ttu-id="0337a-271">2 viikkoa tämän päivän jälkeen</span><span class="sxs-lookup"><span data-stu-id="0337a-271">2 weeks from today</span></span>|

<span data-ttu-id="0337a-272">Seuraava esimerkki näyttää, miten käytetään aikayksikköä ja numeroa.</span><span class="sxs-lookup"><span data-stu-id="0337a-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="0337a-273">Lauseke</span><span class="sxs-lookup"><span data-stu-id="0337a-273">Expression</span></span>  |  <span data-ttu-id="0337a-274">Merkitys</span><span class="sxs-lookup"><span data-stu-id="0337a-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0337a-275">P10</span><span class="sxs-lookup"><span data-stu-id="0337a-275">D10</span></span>|<span data-ttu-id="0337a-276">Kuukauden seuraava 10. päivä</span><span class="sxs-lookup"><span data-stu-id="0337a-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="0337a-277">VIP4</span><span class="sxs-lookup"><span data-stu-id="0337a-277">WD4</span></span>|<span data-ttu-id="0337a-278">Viikon seuraava 4. päivä \(torstai\)</span><span class="sxs-lookup"><span data-stu-id="0337a-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="0337a-279">Seuraavassa esimerkissä näytetään, miten voit yhdistää nämä kolme eri muotoa tarvittaessa:</span><span class="sxs-lookup"><span data-stu-id="0337a-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="0337a-280">Lauseke</span><span class="sxs-lookup"><span data-stu-id="0337a-280">Expression</span></span>  |  <span data-ttu-id="0337a-281">Merkitys</span><span class="sxs-lookup"><span data-stu-id="0337a-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0337a-282">NK+10P</span><span class="sxs-lookup"><span data-stu-id="0337a-282">CM+10D</span></span>|<span data-ttu-id="0337a-283">Nykyinen kuukausi \+ 10 päivää</span><span class="sxs-lookup"><span data-stu-id="0337a-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="0337a-284">Miinus-merkin avulla pystyt ilmaisemaan menneitä päiviä. Esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="0337a-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="0337a-285">Lauseke</span><span class="sxs-lookup"><span data-stu-id="0337a-285">Expression</span></span>  |  <span data-ttu-id="0337a-286">Merkitys</span><span class="sxs-lookup"><span data-stu-id="0337a-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0337a-287">-1 V.</span><span class="sxs-lookup"><span data-stu-id="0337a-287">-1Y</span></span>|<span data-ttu-id="0337a-288">1 vuosi taaksepäin tästä päivästä</span><span class="sxs-lookup"><span data-stu-id="0337a-288">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="0337a-289">Jos sijainti käyttää peruskalenteria, sitten päivämääräkaava, jonka annat esimerkiksi **Toimitusaika** -kenttään, tulkitaan kalenterin mukaan työskentelypäiviksi.</span><span class="sxs-lookup"><span data-stu-id="0337a-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="0337a-290">Esimerkiksi 1K tarkoittaa seitsemää käsittelypäivää.</span><span class="sxs-lookup"><span data-stu-id="0337a-290">For example, 1W  means seven working days.</span></span>
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a><span data-ttu-id="0337a-291">Aikojen syöttäminen</span><span class="sxs-lookup"><span data-stu-id="0337a-291">Entering Times</span></span>
<span data-ttu-id="0337a-292">Kun syötät ajat, voit lisätä yksiköiden välille minkä tahansa erottimen, joka ei ole välilyönti. Jos kuitenkin käytät kahta lukua millisekunteihin asti, erotin ei ole pakollinen.</span><span class="sxs-lookup"><span data-stu-id="0337a-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="0337a-293">Sinun on vain kirjoitettava suurimmat vaaditut yksiköt. Muiden arvoksi määritetään nolla.</span><span class="sxs-lookup"><span data-stu-id="0337a-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="0337a-294">Voit myös jättää mahdollisen AM/PM-osoittimen pois.</span><span class="sxs-lookup"><span data-stu-id="0337a-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="0337a-295">Seuraavassa taulukossa on luettelo eri tavoista, joilla aikoja voi syöttää ja miten niitä tulkitaan:</span><span class="sxs-lookup"><span data-stu-id="0337a-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="0337a-296">Oletusarvo on, että alueasetuksissa ajan muotoilu on **tunnit:minuutit:sekunnit:millisekunnit**</span><span class="sxs-lookup"><span data-stu-id="0337a-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="0337a-297">ja asetuksissa käytetään vastaavasti AM- ja PM-osoittimia.</span><span class="sxs-lookup"><span data-stu-id="0337a-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="0337a-298">**Tapahtuma**</span><span class="sxs-lookup"><span data-stu-id="0337a-298">**Entry**</span></span>      |<span data-ttu-id="0337a-299">**Tulkinta**</span><span class="sxs-lookup"><span data-stu-id="0337a-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="0337a-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="0337a-300">05:23:17</span></span>|<span data-ttu-id="0337a-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="0337a-301">05:23:17</span></span>|
|<span data-ttu-id="0337a-302">5</span><span class="sxs-lookup"><span data-stu-id="0337a-302">5</span></span>|<span data-ttu-id="0337a-303">05:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-303">05:00:00</span></span>|
|<span data-ttu-id="0337a-304">5AM</span><span class="sxs-lookup"><span data-stu-id="0337a-304">5AM</span></span>|<span data-ttu-id="0337a-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-305">05:00:00</span></span>|
|<span data-ttu-id="0337a-306">5P</span><span class="sxs-lookup"><span data-stu-id="0337a-306">5P</span></span>|<span data-ttu-id="0337a-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-307">17:00:00</span></span>|
|<span data-ttu-id="0337a-308">12</span><span class="sxs-lookup"><span data-stu-id="0337a-308">12</span></span>|<span data-ttu-id="0337a-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-309">12:00:00</span></span>|
|<span data-ttu-id="0337a-310">12A</span><span class="sxs-lookup"><span data-stu-id="0337a-310">12A</span></span>|<span data-ttu-id="0337a-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-311">00:00:00</span></span>|
|<span data-ttu-id="0337a-312">12P</span><span class="sxs-lookup"><span data-stu-id="0337a-312">12P</span></span>|<span data-ttu-id="0337a-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-313">12:00:00</span></span>|
|<span data-ttu-id="0337a-314">17</span><span class="sxs-lookup"><span data-stu-id="0337a-314">17</span></span>|<span data-ttu-id="0337a-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-315">17:00:00</span></span>|
|<span data-ttu-id="0337a-316">5:30</span><span class="sxs-lookup"><span data-stu-id="0337a-316">5:30</span></span>|<span data-ttu-id="0337a-317">05:30:00</span><span class="sxs-lookup"><span data-stu-id="0337a-317">05:30:00</span></span>|
|<span data-ttu-id="0337a-318">0530</span><span class="sxs-lookup"><span data-stu-id="0337a-318">0530</span></span>|<span data-ttu-id="0337a-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="0337a-319">05:30:00</span></span>|
|<span data-ttu-id="0337a-320">5:30:5 </span><span class="sxs-lookup"><span data-stu-id="0337a-320">5:30:5</span></span>|<span data-ttu-id="0337a-321">05:30:05</span><span class="sxs-lookup"><span data-stu-id="0337a-321">05:30:05</span></span>|
|<span data-ttu-id="0337a-322">053005</span><span class="sxs-lookup"><span data-stu-id="0337a-322">053005</span></span>|<span data-ttu-id="0337a-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="0337a-323">05:30:05</span></span>|
|<span data-ttu-id="0337a-324">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="0337a-324">5:30:5,50</span></span>|<span data-ttu-id="0337a-325">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="0337a-325">05:30:05.5</span></span>|
|<span data-ttu-id="0337a-326">053005050</span><span class="sxs-lookup"><span data-stu-id="0337a-326">053005050</span></span>|<span data-ttu-id="0337a-327">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="0337a-327">05:30:05.05</span></span>|

<span data-ttu-id="0337a-328">Ota huomioon, että millisekunnit tulkitaan desimaalimuodoksi.</span><span class="sxs-lookup"><span data-stu-id="0337a-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="0337a-329">Esimerkiksi 3, 30 ja 300 merkitsevät 300 millisekuntia, kun taas 03 tarkoittaa 30 ja 003 tarkoittaa 3 millisekuntia.</span><span class="sxs-lookup"><span data-stu-id="0337a-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="0337a-330">Et voi käyttää arvoa 24:00, jos tarkoitat keskiyötä, etkä mitään arvoa, joka on suurempi kuin 24:00.</span><span class="sxs-lookup"><span data-stu-id="0337a-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="0337a-331">Aika-sana [!INCLUDE[d365fin](includes/d365fin_long_md.md)] -sovelluksen käyttämällä kielellä arvioidaan tietokoneen tai mobiililaitteen nykyiseksi ajaksi.</span><span class="sxs-lookup"><span data-stu-id="0337a-331">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="0337a-332">Voit syöttää sanan minkä tahansa alkuosan, kuten a tai AIK.</span><span class="sxs-lookup"><span data-stu-id="0337a-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="0337a-333">Yhdistettyjen pvm:ien ja aikojen syöttäminen</span><span class="sxs-lookup"><span data-stu-id="0337a-333">Entering combined Dates and Times</span></span>
<span data-ttu-id="0337a-334">Kun syötät päivämääriä ja aikoja, joissa päivämäärä ja aika on yhdistetty yhdeksi kentäksi, päivämäärän ja ajan välissä on oltava välilyönti.</span><span class="sxs-lookup"><span data-stu-id="0337a-334">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="0337a-335">Päivämääräosa voi sisältää välilyöntejä vain alueasetusten virallisen päivämääräerottimen muodossa.</span><span class="sxs-lookup"><span data-stu-id="0337a-335">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="0337a-336">Ajan välilyönnit voivat olla AM/PM-osoittimen ympärillä.</span><span class="sxs-lookup"><span data-stu-id="0337a-336">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="0337a-337">Päivämäärän ja ajan kenttään on mahdollista syöttää myös vain päivämäärä, mutta vain aikaa ei voi syöttää.</span><span class="sxs-lookup"><span data-stu-id="0337a-337">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="0337a-338">Seuraavassa luettelossa on joitakin esimerkkejä päivämäärän ja ajan yhdistelmistä.</span><span class="sxs-lookup"><span data-stu-id="0337a-338">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="0337a-339">Esimerkkien alueasetuksissa näytetään päivämäärät muodossa päivä\-kuukausi\-vuosi. Niissä käytetään AM/PM-tunnuksia ja englannin kieltä. Sunnuntai on viikon ensimmäinen päivä.</span><span class="sxs-lookup"><span data-stu-id="0337a-339">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="0337a-340">**Tapahtuma**</span><span class="sxs-lookup"><span data-stu-id="0337a-340">**Entry**</span></span>      |<span data-ttu-id="0337a-341">**Tulkinta**</span><span class="sxs-lookup"><span data-stu-id="0337a-341">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="0337a-342">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="0337a-342">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="0337a-343">1.8.2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="0337a-343">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="0337a-344">131202 132455</span><span class="sxs-lookup"><span data-stu-id="0337a-344">131202 132455</span></span>|<span data-ttu-id="0337a-345">13.12.2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="0337a-345">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="0337a-346">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="0337a-346">1-12-02 10</span></span>|<span data-ttu-id="0337a-347">01.12.2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-347">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="0337a-348">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="0337a-348">1.12.02 5</span></span>|<span data-ttu-id="0337a-349">01.12.2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-349">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="0337a-350">1.12.02</span><span class="sxs-lookup"><span data-stu-id="0337a-350">1.12.02</span></span>|<span data-ttu-id="0337a-351">01.12.2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-351">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="0337a-352">11 12</span><span class="sxs-lookup"><span data-stu-id="0337a-352">11 12</span></span>|<span data-ttu-id="0337a-353">11.käsittelypvm:n kuukausi.käsittelypvm:n vuosi 12:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-353">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="0337a-354">1112 12</span><span class="sxs-lookup"><span data-stu-id="0337a-354">1112 12</span></span>|<span data-ttu-id="0337a-355">11.12.käsittelypvm:n vuosi 12:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-355">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="0337a-356">t tai tänään</span><span class="sxs-lookup"><span data-stu-id="0337a-356">t or today</span></span>|<span data-ttu-id="0337a-357">tämän päivän päivämäärä 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-357">today's date 00:00:00</span></span>|
|<span data-ttu-id="0337a-358">t 10:30:00</span><span class="sxs-lookup"><span data-stu-id="0337a-358">t 10:30</span></span>|<span data-ttu-id="0337a-359">tämän päivän päivämäärä 10:30:00</span><span class="sxs-lookup"><span data-stu-id="0337a-359">today's date 10:30:00</span></span>|
|<span data-ttu-id="0337a-360">t 3:3:3</span><span class="sxs-lookup"><span data-stu-id="0337a-360">t 3:3:3</span></span>|<span data-ttu-id="0337a-361">tämän päivän päivämäärä 03:03:03</span><span class="sxs-lookup"><span data-stu-id="0337a-361">today's date 03:03:03</span></span>|
|<span data-ttu-id="0337a-362">k tai käsittelypvm</span><span class="sxs-lookup"><span data-stu-id="0337a-362">w or workdate</span></span>|<span data-ttu-id="0337a-363">käsittelypvm 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-363">the working date 00:00:00</span></span>|
|<span data-ttu-id="0337a-364">ma tai maanantai</span><span class="sxs-lookup"><span data-stu-id="0337a-364">m or Monday</span></span>|<span data-ttu-id="0337a-365">Käsittelypvm:n viikon maanantai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-365">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="0337a-366">ti tai tiistai</span><span class="sxs-lookup"><span data-stu-id="0337a-366">tu or Tuesday</span></span>|<span data-ttu-id="0337a-367">Käsittelypvm:n viikon tiistai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-367">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="0337a-368">la tai lauantai</span><span class="sxs-lookup"><span data-stu-id="0337a-368">sa or Saturday</span></span>|<span data-ttu-id="0337a-369">Käsittelypvm:n viikon lauantai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-369">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="0337a-370">su tai sunnuntai</span><span class="sxs-lookup"><span data-stu-id="0337a-370">s or Sunday</span></span>|<span data-ttu-id="0337a-371">Käsittelypvm:n viikon sunnuntai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-371">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="0337a-372">ti 10:30:00</span><span class="sxs-lookup"><span data-stu-id="0337a-372">tu 10:30</span></span>|<span data-ttu-id="0337a-373">Käsittelypvm:n viikon tiistai 10:30:00</span><span class="sxs-lookup"><span data-stu-id="0337a-373">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="0337a-374">ti 3:3:3</span><span class="sxs-lookup"><span data-stu-id="0337a-374">tu 3:3:3</span></span>|<span data-ttu-id="0337a-375">Käsittelypvm:n viikon tiistai 03:03:03</span><span class="sxs-lookup"><span data-stu-id="0337a-375">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="0337a-376">t23 t</span><span class="sxs-lookup"><span data-stu-id="0337a-376">t23 t</span></span>|<span data-ttu-id="0337a-377">Käsittelypvm:n vuoden viikon 23 tiistai, nykyinen aika</span><span class="sxs-lookup"><span data-stu-id="0337a-377">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="0337a-378">t23</span><span class="sxs-lookup"><span data-stu-id="0337a-378">t23</span></span>|<span data-ttu-id="0337a-379">Käsittelypvm:n vuoden viikon 23 tiistai</span><span class="sxs-lookup"><span data-stu-id="0337a-379">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="0337a-380">t 23</span><span class="sxs-lookup"><span data-stu-id="0337a-380">t 23</span></span>|<span data-ttu-id="0337a-381">Tänään 23:00:00</span><span class="sxs-lookup"><span data-stu-id="0337a-381">Today 23:00:00</span></span>|
|<span data-ttu-id="0337a-382">t-1</span><span class="sxs-lookup"><span data-stu-id="0337a-382">t-1</span></span>|<span data-ttu-id="0337a-383">Käsittelypvm:n vuoden viikon 1 tiistai</span><span class="sxs-lookup"><span data-stu-id="0337a-383">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="0337a-384">Keston syöttäminen</span><span class="sxs-lookup"><span data-stu-id="0337a-384">Entering Duration</span></span>
<span data-ttu-id="0337a-385">Sovelluksen jotkin kentät edustavat kestoa tai kuluneen ajan määrää tietyn päivämäärän tai ajan sijaan.</span><span class="sxs-lookup"><span data-stu-id="0337a-385">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="0337a-386">Kesto syötetään numerona, jota seuraa sen mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="0337a-386">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="0337a-387">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="0337a-387">Here are some examples.</span></span>

|<span data-ttu-id="0337a-388">**Kesto**</span><span class="sxs-lookup"><span data-stu-id="0337a-388">**Duration**</span></span>|<span data-ttu-id="0337a-389">**Mittayksikkö**</span><span class="sxs-lookup"><span data-stu-id="0337a-389">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="0337a-390">2t</span><span class="sxs-lookup"><span data-stu-id="0337a-390">2h</span></span>|<span data-ttu-id="0337a-391">2 tuntia</span><span class="sxs-lookup"><span data-stu-id="0337a-391">2 hrs</span></span>|
|<span data-ttu-id="0337a-392">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="0337a-392">6h 30 m</span></span>|<span data-ttu-id="0337a-393">6 tuntia 30 minuuttia</span><span class="sxs-lookup"><span data-stu-id="0337a-393">6 hrs 30 mins</span></span>|
|<span data-ttu-id="0337a-394">6,5t</span><span class="sxs-lookup"><span data-stu-id="0337a-394">6.5h</span></span>|<span data-ttu-id="0337a-395">6 tuntia 30 minuuttia</span><span class="sxs-lookup"><span data-stu-id="0337a-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="0337a-396">90 m</span><span class="sxs-lookup"><span data-stu-id="0337a-396">90m</span></span>|<span data-ttu-id="0337a-397">1 tunti 30 minuuttia</span><span class="sxs-lookup"><span data-stu-id="0337a-397">1 hr 30 mins</span></span>|
|<span data-ttu-id="0337a-398">2p 6t 30m</span><span class="sxs-lookup"><span data-stu-id="0337a-398">2d 6h 30m</span></span>|<span data-ttu-id="0337a-399">2 päivää 6 tuntia 30 minuuttia</span><span class="sxs-lookup"><span data-stu-id="0337a-399">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="0337a-400">2p 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="0337a-400">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="0337a-401">2 päivää 6 tuntia 30 minuuttia 56 sekuntia 600 tuhannesosasekuntia</span><span class="sxs-lookup"><span data-stu-id="0337a-401">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="0337a-402">Voit syöttää myös numeron, jonka ohjelma muuntaa automaattisesti kestoksi.</span><span class="sxs-lookup"><span data-stu-id="0337a-402">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="0337a-403">Syöttämäsi numero muunnetaan kestokenttään määritellyn oletusmittayksikön mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="0337a-403">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="0337a-404">Voit tarkastaa, mitä mittayksikköä kestokentässä käytetään, syöttämällä numeron ja katsomalla, mihin mittayksikköön ohjelma muuntaa sen.</span><span class="sxs-lookup"><span data-stu-id="0337a-404">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="0337a-405">Jos mittayksikkö on esimerkiksi Tunnit, numero 5 muunnetaan 5 tunniksi.</span><span class="sxs-lookup"><span data-stu-id="0337a-405">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="0337a-406">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0337a-406">See Also</span></span>
<span data-ttu-id="0337a-407">[[!INCLUDE[d365fin](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0337a-407">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0337a-408">Ostojen päivämäärälaskenta</span><span class="sxs-lookup"><span data-stu-id="0337a-408">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="0337a-409">Ehtojen antaminen suodattimiin</span><span class="sxs-lookup"><span data-stu-id="0337a-409">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
