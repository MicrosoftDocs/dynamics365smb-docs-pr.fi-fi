---
title: "Nimikkeiden järjestäminen luokkiin| Microsoft Docs"
description: "Nimikkeiden hakemista ja löytämistä helpottaa, kun nimikkeille määritetään määritteitä ja nimikkeet järjestetään luokkiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f7f40054c511b5f3bf1d61dc40d6107cc717dcd8
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="categorize-items"></a><span data-ttu-id="d6417-103">Nimikkeiden luokitteleminen</span><span class="sxs-lookup"><span data-stu-id="d6417-103">Categorize Items</span></span>
<span data-ttu-id="d6417-104">Nimikkeet kannattaa järjestää nimikeluokkiin. Niiden avulla voi järjestellä nimikkeitä ja helpottaa nimikkeiden lajittelemista ja etsimistä.</span><span class="sxs-lookup"><span data-stu-id="d6417-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="d6417-105">Voit etsiä nimikkeitä ominaisuuksien mukaan, kun määrität nimikkeille ja nimikeluokille nimikkeen määritteet.</span><span class="sxs-lookup"><span data-stu-id="d6417-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="d6417-106">Lisätietoja on kohdassa [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d6417-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="d6417-107">Nimikeluokan luominen</span><span class="sxs-lookup"><span data-stu-id="d6417-107">To create an item category</span></span>
1. <span data-ttu-id="d6417-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikekategoriat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d6417-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6417-109">Valitse **Nimikeluokat**-ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d6417-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="d6417-110">Täytä tarvittaessa **Nimikeluokkakortti**-ikkunan **Yleinen**-pikavälilehden kentät:</span><span class="sxs-lookup"><span data-stu-id="d6417-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="d6417-111">Määritä **Määritteet**-pikavälilehdessä kaikki nimikeluokan nimikkeen määritteet.</span><span class="sxs-lookup"><span data-stu-id="d6417-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="d6417-112">Lisätietoja on kohdan [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md) osassa Nimikkeen määritteiden määrittäminen nimikeluokkaan.</span><span class="sxs-lookup"><span data-stu-id="d6417-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="d6417-113">Jos nimikeluokalla on Pääluokka-kentässä ilmaistu **Päänimike**-luokka, kaikki tähän päänimikeluokkaan määritetyt nimikkeen määritteet täytetään **Määritteet**-pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="d6417-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d6417-114">Nimikeluokkaan määritettyjä nimikkeen määritteitä käytetään automaattisesti nimikkeessä, johon nimikeluokka on määritetty.</span><span class="sxs-lookup"><span data-stu-id="d6417-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="d6417-115">Nimikeluokan määrittäminen nimikkeeseen</span><span class="sxs-lookup"><span data-stu-id="d6417-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="d6417-116">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d6417-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6417-117">Avaa sen nimikkeen kortti, jonka haluat määrittää nimikeluokkaan.</span><span class="sxs-lookup"><span data-stu-id="d6417-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="d6417-118">Valitse **Nimikeluokan koodi** -kentän valintapainike ja valitse sitten aiemmin määritetty nimikeluokka.</span><span class="sxs-lookup"><span data-stu-id="d6417-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="d6417-119">Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikeluokan "Nimikeluokan luominen" -osassa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="d6417-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6417-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d6417-120">See Also</span></span>
[<span data-ttu-id="d6417-121">Nimikkeen määritteiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="d6417-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="d6417-122">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="d6417-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="d6417-123">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="d6417-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="d6417-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6417-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

