---
title: Komponenttien hallinta tuoterakenteiden avulla| Microsoft Docs
description: "Kokoonpanon tuoterakenne luodaan määrittämään komponentit tai resurssit, joista koostetaan nimike, johon kokoonpanon tuoterakenne viittaa. Voit myös tarkastella kokoonpanonimikkeen komponentteja."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="b63e8-103">Toimintaohje: Tuoterakenteen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="b63e8-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="b63e8-104">[!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyinen versio sisältää vain kokoonpanon hallintaominaisuuden ensimmäisen osan.</span><span class="sxs-lookup"><span data-stu-id="b63e8-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="b63e8-105">Voit luoda nyt vain kokoonpanon tuoterakenteita ja käsitellä sitten liittyviä päänimikkeitä tavallisina varastonimikkeinä.</span><span class="sxs-lookup"><span data-stu-id="b63e8-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="b63e8-106">Tulevan päivityksen jälkeen voit hallita nimikkeiden kokoamista osista joko kokoonpano varastoon tai kokoonpano tilauksiin työkuluissa. Voit myös myydä osia paketteina.</span><span class="sxs-lookup"><span data-stu-id="b63e8-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="b63e8-107">Voit käyttää tuoterakenteita jäsentämään päänimikkeitä, joita myydään päänimikkeen osista koostuvina paketteina tai jotka kootaan tilausta tai varastointia varten.</span><span class="sxs-lookup"><span data-stu-id="b63e8-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="b63e8-108">[!INCLUDE[d365fin](includes/d365fin_md.md)]issa tuoterakennetta kutsutaan kokoonpanon tuoterakenteeksi.</span><span class="sxs-lookup"><span data-stu-id="b63e8-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="b63e8-109">Kokoonpanon tuoterakenteet määrittävät, mitkä osat sisältyvät päänimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="b63e8-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="b63e8-110">Tässä dokumentaatiossa päänimikettä kutsutaan kokoonpanonimikkeeksi.</span><span class="sxs-lookup"><span data-stu-id="b63e8-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="b63e8-111">Kokoonpanon tuoterakenteet sisältävät yleensä nimikkeitä, mutta ne voivat sisältää myös resursseja, joita tarvitaan niiden kokoamiseen.</span><span class="sxs-lookup"><span data-stu-id="b63e8-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="b63e8-112">Kokoonpanon tuoterakenteessa voi olla useita tasoja. Toisin sanoen kokoonpanon tuoterakenteen komponentti voi olla itsessään kokoonpanonimike.</span><span class="sxs-lookup"><span data-stu-id="b63e8-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="b63e8-113">Siinä tapauksessa kokoonpanon tuoterakennerivillä olevassa **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b63e8-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="b63e8-114">Erikoisvaatimukset koskevat kokoonpanon tuoterakenteiden nimikkeiden saatavuutta.</span><span class="sxs-lookup"><span data-stu-id="b63e8-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="b63e8-115">Lisätietoja on ohjeaiheen [Toimintaohje: Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md) kohdassa Nimikkeen saatavuuden tarkastelu sen mukaan, miten sitä käytetään kokoonpanon tuoterakenteessa.</span><span class="sxs-lookup"><span data-stu-id="b63e8-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="b63e8-116">Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**.</span><span class="sxs-lookup"><span data-stu-id="b63e8-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="b63e8-117">Lisätietoja on kohdassa [Financials-kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="b63e8-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="b63e8-118">Luo kokoonpanon tuoterakenne</span><span class="sxs-lookup"><span data-stu-id="b63e8-118">To create an assembly BOM</span></span>
<span data-ttu-id="b63e8-119">Kokoonpanon tuoterakenne on luotava, jos haluat määrittää päänimikkeen, joka koostuu muista nimikkeistä ja mahdollisesti resursseista, joita tarvitaan päänimikkeen kokoamiseen.</span><span class="sxs-lookup"><span data-stu-id="b63e8-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="b63e8-120">Kokoonpanon tuoterakenteen luomisessa on kaksi osaa:</span><span class="sxs-lookup"><span data-stu-id="b63e8-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="b63e8-121">uuden nimikkeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b63e8-121">Setting up a new item</span></span>
- <span data-ttu-id="b63e8-122">kokoonpanonimikkeen tuoterakenteen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="b63e8-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="b63e8-123">Määritä uusi nimike.</span><span class="sxs-lookup"><span data-stu-id="b63e8-123">Set up a new item.</span></span> <span data-ttu-id="b63e8-124">Lisätietoja on kohdassa [Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="b63e8-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="b63e8-125">Jatka antamalla kokoonpanon tuoterakenteen osat tai resurssit.</span><span class="sxs-lookup"><span data-stu-id="b63e8-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="b63e8-126">Valitse kokoonpanonimikkeen **Nimikekortti**-ikkunassa ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b63e8-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="b63e8-127">Täytä **Kokoonpanon tuoterakenne** -ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="b63e8-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="b63e8-128">Kokoonpanonimikkeen osien näyttäminen tuoterakenteen perusteella sisennettyinä</span><span class="sxs-lookup"><span data-stu-id="b63e8-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="b63e8-129">Voit avata **Kokoonpanon tuoterakenne** -ikkunassa erillisen ikkunan, joka näyttää osat ja resursseja sisennettynä kokoonpanonimikkeen alle niiden tuoterakenteen mukaisen sijainnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="b63e8-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="b63e8-130">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b63e8-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b63e8-131">Avaa kokoonpanonimikkeen kortti.</span><span class="sxs-lookup"><span data-stu-id="b63e8-131">Open the card for an assembly item.</span></span> <span data-ttu-id="b63e8-132">(**Nimikkeet**-ikkunan **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)</span><span class="sxs-lookup"><span data-stu-id="b63e8-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="b63e8-133">Valitse **Nimikekortti**-ikkunassa ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b63e8-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="b63e8-134">Valitse **Kokoonpanon tuoterakenne** -ikkunassa **Näytä tuoterakenne** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b63e8-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="b63e8-135">Kokoonpanonimikkeiden ostaminen, myynti tai siirtäminen</span><span class="sxs-lookup"><span data-stu-id="b63e8-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="b63e8-136">Koska [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyisessä versiossa kokoonpanon tuoterakenne voidaan määrittää ja liittää vain nimikkeille, voit käsitellä asiakirjarivien kokoonpanonimikkeitä vain tavallisina nimikkeinä.</span><span class="sxs-lookup"><span data-stu-id="b63e8-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="b63e8-137">**Varoitus**: Tuoterakenneosien varastomäärää ei muuteta, jos teet niin.</span><span class="sxs-lookup"><span data-stu-id="b63e8-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="b63e8-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b63e8-138">See Also</span></span>
[<span data-ttu-id="b63e8-139">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="b63e8-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="b63e8-140">[Toimintaohje: Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="b63e8-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="b63e8-141">Varasto</span><span class="sxs-lookup"><span data-stu-id="b63e8-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b63e8-142">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b63e8-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

