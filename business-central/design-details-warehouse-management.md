---
title: Rakennetiedot – Fyysinen varastointi | Microsoft Docs
description: Tässä ohjeaiheessa on yleiskatsaus Business Central -sovelluksen varastoinninhallinnan ominaisuuksien rakenteesta, käsitteistä ja periaatteista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2f6a84e015ccfd625f3b902281bd8ec59150540f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "937007"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="7c1e8-103">Rakennetiedot: f. varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="7c1e8-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="7c1e8-104">Tässä dokumentaatiossa on yleiskuvaus [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman varastoinninhallinnan toiminnoissa käytettävistä konsepteista ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7c1e8-105">Se kuvaa keskeisten varastointitoimintojen taustalla olevan rakenteen ja miten varastointi integroituu muiden tarjontaketjun ominaisuuksien kanssa.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="7c1e8-106">Varastoinnin eri monimutkaisuustasojen erottamista varten tämä ohjeistus on jaettu kahteen yleiseen ryhmään; toinen on Fyysisen varastoinnin perusmääritykset ja toinen Laajennetut varastomääritykset.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="7c1e8-107">Tämä yksinkertainen erottaminen kattaa tuoteosion ja sijainnin asetusten määrittämät monimutkaisuuden eri tasot.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="7c1e8-108">Katso lisätietoja kohdasta [Rakennetiedot: f. varaston asetus](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="7c1e8-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="7c1e8-109">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="7c1e8-109">In This Section</span></span>  
[<span data-ttu-id="7c1e8-110">Rakennetiedot: f. varaston yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="7c1e8-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="7c1e8-111">Rakennetiedot: f. varaston asetus</span><span class="sxs-lookup"><span data-stu-id="7c1e8-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="7c1e8-112">Rakennetiedot: saapuvan fyysisen varastoinnin virta</span><span class="sxs-lookup"><span data-stu-id="7c1e8-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="7c1e8-113">Rakennetiedot: sisäisen fyysisen varastoinnin virta</span><span class="sxs-lookup"><span data-stu-id="7c1e8-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="7c1e8-114">Rakennetiedot: saatavuus varastossa</span><span class="sxs-lookup"><span data-stu-id="7c1e8-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="7c1e8-115">Rakennetiedot: lähtevän fyysisen varastoinnin virta</span><span class="sxs-lookup"><span data-stu-id="7c1e8-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="7c1e8-116">Rakennetiedot: integrointi varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="7c1e8-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
