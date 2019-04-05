---
title: Nimikkeiden järjestäminen luokkiin| Microsoft Docs
description: Nimikkeiden hakemista ja löytämistä helpottaa, kun nimikkeille määritetään määritteitä ja nimikkeet järjestetään luokkiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: a38b69451e05e2b76f4eaaa06044c8b30214c0f0
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795684"
---
# <a name="categorize-items"></a><span data-ttu-id="0840f-103">Nimikkeiden luokitteleminen</span><span class="sxs-lookup"><span data-stu-id="0840f-103">Categorize Items</span></span>
<span data-ttu-id="0840f-104">Nimikkeet kannattaa järjestää nimikeluokkiin. Niiden avulla voi järjestellä nimikkeitä ja helpottaa nimikkeiden lajittelemista ja etsimistä.</span><span class="sxs-lookup"><span data-stu-id="0840f-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="0840f-105">Voit etsiä nimikkeitä ominaisuuksien mukaan, kun määrität nimikkeille ja nimikeluokille nimikkeen määritteet.</span><span class="sxs-lookup"><span data-stu-id="0840f-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="0840f-106">Lisätietoja on kohdassa [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0840f-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="0840f-107">Nimikeluokan luominen</span><span class="sxs-lookup"><span data-stu-id="0840f-107">To create an item category</span></span>
1. <span data-ttu-id="0840f-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikeluokat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0840f-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="0840f-109">Valitse **Nimikekategoriat**-sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="0840f-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="0840f-110">Täytä tarvittaessa **Nimikeluokan kortti** -sivun **Yleinen**-pikavälilehden kentät.</span><span class="sxs-lookup"><span data-stu-id="0840f-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="0840f-111">Määritä **Määritteet**-pikavälilehdessä kaikki nimikeluokan nimikkeen määritteet.</span><span class="sxs-lookup"><span data-stu-id="0840f-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="0840f-112">Lisätietoja on kohdassa [Nimikkeen määritteiden määrittäminen nimikkeen luokkiin](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="0840f-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
>   <span data-ttu-id="0840f-113">Jos nimikeluokalla on Pääluokka-kentässä ilmaistu **Päänimike**-luokka, kaikki tähän päänimikeluokkaan määritetyt nimikkeen määritteet täytetään **Määritteet**-pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="0840f-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0840f-114">Nimikeluokkaan määritettyjä nimikkeen määritteitä käytetään automaattisesti nimikkeessä, johon nimikeluokka on määritetty.</span><span class="sxs-lookup"><span data-stu-id="0840f-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="0840f-115">Nimikeluokan määrittäminen nimikkeeseen</span><span class="sxs-lookup"><span data-stu-id="0840f-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="0840f-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0840f-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="0840f-117">Avaa sen nimikkeen kortti, jonka haluat määrittää nimikeluokkaan.</span><span class="sxs-lookup"><span data-stu-id="0840f-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="0840f-118">Valitse **Nimikeluokan koodi** -kentän valintapainike ja valitse sitten aiemmin määritetty nimikeluokka.</span><span class="sxs-lookup"><span data-stu-id="0840f-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="0840f-119">Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikeluokan kohdassa [Nimikeluokan luominen](inventory-how-categorize-items.md#to-create-an-item-category) esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="0840f-119">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="see-also"></a><span data-ttu-id="0840f-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0840f-120">See Also</span></span>
[<span data-ttu-id="0840f-121">Nimikkeen määritteiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="0840f-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="0840f-122">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="0840f-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="0840f-123">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="0840f-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0840f-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0840f-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
