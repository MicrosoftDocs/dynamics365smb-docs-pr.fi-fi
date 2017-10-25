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
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 41804dc183f9fa05ec1599db34c2b4f76a790a72
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-inventory-between-locations"></a><span data-ttu-id="40d1b-103">Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä</span><span class="sxs-lookup"><span data-stu-id="40d1b-103">How to: Transfer Inventory Between Locations</span></span>
<span data-ttu-id="40d1b-104">Varastonimikkeitä siirretään sijaintien välillä luomalla siirtotilauksia.</span><span class="sxs-lookup"><span data-stu-id="40d1b-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="40d1b-105">Vaihtoehtoisesti voit käyttää uudelleenluokituspäiväkirjaa.</span><span class="sxs-lookup"><span data-stu-id="40d1b-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="40d1b-106">Siirtotilauksissa lähtevä siirto toimitetaan yhdestä sijainnista vastaanotettavaksi toisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="40d1b-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="40d1b-107">Tämä mahdollistaa liittyvien varastointiaktiviteettien hallinnan ja tarjoaa suuremman varmuuden siitä, että varastosaldot päivitetään oikein.</span><span class="sxs-lookup"><span data-stu-id="40d1b-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="40d1b-108">Uudelleenluokituspäiväkirjaan voit yksinkertaisesti täyttää **Sijaintikoodi**- ja **Uusi sijaintikoodi** -kentät.</span><span class="sxs-lookup"><span data-stu-id="40d1b-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="40d1b-109">Kun teet kirjauksen päiväkirjaan, nimiketapahtumat oikaistaan kyseisissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="40d1b-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="40d1b-110">Varastotoimintoja ei hallita tällä menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="40d1b-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="40d1b-111">Jos varastoon on kirjattu nimikkeitä ilman sijaintikoodia esimerkiksi silloin, kun käytössä oli vain yksi varasto, et voi siirtää kyseisiä nimikkeitä siirtotilauksilla.</span><span class="sxs-lookup"><span data-stu-id="40d1b-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="40d1b-112">Sen sijaan sinun on käytettävä uudelleenluokittelupäiväkirjaa ja luokiteltava nimikkeet uudelleen tyhjästä sijaintikoodista todelliseen sijaintikoodiin.</span><span class="sxs-lookup"><span data-stu-id="40d1b-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="40d1b-113">Lisätietoja on Nimikkeiden siirtäminen uudelleenluokituspäiväkirjan avulla -kohdan vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="40d1b-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="40d1b-114">Sijainnit ja siirtoreitit on määritettävä, jotta nimikkeitä voi siirtää.</span><span class="sxs-lookup"><span data-stu-id="40d1b-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="40d1b-115">Lisätietoja on kohdassa [Toimintaohje: Sijaintien määrittäminen](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="40d1b-115">For more information, see [How to: Set Up Locations](inventory-how-setup-locations.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="40d1b-116">Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**.</span><span class="sxs-lookup"><span data-stu-id="40d1b-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="40d1b-117">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="40d1b-117">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="40d1b-118">Nimikkeiden siirtäminen siirtotilauksella</span><span class="sxs-lookup"><span data-stu-id="40d1b-118">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="40d1b-119">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Siirtotilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="40d1b-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="40d1b-120">Täytä **Siirtotilaus**-ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="40d1b-120">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="40d1b-121">Jos olet täyttänyt **Siirtoreitin määritykset** -ikkunan **Kuljetuksessa-koodi**-, **Kuljetusliikkeen koodi**- ja **Kuljetusliikkeen palvelu** -kentät siirtoreitin määrityksen yhteydessä, ohjelma täyttää siirtotilauksen vastaavat kentät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="40d1b-121">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="40d1b-122">Kun **Kuljetusliikkeen palvelu** -kenttä täytetään, kohteeseen-sijainnin vastaanottopäivämäärä lasketaan lisäämällä kuljetusliikkeen palvelun toimitusajan Kohteesta-pikavälilehden lähetyksen päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="40d1b-122">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="40d1b-123">Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="40d1b-123">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="40d1b-124">Valita ensin **Kirjaa**-toiminto, sitten **Toimitus**-asetus ja lopuksi **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="40d1b-124">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="40d1b-125">Nimikkeet ovat nyt matkalla valittujen sijaintien välillä valitun siirtoreitin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="40d1b-125">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="40d1b-126">Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden vastaanottamiseen.</span><span class="sxs-lookup"><span data-stu-id="40d1b-126">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="40d1b-127">Valita ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-asetus ja lopuksi **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="40d1b-127">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="40d1b-128">Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan avulla</span><span class="sxs-lookup"><span data-stu-id="40d1b-128">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="40d1b-129">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="40d1b-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="40d1b-130">Täytä **Nimik. uud.luok.pvk** -ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="40d1b-130">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="40d1b-131">Anna **Sijaintikoodi**-kentässä sijainti, jossa nimikkeet ovat varastoituna.</span><span class="sxs-lookup"><span data-stu-id="40d1b-131">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="40d1b-132">Jos siirrettävillä nimikkeillä ei ole sijainkoodia, jätä **Sijaintikoodi**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="40d1b-132">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="40d1b-133">Anna **Uusi sijaintikoodi** -kenttään sijainti, johon haluat siirtää nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="40d1b-133">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="40d1b-134">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="40d1b-134">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="40d1b-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="40d1b-135">See Also</span></span>
[<span data-ttu-id="40d1b-136">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="40d1b-136">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="40d1b-137">Toimintaohje: Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="40d1b-137">How to: Set Up Locations</span></span>](inventory-how-setup-locations.md)  
  
<span data-ttu-id="40d1b-138">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="40d1b-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="40d1b-139">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="40d1b-139">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="40d1b-140">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="40d1b-140">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
