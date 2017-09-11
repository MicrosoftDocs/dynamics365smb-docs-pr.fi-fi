---
title: Kanadalaiset GIFI-koodit | Microsoft Docs
Description: "Voit määrittää Kanadassa GIFI-koodeja (General Index of Financial Information) ja liittää ne kirjaustileihin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="88dc2-103">Toimintaohje: Kanadan GIFI-koodien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="88dc2-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="88dc2-104">Taloustiedot voivat sisältää kirjanpitotilejä, raportteja, tuloslaskelmia, taseita ja jakamattoman voiton tiliotteita.</span><span class="sxs-lookup"><span data-stu-id="88dc2-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="88dc2-105">Taloustiedot luokitellaan koodien avulla.</span><span class="sxs-lookup"><span data-stu-id="88dc2-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="88dc2-106">Viranomaiset käyttävät koodeja tietojen käsittelemiseen, sähköiseen arkistoimiseen ja verotietojen sähköiseen tarkistamiseen.</span><span class="sxs-lookup"><span data-stu-id="88dc2-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="88dc2-107">Koodit auttavat myös tilastotietojen tehokkaassa käsittelyssä, koska taloustiedot ovat helpommin käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="88dc2-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="88dc2-108">Lisätietoja on [Kanadan CRA:n (Canada Revenue Agency) verkkosivustossa](http://www.cra-arc.gc.ca/).</span><span class="sxs-lookup"><span data-stu-id="88dc2-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="88dc2-109">Kanadan CRA käyttää tilinpäätösten kirjanpitotietojen yleisindeksikoodeja eli GIFI (General Index of Financial Information) -koodeja talous- ja verotietojen sähköisessä keräämiseen, tarkistamiseen ja käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="88dc2-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="88dc2-110">GIFI-koodit kannattaa liittää vain kirjaustileihin niin, että verojen valmistelussa käytettävä ohjelmisto suorittaa summauksen.</span><span class="sxs-lookup"><span data-stu-id="88dc2-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="88dc2-111">Kun tili on liitetty GIFI-koodiin, kyseistä koodia käytetään verotoimiston raporteissa.</span><span class="sxs-lookup"><span data-stu-id="88dc2-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="88dc2-112">Sama GIFI-koodi voi olla useilla tileillä, mutta tilillä voi olla vain yksi GIFI-koodi.</span><span class="sxs-lookup"><span data-stu-id="88dc2-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="88dc2-113">Saldotiedot voidaan viedä GIFI-koodin avulla, ja viety tiedosto voidaan tallentaa Exceliin. Tämä on hyödyllistä silloin, kun tietoja siirretään verojen valmistelussa käytettävään ohjelmistoon.</span><span class="sxs-lookup"><span data-stu-id="88dc2-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="88dc2-114">GIFI-koodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="88dc2-114">To set up GIFI codes</span></span>
<span data-ttu-id="88dc2-115">Dynamics NAV -ohjelmassa GIFI-koodit on määritettävä kirjanpitotileille, raporteille, taseille, tuloslaskelmille ja jakamattoman voiton tiliotteille.</span><span class="sxs-lookup"><span data-stu-id="88dc2-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="88dc2-116">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **GIFI-koodit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="88dc2-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="88dc2-117">Valitse **GIFI-koodit**-ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="88dc2-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="88dc2-118">Määritä GIFI-koodit täyttämällä kentät.</span><span class="sxs-lookup"><span data-stu-id="88dc2-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="88dc2-119">GIFI-koodien liittäminen kirjanpitotileihin</span><span class="sxs-lookup"><span data-stu-id="88dc2-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="88dc2-120">Voit raportoida taloustiedot GIFI-koodien mukaan, kun kukin GIFI-koodi on liitetty tilikartan asianmukaiseen tiliin.</span><span class="sxs-lookup"><span data-stu-id="88dc2-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="88dc2-121">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="88dc2-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="88dc2-122">Valitse asiaankuuluva kirjanpitotili ja valitse sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="88dc2-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="88dc2-123">Valitse **Kustannuslaskenta**-pikavälilehden **GIFI-koodi**-kenttään asiaankuuluva GIFI-koodi.</span><span class="sxs-lookup"><span data-stu-id="88dc2-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="88dc2-124">Tilien saldojen tarkasteleminen GIFI-koodiraportin avulla</span><span class="sxs-lookup"><span data-stu-id="88dc2-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="88dc2-125">Voit tarkastella tilien saldoja GIFI-koodin mukaan **Tilien saldot GIFI-koodin mukaan** -raportin avulla.</span><span class="sxs-lookup"><span data-stu-id="88dc2-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="88dc2-126">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Tilien saldot GIFI-koodin mukaan** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="88dc2-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="88dc2-127">Määritä raporttiin sisällytettävät tiedot täyttämällä kentät.</span><span class="sxs-lookup"><span data-stu-id="88dc2-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="88dc2-128">Valitse **Tulosta**- tai **Esikatsele**-painike.</span><span class="sxs-lookup"><span data-stu-id="88dc2-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="88dc2-129">Saldotietojen vieminen GIFI-koodien avulla</span><span class="sxs-lookup"><span data-stu-id="88dc2-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="88dc2-130">Voit viedä saldotiedot GIFI-koodien avulla ja tallentaa viedyn tiedoston Excelissä.</span><span class="sxs-lookup"><span data-stu-id="88dc2-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="88dc2-131">Voit muokata tiedostoa tai tallentaa tai poistaa sen.</span><span class="sxs-lookup"><span data-stu-id="88dc2-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="88dc2-132">Tiedoston avulla voit siirtää tietoja verojen valmistelussa käytettävään ohjelmistoon.</span><span class="sxs-lookup"><span data-stu-id="88dc2-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="88dc2-133">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **GIFI-koodit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="88dc2-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="88dc2-134">Määritä Exceliin vietävät tiedot täyttämällä kentät.</span><span class="sxs-lookup"><span data-stu-id="88dc2-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="88dc2-135">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="88dc2-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="88dc2-136">Excel-tiedostolla on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="88dc2-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="88dc2-137">Saldo pyöristetään lähimpään prosenttilukuun, mutta solun arvona pidetään pääkirjanpidossa oleva prosenttiluku.</span><span class="sxs-lookup"><span data-stu-id="88dc2-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="88dc2-138">Negatiiviset luvut esitetään suluissa olevina positiivisina lukuina.</span><span class="sxs-lookup"><span data-stu-id="88dc2-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="88dc2-139">Luku -123 on siis (123).</span><span class="sxs-lookup"><span data-stu-id="88dc2-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="88dc2-140">Katso myös</span><span class="sxs-lookup"><span data-stu-id="88dc2-140">See Also</span></span>
<span data-ttu-id="88dc2-141">[Rahoitus](finance.md) </span><span class="sxs-lookup"><span data-stu-id="88dc2-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="88dc2-142">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="88dc2-142">Setting Up Finance</span></span>](finance-setup-finance.md)

