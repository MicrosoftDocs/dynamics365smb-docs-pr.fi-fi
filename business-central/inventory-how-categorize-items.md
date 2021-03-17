---
title: Nimikkeiden järjestäminen luokkiin| Microsoft Docs
description: Nimikkeiden hakemista ja löytämistä helpottaa, kun nimikkeille määritetään määritteitä ja nimikkeet järjestetään luokkiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: be99e52436605e522756489fa9c804887af18559
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388046"
---
# <a name="categorize-items"></a><span data-ttu-id="c7e87-103">Nimikkeiden luokitteleminen</span><span class="sxs-lookup"><span data-stu-id="c7e87-103">Categorize Items</span></span>

<span data-ttu-id="c7e87-104">Nimikkeet kannattaa järjestää nimikeluokkiin. Niiden avulla voi järjestellä nimikkeitä ja helpottaa nimikkeiden lajittelemista ja etsimistä.</span><span class="sxs-lookup"><span data-stu-id="c7e87-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="c7e87-105">Voit etsiä nimikkeitä ominaisuuksien mukaan, kun määrität nimikkeille ja nimikeluokille nimikkeen määritteet.</span><span class="sxs-lookup"><span data-stu-id="c7e87-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="c7e87-106">Lisätietoja on kohdassa [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="c7e87-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a><span data-ttu-id="c7e87-107">Nimikeluokan luominen</span><span class="sxs-lookup"><span data-stu-id="c7e87-107">To create an item category</span></span>
1. <span data-ttu-id="c7e87-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeiden luokat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c7e87-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="c7e87-109">Valitse **Nimikekategoriat**-sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="c7e87-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="c7e87-110">Täytä tarvittaessa **Nimikeluokan kortti** -sivun **Yleinen**-pikavälilehden kentät.</span><span class="sxs-lookup"><span data-stu-id="c7e87-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="c7e87-111">Määritä **Määritteet**-pikavälilehdessä kaikki nimikeluokan nimikkeen määritteet.</span><span class="sxs-lookup"><span data-stu-id="c7e87-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="c7e87-112">Lisätietoja on kohdassa [Nimikkeen määritteiden määrittäminen nimikkeen luokkiin](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="c7e87-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
> <span data-ttu-id="c7e87-113">Jos nimikeluokalla on Pääluokka-kentässä ilmaistu **Päänimike**-luokka, kaikki tähän päänimikeluokkaan määritetyt nimikkeen määritteet täytetään **Määritteet**-pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="c7e87-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
> <span data-ttu-id="c7e87-114">Nimikeluokkaan määritettyjä nimikkeen määritteitä käytetään automaattisesti nimikkeessä, johon nimikeluokka on määritetty.</span><span class="sxs-lookup"><span data-stu-id="c7e87-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

<span data-ttu-id="c7e87-115">Jos muutat mieltäsi nimikeluokasta, voit poistaa sen.</span><span class="sxs-lookup"><span data-stu-id="c7e87-115">If you change your mind about an item category, you can delete it.</span></span> <span data-ttu-id="c7e87-116">Jos se kuitenkin on jo määritetty jollekin nimikkeelle, kyseinen tehtävä on poistettava, ennen kuin nimikeluokka voidaan poistaa.</span><span class="sxs-lookup"><span data-stu-id="c7e87-116">However, if it has already been assigned to an item, you must remove that assignment before you can delete the item category.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="c7e87-117">Nimikeluokan määrittäminen nimikkeeseen</span><span class="sxs-lookup"><span data-stu-id="c7e87-117">To assign an item category to an item</span></span>

1. <span data-ttu-id="c7e87-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c7e87-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c7e87-119">Avaa sen nimikkeen kortti, jonka haluat määrittää nimikeluokkaan.</span><span class="sxs-lookup"><span data-stu-id="c7e87-119">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="c7e87-120">Valitse **Nimikeluokan koodi** -kentän valintapainike ja valitse sitten aiemmin määritetty nimikeluokka.</span><span class="sxs-lookup"><span data-stu-id="c7e87-120">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="c7e87-121">Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikeluokan kohdassa [Nimikeluokan luominen](inventory-how-categorize-items.md#to-create-an-item-category) esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="c7e87-121">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="categories-attributes-and-variants"></a><span data-ttu-id="c7e87-122">Luokat, määritteet ja variantit</span><span class="sxs-lookup"><span data-stu-id="c7e87-122">Categories, attributes, and variants</span></span>

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><span data-ttu-id="c7e87-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c7e87-123">See Also</span></span>

[<span data-ttu-id="c7e87-124">Nimikkeen määritteiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="c7e87-124">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="c7e87-125">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="c7e87-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c7e87-126">Varasto</span><span class="sxs-lookup"><span data-stu-id="c7e87-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c7e87-127">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c7e87-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]