---
title: Rakennetiedot – suunnittelun kohdistustaulukko | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, mitä tapahtuu, kun muutat nimikkeen suunnittelua.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b981fc2d234c2f8c32e0fe10daa1ce20f25bb4f8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922012"
---
# <a name="design-details-planning-assignment-table"></a><span data-ttu-id="af795-103">Rakennetiedot: suunnittelun kohdistustaulukko</span><span class="sxs-lookup"><span data-stu-id="af795-103">Design Details: Planning Assignment Table</span></span>
<span data-ttu-id="af795-104">Kaikki nimikkeet tulee suunnitella, mutta nimikkeelle ei ole syytä laskea suunnitelmaa ellei kysyntä- tai tarjontakuvio ole muuttunut edellisen suunnitelman laskemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="af795-104">All items should be planned for, however, there is no reason to calculate a plan for an item unless there has been a change in the demand or supply pattern since the last time a plan was calculated.</span></span>  

<span data-ttu-id="af795-105">Jos käyttäjä on kirjoittanut uuden myyntitilauksen tai muuttanut olemassa olevaa, suunnitelman uudelleen laskeminen on tarpeellista.</span><span class="sxs-lookup"><span data-stu-id="af795-105">If the user has entered a new sales order or changed an existing one, there is reason to recalculate the plan.</span></span> <span data-ttu-id="af795-106">Muita syitä ovat muutos ennusteeseen tai haluttu varmuusvaraston määrä.</span><span class="sxs-lookup"><span data-stu-id="af795-106">Other reasons include a change in forecast or the desired safety stock quantity.</span></span> <span data-ttu-id="af795-107">Tuoterakenteen muuttaminen komponentin lisäyksellä tai poistolla ilmaisisi todennäköisesti muutosta, mutta vain komponenttinimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="af795-107">Changing a bill of material by adding or removing a component would most likely indicate a change, but for the component item only.</span></span>  

<span data-ttu-id="af795-108">Useiden sijaintien kohdalla, määritys tapahtuu nimikkeen tasolla sijaintiyhdistelmää kohti.</span><span class="sxs-lookup"><span data-stu-id="af795-108">For multiple locations, the assignment takes place at the level of item per location combination.</span></span> <span data-ttu-id="af795-109">Jos esimerkiksi myyntitilaus on luotu vain yhdessä sijainnissa, sovellus määrittää suunnittelulle tässä tietyssä sijainnissa olevan nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="af795-109">If, for example, a sales order has been created at only one location, application will assign the item at that specific location for planning.</span></span>  

<span data-ttu-id="af795-110">Syy valita nimikkeitä suunnittelua varten on järjestelmän toimintaseikka.</span><span class="sxs-lookup"><span data-stu-id="af795-110">The reason for selecting items for planning is a matter of system performance.</span></span> <span data-ttu-id="af795-111">Jos nimikkeen kysyntä–tarjonta-mallissa ei ole tapahtunut muutosta, suunnittelujärjestelmä ei ehdota toimenpiteitä.</span><span class="sxs-lookup"><span data-stu-id="af795-111">If no change in an item’s demand-supply pattern has occurred, the planning system will not suggest any actions to be taken.</span></span> <span data-ttu-id="af795-112">Ilman suunnittelun tehtävää järjestelmän on suoritettava laskennat kaikille nimikkeille suunnitelmaa ja järjestelmän resurssit kuluttavaa tilannetta määritettäessä.</span><span class="sxs-lookup"><span data-stu-id="af795-112">Without the planning assignment, the system would have to perform the calculations for all items in order to find out what to plan for, and that would drain system resources.</span></span>  

<span data-ttu-id="af795-113">**Suunnittelun tehtävä**-taulukko valvoo kysynnän ja toimituksen tapahtumia ja määrittää sopivat nimikkeet suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="af795-113">The **Planning Assignment** table monitors demand and supply events and assigns the appropriate items for planning.</span></span> <span data-ttu-id="af795-114">Seuraavia tapahtumia tarkkaillaan:</span><span class="sxs-lookup"><span data-stu-id="af795-114">The following events are monitored:</span></span>  

* <span data-ttu-id="af795-115">Uusi myyntitilaus, ennuste, komponentti, ostotilaus, tuotantotilaus, kokoonpanotilaus tai siirtotilaus.</span><span class="sxs-lookup"><span data-stu-id="af795-115">A new sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="af795-116">Nimikkeen, määrän, sijainnin, variantin tai päivämäärän muutos myyntitilauksessa, ennusteessa, komponentissa, ostotilauksessa, tuotantotilauksessa, kokoonpanotilauksessa tai siirtotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="af795-116">Change of item, quantity, location, variant, or date on a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="af795-117">Myyntitilauksen, ennusteen, komponentin, ostotilauksen, tuotantotilauksen, kokoonpanotilauksen tai siirtotilauksen peruutus.</span><span class="sxs-lookup"><span data-stu-id="af795-117">Cancellation of a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="af795-118">Muiden kuin suunniteltujen nimikkeiden kulutus.</span><span class="sxs-lookup"><span data-stu-id="af795-118">Consumption of items other than planned.</span></span>  
* <span data-ttu-id="af795-119">Muiden kuin suunniteltujen nimikkeiden tuotos.</span><span class="sxs-lookup"><span data-stu-id="af795-119">Output of items other than planned.</span></span>  
* <span data-ttu-id="af795-120">Varaston suunnittelemattomat muutokset.</span><span class="sxs-lookup"><span data-stu-id="af795-120">Unplanned changes in inventory.</span></span>  

