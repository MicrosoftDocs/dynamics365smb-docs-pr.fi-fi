---
title: "Kirjanpitojaksojen ja tilikausien käyttäminen | Microsoft Docs"
description: "Lisätietoja tilijaksojen käyttämisestä määrittämään, milloin yrityksen taloudellinen tulos raportoidaan."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/13/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6f760f546ea02fbc19473c70eb26d8b4c47c0987
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="working-with-accounting-periods-and-fiscal-years"></a><span data-ttu-id="3737a-103">Kirjanpitojaksojen ja tilikausien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="3737a-103">Working with Accounting Periods and Fiscal Years</span></span>
<span data-ttu-id="3737a-104">Tilijaksot, joita kutsutaan myös raportointikausiksi, ovat ajanjaksoja, jolloin yritys tai organisaatio raportoi taloudellisen tuloksen luomalla esimerkiksi tuloslaskeman tai taseen.</span><span class="sxs-lookup"><span data-stu-id="3737a-104">Accounting periods, which are also known as reporting periods, are periods of time for which a company or organization reports financial performance, for example, by generating their income statement or balance sheet.</span></span> <span data-ttu-id="3737a-105">Yleensä kirjanpitojaksoilla viitataan yrityksen tilikauteen, joka voi koostua useista tilijaksoista, kuten kuukausista tai neljännesvuosista.</span><span class="sxs-lookup"><span data-stu-id="3737a-105">Typically, accounting periods refer to the company's fiscal year, which can contain several accounting periods, such as months or quarters.</span></span>

<span data-ttu-id="3737a-106">Tilikausi ja kalenterivuosi eivät ole samat monissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="3737a-106">For many companies the fiscal year does not align with the calendar year.</span></span> <span data-ttu-id="3737a-107">Tilikausi voi esimerkiksi päättyä 30.6. eikä 31.12.</span><span class="sxs-lookup"><span data-stu-id="3737a-107">For example, the fiscal year might end on June 30th rather than December 31st.</span></span> <span data-ttu-id="3737a-108">Uusilla yrityksillä tilikausi voi myös olla pidempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="3737a-108">For newly created companies, the fiscal might actually be longer than 12 months.</span></span> 

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="3737a-109">edellyttää kirjanpitojaksoja vain siinä tapauksessa, että haluat sulkea tuloslaskelman tai suorittaa tietojen tiivistystehtäviä.</span><span class="sxs-lookup"><span data-stu-id="3737a-109">only requires accounting periods only if you want to close an income statement, or run data compression tasks.</span></span> 

<span data-ttu-id="3737a-110">Voit käyttää kirjanpitojaksoja raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="3737a-110">You can use accounting periods in reporting.</span></span> <span data-ttu-id="3737a-111">Näin tehdään esimerkiksi silloin, kun kirjattuja tapahtumia tarkastellaan **Saldo/budjetti**-sivulla, jossa raportointiväli voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="3737a-111">For example, when you are reviewing posted entries on the **Balance/Budget** page where the reporting interval can be specified.</span></span> <span data-ttu-id="3737a-112">Yksi vaihtoehdoista on raportoinnin määrittäminen kirjanpitojakson mukaan.</span><span class="sxs-lookup"><span data-stu-id="3737a-112">One of the options you may specify to report by accounting period.</span></span> <span data-ttu-id="3737a-113">Voit myös muodostaa KP-raporttimallin, joka vertaa eri kirjanpitojaksojen tuloksia.</span><span class="sxs-lookup"><span data-stu-id="3737a-113">You can also build an account schedule that compares results for different accounting periods.</span></span>

## <a name="creating-a-new-fiscal-year"></a><span data-ttu-id="3737a-114">Uuden tilikauden luominen</span><span class="sxs-lookup"><span data-stu-id="3737a-114">Creating a new fiscal year</span></span>
<span data-ttu-id="3737a-115">Voit luoda kirjanpitojaksoja joukkotoiminnolla käyttämällä **Luo tilikausi** -eräajoa tai voit luoda ne manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="3737a-115">You can create accounting periods in bulk, by using eh **Create Fiscal Year** batch job, or manually.</span></span>

