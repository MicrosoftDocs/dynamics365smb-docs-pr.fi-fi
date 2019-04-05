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
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 260cd7761b130bbe3748de3cc109a9f4f56c1384
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "853256"
---
# <a name="run-batch-jobs"></a><span data-ttu-id="4ebec-103">Eräajojen ajaminen</span><span class="sxs-lookup"><span data-stu-id="4ebec-103">Run Batch Jobs</span></span>
<span data-ttu-id="4ebec-104">Eräajo on rutiini, joka käsittelee tietoja erissä, esimerkiksi **Valuuttakurssien muutoksen** eräajo.</span><span class="sxs-lookup"><span data-stu-id="4ebec-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="4ebec-105">Ohjelmassa on eräajoja, jotka suorittavat säännöllisiä kirjanpidon toimintoja, kuten tuloslaskelman sulkeminen tilikauden päättyessä.</span><span class="sxs-lookup"><span data-stu-id="4ebec-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="4ebec-106">Monet eräajot suorittavat laskutoimituksia. Tällaiset eräajot voivat esimerkiksi laskea viivästyskulut, vaihtokurssien muutoksen tai yksikköhinnat.</span><span class="sxs-lookup"><span data-stu-id="4ebec-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="4ebec-107">Eräajo vastaa raporttia, mutta se päivittää tiedot suoraan saatujen tulosten perusteella sen sijaan, että tulokset tulostettaisiin.</span><span class="sxs-lookup"><span data-stu-id="4ebec-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="4ebec-108">Eräajon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="4ebec-108">To run a batch job</span></span>
1. <span data-ttu-id="4ebec-109">Jos haluat avata liittyvän erätyön pyyntösivun, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna erätyön nimi ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4ebec-109">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="4ebec-110">Jos eräajolla on **Vaihtoehdot**-pikavälilehti, voit määrittää eräajon toiminnan täyttämällä kentät.</span><span class="sxs-lookup"><span data-stu-id="4ebec-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="4ebec-111">Sivulla voi olla yksi tai useita pikavälilehtiä ja suodattimia, joiden avulla voidaan rajoittaa eräajoon sisällytettyjä tietoa.</span><span class="sxs-lookup"><span data-stu-id="4ebec-111">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="4ebec-112">Voit syöttää kriteerin ehdotetuille suodattimille tai lisätä suodattimia.</span><span class="sxs-lookup"><span data-stu-id="4ebec-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="4ebec-113">Aloita eräajo valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ebec-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ebec-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4ebec-114">See Also</span></span>
[<span data-ttu-id="4ebec-115">Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen</span><span class="sxs-lookup"><span data-stu-id="4ebec-115">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="4ebec-116">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4ebec-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