<span data-ttu-id="af795-121">Näiden suorien tarjonta-kysyntä-siirtojen osalta tilausten seuranta- ja toimenpiteiden viestitysjärjestelmä ylläpitää Suunnittelun tehtävä -taulukkoa ja ilmoittaa suunnittelun syyn toimenpideviestinä.</span><span class="sxs-lookup"><span data-stu-id="af795-121">For these direct supply-demand displacements, the order tracking and action messaging system maintains the Planning Assignment table and states a planning reason as an action message.</span></span>  

<span data-ttu-id="af795-122">Seuraavat muutokset päätiedoissa voivat myös aiheuttaa suunnittelun epätasapainon:</span><span class="sxs-lookup"><span data-stu-id="af795-122">The following changes in master data can also cause a planning imbalance:</span></span>  

* <span data-ttu-id="af795-123">Tilan muutos hyväksytyksi tuotannon tuoterakenteen otsikossa (kaikille tätä otsikkoa käyttäville nimikkeille).</span><span class="sxs-lookup"><span data-stu-id="af795-123">Change of status to Certified in the production BOM header (for all items using that header).</span></span>  
* <span data-ttu-id="af795-124">Poistettu rivi (alinimike).</span><span class="sxs-lookup"><span data-stu-id="af795-124">Deleted line (child item).</span></span>  
* <span data-ttu-id="af795-125">Tilan muutos hyväksytyksi reitityksen otsikossa (kaikille tätä reititystä käyttäville nimikkeille).</span><span class="sxs-lookup"><span data-stu-id="af795-125">Change of status to Certified in the routing header (for all items using that routing).</span></span>  
* <span data-ttu-id="af795-126">Muutokset seuraavissa nimikkeen kortin kentissä.</span><span class="sxs-lookup"><span data-stu-id="af795-126">Changes in the following item card fields.</span></span>  
* <span data-ttu-id="af795-127">Varmuusvaraston määrä tai varmistuksen läpimenoaika</span><span class="sxs-lookup"><span data-stu-id="af795-127">Safety Stock Quantity or Safety Lead Time.</span></span>  
* <span data-ttu-id="af795-128">Toimitusajan laskenta.</span><span class="sxs-lookup"><span data-stu-id="af795-128">Lead Time Calculation.</span></span>  
* <span data-ttu-id="af795-129">Uusintatilauspiste.</span><span class="sxs-lookup"><span data-stu-id="af795-129">Reorder Point.</span></span>  
* <span data-ttu-id="af795-130">Tuotannon tuoterakenteen nro (ja kaikki vanhan tuoterakenteen viitteen alikohteet).</span><span class="sxs-lookup"><span data-stu-id="af795-130">Production BOM No. (and all children of old BOM reference).</span></span>  
* <span data-ttu-id="af795-131">Reititysnro</span><span class="sxs-lookup"><span data-stu-id="af795-131">Routing No.</span></span>  
* <span data-ttu-id="af795-132">Uusintatilauskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="af795-132">Reordering Policy.</span></span>  

<span data-ttu-id="af795-133">Näissä tapauksissa uusi suunnittelun määrityksen hallinta -toiminto ylläpitää taulukkoa ja määrittää suunnittelun syyksi nettomuutoksen.</span><span class="sxs-lookup"><span data-stu-id="af795-133">In these cases, a new function, Planning Assignment Management, maintains the table and states the planning reason as Net Change.</span></span>  

<span data-ttu-id="af795-134">Seuraavat muutokset eivät aiheuta suunnittelutehtävää:</span><span class="sxs-lookup"><span data-stu-id="af795-134">The following changes do not cause a planning assignment:</span></span>  

* <span data-ttu-id="af795-135">Kalenterit</span><span class="sxs-lookup"><span data-stu-id="af795-135">Calendars</span></span>  
* <span data-ttu-id="af795-136">Muut suunnitteluparametrit nimikkeen kortilla:</span><span class="sxs-lookup"><span data-stu-id="af795-136">Other planning parameters on the item card</span></span>  

<span data-ttu-id="af795-137">Tuotanto-ohjelman ja tarvelaskennan laskentaa koskevat seuraavat rajoitukset:</span><span class="sxs-lookup"><span data-stu-id="af795-137">When calculating an MPS or an MRP, the following restrictions apply:</span></span>  

* <span data-ttu-id="af795-138">Tuotanto-ohjelma: suunnittelujärjestelmä tarkistaa, että nimikkeellä on kysyntäennuste tai myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="af795-138">MPS: The planning system checks that the item carries a demand forecast or a sales order.</span></span> <span data-ttu-id="af795-139">Jos ei ole, nimike ei kuulu suunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="af795-139">If not, the item is not included in the plan.</span></span>  
* <span data-ttu-id="af795-140">Tarvelaskenta: jos suunnittelujärjestelmä havaitsee, että tuotanto-ohjelman suunnittelurivi tai tuotanto-ohjelman toimitustilaus täydentää nimikettä, nimike jätetään pois suunnittelusta.</span><span class="sxs-lookup"><span data-stu-id="af795-140">MRP: If the planning system detects that the item is being replenished by an MPS planning line or MPS supply order, the item will be left out of the planning.</span></span> <span data-ttu-id="af795-141">Kaikki kysyntä asiaankuuluvista osista on kuitenkin mukana.</span><span class="sxs-lookup"><span data-stu-id="af795-141">However, any demand from relevant components is included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af795-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="af795-142">See Also</span></span>  
<span data-ttu-id="af795-143">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="af795-143">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="af795-144">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="af795-144">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
<span data-ttu-id="af795-145">[Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md) </span><span class="sxs-lookup"><span data-stu-id="af795-145">[Design Details: Transfers in Planning](design-details-transfers-in-planning.md) </span></span>  
[<span data-ttu-id="af795-146">Rakennetiedot: suunnittelun parametrit</span><span class="sxs-lookup"><span data-stu-id="af795-146">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