### <a name="how-to-create-accounting-periods-in-bulk"></a><span data-ttu-id="3737a-116">Kirjanpitojaksojen luominen joukkotoiminnolla</span><span class="sxs-lookup"><span data-stu-id="3737a-116">How to create accounting periods in-bulk</span></span>
<span data-ttu-id="3737a-117">Jaa tilikausi saman mittaisiksi jaksoiksi **Luo tilikausi** -eräajon avulla.</span><span class="sxs-lookup"><span data-stu-id="3737a-117">Use the **Create Fiscal Year** batch job to divide a fiscal year into periods of equal length.</span></span>  

1. <span data-ttu-id="3737a-118">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3737a-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3737a-119">Valitse **Luo vuosi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3737a-119">Choose the **Create Year** action.</span></span>  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. <span data-ttu-id="3737a-120">Anna **Aloituspvm**-kenttään päivämäärä, jolloin tilikausi alkaa.</span><span class="sxs-lookup"><span data-stu-id="3737a-120">In the **Starting Date** field, enter the date on which the fiscal year starts.</span></span>  
4. <span data-ttu-id="3737a-121">Määrittele **Jaksojen lukumäärä** -kentässä, kuinka moneen kirjanpitojaksoon tilikausi jaetaan.</span><span class="sxs-lookup"><span data-stu-id="3737a-121">In the **No. of Periods** field, enter the number of accounting periods to divide the fiscal year into.</span></span> <span data-ttu-id="3737a-122">Vuodessa voi olla enintään 365 jaksoa.</span><span class="sxs-lookup"><span data-stu-id="3737a-122">There can be up to 365 periods in a year.</span></span>  
5. <span data-ttu-id="3737a-123">Määritä **Jakson pituus** -kentässä kunkin jakson kesto.</span><span class="sxs-lookup"><span data-stu-id="3737a-123">In the **Period Length** field, enter a duration for each period.</span></span> <span data-ttu-id="3737a-124">Esimerkiksi yksi kuukausi on 1K, yksi neljännesvuosi on 1Q ja yksi vuosi 1V.</span><span class="sxs-lookup"><span data-stu-id="3737a-124">For example, 1M for one month, 1Q for one quarter, and 1Y for one year.</span></span>  
6. <span data-ttu-id="3737a-125">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3737a-125">Choose **OK**.</span></span>  

### <a name="how-to-create-accounting-periods-manually"></a><span data-ttu-id="3737a-126">Kirjanpitojaksojen luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="3737a-126">How to create accounting periods manually</span></span>
<span data-ttu-id="3737a-127">Jos tilikauden kirjanpitojaksojen pituudet vaihtelevat, kuten vähittäismyynnissä käytetty 4-4-5-kalenteri, määritys voidaan tehdä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="3737a-127">If the accounting periods in your fiscal year have different durations, like the 4-4-5 calendar used in retail, you can manually set it up.</span></span>  
  
1. <span data-ttu-id="3737a-128">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Kirjanpitojaksot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3737a-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3737a-129">Anna **Aloituspvm**-kenttään päivämäärä, jolloin tilikausi alkaa.</span><span class="sxs-lookup"><span data-stu-id="3737a-129">In the **Starting Date** field, enter the date on which the fiscal year starts.</span></span> <span data-ttu-id="3737a-130">**Nimi**-kentässä on kuukauden nimi.</span><span class="sxs-lookup"><span data-stu-id="3737a-130">The **Name** field will show the name of the month.</span></span>  
3. <span data-ttu-id="3737a-131">Ilmaise **Uusi tilikausi** -valintaruudun valinnalla, että kyse on vuoden ensimmäisestä jaksosta.</span><span class="sxs-lookup"><span data-stu-id="3737a-131">Choose the **New Fiscal Year** check box to indicate that this is the first period in the year.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="3737a-132">määrittää tämän jakson perusteella, mitkä jaksot sulkevat tilikauden.</span><span class="sxs-lookup"><span data-stu-id="3737a-132">will use this period to determine which periods to close at year-end.</span></span>
4. <span data-ttu-id="3737a-133">Toista vaiheet 2 ja 3 kunkin jäljellä olevan jakson kohdalla.</span><span class="sxs-lookup"><span data-stu-id="3737a-133">Repeat steps 2 and 3 for each remaining period.</span></span>  

