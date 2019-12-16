---
title: Tietoja suunnittelutoiminnoista | Microsoft Docs
description: Suunnittelujärjestelmä ottaa kaikki kysyntä- ja tarjontatiedot huomioon, nettouttaa tulokset ja luo ehdotuksia, joita noudattamalla tarjonta ja kysyntä voidaan saattaa tasapainoon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 03ac7e30e65912a5f09d617b87c09a7b15c4f9c5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878093"
---
# <a name="about-planning-functionality"></a><span data-ttu-id="70f85-103">Tietoja toimintojen suunnittelusta</span><span class="sxs-lookup"><span data-stu-id="70f85-103">About Planning Functionality</span></span>
<span data-ttu-id="70f85-104">Suunnittelujärjestelmä ottaa kaikki kysyntä- ja tarjontatiedot huomioon, nettouttaa tulokset ja luo ehdotuksia, joita noudattamalla tarjonta ja kysyntä voidaan saattaa tasapainoon.</span><span class="sxs-lookup"><span data-stu-id="70f85-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="70f85-105">Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Toimitusten suunnittelu](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="70f85-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="70f85-106">Saat lisätietoja kaikkien tässä ohjeaiheessa mainittujen kenttien toiminnoista lukemalla työkaluvihjeen.</span><span class="sxs-lookup"><span data-stu-id="70f85-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="70f85-107">Kysyntä ja tarjonta</span><span class="sxs-lookup"><span data-stu-id="70f85-107">Demand and Supply</span></span>  
<span data-ttu-id="70f85-108">Suunnittelu koostuu kahdesta osasta, jotka ovat kysyntä ja tarjonta.</span><span class="sxs-lookup"><span data-stu-id="70f85-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="70f85-109">Ne täytyy pitää tasapainossa, jotta kysyntään voidaan varmasti vastata taloudellisesti ja ajallaan.</span><span class="sxs-lookup"><span data-stu-id="70f85-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="70f85-110">Kysyntä on yleinen termi, jota käytetään kaikenlaista bruttotarpeesta, esimerkiksi myyntitilauksesta, huoltotilauksesta, kokoonpano- tai tuotantotilausten osatarpeesta, lähtevästä siirrosta, puitetilauksesta tai ennusteesta.</span><span class="sxs-lookup"><span data-stu-id="70f85-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="70f85-111">Näiden lisäksi sovellus sallii myös tiettyjen muiden teknisten kysyntätyyppien käyttämisen. Tällaisia tarpeita ovat esimerkiksi negatiivinen tuotanto- tai ostotilaus, negatiivinen varasto ja ostopalautustilaus.</span><span class="sxs-lookup"><span data-stu-id="70f85-111">In addition to these, application allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="70f85-112">Tarjonta on yleiskäsite mille tahansa täydennykselle, esimerkiksi varastosaldolle, ostotilauksille, kokoonpanotilauksille, tuotantotilauksille tai saapuvalle siirrolle.</span><span class="sxs-lookup"><span data-stu-id="70f85-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="70f85-113">Vastaavalla tavalla voi olla negatiivinen myynti tai huoltotilaus, negatiivinen osatarve tai myyntipalautus – jotka jollakin tavoin edustavat myös tarjontaa.</span><span class="sxs-lookup"><span data-stu-id="70f85-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="70f85-114">Suunnittelujärjestelmän toinen tavoite on varmistaa, että varasto ei kasva tarpeettoman suureksi.</span><span class="sxs-lookup"><span data-stu-id="70f85-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="70f85-115">Jos kysyntä vähenee, suunnittelujärjestelmä ehdottaa tehtyjen täydennystilausten lykkäämistä, pienentämistä tai peruuttamista.</span><span class="sxs-lookup"><span data-stu-id="70f85-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="70f85-116">Suunnittelulaskenta</span><span class="sxs-lookup"><span data-stu-id="70f85-116">Planning Calculation</span></span>  
<span data-ttu-id="70f85-117">Suunnittelujärjestelmän perustana ovat arvioitu ja todellinen asiakaskysyntä sekä varaston uusintatilausten parametrit.</span><span class="sxs-lookup"><span data-stu-id="70f85-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="70f85-118">Kun suunnitelma lasketaan, sovellus ehdottaa tiettyjä toimenpiteitä (toimenpideviestit), jotka liittyvät alihankkijatäydennyksiin, varastojen välisiin siirtoihin tai tuotantoon.</span><span class="sxs-lookup"><span data-stu-id="70f85-118">Running the planning calculation will result in application suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="70f85-119">Jos täydennystilauksia on jo tehty, ehdotettuja toimenpiteitä voivat olla tilausten lisääminen tai vauhdittaminen muuttuneen kysynnän mukaisiksi.</span><span class="sxs-lookup"><span data-stu-id="70f85-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="70f85-120">Suunnitteluohjelma perustuu brutto-netto-laskutoimituksiin.</span><span class="sxs-lookup"><span data-stu-id="70f85-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="70f85-121">Suunnitellut tilausvapautukset perustuvat nettovaatimuksiin, ja ne ajoitetaan reititystietojen (valmistettujen nimikkeiden) perusteella tai nimikkeen kortin toimitusajan (ostonimikkeiden) perusteella.</span><span class="sxs-lookup"><span data-stu-id="70f85-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="70f85-122">Suunniteltujen tilausvapautusten määrät perustuvat suunnittelulaskentaan, ja tilanvapautuksiin vaikuttavat yksittäisissä nimikkeiden korteissa määritettävät parametrit.</span><span class="sxs-lookup"><span data-stu-id="70f85-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="70f85-123">Suunnittelu manuaalisia siirtotilauksia käyttäen.</span><span class="sxs-lookup"><span data-stu-id="70f85-123">Planning with Manual Transfer Orders</span></span>
<span data-ttu-id="70f85-124">Kuten Var. yks. -kortin **Täydennysjärjestelmä**-kentässä näkyy, suunnittelujärjestelmän voi määrittää luomaan siirtotilauksia, jotka tasapainottavat eri sijaintien kysyntää ja tarjontaa.</span><span class="sxs-lookup"><span data-stu-id="70f85-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="70f85-125">Automaattisten siirtotilausten lisäksi voit tarvittaessa siirtää varastoeriä sijainnista toiseen myös kysynnästä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="70f85-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="70f85-126">Luo tällöin siirtotilaus siirrettävällä määrälle manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="70f85-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="70f85-127">Voit estää suunnittelujärjestelmää puuttumasta manuaaliseen siirtotilaukseen määrittämällä siirtorivien **Suunnittelun joustavuus** -kentän arvoksi Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="70f85-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="70f85-128">Jos sen sijaan haluat, että suunnittelujärjestelmä muuttaa siirtotilauksen määriä ja päivämääriä kysynnän mukaan, määritä **Suunnittelun joustavuus** -kentän arvoksi oletusarvo Rajaton.</span><span class="sxs-lookup"><span data-stu-id="70f85-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="70f85-129">Suunnittelun parametrit</span><span class="sxs-lookup"><span data-stu-id="70f85-129">Planning Parameters</span></span>  
<span data-ttu-id="70f85-130">Suunnittelun parametreilla ohjataan sitä, milloin, miten ja kuinka paljon täydennyksiä nimikkeen kortin asetusten (eli varastointiyksikön) ja tuotannon asetusten perusteella tehdään.</span><span class="sxs-lookup"><span data-stu-id="70f85-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="70f85-131">Nimikkeen tai varastointiyksikön korteissa on käytettävissä seuraavat suunnitteluparametrit:</span><span class="sxs-lookup"><span data-stu-id="70f85-131">The following planning parameters exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="70f85-132">Puskuriaika</span><span class="sxs-lookup"><span data-stu-id="70f85-132">Dampener Period</span></span>  
-   <span data-ttu-id="70f85-133">Puskurimäärä</span><span class="sxs-lookup"><span data-stu-id="70f85-133">Dampener Quantity</span></span>  
-   <span data-ttu-id="70f85-134">Uusintatilaustapa</span><span class="sxs-lookup"><span data-stu-id="70f85-134">Reordering Policy</span></span>  
-   <span data-ttu-id="70f85-135">Uusintatilauspiste</span><span class="sxs-lookup"><span data-stu-id="70f85-135">Reorder Point</span></span>
-   <span data-ttu-id="70f85-136">Enimmäisvarasto</span><span class="sxs-lookup"><span data-stu-id="70f85-136">Maximum Inventory</span></span>  
-   <span data-ttu-id="70f85-137">Sallittu ylitys</span><span class="sxs-lookup"><span data-stu-id="70f85-137">Overflow Level</span></span>  
-   <span data-ttu-id="70f85-138">Aikaväli</span><span class="sxs-lookup"><span data-stu-id="70f85-138">Time Bucket</span></span>  
-   <span data-ttu-id="70f85-139">Erän koontijakso</span><span class="sxs-lookup"><span data-stu-id="70f85-139">Lot Accumulation Period</span></span>  
-   <span data-ttu-id="70f85-140">Uudelleenajoitusjakso</span><span class="sxs-lookup"><span data-stu-id="70f85-140">Rescheduling Period</span></span>  
-   <span data-ttu-id="70f85-141">Uusintatilausmäärä</span><span class="sxs-lookup"><span data-stu-id="70f85-141">Reorder Quantity</span></span>  
-   <span data-ttu-id="70f85-142">Toimitusajan varmistus</span><span class="sxs-lookup"><span data-stu-id="70f85-142">Safety Lead Time</span></span>  
-   <span data-ttu-id="70f85-143">Varmuusvaraston määrä</span><span class="sxs-lookup"><span data-stu-id="70f85-143">Safety Stock Quantity</span></span>  
-   <span data-ttu-id="70f85-144">Kokoonpanokäytäntö</span><span class="sxs-lookup"><span data-stu-id="70f85-144">Assembly Policy</span></span>  
-   <span data-ttu-id="70f85-145">Tuotantotapa</span><span class="sxs-lookup"><span data-stu-id="70f85-145">Manufacturing Policy</span></span>  

