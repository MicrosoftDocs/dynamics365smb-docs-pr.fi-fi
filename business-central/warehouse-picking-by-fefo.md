---
title: "FEFO-poiminnan ottaminen käyttöön | Microsoft Docs"
description: "FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin."
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
ms.openlocfilehash: 7e494ebc118b7c75ab565ae57259030987bbeee7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="5fd7f-103">FEFO-poiminnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="5fd7f-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="5fd7f-104">FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="5fd7f-105">Tämä toiminto toimii vain, kun seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="5fd7f-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="5fd7f-106">Nimikkeellä on oltava sarjanumero tai eränumero.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="5fd7f-107">Nimikkeen seurantakoodiasetuksissa on valittava kenttä **Sarjanumerokohtainen varastoseuranta** field or the **Eränumerokohtainen varastoseuranta**.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="5fd7f-108">Nimike on kirjattu varastoon vanhentumispäivämäärän kera.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="5fd7f-109">Sijaintikortissa on valittava valintaruutu **Vaadi poiminta**.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="5fd7f-110">Sijaintikortissa on valittava valintaruutu **FEFO-poiminta**.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="5fd7f-111">Sijaintikortissa on valittava **Var.paikka pakollinen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="5fd7f-112">Kun kaikki ehdot täyttyvät, poimittavat sarja/erä-numeroidut nimikkeet lajitellaan vanhimmat ensin kaikissa poiminnoissa ja siirroissa, lukuun ottamatta nimikkeitä, jotka käyttävät sarjanrokohtaista tai eränumerokohtaista seurantaa.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="5fd7f-113">Jos jotkin sarja-/eränumeroidut nimikkeet käyttävät erityistä seurantaa, ne otetaan ensin huomioon. Näiden jälkeen jäljellä olevat määrittämättömät sarja-/eränumerot luetellaan FEFO:n mukaan.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="5fd7f-114">Jos kahdella erä-/sarjanumeroidulla nimikkeellä on sama vanhentumispäivämäärä, ohjelma valitsee nimikkeen, jolla on pienempi sarja- tai eränumero.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="5fd7f-115">Kun sarja- tai eränumeroituja nimikkeitä poimitaan ohjattua hyllytystä ja poimintaa varten määritetyissä sijainneissa, FEFO poimii vain tyyppiä *Poiminta* olevien varastopaikkojen määrät.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="5fd7f-116">Ota varastosiirrot käyttöön FEFO:n mukaan joko **Varaston siirto** -ikkunassa tai **Siirtotyökirja** -ikkunassa ja jätä **Varastopaikasta** -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-116">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="5fd7f-117">Jos **Tiukka vanhentumisen kirj.** -kenttä on valittuna, poimintaan sisällytetään vain ne kohteet, jotka eivät ole vanhentuneet.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="5fd7f-118">Tämä pätee myös silloin, kun et käytä poimintaa FEFO-periaatteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="5fd7f-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fd7f-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5fd7f-119">See Also</span></span>  
<span data-ttu-id="5fd7f-120">[Nimikkeiden poiminta](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="5fd7f-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="5fd7f-121">[Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="5fd7f-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="5fd7f-122">[Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="5fd7f-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="5fd7f-123">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="5fd7f-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="5fd7f-124">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="5fd7f-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5fd7f-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fd7f-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

