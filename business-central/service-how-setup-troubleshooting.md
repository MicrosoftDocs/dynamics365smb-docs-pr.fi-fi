---
title: Vianmääritysprosessien määrittäminen| Microsoft Docs
description: Lisätietoja sellaisten prosessien määrittämisestä, jotka auttavat huoltohenkilöstöä tunnistamaan ja ratkaisemaan huoltonimikkeiden ongelmia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 214c83c4614a92a8cc94c7dc88efe527686ef397
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773678"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="51577-103">Huoltonimikkeiden vianmäärityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="51577-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="51577-104">Voit määrittää vianmääritykseen ohjeita, jotka auttavat teknikoita ratkaisemaan ongelmia huollon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="51577-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="51577-105">Ohjeet voivat olla esimerkiksi luettelo korjauksessa noudatettavista vaiheista tai nimikkeitä koskeva kysymyssarja.</span><span class="sxs-lookup"><span data-stu-id="51577-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="51577-106">Kun vianmääritysohjeet on määritetty, voit määrittää ne huoltonimikeryhmille, huoltonimikkeille ja nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="51577-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="51577-107">Ohjeet periytyvät hierarkkisesti.</span><span class="sxs-lookup"><span data-stu-id="51577-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="51577-108">Jos määrität huoltonimikeryhmälle, ryhmään sisältyvät nimikkeet perivät ohjeet ellei niitä määritetä erikseen nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="51577-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="51577-109">Huoltonimikkeet puolestaan perivät ohjeet nimikkeiltä.</span><span class="sxs-lookup"><span data-stu-id="51577-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="51577-110">Vianetsinnän suuntaviivojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="51577-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="51577-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Vianetsintä** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="51577-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="51577-112">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="51577-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="51577-113">Vianmääritysohjeiden määrittäminen nimikkeille, huoltonimikkeille tai huoltonimikeryhmille</span><span class="sxs-lookup"><span data-stu-id="51577-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="51577-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet**, **Huoltonimikkeet** tai **Huoltonimikeryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="51577-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="51577-115">Valitse ensin käsiteltävä objekti ja sitten **Vianmääritys**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="51577-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="51577-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="51577-116">See Also</span></span>
[<span data-ttu-id="51577-117">Huoltohallinto</span><span class="sxs-lookup"><span data-stu-id="51577-117">Service Management</span></span>](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]