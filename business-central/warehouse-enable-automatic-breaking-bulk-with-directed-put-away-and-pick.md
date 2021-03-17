---
title: Automaattinen irtotavaran erottelu ohjatulla hyllytyksellä ja poiminnalla | Microsoft Docs
description: Jos sijainneissa käytetään ohjattua hyllytystä ja poimintaa, voit erotella ison mittayksikön pienempiin mittayksiköihin, kun luodaan fyysisen varastoinnin ohjeita, jotka täyttävät lähdeasiakirjojen, tuotantotilausten tai sisäisten poimintojen ja hyllytysten tarpeet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c00a866a731a321c0cf2e7f29dce4fba296b6d06
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385697"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><span data-ttu-id="f1371-103">Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="f1371-103">Enable Automatic Breaking Bulk with Directed Put-away and Pick</span></span>
<span data-ttu-id="f1371-104">Jos sijainneissa käytetään ohjattua hyllytystä ja poimintaa, [!INCLUDE[prod_short](includes/prod_short.md)] voi useissa eri tilanteissa tehdä automaattisen erottelun eli jakaa ison mittayksikön pienempiin mittayksiköihin luodessaan fyysisen varastoinnin ohjeita, jotka täyttävät lähdeasiakirjojen, tuotantotilausten tai sisäisten poimintojen ja hyllytysten tarpeet.</span><span class="sxs-lookup"><span data-stu-id="f1371-104">For locations that use directed put-away and pick, [!INCLUDE[prod_short](includes/prod_short.md)] can, in various situations, automatically breakbulk, that is, break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.</span></span> <span data-ttu-id="f1371-105">Erotteleminen tarkoittaa joskus myös sitä, että pienempiä mittayksiköitä kootaan tarpeen mukaan yhteen, jotta vastattaisiin lähteviin pyyntöihin: tämä siis tarkoittaa itse asiassa ison mittayksikön jakamista lähdeasiakirjassa tai tuotantotilauksessa pienempiin mittayksiköihin, jotka ovat saatavilla fyysisessä varastossa.</span><span class="sxs-lookup"><span data-stu-id="f1371-105">To breakbulk sometimes also means gathering smaller units of measure, if necessary, to meet outbound requests by breaking the larger unit of measure on the source document or production order into the smaller units of measure that are available in the warehouse.</span></span>   

## <a name="breakbulking-in-picks"></a><span data-ttu-id="f1371-106">Erotteleminen poiminnoissa</span><span class="sxs-lookup"><span data-stu-id="f1371-106">Breakbulking in Picks</span></span>  
<span data-ttu-id="f1371-107">Jos haluat varastoida nimikkeitä useissa eri mittayksiköissä ja antaa ohjelman yhdistellä automaattisesti niitä tarpeiden mukaisesti poimintaprosessissa, lisää rasti sijaintikortin  **Salli erottelu** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f1371-107">If you want to store items in several different units of measure and allow them to be automatically combined as needed in the picking process, select the **Allow Breakbulk** field on the location card.</span></span>  

<span data-ttu-id="f1371-108">Sovellus etsii tehtävän toteuttamista varten automaattisesti nimikettä, joka olisi samassa mittayksikössä.</span><span class="sxs-lookup"><span data-stu-id="f1371-108">To fulfill a task, application automatically looks for an item in the same unit of measure.</span></span> <span data-ttu-id="f1371-109">Jos sovellus ei löydä tätä nimikkeen muotoa, ja jos olet valinnut kyseisen kentän, sovellus ehdottaa ison mittayksikön jakamista tarvittavaksi mittayksiköksi.</span><span class="sxs-lookup"><span data-stu-id="f1371-109">But if it cannot find this form of the item, and this field is selected, application will suggest that you break a larger unit of measure into the unit of measure that is needed.</span></span>  

<span data-ttu-id="f1371-110">Jos järjestelmä löytää vain pieniä mittayksiköitä, se ehdottaa, että nimikkeitä kerätään yhteen toimituksen tai tuotantotilauksen määrän täyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="f1371-110">If the system can only find smaller units of measure, it will suggest that you gather items to fulfill the quantity on the shipment or production order.</span></span> <span data-ttu-id="f1371-111">Itse asiassa se jakaa lähdeasiakirjan ison mittayksikön pienempiin poimintaa varten.</span><span class="sxs-lookup"><span data-stu-id="f1371-111">In effect, it breaks the larger unit of measure on the source document into smaller units for picking.</span></span>  