<span data-ttu-id="70f85-146">Nimikkeen tai varastointiyksikön korteissa on käytettävissä seuraavat tilausmääritteet:</span><span class="sxs-lookup"><span data-stu-id="70f85-146">The following order modifiers exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="70f85-147">Vähimmäistilausmäärä</span><span class="sxs-lookup"><span data-stu-id="70f85-147">Minimum Order Quantity</span></span>  
-   <span data-ttu-id="70f85-148">Enimmäistilausmäärä</span><span class="sxs-lookup"><span data-stu-id="70f85-148">Maximum Order Quantity</span></span>  
-   <span data-ttu-id="70f85-149">Tilauskerrannainen</span><span class="sxs-lookup"><span data-stu-id="70f85-149">Order Multiple</span></span>  

<span data-ttu-id="70f85-150">**Tuotannon asetukset** -sivun yleiset suunnitteluasetukset sisältävät seuraavat kohdat:</span><span class="sxs-lookup"><span data-stu-id="70f85-150">Global planning setup fields on the **Manufacturing Setup** page include:</span></span>  

-   <span data-ttu-id="70f85-151">Dynaaminen alatason koodi</span><span class="sxs-lookup"><span data-stu-id="70f85-151">Dynamic Low-Level Code</span></span>  
-   <span data-ttu-id="70f85-152">Nykyinen kysyntäennuste</span><span class="sxs-lookup"><span data-stu-id="70f85-152">Current Demand Forecast</span></span>  
-   <span data-ttu-id="70f85-153">Käytä ennustetta sijainneissa</span><span class="sxs-lookup"><span data-stu-id="70f85-153">Use Forecast on Locations</span></span>  
-   <span data-ttu-id="70f85-154">Oletus toimitusajan varmistus</span><span class="sxs-lookup"><span data-stu-id="70f85-154">Default Safety Lead Time</span></span>  
-   <span data-ttu-id="70f85-155">Tyhjä ylivuototaso</span><span class="sxs-lookup"><span data-stu-id="70f85-155">Blank Overflow Level</span></span>  
-   <span data-ttu-id="70f85-156">Yhdistetty tuot-ohj/tarvelask.</span><span class="sxs-lookup"><span data-stu-id="70f85-156">Combined MPS/MRP Calculation</span></span>   
-   <span data-ttu-id="70f85-157">Komponentit sijainnissa</span><span class="sxs-lookup"><span data-stu-id="70f85-157">Components at Location</span></span>  
-   <span data-ttu-id="70f85-158">Oletusvaimentimen jakso</span><span class="sxs-lookup"><span data-stu-id="70f85-158">Default Dampener Period</span></span>  
-   <span data-ttu-id="70f85-159">Oletuspuskurimäärä</span><span class="sxs-lookup"><span data-stu-id="70f85-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="70f85-160">Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Suunnittelun parametrit](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="70f85-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="70f85-161">Muut tärkeät suunnittelukentät</span><span class="sxs-lookup"><span data-stu-id="70f85-161">Other Important Planning Fields</span></span>
### <a name="planning-flexibility"></a><span data-ttu-id="70f85-162">Suunnittelun joustavuus</span><span class="sxs-lookup"><span data-stu-id="70f85-162">Planning Flexibility</span></span>
<span data-ttu-id="70f85-163">Voit valita useimpien toimitustilausten, kuten tuotantotilausten, riveillä **Suunnittelun juostavuus** -kentässä **Rajoittaminen** tai **Mitään**.</span><span class="sxs-lookup"><span data-stu-id="70f85-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="70f85-164">Näin määritetään, ottaako suunnittelujärjestelmä tuotantotilausrivin osoittaman tarjonnan huomioon toimenpideviestejä laskettaessa.</span><span class="sxs-lookup"><span data-stu-id="70f85-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="70f85-165">Jos kentässä on valittu **Rajaton**, suunnittelujärjestelmä sisällyttää rivin laskiessaan toimenpideviestejä.</span><span class="sxs-lookup"><span data-stu-id="70f85-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="70f85-166">Jos kentässä on valittu **Ei mitään**, rivi on pysyvä, eikä sitä voi muuttaa. Suunnittelujärjestelmä ei sisällytä sitä toimenpideviestien laskentaan.</span><span class="sxs-lookup"><span data-stu-id="70f85-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="70f85-167">Varoitus</span><span class="sxs-lookup"><span data-stu-id="70f85-167">Warning</span></span>
<span data-ttu-id="70f85-168">**Suunnittelutyökirja**-sivun **Varoitus**-tietokenttä ilmoittaa poikkeuksellista tilannetta varten luodusta suunnittelurivistä tekstillä, josta käyttäjä voi lukea lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="70f85-168">The **Warning** information field on the **Planning Worksheet** page informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="70f85-169">Varoitustyyppejä on kolme:</span><span class="sxs-lookup"><span data-stu-id="70f85-169">The following warning types exist:</span></span>

