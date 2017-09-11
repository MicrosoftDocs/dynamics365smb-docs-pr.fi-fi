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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0e480c67ddb2acd5e98799c98cb1cd9d972889df
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-manage-job-budgets"></a><span data-ttu-id="c1008-103">Toimintaohje: Projektibudjettien hallinta</span><span class="sxs-lookup"><span data-stu-id="c1008-103">How to: Manage Job Budgets</span></span>
<span data-ttu-id="c1008-104">Jokaiselle projektille voi määrittää budjetin.</span><span class="sxs-lookup"><span data-stu-id="c1008-104">You can set up a budget for each job.</span></span> <span data-ttu-id="c1008-105">Budjettia käytetään projektille kohdistettavien resurssien suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="c1008-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="c1008-106">Budjetti voi olla joko yleisluonteinen budjetti, joka sisältää vain vähän tapahtumia, tai se voi sisältää monia tapahtumia, jotka on jaettu toimintotasoille.</span><span class="sxs-lookup"><span data-stu-id="c1008-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="c1008-107">Voit verrata budjetoituja summia projektipäiväkirjaan kirjattuun todelliseen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="c1008-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="c1008-108">Kun valvot todellisen ja budjetoidun käytön välisiä eroja, voit hallita suoritettavaa projektia ja parantaa tulevien projektien laatua pienentämällä kustannusten aliarvioinnin riskiä.</span><span class="sxs-lookup"><span data-stu-id="c1008-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="c1008-109">Seuraavissa ohjeissa kerrotaan, miten budjetoituja kustannuksia arvioidaan suunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="c1008-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="c1008-110">Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Toimintaohje: Projektien käytön kirjaaminen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="c1008-110">For information about recording budgeted versus actual job prices and costs, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <span data-ttu-id="c1008-111"><a name="JobBudgetCosts"></a> Projektin budjetoitujen kustannusten arvioiminen</span><span class="sxs-lookup"><span data-stu-id="c1008-111"><a name="JobBudgetCosts"></a> To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="c1008-112">Kun asiakas haluaa tietää sellaisen projektin hinnan, joka laskutetaan käytön perusteella, on määritettävä projektin budjetoidut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="c1008-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="c1008-113">Tähän käytetään **Projektitehtävärivit**-ikkunaa.</span><span class="sxs-lookup"><span data-stu-id="c1008-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="c1008-114">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c1008-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c1008-115">Avaa liittyvä projekti.</span><span class="sxs-lookup"><span data-stu-id="c1008-115">Open a relevant job.</span></span>
3. <span data-ttu-id="c1008-116">Valitse tehtävärivin tyypiksi Kirjaus ja valitse sitten **Projektin suunnittelurivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1008-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="c1008-117">Täytä tarvittaessa uuden rivin kentät.</span><span class="sxs-lookup"><span data-stu-id="c1008-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="c1008-118">Viittaa **Rivityyppi**-kentässä seuraaviin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="c1008-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="c1008-119">Rivityyppi</span><span class="sxs-lookup"><span data-stu-id="c1008-119">Line Type</span></span> | <span data-ttu-id="c1008-120">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="c1008-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="c1008-121">**Sekä budjetti että laskutettava**</span><span class="sxs-lookup"><span data-stu-id="c1008-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="c1008-122">Suunnitteluriville annetut kustannus- ja hintasummat ovat tämän suunnittelurivin budjetoidut kustannukset sekä laskutettava hinta.</span><span class="sxs-lookup"><span data-stu-id="c1008-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="c1008-123">Hinnaston summa laskutetaan.</span><span class="sxs-lookup"><span data-stu-id="c1008-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="c1008-124">**Budjetti**</span><span class="sxs-lookup"><span data-stu-id="c1008-124">**Budget**</span></span> |<span data-ttu-id="c1008-125">Asiakasta ei veloiteta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c1008-125">The customer is not charged for usage.</span></span> <span data-ttu-id="c1008-126">Sitä ei voida koskaan siirtää laskuun, mutta käytetään edelleen KET-laskennassa.</span><span class="sxs-lookup"><span data-stu-id="c1008-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="c1008-127">**Laskutettava**</span><span class="sxs-lookup"><span data-stu-id="c1008-127">**Billable**</span></span> |<span data-ttu-id="c1008-128">Asiakasta veloitetaan käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c1008-128">The customer is charged for usage.</span></span> <span data-ttu-id="c1008-129">Käyttö siirretään laskuun Laskuun siirrettävä määrä -kentässä</span><span class="sxs-lookup"><span data-stu-id="c1008-129">Usage is transferred to the invoice, based on the quantity specified in the Qty.</span></span> <span data-ttu-id="c1008-130">määritetyn määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="c1008-130">to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="c1008-131">Suunnittelurivin **Suunnittelupäivämäärä**-kenttä sisältää päivämäärän, jona suunnitteluriviin liittyvän käytön odotetaan olevan valmis.</span><span class="sxs-lookup"><span data-stu-id="c1008-131">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="c1008-132">Se on myös päivämäärä, jona suunnittelurivi voidaan siirtää myyntilaskuun ja kirjata.</span><span class="sxs-lookup"><span data-stu-id="c1008-132">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="c1008-133">Kun täytät **Määrä**-kentän, ohjelma laskee kaikki kokonaishinnan ja -kustannusten tiedot kyseistä suunnitteluriviä varten.</span><span class="sxs-lookup"><span data-stu-id="c1008-133">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="c1008-134">Voit muokata niitä milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="c1008-134">You can edit them at any time.</span></span>

<span data-ttu-id="c1008-135">**Projektikortti**-ikkunassa on nyt yhteenveto kunkin tehtävän budjetoiduista kokonaiskustannuksista, budjetoidusta hinnasta, laskutettavista kustannuksista ja laskutettavasta hinnasta.</span><span class="sxs-lookup"><span data-stu-id="c1008-135">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="c1008-136">Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Toimintaohje: Projektien käytön kirjaaminen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="c1008-136">For information about recording budgeted versus actual job prices and costs, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1008-137">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c1008-137">See Also</span></span>
[<span data-ttu-id="c1008-138">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="c1008-138">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="c1008-139">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="c1008-139">Finance</span></span>](finance.md)  
<span data-ttu-id="c1008-140">[Osto](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="c1008-140">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="c1008-141">[Myynti](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="c1008-141">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="c1008-142">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c1008-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

