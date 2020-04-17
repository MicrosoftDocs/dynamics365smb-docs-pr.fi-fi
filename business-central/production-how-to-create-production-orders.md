---
title: Tuotantotilauksen otsikoiden luominen | Microsoft Docs
description: Tuotantotilauksen voi luoda manuaalisesti. Ensimmäinen työvaihe on tuotantotilauksen otsikon luominen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3033211d26b89b50fd724ed3398d62dbd5535969
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192049"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="0835b-103">Tuotantotilausten otsikoiden luominen</span><span class="sxs-lookup"><span data-stu-id="0835b-103">Create Production Order Headers</span></span>
<span data-ttu-id="0835b-104">Tuotantotilauksen voi luoda manuaalisesti. Ensimmäinen työvaihe on tuotantotilauksen otsikon luominen.</span><span class="sxs-lookup"><span data-stu-id="0835b-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="0835b-105">Suunnittelutoiminto luo tuotantotilaukset tavallisesti automaattisesti toteuttamaan tunnetun kysynnän.</span><span class="sxs-lookup"><span data-stu-id="0835b-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="0835b-106">Lisätietoja on kohdassa [Suunnittelu](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="0835b-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="0835b-107">Seuraavassa toienpiteessä luodaan sitovasti suunniteltu tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="0835b-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="0835b-108">Voit luoda myös tuotantotilauksia, joilla on eri tila.</span><span class="sxs-lookup"><span data-stu-id="0835b-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="0835b-109">Tuotantotilausten otsikoiden luominen</span><span class="sxs-lookup"><span data-stu-id="0835b-109">To create a production order header</span></span>  
1.  <span data-ttu-id="0835b-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0835b-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0835b-111">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="0835b-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="0835b-112">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="0835b-112">In the **No.**</span></span> <span data-ttu-id="0835b-113">seuraava numero sarjasta.</span><span class="sxs-lookup"><span data-stu-id="0835b-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="0835b-114">Valitse **Lähdetyyppi**-kentässä tuotantotilauksen lähde.</span><span class="sxs-lookup"><span data-stu-id="0835b-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="0835b-115">Voit valita täällä tuotenimikeperheen tuotannon.</span><span class="sxs-lookup"><span data-stu-id="0835b-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="0835b-116">Lisätietoja on kohdassa [Tuotantoperheiden käyttäminen](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="0835b-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="0835b-117">Valitse **Lähteen nro** -kentässä nimikenumero, tuoteperhe tai myynnin tunnistetiedot, jolle tuotantotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="0835b-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="0835b-118">Täytä **Määrä**- ja **Eräpäivä**-kentät määritystesi mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="0835b-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="0835b-119">Kun tuotannon vaatimukset, kuten komponentit tai toiminnot, muuttuvat, voit suunnitella tuotantotilauksen nopeasti uudelleen.</span><span class="sxs-lookup"><span data-stu-id="0835b-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="0835b-120">Lisätietoja on kohdassa [Tuotantotilausten suora uudelleensuunnittelu tai päivitys](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="0835b-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="0835b-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0835b-121">See Also</span></span>  
<span data-ttu-id="0835b-122">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="0835b-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="0835b-123">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0835b-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="0835b-124">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="0835b-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="0835b-125">Varasto</span><span class="sxs-lookup"><span data-stu-id="0835b-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="0835b-126">Osto</span><span class="sxs-lookup"><span data-stu-id="0835b-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="0835b-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0835b-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
