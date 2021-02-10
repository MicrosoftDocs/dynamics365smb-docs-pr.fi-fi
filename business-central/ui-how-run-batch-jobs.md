---
title: Eräajon luominen ja suorittaminen | Microsoft Docs
description: Voit käsitellä ja päivittämää tietoja suorittamalla eräajon esimerkiksi kausiluontoisissa kirjanpitotehtävissä tai laskutoimituksissa.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 04ae13561f44d544d38b04e3a881a0e707b441b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760515"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="9203d-103">Eräajojen ja XMLportien suorittaminen</span><span class="sxs-lookup"><span data-stu-id="9203d-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="9203d-104">Eräajo on rutiini, joka käsittelee tietoja erissä, esimerkiksi **Valuuttakurssien muutoksen** eräajo.</span><span class="sxs-lookup"><span data-stu-id="9203d-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="9203d-105">Ohjelmassa on eräajoja, jotka suorittavat säännöllisiä kirjanpidon toimintoja, kuten tuloslaskelman sulkeminen tilikauden päättyessä.</span><span class="sxs-lookup"><span data-stu-id="9203d-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="9203d-106">Monet eräajot suorittavat laskutoimituksia. Tällaiset eräajot voivat esimerkiksi laskea viivästyskulut, vaihtokurssien muutoksen tai yksikköhinnat.</span><span class="sxs-lookup"><span data-stu-id="9203d-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="9203d-107">Eräajo vastaa raporttia, mutta se päivittää tiedot suoraan saatujen tulosten perusteella sen sijaan, että tulokset tulostettaisiin.</span><span class="sxs-lookup"><span data-stu-id="9203d-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="9203d-108">Voit aikatauluttaa eräajon suorittamisen.</span><span class="sxs-lookup"><span data-stu-id="9203d-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="9203d-109">Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="9203d-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="9203d-110">Eräajon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="9203d-110">To run a batch job</span></span>
1. <span data-ttu-id="9203d-111">Jos haluat avata liittyvän erätyön pyyntösivun, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna erätyön nimi ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9203d-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="9203d-112">Jos eräajolla on **Vaihtoehdot**-pikavälilehti, voit määrittää eräajon toiminnan täyttämällä kentät.</span><span class="sxs-lookup"><span data-stu-id="9203d-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="9203d-113">Sivulla voi olla yksi tai useita pikavälilehtiä ja suodattimia, joiden avulla voidaan rajoittaa eräajoon sisällytettyjä tietoa.</span><span class="sxs-lookup"><span data-stu-id="9203d-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="9203d-114">Voit syöttää kriteerin ehdotetuille suodattimille tai lisätä suodattimia.</span><span class="sxs-lookup"><span data-stu-id="9203d-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="9203d-115">Aloita eräajo valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="9203d-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="9203d-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9203d-116">See Also</span></span>
[<span data-ttu-id="9203d-117">Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen</span><span class="sxs-lookup"><span data-stu-id="9203d-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="9203d-118">Työjonojen käyttäminen ajoitustehtäviin</span><span class="sxs-lookup"><span data-stu-id="9203d-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="9203d-119">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9203d-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
