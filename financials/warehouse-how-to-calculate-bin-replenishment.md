---
title: "Varastopaikan täydennyksen laskeminen | Microsoft Docs"
description: "Kun sijainti on määritetty käyttämään ohjattua hyllytystä ja poimintaa, hyllytysmallin sijainnin painopisteet otetaan huomioon kun vastaanottoja hyllytetään."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a683d2f88f8c30d457d44facd21b0068688ad05a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-calculate-bin-replenishment"></a><span data-ttu-id="b591b-103">Kuinka laskea var.paikan täydennys</span><span class="sxs-lookup"><span data-stu-id="b591b-103">How to: Calculate Bin Replenishment</span></span>
<span data-ttu-id="b591b-104">Kun sijainti on määritetty käyttämään ohjattua hyllytystä ja poimintaa, hyllytysmallin sijainnin prioriteetit otetaan huomioon, kun vastaanottoja hyllytetään.</span><span class="sxs-lookup"><span data-stu-id="b591b-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="b591b-105">Prioriteetteja ovat varastopaikan sisällön pienin ja suurin määrä, joka on vahvistettu tietylle varastopaikalle, sekä varastopaikan luokittelut.</span><span class="sxs-lookup"><span data-stu-id="b591b-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="b591b-106">Tästä seuraa, että jos nimikkeitä saapuu tasaiseen tahtiin, eniten käytetyt poimintavarastopaikat täyttyvät samalla, kun niitä tyhjennetään.</span><span class="sxs-lookup"><span data-stu-id="b591b-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="b591b-107">Varasto ei kuitenkaan aina saavu tasaiseen tahtiin.</span><span class="sxs-lookup"><span data-stu-id="b591b-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="b591b-108">Nimikkeitä ostetaan joskus suurissa määrissä, jotta yritys saisi alennuksen, tai tuotantoyksikkö voi tuottaa suuren määrän yhtä nimikettä, jotta saavutettaisiin alhainen yksikköhinta.</span><span class="sxs-lookup"><span data-stu-id="b591b-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="b591b-109">Sitten taas nimikkeitä ei vastaanoteta fyysiselle varastolle pitkään aikaan, ja fyysisessä varastossa täytyy ajoittain siirtää nimikkeitä poimintavarastopaikkoihin irtotavaran varastointialueilta.</span><span class="sxs-lookup"><span data-stu-id="b591b-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="b591b-110">Voi olla myös niin, että fyysiselle varastolle odotetaan uutta varastoa saapuvaksi lähiaikoina, ja irtotavaran varastointialue halutaan tyhjentää nimikkeistä ennen kuin uudet tavarat saapuvat.</span><span class="sxs-lookup"><span data-stu-id="b591b-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="b591b-111">Jos olet määritellyt irtotavaran varastopaikoille varastopaikan tyypin, jonka toimintona on vain **Hyllytys** (varastopaikalla ei ole rastia **Poiminta**-toiminnon kohdalla), poimintavarastopaikat täytyy aina pitää täydennettyinä, koska ohjelma ei ehdota varaston hyllytystä varaston poiminnalle.</span><span class="sxs-lookup"><span data-stu-id="b591b-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="b591b-112">Poiminnan varastopaikkojen täydentäminen</span><span class="sxs-lookup"><span data-stu-id="b591b-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="b591b-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Siirtotyökirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b591b-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b591b-114">Avaa raportin pyyntösivu valitsemalla **Laske var.paikan täydennys** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b591b-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="b591b-115">Täytä eräajon pyyntöikkuna rajoittaaksesi niiden täydennysehdotusten laajuutta, jotka ohjelma laskee.</span><span class="sxs-lookup"><span data-stu-id="b591b-115">Fill in the batch job request window to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="b591b-116">Sinua voivat kiinnostaa esimerkiksi tietyt nimikkeet, alueet tai varastopaikat.</span><span class="sxs-lookup"><span data-stu-id="b591b-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="b591b-117">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="b591b-117">Choose the **OK** button.</span></span> <span data-ttu-id="b591b-118">Napsauta OK ja ohjelma luo rivejä täydennyssiirtoja varten, jotka tulee suorittaa niiden sääntöjen mukaan, jotka on määritetty varastopaikoille ja varastopaikkojen sisällölle (varastopaikkojen sisältämille nimikkeille).</span><span class="sxs-lookup"><span data-stu-id="b591b-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="b591b-119">Jos haluat suorittaa kaikki ehdotetut täydennykset, valitse **Luo siirto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b591b-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="b591b-120">Työntekijät voivat nyt etsiä ohjeet **Var.siirrot**-valikkoaiheesta, suorittaa ja rekisteröidä ne.</span><span class="sxs-lookup"><span data-stu-id="b591b-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="b591b-121">Jos haluat suorittaa vain joitain ehdotuksista, poista vähemmän tärkeät rivit ja luo sitten siirto.</span><span class="sxs-lookup"><span data-stu-id="b591b-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="b591b-122">Seuraavan kerran kun lasket varastopaikan täydennystä, ohjelma luo uudelleen poistamasi ehdotukset, jos ne ovat silloin vielä voimassa.</span><span class="sxs-lookup"><span data-stu-id="b591b-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b591b-123">Oletetaan, että nimike täyttää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="b591b-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="b591b-124">Nimikkeellä on vanhentumispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b591b-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="b591b-125">Sijaintikortin **FEFO-poiminta**-kentässä valitaan.</span><span class="sxs-lookup"><span data-stu-id="b591b-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="b591b-126">Käytät **Laske var.paikan täydennys**-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="b591b-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="b591b-127">Tällöin **Alue koodista**- ja  **Var.paikasta**-kentät jätetään tyhjiksi, sillä nimikkeiden siirron lähtökohdan laskeva algoritmi käynnistyy vain, kun käytät **Luo siirto** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="b591b-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b591b-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b591b-128">See Also</span></span>  
[<span data-ttu-id="b591b-129">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="b591b-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b591b-130">FEFO-poiminta</span><span class="sxs-lookup"><span data-stu-id="b591b-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="b591b-131">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="b591b-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b591b-132">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="b591b-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="b591b-133">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b591b-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b591b-134">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="b591b-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b591b-135">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b591b-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

