---
title: Varastopaikan täydennyksen laskeminen | Microsoft Docs
description: Kun sijainti on määritetty käyttämään ohjattua hyllytystä ja poimintaa, hyllytysmallin sijainnin painopisteet otetaan huomioon kun vastaanottoja hyllytetään.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1caac5faaaf62fc8e8e53cbb5c6bcce8ce767d6d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911846"
---
# <a name="calculate-bin-replenishment"></a><span data-ttu-id="8aa91-103">Laske var.paikan täydennys</span><span class="sxs-lookup"><span data-stu-id="8aa91-103">Calculate Bin Replenishment</span></span>
<span data-ttu-id="8aa91-104">Kun sijainti on määritetty käyttämään ohjattua hyllytystä ja poimintaa, hyllytysmallin sijainnin painopisteet otetaan huomioon kun vastaanottoja hyllytetään.</span><span class="sxs-lookup"><span data-stu-id="8aa91-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="8aa91-105">Prioriteetteja ovat varastopaikan sisällön pienin ja suurin määrä, joka on vahvistettu tietylle varastopaikalle, sekä varastopaikan luokittelut.</span><span class="sxs-lookup"><span data-stu-id="8aa91-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="8aa91-106">Tästä seuraa, että jos nimikkeitä saapuu tasaiseen tahtiin, eniten käytetyt poimintavarastopaikat täyttyvät samalla, kun niitä tyhjennetään.</span><span class="sxs-lookup"><span data-stu-id="8aa91-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="8aa91-107">Varasto ei kuitenkaan aina saavu tasaiseen tahtiin.</span><span class="sxs-lookup"><span data-stu-id="8aa91-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="8aa91-108">Nimikkeitä ostetaan joskus suurissa määrissä, jotta yritys saisi alennuksen, tai tuotantoyksikkö voi tuottaa suuren määrän yhtä nimikettä, jotta saavutettaisiin alhainen yksikköhinta.</span><span class="sxs-lookup"><span data-stu-id="8aa91-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="8aa91-109">Sitten taas nimikkeitä ei vastaanoteta fyysiselle varastolle pitkään aikaan, ja fyysisessä varastossa täytyy ajoittain siirtää nimikkeitä poimintavarastopaikkoihin irtotavaran varastointialueilta.</span><span class="sxs-lookup"><span data-stu-id="8aa91-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="8aa91-110">Voi olla myös niin, että fyysiselle varastolle odotetaan uutta varastoa saapuvaksi lähiaikoina, ja irtotavaran varastointialue halutaan tyhjentää nimikkeistä ennen kuin uudet tavarat saapuvat.</span><span class="sxs-lookup"><span data-stu-id="8aa91-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="8aa91-111">Jos olet määritellyt irtotavaran varastopaikoille varastopaikan tyypin, jonka toimintona on vain **Hyllytys** (varastopaikalla ei ole rastia **Poiminta**-toiminnon kohdalla), poimintavarastopaikat täytyy aina pitää täydennettyinä, koska ohjelma ei ehdota varaston hyllytystä varaston poiminnalle.</span><span class="sxs-lookup"><span data-stu-id="8aa91-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="8aa91-112">Poiminnan varastopaikkojen täydentäminen</span><span class="sxs-lookup"><span data-stu-id="8aa91-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="8aa91-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Siirtotyökirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8aa91-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8aa91-114">Avaa raportin pyyntösivu valitsemalla **Laske var.paikan täydennys** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="8aa91-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="8aa91-115">Täytä eräajon pyyntösivu rajoittaaksesi niiden täydennysehdotusten laajuutta, jotka ohjelma laskee.</span><span class="sxs-lookup"><span data-stu-id="8aa91-115">Fill in the batch job request page to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="8aa91-116">Sinua voivat kiinnostaa esimerkiksi tietyt nimikkeet, alueet tai varastopaikat.</span><span class="sxs-lookup"><span data-stu-id="8aa91-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="8aa91-117">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="8aa91-117">Choose the **OK** button.</span></span> <span data-ttu-id="8aa91-118">Napsauta OK ja ohjelma luo rivejä täydennyssiirtoja varten, jotka tulee suorittaa niiden sääntöjen mukaan, jotka on määritetty varastopaikoille ja varastopaikkojen sisällölle (varastopaikkojen sisältämille nimikkeille).</span><span class="sxs-lookup"><span data-stu-id="8aa91-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="8aa91-119">Jos haluat suorittaa kaikki ehdotetut täydennykset, valitse **Luo siirto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="8aa91-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="8aa91-120">Työntekijät voivat nyt etsiä ohjeet **Var.siirrot**-valikkoaiheesta, suorittaa ja rekisteröidä ne.</span><span class="sxs-lookup"><span data-stu-id="8aa91-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="8aa91-121">Jos haluat suorittaa vain joitain ehdotuksista, poista vähemmän tärkeät rivit ja luo sitten siirto.</span><span class="sxs-lookup"><span data-stu-id="8aa91-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="8aa91-122">Seuraavan kerran kun lasket varastopaikan täydennystä, ohjelma luo uudelleen poistamasi ehdotukset, jos ne ovat silloin vielä voimassa.</span><span class="sxs-lookup"><span data-stu-id="8aa91-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8aa91-123">Oletetaan, että nimike täyttää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="8aa91-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="8aa91-124">Nimikkeellä on vanhentumispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="8aa91-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="8aa91-125">Sijaintikortin **FEFO-poiminta**-kentässä valitaan.</span><span class="sxs-lookup"><span data-stu-id="8aa91-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="8aa91-126">Käytät **Laske var.paikan täydennys**-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="8aa91-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="8aa91-127">Tällöin **Alue koodista**- ja  **Var.paikasta**-kentät jätetään tyhjiksi, sillä nimikkeiden siirron lähtökohdan laskeva algoritmi käynnistyy vain, kun käytät **Luo siirto** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="8aa91-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8aa91-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8aa91-128">See Also</span></span>  
[<span data-ttu-id="8aa91-129">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="8aa91-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="8aa91-130">FEFO-poiminta</span><span class="sxs-lookup"><span data-stu-id="8aa91-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="8aa91-131">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="8aa91-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="8aa91-132">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="8aa91-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="8aa91-133">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="8aa91-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="8aa91-134">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="8aa91-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="8aa91-135">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8aa91-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
