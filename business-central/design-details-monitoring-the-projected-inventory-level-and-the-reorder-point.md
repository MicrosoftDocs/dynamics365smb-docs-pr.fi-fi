---
title: Rakennetiedot – Arvioidun varastomäärän ja uusintatilauspisteen valvonta | Microsoft Docs
description: Lisätietoja tavasta, jolla varaston suunnittelu erottaa suunnitellun varaston ja suunnitellun saatavilla olevan varastomäärän.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3ae50295fd77de376ac25f2f2e267b765e5de58e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307010"
---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a><span data-ttu-id="40c6f-103">Rakennetiedot: arvioidun varastotason ja uusintatilauspisteen valvonta</span><span class="sxs-lookup"><span data-stu-id="40c6f-103">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>
<span data-ttu-id="40c6f-104">Varasto on tarjonnan tyyppi mutta varaston suunnittelussa suunnittelujärjestelmä erottaa kaksi varastotasoa:</span><span class="sxs-lookup"><span data-stu-id="40c6f-104">Inventory is a type of supply, but for inventory planning, the planning system distinguishes between two inventory levels:</span></span>  

* <span data-ttu-id="40c6f-105">Suunniteltu varasto</span><span class="sxs-lookup"><span data-stu-id="40c6f-105">Projected inventory</span></span>  
* <span data-ttu-id="40c6f-106">Oletettu saatavilla oleva varasto</span><span class="sxs-lookup"><span data-stu-id="40c6f-106">Projected available inventory</span></span>  

## <a name="projected-inventory"></a><span data-ttu-id="40c6f-107">Suunniteltu varasto</span><span class="sxs-lookup"><span data-stu-id="40c6f-107">Projected Inventory</span></span>  
<span data-ttu-id="40c6f-108">Aluksi arvioitu varasto on bruttovaraston määrä, mukaan lukien kysyntä ja tarjonta menneisyydessä vaikka sitä ei ole kirjattu, kun suunnitteluprosessi aloitetaan.</span><span class="sxs-lookup"><span data-stu-id="40c6f-108">Initially, projected inventory is the quantity of gross inventory, including supply and demand in the past even if not posted, when starting the planning process.</span></span> <span data-ttu-id="40c6f-109">Tulevaisuudessa tästä tulee liikkuva arvioitu varastotaso, jota ylläpidetään tulevan tarjonnan ja kysynnän bruttomäärillä, koska nämä tulevat mukaan ajan kuluessa (joko varattu tai muulla tavoin kohdistettu).</span><span class="sxs-lookup"><span data-stu-id="40c6f-109">In the future, this becomes a moving projected inventory level that is maintained by gross quantities from future supply and demand because those are introduced along the time line (whether reserved or in other ways allocated).</span></span>  

<span data-ttu-id="40c6f-110">Suunnittelujärjestelmä käyttää käsiteltyä varastoa tarkkailemaan jälkitilauspistettä ja määrittämään jälkitilausmäärän, kun käytetään jälkitilauksen maksimimäärätapaa.</span><span class="sxs-lookup"><span data-stu-id="40c6f-110">The projected inventory is used by the planning system to monitor the reorder point and to determine the reorder quantity when using the Maximum Qty. reordering policy.</span></span>  

## <a name="projected-available-inventory"></a><span data-ttu-id="40c6f-111">Oletettu saatavilla oleva varasto</span><span class="sxs-lookup"><span data-stu-id="40c6f-111">Projected Available Inventory</span></span>  
<span data-ttu-id="40c6f-112">Käsitelty käytettävissä oleva varasto on osa käsiteltyä varastoa, joka tiettyyn aikaan on käytettävissä täyttämään kysyntää.</span><span class="sxs-lookup"><span data-stu-id="40c6f-112">The projected available inventory is the part of the projected inventory that at a given point in time is available to fulfill demand.</span></span> <span data-ttu-id="40c6f-113">Suunnittelumoottori käyttää käsiteltyä käytettävissä olevaa varastoa, kun varmuusvaraston tasoa tarkkaillaan.</span><span class="sxs-lookup"><span data-stu-id="40c6f-113">The projected available inventory is used by the planning engine when monitoring the safety stock level.</span></span>  

<span data-ttu-id="40c6f-114">Suunnittelujärjestelmä käyttää käsiteltyä käytettävissä olevaa varastoa tarkkaillakseen varmuusvarastoa, koska varmuusvaraston täytyy aina olla käytettävissä palvelemaan odottamatonta kysyntää.</span><span class="sxs-lookup"><span data-stu-id="40c6f-114">The projected available inventory is used by the planning system to monitor the safety stock level, since the safety stock must always be available to serve unexpected demand.</span></span>  

