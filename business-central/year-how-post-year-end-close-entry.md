---
title: Vuositilinpäätöstapahtuman kirjaaminen
description: Tässä ohjeaiheessa kerrotaan, miten Sulje tuloslaskelma -eräajossa määritetty päiväkirja avataan. Sen jälkeen käsitellään vuositilinpäätöstapahtuman tarkastelua ja kirjaamista.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c822685ae5723bc6b13f9fedad45dbddefdb956
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776590"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="d251d-103">Vuositilinpäätöstapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="d251d-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="d251d-104">Kun olet luonut vuositilinpäätöstapahtuman tai -tapahtumat **Sulje tuloslaskelma** -eräajolla, sinun on avattava eräajossa määrittämäsi päiväkirja sekä tarkistettava ja kirjattava tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="d251d-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="d251d-105">Organisaation työprosesseista riippuen voit päättää, suljetaanko vai eikö suljeta kirjanpitojaksoja ja tilikausia [!INCLUDE [prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="d251d-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d251d-106">Seuraavassa oletetaan, että tilikausi on suljettu *Kirjanpitojaksot*-valinnalla ja että tilikauden lopun tapahtuma on luotu **Sulje tuloslaskelma** -eräajon avulla, ja olet nyt valmis kirjaamaan tilikauden päättämistapahtuman yhdessä vastapääomatilitapahtumien kanssa.</span><span class="sxs-lookup"><span data-stu-id="d251d-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="d251d-107">Organisaatio voi valita, että se toimii eri tavalla, kuten kirjata vuoden lopun sulkemistapahtuman tilikauden päättämisen osana.</span><span class="sxs-lookup"><span data-stu-id="d251d-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="d251d-108">Kirjaa vuositilinpäätöstapahtuma</span><span class="sxs-lookup"><span data-stu-id="d251d-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="d251d-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d251d-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="d251d-110">Valitse **Yleinen päiväkirja** -sivulla **Erän nimi** kentässä erä, joka sisältää tilinpäätöstapahtumat.</span><span class="sxs-lookup"><span data-stu-id="d251d-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="d251d-111">Tarkista tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="d251d-111">Review the entries.</span></span>
4. <span data-ttu-id="d251d-112">Kirjaa päiväkirja valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d251d-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="d251d-113">Jos havaitaan virhe, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="d251d-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="d251d-114">Jos kirjaus onnistuu, järjestelmä poistaa kirjatut tapahtumat päiväkirjasta.</span><span class="sxs-lookup"><span data-stu-id="d251d-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="d251d-115">Kirjaamisen jälkeen kullekin tuloslaskelmatilille kirjataan tapahtuma, jolloin tilin saldoksi tulee nolla ja vuoden tulos siirretään taseeseen.</span><span class="sxs-lookup"><span data-stu-id="d251d-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="d251d-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d251d-116">See Also</span></span>

[<span data-ttu-id="d251d-117">Kirjanpitojakson päättäminen</span><span class="sxs-lookup"><span data-stu-id="d251d-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="d251d-118">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="d251d-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="d251d-119">Sulje tuloslaskelma</span><span class="sxs-lookup"><span data-stu-id="d251d-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="d251d-120">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d251d-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]