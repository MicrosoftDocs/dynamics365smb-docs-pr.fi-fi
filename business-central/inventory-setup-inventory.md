---
title: Varaston määrittäminen| Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten varastoinnin ja varaston prosessit määritetään. Kyse voi olla esimerkiksi siirtoreiteistä ja sijainneista, kuten fyysisistä varastoista.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3d11e39e54d864db2eac0a1a2e1919a3cfd7a767
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392997"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="bb142-103">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bb142-103">Setting Up Inventory</span></span>
<span data-ttu-id="bb142-104">Ennen varastoaktiviteettien ja varaston arvostuksen hallinnan aloittamista on määritettävä yrityksen varastonhallintakäytäntöjen säännöt ja arvot.</span><span class="sxs-lookup"><span data-stu-id="bb142-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="bb142-105">Voit parantaa asiakaspalvelua ja optimoida toimitusketjuasi järjestämällä varastosi eri osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="bb142-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="bb142-106">Voit sitten ostaa, varastoida tai myydä nimikkeitä eri sijainneissa ja siirtää varastoa niiden välillä.</span><span class="sxs-lookup"><span data-stu-id="bb142-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="bb142-107">Kun olet määrittänyt varaston, voit hallita nimiketapahtumien liittyviä erilaisia prosesseja.</span><span class="sxs-lookup"><span data-stu-id="bb142-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="bb142-108">Lisätietoja on kohdissa [Varaston hallinta](inventory-manage-inventory.md) ja [Varastoinninhallinta](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="bb142-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="bb142-109">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="bb142-109">To</span></span> | <span data-ttu-id="bb142-110">Katso</span><span class="sxs-lookup"><span data-stu-id="bb142-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="bb142-111">Määritä yleiset varastoasetukset, kuten numerosarjat ja sijaintien käyttötapa.</span><span class="sxs-lookup"><span data-stu-id="bb142-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="bb142-112">Yleisten varastotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bb142-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="bb142-113">Määritä tehokas jakelumallin, joka sisältää liikekumppaneille tai työntekijöille määritetyn eri sijaintien ja vastuupaikkojen yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="bb142-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="bb142-114">Vastuupaikkojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="bb142-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="bb142-115">Järjestele varastonhallinta usealle sijainnille, mukaan lukien siirtoreitit.</span><span class="sxs-lookup"><span data-stu-id="bb142-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="bb142-116">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bb142-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="bb142-117">Luo nimikkeen kortteja varasto- tai huoltonimikkeille tai muille kuin varastonimikkeille, joilla käyt kauppaa.</span><span class="sxs-lookup"><span data-stu-id="bb142-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="bb142-118">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="bb142-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="bb142-119">Luo **Kopioi nimike** -nimikkeellä nopeasti uusi nimikekortti aiemmin luodun kortin perusteella.</span><span class="sxs-lookup"><span data-stu-id="bb142-119">Use the **Copy Item** function to quickly create a new item card based on an existing one.</span></span>|[<span data-ttu-id="bb142-120">Uusien nimikkeiden luominen kopioimalla aiemmin luotuja nimikkeitä</span><span class="sxs-lookup"><span data-stu-id="bb142-120">Copy Existing Items to Create New Items</span></span>](inventory-how-copy-items.md)|
|<span data-ttu-id="bb142-121">Lisätietoja **Tyyppi**-kentän täyttämisestä nimikkeen korteissa liiketoiminnan tarkoituksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="bb142-121">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="bb142-122">Tietoja nimiketyypeistä</span><span class="sxs-lookup"><span data-stu-id="bb142-122">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="bb142-123">Määritä nimikkeelle useita vaihtoehtoisia mittayksiköitä, joita voit esimerkiksi myynti-, osto- tai tuotantotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="bb142-123">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="bb142-124">Nimikkeen mittayksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bb142-124">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="bb142-125">Täydennä nimike kortteja tallentamalla niihin tietoja nimikkeestä tietyn sijainnin ja/tai tietyn varianttikoodin perusteella.</span><span class="sxs-lookup"><span data-stu-id="bb142-125">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="bb142-126">Varastointiyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bb142-126">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="bb142-127">Kun määrität nimikkeitä luokkiin ja annat niille määritteitä, nimikkeiden etsiminen helpottuu.</span><span class="sxs-lookup"><span data-stu-id="bb142-127">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="bb142-128">Nimikkeiden luokitteleminen</span><span class="sxs-lookup"><span data-stu-id="bb142-128">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="bb142-129">Tuo useita nimikekuvia samalla kerralla zip-tiedostosta, jossa tiedostot on nimetty nimikenumeroiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="bb142-129">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="bb142-130">Useiden nimikekuvien tuominen</span><span class="sxs-lookup"><span data-stu-id="bb142-130">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|
|<span data-ttu-id="bb142-131">Määritä oletusraportteja, joita käytetään eri asiakirjatyypeille.</span><span class="sxs-lookup"><span data-stu-id="bb142-131">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="bb142-132">Raporttien valinta Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="bb142-132">Report Selection in Business Central</span></span>](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="bb142-133">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="bb142-133">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="bb142-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="bb142-134">See Also</span></span>

[<span data-ttu-id="bb142-135">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="bb142-135">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="bb142-136">Ostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="bb142-136">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="bb142-137">[Myynnin hallinta](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="bb142-137">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="bb142-138">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bb142-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="bb142-139">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="bb142-139">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]