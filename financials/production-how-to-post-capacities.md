---
title: Kapasiteettien kirjaaminen | Microsoft Docs
description: "Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle. Esimerkiksi ylläpitotyö tulee määritellä kapasiteetille, muttei tuotantotilaukselle."
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
ms.openlocfilehash: a30e62bf2bf62c547398d733fcfe80b0204805cf
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a><span data-ttu-id="80c73-104">Kapasiteettien kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="80c73-104">Post Capacities</span></span>
<span data-ttu-id="80c73-105">Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="80c73-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="80c73-106">Esimerkiksi ylläpitotyö on määritettävä määritellä kapasiteetille mutta ei tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="80c73-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="80c73-107">Kapasiteettien kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="80c73-107">To post capacities</span></span>  
1.  <span data-ttu-id="80c73-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kapasiteettipäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="80c73-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="80c73-109">Täytä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.</span><span class="sxs-lookup"><span data-stu-id="80c73-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="80c73-110">Syötä **Tyyppi**-kenttään kapasiteetin tyyppi (**Kuormitusryhmä** tai **Tuotantosolu**), jota olet kirjaamassa.</span><span class="sxs-lookup"><span data-stu-id="80c73-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="80c73-111">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="80c73-111">In the **No.**</span></span> <span data-ttu-id="80c73-112">kuormitusryhmän tai tuotantosolun numero.</span><span class="sxs-lookup"><span data-stu-id="80c73-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="80c73-113">Syötä asianmukaiset tiedot muihin kenttiin, esimerkiksi **Aloitusaika**-, **Lopetusaika**-, **Määrä**- ja **Hukkatavara**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="80c73-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="80c73-114">Kirjaa kapasiteetit valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="80c73-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="80c73-115">Tuotantosolutapahtumien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="80c73-115">To view work center ledger entries</span></span>  
<span data-ttu-id="80c73-116">Voit tarkastella **Tuotantosolukortti**- ja **Kuormitusryhmän kortti** -ikkunoissa valmiiden tuotantotilausten tuloksena kirjattuja kapasiteetteja.</span><span class="sxs-lookup"><span data-stu-id="80c73-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="80c73-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotantosolut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="80c73-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="80c73-118">Avaa käsiteltävä **Tuotantosolukortti** luettelossa ja valitse sitten **Kapasiteettitapahtumat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="80c73-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="80c73-119">**Kapasiteettitapahtumat**-ikkunassa näkyvät tuotantosolun kirjatut tapahtumat siinä järjestyksessä kuin ne on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="80c73-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="80c73-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="80c73-120">See Also</span></span>  
<span data-ttu-id="80c73-121">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="80c73-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="80c73-122">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="80c73-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="80c73-123">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="80c73-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="80c73-124">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="80c73-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="80c73-125">Osto</span><span class="sxs-lookup"><span data-stu-id="80c73-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="80c73-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80c73-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

