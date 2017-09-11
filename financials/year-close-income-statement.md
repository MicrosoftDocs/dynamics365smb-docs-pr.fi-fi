---
title: Tuloslaskelmatilien sulkeminen | Microsoft Docs
description: "Vuositilinpäätöksessä on suoritettava Sulje tuloslaskelma -etätyö, jolla suljetaan tilikauden muodostavat kirjanpitojaksot."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6ddd7b504f6faa856e92c336f889ad08db0b3d8b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-close-income-statement-accounts"></a><span data-ttu-id="2c1ef-103">Toimintaohje: Tuloslaskelmatilien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="2c1ef-103">How to: Close Income Statement Accounts</span></span>
<span data-ttu-id="2c1ef-104">Kun tilikausi on ohi, sinun täytyy sulkea tilikauteen sisältyvät kirjanpitojaksot.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-104">When a fiscal year is over, you must close the periods that comprise it.</span></span> <span data-ttu-id="2c1ef-105">Voit tehdä sen ajamalla **Sulje tuloslaskelma** -eräajon.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-105">To do this, you run the **Close Income Statement** batch job.</span></span> <span data-ttu-id="2c1ef-106">Tämä ajo siirtää vuoden tuloksen tilille taseeseen ja sulkee tuloslaskelmatilit.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-106">This job transfers the year's result to an account in the balance sheet and closes the income statement accounts.</span></span> <span data-ttu-id="2c1ef-107">Voit tehdä tämän luomalla rivejä päiväkirjaan, jonka sitten voit kirjata.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-107">You do this by creating lines in a journal, which you then can post.</span></span>

## <a name="to-run-the-close-income-statement-batch-job"></a><span data-ttu-id="2c1ef-108">Sulje tuloslaskelma -eräajon ajaminen</span><span class="sxs-lookup"><span data-stu-id="2c1ef-108">To run the Close Income Statement batch job</span></span>
1. <span data-ttu-id="2c1ef-109">Sulje tilikausi.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-109">Close the fiscal year.</span></span> <span data-ttu-id="2c1ef-110">Tilikausi täytyy sulkea ennen eräajon suorittamista.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-110">The fiscal year must closed before the batch job can be run.</span></span> <span data-ttu-id="2c1ef-111">Lisätietoja on kohdassa [Toimintaohje: Kirjanpitojakson päättäminen](year-close-account-periods.md).</span><span class="sxs-lookup"><span data-stu-id="2c1ef-111">For more information, see [How to: Close Accounting Periods](year-close-account-periods.md).</span></span>
2. <span data-ttu-id="2c1ef-112">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sulje tuloslaskelma** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Close Income Statement**, and then choose the related link.</span></span>
3. <span data-ttu-id="2c1ef-113">Suorita eräajo valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-113">Choose the **OK** button to run the batch job.</span></span>

## <a name="about-the-close-income-statement-batch-job"></a><span data-ttu-id="2c1ef-114">Tietoja Sulje tuloslaskelma -eräajosta</span><span class="sxs-lookup"><span data-stu-id="2c1ef-114">About the Close Income Statement Batch Job</span></span>
<span data-ttu-id="2c1ef-115">Eräajo käsittelee kaikki Tuloslaskelma-tyyppiset kirjanpitotilit ja luo niiden saldojen vastatapahtumat.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-115">The batch job processes all general accounts of the income statement type and creates entries that cancel out their respective balances.</span></span> <span data-ttu-id="2c1ef-116">Jokainen tapahtuma on tilikauden kaikkien pääkirjanpidon tilin tapahtumien summa.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-116">That is, each entry is the sum of all the general ledger entries on the account in the fiscal year.</span></span> <span data-ttu-id="2c1ef-117">Nämä uudet tapahtumat sijoitetaan päiväkirjaan, missä sinun täytyy määrittää vastatili ja jakamattoman voiton tili taseeseen ennen kirjausta.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-117">These new entries are placed in a journal in which you must specify a balancing account and retained earnings account in the balance sheet before you post.</span></span> <span data-ttu-id="2c1ef-118">Kun päiväkirja on kirjattu, jokaiselle tuloslaskelmatilille kirjataan tapahtuma, jotta tilin saldoksi tulee nolla, ja samalla vuoden tulos siirretään taseeseen.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-118">When you post the journal, an entry is posted to each income statement account so that its balance becomes zero and at the same time the year's result is transferred to the balance sheet.</span></span>

<span data-ttu-id="2c1ef-119">Sinun täytyy itse kirjata päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-119">You must post the journal yourself.</span></span> <span data-ttu-id="2c1ef-120">Eräajo ei kirjaa niitä automaattisesti, ellei käytetä lisäraportointivaluuttaa.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-120">The batch job does not post the entries automatically, except when an additional reporting currency is being used.</span></span> <span data-ttu-id="2c1ef-121">Lisäraportointivaluuttaa käytettäessä eräajo kirjaa tapahtumat suoraan pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-121">When an additional reporting currency is being used, the batch job posts entries directly to the general ledger.</span></span>

<span data-ttu-id="2c1ef-122">Niillä riveillä, jotka eräajo syöttää päiväkirjan riveille, on aina tilikauden päättämispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-122">The date on the lines that the batch job inserts in the journal is always a closing date for the fiscal year.</span></span> <span data-ttu-id="2c1ef-123">Tilikauden päättämispäivä on kuvitteellinen päivä tilikauden viimeisen päivän ja seuraavan tilikauden ensimmäisen päivän välissä.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-123">The closing date is a fictitious date between the last day of the old fiscal year and the first day of the new year.</span></span> <span data-ttu-id="2c1ef-124">Tilikauden päättämispäivän kirjauksesta on se hyöty, että oikeat saldot säilyvät tilikauden tavallisissa päivämäärissä.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-124">The advantage of posting on a closing date is that you maintain the correct balances for the ordinary dates of the fiscal year.</span></span>

<span data-ttu-id="2c1ef-125">**Sulje tuloslaskelma** -eräajoa voi käyttää monta kertaa.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-125">The **Close Income Statement** batch job can be used several times.</span></span> <span data-ttu-id="2c1ef-126">Jos suoritat eräajon uudelleen, voit kirjata edelliselle tilikaudelle vielä tuloslaskelmatilien päättämisen jälkeenkin.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-126">You can post in a previous fiscal year, even after the income statement accounts have been closed, if you run the batch job again.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c1ef-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2c1ef-127">See Also</span></span>
[<span data-ttu-id="2c1ef-128">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="2c1ef-128">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="2c1ef-129">Toimintaohje: Vuositilinpäätöstapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="2c1ef-129">How to: Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="2c1ef-130">Toimintaohje: Uuden tilikauden avaaminen</span><span class="sxs-lookup"><span data-stu-id="2c1ef-130">How to: Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="2c1ef-131">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c1ef-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

