---
title: "Tuotannon tuotos- ja suoritusaikojen eräkirjaus| Microsoft Docs"
description: "Tuotosmäärä kuvaa työn edistymistä valmiin määrän muodossa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e885149e28c2e09dc244bc5c0a431e7b2fe047a5
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="9ed74-103">Tuotos- ja suoritusaikojen eräkirjaus</span><span class="sxs-lookup"><span data-stu-id="9ed74-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="9ed74-104">Tuotosmäärä kuvaa työn edistymistä valmiin määrän muodossa.</span><span class="sxs-lookup"><span data-stu-id="9ed74-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="9ed74-105">Varasto päivitetään automaattisesti vasta, kun kirjaat viimeisen toiminnon tuotosmäärän.</span><span class="sxs-lookup"><span data-stu-id="9ed74-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="9ed74-106">Vähintään yhden tuotantotilausrivin tuotosmäärän kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="9ed74-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="9ed74-107">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotospäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9ed74-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9ed74-108">Täytä kentät tuotantotilauksen tiedoilla ja tuotostiedoilla.</span><span class="sxs-lookup"><span data-stu-id="9ed74-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="9ed74-109">Jos toiminto on valmis, valitse **Valmis**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="9ed74-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="9ed74-110">Jos fyysisen varaston sijainti, johon nimikkeet hyllytetään, käyttää varastopaikkoja, mutta ei vaadi hyllytystä,  määritä päiväkirjan riville varastopaikkakoodi osoittamaan, mihin nimikkeet tulee sijoittaa fyysisessä varastossa.</span><span class="sxs-lookup"><span data-stu-id="9ed74-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="9ed74-111">Lisätietoja on kohdassa [Tuotannon tai kokoonpanon tuotoksen hyllytys](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="9ed74-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="9ed74-112">Kirjaa toiminnot valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="9ed74-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="9ed74-113">Tuotosmäärä kirjataan.</span><span class="sxs-lookup"><span data-stu-id="9ed74-113">The output quantity will be posted.</span></span> <span data-ttu-id="9ed74-114">Nimike on nyt saatavilla toimitettavaksi.</span><span class="sxs-lookup"><span data-stu-id="9ed74-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="9ed74-115">Vähintään yhden tuotantotilausrivin suoritusaikojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="9ed74-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="9ed74-116">Ajoaika kuvastaa työn edistymistä tarvittavan työajan muodossa.</span><span class="sxs-lookup"><span data-stu-id="9ed74-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="9ed74-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotospäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9ed74-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9ed74-118">Täytä kentät tuotantotilauksen tiedoilla ja tuotostiedoilla.</span><span class="sxs-lookup"><span data-stu-id="9ed74-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="9ed74-119">Jos toiminto on valmis, valitse **Valmis**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="9ed74-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="9ed74-120">Kirjaa toimintakohtainen kulutettu aika valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="9ed74-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="9ed74-121">Käytettyjen tuotantosolujen tai kuormitusryhmien kapasiteettitapahtumat päivitetään.</span><span class="sxs-lookup"><span data-stu-id="9ed74-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ed74-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9ed74-122">See Also</span></span>  
<span data-ttu-id="9ed74-123">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="9ed74-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="9ed74-124">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9ed74-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="9ed74-125">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="9ed74-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="9ed74-126">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="9ed74-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9ed74-127">Osto</span><span class="sxs-lookup"><span data-stu-id="9ed74-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9ed74-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9ed74-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

