---
title: "Tuotantoerän mittayksikön käyttäminen | Microsoft Docs"
description: "Jos nimike varastoidaan yhtä mittayksikköä ja tuotetaan toista mittayksikköä käyttäen, tuotantotilauksen on käytettävä tuotantoerän mittayksikköä komponenttien oikean määrän laskemiseen. Tuotantoerän mittayksikön laskentaa voidaan tarvita esimerkiksi, kun nimike varastoidaan kappaleina mutta tuotetaan tonneina."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1b075d164e18a52fbda56cced8d88fabc77bec3f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-manufacturing-batch-units-of-measure"></a><span data-ttu-id="9d71b-104">Toimintaohje: Tuotantoerän mittayksiköiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="9d71b-104">How to: Work with Manufacturing Batch Units of Measure</span></span>
<span data-ttu-id="9d71b-105">Jos nimike varastoidaan yhtä mittayksikköä ja tuotetaan toista mittayksikköä käyttäen, ohjelma voi laskea komponenttien oikean määrän **Päivitä tuotantotilaus** -eräajon aikana luomalla tuotantoerän mittayksikköä käyttävän tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="9d71b-105">If an item is stocked in one unit of measure but produced in another, a production order is created that uses a manufacturing batch unit of measure to calculate the correct quantity of the components during the **Refresh Production Order** batch job.</span></span> <span data-ttu-id="9d71b-106">Tuotantoerän mittayksikön laskentaa voidaan tarvita esimerkiksi, kun nimike varastoidaan kappaleina mutta tuotetaan tonneina.</span><span class="sxs-lookup"><span data-stu-id="9d71b-106">An example of a manufacturing batch unit of measure calculation is when a manufactured item is stocked in pieces but produced in tons.</span></span>  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a><span data-ttu-id="9d71b-107">Tuotannon tuoterakenteen luominen erän mittayksikköä käyttäen</span><span class="sxs-lookup"><span data-stu-id="9d71b-107">To create a production BOM using a batch unit of measure</span></span>  
1.  <span data-ttu-id="9d71b-108">Tuotantoerän mittayksikkö määritetään vaihtoehtoiseksi mittayksiköksi tuotettavan nimikkeen **Nimikkeen mittayksiköt**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="9d71b-108">The manufacturing batch unit of measure is set up as an alternative unit of measure in the **Item Units of Measure** window on the item to be produced.</span></span> <span data-ttu-id="9d71b-109">Erän mittayksikkö ei korvaa nimikkeen perusmittayksikköä.</span><span class="sxs-lookup"><span data-stu-id="9d71b-109">The batch unit of measure will not replace the base unit of measure on the item.</span></span>  
2.  <span data-ttu-id="9d71b-110">Luo tuotannon tuoterakenne nimikkeelle, johon on määritetty tuotantoerän mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="9d71b-110">Create a production BOM for the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="9d71b-111">Lisätietoja on kohdassa [Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="9d71b-111">For more information, see [How to: Create Production BOMs](production-how-to-create-production-boms.md).</span></span>  
3.  <span data-ttu-id="9d71b-112">Napsauta **Mittayksikön koodi** -kenttää ja valitse tuotantoerän mittayksikön koodi.</span><span class="sxs-lookup"><span data-stu-id="9d71b-112">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure.</span></span>  
4.  <span data-ttu-id="9d71b-113">Lisää tuotannon tuoterakenteen jokaiselle riville **Määrä per** -kenttään tämän komponenttinimikkeen määrä, joka tarvitaan tämän erän mittayksikön luomiseen.</span><span class="sxs-lookup"><span data-stu-id="9d71b-113">For each production BOM line, in the **Quantity Per** field, enter the quantity of this component item that is required to create this batch unit of measure.</span></span>  
5.  <span data-ttu-id="9d71b-114">Avaa liittyvän nimikkeen **Nimikkeen kortti**.</span><span class="sxs-lookup"><span data-stu-id="9d71b-114">Open the **Item Card** for the related item.</span></span>  

    <span data-ttu-id="9d71b-115">Valitse **Täydennys**-pikavälilehden **Tuotannon tuoterakenteen nro** -kentässä edellä luotu tuotannon tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="9d71b-115">On the **Replenishment** FastTab, in the **Production BOM No.** field, select the production BOM created above.</span></span>  
6.  <span data-ttu-id="9d71b-116">Luo tuotantotilauksen otsikko käyttäen nimikettä, johon on määritetty tuotantoerän mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="9d71b-116">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="9d71b-117">Lisätietoja on kohdassa [Toimintaohje: Tuotantotilausten luominen](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="9d71b-117">For more information, see [How to: Create Production Orders](production-how-to-create-production-orders.md).</span></span>  
7.  <span data-ttu-id="9d71b-118">Valitse ensin **Päivitä**-toiminto ja sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d71b-118">Choose the **Refresh** action, and then choose  the **OK** button.</span></span>  

<span data-ttu-id="9d71b-119">Voit tarkastella tuloksia valitsemalla ensin **Rivit**-pikavälilehdessä **Rivi**- ja sitten **Komponentit**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="9d71b-119">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="9d71b-120">Ohjelma laskee tuotantoerän mittayksikön perusteella oikean komponenttimäärän, jonka tuotannon tuoterakenne tarvitsee.</span><span class="sxs-lookup"><span data-stu-id="9d71b-120">The program calculates the correct quantity of the components needed to satisfy the production BOM based on the manufacturing batch unit of measure.</span></span>  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a><span data-ttu-id="9d71b-121">Tuotantotilauksen tuotantoerän mittayksikön laskeminen</span><span class="sxs-lookup"><span data-stu-id="9d71b-121">To calculate a manufacturing batch unit of measure on a production order</span></span>  
1.  <span data-ttu-id="9d71b-122">Luo tuotantotilauksen otsikko käyttäen nimikettä, johon on määritetty tuotantoerän mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="9d71b-122">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span>  
2.  <span data-ttu-id="9d71b-123">Kirjoita otsikossa käytetty nimikkeen numero tuotantotilauksen rivin **Nimikkeen nro** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9d71b-123">In the **Item No.** field in the Production Order line, type the same item number used in the header.</span></span>  
3.  <span data-ttu-id="9d71b-124">Lisää otsikossa käytetty määrä **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9d71b-124">In the **Quantity** field, enter the same quantity used in the header.</span></span>  
4.  <span data-ttu-id="9d71b-125">Napsauta **Mittayksikön koodi** -kenttää ja valitse tuotantoerän mittayksikön koodi.</span><span class="sxs-lookup"><span data-stu-id="9d71b-125">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure code.</span></span>  
5.  <span data-ttu-id="9d71b-126">Valitse **Päivitä**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="9d71b-126">Choose the **Refresh** action.</span></span>
6.  <span data-ttu-id="9d71b-127">Poista **Laske**-pikavälilehden **Rivit**-valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="9d71b-127">On the **Calculate** FastTab, clear the **Lines** check box.</span></span>  
7.  <span data-ttu-id="9d71b-128">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="9d71b-128">Choose the **OK** button.</span></span>  
8.  <span data-ttu-id="9d71b-129">Voit tarkastella tuloksia valitsemalla ensin **Rivit**-pikavälilehdessä **Rivi**- ja sitten **Komponentit**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="9d71b-129">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="9d71b-130">Ohjelma laskee tuotantoerän mittayksikön perusteella oikean komponenttimäärän, jonka tuotannon tuoterakenne tarvitsee.</span><span class="sxs-lookup"><span data-stu-id="9d71b-130">The correct quantity of the components needed to satisfy the production BOM is calculated based on the manufacturing batch unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9d71b-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9d71b-131">See Also</span></span>  
[<span data-ttu-id="9d71b-132">Toimintaohje: Uusien reititysten luominen</span><span class="sxs-lookup"><span data-stu-id="9d71b-132">How to: Create Routings</span></span>](production-how-to-create-routings.md)  
<span data-ttu-id="9d71b-133">[Toimintaohje: Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)   </span><span class="sxs-lookup"><span data-stu-id="9d71b-133">[How to: Create Production BOMs](production-how-to-create-production-boms.md)   </span></span>  
[<span data-ttu-id="9d71b-134">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9d71b-134">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="9d71b-135">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="9d71b-135">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="9d71b-136">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="9d71b-136">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="9d71b-137">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="9d71b-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9d71b-138">Osto</span><span class="sxs-lookup"><span data-stu-id="9d71b-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9d71b-139">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9d71b-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

