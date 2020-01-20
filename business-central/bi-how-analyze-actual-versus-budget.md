---
title: Todellinen vs. Budjetti -analyysi| Microsoft-asiakirjat
description: Kuvaa, miten todellisia summia analysoidaan budjetoituihin summiin nähden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 6773f03a436d1a65eace851abb1e886bdccee55f
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953849"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="9c0c4-103">Todellisten summien analysointi budjetoituihin summiin nähden</span><span class="sxs-lookup"><span data-stu-id="9c0c4-103">Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="9c0c4-104">Yrityksesi tietojen keräämisen, analysoinnin ja jakamisen osana tarkastelet todellisia summia ja vertaat niitä kaikkien tilien sekä useiden ajanjaksojen budjetoituihin summiin.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="9c0c4-105">Budjetoitujen summia analysointia varten on ensin luotava KP-budjetteja.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="9c0c4-106">Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="9c0c4-106">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="9c0c4-107">KP-budjetin tarkastelu</span><span class="sxs-lookup"><span data-stu-id="9c0c4-107">To view a G/L budget</span></span>
<span data-ttu-id="9c0c4-108">Budjetissa, jossa on dimensioita, voi suodattaa tapahtumia ja siten tarkastella tiettyjä budjetteja.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-108">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="9c0c4-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Pääkirjanpidon budjetit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="9c0c4-110">Avaa **KP-budjetit** -sivulla talousarvio, jota haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-110">On the **G/L Budgets** page, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="9c0c4-111">Täyttämällä sivun yläosan kentät määrität, mitä näytetään.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-111">At the top of the page, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="9c0c4-112">Jos olet valinnut **Jakso**-vaihtoehdon joko **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä, täytä **Näyttöperuste**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-112">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="9c0c4-113">Jos et ole valinnut **Jakso**-vaihtoehtoa **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä, määritä asianmukainen jakso **Pvm-suodatus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-113">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="9c0c4-114">Vain ne KP-budjetin tapahtumat, joissa on **Suodattimet**-pikavälilehdessä määrittämäsi suodatinkoodit, sisällytetään laskentaan.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-114">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="9c0c4-115">Budjettitapahtumia, joissa on eri suodatinkoodit tai joissa ei ole suodatinkoodeja ollenkaan, ei sisällytetä.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-115">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="9c0c4-116">Niin kauan kuin suodatin on näkyvissä sivulla, budjetissa näkyvät vain ne budjettitapahtumat, joissa on nämä suodattimen koodit.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-116">As long as the filter remains on the page, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="9c0c4-117">Jos budjettia on tarpeen muokata, voit muokata budjetin tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-117">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="9c0c4-118">Valitse summa, niin saat näkyviin sen perusteena olevat KP-budjetin tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-118">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="9c0c4-119">Todellisten ja budjetoitujen summien tarkastelu kaikkien tilien osalta</span><span class="sxs-lookup"><span data-stu-id="9c0c4-119">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="9c0c4-120">Pääkirjanpidon budjettien tarkastelu ja niiden vertaaminen todellisiin lukuihin useilla [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman osa-alueilla.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-120">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="9c0c4-121">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9c0c4-122">Valitse **Tilikartta**-sivulla **KP-saldo/-budjetti**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-122">On the **Chart of Accounts** page, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="9c0c4-123">Täyttämällä sivun yläosan kentät määrität, mitä näytetään.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-123">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="9c0c4-124">Valitse kenttä nähdäksesi määrityksen, josta näkyvä summa muodostuu.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-124">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="9c0c4-125">Suodattimia, jotka määritit sivun otsikossa, käytetään sekä KP-tapahtumissa että budjettitapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-125">The filters you set on the page header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="9c0c4-126">Vasemmanpuoleisimmisssa sarakkeissa on tilikartta.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-126">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="9c0c4-127">Oikealla olevista viidestä sarakkeesta neljässä ensimmäisessä on kunkin tilin todelliset ja budjetoidut debet- ja kreditsummat.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-127">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="9c0c4-128">Viidennessä sarakkeessa on todellisen ja budjetoidun summan välinen suhde KP-tilillä.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-128">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="9c0c4-129">Käyttämällä **Näyttöperuste**-kenttää **KP-saldo/budjetti**-sivulla voit valita jakson pituuden.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-129">Use the **View by** field on the **G/L Balance/Budget** page to select the period length.</span></span> <span data-ttu-id="9c0c4-130">**Näyttömuoto**-kentän avulla voit valita tavan, jolla summat lasketaan (**Nettomuutos** tai **Saldo pvm:ttäin**).</span><span class="sxs-lookup"><span data-stu-id="9c0c4-130">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="9c0c4-131">Valitse **Edellinen jakso** tai **Seuraava jakso** -toiminto ja muuta jaksoa.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-131">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="9c0c4-132">Useiden jaksojen todellisten ja budjetoitujen summien tarkastelu</span><span class="sxs-lookup"><span data-stu-id="9c0c4-132">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="9c0c4-133">Sen sijaan että tarkastelisit todellisia ja budjetoituja summia kaikkien tilien osalta yhdeltä kaudelta, voit tarkastella useita yhden tilin kausia.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-133">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="9c0c4-134">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9c0c4-135">Valitse **Tilikartta**-sivulla haluamasi KP-tili ja valitse sitten **KP-tilin saldo/budjetti** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-135">On the **Chart of Accounts** page, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="9c0c4-136">Täyttämällä sivun yläosan kentät määrität, mitä näytetään.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-136">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="9c0c4-137">Valitse kenttä nähdäksesi näkyvän summan määrityksen.</span><span class="sxs-lookup"><span data-stu-id="9c0c4-137">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-related-training-at-microsoft-learnlearnmodulesbudgets-exchange-rates-dynamics-365-business-centralindex"></a><span data-ttu-id="9c0c4-138">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="9c0c4-138">See Related Training at [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="9c0c4-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9c0c4-139">See Also</span></span>
[<span data-ttu-id="9c0c4-140">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="9c0c4-140">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="9c0c4-141">KP-raporttimallien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="9c0c4-141">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="9c0c4-142">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="9c0c4-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="9c0c4-143">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9c0c4-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="9c0c4-144">Pääkirjanpito ja tilikartta</span><span class="sxs-lookup"><span data-stu-id="9c0c4-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="9c0c4-145">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9c0c4-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