## <a name="breakbulking-in-put-aways"></a><span data-ttu-id="f1371-112">Erottelu hyllytyksissä</span><span class="sxs-lookup"><span data-stu-id="f1371-112">Breakbulking in Put-aways</span></span>  
<span data-ttu-id="f1371-113">Sovellus ehdottaa fyysisen varastoinnin hyllytyksessä automaattisesti Sijoita toimintorivit hyllytyksen mittayksikössä (esimerkiksi kappaleissa), vaikka nimikkeet saapuvat eri mittayksikössä.</span><span class="sxs-lookup"><span data-stu-id="f1371-113">In the warehouse put-away, application automatically suggests Place action lines in the put-away unit of measure, for example, pieces, even though the items arrive in a different unit of measure.</span></span>  

## <a name="breakbulking-in-movements"></a><span data-ttu-id="f1371-114">Erottelu varastosiirroissa</span><span class="sxs-lookup"><span data-stu-id="f1371-114">Breakbulking in Movements</span></span>  
<span data-ttu-id="f1371-115">Sovellus tekee automaattisen erottelun myös täydennyssiirroissa, jos **Laske var.paikan täydennys** -sivun **Vaihtoehdot**-pikavälilehden **Salli erottelu** -kenttä on valittu.</span><span class="sxs-lookup"><span data-stu-id="f1371-115">The application also breakbulks automatically in replenishment movements, if the **Allow Breakbulk** field is selected on the **Option** FastTab on the **Calculate Bin Replenishment** page.</span></span>  

<span data-ttu-id="f1371-116">Muunnosprosessin mittayksiköstä toiseen tuloksia voi katsella välissä olevina erotteluriveinä hyllytys-, poiminta- ja varastosiirto-ohjeissa.</span><span class="sxs-lookup"><span data-stu-id="f1371-116">You can view the results of the conversion process from one unit of measure to another as intermediate breakbulk lines in the put-away, pick, or movement instructions.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f1371-117">Jos lisäät valintamerkin **Määritä erottelusuodatus** -kenttään fyysisen varaston ohjeiden otsikossa, sovellus piilottaa erottelurivit aina, kun iso mittayksikkö aiotaan käyttää kokonaan.</span><span class="sxs-lookup"><span data-stu-id="f1371-117">If you select the **Set Breakbulk Filter** field on the warehouse instruction header, application will hide the breakbulk lines whenever the larger unit of measure is going to be completely used.</span></span> <span data-ttu-id="f1371-118">Esimerkiksi jos kuormalava on 12 kappaletta ja aiot käyttää kaikki 12 kappaletta, poiminta ohjaa suoraan ottamaan kuormalavan ja sijoittavan 12 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="f1371-118">For example, if a pallet is 12 pieces and you are going to use all 12 pieces, the pick will then direct you to take 1 pallet and place 12 pieces.</span></span> <span data-ttu-id="f1371-119">Jos sinun täytyy kuitenkin poimia vain 9 kappaletta, erottelurivejä ei piiloteta, vaikka olet lisännyt rastin **Erottelusuodatus**-kenttään, koska jäljellä olevat 3 kappaletta täytyy sijoittaa jonnekin varastossa.</span><span class="sxs-lookup"><span data-stu-id="f1371-119">However, if you have to pick only 9 pieces, then the breakbulk lines will not be hidden, even if you have selected the **Breakbulk Filter** field, because you have to place the remaining three pieces somewhere in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f1371-120">Jos haluat mittayksiköiden käytön olevan optimaalista varastossa, myös erotteluominaisuuden yhteydessä, sinun tulisi yrittää aina, kun on mahdollista:</span><span class="sxs-lookup"><span data-stu-id="f1371-120">If you want your units of measure to perform optimally in the warehouse, also in connection with the breakbulk functionality, you should wherever possible try to:</span></span>  
>   
> - <span data-ttu-id="f1371-121">Määrittää nimikkeen perusmittayksiköksi pienin mittayksikkö, jota oletat käsitteleväsi fyysisen varastoinnin prosesseissa.</span><span class="sxs-lookup"><span data-stu-id="f1371-121">Set up the base unit of measure for an item as the smallest unit of measure that you expect to handle in your warehouse processes.</span></span>  
> - <span data-ttu-id="f1371-122">Määrittää nimikkeen vaihtoehtoisiksi mittayksiköiksi perusmittayksikön kerrannaisia.</span><span class="sxs-lookup"><span data-stu-id="f1371-122">Set up your alternative units of measure for the item as multiples of the base unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f1371-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f1371-123">See Also</span></span>  
[<span data-ttu-id="f1371-124">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="f1371-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="f1371-125">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="f1371-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f1371-126">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="f1371-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="f1371-127">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="f1371-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="f1371-128">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="f1371-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="f1371-129">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f1371-129">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]