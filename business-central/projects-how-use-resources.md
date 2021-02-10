---
title: Resurssin käytön ja hintojen kirjaaminen ja muuttaminen| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten voit kirjata projektiin liitetyn resurssin käytön tai kulutuksen sekä seurata ja hallinta kustannuksia, hintoja ja työtyyppejä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c753e38566971c044da3337f0f35f1609bd489c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748866"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="3951a-103">Resurssien käyttäminen projekteissa</span><span class="sxs-lookup"><span data-stu-id="3951a-103">Use Resources for Jobs</span></span>
<span data-ttu-id="3951a-104">Kirjaa resurssien käyttö projektipäiväkirjaan, kun haluat seurata kustannuksia ja hintoja sekä projekteihin linkitettyjä työtyyppejä.</span><span class="sxs-lookup"><span data-stu-id="3951a-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="3951a-105">Lisätietoja on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="3951a-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

> [!NOTE]
> <span data-ttu-id="3951a-106">Voit ostaa myös ulkoisia resursseja, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä.</span><span class="sxs-lookup"><span data-stu-id="3951a-106">You can also purchase external resources, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="3951a-107">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="3951a-107">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="3951a-108">Voit kirjata resurssin käytön myös resurssipäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="3951a-108">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="3951a-109">Resurssipäiväkirjassa kirjatuilla tapahtumilla ei ole vaikutusta pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="3951a-109">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="3951a-110">Resurssien määrittäminen projekteihin:</span><span class="sxs-lookup"><span data-stu-id="3951a-110">To assign resources to jobs</span></span>
<span data-ttu-id="3951a-111">Voit määrittää resursseja projekteihin luomalla projektiin suunnittelurivejä.</span><span class="sxs-lookup"><span data-stu-id="3951a-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="3951a-112">Lisätietoja on kohdassa [Projektien luominen](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="3951a-112">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="3951a-113">Projektin resurssin käytön kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="3951a-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="3951a-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Projektipäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3951a-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="3951a-115">Avaa kyseessä oleva projektipäiväkirjan erä ja täytä vaaditut kentät.</span><span class="sxs-lookup"><span data-stu-id="3951a-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="3951a-116">Kun päiväkirja on valmis, valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="3951a-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="3951a-117">Resurssihintojen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="3951a-117">To adjust resource prices</span></span>
<span data-ttu-id="3951a-118">Jos haluat muuttaa useiden resurssien kustannuksia tai hintoja, voit käyttää eräajoa.</span><span class="sxs-lookup"><span data-stu-id="3951a-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="3951a-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muuta resurssin kustannuksia tai hintoja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3951a-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="3951a-120">Täytä rivin tarvittavat kentät ja valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="3951a-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3951a-121">Tämä eräajo ei luo vaihtoehtoisia kustannuksia tai hintoja resursseille tai muuta niitä.</span><span class="sxs-lookup"><span data-stu-id="3951a-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="3951a-122">Se muuttaa vain sen **Muuta kenttää** -kentässä olevan resurssin kortin kentän sisältöä, joka on valittu eräajoon.</span><span class="sxs-lookup"><span data-stu-id="3951a-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="3951a-123">Muutokset tulevat resurssien osalta voimaan heti, joten tarkista muutoskertoimet ennen eräajon suorittamista.</span><span class="sxs-lookup"><span data-stu-id="3951a-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="3951a-124">Resurssihintojen muutosehdotusten saaminen olemassa olevien vaihtoehtoisten hintojen perusteella</span><span class="sxs-lookup"><span data-stu-id="3951a-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="3951a-125">Jos olet jo määrittänyt vaihtoehtoisia resurssihintoja joillekin resursseille, voit määrittää useita vaihtoehtoisia resurssihintoja eräajon avulla.</span><span class="sxs-lookup"><span data-stu-id="3951a-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="3951a-126">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssin hinnan muutokset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3951a-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="3951a-127">Valitse **Ehdota res.hintamuut. (hinta)** -toiminto ja täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="3951a-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="3951a-128">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="3951a-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="3951a-129">Kun eräajo on päättynyt, eräajon tulokset näkyvät **Resurssin hinnan muutokset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3951a-129">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="3951a-130">Resurssihintojen muutosehdotusten saaminen vakiohintojen perusteella</span><span class="sxs-lookup"><span data-stu-id="3951a-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="3951a-131">Jos haluat määrittää useita vaihtoehtoisia resurssihintoja resurssikorttien vakiohintojen perusteella, voit käyttää eräajoa.</span><span class="sxs-lookup"><span data-stu-id="3951a-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="3951a-132">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssin hinnan muutokset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3951a-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="3951a-133">Valitse **Ehdota res.hintamuut. (res.)** -toiminto ja täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="3951a-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="3951a-134">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="3951a-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="3951a-135">Kun eräajo on päättynyt, voit katsoa eräajon tulokset avaamalla **Resurssin hinnan muutokset** -sivun.</span><span class="sxs-lookup"><span data-stu-id="3951a-135">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="3951a-136">Resurssihintojen muutosehdotusten saaminen vakiohintojen perusteella</span><span class="sxs-lookup"><span data-stu-id="3951a-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="3951a-137">Jos olet jo määrittänyt vaihtoehtoisia resurssihintoja joillekin resursseille, voit määrittää useita vaihtoehtoisia resurssihintoja eräajon avulla.</span><span class="sxs-lookup"><span data-stu-id="3951a-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="3951a-138">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ehdota res.hintamuut. (hinta)** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3951a-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3951a-139">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="3951a-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="3951a-140">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="3951a-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="3951a-141">Kun eräajo on päättynyt, voit katsoa eräajon tulokset avaamalla **Resurssin hinnan muutokset** -sivun.</span><span class="sxs-lookup"><span data-stu-id="3951a-141">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="3951a-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3951a-142">See Also</span></span>
[<span data-ttu-id="3951a-143">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="3951a-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="3951a-144">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="3951a-144">Finance</span></span>](finance.md)  
<span data-ttu-id="3951a-145">[Osto](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="3951a-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="3951a-146">[Myynti](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="3951a-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="3951a-147">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3951a-147">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
