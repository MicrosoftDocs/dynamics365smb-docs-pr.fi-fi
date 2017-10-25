---
title: Tuotantotilauksen otsikoiden luominen | Microsoft Docs
description: "Tuotantotilauksen voi luoda manuaalisesti. Ensimmäinen työvaihe on tuotantotilauksen otsikon luominen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a><span data-ttu-id="df0e5-103">Tuotantotilausten otsikoiden luominen</span><span class="sxs-lookup"><span data-stu-id="df0e5-103">How to: Create Production Order Headers</span></span>
<span data-ttu-id="df0e5-104">Tuotantotilauksen voi luoda manuaalisesti. Ensimmäinen työvaihe on tuotantotilauksen otsikon luominen.</span><span class="sxs-lookup"><span data-stu-id="df0e5-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="df0e5-105">Suunnittelutoiminto luo tuotantotilaukset tavallisesti automaattisesti toteuttamaan tunnetun kysynnän.</span><span class="sxs-lookup"><span data-stu-id="df0e5-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="df0e5-106">Lisätietoja on kohdassa [Suunnittelu](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="df0e5-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="df0e5-107">Seuraavassa toienpiteessä luodaan sitovasti suunniteltu tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="df0e5-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="df0e5-108">Voit luoda myös tuotantotilauksia, joilla on eri tila.</span><span class="sxs-lookup"><span data-stu-id="df0e5-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="df0e5-109">Tuotantotilausten otsikoiden luominen</span><span class="sxs-lookup"><span data-stu-id="df0e5-109">To create a production order header</span></span>  
1.  <span data-ttu-id="df0e5-110">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sitovasti suunn. tuotantotil.** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="df0e5-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="df0e5-111">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="df0e5-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="df0e5-112">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="df0e5-112">In the **No.**</span></span> <span data-ttu-id="df0e5-113">seuraava numero sarjasta.</span><span class="sxs-lookup"><span data-stu-id="df0e5-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="df0e5-114">Valitse **Lähdetyyppi**-kentässä tuotantotilauksen lähde.</span><span class="sxs-lookup"><span data-stu-id="df0e5-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="df0e5-115">Voit valita täällä tuotenimikeperheen tuotannon.</span><span class="sxs-lookup"><span data-stu-id="df0e5-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="df0e5-116">Lisätietoja on kohdassa [Toimintaohje: Tuotantoperheiden käyttäminen](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="df0e5-116">For more information, see [How to: Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="df0e5-117">Valitse **Lähteen nro** -kentässä nimikenumero, tuoteperhe tai myynnin tunnistetiedot, jolle tuotantotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="df0e5-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="df0e5-118">Täytä **Määrä**- ja **Eräpäivä**-kentät määritystesi mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="df0e5-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="df0e5-119">Kun tuotannon vaatimukset, kuten komponentit tai toiminnot, muuttuvat, voit suunnitella tuotantotilauksen nopeasti uudelleen.</span><span class="sxs-lookup"><span data-stu-id="df0e5-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="df0e5-120">Lisätietoja on kohdassa [Toimintaohje: Tuotantotilausten suora päivittäminen tai uudelleensuunnitteleminen](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="df0e5-120">For more information, see [How to: Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="df0e5-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="df0e5-121">See Also</span></span>  
<span data-ttu-id="df0e5-122">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="df0e5-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="df0e5-123">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="df0e5-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="df0e5-124">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="df0e5-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="df0e5-125">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="df0e5-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="df0e5-126">Osto</span><span class="sxs-lookup"><span data-stu-id="df0e5-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="df0e5-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="df0e5-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

