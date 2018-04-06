---
title: Kapasiteettien kirjaaminen | Microsoft Docs
description: "Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle. Esimerkiksi ylläpitotyö tulee määritellä kapasiteetille, muttei tuotantotilaukselle."
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
ms.openlocfilehash: 6114149372b786c20ee7edbe13022abe688ed9a2
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a><span data-ttu-id="74161-104">Kapasiteettien kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="74161-104">Post Capacities</span></span>
<span data-ttu-id="74161-105">Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="74161-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="74161-106">Esimerkiksi ylläpitotyö on määritettävä määritellä kapasiteetille mutta ei tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="74161-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="74161-107">Kapasiteettien kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="74161-107">To post capacities</span></span>  
1.  <span data-ttu-id="74161-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kapasiteettipäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="74161-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="74161-109">Täytä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.</span><span class="sxs-lookup"><span data-stu-id="74161-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="74161-110">Syötä **Tyyppi**-kenttään kapasiteetin tyyppi (**Kuormitusryhmä** tai **Tuotantosolu**), jota olet kirjaamassa.</span><span class="sxs-lookup"><span data-stu-id="74161-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="74161-111">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="74161-111">In the **No.**</span></span> <span data-ttu-id="74161-112">kuormitusryhmän tai tuotantosolun numero.</span><span class="sxs-lookup"><span data-stu-id="74161-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="74161-113">Syötä asianmukaiset tiedot muihin kenttiin, esimerkiksi **Aloitusaika**-, **Lopetusaika**-, **Määrä**- ja **Hukkatavara**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="74161-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="74161-114">Kirjaa kapasiteetit valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="74161-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="74161-115">Tuotantosolutapahtumien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="74161-115">To view work center ledger entries</span></span>  
<span data-ttu-id="74161-116">Voit tarkastella **Tuotantosolukortti**- ja **Kuormitusryhmän kortti** -ikkunoissa valmiiden tuotantotilausten tuloksena kirjattuja kapasiteetteja.</span><span class="sxs-lookup"><span data-stu-id="74161-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="74161-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotantosolut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="74161-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="74161-118">Avaa käsiteltävä **Tuotantosolukortti** luettelossa ja valitse sitten **Kapasiteettitapahtumat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="74161-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="74161-119">**Kapasiteettitapahtumat**-ikkunassa näkyvät tuotantosolun kirjatut tapahtumat siinä järjestyksessä kuin ne on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="74161-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="74161-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="74161-120">See Also</span></span>  
<span data-ttu-id="74161-121">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="74161-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="74161-122">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="74161-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="74161-123">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="74161-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="74161-124">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="74161-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="74161-125">Osto</span><span class="sxs-lookup"><span data-stu-id="74161-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="74161-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="74161-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

