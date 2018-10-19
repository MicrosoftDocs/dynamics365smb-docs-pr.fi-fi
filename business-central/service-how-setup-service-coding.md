---
title: "Vakiohuoltokoodien määrittäminen | Microsoft Docs"
description: "Lisätietoja usein tehtävien huoltotoimintojen koodien määrittämisestä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f73f5b9d74e7b6a75be6320697aa1a4ad84fb4a1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="c5ae5-103">Vakiohuoltokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c5ae5-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="c5ae5-104">Kun suoritat tavallisen huollon, sinun on usein luotava samat tiedot sisältävät huoltoasiakirjat ja huoltorivit.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="c5ae5-105">Voit helpottaa näiden rivien luontia määrittämällä vakiohuoltokoodit, joilla on valmiiksi määritettyjä rivejä.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="c5ae5-106">Kun valitset koodin huoltoasiakirjassa, rivit annetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="c5ae5-107">Voit määrittää haluamasi määrän vakiohuoltokoodeja, ja kullakin koodilla voi olla rajoittamaton määrä erilaisia linkitettyjä huoltorivejä, kuten nimike, resurssi, kustannus tai vakioteksti.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="c5ae5-108">Kunkin vakiohuoltokoodin huoltorivit luodaan **Vakiohuoltokoodi** -kortissa.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="c5ae5-109">Voit liittää huoltonimikeryhmiin vakiohuoltokoodeja **Huoltonimikeryhmän vakiokoodit** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-109">You then assign standard service codes to service item groups in the **Standard Serv. Item Gr. Codes** window.</span></span> <span data-ttu-id="c5ae5-110">Kun luot myöhemmin huoltoasiakirjan, voit lisätä huoltorivejä **Hae vakiohuoltokoodit** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="c5ae5-111">Voit luoda rivejä vastaavasti myös myynti-ja ostoasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="c5ae5-112">Lisätietoja on kohdassa [Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="c5ae5-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="c5ae5-113">Vakiohuoltokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c5ae5-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="c5ae5-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakiohuoltokoodit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c5ae5-115">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="c5ae5-116">Täytä tähän huoltokoodiin linkitetyt huoltorivit.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="c5ae5-117">Vakiohuoltokoodin liittäminen huoltonimikeryhmään:</span><span class="sxs-lookup"><span data-stu-id="c5ae5-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="c5ae5-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikeryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c5ae5-119">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="c5ae5-120">Täytä tähän huoltokoodiin linkitetyt huoltorivit.</span><span class="sxs-lookup"><span data-stu-id="c5ae5-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5ae5-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c5ae5-121">See Also</span></span>
[<span data-ttu-id="c5ae5-122">Service Management</span><span class="sxs-lookup"><span data-stu-id="c5ae5-122">Service Management</span></span>](service-service.md)