- <span data-ttu-id="70f85-170">Hätä</span><span class="sxs-lookup"><span data-stu-id="70f85-170">Emergency</span></span>
- <span data-ttu-id="70f85-171">Poikkeus</span><span class="sxs-lookup"><span data-stu-id="70f85-171">Exception</span></span>
- <span data-ttu-id="70f85-172">Huomautus</span><span class="sxs-lookup"><span data-stu-id="70f85-172">Attention</span></span>
- <span data-ttu-id="70f85-173">Hätä</span><span class="sxs-lookup"><span data-stu-id="70f85-173">Emergency</span></span>

<span data-ttu-id="70f85-174">Hätä-varoitus tulee näkyviin kahdessa tilanteessa:</span><span class="sxs-lookup"><span data-stu-id="70f85-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="70f85-175">Varasto on negatiivinen suunnittelun aloituspäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="70f85-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="70f85-176">Nykyhetkeä aikaisempia tarjonta- tai kysyntätapahtumia on olemassa.</span><span class="sxs-lookup"><span data-stu-id="70f85-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="70f85-177">Jos nimikkeen varasto on negatiivinen suunnittelun aloituspäivämääränä, suunnittelujärjestelmä ehdottaa negatiiviselle määrälle hätätoimitustilausta, joka saapuu suunnittelun aloituspäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="70f85-177">If an item’s inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="70f85-178">Varoitustekstissä kerrotaan aloituspäivämäärä ja hätätilauksen määrä.</span><span class="sxs-lookup"><span data-stu-id="70f85-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="70f85-179">Jos asiakirjassa on rivejä, joiden eräpäivä on ennen suunnittelun aloituspäivämäärää, rivit yhdistetään yhdeksi hätätoimitustilaukseksi, jotta nimike saapuisi suunnittelun aloituspäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="70f85-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="70f85-180">Poikkeus</span><span class="sxs-lookup"><span data-stu-id="70f85-180">Exception</span></span>
<span data-ttu-id="70f85-181">Poikkeus-varoitus näytetään, jos oletettu saatavilla oleva varasto pienenee varmuusvaraston määrää pienemmäksi.</span><span class="sxs-lookup"><span data-stu-id="70f85-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="70f85-182">Suunnittelujärjestelmä ehdottaa toimitustilausta, joka täyttää kysynnän eräpäivänä.</span><span class="sxs-lookup"><span data-stu-id="70f85-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="70f85-183">Varoitustekstissä kerrotaan nimikkeen varmuusvaraston määrä ja päivämäärä, jolloin se vähenee liian pieneksi.</span><span class="sxs-lookup"><span data-stu-id="70f85-183">The warning text states the item’s safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="70f85-184">Varmuusvaraston tason alittaminen aiheuttaa poikkeuksen, koska näin ei pitäisi käydä, jos uusintatilauspiste on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="70f85-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="70f85-185">Tarjontaa suunnitteluriveillä, joilla on poikkeusvaroituksia, ei yleensä muokata suunnitteluparametrien mukaan.</span><span class="sxs-lookup"><span data-stu-id="70f85-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="70f85-186">Suunnittelujärjestelmä ehdottaa sen sijaan vain toimitusmäärää, joka kattaa kysyntämäärän täsmällisesti.</span><span class="sxs-lookup"><span data-stu-id="70f85-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="70f85-187">Voit kuitenkin määrittää suunnittelun noudattamaan tiettyjä suunnittelurivien suunnitteluparametreja, joihin liittyy tiettyjä varoituksia.</span><span class="sxs-lookup"><span data-stu-id="70f85-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="70f85-188">Lisätietoja on kohdassa Noudata suunnitteluparametreja poikkeusvaroituksille Laske suunn. - Suunn.</span><span class="sxs-lookup"><span data-stu-id="70f85-188">For more information, see “Respect Planning Parameters for Exception Warnings” in Calculate Plan - Plan.</span></span> <span data-ttu-id="70f85-189">työk. -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="70f85-189">Wksh.</span></span>

