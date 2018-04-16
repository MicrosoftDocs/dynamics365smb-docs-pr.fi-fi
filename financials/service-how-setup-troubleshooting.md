---
title: "Vianmääritysprosessien määrittäminen| Microsoft Docs"
description: "Lisätietoja sellaisten prosessien määrittämisestä, jotka auttavat huoltohenkilöstöä tunnistamaan ja ratkaisemaan huoltonimikkeiden ongelmia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 14b7dddf1415e06df5e27f063447de633167b81f
ms.contentlocale: fi-fi
ms.lasthandoff: 04/16/2018

---

# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="bf81d-103">Huoltonimikkeiden vianmäärityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf81d-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="bf81d-104">Voit määrittää vianmääritykseen ohjeita, jotka auttavat teknikoita ratkaisemaan ongelmia huollon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bf81d-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="bf81d-105">Ohjeet voivat olla esimerkiksi luettelo korjauksessa noudatettavista vaiheista tai nimikkeitä koskeva kysymyssarja.</span><span class="sxs-lookup"><span data-stu-id="bf81d-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="bf81d-106">Kun vianmääritysohjeet on määritetty, voit määrittää ne huoltonimikeryhmille, huoltonimikkeille ja nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="bf81d-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="bf81d-107">Ohjeet periytyvät hierarkkisesti.</span><span class="sxs-lookup"><span data-stu-id="bf81d-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="bf81d-108">Jos määrität huoltonimikeryhmälle, ryhmään sisältyvät nimikkeet perivät ohjeet ellei niitä määritetä erikseen nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="bf81d-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="bf81d-109">Huoltonimikkeet puolestaan perivät ohjeet nimikkeiltä.</span><span class="sxs-lookup"><span data-stu-id="bf81d-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="bf81d-110">Vianetsinnän suuntaviivojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf81d-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="bf81d-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Vianmääritys** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="bf81d-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bf81d-112">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="bf81d-112">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="bf81d-113">Vianmääritysohjeiden määrittäminen nimikkeille, huoltonimikkeille tai huoltonimikeryhmille</span><span class="sxs-lookup"><span data-stu-id="bf81d-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="bf81d-114">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nimikkeet**, **Huoltonimikkeet** tai **Huoltonimikeryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="bf81d-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bf81d-115">Valitse ensin käsiteltävä objekti ja sitten **Vianmääritys**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="bf81d-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bf81d-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="bf81d-116">See Also</span></span>
[<span data-ttu-id="bf81d-117">Service Management</span><span class="sxs-lookup"><span data-stu-id="bf81d-117">Service Management</span></span>](service-service.md)
