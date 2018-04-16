---
title: Raportin ulkoasun muuttaminen erilaisilla asetteluvalinnoilla | Microsoft Docs
description: "Voit käyttää raportissa erilaisia asetteluja ja muuttaa raportin ulkoa asua asetteluja vaihtelemalla."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: adbae31d6c9b601f4a484b8ea8bacecf0179a408
ms.contentlocale: fi-fi
ms.lasthandoff: 04/16/2018

---
# <a name="change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="2bc23-103">Raportissa tällä hetkellä käytettävän asettelun muuttaminen</span><span class="sxs-lookup"><span data-stu-id="2bc23-103">Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="2bc23-104">Raportti voidaan määrittää useille raportin asetteluille, joita voidaan vaihtaa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2bc23-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="2bc23-105">Raporttiin käytettävissä olevien asettelujen mukaan voit valita valmiin RDLC-raporttiasettelun, sisäänrakennetun Word-raportin asettelun tai mukautetun asettelun käytön välillä.</span><span class="sxs-lookup"><span data-stu-id="2bc23-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="2bc23-106">Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on kohdassa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="2bc23-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="2bc23-107">Raportissa käytetyn asettelun muuttaminen</span><span class="sxs-lookup"><span data-stu-id="2bc23-107">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="2bc23-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Raporttiasetteluvalinta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2bc23-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="2bc23-109">**Raporttiasetteluvalinta**-ikkunassa näkyvät kaikki raportit, jotka ovat käytettävissä yritykselle, joka on määritetty Yritys-kentässä ikkunan yläosassa.</span><span class="sxs-lookup"><span data-stu-id="2bc23-109">The **Report Layout Selection** window lists all the reports that are available for the company that is specified in the Company field at the top of the window.</span></span> <span data-ttu-id="2bc23-110">Valittu asettelu -kenttä määrittää tällä hetkellä raportissa käytetyn asettelun.</span><span class="sxs-lookup"><span data-stu-id="2bc23-110">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="2bc23-111">Aseta **Yritys**-kenttä ikkunan yläosassa yritykseksi, joka sisältää raportin.</span><span class="sxs-lookup"><span data-stu-id="2bc23-111">Set the **Company** field at the top of the window to the company that includes the report.</span></span>
3. <span data-ttu-id="2bc23-112">Voit muuttaa raportin käyttämää asettelua valitsemalla raportin rivin luettelosta ja asettamalla **Valittu asettelu** -kentän arvoksi yhden seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="2bc23-112">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="2bc23-113">RDLC (valmis), käyttää raportissa valmista RDLC-raporttiasettelua.</span><span class="sxs-lookup"><span data-stu-id="2bc23-113">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="2bc23-114">Word (valmis), käyttää raportissa valmista Word-raporttiasettelua.</span><span class="sxs-lookup"><span data-stu-id="2bc23-114">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="2bc23-115">Mukautettu, käyttää raportissa mukautettua asettelua.</span><span class="sxs-lookup"><span data-stu-id="2bc23-115">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="2bc23-116">Raportissa käytettävissä olevat mukautetut asettelut näkyvät Raporttiasettelujen osat -tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="2bc23-116">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="2bc23-117">Jos raportille ei ole mukautettuja asetteluja, sinun on ensin luotava yksi.</span><span class="sxs-lookup"><span data-stu-id="2bc23-117">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="2bc23-118">Jos valitset tämän vaihtoehdon, siirry seuraavaan toimenpiteeseen ja määritä mukautettu asettelu, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="2bc23-118">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

     > [!NOTE]  
     >   <span data-ttu-id="2bc23-119">Jos valitset **RDLC (sisäinen)** tai **Word (sisäinen)** ja näyttöön tulee virhesanoma siitä, että raportin asettelu ei määritetyn tyyppinen, sinun on valittava toinen asetteluvaihtoehto tai luotava mukautettu raportin asettelu, joka on haluamasi tyyppinen.</span><span class="sxs-lookup"><span data-stu-id="2bc23-119">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="2bc23-120">Lisätoimia ei vaadita, jos valitsit valmiin RDLC- tai Word-raporttiasettelun ja asettelua käytetään, kun raportti suoritetaan seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="2bc23-120">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="2bc23-121">Mukautetun asettelun määrittäminen raportille</span><span class="sxs-lookup"><span data-stu-id="2bc23-121">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="2bc23-122">Voit määrittää **Mukautetut raporttiasettelut** -ikkunassa raportille käytettävän mukautetun asettelun.</span><span class="sxs-lookup"><span data-stu-id="2bc23-122">You specify which custom layout to use on the report from the **Custom Report Layouts** window.</span></span> <span data-ttu-id="2bc23-123">Jos **Mukautetut raporttiasettelut** -ikkuna ei ole avoinna, valitse hakupainike **Raporttiasettelun kuvaus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2bc23-123">If the **Custom Report Layouts** window is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="2bc23-124">Valitse **Mukautetut raporttiasettelut** -ikkunassa rivi mukautetulle asettelulle, jota haluat käyttää, ja sulje ikkuna.</span><span class="sxs-lookup"><span data-stu-id="2bc23-124">In the **Custom Report Layouts** window, select the row for custom layout that you want to use, and then close the window.</span></span>

<span data-ttu-id="2bc23-125">Palaa **Raporttiasetteluvalinta**-ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="2bc23-125">You return to the **Report Layout Selection** window.</span></span> <span data-ttu-id="2bc23-126">Valitun mukautetun asettelun nimi näkyy **Mukautetun asettelun kuvaus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2bc23-126">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="2bc23-127">Mukautettua asettelua käytetään seuraavan kerran, kun suoritat raportin.</span><span class="sxs-lookup"><span data-stu-id="2bc23-127">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bc23-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2bc23-128">See Also</span></span>
[<span data-ttu-id="2bc23-129">Raporttiasetteluiden hallinta</span><span class="sxs-lookup"><span data-stu-id="2bc23-129">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="2bc23-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2bc23-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

