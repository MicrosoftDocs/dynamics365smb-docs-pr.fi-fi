---
title: KP-budjettien luominen| Microsoft Docs
description: "Tässä artikkelissa käsitellään, miten luodaan KP-budjetteja ennustamaan erilaisia taloudellisia toimintoja ja miten dimensiot määritetään liiketoimintatietoja varten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 4cf8738c7bab09f7bcf900baae54731b6772e7e9
ms.contentlocale: fi-fi
ms.lasthandoff: 11/22/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="e63d5-103">KP-budjettien luominen</span><span class="sxs-lookup"><span data-stu-id="e63d5-103">Create G/L Budgets</span></span>
<span data-ttu-id="e63d5-104">Sinulla voi olla useita budjetteja samalle ajanjaksolle, kun luot budjetit eri nimillä.</span><span class="sxs-lookup"><span data-stu-id="e63d5-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="e63d5-105">Määrittele ensin budjetin nimi ja syötä budjettiluvut.</span><span class="sxs-lookup"><span data-stu-id="e63d5-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="e63d5-106">Budjetin nimi tulee sitten kaikkiin luomiisi budjettitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="e63d5-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="e63d5-107">Kun luot budjetin, voit määritellä jokaiselle budjetille neljä dimensiota.</span><span class="sxs-lookup"><span data-stu-id="e63d5-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="e63d5-108">Näitä budjettikohtaisia dimensioita kutsutaan budjettidimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="e63d5-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="e63d5-109">Valitse budjettidimensiot jo luomistasi dimensioista.</span><span class="sxs-lookup"><span data-stu-id="e63d5-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="e63d5-110">Budjettidimensioita voidaan käyttää, kun halutaan asettaa suodatin budjetille tai kun halutaan lisätä dimensiotietoa budjettitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="e63d5-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="e63d5-111">Lisätietoja on kohdassa [Dimensioiden käyttäminen](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="e63d5-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="e63d5-112">Budjeteilla on tärkeä osa liiketoimintatiedoissa, kuten KP-raporttimalleihin perustuvissa tilinpäätöksissä, jotka sisältävät budjettitapahtumia, tai analysoitaessa budjetoituja summia todellisia summia vastaan tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="e63d5-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="e63d5-113">Lisätietoja on ohjeaiheessa [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="e63d5-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="e63d5-114">Budjeteilla on tärkeä osa budjettitapahtumia sisältävissä liiketoimintatiedoissa, kuten KP-raporttimalleihin perustuvissa tilinpäätöksissä, tai analysoitaessa tilikartan budjetoituja ja todellisia summia.</span><span class="sxs-lookup"><span data-stu-id="e63d5-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="e63d5-115">Lisätietoja on kohdassa [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="e63d5-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="e63d5-116">Voit käsitellä kustannusbudjetteja samalla tavoin kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="e63d5-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="e63d5-117">Lisätietoja on kohdassa [Kustannusbudjettien luominen](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="e63d5-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="e63d5-118">Uuden KP-budjetin luominen</span><span class="sxs-lookup"><span data-stu-id="e63d5-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="e63d5-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-budjetit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e63d5-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e63d5-120">Valitse **Muokkaa luetteloa** -toiminto ja täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="e63d5-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="e63d5-121">Valitse **Muokkaa budjettia** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e63d5-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="e63d5-122">Täyttämällä **Budjetti**-sivun yläosan kentät määrität, mitä näytetään.</span><span class="sxs-lookup"><span data-stu-id="e63d5-122">At the top of the **Budget** page, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="e63d5-123">Näytössä näkyvät vain ne tapahtumat, joilla on **Budjetin nimi** -kentässä annettu nimi.</span><span class="sxs-lookup"><span data-stu-id="e63d5-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="e63d5-124">Koska budjetin nimi on juuri luotu, suodatinta vastaavia tapahtumia ei ole.</span><span class="sxs-lookup"><span data-stu-id="e63d5-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="e63d5-125">Tämän vuoksi sivu on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="e63d5-125">Therefore, the page is empty.</span></span>  
5. <span data-ttu-id="e63d5-126">Jos haluat lisätä summan, napsauta solua matriisissa.</span><span class="sxs-lookup"><span data-stu-id="e63d5-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="e63d5-127">**KP-budjetin tapahtumat** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="e63d5-127">The **G/L Budget Entries** page opens.</span></span>  
6. <span data-ttu-id="e63d5-128">Luo uusi rivi ja määritä **Summa**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="e63d5-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="e63d5-129">Sulje **KP-budjetin tapahtumat** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e63d5-129">Close the **G/L Budget Entries** page.</span></span>  
7. <span data-ttu-id="e63d5-130">Toista vaiheet 5 ja 6, kunnes olet määrittänyt kaikki budjettisummat.</span><span class="sxs-lookup"><span data-stu-id="e63d5-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e63d5-131">**Suodattimet** -pikavälilehdessä voit suodattaa budjettitietoja sen mukaan, mitä budjettidimensioita olet luonut budjetin nimen alle.</span><span class="sxs-lookup"><span data-stu-id="e63d5-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="e63d5-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e63d5-132">See Also</span></span>
[<span data-ttu-id="e63d5-133">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="e63d5-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="e63d5-134">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="e63d5-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="e63d5-135">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e63d5-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="e63d5-136">Pääkirjanpito ja tilikartta</span><span class="sxs-lookup"><span data-stu-id="e63d5-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="e63d5-137">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e63d5-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

