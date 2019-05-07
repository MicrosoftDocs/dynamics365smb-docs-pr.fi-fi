---
title: Nimikkeiden viittausten käyttäminen | Microsoft Docs
description: Jos määrität viittauksen käyttämäsi nimikkeen nimikekuvauksen ja kyseisen nimikkeen toimittajan käyttämän kuvauksen välille, toimittajan nimikekuvaus lisätään automaattiesti toimittajan ostoasiakirjoihin, kun annat arvon **Viitenro** -kentässä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca9f31b737fbd81bd1abba2a942301d0c9c919a6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "927100"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="90310-104">Nimikkeen viittausten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="90310-104">Use Item Cross References</span></span>
<span data-ttu-id="90310-105">Jos määrität viittauksen käyttämäsi nimikkeen nimikekuvauksen ja kyseisen nimikkeen toimittajan käyttämän kuvauksen välille, toimittajan nimikekuvaus lisätään automaattiesti toimittajan ostoasiakirjoihin, kun annat arvon **Viitenro**</span><span class="sxs-lookup"><span data-stu-id="90310-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="90310-106">-kentässä.</span><span class="sxs-lookup"><span data-stu-id="90310-106">field.</span></span> <span data-ttu-id="90310-107">Myyntiasiakirjojen asiakkaan nimikenumeroissa käytetään samoja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="90310-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="90310-108">Seuraavaksi käsitellään nimikkeen viittausten käyttämistä ostojen puolella.</span><span class="sxs-lookup"><span data-stu-id="90310-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="90310-109">Ostojen puolen vaiheet ovat vastaavanlaiset.</span><span class="sxs-lookup"><span data-stu-id="90310-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="90310-110">Nimikkeen viittauksen määrittäminen toimittajan nimikkeen kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="90310-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="90310-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="90310-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="90310-112">Avaa sen nimikkeen kortti, jolle haluat luoda viittauksen toimittajan kyseistä nimikettä koskevaan nimikkeen kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="90310-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="90310-113">Valitse **Ristiviittaukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="90310-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="90310-114">Täytä **Nimikkeen viittaustapahtumat** -sivun uudella rivillä kenttiä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="90310-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="90310-115">.</span><span class="sxs-lookup"><span data-stu-id="90310-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="90310-116">Toimittajan nimikkeen kuvauksen antaminen ostotilauksessa</span><span class="sxs-lookup"><span data-stu-id="90310-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="90310-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="90310-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="90310-118">Luo ostotilaus toimittajalle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="90310-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="90310-119">Luo ostorivi nimikkeelle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="90310-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="90310-120">Valitse **Viittauksen tyypin nro**</span><span class="sxs-lookup"><span data-stu-id="90310-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="90310-121">-kentässä nimikkeen viittaus, jonka loit, ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="90310-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="90310-122">Rivin **Kuvaus**-kentän tiedot on korvattu toimittajan nimikkeen kuvauksella nimikkeen viittaustapauksessa määritetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="90310-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="90310-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="90310-123">See Also</span></span>
[<span data-ttu-id="90310-124">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="90310-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="90310-125">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="90310-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="90310-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90310-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
