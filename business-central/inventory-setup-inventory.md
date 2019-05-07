---
title: Varaston määrittäminen| Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten varastoinnin ja varaston prosessit määritetään. Kyse voi olla esimerkiksi siirtoreiteistä ja sijainneista, kuten fyysisistä varastoista.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: 038e3a9bfdb66a8d714f4f9452f0322623e6ddc4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "934325"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="44fb6-103">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="44fb6-103">Setting Up Inventory</span></span>
<span data-ttu-id="44fb6-104">Ennen varastoaktiviteettien ja varaston arvostuksen hallinnan aloittamista on määritettävä yrityksen varastonhallintakäytäntöjen säännöt ja arvot.</span><span class="sxs-lookup"><span data-stu-id="44fb6-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="44fb6-105">Voit parantaa asiakaspalvelua ja optimoida toimitusketjuasi järjestämällä varastosi eri osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="44fb6-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="44fb6-106">Voit sitten ostaa, varastoida tai myydä nimikkeitä eri sijainneissa ja siirtää varastoa niiden välillä.</span><span class="sxs-lookup"><span data-stu-id="44fb6-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="44fb6-107">Kun olet määrittänyt varaston, voit hallita nimiketapahtumien liittyviä erilaisia prosesseja.</span><span class="sxs-lookup"><span data-stu-id="44fb6-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="44fb6-108">Lisätietoja on kohdissa [Varaston hallinta](inventory-manage-inventory.md) ja [Varastoinninhallinta](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="44fb6-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="44fb6-109">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="44fb6-109">To</span></span> | <span data-ttu-id="44fb6-110">Katso</span><span class="sxs-lookup"><span data-stu-id="44fb6-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="44fb6-111">Määritä yleiset varastoasetukset, kuten numerosarjat ja sijaintien käyttötapa.</span><span class="sxs-lookup"><span data-stu-id="44fb6-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="44fb6-112">Yleisten varastotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="44fb6-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="44fb6-113">Määritä tehokas jakelumallin, joka sisältää liikekumppaneille tai työntekijöille määritetyn eri sijaintien ja vastuupaikkojen yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="44fb6-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="44fb6-114">Vastuupaikkojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="44fb6-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="44fb6-115">Järjestele varastonhallinta usealle sijainnille, mukaan lukien siirtoreitit.</span><span class="sxs-lookup"><span data-stu-id="44fb6-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="44fb6-116">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="44fb6-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="44fb6-117">Luo nimikkeen kortteja varasto- tai huoltonimikkeille tai muille kuin varastonimikkeille, joilla käyt kauppaa.</span><span class="sxs-lookup"><span data-stu-id="44fb6-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="44fb6-118">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="44fb6-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="44fb6-119">Lisätietoja **Tyyppi**-kentän täyttämisestä nimikkeen korteissa liiketoiminnan tarkoituksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="44fb6-119">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="44fb6-120">Tietoja nimiketyypeistä</span><span class="sxs-lookup"><span data-stu-id="44fb6-120">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="44fb6-121">Määritä nimikkeelle useita vaihtoehtoisia mittayksiköitä, joita voit esimerkiksi myynti-, osto- tai tuotantotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="44fb6-121">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="44fb6-122">Nimikkeen mittayksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="44fb6-122">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="44fb6-123">Täydennä nimike kortteja tallentamalla niihin tietoja nimikkeestä tietyn sijainnin ja/tai tietyn varianttikoodin perusteella.</span><span class="sxs-lookup"><span data-stu-id="44fb6-123">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="44fb6-124">Varastointiyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="44fb6-124">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="44fb6-125">Kun määrität nimikkeitä luokkiin ja annat niille määritteitä, nimikkeiden etsiminen helpottuu.</span><span class="sxs-lookup"><span data-stu-id="44fb6-125">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="44fb6-126">Nimikkeiden luokitteleminen</span><span class="sxs-lookup"><span data-stu-id="44fb6-126">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="44fb6-127">Tuo useita nimikekuvia samalla kerralla zip-tiedostosta, jossa tiedostot on nimetty nimikenumeroiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="44fb6-127">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="44fb6-128">Useiden nimikekuvien tuominen</span><span class="sxs-lookup"><span data-stu-id="44fb6-128">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|

## <a name="see-also"></a><span data-ttu-id="44fb6-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="44fb6-129">See Also</span></span>
[<span data-ttu-id="44fb6-130">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="44fb6-130">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="44fb6-131">Ostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="44fb6-131">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="44fb6-132">[Myynnin hallinta](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="44fb6-132">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="44fb6-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="44fb6-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="44fb6-134">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="44fb6-134">General Business Functionality</span></span>](ui-across-business-areas.md)
