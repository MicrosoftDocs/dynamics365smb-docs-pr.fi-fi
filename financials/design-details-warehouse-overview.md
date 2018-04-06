---
title: "Rakennetiedot – Fyysisen varastoinnin yleiskatsaus | Microsoft Docs"
description: "Fyysisen varaston jokaisen tapahtuman ja siirron tiedot on voitava jäljittää, jotta nimikkeiden fyysistä käsittelyä voidaan tukea alue- ja varastopaikkatasolla. Tätä hallitaan **F. var. tapahtuma** -taulukossa. Jokainen tapahtuma tallennetaan varastorekisteriin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f5dc30ab398ae41ab8c36b6c207d2f48036cc98c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="9adee-105">Rakennetiedot: f. varaston yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="9adee-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="9adee-106">Fyysisen varaston jokaisen tapahtuman ja siirron tiedot on voitava jäljittää, jotta nimikkeiden fyysistä käsittelyä voidaan tukea alue- ja varastopaikkatasolla.</span><span class="sxs-lookup"><span data-stu-id="9adee-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="9adee-107">Tätä hallitaan **F. var. tapahtuma** -taulukossa.</span><span class="sxs-lookup"><span data-stu-id="9adee-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="9adee-108">Jokainen tapahtuma tallennetaan varastorekisteriin.</span><span class="sxs-lookup"><span data-stu-id="9adee-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="9adee-109">Fyysisen varastoinnin asiakirjoja ja fyysisen varastoinnin päiväkirjaa käytetään fyysisen varastoinnin nimikesiirtojen rekisteröimisessä.</span><span class="sxs-lookup"><span data-stu-id="9adee-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="9adee-110">Jokaisen f. varaston nimikkeen siirron, vastaanoton, hyllytyksen, poiminnan, toimituksen tai muutoksen yhteydessä tapahtumat rekisteröidään tallentamaan fyysiset tiedot vyöhykkeestä, lokerosta ja määrästä.</span><span class="sxs-lookup"><span data-stu-id="9adee-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span> <span data-ttu-id="9adee-111">Lisätietoja on kohdassa [Rakennetiedot: Saapuva fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="9adee-111">For more information, see [Design Details: Inbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="9adee-112">**Bin-tiedoston sisältö** -taulukkoa käytetään käsiteltäessä kaikkia eri sisältödimensioita bineissä nimikettä kohden, kuten mittayksikkö, maksimimäärä ja minimimäärä.</span><span class="sxs-lookup"><span data-stu-id="9adee-112">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="9adee-113">**Binin sisältö** -taulukko sisältää myös virtauskentät varastokirjauksiin, varaston ohjeisiin ja varaston lokiriveihin, mikä varmistaa sen, että nimikkeen saatavuus biniä kohden ja nimikkeen bin voidaan laskea nopeasti.</span><span class="sxs-lookup"><span data-stu-id="9adee-113">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="9adee-114">Lisätietoja on kohdassa [Rakennetiedot: Saatavuus varastossa.](design-details-availability-in-the-warehouse.md)</span><span class="sxs-lookup"><span data-stu-id="9adee-114">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="9adee-115">Kun nimikkeiden kirjaukset tapahtuvat fyysisen varastoinnin moduulin ulkopuolella, fyysisen varastoinnin tapahtumat ja varastotapahtumat synkronoidaan sijaintikohtaisten muutosten oletusvarastopaikan avulla.</span><span class="sxs-lookup"><span data-stu-id="9adee-115">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="9adee-116">Varaston fyysisen inventoinnin aikana kaikki määritetyt ja lasketut määrät tallennetaan muutoslokeroon ja kirjataan tämän jälkeen korjaavina nimiketapahtumina.</span><span class="sxs-lookup"><span data-stu-id="9adee-116">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="9adee-117">Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Integrointi varaston kanssa](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="9adee-117">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="9adee-118">Seuraavassa kuvassa on luonnosteltu tyypillinen varaston kulku.</span><span class="sxs-lookup"><span data-stu-id="9adee-118">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="9adee-119">![Varastointiprosessien yleiskatsaus](media/design_details_warehouse_management_overview.png "design_details_warehouse_management_overview")</span><span class="sxs-lookup"><span data-stu-id="9adee-119">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "design_details_warehouse_management_overview")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="9adee-120">Perus tai lisävarastointi</span><span class="sxs-lookup"><span data-stu-id="9adee-120">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="9adee-121">[!INCLUDE[d365fin](includes/d365fin_md.md)]in varastotoiminto voidaan toteuttaa yrityksen prosessien ja tilausmäärän mukaan valittavalla monimutkaisuustasolla.</span><span class="sxs-lookup"><span data-stu-id="9adee-121">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="9adee-122">Pääero on, että toiminnot suoritetaan tilaus tilaukselta perusvarastoinnissa, kun ne yhdistetään useisiin tilauksiin kehittyneessä varastoinnissa.</span><span class="sxs-lookup"><span data-stu-id="9adee-122">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="9adee-123">Eri monimutkaisuuden tasojen erottamista varten tässä dokumentaatiossa käsitellään kahta yleistä nimitystä: Perus ja Lisävarastointi.</span><span class="sxs-lookup"><span data-stu-id="9adee-123">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="9adee-124">Tämä yksinkertainen erottaminen kattaa tuoteosion ja sijainnin asetusten määrittämät monimutkaisuuden useat eri tasot, joita tukevat erilaiset käyttöliittymäasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="9adee-124">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="9adee-125">Katso lisätietoja kohdasta [Rakennetiedot: f. varaston asetus](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="9adee-125">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9adee-126">Varaston kehittyneintä tasoa kutsutaan tässä asiakirjassa nimellä "WMS-asennukset", koska tämä taso vaatii kehittyneimmän yksikön, Warehouse Management Systems.</span><span class="sxs-lookup"><span data-stu-id="9adee-126">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="9adee-127">Seuraavia eri käyttöliittymäasiakirjoja käytetään perus- ja kehittyneessä varastoinnissa.</span><span class="sxs-lookup"><span data-stu-id="9adee-127">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="9adee-128">Peruskäyttöliittymäasiakirjat</span><span class="sxs-lookup"><span data-stu-id="9adee-128">Basic UI Documents</span></span>  

