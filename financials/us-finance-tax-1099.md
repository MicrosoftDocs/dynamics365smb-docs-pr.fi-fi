---
title: Freelance-tulojen ilmoitukset (lomake 1099) USA:ssa | Microsoft Docs
description: "IRS edellyttää 1099-verolomakkeen käyttöä toimittajille tehtävissä maksuissa, ja voit määrittää, että 1099-lomake koskee ostoasiakirjaa. Voit myös määrittää toimittajan 1099-koodin."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a><span data-ttu-id="e4dc8-103">Tapahtumien ilmoittaminen 1099-lomakkeella USA:ssa</span><span class="sxs-lookup"><span data-stu-id="e4dc8-103">Reporting Transactions as 1099 Liable in the US</span></span>

<span data-ttu-id="e4dc8-104">Yhdysvaltain verohallinto (IRS) vaatii vähintään yhdenlaisen version 1099-lomakkeella tehdystä veroilmoituksesta, joka käsittelee toimittajille suoritettuja maksuja.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-104">The Internal Revenue Service (IRS) requires one or more versions of the 1099 tax form for payments to vendors.</span></span> <span data-ttu-id="e4dc8-105">Kopiot näistä lomakkeista on lähetettävä toimittajille vuosittain tai ennen tammikuun viimeistä päivää.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-105">Copies of these forms must be sent to vendors annually on or before the last day of January.</span></span> <span data-ttu-id="e4dc8-106">Voit määrittää ostoasiakirjoissa, että asiakirja on 1099-lomakkeen alainen sekä määrittää toimittajan 1099-verokoodin.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-106">On your purchase documents, you can specify that the document is 1099 liable, and you can specify the 1099 code for the vendor.</span></span>  

## <a name="1099-codes"></a><span data-ttu-id="e4dc8-107">1099-verokoodit</span><span class="sxs-lookup"><span data-stu-id="e4dc8-107">1099 codes</span></span>
<span data-ttu-id="e4dc8-108">[!INCLUDE[d365fin](includes/d365fin_md.md)]issa yleisimmät 1099-koodit on määritetty valmiiksi, eli olet valmis luomaan vaadittavat raportit.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the most common 1099 codes are already set up for you so you are ready to generate the required reports.</span></span> <span data-ttu-id="e4dc8-109">Koodit on määritetty **IRS 1099 -lomakkeen ruutu** -ikkunassa, jossa voit myös lisätä uusia 1099-koodeja.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-109">The codes are defined in the **IRS 1099 Form Box** window where you can also add new 1099 codes.</span></span> <span data-ttu-id="e4dc8-110">Voit sitten määrittää kullekin verovelvolliselle toimittajalle oikean 1099-koodin toimittajakortin **Maksut**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-110">For each tax liable vendor, you can then specify the relevant 1099 code on the **Payments** FastTab on the Vendor card.</span></span>  

<span data-ttu-id="e4dc8-111">**Toimittajan 1099-verotiedot** -raportilla voit tarkastella tietyn kauden aikana maksettuja 1099-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-111">With the **Vendor 1099 Information** report, you can review 1099 transactions paid during a specified period.</span></span> <span data-ttu-id="e4dc8-112">Voit tulostaa 1099-tapahtumat esitäytetyille lomakkeille vuoden lopussa.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-112">At the end of the year, you can print 1099 transactions on preprinted forms.</span></span>  

## <a name="printing-1099-tax-forms"></a><span data-ttu-id="e4dc8-113">1099-verolomakkeiden tulostus</span><span class="sxs-lookup"><span data-stu-id="e4dc8-113">Printing 1099 tax forms</span></span>
<span data-ttu-id="e4dc8-114">Voit käyttää seuraavia verolomakkeita **IRS 1099-verolomakkeen ruutu** -ikkunassa:</span><span class="sxs-lookup"><span data-stu-id="e4dc8-114">From the **IRS 1099 Form Box** window, you can access the following tax forms:</span></span>  

