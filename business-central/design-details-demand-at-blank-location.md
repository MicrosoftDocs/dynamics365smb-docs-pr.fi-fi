---
title: Rakennetiedot – kysyntä ja tarjonta | Microsoft Docs
description: Tässä ohjeaiheessa esitellään kysyntä-termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 8cf7ffe90ccaf32258b4a51fb12f93a8df8ba7eb
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796058"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="4a76d-103">Rakennetiedot: kysyntä ja tarjonta</span><span class="sxs-lookup"><span data-stu-id="4a76d-103">Design Details: Demand and Supply</span></span>
<span data-ttu-id="4a76d-104">Kysyntä on yleinen termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta.</span><span class="sxs-lookup"><span data-stu-id="4a76d-104">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="4a76d-105">Lisäksi ohjelma sallii teknisemmät kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset.</span><span class="sxs-lookup"><span data-stu-id="4a76d-105">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
<span data-ttu-id="4a76d-106">Tarjonta on yleinen termi, jota käytetään mille tahansa positiiviselle tai tulevalle määrälle, kuten varasto, ostot, kokoonpano, tuotanto tai tulevat siirrot.</span><span class="sxs-lookup"><span data-stu-id="4a76d-106">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="4a76d-107">Lisäksi myyntipalautus voi myös kuvata tarjontaa.</span><span class="sxs-lookup"><span data-stu-id="4a76d-107">In addition, a sales return may also represent supply.</span></span>  
  
<span data-ttu-id="4a76d-108">Voit lajitella useita kysynnän ja tarjonnan lähteitä, kun suunnittelujärjestelmä järjestää ne kahdelle aikajanalle, joita kutsutaan varastoprofiileiksi.</span><span class="sxs-lookup"><span data-stu-id="4a76d-108">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="4a76d-109">Yksi profiili sisältää kysyntätapahtumat ja toinen sisältää vastaavat tarjontatapahtumat.</span><span class="sxs-lookup"><span data-stu-id="4a76d-109">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="4a76d-110">Kukin tapahtuma edustaa yhtä tilausverkon kokonaisuutta, kuten myyntitilausriviä, nimiketapahtumaa tai tuotantotilausriviä.</span><span class="sxs-lookup"><span data-stu-id="4a76d-110">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
<span data-ttu-id="4a76d-111">Kun varaston profiilit ladataan, erilaiset kysyntä- ja tarjontajoukot täsmäytetään listatut tavoitteet täyttävän tarjontasuunnitelman tuotoksen saamiseksi.</span><span class="sxs-lookup"><span data-stu-id="4a76d-111">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
<span data-ttu-id="4a76d-112">Suunnitteluparametrit ja varastotasot ovat muita kysynnän ja tarjonnan tyyppejä, jotka käyvät läpi integroidun täsmäytyksen varastonimikkeiden täydentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="4a76d-112">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="4a76d-113">Lisätietoja on kohdassa [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="4a76d-113">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a76d-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4a76d-114">See Also</span></span>  
<span data-ttu-id="4a76d-115">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="4a76d-115">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="4a76d-116">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="4a76d-116">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="4a76d-117">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="4a76d-117">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)