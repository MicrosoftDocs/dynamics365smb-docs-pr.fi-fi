---
title: "Rakennetiedot – Integrointi varaston kanssa | Microsoft Docs"
description: "Varastoinninhallinta- ja Varasto-sovellusalue ovat yhteydessä toistensa kanssa inventoinnissa ja inventoinnin tai fyysisen varaston muutoksessa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="130e2-103">Rakennetiedot: integrointi varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="130e2-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="130e2-104">Varastoinninhallinta- ja Varasto-sovellusalue ovat yhteydessä toistensa kanssa inventoinnissa ja inventoinnin tai fyysisen varaston muutoksessa.</span><span class="sxs-lookup"><span data-stu-id="130e2-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="130e2-105">Physical Inventory</span><span class="sxs-lookup"><span data-stu-id="130e2-105">Physical Inventory</span></span>  
 <span data-ttu-id="130e2-106">**F. var. inventointipvk** -ikkunaa käytetään **Inventointipäiväkirja** -ikkunassa kaikkien fyysisen varaston lisäsijaintien osalta.</span><span class="sxs-lookup"><span data-stu-id="130e2-106">The **Whse. Phys. Inventory Journal** window is used with the **Phys. Inventory Journal** window for all advanced warehouse locations.</span></span> <span data-ttu-id="130e2-107">Varaston tai bin-tiedoston taso lasketaan ja tulostettu luettelo annetaan varastotyöntekijälle.</span><span class="sxs-lookup"><span data-stu-id="130e2-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="130e2-108">Luettelossa näytetään, mitkä nimikkeet missä bineissä täytyy laskea.</span><span class="sxs-lookup"><span data-stu-id="130e2-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="130e2-109">Varastotyöntekijä syöttää inventoidun määrän **F. var. inventointipvk** -ikkunaan ja kirjaa päiväkirjan.</span><span class="sxs-lookup"><span data-stu-id="130e2-109">The warehouse employee enters the counted quantity in the **Whse. Phys. Inventory Journal** window and then posts the journal.</span></span>  
  
 <span data-ttu-id="130e2-110">Jos laskettu määrä on suurempi kuin päiväkirjarivillä oleva määrä, siirto kirjataan tälle erolle oletusarvoisesta muutosvarastopaikasta laskettuun varastopaikkaan.</span><span class="sxs-lookup"><span data-stu-id="130e2-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="130e2-111">Tämä nostaa määrää inventoidussa varastopaikassa ja laskee määrää muutoksen oletusvarastopaikassa.</span><span class="sxs-lookup"><span data-stu-id="130e2-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="130e2-112">Jos laskettu määrä on pienempi kuin päiväkirjarivillä oleva määrä, siirto kirjataan tälle erolle lasketusta varastopaikasta oletusarvoiseen muutosvarastopaikkaan.</span><span class="sxs-lookup"><span data-stu-id="130e2-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="130e2-113">Tämä laskee määrää inventoidussa varastopaikassa ja nostaa määrää muutoksen oletusvarastopaikassa.</span><span class="sxs-lookup"><span data-stu-id="130e2-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="130e2-114">Laajennetuissa varastomäärityksissä **Määrä (laskettu)**-kentän arvo noudetaan nimiketapahtumista ja **Määrä (inventointi)**-kentän arvo noudetaan fyysisen varaston tapahtumista, varastopaikan sisällön muutosta lukuun ottamatta.</span><span class="sxs-lookup"><span data-stu-id="130e2-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="130e2-115">**Määrä**-kenttä määrittää eron ensimmäisten kahden kentän välillä, jonka tulisi olla yhtä suuri kuin mukautetun binin sisältö.</span><span class="sxs-lookup"><span data-stu-id="130e2-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="130e2-116">Kun kirjaat inventointipäiväkirjan, varaston ja oletusmuutoksen varastopaikka päivitetään.</span><span class="sxs-lookup"><span data-stu-id="130e2-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="130e2-117">Nimikekirjausten fyysisen varastoinnin muutokset</span><span class="sxs-lookup"><span data-stu-id="130e2-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="130e2-118">**Nimikepäiväkirja**-ikkunan ja **Laske f.var. muutos** -toiminnon avulla voit muuttaa nimiketapahtuman varaston sen mukaan, miten fyysisen varastoinnin varastopaikan nimikemäärää on muutettu.</span><span class="sxs-lookup"><span data-stu-id="130e2-118">You use the **Item Journal** window and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="130e2-119">Kun haluat luoda linkin varaston ja fyysisen varaston välille, määritä oletusmuutosvarastopaikka sijaintia kohti.</span><span class="sxs-lookup"><span data-stu-id="130e2-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="130e2-120">Oletusarvoinen mukautettava bin rekisteröi varastonimikkeet, kun tiliöit varaston kasvun.</span><span class="sxs-lookup"><span data-stu-id="130e2-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="130e2-121">Jos kuitenkin kirjaat vähennystä, myös oletusvarastopaikan määrä vähenee.</span><span class="sxs-lookup"><span data-stu-id="130e2-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="130e2-122">Molemmissa tapauksissa luodaan nimiketapahtumat ja fyysisen varastoinnin tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="130e2-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="130e2-123">Mukautettua biniä ei ole sisällytetty saatavuuslaskelmaan.</span><span class="sxs-lookup"><span data-stu-id="130e2-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="130e2-124">Jos haluat muuttaa varastopaikan sisältöä, voit käyttää fyysisen varastoinnin nimikepäiväkirjaa, josta voit kirjoittaa muutettavan nimikenumeron, vyöhykekoodin, varastopaikkakoodin ja määrän.</span><span class="sxs-lookup"><span data-stu-id="130e2-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="130e2-125">Jos kirjoitat positiivisen määrän ja kirjaat rivin, varastopaikkaan tallennettu varaston määrä lisääntyy ja oletusarvoisen muutosvarastopaikan määrä pienenee vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="130e2-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="130e2-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="130e2-126">See Also</span></span>  
 <span data-ttu-id="130e2-127">[Rakennetiedot: f. varaston hallinta](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="130e2-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="130e2-128">Rakennetiedot: saatavuus varastossa</span><span class="sxs-lookup"><span data-stu-id="130e2-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)
