---
title: "Tuotannon tuotos- ja suoritusaikojen eräkirjaus| Microsoft Docs"
description: "Tuotosmäärä kuvaa työn edistymistä valmiin määrän muodossa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d1813ab3105023e56347c9321fbbb10944e7f09f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="db792-103">Tuotos- ja suoritusaikojen eräkirjaus</span><span class="sxs-lookup"><span data-stu-id="db792-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="db792-104">Tuotosmäärä kuvaa työn edistymistä valmiin määrän muodossa.</span><span class="sxs-lookup"><span data-stu-id="db792-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="db792-105">Varasto päivitetään automaattisesti vasta, kun kirjaat viimeisen toiminnon tuotosmäärän.</span><span class="sxs-lookup"><span data-stu-id="db792-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="db792-106">Vähintään yhden tuotantotilausrivin tuotosmäärän kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="db792-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="db792-107">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotospäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="db792-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="db792-108">Täytä kentät tuotantotilauksen tiedoilla ja tuotostiedoilla.</span><span class="sxs-lookup"><span data-stu-id="db792-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="db792-109">Jos toiminto on valmis, valitse **Valmis**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="db792-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="db792-110">Jos fyysisen varaston sijainti, johon nimikkeet hyllytetään, käyttää varastopaikkoja, mutta ei vaadi hyllytystä,  määritä päiväkirjan riville varastopaikkakoodi osoittamaan, mihin nimikkeet tulee sijoittaa fyysisessä varastossa.</span><span class="sxs-lookup"><span data-stu-id="db792-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="db792-111">Lisätietoja on kohdassa [Tuotannon tai kokoonpanon tuotoksen hyllytys](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="db792-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="db792-112">Kirjaa toiminnot valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="db792-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="db792-113">Tuotosmäärä kirjataan.</span><span class="sxs-lookup"><span data-stu-id="db792-113">The output quantity will be posted.</span></span> <span data-ttu-id="db792-114">Nimike on nyt saatavilla toimitettavaksi.</span><span class="sxs-lookup"><span data-stu-id="db792-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="db792-115">Vähintään yhden tuotantotilausrivin suoritusaikojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="db792-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="db792-116">Ajoaika kuvastaa työn edistymistä tarvittavan työajan muodossa.</span><span class="sxs-lookup"><span data-stu-id="db792-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="db792-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotospäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="db792-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="db792-118">Täytä kentät tuotantotilauksen tiedoilla ja tuotostiedoilla.</span><span class="sxs-lookup"><span data-stu-id="db792-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="db792-119">Jos toiminto on valmis, valitse **Valmis**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="db792-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="db792-120">Kirjaa toimintakohtainen kulutettu aika valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="db792-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="db792-121">Käytettyjen tuotantosolujen tai kuormitusryhmien kapasiteettitapahtumat päivitetään.</span><span class="sxs-lookup"><span data-stu-id="db792-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="db792-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="db792-122">See Also</span></span>  
<span data-ttu-id="db792-123">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="db792-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="db792-124">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="db792-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="db792-125">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="db792-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="db792-126">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="db792-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="db792-127">Osto</span><span class="sxs-lookup"><span data-stu-id="db792-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="db792-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="db792-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

