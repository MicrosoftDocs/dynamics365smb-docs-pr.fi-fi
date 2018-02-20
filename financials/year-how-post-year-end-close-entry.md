---
title: "Vuositilinpäätöstapahtuman tarkasteleminen ja kirjaaminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten Sulje tuloslaskelma -eräajossa määritetty päiväkirja avataan. Sen jälkeen käsitellään vuositilinpäätöstapahtuman tarkastelua ja kirjaamista."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 78039e9387866ce17ff3be5a2ff509545e8439d2
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="1e6f3-103">Vuositilinpäätöstapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="1e6f3-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="1e6f3-104">Kun olet luonut vuositilinpäätöstapahtuman tai -tapahtumat **Sulje tuloslaskelma** -eräajolla, sinun on avattava eräajossa määrittämäsi päiväkirja sekä tarkistettava ja kirjattava tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="1e6f3-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="1e6f3-105">Kirjaa vuositilinpäätöstapahtuma</span><span class="sxs-lookup"><span data-stu-id="1e6f3-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="1e6f3-106">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1e6f3-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="1e6f3-107">Valitse **Yleinen päiväkirja** -ikkunassa **Erän nimi** kenttää ja valitse erä, joka sisältää tilinpäätöstapahtumat.</span><span class="sxs-lookup"><span data-stu-id="1e6f3-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="1e6f3-108">Tarkista tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="1e6f3-108">Review the entries.</span></span>
4. <span data-ttu-id="1e6f3-109">Kirjaa päiväkirja valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="1e6f3-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1e6f3-110">Jos havaitaan virhe, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="1e6f3-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="1e6f3-111">Jos kirjaus onnistuu, järjestelmä poistaa kirjatut tapahtumat päiväkirjasta.</span><span class="sxs-lookup"><span data-stu-id="1e6f3-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="1e6f3-112">Kirjaamisen jälkeen kullekin tuloslaskelmatilille kirjataan tapahtuma, jolloin tilin saldoksi tulee nolla ja vuoden tulos siirretään taseeseen.</span><span class="sxs-lookup"><span data-stu-id="1e6f3-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e6f3-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1e6f3-113">See Also</span></span>
[<span data-ttu-id="1e6f3-114">Kirjanpitojakson päättäminen</span><span class="sxs-lookup"><span data-stu-id="1e6f3-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="1e6f3-115">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="1e6f3-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="1e6f3-116">Sulje tuloslaskelma</span><span class="sxs-lookup"><span data-stu-id="1e6f3-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="1e6f3-117">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1e6f3-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

