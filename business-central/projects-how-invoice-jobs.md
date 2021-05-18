---
title: Projektin laskuttaminen luomalla projektimyynnin lasku| Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten projektin kustannukset laskutetaan asiakkailta projektin edetessä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 873135d2fa6053b7101a999981fb3117ee8689ab
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938144"
---
# <a name="invoice-jobs"></a><span data-ttu-id="d6156-103">Projektien laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="d6156-103">Invoice Jobs</span></span>
<span data-ttu-id="d6156-104">Projektin aikana voi kertyä projektin kustannuksia resurssien käytöstä, materiaaleista ja projektiin liittyvistä ostoista.</span><span class="sxs-lookup"><span data-stu-id="d6156-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="d6156-105">Projektin edetessä nämä tapahtumat kirjataan projektipäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="d6156-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="d6156-106">On tärkeää, että kaikki kustannukset kirjataan projektipäiväkirjaan ennen asiakkaan laskuttamista.</span><span class="sxs-lookup"><span data-stu-id="d6156-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="d6156-107">Voit ostaa myös ulkoisia resursseja, jotka eivät liity työhön, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä.</span><span class="sxs-lookup"><span data-stu-id="d6156-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="d6156-108">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="d6156-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="d6156-109">Voit laskuttaa koko projektin **Projektitehtävärivit**-sivulla tai laskuttaa vain valitut laskutettavat rivit **Suunnittelurivit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d6156-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="d6156-110">Laskutuksen voi tehdä joko projektin valmistumisen jälkeen tai tietyin laskutusaikataulun mukaisin väliajoin projektin aikana.</span><span class="sxs-lookup"><span data-stu-id="d6156-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
> <span data-ttu-id="d6156-111">Jos valitset projektiin liittyvien ostojen ostoasiakirjojen **Projektin rivityyppi** -kentässä **Laskutettava**, projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutusta varten, luodaan.</span><span class="sxs-lookup"><span data-stu-id="d6156-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="d6156-112">Lisätietoja on kohdassa [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="d6156-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-multiple-job-sales-invoices"></a><span data-ttu-id="d6156-113">Voit luoda monta projektin myyntilaskua</span><span class="sxs-lookup"><span data-stu-id="d6156-113">To create multiple job sales invoices</span></span>
<span data-ttu-id="d6156-114">Voit luoda asiakkaalle laskun projektista tai vähintään yhdestä projektitehtävästä, kun laskutettava työ on valmis tai kun laskutusaikatauluun perustuva laskutuspäivämäärä on saavutettu.</span><span class="sxs-lookup"><span data-stu-id="d6156-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="d6156-115">Seuraavassa kerrotaan, miten eräajoa käytetään useiden projektien laskuttamisessa.</span><span class="sxs-lookup"><span data-stu-id="d6156-115">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="d6156-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo projektin myyntilasku** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d6156-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d6156-117">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="d6156-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d6156-118">Määritä suodattimet, jos haluat rajata erätyön käsittelemien projektien määrää.</span><span class="sxs-lookup"><span data-stu-id="d6156-118">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="d6156-119">Luo laskut valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6156-119">Choose the **OK** button to create the invoices.</span></span>  

<span data-ttu-id="d6156-120">Voit tarkastella ja kirjata luotuja laskuja **Myyntilaskut**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="d6156-120">You can review and post created invoices in the **Sales Invoices** window.</span></span>

> [!NOTE]
> <span data-ttu-id="d6156-121">Vaihtoehtoisesti voit laskuttaa Projektit-sivulla asiakasta valitsemalla projektin ja valitsemalla sitten **Luo projektin myyntilasku** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="d6156-121">Alternatively, invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a><span data-ttu-id="d6156-122">Projektin myyntilaskun luominen ja kirjaaminen projektin suunnitteluriveistä</span><span class="sxs-lookup"><span data-stu-id="d6156-122">To create and post job sales invoice from job planning lines</span></span>
<span data-ttu-id="d6156-123">Voit luoda laskun projektin suunnitteluriveiltä ja määrittää samalla nimikkeen määrän, resurssin tai KP-tilin, jonka haluat laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="d6156-123">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="d6156-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työt** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d6156-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6156-125">Avaa liittyvä projekti.</span><span class="sxs-lookup"><span data-stu-id="d6156-125">Open a relevant job.</span></span>
3. <span data-ttu-id="d6156-126">Valitse projektitehtävä, jonka **Projektitehtävätyyppi**-kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d6156-126">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="d6156-127">Annan projektin suunnittelurivin **Laskuun siirrettävä määrä** -kentässä nimikkeen, resurssin tai pääkirjanpidon tilin tyyppi, jonka haluat laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="d6156-127">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="d6156-128">Valitse **Luo myyntilasku** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d6156-128">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="d6156-129">Anna **Luo projektin myyntilasku** -sivulla kirjauspäivämäärä. Määritä, haluatko luoda uuden laskun vai kohdistaa tämän laskun aiemmin luotuun laskuun.</span><span class="sxs-lookup"><span data-stu-id="d6156-129">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="d6156-130">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="d6156-130">Choose the **OK** button.</span></span>  
8. <span data-ttu-id="d6156-131">Valitse **Projektin suunnittelurivit** -sivulla **Myyntilaskut/hyvityslaskut**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d6156-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="d6156-132">Avautuvassa **Myyntilasku**-sivulla näkyy laskuun siirretty määrä.</span><span class="sxs-lookup"><span data-stu-id="d6156-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>
9. <span data-ttu-id="d6156-133">Tee tarvittavat muutokset ja valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d6156-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d6156-134">Projektiin liittyvän myyntihyvityslaskun luominen, tarkistaminen ja kirjaaminen tapahtuu vastaavalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="d6156-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>


## <a name="see-also"></a><span data-ttu-id="d6156-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d6156-135">See Also</span></span>
[<span data-ttu-id="d6156-136">Projektien hallinta</span><span class="sxs-lookup"><span data-stu-id="d6156-136">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="d6156-137">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="d6156-137">Finance</span></span>](finance.md)  
<span data-ttu-id="d6156-138">[Osto](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="d6156-138">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="d6156-139">[Myynti](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="d6156-139">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="d6156-140">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6156-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
