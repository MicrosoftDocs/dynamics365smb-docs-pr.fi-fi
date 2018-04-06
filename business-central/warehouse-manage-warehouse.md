---
title: Varastotoiminnot | Microsoft Docs
description: "Tavaroiden vastaanoton jälkeen ja ennen tavaroiden toimitusta suoritetaan joukko sisäisiä varastotoimintoja, joiden avulla varmistetaan nimikkeiden tehokas kulku varastossa sekä järjestellään ja ylläpidetään yrityksen varastoja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 604f7e55067efaebed412683ed51ce8717562688
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="36c17-103">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="36c17-103">Warehouse Management</span></span>
<span data-ttu-id="36c17-104">Tavaroiden vastaanoton jälkeen ja ennen tavaroiden toimitusta suoritetaan joukko sisäisiä varastotoimintoja, joiden avulla varmistetaan nimikkeiden tehokas kulku varastossa sekä järjestellään ja ylläpidetään yrityksen varastoja.</span><span class="sxs-lookup"><span data-stu-id="36c17-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="36c17-105">Tyypillisiin varastotoimintoihin kuuluvat nimikkeiden hyllytys, nimikkeiden siirtäminen varaston sisällä tai varastoiden välillä sekä nimikkeiden poiminta kokoonpanoa, tuotantoa tai toimitusta varten.</span><span class="sxs-lookup"><span data-stu-id="36c17-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="36c17-106">Myös nimikkeiden kokoamista myyntiin tai varastoon voidaan pitää varastotoimintoja, mutta niitä käsitellään toisaalla.</span><span class="sxs-lookup"><span data-stu-id="36c17-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="36c17-107">Lisätietoja on kohdassa [Kokoonpanon hallinta](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="36c17-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="36c17-108">Suurissa fyysisissä varastoissa eri käsittelytehtävät voi erotella osastojen mukaan ja niiden integrointia voi hallita ohjatun työnkulun avulla.</span><span class="sxs-lookup"><span data-stu-id="36c17-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="36c17-109">Yksinkertaisissa asennuksissa toiminta on epämuodollisempaa ja varastotoiminnot suoritetaan niin kutsuttuina varaston hyllytyksinä ja poimintoina.</span><span class="sxs-lookup"><span data-stu-id="36c17-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="36c17-110">Lisätietoja fyysisen varastoinnin perusmäärityksistä ja laajennetuista varastomäärityksistä on kohdassa [Rakennetiedot: Fyysisen varaston yleiskuvaus](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="36c17-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="36c17-111">Ennen varastotoimintojen suorittamista järjestelmään on määritettävä soveltuva fyysisen varastoinnin monimutkaisuustaso.</span><span class="sxs-lookup"><span data-stu-id="36c17-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="36c17-112">Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="36c17-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="36c17-113">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="36c17-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="36c17-114">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="36c17-114">**To**</span></span>|<span data-ttu-id="36c17-115">**Katso**</span><span class="sxs-lookup"><span data-stu-id="36c17-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="36c17-116">Kirjaa nimikkeiden vastaanotto fyysisissä varastosijainneissa joko pelkällä ostotilauksella (yksinkertaiset sijaintimääritykset) tai fyysisen varastoinnin vastaanottona, jos sijainnissa käytetään osittain tai kokonaan automatisoitua varastokäsittelyä.</span><span class="sxs-lookup"><span data-stu-id="36c17-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="36c17-117">Nimikkeiden vastaanottaminen</span><span class="sxs-lookup"><span data-stu-id="36c17-117">Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="36c17-118">Nopeuta nimikkeen siirtymistä vastaanotosta tai tuotannosta suoraan toimitukseen ohittamalla hyllytys- ja poimintakäsittelyt.</span><span class="sxs-lookup"><span data-stu-id="36c17-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="36c17-119">Nimikkeiden laiturointi</span><span class="sxs-lookup"><span data-stu-id="36c17-119">Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="36c17-120">Hyllytä ostoista, myyntipalautuksista, siirroista tai tuotannon tuotoksesta vastaanotettuja nimikkeitä määritetyn varastokäsittelyn mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="36c17-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="36c17-121">Nimikkeiden hyllyttäminen</span><span class="sxs-lookup"><span data-stu-id="36c17-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="36c17-122">Siirrä nimikkeitä fyysisen varaston varastopaikkojen välillä.</span><span class="sxs-lookup"><span data-stu-id="36c17-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="36c17-123">Nimikkeiden siirtäminen</span><span class="sxs-lookup"><span data-stu-id="36c17-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="36c17-124">Poimi toimitettavia, siirrettäviä tai kokoonpanossa tai tuotannossa kulutettavia nimikkeitä määritetyn varastokäsittelyn mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="36c17-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="36c17-125">Nimikkeiden poiminta</span><span class="sxs-lookup"><span data-stu-id="36c17-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="36c17-126">Kirjaa nimikkeiden toimitus fyysisistä varastosijainneista joko pelkällä myyntitilauksella (yksinkertaiset sijaintimääritykset) tai fyysisen varastoinnin toimituksena, jos sijainnissa käytetään osittain tai kokonaan automatisoitua varastokäsittelyä.</span><span class="sxs-lookup"><span data-stu-id="36c17-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="36c17-127">Nimikkeiden lähettäminen</span><span class="sxs-lookup"><span data-stu-id="36c17-127">Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="36c17-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="36c17-128">See Also</span></span>  
[<span data-ttu-id="36c17-129">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="36c17-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="36c17-130">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="36c17-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="36c17-131">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="36c17-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="36c17-132">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="36c17-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="36c17-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="36c17-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

