---
title: Kassavirtojen analyysi| Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten käyttöpääomasykli-, tulot ja kulut-, kassavirta- ja kassavirtaennustekaavioilla voidaan analysoida yrityksen historiallista ja tulevaa kassavirran liikkumista.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f3f7e9c33e5dab3de6461fcda5732168f0e6e89b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751028"
---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="d21e4-103">Yrityksen kassavirran analysoiminen</span><span class="sxs-lookup"><span data-stu-id="d21e4-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="d21e4-104">Kirjanpitäjän roolikeskuksesta saa merkityksellisiä tietoja, joiden avulla voi päättää järkevästi käteisvarojen käytöstä.</span><span class="sxs-lookup"><span data-stu-id="d21e4-104">The charts on the Accountant Role Center provide insights that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="d21e4-105">Vastattava kysymys</span><span class="sxs-lookup"><span data-stu-id="d21e4-105">To answer questions like these</span></span> | <span data-ttu-id="d21e4-106">Käytettävä kaavio</span><span class="sxs-lookup"><span data-stu-id="d21e4-106">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="d21e4-107">Kuinka pitkään käteisvarat ovat kiinni myyntiprosessissa?</span><span class="sxs-lookup"><span data-stu-id="d21e4-107">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="d21e4-108">Onko varastotasoa suurennettava vai pienennettävä?</span><span class="sxs-lookup"><span data-stu-id="d21e4-108">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="d21e4-109">Käyttöpääomasykli</span><span class="sxs-lookup"><span data-stu-id="d21e4-109">Cash Cycle</span></span> |
| <span data-ttu-id="d21e4-110">Milloin käteisvaroja siirtyy yritykseen ja milloin yrityksestä pois?</span><span class="sxs-lookup"><span data-stu-id="d21e4-110">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="d21e4-111">Ovatko tietyt jaksot muita jaksoja parempia?</span><span class="sxs-lookup"><span data-stu-id="d21e4-111">Are some periods better than others?</span></span> |<span data-ttu-id="d21e4-112">Kassavirta</span><span class="sxs-lookup"><span data-stu-id="d21e4-112">Cash Flow</span></span> |
| <span data-ttu-id="d21e4-113">Näyttävätkö jonkin kauden luvut epätavallisilta?</span><span class="sxs-lookup"><span data-stu-id="d21e4-113">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="d21e4-114">Pitäisikö asiaa tutkia?</span><span class="sxs-lookup"><span data-stu-id="d21e4-114">Should I investigate?</span></span> |<span data-ttu-id="d21e4-115">Tulot ja kulut</span><span class="sxs-lookup"><span data-stu-id="d21e4-115">Income & Expense</span></span> |
| <span data-ttu-id="d21e4-116">Milloin voi esiintyä käteisen yli- tai alijäämää?</span><span class="sxs-lookup"><span data-stu-id="d21e4-116">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="d21e4-117">Pitäisikö velka maksaa pois vai ottaa lainaa tulevia menoja varten?</span><span class="sxs-lookup"><span data-stu-id="d21e4-117">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="d21e4-118">Kassavirtaennusteet</span><span class="sxs-lookup"><span data-stu-id="d21e4-118">Cash Flow Forecasts</span></span> |

<span data-ttu-id="d21e4-119">Kirjanpitäjä-roolikeskuksen **Rahoituksen suorituskyky** -kohdan **Käyttöpääomasykli**-, **Kassavirta**- ja **Tulot ja kulut** -kaavioiden avulla voi analysoida kassavirtaa eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="d21e4-119">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="d21e4-120">Voit tarkastella kauden lukuja aikajanan liukusäätimellä.</span><span class="sxs-lookup"><span data-stu-id="d21e4-120">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="d21e4-121">Voit suodattaa kaaviota valitsemalla selitteessä lähteen.</span><span class="sxs-lookup"><span data-stu-id="d21e4-121">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="d21e4-122">Voit muuttaa kauden pituutta tai siirtyä edelliseen tai seuraavaan kauteen valitsemalla avattavasta **Rahoituksen suorituskyky** -luettelosta sopivan vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="d21e4-122">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="d21e4-123">Voit tarkastella tapahtumia valitsemalla kaaviossa jonkin kohdan.</span><span class="sxs-lookup"><span data-stu-id="d21e4-123">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="d21e4-124">Voit valita kohdan esimerkiksi aikajanalla tai sarakkeen osan.</span><span class="sxs-lookup"><span data-stu-id="d21e4-124">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="d21e4-125">Jos luvut eivät näytä olevan kunnossa, voit muuttaa niitä täällä.</span><span class="sxs-lookup"><span data-stu-id="d21e4-125">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="d21e4-126">Vaikka **Kassavirtaennuste**-kaavio on oma kaavionsa, se on vastaavanlainen.</span><span class="sxs-lookup"><span data-stu-id="d21e4-126">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="d21e4-127">Voit tarkastella tietoja, suodattaa tuloksia ja tehdä näkyvissä oleviin tietoihin muutoksia samalla tavoin.</span><span class="sxs-lookup"><span data-stu-id="d21e4-127">You view details, filter results, and change what is displayed in the same ways.</span></span> <span data-ttu-id="d21e4-128">Jos muutat asetusta, voit päivittää ennusteen valitsemalla ensin **Kassavirtaennuste** ja sitten **Laske ennuste uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="d21e4-128">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="d21e4-129">Jos haluat tarkastella ennustetta, voit perehtyä ennustetapahtumien lisäksi myös kassavirtakaavioon.</span><span class="sxs-lookup"><span data-stu-id="d21e4-129">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="d21e4-130">Saat tietoja esimerkiksi siitä, miten ennuste</span><span class="sxs-lookup"><span data-stu-id="d21e4-130">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="d21e4-131">käsittelee vahvistetun myynnin ja ostot</span><span class="sxs-lookup"><span data-stu-id="d21e4-131">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="d21e4-132">vähentää ostoreskontran ja lisää myyntireskontran</span><span class="sxs-lookup"><span data-stu-id="d21e4-132">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="d21e4-133">ohittaa myynti- ja ostotilausten kaksoiskappaleet.</span><span class="sxs-lookup"><span data-stu-id="d21e4-133">Skips duplicate sales orders and purchase orders.</span></span>  

## <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="d21e4-134">Kassavirtatyökirjan tarkastelu</span><span class="sxs-lookup"><span data-stu-id="d21e4-134">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="d21e4-135">Hae **Kassavirtaennusteet** ja valitse liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d21e4-135">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d21e4-136">Valitse ensin kassavirtaennustee ja sitten **Kassavirtatyökirja**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d21e4-136">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="d21e4-137">Valitse **Kassavirtatyökirja**-sivulla **Ehdota työkirjan rivejä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d21e4-137">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="d21e4-138">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="d21e4-138">See Related Training at [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="d21e4-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d21e4-139">See Also</span></span>
[<span data-ttu-id="d21e4-140">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d21e4-140">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="d21e4-141">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d21e4-141">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d21e4-142">Kassavirta-analyysin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d21e4-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  
