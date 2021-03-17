---
title: Rakennetiedot – nimikkeen seuranta varastossa | Microsoft Docs
description: Sarjanumeron ja eränumeron käsittely on ensisijaisesti varaston tehtävä ja siksi kaikilla saapuvilla ja lähtevillä varastodokumenteilla on perustoimintatarkoitus nimikkeiden seurantanumeroiden määrittämiselle ja valinnalle. Koska varausjärjestelmä perustuu nimiketapahtumiin, sellaisia varastoinnin toimenpideasiakirjoja ei tueta täysin, jotka rekisteröivät vain fyysisen varastoinnin tapahtumia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6deebef5b1413ac04febe3333d21fe730e3bdea7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390947"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="a0dca-104">Rakennetiedot: nimikkeen seuranta f. varastossa</span><span class="sxs-lookup"><span data-stu-id="a0dca-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="a0dca-105">Sarjanumeron ja eränumeron käsittely on ensisijaisesti varaston tehtävä ja siksi kaikilla saapuvilla ja lähtevillä varastodokumenteilla on perustoimintatarkoitus nimikkeiden seurantanumeroiden määrittämiselle ja valinnalle.</span><span class="sxs-lookup"><span data-stu-id="a0dca-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="a0dca-106">Koska varausjärjestelmä perustuu nimiketapahtumiin, sellaisia varastoinnin toimenpideasiakirjoja ei tueta täysin, jotka rekisteröivät vain fyysisen varastoinnin tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a0dca-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="a0dca-107">Koska varaukset ja nimikkeen seurantanumerot voidaan käsitellä vain sijaintitasolla, ei lokero- ja vyöhyketasolla, **Nimikkeen seurantarivi**-sivua ei voida avata varastotoiminnon asiakirjoista.</span><span class="sxs-lookup"><span data-stu-id="a0dca-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="a0dca-108">Sama koskee **Varaus**-sivua.</span><span class="sxs-lookup"><span data-stu-id="a0dca-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="a0dca-109">Kun sarja- tai eränumero on lisätty nimikkeeseen varastosijainnissa, se voidaan vapaasti siirtää ja luokitella varastossa uudelleen käyttämällä riippumatonta nimikkeen seurantarakennetta, joka ei ole riippuvainen varausjärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="a0dca-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="a0dca-110">**Sarjanro** ja **eränro** -kenttiin pääsee suoraan varaston asiakirjariveiltä.</span><span class="sxs-lookup"><span data-stu-id="a0dca-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="a0dca-111">Kun sarja- tai eränumero myöhemmin ottaa osaa lähtevään kirjaukseen, se synkronoidaan varausjärjestelmän kanssa tavallisen varastopaikan muutoksen osana.</span><span class="sxs-lookup"><span data-stu-id="a0dca-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="a0dca-112">Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Integrointi varaston kanssa](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="a0dca-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="a0dca-113">Varausjärjestelmä ottaa saatavuuden laskennassa kuitenkin huomioon fyysisen varastoinnin toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="a0dca-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="a0dca-114">Esimerkiksi poimintoihin varattuja tai poimituiksi rekisteröityjä nimikkeitä ei voi varata.</span><span class="sxs-lookup"><span data-stu-id="a0dca-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="a0dca-115">Lisätietoja on kohdassa [Rakennetiedot: varastosaatavuus](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="a0dca-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a0dca-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a0dca-116">See Also</span></span>  
[<span data-ttu-id="a0dca-117">Rakennetiedot: nimikkeen seuranta</span><span class="sxs-lookup"><span data-stu-id="a0dca-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="a0dca-118">Rakennetiedot: integrointi varaston kanssa</span><span class="sxs-lookup"><span data-stu-id="a0dca-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="a0dca-119">Rakennetiedot: varastosaatavuus</span><span class="sxs-lookup"><span data-stu-id="a0dca-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="a0dca-120">Rakennetiedot: nimikkeen seurannan rakenne</span><span class="sxs-lookup"><span data-stu-id="a0dca-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]