---
title: "Varaston määrittäminen| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten varastoinnin ja varaston prosessit määritetään. Kyse voi olla esimerkiksi siirtoreiteistä ja sijainneista, kuten fyysisistä varastoista."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 09/08/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 022cd32a11546913e74aeccdd74772e6e01755d3
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-inventory"></a><span data-ttu-id="c0006-103">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c0006-103">Setting Up Inventory</span></span>
<span data-ttu-id="c0006-104">Ennen varastoaktiviteettien ja varaston arvostuksen hallinnan aloittamista on määritettävä yrityksen varastonhallintakäytäntöjen säännöt ja arvot.</span><span class="sxs-lookup"><span data-stu-id="c0006-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="c0006-105">Voit parantaa asiakaspalvelua ja optimoida toimitusketjuasi järjestämällä varastosi eri osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="c0006-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="c0006-106">Voit sitten ostaa, varastoida tai myydä nimikkeitä eri sijainneissa ja siirtää varastoa niiden välillä.</span><span class="sxs-lookup"><span data-stu-id="c0006-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="c0006-107">Kun olet määrittänyt varaston, voit hallita nimiketapahtumien liittyviä erilaisia prosesseja.</span><span class="sxs-lookup"><span data-stu-id="c0006-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="c0006-108">Lisätietoja on kohdissa [Varaston hallinta](inventory-manage-inventory.md) ja [Varastoinninhallinta](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="c0006-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="c0006-109">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="c0006-109">To</span></span> | <span data-ttu-id="c0006-110">Katso</span><span class="sxs-lookup"><span data-stu-id="c0006-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="c0006-111">Määritä yleiset varastoasetukset, kuten numerosarjat ja sijaintien käyttötapa.</span><span class="sxs-lookup"><span data-stu-id="c0006-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="c0006-112">Toimintaohje: Yleisten varastotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c0006-112">How to: Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="c0006-113">Määritä tehokas jakelumallin, joka sisältää liikekumppaneille tai työntekijöille määritetyn eri sijaintien ja vastuupaikkojen yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="c0006-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="c0006-114">Toimintaohje: Vastuupaikkojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="c0006-114">How to: Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="c0006-115">Järjestele varastonhallinta usealle sijainnille, mukaan lukien siirtoreitit.</span><span class="sxs-lookup"><span data-stu-id="c0006-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="c0006-116">Toimintaohje: Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c0006-116">How to: Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="c0006-117">Luo niille varastonimikkeille nimikekortit, joilla käyt kauppaa.</span><span class="sxs-lookup"><span data-stu-id="c0006-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="c0006-118">Toimintaohje: Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="c0006-118">How to: Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="c0006-119">Täydennä nimike kortteja tallentamalla niihin tietoja nimikkeestä tietyn sijainnin ja/tai tietyn varianttikoodin perusteella.</span><span class="sxs-lookup"><span data-stu-id="c0006-119">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="c0006-120">Varastointiyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c0006-120">How to: Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="c0006-121">Kun määrität nimikkeitä luokkiin ja annat niille määritteitä, nimikkeiden etsiminen helpottuu.</span><span class="sxs-lookup"><span data-stu-id="c0006-121">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="c0006-122">Toimintaohje: Nimikkeiden luokitteleminen</span><span class="sxs-lookup"><span data-stu-id="c0006-122">How to: Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="c0006-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c0006-123">See Also</span></span>
[<span data-ttu-id="c0006-124">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="c0006-124">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c0006-125">Ostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="c0006-125">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c0006-126">[Myynnin hallinta](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="c0006-126">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="c0006-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c0006-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c0006-128">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="c0006-128">General Business Functionality</span></span>](ui-across-business-areas.md)

