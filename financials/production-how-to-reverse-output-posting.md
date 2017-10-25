---
title: Tuotoksen kirjaamisen peruuttaminen | Microsoft Docs
description: "Tuotoksen kirjaus täytyy joissakin tilanteissa peruuttaa. Tällainen tilanne voi olla esimerkiksi, jos tietojen syötössä on ilmennyt virhe ja tuotantotilaukseen kirjataan väärä tuotoksen määrä."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7ac453ff87d78e6be0567ba93b58c0f8938f4052
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-output-posting"></a><span data-ttu-id="15e71-104">Tuotoksen kirjaamisen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="15e71-104">How to: Reverse Output Posting</span></span>
<span data-ttu-id="15e71-105">Tuotoksen kirjaus täytyy joissakin tilanteissa peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="15e71-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="15e71-106">Tällainen tilanne voi olla esimerkiksi, jos tiedot annettiin virheellisesti ja tuotantotilaukseen kirjataan väärä tuotoksen määrä.</span><span class="sxs-lookup"><span data-stu-id="15e71-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="15e71-107">Peruuta tuotoksen kirjaus</span><span class="sxs-lookup"><span data-stu-id="15e71-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="15e71-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotospäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="15e71-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="15e71-109">Valitse haluamasi erä.</span><span class="sxs-lookup"><span data-stu-id="15e71-109">Select your batch.</span></span>  
2. <span data-ttu-id="15e71-110">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="15e71-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="15e71-111">Lisätietoja on kohdassa [Toimintaohje: Tuotoksen ja ajoaikojen eräkirjaaminen](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="15e71-111">For more information, see [How to: Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="15e71-112">Valitse **Kohdistetaan tapahtumaan** -kentässä asiaan liittyvä nimiketapahtuma.</span><span class="sxs-lookup"><span data-stu-id="15e71-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="15e71-113">Tämä peruuttaa kapasiteetti- ja nimiketapahtumat.</span><span class="sxs-lookup"><span data-stu-id="15e71-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="15e71-114">Kirjaa peruutus kirjaamalla päiväkirja.</span><span class="sxs-lookup"><span data-stu-id="15e71-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="15e71-115">Tuotospäiväkirjan tapahtumat kirjataan nimiketapahtumiin positiivisena muutoksena.</span><span class="sxs-lookup"><span data-stu-id="15e71-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="15e71-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="15e71-116">See Also</span></span>  
 <span data-ttu-id="15e71-117">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="15e71-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="15e71-118">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="15e71-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="15e71-119">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="15e71-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="15e71-120">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="15e71-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="15e71-121">Osto</span><span class="sxs-lookup"><span data-stu-id="15e71-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="15e71-122">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="15e71-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

