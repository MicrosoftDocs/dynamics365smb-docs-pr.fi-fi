---
title: Rakennetiedot – Integrointi varaston kanssa | Microsoft Docs
description: Varastoinninhallinta- ja Varasto-sovellusalue ovat yhteydessä toistensa kanssa inventoinnissa ja inventoinnin tai fyysisen varaston muutoksessa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 40b80ec45f998831c1fe71eb52a21f098c25dfdb
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307106"
---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="487bb-103">Rakennetiedot: integrointi varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="487bb-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="487bb-104">Varastoinninhallinta- ja Varasto-sovellusalue ovat yhteydessä toistensa kanssa inventoinnissa ja inventoinnin tai fyysisen varaston muutoksessa.</span><span class="sxs-lookup"><span data-stu-id="487bb-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="487bb-105">Fyysinen varasto</span><span class="sxs-lookup"><span data-stu-id="487bb-105">Physical Inventory</span></span>  
 <span data-ttu-id="487bb-106">**F. var. inventointipvk** -sivu käytetään **Inventointipäiväkirja**-sivulla kaikkien fyysisen varaston lisäsijaintien osalta.</span><span class="sxs-lookup"><span data-stu-id="487bb-106">The **Whse. Phys. Inventory Journal** page is used with the **Phys. Inventory Journal** page for all advanced warehouse locations.</span></span> <span data-ttu-id="487bb-107">Varaston tai bin-tiedoston taso lasketaan ja tulostettu luettelo annetaan varastotyöntekijälle.</span><span class="sxs-lookup"><span data-stu-id="487bb-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="487bb-108">Luettelossa näytetään, mitkä nimikkeet missä bineissä täytyy laskea.</span><span class="sxs-lookup"><span data-stu-id="487bb-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="487bb-109">Varastotyöntekijä antaa inventoidun määrän **F. var. inventointipvk** -sivulla ja kirjaa päiväkirjan.</span><span class="sxs-lookup"><span data-stu-id="487bb-109">The warehouse employee enters the counted quantity on the **Whse. Phys. Inventory Journal** page and then posts the journal.</span></span>  
  
 <span data-ttu-id="487bb-110">Jos laskettu määrä on suurempi kuin päiväkirjarivillä oleva määrä, siirto kirjataan tälle erolle oletusarvoisesta muutosvarastopaikasta laskettuun varastopaikkaan.</span><span class="sxs-lookup"><span data-stu-id="487bb-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="487bb-111">Tämä nostaa määrää inventoidussa varastopaikassa ja laskee määrää muutoksen oletusvarastopaikassa.</span><span class="sxs-lookup"><span data-stu-id="487bb-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="487bb-112">Jos laskettu määrä on pienempi kuin päiväkirjarivillä oleva määrä, siirto kirjataan tälle erolle lasketusta varastopaikasta oletusarvoiseen muutosvarastopaikkaan.</span><span class="sxs-lookup"><span data-stu-id="487bb-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="487bb-113">Tämä laskee määrää inventoidussa varastopaikassa ja nostaa määrää muutoksen oletusvarastopaikassa.</span><span class="sxs-lookup"><span data-stu-id="487bb-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="487bb-114">Laajennetuissa varastomäärityksissä **Määrä (laskettu)**-kentän arvo noudetaan nimiketapahtumista ja **Määrä (inventointi)**-kentän arvo noudetaan fyysisen varaston tapahtumista, varastopaikan sisällön muutosta lukuun ottamatta.</span><span class="sxs-lookup"><span data-stu-id="487bb-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="487bb-115">**Määrä**-kenttä määrittää eron ensimmäisten kahden kentän välillä, jonka tulisi olla yhtä suuri kuin mukautetun binin sisältö.</span><span class="sxs-lookup"><span data-stu-id="487bb-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="487bb-116">Kun kirjaat inventointipäiväkirjan, varaston ja oletusmuutoksen varastopaikka päivitetään.</span><span class="sxs-lookup"><span data-stu-id="487bb-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="487bb-117">Nimikekirjausten fyysisen varastoinnin muutokset</span><span class="sxs-lookup"><span data-stu-id="487bb-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="487bb-118">**Nimikepäiväkirja**-sivun ja **Laske f.var. muutos** -toiminnon avulla voit muuttaa nimiketapahtuman varaston sen mukaan, miten fyysisen varastoinnin varastopaikan nimikemäärää on muutettu.</span><span class="sxs-lookup"><span data-stu-id="487bb-118">You use the **Item Journal** page and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="487bb-119">Kun haluat luoda linkin varaston ja fyysisen varaston välille, määritä oletusmuutosvarastopaikka sijaintia kohti.</span><span class="sxs-lookup"><span data-stu-id="487bb-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="487bb-120">Oletusarvoinen mukautettava bin rekisteröi varastonimikkeet, kun tiliöit varaston kasvun.</span><span class="sxs-lookup"><span data-stu-id="487bb-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="487bb-121">Jos kuitenkin kirjaat vähennystä, myös oletusvarastopaikan määrä vähenee.</span><span class="sxs-lookup"><span data-stu-id="487bb-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="487bb-122">Molemmissa tapauksissa luodaan nimiketapahtumat ja fyysisen varastoinnin tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="487bb-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="487bb-123">Mukautettua biniä ei ole sisällytetty saatavuuslaskelmaan.</span><span class="sxs-lookup"><span data-stu-id="487bb-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="487bb-124">Jos haluat muuttaa varastopaikan sisältöä, voit käyttää fyysisen varastoinnin nimikepäiväkirjaa, josta voit kirjoittaa muutettavan nimikenumeron, vyöhykekoodin, varastopaikkakoodin ja määrän.</span><span class="sxs-lookup"><span data-stu-id="487bb-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="487bb-125">Jos kirjoitat positiivisen määrän ja kirjaat rivin, varastopaikkaan tallennettu varaston määrä lisääntyy ja oletusarvoisen muutosvarastopaikan määrä pienenee vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="487bb-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="487bb-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="487bb-126">See Also</span></span>  
 <span data-ttu-id="487bb-127">[Rakennetiedot: f. varaston hallinta](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="487bb-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="487bb-128">Rakennetiedot: saatavuus varastossa</span><span class="sxs-lookup"><span data-stu-id="487bb-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)