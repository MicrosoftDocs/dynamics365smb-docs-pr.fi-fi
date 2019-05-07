---
title: Kysynnän ja tarjonnan välisten suhteiden seuraaminen | Microsoft Docs
description: Voit seurata tilausverkon kysyntä- tai tarjousasiakirjojen avulla tilauskysyntää (seurattu määrä), ennustetta, myyntipuitetilausta tai suunnitteluparametria (ei-seurattu määrä), joka on kiinnittänyt huomion kyseiseen suunnitteluriviin.
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
ms.openlocfilehash: beb438be379cfc6e3f239ebb0ae270a2e957651c
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2019
ms.locfileid: "938488"
---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="b63e0-103">Kysynnän ja tarjonnan välisten suhteiden seuraaminen</span><span class="sxs-lookup"><span data-stu-id="b63e0-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="b63e0-104">Voit seurata tilausverkon kysyntä- tai tarjousasiakirjojen avulla tilauskysyntää (seurattu määrä), ennustetta, myyntipuitetilausta tai suunnitteluparametria (ei-seurattu määrä), joka on kiinnittänyt huomion kyseiseen suunnitteluriviin.</span><span class="sxs-lookup"><span data-stu-id="b63e0-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="b63e0-105">Suunnittelutyökirjasta saa myös suunnittelua tukevia tietoja muista kuin tilattavista yksiköistä, mikä auttaa suunnittelijaa saamaa mahdollisimman hyvän toimitussuunnitelman.</span><span class="sxs-lookup"><span data-stu-id="b63e0-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="b63e0-106">Lisätietoja on kohdassa [Ei-seuratut suunnitteluelementit.](production-how-track-demand-supply.md#untracked-planning-elements).</span><span class="sxs-lookup"><span data-stu-id="b63e0-106">For more information, see [Untracked Planning Elements](production-how-track-demand-supply.md#untracked-planning-elements).</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="b63e0-107">Linkitettyjen kohteiden seuraaminen</span><span class="sxs-lookup"><span data-stu-id="b63e0-107">To track linked items</span></span>
<span data-ttu-id="b63e0-108">Tilauksen seurannan avulla voi nähdä, miten myyntitilaukset, tuotantotilaukset ja ostotilaukset liittyvät tuotantotilaukseen suunnittelu- ja varausjärjestelmien kautta.</span><span class="sxs-lookup"><span data-stu-id="b63e0-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="b63e0-109">Seuraavaksi käsitellään linkitettyjen nimikkeiden seuraamista sitovasti suunnitellussa tuotantotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="b63e0-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="b63e0-110">Nämä vaiheet ovat samankaltaiset kaikilla muilla tilaustyypeillä ja suunnittelutyökirjan riveillä.</span><span class="sxs-lookup"><span data-stu-id="b63e0-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="b63e0-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sitovasti suun. tuotantotil.** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b63e0-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="b63e0-112">Avaa asianmukainen sitovasti suunniteltu tuotantotilaus luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b63e0-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="b63e0-113">Valitse **Rivit**-pikavälilehdessä ensin **Toiminnot**-toiminto ja sitten **Tilauksen seuranta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b63e0-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="b63e0-114">Nykyiseen tuotantotilauksen riviin liittyvät asiakirjat näkyvät **Tilauksen seuranta** -ikkunan riveillä.</span><span class="sxs-lookup"><span data-stu-id="b63e0-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="b63e0-115">Ei-seuratut suunnitteluelementit</span><span class="sxs-lookup"><span data-stu-id="b63e0-115">Untracked Planning Elements</span></span>
<span data-ttu-id="b63e0-116">**Ei-seuratut suunnitteluelementit** -sivu avautuu, kun valitset **Ei-seurattu määrä** -kentän **Tilauksen suunnittelu** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b63e0-116">The **Untracked Planning Elements** page opens when you choose the **Untracked Qty.** field on the **order Planning** page.</span></span> <span data-ttu-id="b63e0-117">Sillä on kaksi tarkoitusta:</span><span class="sxs-lookup"><span data-stu-id="b63e0-117">It serves two purposes:</span></span>

