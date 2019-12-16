---
title: Sijaintikortin ja siirtoreittien määrittäminen| Microsoft Docs
description: Jokaisille varastoitavalle varastonimikkeelle luodaan sijaintikortti, kuten varasto tai jakelukeskus. Lisäksi sijaintien välille määritetään siirtoreitit.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2019
ms.author: SorenGP
ms.openlocfilehash: 5554bb1576705cd1f3cbcddc7ef33da7b5db3796
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878308"
---
# <a name="set-up-locations"></a><span data-ttu-id="859e4-103">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="859e4-103">Set Up Locations</span></span>
<span data-ttu-id="859e4-104">Jos ostat, varastoit tai myyt nimikkeitä useamman varaston avulla, sijaintikortti ja siirtoreitit on määritettävä jokaiselle sijainnille.</span><span class="sxs-lookup"><span data-stu-id="859e4-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="859e4-105">Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen.</span><span class="sxs-lookup"><span data-stu-id="859e4-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="859e4-106">Lisätietoja on myös kohdassa [Varaston hallinta](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="859e4-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq]

## <a name="to-create-a-location-card"></a><span data-ttu-id="859e4-107">Sijaintikortin luominen</span><span class="sxs-lookup"><span data-stu-id="859e4-107">To create a location card</span></span>
1. <span data-ttu-id="859e4-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sijainnit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="859e4-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="859e4-109">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="859e4-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="859e4-110">Täytä **Sijaintikortti**-sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="859e4-110">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="859e4-111">Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.</span><span class="sxs-lookup"><span data-stu-id="859e4-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="859e4-112">Monet sijaintikortin kentät viittaavat saapuvien ja lähtevien varastoprosessien nimikkeiden käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="859e4-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="859e4-113">Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="859e4-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="859e4-114">Siirtoreittien luominen</span><span class="sxs-lookup"><span data-stu-id="859e4-114">To create a transfer route</span></span>
1. <span data-ttu-id="859e4-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Siirtoreitit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="859e4-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="859e4-116">Voit myös valita **Siirtoreitit**-toiminnon miltä tahansa **Sijaintikortti**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="859e4-116">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="859e4-117">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="859e4-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="859e4-118">Täytä **Sijaintikortti**-sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="859e4-118">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="859e4-119">Voit nyt siirtää varastonimikkeitä sijaintien välillä.</span><span class="sxs-lookup"><span data-stu-id="859e4-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="859e4-120">Lisätietoja on kohdassa [Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="859e4-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="859e4-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="859e4-121">See Also</span></span>
[<span data-ttu-id="859e4-122">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="859e4-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="859e4-123">[Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="859e4-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="859e4-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="859e4-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="859e4-125">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="859e4-125">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="859e4-126">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="859e4-126">General Business Functionality</span></span>](ui-across-business-areas.md)
