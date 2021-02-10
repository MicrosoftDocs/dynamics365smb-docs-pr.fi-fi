---
title: Tuotoksen kirjaamisen peruuttaminen | Microsoft Docs
description: Tuotoksen kirjaus täytyy joissakin tilanteissa peruuttaa. Tällainen tilanne voi olla esimerkiksi, jos tiedot annettiin virheellisesti ja tuotantotilaukseen kirjataan väärä tuotoksen määrä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ed275469dd172af43ceb96b85d5ac0aa99e96a2f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759040"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="a381c-104">Tuotoksen kirjaamisen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="a381c-104">Reverse Output Posting</span></span>
<span data-ttu-id="a381c-105">Tuotoksen kirjaus täytyy joissakin tilanteissa peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="a381c-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="a381c-106">Tällainen tilanne voi olla esimerkiksi, jos tiedot annettiin virheellisesti ja tuotantotilaukseen kirjataan väärä tuotoksen määrä.</span><span class="sxs-lookup"><span data-stu-id="a381c-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="a381c-107">Peruuta tuotoksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="a381c-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="a381c-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tuotospäiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a381c-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="a381c-109">Valitse haluamasi erä.</span><span class="sxs-lookup"><span data-stu-id="a381c-109">Select your batch.</span></span>  
2. <span data-ttu-id="a381c-110">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="a381c-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="a381c-111">Lisätietoja on kohdassa [Tuotoksen ja ajoaikojen eräkirjaaminen](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="a381c-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="a381c-112">Valitse **Kohdistetaan tapahtumaan** -kentässä asiaan liittyvä nimiketapahtuma.</span><span class="sxs-lookup"><span data-stu-id="a381c-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="a381c-113">Tämä peruuttaa kapasiteetti- ja nimiketapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a381c-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="a381c-114">Kirjaa peruutus kirjaamalla päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="a381c-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="a381c-115">Tuotospäiväkirjan tapahtumat kirjataan nimiketapahtumiin positiivisena muutoksena.</span><span class="sxs-lookup"><span data-stu-id="a381c-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a381c-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a381c-116">See Also</span></span>  
 <span data-ttu-id="a381c-117">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a381c-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="a381c-118">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a381c-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="a381c-119">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="a381c-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="a381c-120">Varasto</span><span class="sxs-lookup"><span data-stu-id="a381c-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="a381c-121">Osto</span><span class="sxs-lookup"><span data-stu-id="a381c-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="a381c-122">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a381c-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