## <a name="time-buckets"></a><span data-ttu-id="40c6f-115">Aikavälit</span><span class="sxs-lookup"><span data-stu-id="40c6f-115">Time Buckets</span></span>  
<span data-ttu-id="40c6f-116">Ennustetun varastosaldon tiukka hallinta on tärkeää lisätilauspisteen tunnistamiseksi sekä oikean tilausmäärän laskemiseksi, kun enimmäistilausmäärän sääntö on käytössä.</span><span class="sxs-lookup"><span data-stu-id="40c6f-116">Having a tight control of the projected inventory is crucial to detect when the reorder point is reached or crossed and to calculate the right order quantity when using the Maximum Qty. reordering policy.</span></span>  

<span data-ttu-id="40c6f-117">Kuten aiemmin mainittiin, arvioitu varastotaso lasketaan suunnittelujakson alussa.</span><span class="sxs-lookup"><span data-stu-id="40c6f-117">As stated earlier, the projected inventory level is calculated at the start of the planning period.</span></span> <span data-ttu-id="40c6f-118">Se on bruttotaso, joka ei huomioi varauksia ja vastaavia kohdistuksia.</span><span class="sxs-lookup"><span data-stu-id="40c6f-118">It is a gross level that does not consider reservations and similar allocations.</span></span> <span data-ttu-id="40c6f-119">Järjestelmä valvoo aikavälin koottuja muutoksia ja valvoo tätä varaston tasoa suunnitteluvaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="40c6f-119">To monitor this inventory level during the planning sequence, the system monitors the aggregated changes over a period of time, a time bucket.</span></span> <span data-ttu-id="40c6f-120">Järjestelmä varmistaa, että aikaväli on vähintään yksi päivä, koska se on kysyntä- tai tarjontatapahtuman tarkin aikayksikkö.</span><span class="sxs-lookup"><span data-stu-id="40c6f-120">The system ensures that the time bucket is at least one day since it is the most precise unit of time for a demand or supply event.</span></span>  

## <a name="determining-the-projected-inventory-level"></a><span data-ttu-id="40c6f-121">Arvioidun varastotason määrittäminen</span><span class="sxs-lookup"><span data-stu-id="40c6f-121">Determining the Projected Inventory Level</span></span>  
<span data-ttu-id="40c6f-122">Seuraava jakso kuvaa sitä, kuinka suunniteltu varaston taso määritellään:</span><span class="sxs-lookup"><span data-stu-id="40c6f-122">The following sequence describes how the projected inventory level is determined:</span></span>  

* <span data-ttu-id="40c6f-123">Kun tarjontatapahtuma, kuten ostotilaus, on kokonaan suunniteltu, se nostaa oletetun varaston arvoa eräpäivänä.</span><span class="sxs-lookup"><span data-stu-id="40c6f-123">When a supply event, such as a purchase order has been totally planned, it will increase the projected inventory on its due date.</span></span>  
* <span data-ttu-id="40c6f-124">Kokonaan täytetty kysyntätapahtuma ei vähennä oletetun varaston arvoa heti.</span><span class="sxs-lookup"><span data-stu-id="40c6f-124">When a demand event has been fully satisfied, it will not decrease the projected inventory right away.</span></span> <span data-ttu-id="40c6f-125">Sen sijaan se kirjaa vähennyksen muistutuksen, joka on sisäinen tietue, joka sisältää päivämäärän ja arvioituun varastoon lisättävän määrän.</span><span class="sxs-lookup"><span data-stu-id="40c6f-125">Instead, it posts a decrease reminder, which is an internal record that holds the date and quantity of the contribution to the projected inventory.</span></span>  
* <span data-ttu-id="40c6f-126">Kun seuraavaa tarjontatapahtumaa suunnitellaan ja se asetetaan aikajanalle, kirjatut vähennyksen muistutukset tutkitaan yksi kerrallaan tarjonnan suunniteltuun päivämäärään asti oletetun varaston päivityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="40c6f-126">When a subsequent supply event is planned and placed on the time line, the posted decrease reminders are investigated one by one up until the planned date of the supply while updating the projected inventory.</span></span> <span data-ttu-id="40c6f-127">Tämän prosessin aikana sisäisen noston lisätilaustaso voidaan saavuttaa tai ylittää.</span><span class="sxs-lookup"><span data-stu-id="40c6f-127">During this process, the reorder point level of the internal increase reminder may be reached or crossed.</span></span>  
* <span data-ttu-id="40c6f-128">Jos uusi toimitustilaus otetaan käyttöön, järjestelmä tarkistaa, onko se kirjoitettu ennen nykyistä tarjontaa.</span><span class="sxs-lookup"><span data-stu-id="40c6f-128">If a new supply order is introduced, the system checks if it is entered before the current supply.</span></span> <span data-ttu-id="40c6f-129">Jos se on, uudesta tarjonnasta tulee nykyinen tarjonta ja täsmäytys käynnistyy uudelleen.</span><span class="sxs-lookup"><span data-stu-id="40c6f-129">If it is, the new supply becomes current supply and the balancing procedure starts over.</span></span>  

<span data-ttu-id="40c6f-130">Seuraavassa esitetään graafinen kuvaus tästä periaatteesta:</span><span class="sxs-lookup"><span data-stu-id="40c6f-130">The following shows a graphical illustration of this principle:</span></span>  

