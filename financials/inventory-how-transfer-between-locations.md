---
title: "Nimikkeiden siirtäminen varastosijaintien välillä| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten varastonimikkeitä siirretään varastosta toiseen joko uudelleenluokituspäiväkirjan tai siirtotilausten avulla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: f13da8ac565e0af7f4ab612ebd23c9cee158dbb9
ms.contentlocale: fi-fi
ms.lasthandoff: 04/16/2018

---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="e7343-103">Varastonimikkeiden siirtäminen sijaintien välillä</span><span class="sxs-lookup"><span data-stu-id="e7343-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="e7343-104">Varastonimikkeitä siirretään sijaintien välillä luomalla siirtotilauksia.</span><span class="sxs-lookup"><span data-stu-id="e7343-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="e7343-105">Vaihtoehtoisesti voit käyttää uudelleenluokituspäiväkirjaa.</span><span class="sxs-lookup"><span data-stu-id="e7343-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="e7343-106">Siirtotilauksissa lähtevä siirto toimitetaan yhdestä sijainnista vastaanotettavaksi toisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="e7343-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="e7343-107">Tämä mahdollistaa liittyvien varastointiaktiviteettien hallinnan ja tarjoaa suuremman varmuuden siitä, että varastosaldot päivitetään oikein.</span><span class="sxs-lookup"><span data-stu-id="e7343-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="e7343-108">Uudelleenluokituspäiväkirjaan voit yksinkertaisesti täyttää **Sijaintikoodi**- ja **Uusi sijaintikoodi** -kentät.</span><span class="sxs-lookup"><span data-stu-id="e7343-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="e7343-109">Kun teet kirjauksen päiväkirjaan, nimiketapahtumat oikaistaan kyseisissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="e7343-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="e7343-110">Varastotoimintoja ei hallita tällä menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="e7343-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e7343-111">Jos varastoon on kirjattu nimikkeitä ilman sijaintikoodia esimerkiksi silloin, kun käytössä oli vain yksi varasto, et voi siirtää kyseisiä nimikkeitä siirtotilauksilla.</span><span class="sxs-lookup"><span data-stu-id="e7343-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="e7343-112">Sen sijaan sinun on käytettävä uudelleenluokittelupäiväkirjaa ja luokiteltava nimikkeet uudelleen tyhjästä sijaintikoodista todelliseen sijaintikoodiin.</span><span class="sxs-lookup"><span data-stu-id="e7343-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="e7343-113">Lisätietoja on Nimikkeiden siirtäminen uudelleenluokituspäiväkirjan avulla -kohdan vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="e7343-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="e7343-114">Sijainnit ja siirtoreitit on määritettävä, jotta nimikkeitä voi siirtää.</span><span class="sxs-lookup"><span data-stu-id="e7343-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="e7343-115">Lisätietoja on kohdassa [Sijaintien määrittäminen](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="e7343-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="e7343-116">Nimikkeiden siirtäminen siirtotilauksella</span><span class="sxs-lookup"><span data-stu-id="e7343-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="e7343-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Siirtotilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e7343-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="e7343-118">Täytä **Siirtotilaus**-ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="e7343-118">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
   >   <span data-ttu-id="e7343-119">Jos olet täyttänyt **Siirtoreitin määritykset** -ikkunan **Kuljetuksessa-koodi**-, **Kuljetusliikkeen koodi**- ja **Kuljetusliikkeen palvelu** -kentät siirtoreitin määrityksen yhteydessä, ohjelma täyttää siirtotilauksen vastaavat kentät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e7343-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="e7343-120">Kun **Kuljetusliikkeen palvelu** -kenttä täytetään, kohteeseen-sijainnin vastaanottopäivämäärä lasketaan lisäämällä kuljetusliikkeen palvelun toimitusajan Kohteesta-pikavälilehden lähetyksen päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="e7343-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="e7343-121">Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="e7343-121">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="e7343-122">Valita ensin **Kirjaa**-toiminto, sitten **Toimitus**-asetus ja lopuksi **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="e7343-122">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="e7343-123">Nimikkeet ovat nyt matkalla valittujen sijaintien välillä valitun siirtoreitin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e7343-123">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="e7343-124">Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden vastaanottamiseen.</span><span class="sxs-lookup"><span data-stu-id="e7343-124">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="e7343-125">Valita ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-asetus ja lopuksi **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="e7343-125">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="e7343-126">Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan avulla</span><span class="sxs-lookup"><span data-stu-id="e7343-126">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="e7343-127">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e7343-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e7343-128">Täytä **Nimik. uud.luok.pvk** -ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="e7343-128">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e7343-129">Anna **Sijaintikoodi**-kentässä sijainti, jossa nimikkeet ovat varastoituna.</span><span class="sxs-lookup"><span data-stu-id="e7343-129">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
   >   <span data-ttu-id="e7343-130">Jos siirrettävillä nimikkeillä ei ole sijainkoodia, jätä **Sijaintikoodi**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="e7343-130">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="e7343-131">Anna **Uusi sijaintikoodi** -kenttään sijainti, johon haluat siirtää nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="e7343-131">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="e7343-132">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e7343-132">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7343-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e7343-133">See Also</span></span>
[<span data-ttu-id="e7343-134">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="e7343-134">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e7343-135">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e7343-135">Set Up Locations</span></span>](inventory-how-setup-locations.md)  

<span data-ttu-id="e7343-136">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e7343-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="e7343-137">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="e7343-137">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="e7343-138">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="e7343-138">General Business Functionality</span></span>](ui-across-business-areas.md)

