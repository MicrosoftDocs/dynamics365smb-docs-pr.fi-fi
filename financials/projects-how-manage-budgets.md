---
title: "Projektin budjetin määrittäminen ja hallinta| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten resursseja suunnitellaan ja ennakoidaan sekä miten projektin kustannukset määritetään kullekin projektille."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e88eaebf65d950dcbb6c0296be24e68628a9494e
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="manage-job-budgets"></a><span data-ttu-id="7f61c-103">Projektibudjettien hallinta</span><span class="sxs-lookup"><span data-stu-id="7f61c-103">Manage Job Budgets</span></span>
<span data-ttu-id="7f61c-104">Jokaiselle projektille voi määrittää budjetin.</span><span class="sxs-lookup"><span data-stu-id="7f61c-104">You can set up a budget for each job.</span></span> <span data-ttu-id="7f61c-105">Budjettia käytetään projektille kohdistettavien resurssien suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="7f61c-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="7f61c-106">Budjetti voi olla joko yleisluonteinen budjetti, joka sisältää vain vähän tapahtumia, tai se voi sisältää monia tapahtumia, jotka on jaettu toimintotasoille.</span><span class="sxs-lookup"><span data-stu-id="7f61c-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="7f61c-107">Voit verrata budjetoituja summia projektipäiväkirjaan kirjattuun todelliseen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7f61c-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="7f61c-108">Kun valvot todellisen ja budjetoidun käytön välisiä eroja, voit hallita suoritettavaa projektia ja parantaa tulevien projektien laatua pienentämällä kustannusten aliarvioinnin riskiä.</span><span class="sxs-lookup"><span data-stu-id="7f61c-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="7f61c-109">Seuraavissa ohjeissa kerrotaan, miten budjetoituja kustannuksia arvioidaan suunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="7f61c-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="7f61c-110">Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="7f61c-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="7f61c-111">Projektin budjetoitujen kustannusten arvioiminen</span><span class="sxs-lookup"><span data-stu-id="7f61c-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="7f61c-112">Kun asiakas haluaa tietää sellaisen projektin hinnan, joka laskutetaan käytön perusteella, on määritettävä projektin budjetoidut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="7f61c-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="7f61c-113">Tähän käytetään **Projektitehtävärivit**-ikkunaa.</span><span class="sxs-lookup"><span data-stu-id="7f61c-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="7f61c-114">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7f61c-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7f61c-115">Avaa liittyvä projekti.</span><span class="sxs-lookup"><span data-stu-id="7f61c-115">Open a relevant job.</span></span>
3. <span data-ttu-id="7f61c-116">Valitse tehtävärivin tyypiksi Kirjaus ja valitse sitten **Projektin suunnittelurivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="7f61c-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="7f61c-117">Täytä tarvittaessa uuden rivin kentät.</span><span class="sxs-lookup"><span data-stu-id="7f61c-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="7f61c-118">Viittaa **Rivityyppi**-kentässä seuraaviin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="7f61c-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="7f61c-119">Rivityyppi</span><span class="sxs-lookup"><span data-stu-id="7f61c-119">Line Type</span></span> | <span data-ttu-id="7f61c-120">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="7f61c-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="7f61c-121">**Sekä budjetti että laskutettava**</span><span class="sxs-lookup"><span data-stu-id="7f61c-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="7f61c-122">Suunnitteluriville annetut kustannus- ja hintasummat ovat tämän suunnittelurivin budjetoidut kustannukset sekä laskutettava hinta.</span><span class="sxs-lookup"><span data-stu-id="7f61c-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="7f61c-123">Hinnaston summa laskutetaan.</span><span class="sxs-lookup"><span data-stu-id="7f61c-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="7f61c-124">**Budjetti**</span><span class="sxs-lookup"><span data-stu-id="7f61c-124">**Budget**</span></span> |<span data-ttu-id="7f61c-125">Asiakasta ei veloiteta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="7f61c-125">The customer is not charged for usage.</span></span> <span data-ttu-id="7f61c-126">Sitä ei voida koskaan siirtää laskuun, mutta käytetään edelleen KET-laskennassa.</span><span class="sxs-lookup"><span data-stu-id="7f61c-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="7f61c-127">**Laskutettava**</span><span class="sxs-lookup"><span data-stu-id="7f61c-127">**Billable**</span></span> |<span data-ttu-id="7f61c-128">Asiakasta veloitetaan käytöstä.</span><span class="sxs-lookup"><span data-stu-id="7f61c-128">The customer is charged for usage.</span></span> <span data-ttu-id="7f61c-129">Laskutettava määrä on määritetty kunkin ostorivin Laskuun siirrettävä määrä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7f61c-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="7f61c-130">Suunnittelurivin **Suunnittelupäivämäärä**-kenttä sisältää päivämäärän, jona suunnitteluriviin liittyvän käytön odotetaan olevan valmis.</span><span class="sxs-lookup"><span data-stu-id="7f61c-130">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="7f61c-131">Se on myös päivämäärä, jona suunnittelurivi voidaan siirtää myyntilaskuun ja kirjata.</span><span class="sxs-lookup"><span data-stu-id="7f61c-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="7f61c-132">Kun täytät **Määrä**-kentän, ohjelma laskee kaikki kokonaishinnan ja -kustannusten tiedot kyseistä suunnitteluriviä varten.</span><span class="sxs-lookup"><span data-stu-id="7f61c-132">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="7f61c-133">Voit muokata niitä milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="7f61c-133">You can edit them at any time.</span></span>

<span data-ttu-id="7f61c-134">**Projektikortti**-ikkunassa on nyt yhteenveto kunkin tehtävän budjetoiduista kokonaiskustannuksista, budjetoidusta hinnasta, laskutettavista kustannuksista ja laskutettavasta hinnasta.</span><span class="sxs-lookup"><span data-stu-id="7f61c-134">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="7f61c-135">Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="7f61c-135">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7f61c-136">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7f61c-136">See Also</span></span>
[<span data-ttu-id="7f61c-137">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="7f61c-137">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="7f61c-138">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="7f61c-138">Finance</span></span>](finance.md)  
<span data-ttu-id="7f61c-139">[Osto](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="7f61c-139">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="7f61c-140">[Myynti](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="7f61c-140">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="7f61c-141">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7f61c-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

