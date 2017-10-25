---
title: "Dynamics 365 for Financialsin päivämääräalueiden määrittäminen | Microsoft Docs"
description: "Tutustu, miten luodaan raportti näyttämään tietyn ajanjakson tiedot käyttämällä Dynamics 365 for Financialsin päivämääräalueita."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dc7cd392843ce7c39200bb2331c09cc44c7a394a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="entering-date-ranges-in-dynamics-365-for-financials"></a><span data-ttu-id="32078-103">Dynamics 365 for Financialsin päivämääräalueiden antaminen</span><span class="sxs-lookup"><span data-stu-id="32078-103">Entering Date Ranges in Dynamics 365 for Financials</span></span>
<span data-ttu-id="32078-104">Voit asettaa suodattimia, jotka sisältävät alkupäivämäärän ja loppupäivämäärän, jos haluat tarkastella vain kyseisen päivämääräalueen tai aikavälin tietoja.</span><span class="sxs-lookup"><span data-stu-id="32078-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="32078-105">Päivämääräalueiden määrittämiseen liittyy erityissääntöjä:</span><span class="sxs-lookup"><span data-stu-id="32078-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="32078-106">Käytetään esimerkkinä **10 pääasiakasta**:</span><span class="sxs-lookup"><span data-stu-id="32078-106">Let's take the **Customer Top 10** as an example:</span></span>

![10 pääasiakkaan luettelon päivämääräalueen määrittäminen pyyntösivulla](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="32078-108">Voit rajoittaa raportin päivämääräalueeksi viimeiset kaksi viikkoa, yhteensä kuusi viikkoa tai minkä tahansa sopivan alueen.</span><span class="sxs-lookup"><span data-stu-id="32078-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="32078-109">Päivämääräalue määritetään antamalla päivämäärät ja määrittämällä alueen joko **..**-</span><span class="sxs-lookup"><span data-stu-id="32078-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="32078-110">tai **|**-merkillä.</span><span class="sxs-lookup"><span data-stu-id="32078-110">or **|** to set the range.</span></span> <span data-ttu-id="32078-111">Tässä esimerkissä 10 pääasiakkaan näyttäminen toukokuun kahdella ensimmäisellä viikolla edellyttää, että päivämääräsuodatin määritetään muotoon *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="32078-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="32078-112">Lisää esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="32078-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="32078-113">Merkitys</span><span class="sxs-lookup"><span data-stu-id="32078-113">Meaning</span></span> | <span data-ttu-id="32078-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="32078-114">Example</span></span> | <span data-ttu-id="32078-115">Sisällytetyt tapahtumat</span><span class="sxs-lookup"><span data-stu-id="32078-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="32078-116">Sama kuin</span><span class="sxs-lookup"><span data-stu-id="32078-116">Equal to</span></span>| <span data-ttu-id="32078-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="32078-117">12 15 16</span></span> |<span data-ttu-id="32078-118">Vain tapahtumat, jotka on kirjattu 15.12.2016.</span><span class="sxs-lookup"><span data-stu-id="32078-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="32078-119">Väli</span><span class="sxs-lookup"><span data-stu-id="32078-119">Interval</span></span>| <span data-ttu-id="32078-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="32078-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="32078-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="32078-121">..12 15 16</span></span>|<span data-ttu-id="32078-122">Tapahtumat, jotka on kirjattu ajalla 15.12.2016–15.1.2017 (kyseiset päivämäärät mukaan lukien).</span><span class="sxs-lookup"><span data-stu-id="32078-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="32078-123">Tapahtumat, jotka on kirjattu 15.12.2016 tai sitä aiemmin.</span><span class="sxs-lookup"><span data-stu-id="32078-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="32078-124">Joko/tai</span><span class="sxs-lookup"><span data-stu-id="32078-124">Either/or</span></span>|<span data-ttu-id="32078-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="32078-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="32078-126">Tapahtumat, jotka on kirjattu joko 15.12. tai 16.12.2016.</span><span class="sxs-lookup"><span data-stu-id="32078-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="32078-127">Jos molempina päivinä on kirjattu tapahtumia, kaikki kyseisten päivien tapahtumat näytetään.</span><span class="sxs-lookup"><span data-stu-id="32078-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="32078-128">Eri muotoja voi myös yhdistellä:</span><span class="sxs-lookup"><span data-stu-id="32078-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="32078-129">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="32078-129">Example</span></span> | <span data-ttu-id="32078-130">Sisällytetyt tapahtumat</span><span class="sxs-lookup"><span data-stu-id="32078-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="32078-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="32078-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="32078-132">Tapahtumat, jotka on kirjattu joko 15.12.2011 tai ajalla 1.12.2016– 31.5.2017 (kyseiset päivämäärät mukaan lukien).</span><span class="sxs-lookup"><span data-stu-id="32078-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="32078-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="32078-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="32078-134">Tapahtumat, jotka on kirjattu 14.12 tai sitä ennen, tai tapahtumat, jotka on kirjattu 30.12. tai sen jälkeen – toisin sanoen kaikki muut paitsi 15.–29.12. kirjatut tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="32078-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="32078-135">Huomaa, että tässä on käytetty yhdysvaltalaista päivämäärämuoto KKPPVV.</span><span class="sxs-lookup"><span data-stu-id="32078-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="32078-136">Kun [!INCLUDE[d365fin](includes/d365fin_md.md)] on saatavana muilla markkina-alueilla, saat käyttöösi tutut päivämäärämuodot.</span><span class="sxs-lookup"><span data-stu-id="32078-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="32078-137">Katso myös</span><span class="sxs-lookup"><span data-stu-id="32078-137">See Also</span></span>
<span data-ttu-id="32078-138">[[!INCLUDE[d365fin](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="32078-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="32078-139">Ehtojen antaminen suodattimiin</span><span class="sxs-lookup"><span data-stu-id="32078-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="32078-140">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="32078-140">General Business Functionality</span></span>](ui-across-business-areas.md)

