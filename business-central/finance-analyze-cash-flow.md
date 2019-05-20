---
title: Kassavirtojen analyysi| Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten käyttöpääomasykli-, tulot ja kulut-, kassavirta- ja kassavirtaennustekaavioilla voidaan analysoida yrityksen historiallista ja tulevaa kassavirran liikkumista.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera
ms.date: 06/02/2017
ms.author: bholtorf
ms.openlocfilehash: 40e180222968f3ede5a69530e05bf5c0a74fdeb3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239059"
---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="33362-103">Yrityksen kassavirran analysoiminen</span><span class="sxs-lookup"><span data-stu-id="33362-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="33362-104">Käteisvarat ovat tunnetusti tärkeitä.</span><span class="sxs-lookup"><span data-stu-id="33362-104">As they say, cash is king.</span></span> <span data-ttu-id="33362-105">Kirjanpitäjä-roolikeskuksesta saa tietoja, joiden avulla voi päättää järkevästi käteisvarojen käytöstä.</span><span class="sxs-lookup"><span data-stu-id="33362-105">The charts on the Accountant Role Center provide insight that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="33362-106">Vastattava kysymys</span><span class="sxs-lookup"><span data-stu-id="33362-106">To answer questions like these</span></span> | <span data-ttu-id="33362-107">Käytettävä kaavio</span><span class="sxs-lookup"><span data-stu-id="33362-107">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="33362-108">Kuinka pitkään käteisvarat ovat kiinni myyntiprosessissa?</span><span class="sxs-lookup"><span data-stu-id="33362-108">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="33362-109">Onko varastotasoa suurennettava vai pienennettävä?</span><span class="sxs-lookup"><span data-stu-id="33362-109">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="33362-110">Käyttöpääomasykli</span><span class="sxs-lookup"><span data-stu-id="33362-110">Cash Cycle</span></span> |
| <span data-ttu-id="33362-111">Milloin käteisvaroja siirtyy yritykseen ja milloin yrityksestä pois?</span><span class="sxs-lookup"><span data-stu-id="33362-111">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="33362-112">Ovatko tietyt jaksot muita jaksoja parempia?</span><span class="sxs-lookup"><span data-stu-id="33362-112">Are some periods better than others?</span></span> |<span data-ttu-id="33362-113">Kassavirta</span><span class="sxs-lookup"><span data-stu-id="33362-113">Cash Flow</span></span> |
| <span data-ttu-id="33362-114">Näyttävätkö jonkin kauden luvut epätavallisilta?</span><span class="sxs-lookup"><span data-stu-id="33362-114">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="33362-115">Pitäisikö asiaa tutkia?</span><span class="sxs-lookup"><span data-stu-id="33362-115">Should I investigate?</span></span> |<span data-ttu-id="33362-116">Tulot ja kulut</span><span class="sxs-lookup"><span data-stu-id="33362-116">Income & Expense</span></span> |
| <span data-ttu-id="33362-117">Milloin voi esiintyä käteisen yli- tai alijäämää?</span><span class="sxs-lookup"><span data-stu-id="33362-117">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="33362-118">Pitäisikö velka maksaa pois vai ottaa lainaa tulevia menoja varten?</span><span class="sxs-lookup"><span data-stu-id="33362-118">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="33362-119">Kassavirtaennusteet</span><span class="sxs-lookup"><span data-stu-id="33362-119">Cash Flow Forecasts</span></span> |

<span data-ttu-id="33362-120">Kirjanpitäjä-roolikeskuksen **Rahoituksen suorituskyky** -kohdan **Käyttöpääomasykli**-, **Kassavirta**- ja **Tulot ja kulut** -kaavioiden avulla voi analysoida kassavirtaa eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="33362-120">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="33362-121">Voit tarkastella kauden lukuja aikajanan liukusäätimellä.</span><span class="sxs-lookup"><span data-stu-id="33362-121">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="33362-122">Voit suodattaa kaaviota valitsemalla selitteessä lähteen.</span><span class="sxs-lookup"><span data-stu-id="33362-122">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="33362-123">Voit muuttaa kauden pituutta tai siirtyä edelliseen tai seuraavaan kauteen valitsemalla avattavasta **Rahoituksen suorituskyky** -luettelosta sopivan vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="33362-123">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="33362-124">Voit tarkastella tapahtumia valitsemalla kaaviossa jonkin kohdan.</span><span class="sxs-lookup"><span data-stu-id="33362-124">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="33362-125">Voit valita kohdan esimerkiksi aikajanalla tai sarakkeen osan.</span><span class="sxs-lookup"><span data-stu-id="33362-125">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="33362-126">Jos luvut eivät näytä olevan kunnossa, voit muuttaa niitä täällä.</span><span class="sxs-lookup"><span data-stu-id="33362-126">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="33362-127">Vaikka **Kassavirtaennuste**-kaavio on oma kaavionsa, se on vastaavanlainen.</span><span class="sxs-lookup"><span data-stu-id="33362-127">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="33362-128">Voit tarkastella tietoja, suodattaa tuloksia ja tehdä näkyvissä oleviin tietoihin muutoksia samalla tavoin.</span><span class="sxs-lookup"><span data-stu-id="33362-128">You view details, filter results, and change what is displayed in the same ways.</span></span> <span data-ttu-id="33362-129">Jos muutat asetusta, voit päivittää ennusteen valitsemalla ensin **Kassavirtaennuste** ja sitten **Laske ennuste uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="33362-129">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="33362-130">Jos haluat tarkastella ennustetta, voit perehtyä ennustetapahtumien lisäksi myös kassavirtakaavioon.</span><span class="sxs-lookup"><span data-stu-id="33362-130">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="33362-131">Saat tietoja esimerkiksi siitä, miten ennuste</span><span class="sxs-lookup"><span data-stu-id="33362-131">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="33362-132">käsittelee vahvistetun myynnin ja ostot</span><span class="sxs-lookup"><span data-stu-id="33362-132">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="33362-133">vähentää ostoreskontran ja lisää myyntireskontran</span><span class="sxs-lookup"><span data-stu-id="33362-133">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="33362-134">ohittaa myynti- ja ostotilausten kaksoiskappaleet.</span><span class="sxs-lookup"><span data-stu-id="33362-134">Skips duplicate sales orders and purchase orders.</span></span>  

## <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="33362-135">Kassavirtatyökirjan tarkastelu</span><span class="sxs-lookup"><span data-stu-id="33362-135">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="33362-136">Hae **Kassavirtaennusteet** ja valitse liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="33362-136">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="33362-137">Valitse ensin kassavirtaennustee ja sitten **Kassavirtatyökirja**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="33362-137">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="33362-138">Valitse **Kassavirtatyökirja**-sivulla **Ehdota työkirjan rivejä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="33362-138">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="33362-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="33362-139">See Also</span></span>
[<span data-ttu-id="33362-140">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="33362-140">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="33362-141">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="33362-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="33362-142">Kassavirta-analyysin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="33362-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  
