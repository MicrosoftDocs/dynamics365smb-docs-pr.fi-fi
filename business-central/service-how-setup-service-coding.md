---
title: Vakiohuoltokoodien määrittäminen | Microsoft Docs
description: Lisätietoja usein tehtävien huoltotoimintojen koodien määrittämisestä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: b9bf54d61ba71281a7069a6977ad1264637eba46
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795641"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="3027d-103">Vakiohuoltokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3027d-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="3027d-104">Kun suoritat tavallisen huollon, sinun on usein luotava samat tiedot sisältävät huoltoasiakirjat ja huoltorivit.</span><span class="sxs-lookup"><span data-stu-id="3027d-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="3027d-105">Voit helpottaa näiden rivien luontia määrittämällä vakiohuoltokoodit, joilla on valmiiksi määritettyjä rivejä.</span><span class="sxs-lookup"><span data-stu-id="3027d-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="3027d-106">Kun valitset koodin huoltoasiakirjassa, rivit annetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="3027d-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="3027d-107">Voit määrittää haluamasi määrän vakiohuoltokoodeja, ja kullakin koodilla voi olla rajoittamaton määrä erilaisia linkitettyjä huoltorivejä, kuten nimike, resurssi, kustannus tai vakioteksti.</span><span class="sxs-lookup"><span data-stu-id="3027d-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="3027d-108">Kunkin vakiohuoltokoodin huoltorivit luodaan **Vakiohuoltokoodi** -kortissa.</span><span class="sxs-lookup"><span data-stu-id="3027d-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="3027d-109">Voit määrittää vakiohuoltokoodit sitten huoltonimikeryhmiin **Huoltonimikeryhmän vakiokoodit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3027d-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="3027d-110">Kun luot myöhemmin huoltoasiakirjan, voit lisätä huoltorivejä **Hae vakiohuoltokoodit** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="3027d-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="3027d-111">Voit luoda rivejä vastaavasti myös myynti-ja ostoasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="3027d-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="3027d-112">Lisätietoja on kohdassa [Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="3027d-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="3027d-113">Vakiohuoltokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3027d-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="3027d-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakiohuoltokoodit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3027d-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3027d-115">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="3027d-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="3027d-116">Täytä tähän huoltokoodiin linkitetyt huoltorivit.</span><span class="sxs-lookup"><span data-stu-id="3027d-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="3027d-117">Vakiohuoltokoodin liittäminen huoltonimikeryhmään:</span><span class="sxs-lookup"><span data-stu-id="3027d-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="3027d-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikeryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3027d-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3027d-119">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="3027d-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="3027d-120">Täytä tähän huoltokoodiin linkitetyt huoltorivit.</span><span class="sxs-lookup"><span data-stu-id="3027d-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3027d-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3027d-121">See Also</span></span>
[<span data-ttu-id="3027d-122">Huoltohallinto</span><span class="sxs-lookup"><span data-stu-id="3027d-122">Service Management</span></span>](service-service.md)