<span data-ttu-id="40c6f-131">![Suunnitellun varastotason määrittäminen](media/nav_app_supply_planning_2_projected_inventory.png "Suunnitellun varastotason määrittäminen")</span><span class="sxs-lookup"><span data-stu-id="40c6f-131">![Determining the Projected Inventory Level](media/nav_app_supply_planning_2_projected_inventory.png "Determining the Projected Inventory Level")</span></span>  

1. <span data-ttu-id="40c6f-132">Määrän 4 tarjonta **Sa** (kiinteä) sulkee kysynnän **Da** määrällä -3.</span><span class="sxs-lookup"><span data-stu-id="40c6f-132">Supply **Sa** of 4 (fixed) closes Demand **Da** of -3.</span></span>  
2. <span data-ttu-id="40c6f-133">CloseDemand: Luo vähennyksen muistutus -3 (ei näkyvillä).</span><span class="sxs-lookup"><span data-stu-id="40c6f-133">CloseDemand: Create a decrease reminder of -3 (not shown).</span></span>  
3. <span data-ttu-id="40c6f-134">Tarjonta **Sa** on suljettu ylijäämällä 1 (kysyntää ei enää ole).</span><span class="sxs-lookup"><span data-stu-id="40c6f-134">Supply **Sa** is closed with a surplus of 1 (no more demand exists).</span></span>  

     <span data-ttu-id="40c6f-135">Tämä nostaa oletetun varaston tasoksi +4, kun taas oletetun **saatavilla** olevan varaston tasoksi tulee -1.</span><span class="sxs-lookup"><span data-stu-id="40c6f-135">This increases the projected inventory level to +4, while the projected **available** inventory becomes -1.</span></span>  

4. <span data-ttu-id="40c6f-136">Seuraava määrältään 2 tarjonta **Sb** (toinen tilaus) on jo asetettu aikajanalle.</span><span class="sxs-lookup"><span data-stu-id="40c6f-136">The next supply **Sb** of 2 (another order) has already been placed on the timeline.</span></span>  
5. <span data-ttu-id="40c6f-137">Järjestelmä tarkistaa, onko mitään vähenemismuistutusta ennen **Sb:tä** (ei ole, joten mitään toimintoa ei suoriteta).</span><span class="sxs-lookup"><span data-stu-id="40c6f-137">System checks if there is any decrease reminder preceding **Sb** (there is not, so no action is taken).</span></span>  
6. <span data-ttu-id="40c6f-138">Järjestelmä sulkee tarjonnan **Sb** (kysyntää ei enää ole) – joko A: vähentämällä sen nollaan (peruutus) tai B: jättämällä sen ennalleen.</span><span class="sxs-lookup"><span data-stu-id="40c6f-138">System closes supply **Sb** (no more demand exists)—either A: by reducing it to 0 (cancel) or B: by leaving as is.</span></span>  

     <span data-ttu-id="40c6f-139">Tämä kasvattaa ennustettua varastosaldoa (A: +0 => +4 tai B: +2 = +6).</span><span class="sxs-lookup"><span data-stu-id="40c6f-139">This increases the projected inventory level (A: +0 => +4 or B: +2 = +6).</span></span>  

7. <span data-ttu-id="40c6f-140">Järjestelmä tekee lopullisen tarkastuksen: onko mitään vähenemismuistutusta?</span><span class="sxs-lookup"><span data-stu-id="40c6f-140">System makes a final check: Is there any decrease reminder?</span></span> <span data-ttu-id="40c6f-141">Kyllä, löytyy yksi päivämääränä **Da**.</span><span class="sxs-lookup"><span data-stu-id="40c6f-141">Yes, there is one on the date of **Da**.</span></span>  
8. <span data-ttu-id="40c6f-142">Järjestelmä lisää muistutuslaskun (-3) ennustettuun varastosaldoon, joko A: +4 -3 = 1 tai B: +6 -3 = +3.</span><span class="sxs-lookup"><span data-stu-id="40c6f-142">System adds the decrease reminder of -3 reminder to the projected inventory level, either A: +4 -3 = 1 or B: +6 -3 = +3.</span></span>  
9. <span data-ttu-id="40c6f-143">Tapauksessa A järjestelmä luo tulevaisuuteen aikataulutetun tilauksen aloituspäivämäärällä **Da**.</span><span class="sxs-lookup"><span data-stu-id="40c6f-143">In case of A, the system creates a forward-scheduled order starting on date **Da**.</span></span>  

     <span data-ttu-id="40c6f-144">Tapauksessa B lisätilauspiste on saavutettu ja uusi tilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="40c6f-144">In case of B, the reorder point is reached and a new order is created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="40c6f-145">Katso myös</span><span class="sxs-lookup"><span data-stu-id="40c6f-145">See Also</span></span>  
<span data-ttu-id="40c6f-146">[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="40c6f-146">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="40c6f-147">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="40c6f-147">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="40c6f-148">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="40c6f-148">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="40c6f-149">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="40c6f-149">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
