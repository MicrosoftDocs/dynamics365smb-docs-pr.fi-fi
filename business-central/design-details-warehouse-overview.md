---
title: Rakennetiedot – Fyysisen varastoinnin yleiskatsaus | Microsoft Docs
description: Fyysisen varaston jokaisen tapahtuman ja siirron tiedot on voitava jäljittää, jotta nimikkeiden fyysistä käsittelyä voidaan tukea alue- ja varastopaikkatasolla. Tätä hallitaan **F. var. tapahtuma** -taulukossa. Jokainen tapahtuma tallennetaan varastorekisteriin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 41f18acde6140ca67050391273e9ace61f48fbb5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184578"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="dfc0c-105">Rakennetiedot: f. varaston yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="dfc0c-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="dfc0c-106">Fyysisen varaston jokaisen tapahtuman ja siirron tiedot on voitava jäljittää, jotta nimikkeiden fyysistä käsittelyä voidaan tukea alue- ja varastopaikkatasolla.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="dfc0c-107">Tätä hallitaan **F. var. tapahtuma** -taulukossa.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="dfc0c-108">Jokainen tapahtuma tallennetaan varastorekisteriin.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="dfc0c-109">Fyysisen varastoinnin asiakirjoja ja fyysisen varastoinnin päiväkirjaa käytetään fyysisen varastoinnin nimikesiirtojen rekisteröimisessä.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="dfc0c-110">Jokaisen f. varaston nimikkeen siirron, vastaanoton, hyllytyksen, poiminnan, toimituksen tai muutoksen yhteydessä tapahtumat rekisteröidään tallentamaan fyysiset tiedot vyöhykkeestä, lokerosta ja määrästä.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="dfc0c-111">**Bin-tiedoston sisältö** -taulukkoa käytetään käsiteltäessä kaikkia eri sisältödimensioita bineissä nimikettä kohden, kuten mittayksikkö, maksimimäärä ja minimimäärä.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="dfc0c-112">**Binin sisältö** -taulukko sisältää myös virtauskentät varastokirjauksiin, varaston ohjeisiin ja varaston lokiriveihin, mikä varmistaa sen, että nimikkeen saatavuus biniä kohden ja nimikkeen bin voidaan laskea nopeasti.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="dfc0c-113">Lisätietoja on kohdassa [Rakennetiedot: Saatavuus varastossa.](design-details-availability-in-the-warehouse.md)</span><span class="sxs-lookup"><span data-stu-id="dfc0c-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="dfc0c-114">Kun nimikkeiden kirjaukset tapahtuvat fyysisen varastoinnin moduulin ulkopuolella, fyysisen varastoinnin tapahtumat ja varastotapahtumat synkronoidaan sijaintikohtaisten muutosten oletusvarastopaikan avulla.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="dfc0c-115">Varaston fyysisen inventoinnin aikana kaikki määritetyt ja lasketut määrät tallennetaan muutoslokeroon ja kirjataan tämän jälkeen korjaavina nimiketapahtumina.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="dfc0c-116">Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Integrointi varaston kanssa](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="dfc0c-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="dfc0c-117">Seuraavassa kuvassa on luonnosteltu tyypillinen varaston kulku.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="dfc0c-118">![Varastoprosessien yleiskatsaus](media/design_details_warehouse_management_overview.png "Varastoprosessien yleiskatsaus")</span><span class="sxs-lookup"><span data-stu-id="dfc0c-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="dfc0c-119">Perus tai lisävarastointi</span><span class="sxs-lookup"><span data-stu-id="dfc0c-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="dfc0c-120">[!INCLUDE[d365fin](includes/d365fin_md.md)]in varastotoiminto voidaan toteuttaa yrityksen prosessien ja tilausmäärän mukaan valittavalla monimutkaisuustasolla.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-120">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="dfc0c-121">Pääero on, että toiminnot suoritetaan tilaus tilaukselta perusvarastoinnissa, kun ne yhdistetään useisiin tilauksiin kehittyneessä varastoinnissa.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="dfc0c-122">Eri monimutkaisuuden tasojen erottamista varten tässä dokumentaatiossa käsitellään kahta yleistä nimitystä: Perus ja Lisävarastointi.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="dfc0c-123">Tämä yksinkertainen erottaminen kattaa tuoteosion ja sijainnin asetusten määrittämät monimutkaisuuden useat eri tasot, joita tukevat erilaiset käyttöliittymäasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="dfc0c-124">Katso lisätietoja kohdasta [Rakennetiedot: f. varaston asetus](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="dfc0c-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="dfc0c-125">Varaston kehittyneintä tasoa kutsutaan tässä asiakirjassa nimellä "WMS-asennukset", koska tämä taso vaatii kehittyneimmän yksikön, Warehouse Management Systems.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="dfc0c-126">Seuraavia eri käyttöliittymäasiakirjoja käytetään perus- ja kehittyneessä varastoinnissa.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="dfc0c-127">Peruskäyttöliittymäasiakirjat</span><span class="sxs-lookup"><span data-stu-id="dfc0c-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="dfc0c-128">**Varastohyllytys**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="dfc0c-129">**Varaston poiminta**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="dfc0c-130">**Varaston siirto**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="dfc0c-131">**Nimikepäiväkirja**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-131">**Item Journal**</span></span>  
-   <span data-ttu-id="dfc0c-132">**Nimikkeen uudelleenluokituspäiväkirja**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="dfc0c-133">(Eri raportit)</span><span class="sxs-lookup"><span data-stu-id="dfc0c-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="dfc0c-134">Käyttöliittymän lisäasiakirjat</span><span class="sxs-lookup"><span data-stu-id="dfc0c-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="dfc0c-135">**F. varastoinnin vastaanotto**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="dfc0c-136">**Hyllytystyökirja**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="dfc0c-137">**F.varastoinnin hyllytys**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="dfc0c-138">**Poimintatyökirja**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="dfc0c-139">**F.varastoinnin poiminta**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="dfc0c-140">**Siirtotyökirja**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="dfc0c-141">**F. var. siirto**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="dfc0c-142">**Sisäinen f.var. poim.**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="dfc0c-143">**Sisäinen f.var. hyllytys**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="dfc0c-144">**Var.paikan luontityökirja**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="dfc0c-145">**Var.p. sisällön luontityökirja**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="dfc0c-146">**F.var. nimikepvk**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="dfc0c-147">**Var. nimik. uud.luok.pvk**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="dfc0c-148">(Eri raportit)</span><span class="sxs-lookup"><span data-stu-id="dfc0c-148">(Various reports)</span></span>  

