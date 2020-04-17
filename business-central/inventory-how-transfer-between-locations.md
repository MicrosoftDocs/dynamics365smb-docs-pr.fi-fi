---
title: Nimikkeiden siirtäminen varastosijaintien välillä| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten varastonimikkeitä siirretään varastosta toiseen joko uudelleenluokituspäiväkirjan tai siirtotilausten avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 04/01/2020
ms.author: SorenGP
ms.openlocfilehash: c7d383fdaf75857013651944207616bdc7208e6d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181962"
---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="487c0-103">Varastonimikkeiden siirtäminen sijaintien välillä</span><span class="sxs-lookup"><span data-stu-id="487c0-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="487c0-104">Varastonimikkeitä siirretään sijaintien välillä luomalla siirtotilauksia.</span><span class="sxs-lookup"><span data-stu-id="487c0-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="487c0-105">Vaihtoehtoisesti voit käyttää uudelleenluokituspäiväkirjaa.</span><span class="sxs-lookup"><span data-stu-id="487c0-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="487c0-106">Siirtotilauksissa lähtevä siirto toimitetaan yhdestä sijainnista vastaanotettavaksi toisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="487c0-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="487c0-107">Tämä mahdollistaa liittyvien varastointiaktiviteettien hallinnan ja tarjoaa suuremman varmuuden siitä, että varastosaldot päivitetään oikein.</span><span class="sxs-lookup"><span data-stu-id="487c0-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="487c0-108">Uudelleenluokituspäiväkirjaan voit yksinkertaisesti täyttää **Sijaintikoodi**- ja **Uusi sijaintikoodi** -kentät.</span><span class="sxs-lookup"><span data-stu-id="487c0-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="487c0-109">Kun teet kirjauksen päiväkirjaan, nimiketapahtumat oikaistaan kyseisissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="487c0-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="487c0-110">Varastotoimintoja ei hallita tällä menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="487c0-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="487c0-111">Jos varastoon on kirjattu nimikkeitä ilman sijaintikoodia esimerkiksi silloin, kun käytössä oli vain yksi varasto, et voi siirtää kyseisiä nimikkeitä siirtotilauksilla.</span><span class="sxs-lookup"><span data-stu-id="487c0-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="487c0-112">Sen sijaan sinun on käytettävä uudelleenluokittelupäiväkirjaa ja luokiteltava nimikkeet uudelleen tyhjästä sijaintikoodista todelliseen sijaintikoodiin.</span><span class="sxs-lookup"><span data-stu-id="487c0-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="487c0-113">Lisätietoja on kohdan [Nimikkeiden siirtäminen uudelleenluokituspäiväkirjan avulla](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal) vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="487c0-113">For more information, see step 3 in [To transfer items with the item reclassification journal](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span></span>

<span data-ttu-id="487c0-114">Sijainnit ja siirtoreitit on määritettävä, jotta nimikkeitä voi siirtää.</span><span class="sxs-lookup"><span data-stu-id="487c0-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="487c0-115">Lisätietoja on kohdassa [Sijaintien määrittäminen](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="487c0-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="487c0-116">Nimikkeiden siirtäminen siirtotilauksella</span><span class="sxs-lookup"><span data-stu-id="487c0-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="487c0-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtotilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="487c0-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="487c0-118">Täytä tarvittavat kentät **Siirtotilaus**-sivun otsikossa.</span><span class="sxs-lookup"><span data-stu-id="487c0-118">On the header of the **Transfer Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="487c0-119">Jos olet täyttänyt **Siirtoreitin määritykset** -sivun **Kuljetuksessa-koodi**-, **Kuljetusliikkeen koodi**- ja **Kuljetusliikkeen palvelu** -kentät siirtoreitin määrityksen yhteydessä, ohjelma täyttää siirtotilauksen vastaavat kentät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="487c0-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields on the **Trans. Route Spec.** page when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="487c0-120">Kun **Kuljetusliikkeen palvelu** -kenttä täytetään, kohteeseen-sijainnin vastaanottopäivämäärä lasketaan lisäämällä kuljetusliikkeen palvelun toimitusajan Kohteesta-pikavälilehden lähetyksen päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="487c0-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

3. <span data-ttu-id="487c0-121">Täytä rivit joka antamalla ne manuaalisesti tai valitsemalla jonkin seuraavista vaihtoehdoista **Funktiot**-toiminnossa:</span><span class="sxs-lookup"><span data-stu-id="487c0-121">To fill in the lines, either enter them manually or choose one of the following options on the under the **Functions** action:</span></span>
    - <span data-ttu-id="487c0-122">Valitse **Hae var.paikan sisältö** -toiminnolla aiemmin luotuja nimikkeita tietystä sijainnin varastopaikasta.</span><span class="sxs-lookup"><span data-stu-id="487c0-122">Choose the **Get Bin Content** action to select existing items from a specific bin at the location.</span></span>
    - <span data-ttu-id="487c0-123">Valitse **Hae vastaanottorivit** -toiminnolla nimikkeet, jotka ovat juuri saapuneet kohteesta-sijainnista.</span><span class="sxs-lookup"><span data-stu-id="487c0-123">Choose the **Get Receipt Lines** to select items that have just arrived at the transfer-from location.</span></span>   

    <span data-ttu-id="487c0-124">Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="487c0-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
4. <span data-ttu-id="487c0-125">Valita ensin **Kirjaa**-toiminto, sitten **Toimitus**-asetus ja lopuksi **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="487c0-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="487c0-126">Nimikkeet ovat nyt matkalla valittujen sijaintien välillä valitun siirtoreitin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="487c0-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="487c0-127">Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden vastaanottamiseen.</span><span class="sxs-lookup"><span data-stu-id="487c0-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span> <span data-ttu-id="487c0-128">Siirtotilausrivit ovat samat kuin toimituksen aikana eikä niitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="487c0-128">The transfer order lines are the same as when shipped and cannot be edited.</span></span>
5. <span data-ttu-id="487c0-129">Valita ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-asetus ja lopuksi **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="487c0-129">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="487c0-130">Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan avulla</span><span class="sxs-lookup"><span data-stu-id="487c0-130">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="487c0-131">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="487c0-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="487c0-132">Täytä tarvittavat kentät **Nimik. uud.luok.pvk** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="487c0-132">On the **Item Reclass. Journal** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="487c0-133">Anna **Sijaintikoodi**-kentässä sijainti, jossa nimikkeet ovat varastoituna.</span><span class="sxs-lookup"><span data-stu-id="487c0-133">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="487c0-134">Jos siirrettävillä nimikkeillä ei ole sijainkoodia, jätä **Sijaintikoodi**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="487c0-134">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="487c0-135">Anna **Uusi sijaintikoodi** -kenttään sijainti, johon haluat siirtää nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="487c0-135">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="487c0-136">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="487c0-136">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="487c0-137">Katso myös</span><span class="sxs-lookup"><span data-stu-id="487c0-137">See Also</span></span>
[<span data-ttu-id="487c0-138">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="487c0-138">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="487c0-139">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="487c0-139">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="487c0-140">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="487c0-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="487c0-141">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="487c0-141">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="487c0-142">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="487c0-142">General Business Functionality</span></span>](ui-across-business-areas.md)
