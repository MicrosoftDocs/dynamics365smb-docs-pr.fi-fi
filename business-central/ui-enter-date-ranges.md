---
title: "Päivämääräalueiden asettaminen Business Central -sovelluksessa | Microsoft Docs"
description: "Tutustu, miten luodaan raportti näyttämään tietyn ajanjakson tiedot käyttämällä Business Central -sovelluksen päivämääräalueita."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: fi-fi
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="5c7a7-103">Päivämääräalueiden syöttäminen</span><span class="sxs-lookup"><span data-stu-id="5c7a7-103">Entering Date Ranges</span></span>
<span data-ttu-id="5c7a7-104">Voit asettaa suodattimia, jotka sisältävät alkupäivämäärän ja loppupäivämäärän, jos haluat tarkastella vain kyseisen päivämääräalueen tai aikavälin tietoja.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="5c7a7-105">Päivämääräalueiden määrittämiseen liittyy erityissääntöjä:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="5c7a7-106">Käytetään esimerkkinä **10 pääasiakasta**:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-106">Let's take the **Customer Top 10** as an example:</span></span>

![10 pääasiakkaan luettelon päivämääräalueen määrittäminen pyyntösivulla](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="5c7a7-108">Voit rajoittaa raportin päivämääräalueeksi viimeiset kaksi viikkoa, yhteensä kuusi viikkoa tai minkä tahansa sopivan alueen.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="5c7a7-109">Päivämääräalue määritetään antamalla päivämäärät ja määrittämällä alueen joko **..**-</span><span class="sxs-lookup"><span data-stu-id="5c7a7-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="5c7a7-110">tai **|**-merkillä.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-110">or **|** to set the range.</span></span> <span data-ttu-id="5c7a7-111">Tässä esimerkissä 10 pääasiakkaan näyttäminen toukokuun kahdella ensimmäisellä viikolla edellyttää, että päivämääräsuodatin määritetään muotoon *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="5c7a7-112">Lisää esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="5c7a7-113">Merkitys</span><span class="sxs-lookup"><span data-stu-id="5c7a7-113">Meaning</span></span> | <span data-ttu-id="5c7a7-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5c7a7-114">Example</span></span> | <span data-ttu-id="5c7a7-115">Sisällytetyt tapahtumat</span><span class="sxs-lookup"><span data-stu-id="5c7a7-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="5c7a7-116">Sama kuin</span><span class="sxs-lookup"><span data-stu-id="5c7a7-116">Equal to</span></span>| <span data-ttu-id="5c7a7-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="5c7a7-117">12 15 16</span></span> |<span data-ttu-id="5c7a7-118">Vain tapahtumat, jotka on kirjattu 15.12.2016.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="5c7a7-119">Väli</span><span class="sxs-lookup"><span data-stu-id="5c7a7-119">Interval</span></span>| <span data-ttu-id="5c7a7-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="5c7a7-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="5c7a7-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="5c7a7-121">..12 15 16</span></span>|<span data-ttu-id="5c7a7-122">Tapahtumat, jotka on kirjattu ajalla 15.12.2016–15.1.2017 (kyseiset päivämäärät mukaan lukien).</span><span class="sxs-lookup"><span data-stu-id="5c7a7-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="5c7a7-123">Tapahtumat, jotka on kirjattu 15.12.2016 tai sitä aiemmin.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="5c7a7-124">Joko/tai</span><span class="sxs-lookup"><span data-stu-id="5c7a7-124">Either/or</span></span>|<span data-ttu-id="5c7a7-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="5c7a7-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="5c7a7-126">Tapahtumat, jotka on kirjattu joko 15.12. tai 16.12.2016.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="5c7a7-127">Jos molempina päivinä on kirjattu tapahtumia, kaikki kyseisten päivien tapahtumat näytetään.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="5c7a7-128">Eri muotoja voi myös yhdistellä:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="5c7a7-129">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5c7a7-129">Example</span></span> | <span data-ttu-id="5c7a7-130">Sisällytetyt tapahtumat</span><span class="sxs-lookup"><span data-stu-id="5c7a7-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="5c7a7-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="5c7a7-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="5c7a7-132">Tapahtumat, jotka on kirjattu joko 15.12.2011 tai ajalla 1.12.2016– 31.5.2017 (kyseiset päivämäärät mukaan lukien).</span><span class="sxs-lookup"><span data-stu-id="5c7a7-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="5c7a7-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="5c7a7-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="5c7a7-134">Tapahtumat, jotka on kirjattu 14.12 tai sitä ennen, tai tapahtumat, jotka on kirjattu 30.12. tai sen jälkeen – toisin sanoen kaikki muut paitsi 15.–29.12. kirjatut tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="5c7a7-135">Huomaa, että tässä on käytetty yhdysvaltalaista päivämäärämuoto KKPPVV.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="5c7a7-136">Kun [!INCLUDE[d365fin](includes/d365fin_md.md)] on saatavana muilla markkina-alueilla, saat käyttöösi tutut päivämäärämuodot.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="5c7a7-137">Päivämäärän kaavojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="5c7a7-137">Using Date Formulas</span></span>
<span data-ttu-id="5c7a7-138">Päivämäärän kaava on lyhyt kirjain- ja numeroyhdistelmä, joka kertoo ohjelmalle, miten päivämäärät lasketaan.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="5c7a7-139">Voit kirjoittaa päivämäärän kaavoja erilaisiin päivämäärän laskentakenttiin sekä toistuvien päiväkirjojen toistotiheyskenttiin.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="5c7a7-140">Kaikissa tietokaavakentissä yksi päivä sisällytetään automaattisesti edustamaan kuluvaa päivää kauden alkupäivänä.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="5c7a7-141">Jos näin ollen annat esimerkiksi **1V**, kausi on kahdeksan päivää, koska tämä päivä lasketaan mukaan.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="5c7a7-142">Määritä seitsemän päivän kausi (yksi kokonainen viikko), joka sisältää alkamispäivämäärän, ja syötä sitten **6D** tai **1W\-1D**.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="5c7a7-143">Seuraavassa on joitakin esimerkkejä päivämäärän kaavojen käytöstä:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="5c7a7-144">Toistuvien päiväkirjojen toistotiheys-kentän päivämäärän kaava määrittää, kuinka usein päiväkirjan rivin tapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="5c7a7-145">**Ylityskausi**-kentän tietyn tason muistutusta koskeva päivämäärän kaava määrittelee ajanjakson, joka on kuluttava eräpäivästä (tai edellisen muistutuksen eräpäivästä), ennen kuin muistutus voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="5c7a7-146">**Eräpäivän laskenta** -kentän kaava määrittää, miten ohjelma laskee muistutuksen eräpäivän.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="5c7a7-147">Eräpäivän laskentakaavassa voi olla enintään 20 merkkiä, sekä numeroita että kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="5c7a7-148">Voit käyttää seuraavia kirjaimia, jotka ovat aikamääreiden lyhenteitä:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="5c7a7-149">Kirjain</span><span class="sxs-lookup"><span data-stu-id="5c7a7-149">Letter</span></span>  |  <span data-ttu-id="5c7a7-150">Aikamääritys</span><span class="sxs-lookup"><span data-stu-id="5c7a7-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="5c7a7-151">S</span><span class="sxs-lookup"><span data-stu-id="5c7a7-151">C</span></span>|<span data-ttu-id="5c7a7-152">Nykyinen</span><span class="sxs-lookup"><span data-stu-id="5c7a7-152">Current</span></span>|
|<span data-ttu-id="5c7a7-153">P</span><span class="sxs-lookup"><span data-stu-id="5c7a7-153">D</span></span>|<span data-ttu-id="5c7a7-154">Päivä</span><span class="sxs-lookup"><span data-stu-id="5c7a7-154">Day\(s\)</span></span>|
|<span data-ttu-id="5c7a7-155">L</span><span class="sxs-lookup"><span data-stu-id="5c7a7-155">W</span></span>|<span data-ttu-id="5c7a7-156">Viikko</span><span class="sxs-lookup"><span data-stu-id="5c7a7-156">Week\(s\)</span></span>|
|<span data-ttu-id="5c7a7-157">M</span><span class="sxs-lookup"><span data-stu-id="5c7a7-157">M</span></span>|<span data-ttu-id="5c7a7-158">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="5c7a7-158">Month\(s\)</span></span>|
|<span data-ttu-id="5c7a7-159">Q</span><span class="sxs-lookup"><span data-stu-id="5c7a7-159">Q</span></span>|<span data-ttu-id="5c7a7-160">Vuosineljännes</span><span class="sxs-lookup"><span data-stu-id="5c7a7-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="5c7a7-161">V</span><span class="sxs-lookup"><span data-stu-id="5c7a7-161">Y</span></span>|<span data-ttu-id="5c7a7-162">Vuosi</span><span class="sxs-lookup"><span data-stu-id="5c7a7-162">Year\(s\)</span></span>|

<span data-ttu-id="5c7a7-163">Voit rakentaa päivämääräkaavan kolmella eri tavalla:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="5c7a7-164">Seuraava esimerkki näyttää, miten käytetään kirjainta **C** (nykyinen) ja aikayksikköä.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="5c7a7-165">Lauseke</span><span class="sxs-lookup"><span data-stu-id="5c7a7-165">Expression</span></span>  |  <span data-ttu-id="5c7a7-166">Merkitys</span><span class="sxs-lookup"><span data-stu-id="5c7a7-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="5c7a7-167">NVI</span><span class="sxs-lookup"><span data-stu-id="5c7a7-167">CW</span></span>|<span data-ttu-id="5c7a7-168">Nykyinen viikko</span><span class="sxs-lookup"><span data-stu-id="5c7a7-168">Current week</span></span>|
|<span data-ttu-id="5c7a7-169">NK</span><span class="sxs-lookup"><span data-stu-id="5c7a7-169">CM</span></span>|<span data-ttu-id="5c7a7-170">Nykyinen kuukausi</span><span class="sxs-lookup"><span data-stu-id="5c7a7-170">Current month</span></span>|

<span data-ttu-id="5c7a7-171">Seuraava esimerkki näyttää, miten käytetään numeroa ja aikayksikköä.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="5c7a7-172">Numero ei voi olla suurempi kuin 9999.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="5c7a7-173">Lauseke</span><span class="sxs-lookup"><span data-stu-id="5c7a7-173">Expression</span></span>  |  <span data-ttu-id="5c7a7-174">Merkitys</span><span class="sxs-lookup"><span data-stu-id="5c7a7-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="5c7a7-175">10P</span><span class="sxs-lookup"><span data-stu-id="5c7a7-175">10D</span></span>|<span data-ttu-id="5c7a7-176">10 päivää tästä päivästä</span><span class="sxs-lookup"><span data-stu-id="5c7a7-176">10 days from today</span></span>|
|<span data-ttu-id="5c7a7-177">2VI</span><span class="sxs-lookup"><span data-stu-id="5c7a7-177">2W</span></span>|<span data-ttu-id="5c7a7-178">2 viikkoa tämän päivän jälkeen</span><span class="sxs-lookup"><span data-stu-id="5c7a7-178">2 weeks from today</span></span>|

<span data-ttu-id="5c7a7-179">Seuraava esimerkki näyttää, miten käytetään aikayksikköä ja numeroa.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="5c7a7-180">Lauseke</span><span class="sxs-lookup"><span data-stu-id="5c7a7-180">Expression</span></span>  |  <span data-ttu-id="5c7a7-181">Merkitys</span><span class="sxs-lookup"><span data-stu-id="5c7a7-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="5c7a7-182">P10</span><span class="sxs-lookup"><span data-stu-id="5c7a7-182">D10</span></span>|<span data-ttu-id="5c7a7-183">Kuukauden seuraava 10. päivä</span><span class="sxs-lookup"><span data-stu-id="5c7a7-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="5c7a7-184">VIP4</span><span class="sxs-lookup"><span data-stu-id="5c7a7-184">WD4</span></span>|<span data-ttu-id="5c7a7-185">Viikon seuraava 4. päivä \(torstai\)</span><span class="sxs-lookup"><span data-stu-id="5c7a7-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="5c7a7-186">Seuraavassa esimerkissä näytetään, miten voit yhdistää nämä kolme eri muotoa tarvittaessa:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="5c7a7-187">Lauseke</span><span class="sxs-lookup"><span data-stu-id="5c7a7-187">Expression</span></span>  |  <span data-ttu-id="5c7a7-188">Merkitys</span><span class="sxs-lookup"><span data-stu-id="5c7a7-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="5c7a7-189">CM\+10D</span><span class="sxs-lookup"><span data-stu-id="5c7a7-189">CM\+10D</span></span>|<span data-ttu-id="5c7a7-190">Nykyinen kuukausi \+ 10 päivää</span><span class="sxs-lookup"><span data-stu-id="5c7a7-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="5c7a7-191">Miinus-merkin avulla pystyt ilmaisemaan menneitä päiviä. Esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="5c7a7-192">Lauseke</span><span class="sxs-lookup"><span data-stu-id="5c7a7-192">Expression</span></span>  |  <span data-ttu-id="5c7a7-193">Merkitys</span><span class="sxs-lookup"><span data-stu-id="5c7a7-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="5c7a7-194">-1 V.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-194">-1Y</span></span>|<span data-ttu-id="5c7a7-195">1 vuosi taaksepäin tästä päivästä</span><span class="sxs-lookup"><span data-stu-id="5c7a7-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="5c7a7-196">Jos sijainti käyttää peruskalenteria, sitten päivämääräkaava, jonka annat esimerkiksi **Toimitusaika** -kenttään, tulkitaan kalenterin mukaan työskentelypäiviksi.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="5c7a7-197">Esimerkiksi **1V** tarkoittaa seitsemää työpäivää.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c7a7-198">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5c7a7-198">See Also</span></span>
<span data-ttu-id="5c7a7-199">[[!INCLUDE[d365fin](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5c7a7-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5c7a7-200">Ostojen päivämäärälaskenta</span><span class="sxs-lookup"><span data-stu-id="5c7a7-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="5c7a7-201">Ehtojen antaminen suodattimiin</span><span class="sxs-lookup"><span data-stu-id="5c7a7-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

