---
title: Projektin laskuttaminen luomalla projektimyynnin lasku| Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten projektin kustannukset laskutetaan asiakkailta projektin edetessä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 368b0b1edf1105045a365d8d5ac523c88955ad8a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758740"
---
# <a name="invoice-jobs"></a><span data-ttu-id="c1a8e-103">Projektien laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="c1a8e-103">Invoice Jobs</span></span>
<span data-ttu-id="c1a8e-104">Projektin aikana voi kertyä projektin kustannuksia resurssien käytöstä, materiaaleista ja projektiin liittyvistä ostoista.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="c1a8e-105">Projektin edetessä nämä tapahtumat kirjataan projektipäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="c1a8e-106">On tärkeää, että kaikki kustannukset kirjataan projektipäiväkirjaan ennen asiakkaan laskuttamista.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="c1a8e-107">Voit ostaa myös ulkoisia resursseja, jotka eivät liity työhön, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="c1a8e-108">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="c1a8e-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="c1a8e-109">Voit laskuttaa koko projektin **Projektitehtävärivit**-sivulla tai laskuttaa vain valitut laskutettavat rivit **Suunnittelurivit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="c1a8e-110">Laskutuksen voi tehdä joko projektin valmistumisen jälkeen tai tietyin laskutusaikataulun mukaisin väliajoin projektin aikana.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
> <span data-ttu-id="c1a8e-111">Jos valitset projektiin liittyvien ostojen ostoasiakirjojen **Projektin rivityyppi** -kentässä **Laskutettava**, projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutusta varten, luodaan.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="c1a8e-112">Lisätietoja on kohdassa [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="c1a8e-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-multiple-job-sales-invoices"></a><span data-ttu-id="c1a8e-113">Voit luoda monta projektin myyntilaskua</span><span class="sxs-lookup"><span data-stu-id="c1a8e-113">To create multiple job sales invoices</span></span>
<span data-ttu-id="c1a8e-114">Voit luoda asiakkaalle laskun projektista tai vähintään yhdestä projektitehtävästä, kun laskutettava työ on valmis tai kun laskutusaikatauluun perustuva laskutuspäivämäärä on saavutettu.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="c1a8e-115">Seuraavassa kerrotaan, miten eräajoa käytetään useiden projektien laskuttamisessa.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-115">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="c1a8e-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo projektin myyntilasku** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c1a8e-117">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="c1a8e-118">Määritä suodattimet, jos haluat rajata erätyön käsittelemien projektien määrää.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-118">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="c1a8e-119">Luo laskut valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-119">Choose the **OK** button to create the invoices.</span></span>  

<span data-ttu-id="c1a8e-120">Voit tarkastella ja kirjata luotuja laskuja **Myyntilaskut**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-120">You can review and post created invoices in the **Sales Invoices** window.</span></span>

> [!NOTE]
> <span data-ttu-id="c1a8e-121">Vaihtoehtoisesti voit laskuttaa Projektit-sivulla asiakasta valitsemalla projektin ja valitsemalla sitten **Luo projektin myyntilasku** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-121">Alternatively, invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a><span data-ttu-id="c1a8e-122">Projektin myyntilaskun luominen ja kirjaaminen projektin suunnitteluriveistä</span><span class="sxs-lookup"><span data-stu-id="c1a8e-122">To create and post job sales invoice from job planning lines</span></span>
<span data-ttu-id="c1a8e-123">Voit luoda laskun projektin suunnitteluriveiltä ja määrittää samalla nimikkeen määrän, resurssin tai KP-tilin, jonka haluat laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-123">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="c1a8e-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työt** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="c1a8e-125">Avaa liittyvä projekti.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-125">Open a relevant job.</span></span>
3. <span data-ttu-id="c1a8e-126">Valitse projektitehtävä, jonka **Projektitehtävätyyppi**-kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-126">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="c1a8e-127">Annan projektin suunnittelurivin **Laskuun siirrettävä määrä** -kentässä nimikkeen, resurssin tai pääkirjanpidon tilin tyyppi, jonka haluat laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-127">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="c1a8e-128">Valitse **Luo myyntilasku** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-128">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="c1a8e-129">Anna **Luo projektin myyntilasku** -sivulla kirjauspäivämäärä. Määritä, haluatko luoda uuden laskun vai kohdistaa tämän laskun aiemmin luotuun laskuun.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-129">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="c1a8e-130">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-130">Choose the **OK** button.</span></span>  
8. <span data-ttu-id="c1a8e-131">Valitse **Projektin suunnittelurivit** -sivulla **Myyntilaskut/hyvityslaskut**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="c1a8e-132">Avautuvassa **Myyntilasku**-sivulla näkyy laskuun siirretty määrä.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>
9. <span data-ttu-id="c1a8e-133">Tee tarvittavat muutokset ja valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c1a8e-134">Projektiin liittyvän myyntihyvityslaskun luominen, tarkistaminen ja kirjaaminen tapahtuu vastaavalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="c1a8e-135">Projektin valmistumistapahtumien laskeminen ja kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="c1a8e-135">To calculate and post job completion entries</span></span>
<span data-ttu-id="c1a8e-136">Kun olet saanut kaikki projektin toimenpiteet, kuten käytön kirjauksen ja laskutuksen, valmiiksi, projekti on päivitettävä **tilaan** **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-136">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="c1a8e-137">Tämän jälkeen mahdollinen kirjanpitoon kirjattu KET peruuntuu.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-137">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="c1a8e-138">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työt** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c1a8e-139">Valitse avoin projekti ja valitse sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-139">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="c1a8e-140">Valitse **Tila**-kentässä **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-140">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="c1a8e-141">Laske ja kirjaa KET ohjattujen vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-141">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="c1a8e-142">Vaihtoehtoisesti voit tehdä toiminnot manuaalisesti vaiheiden 5 ja 6 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-142">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="c1a8e-143">Valitse **Laske KET** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-143">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="c1a8e-144">Täytä **Laske projektin KET** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-144">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="c1a8e-145">Erätyön luomien projektin KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-145">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="c1a8e-146">Valitse **Kirjaa projektin KET kirjanpitoon** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-146">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="c1a8e-147">Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-147">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="c1a8e-148">Erätyön luomien projektin pääkirjanpidon KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.</span><span class="sxs-lookup"><span data-stu-id="c1a8e-148">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1a8e-149">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c1a8e-149">See Also</span></span>
[<span data-ttu-id="c1a8e-150">Projektien hallinta</span><span class="sxs-lookup"><span data-stu-id="c1a8e-150">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="c1a8e-151">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="c1a8e-151">Finance</span></span>](finance.md)  
<span data-ttu-id="c1a8e-152">[Osto](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="c1a8e-152">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="c1a8e-153">[Myynti](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="c1a8e-153">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="c1a8e-154">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c1a8e-154">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
