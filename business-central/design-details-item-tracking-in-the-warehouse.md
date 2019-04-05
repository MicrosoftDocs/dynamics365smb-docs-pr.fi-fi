---
title: Rakennetiedot – nimikkeen seuranta varastossa | Microsoft Docs
description: Sarjanumeron ja eränumeron käsittely on ensisijaisesti varaston tehtävä ja siksi kaikilla saapuvilla ja lähtevillä varastodokumenteilla on perustoimintatarkoitus nimikkeiden seurantanumeroiden määrittämiselle ja valinnalle. Koska varausjärjestelmä perustuu nimiketapahtumiin, sellaisia varastoinnin toimenpideasiakirjoja ei tueta täysin, jotka rekisteröivät vain fyysisen varastoinnin tapahtumia.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 01/15/2019
ms.author: sgroespe
ms.openlocfilehash: e780dba122374bd80e48ca6bbc74b7540e034ac6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795070"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="4d26b-104">Rakennetiedot: nimikkeen seuranta f. varastossa</span><span class="sxs-lookup"><span data-stu-id="4d26b-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="4d26b-105">Sarjanumeron ja eränumeron käsittely on ensisijaisesti varaston tehtävä ja siksi kaikilla saapuvilla ja lähtevillä varastodokumenteilla on perustoimintatarkoitus nimikkeiden seurantanumeroiden määrittämiselle ja valinnalle.</span><span class="sxs-lookup"><span data-stu-id="4d26b-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="4d26b-106">Koska varausjärjestelmä perustuu nimiketapahtumiin, sellaisia varastoinnin toimenpideasiakirjoja ei tueta täysin, jotka rekisteröivät vain fyysisen varastoinnin tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="4d26b-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="4d26b-107">Koska varaukset ja nimikkeen seurantanumerot voidaan käsitellä vain sijaintitasolla, ei lokero- ja vyöhyketasolla, **Nimikkeen seurantarivi**-sivua ei voida avata varastotoiminnon asiakirjoista.</span><span class="sxs-lookup"><span data-stu-id="4d26b-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="4d26b-108">Sama koskee **Varaus**-sivua.</span><span class="sxs-lookup"><span data-stu-id="4d26b-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="4d26b-109">Kun sarja- tai eränumero on lisätty nimikkeeseen varastosijainnissa, se voidaan vapaasti siirtää ja luokitella varastossa uudelleen käyttämällä riippumatonta nimikkeen seurantarakennetta, joka ei ole riippuvainen varausjärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="4d26b-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="4d26b-110">**Sarjanro** ja **eränro** -kenttiin pääsee suoraan varaston asiakirjariveiltä.</span><span class="sxs-lookup"><span data-stu-id="4d26b-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="4d26b-111">Kun sarja- tai eränumero myöhemmin ottaa osaa lähtevään kirjaukseen, se synkronoidaan varausjärjestelmän kanssa tavallisen varastopaikan muutoksen osana.</span><span class="sxs-lookup"><span data-stu-id="4d26b-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="4d26b-112">Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Integrointi varaston kanssa](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="4d26b-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="4d26b-113">Varausjärjestelmä ottaa saatavuuden laskennassa kuitenkin huomioon fyysisen varastoinnin toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="4d26b-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="4d26b-114">Esimerkiksi poimintoihin varattuja tai poimituiksi rekisteröityjä nimikkeitä ei voi varata.</span><span class="sxs-lookup"><span data-stu-id="4d26b-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="4d26b-115">Lisätietoja on kohdassa [Rakennetiedot: varastosaatavuus](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="4d26b-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4d26b-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4d26b-116">See Also</span></span>  
[<span data-ttu-id="4d26b-117">Rakennetiedot: nimikkeen seuranta</span><span class="sxs-lookup"><span data-stu-id="4d26b-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="4d26b-118">Rakennetiedot: integrointi varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="4d26b-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="4d26b-119">Rakennetiedot: varastosaatavuus</span><span class="sxs-lookup"><span data-stu-id="4d26b-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="4d26b-120">Rakennetiedot: nimikkeen seurannan rakenne</span><span class="sxs-lookup"><span data-stu-id="4d26b-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)
