---
title: Tuotannon tuotos- ja suoritusaikojen eräkirjaus
description: Tuotosmäärä ilmaisee työn edistymisen valmiina määränä ja tuotantosolun tai kuormitusryhmän käytettynä kapasiteettina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787875"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="e3bc9-103">Tuotos- ja suoritusaikojen eräkirjaus</span><span class="sxs-lookup"><span data-stu-id="e3bc9-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="e3bc9-104">Tuotosmäärä ilmaisee työn edistymisen valmiina määränä ja tuotantosolun tai kuormitusryhmän käytettynä kapasiteettina.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="e3bc9-105">Tuotospäiväkirjaa voi käyttää seuraaviin:</span><span class="sxs-lookup"><span data-stu-id="e3bc9-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="e3bc9-106">Varastomäärän muutos valmiiden nimikkeiden tuotannon mukaan.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="e3bc9-107">Määrien ja hävikin rekisteröinti kussakin tuotantoreitityksen toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="e3bc9-108">Tuotantosolujen ja kuormitusryhmien määrityksen ja suoritusajan rekisteröinti.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="e3bc9-109">Jos tuotannon reititystä käytetään, varasto päivitetään vasta, kun kirjaat viimeisen toiminnon tuotosmäärän.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="e3bc9-110">**Tuotantopäiväkirja**-ikkunassa voi suorittaa samat tehtävät kuin **Tuotospäivä**-ikkunassa ja samaan aikaan voi suorittaa kulutuskirjauksiin liittyviä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="e3bc9-111">Lisätietoja on kohdassa [Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen rekisteröiminen](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="e3bc9-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="e3bc9-112">Vähintään yhden tuotantotilausrivin tuotosmäärän ja/tai suoritusaikojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="e3bc9-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="e3bc9-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tuotospäiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e3bc9-114">Täytä kentät tuotantotilauksen tiedoilla, tuotostiedoilla ja/tai suoritusajalla.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="e3bc9-115">**Pura reititys** -toiminnolla voi luoda päiväkirjarivejä tuotantotilauksista.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="e3bc9-116">Jos toiminto on valmis, valitse **Valmis**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="e3bc9-117">Kirjaa toiminnot valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="e3bc9-118">Kapasiteettitapahtumat kirjataan käytetyille tuotantosoluille ja kuormitusryhmille yhdessä aikaa sekä tuotoksen ja hävikin määrää koskevien tietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="e3bc9-119">Jos viimeinen toiminto on kirjattu, nimike lisätään varastoon.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="e3bc9-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e3bc9-120">See Also</span></span>  
<span data-ttu-id="e3bc9-121">[Hävikin kirjaaminen manuaalisesti](production-how-to-post-scrap.md)
[Tuotoksen kirjaamisen peruuttaminen](production-how-to-reverse-output-posting.md)
[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="e3bc9-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="e3bc9-122">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e3bc9-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="e3bc9-123">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="e3bc9-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="e3bc9-124">Varasto</span><span class="sxs-lookup"><span data-stu-id="e3bc9-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="e3bc9-125">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e3bc9-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
