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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ea9974a8fb63d4e119cdc8b78930fd94777e6a38
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749566"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="42bf7-103">Rakennetiedot: f. varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="42bf7-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="42bf7-104">Tässä dokumentaatiossa on yleiskuvaus [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman varastoinninhallinnan toiminnoissa käytettävistä konsepteista ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="42bf7-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="42bf7-105">Se kuvaa keskeisten varastointitoimintojen taustalla olevan rakenteen ja miten varastointi integroituu muiden tarjontaketjun ominaisuuksien kanssa.</span><span class="sxs-lookup"><span data-stu-id="42bf7-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="42bf7-106">Varastoinnin eri monimutkaisuustasojen erottamista varten tämä ohjeistus on jaettu kahteen yleiseen ryhmään; toinen on Fyysisen varastoinnin perusmääritykset ja toinen Laajennetut varastomääritykset.</span><span class="sxs-lookup"><span data-stu-id="42bf7-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="42bf7-107">Tämä yksinkertainen erottaminen kattaa tuoteosion ja sijainnin asetusten määrittämät monimutkaisuuden eri tasot.</span><span class="sxs-lookup"><span data-stu-id="42bf7-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="42bf7-108">Katso lisätietoja kohdasta [Rakennetiedot: f. varaston asetus](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="42bf7-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="42bf7-109">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="42bf7-109">In This Section</span></span>  
[<span data-ttu-id="42bf7-110">Rakennetiedot: f. varaston yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="42bf7-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="42bf7-111">Rakennetiedot: f. varaston asetus</span><span class="sxs-lookup"><span data-stu-id="42bf7-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="42bf7-112">Rakennetiedot: saapuvan fyysisen varastoinnin virta</span><span class="sxs-lookup"><span data-stu-id="42bf7-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="42bf7-113">Rakennetiedot: sisäisen fyysisen varastoinnin virta</span><span class="sxs-lookup"><span data-stu-id="42bf7-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="42bf7-114">Rakennetiedot: saatavuus varastossa</span><span class="sxs-lookup"><span data-stu-id="42bf7-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="42bf7-115">Rakennetiedot: lähtevän fyysisen varastoinnin virta</span><span class="sxs-lookup"><span data-stu-id="42bf7-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="42bf7-116">Rakennetiedot: integrointi varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="42bf7-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
