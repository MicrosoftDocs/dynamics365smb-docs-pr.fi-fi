---
title: "Rakennetiedot – kysyntä ja tarjonta | Microsoft Docs"
description: "Kysyntä on yleinen termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta. Lisäksi ohjelma sallii teknisemmät kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 983fbb1a4ce652900185010800474b80350f193d
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="fe5dd-104">Rakennetiedot: kysyntä ja tarjonta</span><span class="sxs-lookup"><span data-stu-id="fe5dd-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="fe5dd-105">Kysyntä on yleinen termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="fe5dd-106">Lisäksi ohjelma sallii teknisemmät kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-106">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
 <span data-ttu-id="fe5dd-107">Tarjonta on yleinen termi, jota käytetään mille tahansa positiiviselle tai tulevalle määrälle, kuten varasto, ostot, kokoonpano, tuotanto tai tulevat siirrot.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="fe5dd-108">Lisäksi myyntipalautus voi myös kuvata tarjontaa.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-108">In addition, a sales return may also represent supply.</span></span>  
  
 <span data-ttu-id="fe5dd-109">Voit lajitella useita kysynnän ja tarjonnan lähteitä, kun suunnittelujärjestelmä järjestää ne kahdelle aikajanalle, joita kutsutaan varastoprofiileiksi.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="fe5dd-110">Yksi profiili sisältää kysyntätapahtumat ja toinen sisältää vastaavat tarjontatapahtumat.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="fe5dd-111">Kukin tapahtuma edustaa yhtä tilausverkon kokonaisuutta, kuten myyntitilausriviä, nimiketapahtumaa tai tuotantotilausriviä.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
 <span data-ttu-id="fe5dd-112">Kun varaston profiilit ladataan, erilaiset kysyntä- ja tarjontajoukot täsmäytetään listatut tavoitteet täyttävän tarjontasuunnitelman tuotoksen saamiseksi.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
 <span data-ttu-id="fe5dd-113">Suunnitteluparametrit ja varastotasot ovat muita kysynnän ja tarjonnan tyyppejä, jotka käyvät läpi integroidun täsmäytyksen varastonimikkeiden täydentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="fe5dd-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="fe5dd-114">Lisätietoja on kohdassa [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="fe5dd-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe5dd-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fe5dd-115">See Also</span></span>  
 <span data-ttu-id="fe5dd-116">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="fe5dd-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="fe5dd-117">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="fe5dd-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="fe5dd-118">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="fe5dd-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