-   <span data-ttu-id="9adee-129">**Varastohyllytys**</span><span class="sxs-lookup"><span data-stu-id="9adee-129">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="9adee-130">**Varaston poiminta**</span><span class="sxs-lookup"><span data-stu-id="9adee-130">**Inventory Pick**</span></span>  
-   <span data-ttu-id="9adee-131">**Varaston siirto**</span><span class="sxs-lookup"><span data-stu-id="9adee-131">**Inventory Movement**</span></span>  
-   <span data-ttu-id="9adee-132">**Nimikepäiväkirja**</span><span class="sxs-lookup"><span data-stu-id="9adee-132">**Item Journal**</span></span>  
-   <span data-ttu-id="9adee-133">**Nimikkeen uudelleenluokituspäiväkirja**</span><span class="sxs-lookup"><span data-stu-id="9adee-133">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="9adee-134">(Eri raportit)</span><span class="sxs-lookup"><span data-stu-id="9adee-134">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="9adee-135">Käyttöliittymän lisäasiakirjat</span><span class="sxs-lookup"><span data-stu-id="9adee-135">Advanced UI Documents</span></span>  

-   <span data-ttu-id="9adee-136">**F. varastoinnin vastaanotto**</span><span class="sxs-lookup"><span data-stu-id="9adee-136">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="9adee-137">**Hyllytystyökirja**</span><span class="sxs-lookup"><span data-stu-id="9adee-137">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="9adee-138">**F.varastoinnin hyllytys**</span><span class="sxs-lookup"><span data-stu-id="9adee-138">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="9adee-139">**Poimintatyökirja**</span><span class="sxs-lookup"><span data-stu-id="9adee-139">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="9adee-140">**F.varastoinnin poiminta**</span><span class="sxs-lookup"><span data-stu-id="9adee-140">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="9adee-141">**Siirtotyökirja**</span><span class="sxs-lookup"><span data-stu-id="9adee-141">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="9adee-142">**F. var. siirto**</span><span class="sxs-lookup"><span data-stu-id="9adee-142">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="9adee-143">**Sisäinen f.var. poim.**</span><span class="sxs-lookup"><span data-stu-id="9adee-143">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="9adee-144">**Sisäinen f.var. hyllytys**</span><span class="sxs-lookup"><span data-stu-id="9adee-144">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="9adee-145">**Var.paikan luontityökirja**</span><span class="sxs-lookup"><span data-stu-id="9adee-145">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="9adee-146">**Var.p. sisällön luontityökirja**</span><span class="sxs-lookup"><span data-stu-id="9adee-146">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="9adee-147">**F.var. nimikepvk**</span><span class="sxs-lookup"><span data-stu-id="9adee-147">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="9adee-148">**Var. nimik. uud.luok.pvk**</span><span class="sxs-lookup"><span data-stu-id="9adee-148">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="9adee-149">(Eri raportit)</span><span class="sxs-lookup"><span data-stu-id="9adee-149">(Various reports)</span></span>  

<span data-ttu-id="9adee-150">Katso lisätietoja jokaisesta asiakirjasta kunkin ikkunan aiheista.</span><span class="sxs-lookup"><span data-stu-id="9adee-150">For more information about each document, see the respective window topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="9adee-151">Termit</span><span class="sxs-lookup"><span data-stu-id="9adee-151">Terminology</span></span>  
<span data-ttu-id="9adee-152">[!INCLUDE[d365fin](includes/d365fin_md.md)]in fyysisen varastoinnin ohjeistus käyttää seuraavia ostojen ja myyntien talouskäsitteiden mukaisia varaston nimikevirran termejä.</span><span class="sxs-lookup"><span data-stu-id="9adee-152">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="9adee-153">Kausi</span><span class="sxs-lookup"><span data-stu-id="9adee-153">Term</span></span>|<span data-ttu-id="9adee-154">Description</span><span class="sxs-lookup"><span data-stu-id="9adee-154">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="9adee-155">Saapuva virta</span><span class="sxs-lookup"><span data-stu-id="9adee-155">Inbound flow</span></span>|<span data-ttu-id="9adee-156">Fyysisen varaston sijaintiin siirtyvät nimikkeet, kuten ostot ja saapuvat siirrot.</span><span class="sxs-lookup"><span data-stu-id="9adee-156">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="9adee-157">Sisäinen virta</span><span class="sxs-lookup"><span data-stu-id="9adee-157">Internal flow</span></span>|<span data-ttu-id="9adee-158">Fyysisen varaston sijainnin sisällä siirtyvät nimikkeet, kuten tuotantokomponentit ja tuotos.</span><span class="sxs-lookup"><span data-stu-id="9adee-158">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="9adee-159">Lähtevä virta</span><span class="sxs-lookup"><span data-stu-id="9adee-159">Outbound flow</span></span>|<span data-ttu-id="9adee-160">Fyysisen varaston sijainnista ulos siirtyvät nimikkeet, kuten myynnit ja lähtevät siirrot.</span><span class="sxs-lookup"><span data-stu-id="9adee-160">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="9adee-161">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9adee-161">See Also</span></span>  
 [<span data-ttu-id="9adee-162">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="9adee-162">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

