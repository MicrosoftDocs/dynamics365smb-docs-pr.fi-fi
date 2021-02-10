---
title: Tilikauden kirjanpitojaksojen sulkeminen | Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten tilikauden muodostavat kirjanpitojaksot suljetaan.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6acdc86afc195185f66836bf723c83d4a1647927
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755665"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="c40e1-103">Kirjanpitojakson päättäminen</span><span class="sxs-lookup"><span data-stu-id="c40e1-103">Close Accounting Periods</span></span>
<span data-ttu-id="c40e1-104">Kun tilikausi on ohi, sinun täytyy päättää tilikauteen sisältyvät kirjanpitojaksot.</span><span class="sxs-lookup"><span data-stu-id="c40e1-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="c40e1-105">Kirjanpitojakson päättäminen</span><span class="sxs-lookup"><span data-stu-id="c40e1-105">To close accounting periods</span></span>
1. <span data-ttu-id="c40e1-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c40e1-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="c40e1-107">Valitse **Kirjanpitojaksot**-sivulla **Sulje vuosi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c40e1-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="c40e1-108">Jos avoinna on useita tilikausia, niistä valitaan automaattisesti ensimmäinen suljettavaksi.</span><span class="sxs-lookup"><span data-stu-id="c40e1-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="c40e1-109">Näyttöön tulee sanoma, jossa näkyy suljettava kausi ja jossa selostetaan sulkemisen seuraukset.</span><span class="sxs-lookup"><span data-stu-id="c40e1-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="c40e1-110">Sulje vuosi valitsemalla **Kyllä** -painike.</span><span class="sxs-lookup"><span data-stu-id="c40e1-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="c40e1-111">Tilikausi on päätetty, ja **Suljettu**- ja **Pvm lukittu** -kentät on valittu kaikkien kauden jaksojen osalta.</span><span class="sxs-lookup"><span data-stu-id="c40e1-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="c40e1-112">Nyt tilikautta ei voi avata uudestaan, eikä valintamerkkiä voi poistaa **Suljettu**- tai **Pvm lukittu** -kentistä.</span><span class="sxs-lookup"><span data-stu-id="c40e1-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c40e1-113">Et voi sulkea tilikautta ennen kuin luot uuden.</span><span class="sxs-lookup"><span data-stu-id="c40e1-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="c40e1-114">Huomaa, että kun tilikausi on suljettu, et voi muuttaa seuraavan tilikauden aloituspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="c40e1-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="c40e1-115">Vaikka tilikausi on suljettu, voit silti kirjata tilikaudelle KP-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="c40e1-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="c40e1-116">Kun teet tämän, tapahtumat merkitään kirjatuiksi suljetulle tilikaudelle ja **Edellisen vuoden tapahtuma** -kenttä valitaan.</span><span class="sxs-lookup"><span data-stu-id="c40e1-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="c40e1-117">Kun tilikausi on suljettu, tuloslaskelmatilien saldo eli tilikauden tulos tulee siirtää tasetilille.</span><span class="sxs-lookup"><span data-stu-id="c40e1-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="c40e1-118">Tämä toistetaan aina, kun suljetulle tilikaudelle tehdään kirjauksia.</span><span class="sxs-lookup"><span data-stu-id="c40e1-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="c40e1-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c40e1-119">See Also</span></span>

[<span data-ttu-id="c40e1-120">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="c40e1-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="c40e1-121">Vuositilinpäätöstapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="c40e1-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="c40e1-122">Kirjanpitojaksojen ja tilikausien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="c40e1-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="c40e1-123">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c40e1-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
