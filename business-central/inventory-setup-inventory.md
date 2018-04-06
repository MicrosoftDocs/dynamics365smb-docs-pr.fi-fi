---
title: "Varaston määrittäminen| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten varastoinnin ja varaston prosessit määritetään. Kyse voi olla esimerkiksi siirtoreiteistä ja sijainneista, kuten fyysisistä varastoista."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 62eee7532e457721430cb31519b5acb23e95bfcb
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="9c9cb-103">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9c9cb-103">Setting Up Inventory</span></span>
<span data-ttu-id="9c9cb-104">Ennen varastoaktiviteettien ja varaston arvostuksen hallinnan aloittamista on määritettävä yrityksen varastonhallintakäytäntöjen säännöt ja arvot.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="9c9cb-105">Voit parantaa asiakaspalvelua ja optimoida toimitusketjuasi järjestämällä varastosi eri osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="9c9cb-106">Voit sitten ostaa, varastoida tai myydä nimikkeitä eri sijainneissa ja siirtää varastoa niiden välillä.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="9c9cb-107">Kun olet määrittänyt varaston, voit hallita nimiketapahtumien liittyviä erilaisia prosesseja.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="9c9cb-108">Lisätietoja on kohdissa [Varaston hallinta](inventory-manage-inventory.md) ja [Varastoinninhallinta](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="9c9cb-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="9c9cb-109">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="9c9cb-109">To</span></span> | <span data-ttu-id="9c9cb-110">Katso</span><span class="sxs-lookup"><span data-stu-id="9c9cb-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="9c9cb-111">Määritä yleiset varastoasetukset, kuten numerosarjat ja sijaintien käyttötapa.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="9c9cb-112">Yleisten varastotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9c9cb-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="9c9cb-113">Määritä tehokas jakelumallin, joka sisältää liikekumppaneille tai työntekijöille määritetyn eri sijaintien ja vastuupaikkojen yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="9c9cb-114">Vastuupaikkojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="9c9cb-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="9c9cb-115">Järjestele varastonhallinta usealle sijainnille, mukaan lukien siirtoreitit.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="9c9cb-116">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9c9cb-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="9c9cb-117">Luo niille varastonimikkeille nimikekortit, joilla käyt kauppaa.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="9c9cb-118">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="9c9cb-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="9c9cb-119">Määritä nimikkeelle useita vaihtoehtoisia mittayksiköitä, joita voit esimerkiksi myynti-, osto- tai tuotantotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-119">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="9c9cb-120">Nimikkeen mittayksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9c9cb-120">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="9c9cb-121">Täydennä nimike kortteja tallentamalla niihin tietoja nimikkeestä tietyn sijainnin ja/tai tietyn varianttikoodin perusteella.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-121">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="9c9cb-122">Varastointiyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9c9cb-122">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="9c9cb-123">Kun määrität nimikkeitä luokkiin ja annat niille määritteitä, nimikkeiden etsiminen helpottuu.</span><span class="sxs-lookup"><span data-stu-id="9c9cb-123">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="9c9cb-124">Nimikkeiden luokitteleminen</span><span class="sxs-lookup"><span data-stu-id="9c9cb-124">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="9c9cb-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9c9cb-125">See Also</span></span>
[<span data-ttu-id="9c9cb-126">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="9c9cb-126">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9c9cb-127">Ostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="9c9cb-127">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9c9cb-128">[Myynnin hallinta](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="9c9cb-128">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="9c9cb-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9c9cb-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9c9cb-130">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="9c9cb-130">General Business Functionality</span></span>](ui-across-business-areas.md)

