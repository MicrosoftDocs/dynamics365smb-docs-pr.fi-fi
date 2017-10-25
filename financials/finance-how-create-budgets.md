---
title: Budjettien luonti| Microsoft Docs
description: "Tässä artikkelissa kuvataan, miten luot budjetteja ennustamaan erilaisia taloudellisia toimintoja ja miten määrität dimensioita liiketoimintatietoja varten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cda69d70ece090a149a13e5e1f4ed02fa70c49f7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create--budgets"></a><span data-ttu-id="89498-103">Uusien budjettien luominen</span><span class="sxs-lookup"><span data-stu-id="89498-103">How to: Create  Budgets</span></span>
<span data-ttu-id="89498-104">Sinulla voi olla useita budjetteja samalle ajanjaksolle, kun luot budjetit eri nimillä.</span><span class="sxs-lookup"><span data-stu-id="89498-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="89498-105">Määrittele ensin budjetin nimi ja syötä budjettiluvut.</span><span class="sxs-lookup"><span data-stu-id="89498-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="89498-106">Budjetin nimi tulee sitten kaikkiin luomiisi budjettitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="89498-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="89498-107">Kun luot budjetin, voit määritellä jokaiselle budjetille neljä dimensiota.</span><span class="sxs-lookup"><span data-stu-id="89498-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="89498-108">Näitä budjettikohtaisia dimensioita kutsutaan budjettidimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="89498-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="89498-109">Valitse budjettidimensiot jo luomistasi dimensioista.</span><span class="sxs-lookup"><span data-stu-id="89498-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="89498-110">Budjettidimensioita voidaan käyttää, kun halutaan asettaa suodatin budjetille tai kun halutaan lisätä dimensiotietoa budjettitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="89498-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="89498-111">Lisätietoja on kohdassa [Dimensioiden käyttäminen](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="89498-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="89498-112">Budjeteilla on tärkeä osa liiketoimintatiedoissa, kuten KP-raporttimalleihin perustuvissa tilinpäätöksissä, jotka sisältävät budjettitapahtumia, tai analysoitaessa budjetoituja summia todellisia summia vastaan tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="89498-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="89498-113">Lisätietoja on ohjeaiheessa [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="89498-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="89498-114">Budjeteilla on tärkeä osa budjettitapahtumia sisältävissä liiketoimintatiedoissa, kuten KP-raporttimalleihin perustuvissa tilinpäätöksissä, tai analysoitaessa tilikartan budjetoituja ja todellisia summia.</span><span class="sxs-lookup"><span data-stu-id="89498-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="89498-115">Lisätietoja on kohdassa [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="89498-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="89498-116">Voit käsitellä kustannusbudjetteja samalla tavoin kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="89498-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="89498-117">Lisätietoja on kohdassa [Kustannusbudjettien luominen](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="89498-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

 > [!NOTE]  
>   <span data-ttu-id="89498-118">Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**.</span><span class="sxs-lookup"><span data-stu-id="89498-118">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="89498-119">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="89498-119">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>  

### <a name="to-create-a-new-budget"></a><span data-ttu-id="89498-120">Uuden budjetin luominen</span><span class="sxs-lookup"><span data-stu-id="89498-120">To create a new budget</span></span>  

1. <span data-ttu-id="89498-121">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **KP-budjetit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="89498-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="89498-122">Valitse **Muokkaa luetteloa** -toiminto ja täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="89498-122">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="89498-123">Valitse **Muokkaa budjettia** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="89498-123">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="89498-124">Täyttämällä **Budjetti**-ikkunan yläosan kentät määrität, mitä näytetään.</span><span class="sxs-lookup"><span data-stu-id="89498-124">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="89498-125">Näytössä näkyvät vain ne tapahtumat, joilla on **Budjetin nimi** -kentässä annettu nimi.</span><span class="sxs-lookup"><span data-stu-id="89498-125">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="89498-126">Koska budjetin nimi on juuri luotu, suodatinta vastaavia tapahtumia ei ole.</span><span class="sxs-lookup"><span data-stu-id="89498-126">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="89498-127">Tämän vuoksi ikkuna on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="89498-127">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="89498-128">Jos haluat lisätä summan, napsauta solua matriisissa.</span><span class="sxs-lookup"><span data-stu-id="89498-128">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="89498-129">**KP-budjetin tapahtumat** -ikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="89498-129">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="89498-130">Luo uusi rivi ja määritä **Summa**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="89498-130">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="89498-131">Sulje **KP-budjetin tapahtumat** -ikkuna.</span><span class="sxs-lookup"><span data-stu-id="89498-131">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="89498-132">Toista vaiheet 5 ja 6, kunnes olet määrittänyt kaikki budjettisummat.</span><span class="sxs-lookup"><span data-stu-id="89498-132">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="89498-133">**Suodattimet** -pikavälilehdessä voit suodattaa budjettitietoja sen mukaan, mitä budjettidimensioita olet luonut budjetin nimen alle.</span><span class="sxs-lookup"><span data-stu-id="89498-133">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="89498-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="89498-134">See Also</span></span>
[<span data-ttu-id="89498-135">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="89498-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="89498-136">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="89498-136">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="89498-137">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="89498-137">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="89498-138">Pääkirjanpito ja tilikartta</span><span class="sxs-lookup"><span data-stu-id="89498-138">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="89498-139">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="89498-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

