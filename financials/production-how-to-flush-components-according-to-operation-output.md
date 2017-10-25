---
title: Komponenttien materiaalinotto toiminnan tuotoksen mukaan | Microsoft Docs
description: "Jos nimikkeiden määrityksessä on käytetty Taaksepäin-materiaalinottotapaa, oletustoiminto laskee ja kirjaa kulutuksen automaattisesti, kun vapautetun tuotantotilauksen tilaksi muutetaan **Valmis**. Lisätietoja on kohdassa Materiaalinottotapa."
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
ms.openlocfilehash: b58e897768848b50232b360f3822846d6dd316df
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-flush-components-according-to-operation-output"></a><span data-ttu-id="05efa-104">Komponenttien materiaalinotto toiminnan tuotoksen mukaan</span><span class="sxs-lookup"><span data-stu-id="05efa-104">How to: Flush Components According to Operation Output</span></span>
<span data-ttu-id="05efa-105">Jos nimikkeiden määrityksessä on käytetty Taaksepäin-materiaalinottotapaa, oletustoiminto laskee ja kirjaa kulutuksen automaattisesti, kun vapautetun tuotantotilauksen tilaksi muutetaan **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="05efa-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="05efa-106">Jos määrität myös reitityslinkin koodeja, laskenta ja kirjaus tehdään toiminnon valmistuttua. Toiminnon kuluttama todellinen määrä kirjataan.</span><span class="sxs-lookup"><span data-stu-id="05efa-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="05efa-107">Lisätietoja on kohdassa [Toimintaohje: Reititysten luominen](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="05efa-107">For more information, see [How to: Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="05efa-108">Tuotantotilauksessa voidaan esimerkiksi määrittää, että 800 metrin tuottaminen vaatii 8 kg komponentteja. Jos tuotokseksi kirjataan 200 metriä, kulutukseksi kirjataan automaattisesti 2 kg.</span><span class="sxs-lookup"><span data-stu-id="05efa-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="05efa-109">Tämä toiminto on hyödyllinen seuraavista syistä:</span><span class="sxs-lookup"><span data-stu-id="05efa-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="05efa-110">**Varaston arvostus** - Tuotoksen ja kulutuksen arvotapahtumat luodaan rinnakkain tuotantotilauksen edetessä.</span><span class="sxs-lookup"><span data-stu-id="05efa-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="05efa-111">Ilman reitityslinkkien koodeja varastoarvo kasvaa, kun tuotos kirjataan ja vähenee sitten myöhemmin, kun komponentin kulutusarvo kirjataan yhdessä valmiin tuotantotilauksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="05efa-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="05efa-112">**Varastosaatavuus** - Asteittaista kulutuskirjausta käytettäessä komponenttinimikkeiden saatavuus on paremmin ajan tasalla, mikä on tärkeää kysynnän ja tarjonnan välilsen sisäisen tasapainon ylläpitämiseksi.</span><span class="sxs-lookup"><span data-stu-id="05efa-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="05efa-113">Ilman reitityslinkkien koodeja muut osan vaatimukset voivat olettaa, että se on käytettävissä, niin kauan kuin se odottaa viivästynyttä kulukirjausta.</span><span class="sxs-lookup"><span data-stu-id="05efa-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="05efa-114">**Just-in-Time** – Voit mukauttaa tuotteita asikkaan pyyntöjen mukaan ja siten minimoida jätteet varmistamalla, että työ- ja järjestelmämuutoksia tehdään vain tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="05efa-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="05efa-115">Seuraavassa ohjeessa neuvotaan, miten taaksepäin suuntautuvan materiaalinoton ja reitityslinkkien koodit voidaan yhdistää niin, että materiaalinottomäärä toimintoa kohden on verrannollinen toiminnon todelliseen tuotokseen.</span><span class="sxs-lookup"><span data-stu-id="05efa-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="05efa-116">Voit tyhjentää osat toiminnon tuotoksen mukaan</span><span class="sxs-lookup"><span data-stu-id="05efa-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="05efa-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="05efa-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="05efa-118">Valitse **Muokkaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="05efa-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="05efa-119">Valitse **Täydennys**-pikavälilehden **Materiaalinottotapa**-kentässä select **Eteenpäin**.</span><span class="sxs-lookup"><span data-stu-id="05efa-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="05efa-120">Valitse **Poiminta + eteenpäin**, jos komponenttia käytetään ohjatuille hyllytyksille ja poiminnoille määritetyssä sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="05efa-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="05efa-121">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Reititykset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="05efa-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="05efa-122">Määritä reitityslinkkikoodit jokaiselle työvaiheelle, joka kuluttaa komponentin.</span><span class="sxs-lookup"><span data-stu-id="05efa-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="05efa-123">Lisätietoja on kohdassa [Uusien reititysten luominen](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="05efa-123">For more information, see [How to: Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="05efa-124">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotannon tuoterakenne** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="05efa-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="05efa-125">Määritä reitityslinkkikoodit kustakin komponentin esiintymästä toimintoon, jossa se kulutetaan.</span><span class="sxs-lookup"><span data-stu-id="05efa-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="05efa-126">Osalla on oltava reitityslinkki viimeisimpään reititysoperaatioon.</span><span class="sxs-lookup"><span data-stu-id="05efa-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="05efa-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="05efa-127">See Also</span></span>  
[<span data-ttu-id="05efa-128">Toimintaohje: Uusien tuotannon tuoterakenteiden luominen</span><span class="sxs-lookup"><span data-stu-id="05efa-128">How to: Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="05efa-129">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="05efa-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="05efa-130">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="05efa-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="05efa-131">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="05efa-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="05efa-132">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="05efa-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="05efa-133">Osto</span><span class="sxs-lookup"><span data-stu-id="05efa-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="05efa-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="05efa-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

