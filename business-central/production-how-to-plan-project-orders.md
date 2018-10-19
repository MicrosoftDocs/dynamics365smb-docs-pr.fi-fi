---
title: Projektitilausten suunnittelu | Microsoft Docs
description: "Tämä suunnittelutehtävä aloitetaan myyntitilauksesta ja tehdään **Myyntitilaus suunnittelu** -ikkunan avulla. Kun projektituotantotilaus on luotu, voit jatkaa suunnittelua **Tilauksen suunnittelu** -ikkunassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 08cd8c323e8f5221bd6915618582441a739e77c8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="plan-project-orders"></a><span data-ttu-id="4afa6-104">Projektitilausten suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="4afa6-104">Plan Project Orders</span></span>
<span data-ttu-id="4afa6-105">Tämä suunnittelutehtävä aloitetaan myyntitilauksesta ja tehdään **Myyntitilaus suunnittelu** -ikkunan avulla.</span><span class="sxs-lookup"><span data-stu-id="4afa6-105">This planning task starts from a sales order and uses the **Sales Order Planning** window.</span></span> <span data-ttu-id="4afa6-106">Kun projektituotantotilaus on luotu, voit jatkaa suunnittelua **Tilauksen suunnittelu** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="4afa6-106">Once you have created a project production order, you can plan it further by using the **Order Planning** window.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="4afa6-107">Projektituotantotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="4afa6-107">To create a project production order</span></span>  

1.  <span data-ttu-id="4afa6-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4afa6-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4afa6-109">Valitse tuotantoprojektia vastaava myyntitilaus ja valitse sitten **Suunnittelu**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4afa6-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="4afa6-110">Valitse **Myyntitilaus suunnittelu** -ikkunassa **Luo tuotantotilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="4afa6-110">In the **Sales Order Planning** window, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="4afa6-111">Valitse **Luo tilaus myynnistä** -ikkunan **Tilaustyyppi**-kentästä **Projektitilaus**.</span><span class="sxs-lookup"><span data-stu-id="4afa6-111">In the **Create Order from Sales** window, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="4afa6-112">Valitse **Kyllä**-painike.</span><span class="sxs-lookup"><span data-stu-id="4afa6-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="4afa6-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotantotilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4afa6-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="4afa6-114">Avaa juuri luotuun tuotantotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="4afa6-114">Open the production order just created.</span></span>  

    <span data-ttu-id="4afa6-115">Huomaa, että tuotantotilauksen **Lähdetyyppi**-kentässä on **Myynnin tunnistetiedot** ja että tilaus sisältää useita rivejä (yhden kutakin tuotettavaa myyntirivin nimikettä kohden).</span><span class="sxs-lookup"><span data-stu-id="4afa6-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="4afa6-116">Valitse **Suunnittelu**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4afa6-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="4afa6-117">Laske uusi kysyntä valitsemalla **Tilauksen suunnittelu** -ikkunassa **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="4afa6-117">In the **Order Planning** window, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="4afa6-118">Projektin tilauksen tilausotsikkorivillä näytetään kaikki täyttämättömät kysyntärivit, kun se laajennetaan.</span><span class="sxs-lookup"><span data-stu-id="4afa6-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="4afa6-119">Vaikka tuotantotilauksessa on rivejä useille tuotantonimikkeille, kaikkien tuotantotilausrivien kokonaiskysyntä näkyy yhden tilausotsikkorivin alla **Tilauksen suunnittelu** -ikkunassa, ja alkuperäisen asiakkaan nimi näytetään.</span><span class="sxs-lookup"><span data-stu-id="4afa6-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line in the **Order Planning** window, and the original customer name is displayed.</span></span> <span data-ttu-id="4afa6-120">Voit nyt suunnitella kysynnän kohdassa [Uuden kysynnän tilauskohtainen suunnittelu](production-how-to-plan-for-new-demand.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="4afa6-120">You can now proceed to plan for the demand as described in [Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4afa6-121">Projektin tuotantotilauksen kysyntärivellä, joilla on **Tuotantotilaus** niiden **Täydennysjärjestelmä** -kentässä, edustavat perustana olevia tuotantotilauksia..</span><span class="sxs-lookup"><span data-stu-id="4afa6-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="4afa6-122">Kun olet luonut nämä tuotantotilaukset, suunnitelma on laskettava uudelleen **Tilauksen suunnittelu** -ikkunassa, jotta tunnistetaan niiden mahdolliset täyttämättömät osavaatimukset.</span><span class="sxs-lookup"><span data-stu-id="4afa6-122">After you have generated these production orders, you must again calculate a plan in the **Order Planning** window to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="4afa6-123">Komponentit näytetään kysyntäriveinä normaalin tuotantotilausotsikon alla, eli projektisuhde ei enää näy ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="4afa6-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible in the window.</span></span> <span data-ttu-id="4afa6-124">Jos kuitenkin käytetään tilauksen seurantaa, voidaan katsella ja selata kaikkia alkuperäisen myyntitilauksen johdannaisina tehtyjä toimitustilauksia.</span><span class="sxs-lookup"><span data-stu-id="4afa6-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4afa6-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4afa6-125">See Also</span></span>
<span data-ttu-id="4afa6-126">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4afa6-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="4afa6-127">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4afa6-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="4afa6-128">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="4afa6-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="4afa6-129">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="4afa6-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4afa6-130">Osto</span><span class="sxs-lookup"><span data-stu-id="4afa6-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4afa6-131">[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4afa6-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="4afa6-132">Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu</span><span class="sxs-lookup"><span data-stu-id="4afa6-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="4afa6-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4afa6-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

