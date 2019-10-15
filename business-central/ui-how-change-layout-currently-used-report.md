---
title: Raportin ulkoasun muuttaminen erilaisilla asetteluvalinnoilla | Microsoft Docs
description: Voit käyttää raportissa erilaisia asetteluja ja muuttaa raportin ulkoa asua asetteluja vaihtelemalla.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07de4be7bc516cf9f4b802a48dc59293b1992f5f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315250"
---
# <a name="change-the-current-report-layout"></a><span data-ttu-id="a7c58-103">Nykyisen raportin asettelun muuttaminen</span><span class="sxs-lookup"><span data-stu-id="a7c58-103">Change the Current Report Layout</span></span>
<span data-ttu-id="a7c58-104">Raportti voidaan määrittää useille raportin asetteluille, joita voidaan vaihtaa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a7c58-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="a7c58-105">Raporttiin käytettävissä olevien asettelujen mukaan voit valita valmiin RDLC-raporttiasettelun, sisäänrakennetun Word-raportin asettelun tai mukautetun asettelun käytön välillä.</span><span class="sxs-lookup"><span data-stu-id="a7c58-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="a7c58-106">Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on ohjeaiheessa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="a7c58-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

> [!TIP]  
> <span data-ttu-id="a7c58-107">Word-raportin asettelua käyttävät asiakirjaraportit (eivät luettelot) ovat yleensä nopeampia kuin RDLC-raporttiasettelua käyttävät raportit.</span><span class="sxs-lookup"><span data-stu-id="a7c58-107">Document reports (not lists) that use a Word report layout are typically faster than those that use an RDLC report layout.</span></span> <span data-ttu-id="a7c58-108">Jos sinulla on mahdollisuus valita asiakirjaraportin asetteluksi joko Word- tai RDLC-raportin asettelua, Word-raporttiasettelu on paras vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="a7c58-108">So if you have the option to choose between a Word or RDLC report layout for a document report, use the Word report layout for the best performance.</span></span>  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="a7c58-109">Raportissa käytetyn asettelun muuttaminen</span><span class="sxs-lookup"><span data-stu-id="a7c58-109">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="a7c58-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasetteluvalinta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a7c58-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="a7c58-111">**Raporttiasetteluvalinta**-sivulla on luettelo kaikista raporteista, joita voi käyttää sivun yläosan Yritys-kentässä määritetyssä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="a7c58-111">The **Report Layout Selection** page lists all the reports that are available for the company that is specified in the Company field at the top of the page.</span></span> <span data-ttu-id="a7c58-112">Valittu asettelu -kenttä määrittää tällä hetkellä raportissa käytetyn asettelun.</span><span class="sxs-lookup"><span data-stu-id="a7c58-112">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="a7c58-113">Määritä **Yritys**-kenttä sivun yläosassa yritykseksi, joka sisältää raportin.</span><span class="sxs-lookup"><span data-stu-id="a7c58-113">Set the **Company** field at the top of the page to the company that includes the report.</span></span>
3. <span data-ttu-id="a7c58-114">Voit muuttaa raportin käyttämää asettelua valitsemalla raportin rivin luettelosta ja asettamalla **Valittu asettelu** -kentän arvoksi yhden seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="a7c58-114">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="a7c58-115">RDLC (valmis), käyttää raportissa valmista RDLC-raporttiasettelua.</span><span class="sxs-lookup"><span data-stu-id="a7c58-115">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="a7c58-116">Word (valmis), käyttää raportissa valmista Word-raporttiasettelua.</span><span class="sxs-lookup"><span data-stu-id="a7c58-116">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="a7c58-117">Mukautettu, käyttää raportissa mukautettua asettelua.</span><span class="sxs-lookup"><span data-stu-id="a7c58-117">Custom, uses a custom layout on the report.</span></span>  

<span data-ttu-id="a7c58-118">Raportissa käytettävissä olevat mukautetut asettelut näkyvät **Raporttiasettelujen osat** -tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="a7c58-118">You can see which custom layouts are available for the report in the **Report Layouts Part** FactBox.</span></span> <span data-ttu-id="a7c58-119">Jos raportille ei ole mukautettuja asetteluja, sinun on ensin luotava yksi.</span><span class="sxs-lookup"><span data-stu-id="a7c58-119">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="a7c58-120">Jos valitset tämän vaihtoehdon, siirry seuraavaan toimenpiteeseen ja määritä mukautettu asettelu, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="a7c58-120">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

> [!NOTE]
> <span data-ttu-id="a7c58-121">Jos valitset **RDLC (sisäinen)** tai **Word (sisäinen)** ja näyttöön tulee virhesanoma siitä, että raportin asettelu ei määritetyn tyyppinen, sinun on valittava toinen asetteluvaihtoehto tai luotava mukautettu raportin asettelu, joka on haluamasi tyyppinen.</span><span class="sxs-lookup"><span data-stu-id="a7c58-121">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="a7c58-122">Lisätoimia ei vaadita, jos valitsit valmiin RDLC- tai Word-raporttiasettelun ja asettelua käytetään, kun raportti suoritetaan seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="a7c58-122">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="a7c58-123">Mukautetun asettelun määrittäminen raportille</span><span class="sxs-lookup"><span data-stu-id="a7c58-123">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="a7c58-124">Voit määrittää **Mukautetut raporttiasettelut** -sivulla raportille käytettävän mukautetun asettelun.</span><span class="sxs-lookup"><span data-stu-id="a7c58-124">You specify which custom layout to use on the report from the **Custom Report Layouts** page.</span></span> <span data-ttu-id="a7c58-125">Jos **Mukautetut raporttiasettelut** -sivu ei ole avoinna, valitse hakupainike **Raporttiasettelun kuvaus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a7c58-125">If the **Custom Report Layouts** page is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="a7c58-126">Valitse **Mukautetut raporttiasettelut** -sivulla rivi mukautetulle asettelulle, jota haluat käyttää, ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a7c58-126">On the **Custom Report Layouts** page, select the row for custom layout that you want to use, and then close the page.</span></span>

<span data-ttu-id="a7c58-127">Palaa **Raporttiasetteluvalinta**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="a7c58-127">You return to the **Report Layout Selection** page.</span></span> <span data-ttu-id="a7c58-128">Valitun mukautetun asettelun nimi näkyy **Mukautetun asettelun kuvaus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a7c58-128">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="a7c58-129">Mukautettua asettelua käytetään seuraavan kerran, kun suoritat raportin.</span><span class="sxs-lookup"><span data-stu-id="a7c58-129">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7c58-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a7c58-130">See Also</span></span>
[<span data-ttu-id="a7c58-131">Raporttiasetteluiden hallinta</span><span class="sxs-lookup"><span data-stu-id="a7c58-131">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="a7c58-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a7c58-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