* <span data-ttu-id="e4dc8-115">Toimittajan 1099 Div</span><span class="sxs-lookup"><span data-stu-id="e4dc8-115">Vendor 1099 Div</span></span>  

  <span data-ttu-id="e4dc8-116">Tulostaa liittovaltion 1099-DIV -lomakkeen, joka koskee osinkoja ja osakeantia.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-116">Prints the federal form 1099-DIV for dividends and distribution.</span></span> <span data-ttu-id="e4dc8-117">Voit tulostaa kaikki tai tietyt 1099-DIV -lomakkeet.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-117">You can print all or specific 1099-DIV forms.</span></span> <span data-ttu-id="e4dc8-118">Raportti käyttää koodeja **IRS 1099 -verolomakkeen ruutu** -ikkunasta, jotka koskevat DIV-lomakkeen määrä-ruutuja.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-118">The report uses the codes that apply to the DIV form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="e4dc8-119">Toimittajan 1099 Int -lomake</span><span class="sxs-lookup"><span data-stu-id="e4dc8-119">Vendor 1099 Int</span></span>  

  <span data-ttu-id="e4dc8-120">Tulostaa liittovaltion 1099-INT -lomakkeen, joka koskee korkotuloja.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-120">Prints the federal form 1099-INT for interest income.</span></span> <span data-ttu-id="e4dc8-121">Voit tulostaa kaikki tai tietyt 1099-INT -lomakkeet.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-121">You can print all or specific 1099-INT forms.</span></span> <span data-ttu-id="e4dc8-122">Raportti käyttää koodeja **IRS 1099 -verolomakkeen ruutu** -ikkunasta, jotka koskevat INT-lomakkeen määrä-ruutuja.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-122">The report uses the codes that apply to the INT form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="e4dc8-123">Toimittajan 1099 Misc -lomake - Sekalaiset tulot</span><span class="sxs-lookup"><span data-stu-id="e4dc8-123">Vendor 1099 Misc - Miscellaneous income</span></span>  

  <span data-ttu-id="e4dc8-124">Tulostaa liittovaltion 1099-MISC -lomakkeen, joka koskee sekalaisia tuloja.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-124">Prints the federal form 1099-MISC for miscellaneous income.</span></span> <span data-ttu-id="e4dc8-125">Voti tulostaa kaikki tai tietyt 1099-MISC -lomakkeet.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-125">You can print all or specific 1099-MISC forms.</span></span> <span data-ttu-id="e4dc8-126">Raportti käyttää koodeja **IRS 1099 -verolomakkeen ruutu** -ikkunasta, jotka koskevat MISC-lomakkeen määrä-ruutuja.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-126">The report uses the codes that apply to the MISC form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  

<span data-ttu-id="e4dc8-127">Tätä raporttia ja taulukkotietoja koskevat lainsäädännölliset muutokset käsitellään yleensä vuodenvaihteen päivityksissä.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-127">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="e4dc8-128">**Toimittajan 1099-tiedot** -raportin suorittaminen ja tarkastus ennen lomakkeiden tulostamista voi olla tarpeen.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-128">It may be helpful to run the **Vendor 1099 Information** report to review the data before printing the forms.</span></span>

## <a name="submitting-1099-tax-forms-electronically"></a><span data-ttu-id="e4dc8-129">1099-veroilmoituksen lähettäminen sähköisesti</span><span class="sxs-lookup"><span data-stu-id="e4dc8-129">Submitting 1099 tax forms electronically</span></span>
<span data-ttu-id="e4dc8-130">Voit lähettää 1099-veroilmoituksen sähköisesti käyttämällä **Toimittajan 1099-lomake magneettisella tallennusvälineellä** -raporttia.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-130">To submit the 1099 tax forms electronically, use the **Vendor 1099 Magnetic Media** report.</span></span> <span data-ttu-id="e4dc8-131">Määrittää 1099-lomakkeet, jotka voidaan viedä.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-131">Specifies the 1099 forms that can be exported.</span></span> <span data-ttu-id="e4dc8-132">Tämän raportin viemät lomaketiedot ovat samat kuin aikaisemmassa osassa kuvattujen raporttien, jotka tulostavat 1099-lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-132">The form information exported by this report is the same as the reports that print 1099 forms that are described in the previous section.</span></span>  

<span data-ttu-id="e4dc8-133">Raportti käyttää koodeja **IRS 1099 -verolomakkeen ruutu** -ikkunasta, jotka koskevat lomakkeen määrä-ruutuja.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-133">The report uses the codes that apply to the form amount boxes from the **IRS 1099 Form-Box** window.</span></span> <span data-ttu-id="e4dc8-134">Koodit on yhdistetty tämän raportin tiedostoasetteluiden lomakeruutuihin, joten taulukon tietojen ja raportin version on vastattava tiettyä verovuotta.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-134">The codes are mapped to the form boxes in the file layouts of this report, therefore the table data and report version for a particular tax year must be in agreement.</span></span> <span data-ttu-id="e4dc8-135">Jos taulukkoon on lisätty mukautettuja koodeja, ne on yhdistettävä lomakeruutuihin tässä objektissa.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-135">If any custom codes are added to the table these must be mapped to the form boxes inside this object.</span></span>  

<span data-ttu-id="e4dc8-136">Tätä raporttia ja taulukkotietoja koskevat lainsäädännölliset muutokset käsitellään yleensä vuodenvaihteen päivityksissä.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-136">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="e4dc8-137">**Toimittajan 1099-tiedot** -raportin suorittaminen ja tarkastus ennen tiedoston luontia voi olla tarpeen.</span><span class="sxs-lookup"><span data-stu-id="e4dc8-137">It may be helpful to run the **Vendor 1099 Information** report to review the data before generating the electronic file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4dc8-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e4dc8-138">See Also</span></span>
[<span data-ttu-id="e4dc8-139">Toimintaohje: Uusien toimittajien rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="e4dc8-139">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
[<span data-ttu-id="e4dc8-140">Toimintaohje: Ostojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="e4dc8-140">How to: Record Purchase</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="e4dc8-141">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e4dc8-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

