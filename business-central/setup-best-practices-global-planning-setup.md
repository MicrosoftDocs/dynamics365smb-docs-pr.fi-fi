---
title: Yleisten suunnitteluasetusten parhaat käytännöt | Microsoft Docs
description: Suunnittelu-pikavälilehden Tuotannon asetukset-sivulla on useita kenttiä, jotka määrittävät tarjonnan suunnittelun yleiset säännöt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9dfc1c42d2ce74792209b25b1fb6e48126ed9d5a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391097"
---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="98c7d-103">Asetukset - parhaat käytännöt: yleiset suunnitteluasetukset</span><span class="sxs-lookup"><span data-stu-id="98c7d-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="98c7d-104">**Suunnittelu**-pikavälilehden **Tuotannon asetukset**-sivulla on useita kenttiä, jotka määrittävät tarjonnan suunnittelun yleiset säännöt.</span><span class="sxs-lookup"><span data-stu-id="98c7d-104">The **Planning** FastTab on the **Manufacturing Setup** page contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="98c7d-105">Seuraavassa taulukossa on parhaita käytäntöjä siitä, miten voit määrittää valitun yleisen suunnitteluparametrin kentät.</span><span class="sxs-lookup"><span data-stu-id="98c7d-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="98c7d-106">Saat lisätietoja kentästä valitsemalla **Asetuskenttä**-sarakkeessa olevan linkin.</span><span class="sxs-lookup"><span data-stu-id="98c7d-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="98c7d-107">Kentän asetukset</span><span class="sxs-lookup"><span data-stu-id="98c7d-107">Setup field</span></span>|<span data-ttu-id="98c7d-108">Parhaat käytännöt</span><span class="sxs-lookup"><span data-stu-id="98c7d-108">Best practice</span></span>|<span data-ttu-id="98c7d-109">Kommentti</span><span class="sxs-lookup"><span data-stu-id="98c7d-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="98c7d-110">Käytä ennustetta sijainneissa</span><span class="sxs-lookup"><span data-stu-id="98c7d-110">Use Forecast on Locations</span></span>|<span data-ttu-id="98c7d-111">Valitse, jos sinulla on määrättyjen sijaintien ennusteet.</span><span class="sxs-lookup"><span data-stu-id="98c7d-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="98c7d-112">Komponentit sijainnissa</span><span class="sxs-lookup"><span data-stu-id="98c7d-112">Components at Location</span></span>|<span data-ttu-id="98c7d-113">Jos nimikkeitä ei ole määritetty varastointiyksikköinä, valitse fyysisen päävaraston sijaintikoodi.</span><span class="sxs-lookup"><span data-stu-id="98c7d-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="98c7d-114">Tämä pätee myös, jos käytetään vain hankintalistaa.</span><span class="sxs-lookup"><span data-stu-id="98c7d-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="98c7d-115">Tyhjä ylivuototaso</span><span class="sxs-lookup"><span data-stu-id="98c7d-115">Blank Overflow Level</span></span>|<span data-ttu-id="98c7d-116">Valitse **Salli oletuslaskenta**, jos siirryt Microsoft Dynamics NAV 5.0- tai sitä aikaisemmasta versiosta.</span><span class="sxs-lookup"><span data-stu-id="98c7d-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="98c7d-117">Käytä vain, jos haluat sallia kaikkien tai joidenkin kohteiden ylittää uusintatilauspisteen.</span><span class="sxs-lookup"><span data-stu-id="98c7d-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="98c7d-118">Oletusvaimentimen jakso</span><span class="sxs-lookup"><span data-stu-id="98c7d-118">Default Dampener Period</span></span>|<span data-ttu-id="98c7d-119">Valitse 1D tai 5D.</span><span class="sxs-lookup"><span data-stu-id="98c7d-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="98c7d-120">Jos et ole aiemmin käyttänyt ohjelman [!INCLUDE[prod_short](includes/prod_short.md)] suunnittelutoimintoa, määritä pidempi jakso.</span><span class="sxs-lookup"><span data-stu-id="98c7d-120">If new to planning in [!INCLUDE[prod_short](includes/prod_short.md)], then set a longer period.</span></span>|<span data-ttu-id="98c7d-121">Kun käyttäjät tuntevat toimintosanomien eri syyt, lyhennä puskuriaikaa antaaksesi lisää muutosehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="98c7d-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="98c7d-122">Oletuspuskurimäärä-%</span><span class="sxs-lookup"><span data-stu-id="98c7d-122">Default Dampener Quantity %</span></span>|<span data-ttu-id="98c7d-123">Määritä 5-20% nimikkeen eräkoosta.</span><span class="sxs-lookup"><span data-stu-id="98c7d-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="98c7d-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="98c7d-124">See Also</span></span>  
 <span data-ttu-id="98c7d-125">[Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="98c7d-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="98c7d-126">[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="98c7d-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="98c7d-127">Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla</span><span class="sxs-lookup"><span data-stu-id="98c7d-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="98c7d-128">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98c7d-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]