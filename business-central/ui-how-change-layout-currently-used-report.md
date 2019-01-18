---
title: Raportin ulkoasun muuttaminen erilaisilla asetteluvalinnoilla | Microsoft Docs
description: "Voit käyttää raportissa erilaisia asetteluja ja muuttaa raportin ulkoa asua asetteluja vaihtelemalla."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a68c26e94aa4adda7c1f546e57331a741dcfe94b
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="151ec-103">Raportissa tällä hetkellä käytettävän asettelun muuttaminen</span><span class="sxs-lookup"><span data-stu-id="151ec-103">Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="151ec-104">Raportti voidaan määrittää useille raportin asetteluille, joita voidaan vaihtaa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="151ec-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="151ec-105">Raporttiin käytettävissä olevien asettelujen mukaan voit valita valmiin RDLC-raporttiasettelun, sisäänrakennetun Word-raportin asettelun tai mukautetun asettelun käytön välillä.</span><span class="sxs-lookup"><span data-stu-id="151ec-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="151ec-106">Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on ohjeaiheessa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="151ec-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="151ec-107">Raportissa käytetyn asettelun muuttaminen</span><span class="sxs-lookup"><span data-stu-id="151ec-107">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="151ec-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasetteluvalinta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="151ec-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="151ec-109">**Raporttiasetteluvalinta**-sivulla on luettelo kaikista raporteista, joita voi käyttää sivun yläosan Yritys-kentässä määritetyssä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="151ec-109">The **Report Layout Selection** page lists all the reports that are available for the company that is specified in the Company field at the top of the page.</span></span> <span data-ttu-id="151ec-110">Valittu asettelu -kenttä määrittää tällä hetkellä raportissa käytetyn asettelun.</span><span class="sxs-lookup"><span data-stu-id="151ec-110">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="151ec-111">Määritä **Yritys**-kenttä sivun yläosassa yritykseksi, joka sisältää raportin.</span><span class="sxs-lookup"><span data-stu-id="151ec-111">Set the **Company** field at the top of the page to the company that includes the report.</span></span>
3. <span data-ttu-id="151ec-112">Voit muuttaa raportin käyttämää asettelua valitsemalla raportin rivin luettelosta ja asettamalla **Valittu asettelu** -kentän arvoksi yhden seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="151ec-112">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="151ec-113">RDLC (valmis), käyttää raportissa valmista RDLC-raporttiasettelua.</span><span class="sxs-lookup"><span data-stu-id="151ec-113">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="151ec-114">Word (valmis), käyttää raportissa valmista Word-raporttiasettelua.</span><span class="sxs-lookup"><span data-stu-id="151ec-114">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="151ec-115">Mukautettu, käyttää raportissa mukautettua asettelua.</span><span class="sxs-lookup"><span data-stu-id="151ec-115">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="151ec-116">Raportissa käytettävissä olevat mukautetut asettelut näkyvät Raporttiasettelujen osat -tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="151ec-116">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="151ec-117">Jos raportille ei ole mukautettuja asetteluja, sinun on ensin luotava yksi.</span><span class="sxs-lookup"><span data-stu-id="151ec-117">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="151ec-118">Jos valitset tämän vaihtoehdon, siirry seuraavaan toimenpiteeseen ja määritä mukautettu asettelu, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="151ec-118">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="151ec-119">Jos valitset **RDLC (sisäinen)** tai **Word (sisäinen)** ja näyttöön tulee virhesanoma siitä, että raportin asettelu ei määritetyn tyyppinen, sinun on valittava toinen asetteluvaihtoehto tai luotava mukautettu raportin asettelu, joka on haluamasi tyyppinen.</span><span class="sxs-lookup"><span data-stu-id="151ec-119">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="151ec-120">Lisätoimia ei vaadita, jos valitsit valmiin RDLC- tai Word-raporttiasettelun ja asettelua käytetään, kun raportti suoritetaan seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="151ec-120">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="151ec-121">Mukautetun asettelun määrittäminen raportille</span><span class="sxs-lookup"><span data-stu-id="151ec-121">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="151ec-122">Voit määrittää **Mukautetut raporttiasettelut** -sivulla raportille käytettävän mukautetun asettelun.</span><span class="sxs-lookup"><span data-stu-id="151ec-122">You specify which custom layout to use on the report from the **Custom Report Layouts** page.</span></span> <span data-ttu-id="151ec-123">Jos **Mukautetut raporttiasettelut** -sivu ei ole avoinna, valitse hakupainike **Raporttiasettelun kuvaus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="151ec-123">If the **Custom Report Layouts** page is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="151ec-124">Valitse **Mukautetut raporttiasettelut** -sivulla rivi mukautetulle asettelulle, jota haluat käyttää, ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="151ec-124">On the **Custom Report Layouts** page, select the row for custom layout that you want to use, and then close the page.</span></span>

<span data-ttu-id="151ec-125">Palaa **Raporttiasetteluvalinta**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="151ec-125">You return to the **Report Layout Selection** page.</span></span> <span data-ttu-id="151ec-126">Valitun mukautetun asettelun nimi näkyy **Mukautetun asettelun kuvaus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="151ec-126">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="151ec-127">Mukautettua asettelua käytetään seuraavan kerran, kun suoritat raportin.</span><span class="sxs-lookup"><span data-stu-id="151ec-127">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="151ec-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="151ec-128">See Also</span></span>
[<span data-ttu-id="151ec-129">Raporttiasetteluiden hallinta</span><span class="sxs-lookup"><span data-stu-id="151ec-129">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="151ec-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="151ec-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