<span data-ttu-id="dfc0c-149">Katso lisätietoja jokaisesta asiakirjasta kunkin sivun aiheista.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="dfc0c-150">Termit</span><span class="sxs-lookup"><span data-stu-id="dfc0c-150">Terminology</span></span>  
<span data-ttu-id="dfc0c-151">[!INCLUDE[d365fin](includes/d365fin_md.md)]in fyysisen varastoinnin ohjeistus käyttää seuraavia ostojen ja myyntien talouskäsitteiden mukaisia varaston nimikevirran termejä.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-151">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="dfc0c-152">Kausi</span><span class="sxs-lookup"><span data-stu-id="dfc0c-152">Term</span></span>|<span data-ttu-id="dfc0c-153">Description</span><span class="sxs-lookup"><span data-stu-id="dfc0c-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="dfc0c-154">Saapuva virta</span><span class="sxs-lookup"><span data-stu-id="dfc0c-154">Inbound flow</span></span>|<span data-ttu-id="dfc0c-155">Fyysisen varaston sijaintiin siirtyvät nimikkeet, kuten ostot ja saapuvat siirrot.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="dfc0c-156">Sisäinen virta</span><span class="sxs-lookup"><span data-stu-id="dfc0c-156">Internal flow</span></span>|<span data-ttu-id="dfc0c-157">Fyysisen varaston sijainnin sisällä siirtyvät nimikkeet, kuten tuotantokomponentit ja tuotos.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="dfc0c-158">Lähtevä virta</span><span class="sxs-lookup"><span data-stu-id="dfc0c-158">Outbound flow</span></span>|<span data-ttu-id="dfc0c-159">Fyysisen varaston sijainnista ulos siirtyvät nimikkeet, kuten myynnit ja lähtevät siirrot.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="dfc0c-160">Katso myös</span><span class="sxs-lookup"><span data-stu-id="dfc0c-160">See Also</span></span>  
 [<span data-ttu-id="dfc0c-161">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="dfc0c-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)
