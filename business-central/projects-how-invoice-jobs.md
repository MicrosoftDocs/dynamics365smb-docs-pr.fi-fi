---
title: Projektin laskuttaminen luomalla projektimyynnin lasku| Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten projektin kustannukset laskutetaan asiakkailta projektin edetessä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 277e5e6cb212202f930ed49012184aa67a23d03f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191257"
---
# <a name="invoice-jobs"></a><span data-ttu-id="f009f-103">Projektien laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="f009f-103">Invoice Jobs</span></span>
<span data-ttu-id="f009f-104">Projektin aikana voi kertyä projektin kustannuksia resurssien käytöstä, materiaaleista ja projektiin liittyvistä ostoista.</span><span class="sxs-lookup"><span data-stu-id="f009f-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="f009f-105">Projektin edetessä nämä tapahtumat kirjataan projektipäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="f009f-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="f009f-106">On tärkeää, että kaikki kustannukset kirjataan projektipäiväkirjaan ennen asiakkaan laskuttamista.</span><span class="sxs-lookup"><span data-stu-id="f009f-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="f009f-107">Voit ostaa myös ulkoisia resursseja, jotka eivät liity työhön, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä.</span><span class="sxs-lookup"><span data-stu-id="f009f-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="f009f-108">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="f009f-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="f009f-109">Voit laskuttaa koko projektin **Projektitehtävärivit**-sivulla tai laskuttaa vain valitut laskutettavat rivit **Suunnittelurivit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f009f-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="f009f-110">Laskutuksen voi tehdä joko projektin valmistumisen jälkeen tai tietyin laskutusaikataulun mukaisin väliajoin projektin aikana.</span><span class="sxs-lookup"><span data-stu-id="f009f-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f009f-111">Jos valitset projektiin liittyvien ostojen ostoasiakirjojen **Projektin rivityyppi** -kentässä **Laskutettava**, projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutusta varten, luodaan.</span><span class="sxs-lookup"><span data-stu-id="f009f-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="f009f-112">Lisätietoja on kohdassa [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="f009f-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="f009f-113">Voit luoda projektin myyntilaskun seuraavasti</span><span class="sxs-lookup"><span data-stu-id="f009f-113">To create and post a job sales invoice</span></span>
<span data-ttu-id="f009f-114">Voit luoda asiakkaalle laskun projektista tai vähintään yhdestä projektitehtävästä, kun laskutettava työ on valmis tai kun laskutusaikatauluun perustuva laskutuspäivämäärä on saavutettu.</span><span class="sxs-lookup"><span data-stu-id="f009f-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="f009f-115">Voit laskuttaa **Projektit**-sivulla asiakasta valitsemalla projektin ja valitsemalla sitten **Luo projektin myyntilasku** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="f009f-115">From the **Jobs** page, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="f009f-116">Seuraavassa kerrotaan, miten eräajoa käytetään useiden projektien laskuttamisessa.</span><span class="sxs-lookup"><span data-stu-id="f009f-116">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="f009f-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo projektin myyntilasku** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f009f-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f009f-118">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f009f-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="f009f-119">Määritä suodattimet, jos haluat rajata erätyön käsittelemien projektien määrää.</span><span class="sxs-lookup"><span data-stu-id="f009f-119">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="f009f-120">Luo laskut valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="f009f-120">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="f009f-121">Useiden projektin myyntilaskujen luominen projektin suunnitteluriveistä</span><span class="sxs-lookup"><span data-stu-id="f009f-121">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="f009f-122">Voit luoda laskun projektin suunnitteluriveiltä ja määrittää samalla nimikkeen määrän, resurssin tai KP-tilin, jonka haluat laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="f009f-122">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="f009f-123">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työt** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f009f-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="f009f-124">Avaa liittyvä projekti.</span><span class="sxs-lookup"><span data-stu-id="f009f-124">Open a relevant job.</span></span>
3. <span data-ttu-id="f009f-125">Valitse projektitehtävä, jonka **Projektitehtävätyyppi**-kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f009f-125">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="f009f-126">Annan projektin suunnittelurivin **Laskuun siirrettävä määrä** -kentässä nimikkeen, resurssin tai pääkirjanpidon tilin tyyppi, jonka haluat laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="f009f-126">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="f009f-127">Valitse **Luo myyntilasku** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f009f-127">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="f009f-128">Anna **Luo projektin myyntilasku** -sivulla kirjauspäivämäärä. Määritä, haluatko luoda uuden laskun vai kohdistaa tämän laskun aiemmin luotuun laskuun.</span><span class="sxs-lookup"><span data-stu-id="f009f-128">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="f009f-129">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="f009f-129">Choose the **OK** button.</span></span>  

    <span data-ttu-id="f009f-130">Projektin suunnittelurivin **Laskuun siirretty määrä** -kentässä näkyy määrä.</span><span class="sxs-lookup"><span data-stu-id="f009f-130">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="f009f-131">Valitse **Projektin suunnittelurivit** -sivulla **Myyntilaskut/hyvityslaskut**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f009f-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="f009f-132">Avautuvassa **Myyntilasku**-sivulla näkyy laskuun siirretty määrä.</span><span class="sxs-lookup"><span data-stu-id="f009f-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="f009f-133">Tee tarvittavat muutokset ja valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f009f-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f009f-134">Projektiin liittyvän myyntihyvityslaskun luominen, tarkistaminen ja kirjaaminen tapahtuu vastaavalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f009f-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="f009f-135">Projektin valmistumistapahtumien laskeminen ja kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="f009f-135">To calculate and post job completion entries</span></span>
<span data-ttu-id="f009f-136">Kun olet saanut kaikki projektin toimenpiteet, kuten käytön kirjauksen ja laskutuksen, valmiiksi, projekti on päivitettävä **tilaan** **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="f009f-136">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="f009f-137">Tämän jälkeen mahdollinen kirjanpitoon kirjattu KET peruuntuu.</span><span class="sxs-lookup"><span data-stu-id="f009f-137">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="f009f-138">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työt** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f009f-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f009f-139">Valitse avoin projekti ja valitse sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f009f-139">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="f009f-140">Valitse **Tila**-kentässä **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="f009f-140">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="f009f-141">Laske ja kirjaa KET ohjattujen vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="f009f-141">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="f009f-142">Vaihtoehtoisesti voit tehdä toiminnot manuaalisesti vaiheiden 5 ja 6 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f009f-142">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="f009f-143">Valitse **Laske KET** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f009f-143">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="f009f-144">Täytä **Laske projektin KET** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f009f-144">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="f009f-145">Erätyön luomien projektin KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f009f-145">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="f009f-146">Valitse **Kirjaa projektin KET kirjanpitoon** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f009f-146">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="f009f-147">Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f009f-147">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="f009f-148">Erätyön luomien projektin pääkirjanpidon KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f009f-148">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="f009f-149">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f009f-149">See Also</span></span>
[<span data-ttu-id="f009f-150">Projektien hallinta</span><span class="sxs-lookup"><span data-stu-id="f009f-150">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="f009f-151">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="f009f-151">Finance</span></span>](finance.md)  
<span data-ttu-id="f009f-152">[Osto](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="f009f-152">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="f009f-153">[Myynti](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="f009f-153">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="f009f-154">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f009f-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
