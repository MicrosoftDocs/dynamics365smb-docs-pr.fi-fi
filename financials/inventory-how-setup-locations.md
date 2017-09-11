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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 146fc08f389a5c068044358c59b7d8911f0b3343
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-locations"></a><span data-ttu-id="0c332-103">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0c332-103">How to: Set Up Locations</span></span>
<span data-ttu-id="0c332-104">Jos ostat, varastoit tai myyt nimikkeitä useamman varaston avulla, sijaintikortti ja siirtoreitit on määritettävä jokaiselle sijainnille.</span><span class="sxs-lookup"><span data-stu-id="0c332-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="0c332-105">Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen.</span><span class="sxs-lookup"><span data-stu-id="0c332-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="0c332-106">Lisätietoja on myös kohdassa [Varaston hallinta](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="0c332-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="0c332-107">Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**.</span><span class="sxs-lookup"><span data-stu-id="0c332-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="0c332-108">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="0c332-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="0c332-109">Sijaintikortin luominen</span><span class="sxs-lookup"><span data-stu-id="0c332-109">To create a location card</span></span>
1. <span data-ttu-id="0c332-110">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0c332-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c332-111">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="0c332-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="0c332-112">Täytä **Sijaintikortti**-ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="0c332-112">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="0c332-113">Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.</span><span class="sxs-lookup"><span data-stu-id="0c332-113">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="0c332-114">Siirtoreittien luominen</span><span class="sxs-lookup"><span data-stu-id="0c332-114">To create a transfer route</span></span>
1. <span data-ttu-id="0c332-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0c332-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c332-116">Voit myös valita **Siirtoreitit**-toiminnon mistä tahansa **Sijaintikortti**-ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="0c332-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="0c332-117">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="0c332-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="0c332-118">Täytä **Sijaintikortti**-ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="0c332-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="0c332-119">Voit nyt siirtää varastonimikkeitä sijaintien välillä.</span><span class="sxs-lookup"><span data-stu-id="0c332-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="0c332-120">Lisätietoja on kohdassa [Toimintaohje: Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="0c332-120">For more information, see [How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="0c332-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0c332-121">See Also</span></span>
[<span data-ttu-id="0c332-122">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="0c332-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="0c332-123">Toimitusketju</span><span class="sxs-lookup"><span data-stu-id="0c332-123">Supply Chain</span></span>](madeira-supply-chain.md)  
<span data-ttu-id="0c332-124">[Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="0c332-124">[How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="0c332-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c332-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="0c332-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="0c332-126">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="0c332-127">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="0c332-127">General Business Functionality</span></span>](ui-across-business-areas.md)

