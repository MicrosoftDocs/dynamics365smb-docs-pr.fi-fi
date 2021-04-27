---
title: Kapasiteettien kirjaaminen | Microsoft Docs
description: Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle. Esimerkiksi ylläpitotyö tulee määritellä kapasiteetille, muttei tuotantotilaukselle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8f41a5033c79ec500a635d27f8296d01d895ed27
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787925"
---
# <a name="post-capacities"></a><span data-ttu-id="f443c-104">Kapasiteettien kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="f443c-104">Post Capacities</span></span>
<span data-ttu-id="f443c-105">Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="f443c-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="f443c-106">Esimerkiksi ylläpitotyö tulee määritellä kapasiteetille, muttei tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="f443c-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="f443c-107">Kapasiteettien kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="f443c-107">To post capacities</span></span>  
1.  <span data-ttu-id="f443c-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kapasiteettipäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f443c-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f443c-109">Täytä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.</span><span class="sxs-lookup"><span data-stu-id="f443c-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="f443c-110">Syötä **Tyyppi**-kenttään kapasiteetin tyyppi (**Kuormitusryhmä** tai **Tuotantosolu**), jota olet kirjaamassa.</span><span class="sxs-lookup"><span data-stu-id="f443c-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="f443c-111">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="f443c-111">In the **No.**</span></span> <span data-ttu-id="f443c-112">kuormitusryhmän tai tuotantosolun numero.</span><span class="sxs-lookup"><span data-stu-id="f443c-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="f443c-113">Syötä asianmukaiset tiedot muihin kenttiin, esimerkiksi **Aloitusaika**-, **Lopetusaika**-, **Määrä**- ja **Hukkatavara**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="f443c-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="f443c-114">Kirjaa kapasiteetit valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f443c-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="f443c-115">Tuotantosolutapahtumien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="f443c-115">To view work center ledger entries</span></span>  
<span data-ttu-id="f443c-116">Voit tarkastella **Tuotantosolukortti**- ja **Kuormitusryhmän kortti** -sivuilla valmiiden tuotantotilausten tuloksena kirjattuja kapasiteetteja.</span><span class="sxs-lookup"><span data-stu-id="f443c-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="f443c-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tuotantosolut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f443c-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f443c-118">Avaa käsiteltävä **Tuotantosolukortti** luettelossa ja valitse sitten **Kapasiteettitapahtumat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f443c-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="f443c-119">**Kapasiteettitapahtumat**-sivulla näkyvät tuotantosolun kirjatut tapahtumat siinä järjestyksessä kuin ne on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="f443c-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="f443c-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f443c-120">See Also</span></span>  
<span data-ttu-id="f443c-121">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="f443c-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="f443c-122">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f443c-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="f443c-123">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="f443c-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="f443c-124">Varasto</span><span class="sxs-lookup"><span data-stu-id="f443c-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f443c-125">Osto</span><span class="sxs-lookup"><span data-stu-id="f443c-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f443c-126">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f443c-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]