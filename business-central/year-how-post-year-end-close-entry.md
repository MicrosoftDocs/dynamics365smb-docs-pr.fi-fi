---
title: Vuositilinpäätöstapahtuman tarkasteleminen ja kirjaaminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten Sulje tuloslaskelma -eräajossa määritetty päiväkirja avataan. Sen jälkeen käsitellään vuositilinpäätöstapahtuman tarkastelua ja kirjaamista.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ca92d9535a9a15d46d93de6febdfd169c3d7d17a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755540"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="e5395-103">Vuositilinpäätöstapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="e5395-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="e5395-104">Kun olet luonut vuositilinpäätöstapahtuman tai -tapahtumat **Sulje tuloslaskelma** -eräajolla, sinun on avattava eräajossa määrittämäsi päiväkirja sekä tarkistettava ja kirjattava tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="e5395-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="e5395-105">Kirjaa vuositilinpäätöstapahtuma</span><span class="sxs-lookup"><span data-stu-id="e5395-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="e5395-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e5395-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="e5395-107">Valitse **Yleinen päiväkirja** -sivulla **Erän nimi** kentässä erä, joka sisältää tilinpäätöstapahtumat.</span><span class="sxs-lookup"><span data-stu-id="e5395-107">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="e5395-108">Tarkista tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="e5395-108">Review the entries.</span></span>
4. <span data-ttu-id="e5395-109">Kirjaa päiväkirja valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e5395-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e5395-110">Jos havaitaan virhe, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="e5395-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="e5395-111">Jos kirjaus onnistuu, järjestelmä poistaa kirjatut tapahtumat päiväkirjasta.</span><span class="sxs-lookup"><span data-stu-id="e5395-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="e5395-112">Kirjaamisen jälkeen kullekin tuloslaskelmatilille kirjataan tapahtuma, jolloin tilin saldoksi tulee nolla ja vuoden tulos siirretään taseeseen.</span><span class="sxs-lookup"><span data-stu-id="e5395-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5395-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e5395-113">See Also</span></span>
[<span data-ttu-id="e5395-114">Kirjanpitojakson päättäminen</span><span class="sxs-lookup"><span data-stu-id="e5395-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="e5395-115">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="e5395-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="e5395-116">Sulje tuloslaskelma</span><span class="sxs-lookup"><span data-stu-id="e5395-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="e5395-117">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e5395-117">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
