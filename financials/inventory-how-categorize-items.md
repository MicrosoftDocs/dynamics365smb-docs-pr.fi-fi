---
title: "Nimikkeiden järjestäminen luokkiin| Microsoft Docs"
description: "Nimikkeiden hakemista ja löytämistä helpottaa, kun nimikkeille määritetään määritteitä ja nimikkeet järjestetään luokkiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: e34e4951921f144ea7b718f62b116f9f01fc240d
ms.contentlocale: fi-fi
ms.lasthandoff: 04/16/2018

---
# <a name="categorize-items"></a><span data-ttu-id="a1a28-103">Nimikkeiden luokitteleminen</span><span class="sxs-lookup"><span data-stu-id="a1a28-103">Categorize Items</span></span>
<span data-ttu-id="a1a28-104">Nimikkeet kannattaa järjestää nimikeluokkiin. Niiden avulla voi järjestellä nimikkeitä ja helpottaa nimikkeiden lajittelemista ja etsimistä.</span><span class="sxs-lookup"><span data-stu-id="a1a28-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="a1a28-105">Voit etsiä nimikkeitä ominaisuuksien mukaan, kun määrität nimikkeille ja nimikeluokille nimikkeen määritteet.</span><span class="sxs-lookup"><span data-stu-id="a1a28-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="a1a28-106">Lisätietoja on kohdassa [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a1a28-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="a1a28-107">Nimikeluokan luominen</span><span class="sxs-lookup"><span data-stu-id="a1a28-107">To create an item category</span></span>
1. <span data-ttu-id="a1a28-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikekategoriat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a1a28-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="a1a28-109">Valitse **Nimikeluokat**-ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="a1a28-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="a1a28-110">Täytä tarvittaessa **Nimikeluokkakortti**-ikkunan **Yleinen**-pikavälilehden kentät:</span><span class="sxs-lookup"><span data-stu-id="a1a28-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="a1a28-111">Määritä **Määritteet**-pikavälilehdessä kaikki nimikeluokan nimikkeen määritteet.</span><span class="sxs-lookup"><span data-stu-id="a1a28-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="a1a28-112">Lisätietoja on kohdan [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md) osassa Nimikkeen määritteiden määrittäminen nimikeluokkaan.</span><span class="sxs-lookup"><span data-stu-id="a1a28-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="a1a28-113">Jos nimikeluokalla on Pääluokka-kentässä ilmaistu **Päänimike**-luokka, kaikki tähän päänimikeluokkaan määritetyt nimikkeen määritteet täytetään **Määritteet**-pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="a1a28-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a1a28-114">Nimikeluokkaan määritettyjä nimikkeen määritteitä käytetään automaattisesti nimikkeessä, johon nimikeluokka on määritetty.</span><span class="sxs-lookup"><span data-stu-id="a1a28-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="a1a28-115">Nimikeluokan määrittäminen nimikkeeseen</span><span class="sxs-lookup"><span data-stu-id="a1a28-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="a1a28-116">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a1a28-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="a1a28-117">Avaa sen nimikkeen kortti, jonka haluat määrittää nimikeluokkaan.</span><span class="sxs-lookup"><span data-stu-id="a1a28-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="a1a28-118">Valitse **Nimikeluokan koodi** -kentän valintapainike ja valitse sitten aiemmin määritetty nimikeluokka.</span><span class="sxs-lookup"><span data-stu-id="a1a28-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="a1a28-119">Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikeluokan "Nimikeluokan luominen" -osassa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="a1a28-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1a28-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a1a28-120">See Also</span></span>
[<span data-ttu-id="a1a28-121">Nimikkeen määritteiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="a1a28-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="a1a28-122">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="a1a28-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="a1a28-123">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="a1a28-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a1a28-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a1a28-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

