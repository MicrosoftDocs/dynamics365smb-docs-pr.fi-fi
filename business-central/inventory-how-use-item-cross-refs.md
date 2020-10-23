---
title: Nimikkeiden viittausten käyttäminen | Microsoft Docs
description: Määritä viittaukset niiden kuvauksien välille, joita sinä ja toimittajasi käytätte nimikkeelle, jotta voit lisätä toimittajan nimikekuvauksen ostoasiakirjoihin.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 056897c799dd12755432637690446a0797c9f18c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919436"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="5dddc-103">Nimikkeen viittausten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="5dddc-103">Use Item Cross References</span></span>
<span data-ttu-id="5dddc-104">Jos määrität viittauksen käyttämäsi nimikkeen nimikekuvauksen ja kyseisen nimikkeen toimittajan käyttämän kuvauksen välille, toimittajan nimikekuvaus lisätään automaattiesti toimittajan ostoasiakirjoihin, kun annat arvon **Viitenro**</span><span class="sxs-lookup"><span data-stu-id="5dddc-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="5dddc-105">-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5dddc-105">field.</span></span> <span data-ttu-id="5dddc-106">Myyntiasiakirjojen asiakkaan nimikenumeroissa käytetään samoja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="5dddc-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="5dddc-107">Seuraavaksi käsitellään nimikkeen viittausten käyttämistä ostojen puolella.</span><span class="sxs-lookup"><span data-stu-id="5dddc-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="5dddc-108">Ostojen puolen vaiheet ovat vastaavanlaiset.</span><span class="sxs-lookup"><span data-stu-id="5dddc-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="5dddc-109">Yhä yleisempää on, että tuotetunnisteet, kuten GTIN- tai GUID-tunnukset, sisältävät vähintään 30 merkkiä, mikä on enemmän kuin nykyinen ominaisuus, jota kohteen ristiviittaukset pystyvät käsittelemään.</span><span class="sxs-lookup"><span data-stu-id="5dddc-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="5dddc-110">Jos tarvitset viittauksia, joissa on enemmän kuin 30 merkkiä, järjestelmänvalvoja voi ottaa käyttöön **Kirjoita pidempiä viitteitä** -ominaisuuden [Ominaisuuksien hallinta](https://businesscentral.dynamics.com/?page=xzy) -sivulla (linkki edellyttää, että sinulla on [!INCLUDE[d365fin](includes/d365fin_md.md)] -vuokraaja).</span><span class="sxs-lookup"><span data-stu-id="5dddc-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=xzy) page (link requires that you have a [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant).</span></span> <span data-ttu-id="5dddc-111">Viittausten käyttö ei muutu, mutta sivujen ja painikkeiden kaltaisten asioiden nimet muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="5dddc-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="5dddc-112">Esimerkiksi **Nimikkeen ristiviittaustapahtumat** -sivulta tulee **Nimikkeen viitetapahtumat** -sivu.</span><span class="sxs-lookup"><span data-stu-id="5dddc-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="5dddc-113">Nimikkeen viittauksen määrittäminen toimittajan nimikkeen kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="5dddc-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="5dddc-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5dddc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="5dddc-115">Avaa sen nimikkeen kortti, jolle haluat luoda viittauksen toimittajan kyseistä nimikettä koskevaan nimikkeen kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="5dddc-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="5dddc-116">Valitse **Ristiviittaukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="5dddc-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="5dddc-117">Jos **Ristiviittaukset**-toimintoa ei löydy, valitse lisäasetusten näyttäminen ja etsi se sitten kohdassa **Liittyvät** > **Nimike**.</span><span class="sxs-lookup"><span data-stu-id="5dddc-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="5dddc-118">Täytä **Nimikkeen viittaustapahtumat** -sivun uudella rivillä kenttiä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="5dddc-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="5dddc-119">.</span><span class="sxs-lookup"><span data-stu-id="5dddc-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="5dddc-120">Toimittajan nimikkeen kuvauksen antaminen ostotilauksessa</span><span class="sxs-lookup"><span data-stu-id="5dddc-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="5dddc-121">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5dddc-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5dddc-122">Luo ostotilaus toimittajalle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="5dddc-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="5dddc-123">Luo ostorivi nimikkeelle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="5dddc-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="5dddc-124">Valitse **Viittauksen tyypin nro**</span><span class="sxs-lookup"><span data-stu-id="5dddc-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="5dddc-125">-kentässä nimikkeen viittaus, jonka loit, ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="5dddc-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="5dddc-126">Rivin **Kuvaus**-kentän tiedot on korvattu toimittajan nimikkeen kuvauksella nimikkeen viittaustapauksessa määritetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="5dddc-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="5dddc-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5dddc-127">See Also</span></span>
[<span data-ttu-id="5dddc-128">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="5dddc-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="5dddc-129">Varasto</span><span class="sxs-lookup"><span data-stu-id="5dddc-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5dddc-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5dddc-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
