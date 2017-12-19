---
title: Rakennetiedot | Microsoft Docs
description: "Tässä sisällössä on yksityiskohtaisia teknisiä tietoja Dynamics 365:n monimutkaisista ominaisuuksista."
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 385a9593da2149bea96fa314826f267640b2a2e0
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="design-details"></a><span data-ttu-id="e10af-103">Rakennetiedot</span><span class="sxs-lookup"><span data-stu-id="e10af-103">Design Details</span></span>
<span data-ttu-id="e10af-104">Tässä sisällössä on yksityiskohtaisia teknisiä tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] monimutkaisista ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="e10af-104">This content contains detailed technical information about complex application features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

 <span data-ttu-id="e10af-105">Rakennetietojen sisältö on tarkoitettu käyttöönottajille, kehittäjille ja pääkäyttäjille, jotka tarvitsevat kattavan näkemyksen kyseessä olevan ominaisuuden toteuttamisesta, mukauttamisesta tai määrittämisestä.</span><span class="sxs-lookup"><span data-stu-id="e10af-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="e10af-106">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="e10af-106">**To**</span></span>|<span data-ttu-id="e10af-107">**Katso**</span><span class="sxs-lookup"><span data-stu-id="e10af-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e10af-108">Katso lisätietoja dimensioiden tallennuksen ja kirjauksen suunnittelusta, kuten koodiesimerkkejä dimensiokoodien siirrosta ja päivityksestä.</span><span class="sxs-lookup"><span data-stu-id="e10af-108">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="e10af-109">Rakennetiedot: dimensioyhdistelmä-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="e10af-109">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)|  
|<span data-ttu-id="e10af-110">Lue kuinka suunnittelujärjestelmä toimii, ja kuinka algoritmeja voidaan muuttaa eri ympäristöjen suunnitteluvaatimuksia vastaaviksi.</span><span class="sxs-lookup"><span data-stu-id="e10af-110">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="e10af-111">Rakennetiedot: tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="e10af-111">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="e10af-112">Tietoja kustannuslaskentaohjelman mekanismeista, kuten arvostusmenetelmästä ja kustannusten muuttamisesta sekä niiden laskentaperiaatteista.</span><span class="sxs-lookup"><span data-stu-id="e10af-112">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="e10af-113">Rakennetiedot: varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="e10af-113">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="e10af-114">Lue lisää laajennetun varastoinnin ja perusvarastoinnin ominaisuuksien keskeisistä periaatteista ja kuinka ne integroituvat muiden toimitusketjun ominaisuuksien kanssa.</span><span class="sxs-lookup"><span data-stu-id="e10af-114">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="e10af-115">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="e10af-115">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="e10af-116">Lisätietoja nimikeseurannan historiallisesta ja nykyisestä rakenteesta, ja kuinka se integroituu varausjärjestelmään, ja sisällyttää sarja-/ eränumerot saatavuuslaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="e10af-116">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="e10af-117">Rakennetiedot: nimikkeen seuranta</span><span class="sxs-lookup"><span data-stu-id="e10af-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="e10af-118">Tietoja yleisen päiväkirjan kirjausrivi -ominaisuudesta, kuten viimeisimmät yksinkertaistukset koodiyksikkö 12:n suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="e10af-118">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="e10af-119">Rakenteen tiedot: Yleisen päiväkirjan kirjausrivi</span><span class="sxs-lookup"><span data-stu-id="e10af-119">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|  

## <a name="see-also"></a><span data-ttu-id="e10af-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e10af-120">See Also</span></span>  
 <span data-ttu-id="e10af-121">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="e10af-121">[Planning](production-planning.md) </span></span>  
 <span data-ttu-id="e10af-122">[Varaston kustannusten hallinta](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="e10af-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="e10af-123">[Varastoinninhallinta](warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="e10af-123">[Warehouse Management](warehouse-manage-warehouse.md) </span></span>  
 [<span data-ttu-id="e10af-124">Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla</span><span class="sxs-lookup"><span data-stu-id="e10af-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="e10af-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e10af-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

