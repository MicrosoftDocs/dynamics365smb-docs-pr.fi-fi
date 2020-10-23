---
title: Komponenttien materiaalinotto toiminnan tuotoksen mukaan | Microsoft Docs
description: Jos nimikkeiden määrityksessä on käytetty Taaksepäin-materiaalinottotapaa, oletustoiminto laskee ja kirjaa kulutuksen automaattisesti, kun vapautetun tuotantotilauksen tilaksi muutetaan **Valmis**. Lisätietoja on kohdassa Materiaalinottotapa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 366c450924367ba70eece30809035895c42a0838
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921615"
---
# <a name="flush-components-according-to-operation-output"></a><span data-ttu-id="919f2-104">Komponenttien materiaalinotto toiminnan tuotoksen mukaan</span><span class="sxs-lookup"><span data-stu-id="919f2-104">Flush Components According to Operation Output</span></span>
<span data-ttu-id="919f2-105">Jos nimikkeiden määrityksessä on käytetty Taaksepäin-materiaalinottotapaa, oletustoiminto laskee ja kirjaa kulutuksen automaattisesti, kun vapautetun tuotantotilauksen tilaksi muutetaan **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="919f2-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="919f2-106">Jos määrität myös reitityslinkin koodeja, laskenta ja kirjaus tehdään toiminnon valmistuttua. Toiminnon kuluttama todellinen määrä kirjataan.</span><span class="sxs-lookup"><span data-stu-id="919f2-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="919f2-107">Lisätietoja on kohdassa [Reititysten luominen](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="919f2-107">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="919f2-108">Tuotantotilauksessa voidaan esimerkiksi määrittää, että 800 metrin tuottaminen vaatii 8 kg komponentteja. Jos tuotokseksi kirjataan 200 metriä, kulutukseksi kirjataan automaattisesti 2 kg.</span><span class="sxs-lookup"><span data-stu-id="919f2-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="919f2-109">Tämä toiminto on hyödyllinen seuraavista syistä:</span><span class="sxs-lookup"><span data-stu-id="919f2-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="919f2-110">**Varaston arvostus** - Tuotoksen ja kulutuksen arvotapahtumat luodaan rinnakkain tuotantotilauksen edetessä.</span><span class="sxs-lookup"><span data-stu-id="919f2-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="919f2-111">Ilman reitityslinkkien koodeja varastoarvo kasvaa, kun tuotos kirjataan ja vähenee sitten myöhemmin, kun komponentin kulutusarvo kirjataan yhdessä valmiin tuotantotilauksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="919f2-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="919f2-112">**Varastosaatavuus** - Asteittaista kulutuskirjausta käytettäessä komponenttinimikkeiden saatavuus on paremmin ajan tasalla, mikä on tärkeää kysynnän ja tarjonnan välilsen sisäisen tasapainon ylläpitämiseksi.</span><span class="sxs-lookup"><span data-stu-id="919f2-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="919f2-113">Ilman reitityslinkkien koodeja muut osan vaatimukset voivat olettaa, että se on käytettävissä, niin kauan kuin se odottaa viivästynyttä kulukirjausta.</span><span class="sxs-lookup"><span data-stu-id="919f2-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="919f2-114">**Just-in-Time** – Voit mukauttaa tuotteita asikkaan pyyntöjen mukaan ja siten minimoida jätteet varmistamalla, että työ- ja järjestelmämuutoksia tehdään vain tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="919f2-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="919f2-115">Seuraavassa ohjeessa neuvotaan, miten taaksepäin suuntautuvan materiaalinoton ja reitityslinkkien koodit voidaan yhdistää niin, että materiaalinottomäärä toimintoa kohden on verrannollinen toiminnon todelliseen tuotokseen.</span><span class="sxs-lookup"><span data-stu-id="919f2-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="919f2-116">Voit tyhjentää osat toiminnon tuotoksen mukaan</span><span class="sxs-lookup"><span data-stu-id="919f2-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="919f2-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="919f2-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="919f2-118">Valitse **Muokkaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="919f2-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="919f2-119">Valitse **Täydennys**-pikavälilehden **Materiaalinottotapa**-kentässä select **Eteenpäin**.</span><span class="sxs-lookup"><span data-stu-id="919f2-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="919f2-120">Valitse **Poiminta + eteenpäin**, jos komponenttia käytetään ohjatuille hyllytyksille ja poiminnoille määritetyssä sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="919f2-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="919f2-121">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Reititykset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="919f2-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="919f2-122">Määritä reitityslinkkikoodit jokaiselle työvaiheelle, joka kuluttaa komponentin.</span><span class="sxs-lookup"><span data-stu-id="919f2-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="919f2-123">Lisätietoja on kohdassa [Reititysten luominen ](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="919f2-123">For more information, see [Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="919f2-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tuotannon tuoterakenne** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="919f2-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="919f2-125">Määritä reitityslinkkikoodit kustakin komponentin esiintymästä toimintoon, jossa se kulutetaan.</span><span class="sxs-lookup"><span data-stu-id="919f2-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="919f2-126">Osalla on oltava reitityslinkki viimeisimpään reititysoperaatioon.</span><span class="sxs-lookup"><span data-stu-id="919f2-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="919f2-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="919f2-127">See Also</span></span>  
[<span data-ttu-id="919f2-128">Tuotannon tuoterakenteiden luominen</span><span class="sxs-lookup"><span data-stu-id="919f2-128">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="919f2-129">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="919f2-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="919f2-130">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="919f2-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="919f2-131">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="919f2-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="919f2-132">Varasto</span><span class="sxs-lookup"><span data-stu-id="919f2-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="919f2-133">Osto</span><span class="sxs-lookup"><span data-stu-id="919f2-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="919f2-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="919f2-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