### <a name="attention"></a><span data-ttu-id="70f85-190">Huomautus</span><span class="sxs-lookup"><span data-stu-id="70f85-190">Attention</span></span>
<span data-ttu-id="70f85-191">Huomautus-varoitus tulee näkyviin kahdessa tilanteessa:</span><span class="sxs-lookup"><span data-stu-id="70f85-191">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="70f85-192">Suunnittelun aloituspäivämäärä on varhaisempi kuin käsittelypäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="70f85-192">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="70f85-193">Suunnittelurivi ehdottaa vapautetun osto- tai tuotantotilauksen muuttamista.</span><span class="sxs-lookup"><span data-stu-id="70f85-193">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="70f85-194">Suunnitteluriveillä, joilla on varoituksia, ei valita **Hyväksy toimenpideviesti** -kenttää, koska suunnitteluohjelman oletetaan tutkivan tarkemmin näitä rivejä ennen suunnitelman toteutusta.</span><span class="sxs-lookup"><span data-stu-id="70f85-194">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="see-also"></a><span data-ttu-id="70f85-195">Katso myös</span><span class="sxs-lookup"><span data-stu-id="70f85-195">See Also</span></span>  
[<span data-ttu-id="70f85-196">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="70f85-196">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
<span data-ttu-id="70f85-197">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="70f85-197">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="70f85-198">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="70f85-198">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="70f85-199">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="70f85-199">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="70f85-200">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="70f85-200">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="70f85-201">Osto</span><span class="sxs-lookup"><span data-stu-id="70f85-201">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="70f85-202">Asetukset - parhaat käytännöt: toimitusten suunnittelu</span><span class="sxs-lookup"><span data-stu-id="70f85-202">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="70f85-203">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="70f85-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
