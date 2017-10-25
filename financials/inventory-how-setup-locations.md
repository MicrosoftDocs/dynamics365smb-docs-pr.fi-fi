---
title: "Sijaintikortin ja siirtoreittien määrittäminen| Microsoft Docs"
description: "Jokaisille varastoitavalle varastonimikkeelle luodaan sijaintikortti, kuten varasto tai jakelukeskus. Lisäksi sijaintien välille määritetään siirtoreitit."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7d82b1c63bb1da367736f8dd044640b583493af8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-locations"></a><span data-ttu-id="18cd8-103">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="18cd8-103">How to: Set Up Locations</span></span>
<span data-ttu-id="18cd8-104">Jos ostat, varastoit tai myyt nimikkeitä useamman varaston avulla, sijaintikortti ja siirtoreitit on määritettävä jokaiselle sijainnille.</span><span class="sxs-lookup"><span data-stu-id="18cd8-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="18cd8-105">Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen.</span><span class="sxs-lookup"><span data-stu-id="18cd8-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="18cd8-106">Lisätietoja on myös kohdassa [Varaston hallinta](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="18cd8-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="18cd8-107">Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**.</span><span class="sxs-lookup"><span data-stu-id="18cd8-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="18cd8-108">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="18cd8-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="18cd8-109">Sijaintikortin luominen</span><span class="sxs-lookup"><span data-stu-id="18cd8-109">To create a location card</span></span>
1. <span data-ttu-id="18cd8-110">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="18cd8-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="18cd8-111">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="18cd8-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="18cd8-112">Täytä **Sijaintikortti**-ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="18cd8-112">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="18cd8-113">Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.</span><span class="sxs-lookup"><span data-stu-id="18cd8-113">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="18cd8-114">Monet sijaintikortin kentät viittaavat saapuvien ja lähtevien varastoprosessien nimikkeiden käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="18cd8-114">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="18cd8-115">Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="18cd8-115">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span> 

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="18cd8-116">Siirtoreittien luominen</span><span class="sxs-lookup"><span data-stu-id="18cd8-116">To create a transfer route</span></span>
1. <span data-ttu-id="18cd8-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="18cd8-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="18cd8-118">Voit myös valita **Siirtoreitit**-toiminnon mistä tahansa **Sijaintikortti**-ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="18cd8-118">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="18cd8-119">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="18cd8-119">Choose the **New** action.</span></span>
4. <span data-ttu-id="18cd8-120">Täytä **Sijaintikortti**-ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="18cd8-120">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="18cd8-121">Voit nyt siirtää varastonimikkeitä sijaintien välillä.</span><span class="sxs-lookup"><span data-stu-id="18cd8-121">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="18cd8-122">Lisätietoja on kohdassa [Toimintaohje: Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="18cd8-122">For more information, see [How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="18cd8-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="18cd8-123">See Also</span></span>
[<span data-ttu-id="18cd8-124">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="18cd8-124">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="18cd8-125">[Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="18cd8-125">[How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="18cd8-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="18cd8-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="18cd8-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="18cd8-127">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="18cd8-128">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="18cd8-128">General Business Functionality</span></span>](ui-across-business-areas.md)