1. <span data-ttu-id="b63e0-118">Se sisältää tietoja ei-seuratuista määristä, jotka näytetään, kun käyttäjä etsii ei-seurattuja määriä Tilauksen seuranta -sivun avulla.</span><span class="sxs-lookup"><span data-stu-id="b63e0-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking page to see untracked quantities.</span></span>
2. <span data-ttu-id="b63e0-119">Se sisältää varoitussanomia, jotka näytetään, kun käyttäjä napsauttaa **varoituskuvaketta** **Suunnittelutyökirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b63e0-119">To hold warning messages displayed when the user chooses the **Warning** icon on the **Planning Worksheet** page.</span></span>

<span data-ttu-id="b63e0-120">Sivu sisältää tapahtumia, jotka selittävät ei-seuratun ylijäämämäärän tilauksen seurantaverkossa.</span><span class="sxs-lookup"><span data-stu-id="b63e0-120">The page contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="b63e0-121">Tapahtumat luodaan suunnitteluajon aikana ja ne selvittävät, mistä tilauksen seurantarivien ei-seurattu ylijäämämäärä on peräisin.</span><span class="sxs-lookup"><span data-stu-id="b63e0-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="b63e0-122">Ei-seurattu ylijäämä voi olla peräisin seuraavista kohteista:</span><span class="sxs-lookup"><span data-stu-id="b63e0-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="b63e0-123">Tuotantoennuste</span><span class="sxs-lookup"><span data-stu-id="b63e0-123">Production forecast</span></span>
- <span data-ttu-id="b63e0-124">Puitetilaukset</span><span class="sxs-lookup"><span data-stu-id="b63e0-124">Blanket orders</span></span>
- <span data-ttu-id="b63e0-125">Varmuusvaraston määrä</span><span class="sxs-lookup"><span data-stu-id="b63e0-125">Safety stock quantity</span></span>
- <span data-ttu-id="b63e0-126">Uusintatilauspiste</span><span class="sxs-lookup"><span data-stu-id="b63e0-126">Reorder point</span></span>
- <span data-ttu-id="b63e0-127">Enimmäisvarasto</span><span class="sxs-lookup"><span data-stu-id="b63e0-127">Maximum inventory</span></span>
- <span data-ttu-id="b63e0-128">Uusintatilausmäärä</span><span class="sxs-lookup"><span data-stu-id="b63e0-128">Reorder quantity</span></span>
- <span data-ttu-id="b63e0-129">Enimmäistilausmäärä</span><span class="sxs-lookup"><span data-stu-id="b63e0-129">Maximum order quantity</span></span>
- <span data-ttu-id="b63e0-130">Vähimmäistilausmäärä</span><span class="sxs-lookup"><span data-stu-id="b63e0-130">Minimum order quantity</span></span>
- <span data-ttu-id="b63e0-131">Tilauskerrannainen</span><span class="sxs-lookup"><span data-stu-id="b63e0-131">Order multiple</span></span>
- <span data-ttu-id="b63e0-132">Vaimennin (% eräkoosta).</span><span class="sxs-lookup"><span data-stu-id="b63e0-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="b63e0-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b63e0-133">See Also</span></span>  
<span data-ttu-id="b63e0-134">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b63e0-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="b63e0-135">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b63e0-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b63e0-136">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b63e0-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="b63e0-137">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="b63e0-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b63e0-138">Osto</span><span class="sxs-lookup"><span data-stu-id="b63e0-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="b63e0-139">Rakennetiedot: Varaus, seuranta ja toimenpiteiden viestitys</span><span class="sxs-lookup"><span data-stu-id="b63e0-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="b63e0-140">[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b63e0-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="b63e0-141">Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu</span><span class="sxs-lookup"><span data-stu-id="b63e0-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="b63e0-142">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b63e0-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
