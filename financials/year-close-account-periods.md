---
title: Tilikauden kirjanpitojaksojen sulkeminen | Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten tilikauden muodostavat kirjanpitojaksot suljetaan.
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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e136195c7b89635ca85601cdae5047493c237d09
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="close-accounting-periods"></a><span data-ttu-id="af491-103">Kirjanpitojakson päättäminen</span><span class="sxs-lookup"><span data-stu-id="af491-103">Close Accounting Periods</span></span>
<span data-ttu-id="af491-104">Kun tilikausi on ohi, sinun täytyy päättää tilikauteen sisältyvät kirjanpitojaksot.</span><span class="sxs-lookup"><span data-stu-id="af491-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="af491-105">Kirjanpitojakson päättäminen</span><span class="sxs-lookup"><span data-stu-id="af491-105">To close accounting periods</span></span>
1. <span data-ttu-id="af491-106">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="af491-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="af491-107">Valitse **Kirjanpitojaksot**-ikkunassa **Sulje vuosi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="af491-107">In the **Accounting Periods** window, choose the **Close Year** action.</span></span>

    <span data-ttu-id="af491-108">Jos avoinna on useita tilikausia, niistä valitaan automaattisesti ensimmäinen suljettavaksi.</span><span class="sxs-lookup"><span data-stu-id="af491-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="af491-109">Näyttöön tulee sanoma, jossa näkyy suljettava kausi ja jossa selostetaan sulkemisen seuraukset.</span><span class="sxs-lookup"><span data-stu-id="af491-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="af491-110">Sulje vuosi valitsemalla **Kyllä** -painike.</span><span class="sxs-lookup"><span data-stu-id="af491-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="af491-111">Tilikausi on päätetty, ja **Suljettu**- ja **Pvm lukittu** -kentät on valittu kaikkien kauden jaksojen osalta.</span><span class="sxs-lookup"><span data-stu-id="af491-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="af491-112">Nyt tilikautta ei voi avata uudestaan, eikä valintamerkkiä voi poistaa **Suljettu**- tai **Pvm lukittu** -kentistä.</span><span class="sxs-lookup"><span data-stu-id="af491-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="af491-113">Et voi sulkea tilikautta ennen kuin luot uuden.</span><span class="sxs-lookup"><span data-stu-id="af491-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="af491-114">Huomaa, että kun tilikausi on suljettu, et voi muuttaa seuraavan tilikauden aloituspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="af491-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="af491-115">Vaikka tilikausi on suljettu, voit silti kirjata tilikaudelle KP-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="af491-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="af491-116">Kun teet tämän, tapahtumat merkitään kirjatuiksi suljetulle tilikaudelle ja **Edellisen vuoden tapahtuma** -kenttä valitaan.</span><span class="sxs-lookup"><span data-stu-id="af491-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="af491-117">Kun tilikausi on suljettu, tuloslaskelmatilien saldo eli tilikauden tulos tulee siirtää tasetilille.</span><span class="sxs-lookup"><span data-stu-id="af491-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="af491-118">Tämä toistetaan aina, kun suljetulle tilikaudelle tehdään kirjauksia.</span><span class="sxs-lookup"><span data-stu-id="af491-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="af491-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="af491-119">See Also</span></span>
[<span data-ttu-id="af491-120">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="af491-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="af491-121">Vuositilinpäätöstapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="af491-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="af491-122">Uuden tilikauden avaaminen</span><span class="sxs-lookup"><span data-stu-id="af491-122">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="af491-123">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af491-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

