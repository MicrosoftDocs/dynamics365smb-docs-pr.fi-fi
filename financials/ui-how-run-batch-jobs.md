---
title: "Eräajon luominen ja suorittaminen | Microsoft Docs"
description: "Voit käsitellä ja päivittämää tietoja suorittamalla eräajon esimerkiksi kausiluontoisissa kirjanpitotehtävissä tai laskutoimituksissa."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6844d5fe3efba5349eef166161c5956116bc7fc0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-run-batch-jobs"></a><span data-ttu-id="7966c-103">Eräajojen ajaminen</span><span class="sxs-lookup"><span data-stu-id="7966c-103">How to: Run Batch Jobs</span></span>
<span data-ttu-id="7966c-104">Eräajo on rutiini, joka käsittelee tietoja erissä, esimerkiksi **Valuuttakurssien muutoksen** eräajo.</span><span class="sxs-lookup"><span data-stu-id="7966c-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="7966c-105">Ohjelmassa on eräajoja, jotka suorittavat säännöllisiä kirjanpidon toimintoja, kuten tuloslaskelman sulkeminen tilikauden päättyessä.</span><span class="sxs-lookup"><span data-stu-id="7966c-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="7966c-106">Monet eräajot suorittavat laskutoimituksia. Tällaiset eräajot voivat esimerkiksi laskea viivästyskulut, vaihtokurssien muutoksen tai yksikköhinnat.</span><span class="sxs-lookup"><span data-stu-id="7966c-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="7966c-107">Eräajo vastaa raporttia, mutta se päivittää tiedot suoraan saatujen tulosten perusteella sen sijaan, että tulokset tulostettaisiin.</span><span class="sxs-lookup"><span data-stu-id="7966c-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="7966c-108">Eräajon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="7966c-108">To run a batch job</span></span>
1. <span data-ttu-id="7966c-109">Voit avata kyseisten eräajojen pyyntöikkunan valitsemalla ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvakkeen, antamalla eräajon nimen ja valitsemalla aiheeseen liittyvän linkin.</span><span class="sxs-lookup"><span data-stu-id="7966c-109">To open the request window for the relevant batch job, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="7966c-110">Jos eräajolla on **Vaihtoehdot**-pikavälilehti, voit määrittää eräajon toiminnan täyttämällä kentät.</span><span class="sxs-lookup"><span data-stu-id="7966c-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="7966c-111">Ikkunassa voi olla yksi tai useita pikavälilehtiä ja suodattimia, joiden avulla voidaan rajoittaa eräajoon sisällytettyjä tietoa.</span><span class="sxs-lookup"><span data-stu-id="7966c-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="7966c-112">Voit syöttää kriteerin ehdotetuille suodattimille tai lisätä suodattimia.</span><span class="sxs-lookup"><span data-stu-id="7966c-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="7966c-113">Aloita eräajo valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="7966c-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="7966c-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7966c-114">See Also</span></span>
[<span data-ttu-id="7966c-115">Suodattimen ehtojen antaminen</span><span class="sxs-lookup"><span data-stu-id="7966c-115">Entering Criteria in Filters</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="7966c-116">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7966c-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