## <a name="closing-a-fiscal-year"></a><span data-ttu-id="3737a-134">Tilikauden sulkeminen</span><span class="sxs-lookup"><span data-stu-id="3737a-134">Closing a Fiscal Year</span></span>
<span data-ttu-id="3737a-135">Tilikauden sulkeminen on yksi kirjojen sulkemistehtävistä.</span><span class="sxs-lookup"><span data-stu-id="3737a-135">Closing the fiscal year is one of the tasks for closing the books.</span></span> <span data-ttu-id="3737a-136">Kun tilikausi on suljettu, **Suljettu**- ja **Pvm lukittu** -valintaruudut valitaan kaikille tilikauden jaksoille.</span><span class="sxs-lookup"><span data-stu-id="3737a-136">After you close a fiscal year, the **Closed** and **Date Locked** check boxes are selected for all periods in the year.</span></span> <span data-ttu-id="3737a-137">Tilakautta ei voi avata uudelleen eikä valintaruutujen valintaa poistaa.</span><span class="sxs-lookup"><span data-stu-id="3737a-137">You cannot reopen a year or clear the check boxes.</span></span>

> [!NOTE]  
>  <span data-ttu-id="3737a-138">Avoimena on oltava aina ainakin yksi tilikausi.</span><span class="sxs-lookup"><span data-stu-id="3737a-138">You must always have at least one open fiscal year.</span></span> <span data-ttu-id="3737a-139">Varmista tilikautta suljettaessa, että tilikausi on luotu.</span><span class="sxs-lookup"><span data-stu-id="3737a-139">When closing a year, ensure that a new year has been created.</span></span> <span data-ttu-id="3737a-140">Huomaa myös, että kun tilikausi on suljettu, et voi muuttaa seuraavan tilikauden aloituspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="3737a-140">Also, note that after you close one year, you cannot change the starting date of the following year.</span></span>

1. <span data-ttu-id="3737a-141">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Kirjanpitojaksot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3737a-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3737a-142">Valitse **Sulje vuosi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3737a-142">Choose the **Close Year** action.</span></span>  

## <a name="posting-entries-to-a-closed-fiscal-year"></a><span data-ttu-id="3737a-143">Tapahtumien kirjaaminen suljettuun tilikauteen</span><span class="sxs-lookup"><span data-stu-id="3737a-143">Posting Entries to a Closed Fiscal Year</span></span>
<span data-ttu-id="3737a-144">Vaikka tilikausi on suljettu, voit silti kirjata tilikaudelle KP-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="3737a-144">Although a fiscal year is closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="3737a-145">Kun teet tämän, tapahtumat merkitään kirjatuiksi suljetulle tilikaudelle ja **Edellisen vuoden tapahtuma** -valintaruutu valitaan.</span><span class="sxs-lookup"><span data-stu-id="3737a-145">When you do, the entries are marked as posted to a closed fiscal year and the **Prior Year Entry** check box is selected.</span></span> <span data-ttu-id="3737a-146">Valintaruutu ei oletusarvoisesti näy sivulla, mutta voit lisätä sen.</span><span class="sxs-lookup"><span data-stu-id="3737a-146">By default, the check box is not displayed on the page, but you can add it.</span></span> <span data-ttu-id="3737a-147">Seuraavaksi suljetaan tuloslaskelmatilit ja siirretään vuoden tulostaseessa olevalle tilille.</span><span class="sxs-lookup"><span data-stu-id="3737a-147">The next steps are to close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="3737a-148">Toista nämä vaiheet aina, kun kirjaat tapahtumia suljetulle tilikaudelle.</span><span class="sxs-lookup"><span data-stu-id="3737a-148">Repeat these steps each time you post entries to a closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="3737a-149">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3737a-149">See Also</span></span>
[<span data-ttu-id="3737a-150">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="3737a-150">Closing the Books</span></span>](year-close-books.md)  
[<span data-ttu-id="3737a-151">Vuosien ja jaksojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="3737a-151">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="3737a-152">KP-raporttimallien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="3737a-152">How to Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
  






