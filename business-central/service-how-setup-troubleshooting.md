---
title: Vianmääritysprosessien määrittäminen| Microsoft Docs
description: Lisätietoja sellaisten prosessien määrittämisestä, jotka auttavat huoltohenkilöstöä tunnistamaan ja ratkaisemaan huoltonimikkeiden ongelmia.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 24a4fa9811547acfd3372d3eaf7de7b9f1882c7d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795613"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="21303-103">Huoltonimikkeiden vianmäärityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="21303-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="21303-104">Voit määrittää vianmääritykseen ohjeita, jotka auttavat teknikoita ratkaisemaan ongelmia huollon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="21303-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="21303-105">Ohjeet voivat olla esimerkiksi luettelo korjauksessa noudatettavista vaiheista tai nimikkeitä koskeva kysymyssarja.</span><span class="sxs-lookup"><span data-stu-id="21303-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="21303-106">Kun vianmääritysohjeet on määritetty, voit määrittää ne huoltonimikeryhmille, huoltonimikkeille ja nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="21303-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="21303-107">Ohjeet periytyvät hierarkkisesti.</span><span class="sxs-lookup"><span data-stu-id="21303-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="21303-108">Jos määrität huoltonimikeryhmälle, ryhmään sisältyvät nimikkeet perivät ohjeet ellei niitä määritetä erikseen nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="21303-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="21303-109">Huoltonimikkeet puolestaan perivät ohjeet nimikkeiltä.</span><span class="sxs-lookup"><span data-stu-id="21303-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="21303-110">Vianetsinnän suuntaviivojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="21303-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="21303-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vianmääritys** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="21303-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="21303-112">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="21303-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="21303-113">Vianmääritysohjeiden määrittäminen nimikkeille, huoltonimikkeille tai huoltonimikeryhmille</span><span class="sxs-lookup"><span data-stu-id="21303-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="21303-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet**, **Huoltonimikkeet** tai **Huoltonimikeryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="21303-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="21303-115">Valitse ensin käsiteltävä objekti ja sitten **Vianmääritys**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="21303-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="21303-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="21303-116">See Also</span></span>
[<span data-ttu-id="21303-117">Huoltohallinto</span><span class="sxs-lookup"><span data-stu-id="21303-117">Service Management</span></span>](service-service.md)