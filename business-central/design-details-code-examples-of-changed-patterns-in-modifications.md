---
title: "Rakennetiedot – kysynnän ja tarjonnan sulkeminen | Microsoft Docs"
description: "Kun tarjonnan tasapainotusmenetelmät on suoritettu, tulos voi olla jokin kolmesta vaihtoehdosta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2be48e11d562f469ab9ef5ac156fdeb46ea51107
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-closing-demand-and-supply"></a><span data-ttu-id="09cc2-103">Rakennetiedot: kysynnän ja tarjonnan sulkeminen</span><span class="sxs-lookup"><span data-stu-id="09cc2-103">Design Details: Closing Demand and Supply</span></span>
<span data-ttu-id="09cc2-104">Kun tarjonnan tasapainotusmenetelmät on suoritettu, tulos voi olla jokin seuraavista kolmesta vaihtoehdosta:</span><span class="sxs-lookup"><span data-stu-id="09cc2-104">When the supply balancing procedures have been performed, there are three possible end situations:</span></span>  

-   <span data-ttu-id="09cc2-105">Vaadittu kysyntätapahtumien määrä ja päivämäärä on kohdattu ja niiden suunnittelu voidaan sulkea,.</span><span class="sxs-lookup"><span data-stu-id="09cc2-105">The required quantity and date of the demand events have been met and the planning for them can be closed.</span></span> <span data-ttu-id="09cc2-106">Tarjontatapahtuma on yhä avoinna ja se voi kattaa seuraavan kysynnän, joten täsmäytys voi alkaa nykyisestä tarjontatapahtumasta ja seuraavasta kysynnästä.</span><span class="sxs-lookup"><span data-stu-id="09cc2-106">The supply event is still open and may be able to cover the next demand, so the balancing procedure can start over with the current supply event and the next demand.</span></span>  

-   <span data-ttu-id="09cc2-107">Toimitustilausta ei voi muokata niin, että se kattaa koko kysynnän.</span><span class="sxs-lookup"><span data-stu-id="09cc2-107">The supply order cannot be modified to cover all of the demand.</span></span> <span data-ttu-id="09cc2-108">Kysyntätapahtuma on edelleen avoinna. Siinä on jokin katteeton määrä, joka voidaan kattaa seuraavalla tuotantotapahtumalla.</span><span class="sxs-lookup"><span data-stu-id="09cc2-108">The demand event is still open, with some uncovered quantity that may be covered by the next supply event.</span></span> <span data-ttu-id="09cc2-109">Nykyinen tarjontatapahtuma siis suljetaan ja täsmäytystoiminto alkaa alusta nykyisestä kysynnästä ja seuraavasta tarjontatapahtumasta.</span><span class="sxs-lookup"><span data-stu-id="09cc2-109">Thus the current supply event is closed, so the balancing act can start over with the current demand and the next supply event.</span></span>  

-   <span data-ttu-id="09cc2-110">Kaikki kysyntä on otettu huomioon; kysyntää ei ole myöhemmin (tai kysyntää ei ole lainkaan).</span><span class="sxs-lookup"><span data-stu-id="09cc2-110">All of the demand has been covered; there is no subsequent demand (or there has been no demand at all).</span></span> <span data-ttu-id="09cc2-111">Jos olemassa on ylimääräistä tarjontaa, se voidaan vähentää (tai peruuttaa) ja sitten sulkea.</span><span class="sxs-lookup"><span data-stu-id="09cc2-111">If there is any surplus supply, it may be decreased (or canceled) and then closed.</span></span> <span data-ttu-id="09cc2-112">On mahdollista, että myöhempänä ketjussa on lisää tarjontatapahtumia ja myös ne tulisi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="09cc2-112">It is possible that additional supply events exist further along in the chain, and they should also be canceled.</span></span>  

 <span data-ttu-id="09cc2-113">Viimeiseksi suunnittelujärjestelmä luo tilauksen seurantalinkin tarjonnan ja kysynnän välille.</span><span class="sxs-lookup"><span data-stu-id="09cc2-113">Last, the planning system will create an order tracking link between the supply and the demand.</span></span>  

## <a name="creating-the-planning-line-suggested-action"></a><span data-ttu-id="09cc2-114">Suunnittelurivin luonti (ehdotettu toimenpide)</span><span class="sxs-lookup"><span data-stu-id="09cc2-114">Creating the Planning Line (Suggested Action)</span></span>  
 <span data-ttu-id="09cc2-115">Jos toimitustilauksen korjaamista ehdotetaan jollakin toiminnolla, kuten uusi, muuta määrä, aikatauluta uudelleen, aikatauluta uudelleen ja muuta määrää tai peruuta, suunnittelujärjestelmä luo suunnittelurivin suunnittelutyökirjassa.</span><span class="sxs-lookup"><span data-stu-id="09cc2-115">If any action – New, Change Quantity, Reschedule, Reschedule and Change Quantity, or Cancel – is suggested to revise the supply order, the planning system creates a planning line in the planning worksheet.</span></span> <span data-ttu-id="09cc2-116">Tilauksen seurannasta johtuen suunnitteluriviä ei luoda vain tarjontatapahtuman lopuksi mutta myös siinä tapauksessa, jos kysyntätapahtuma suljetaan, vaikka tarjontatapahtuma on yhä avoinna ja siihen saattaa kohdistua muita muutoksia seuraavan kysyntätapahtuman käsittelyn yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="09cc2-116">Due to order tracking, the planning line is created not only when the supply event is closed, but also if the demand event is closed, even though the supply event is still open and may be subject to additional changes when the next demand event is processed.</span></span> <span data-ttu-id="09cc2-117">Tämä tarkoittaa sitä, että jos suunnittelurivi on luotu ensimmäisenä, sitä voidaan muuttaa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="09cc2-117">This means that when first created, the planning line may be changed again.</span></span>  

 <span data-ttu-id="09cc2-118">Tuotantotilausten käsittelyn aikaista tietokantayhteyden käyttöä voi minimoida ylläpitämällä suunnittelurivejä kolmella tasolla ja pyrkimällä käyttämään vähiten kuormittava ylläpitotasoa.</span><span class="sxs-lookup"><span data-stu-id="09cc2-118">To minimize database access when handling production orders, the planning line can be maintained in three levels, while aiming to perform the least demanding maintenance level:</span></span>  

-   <span data-ttu-id="09cc2-119">Luo vain suunnittelurivi nykyisellä eräpäivällä ja määrällä, mutta ilman reititystä ja komponentteja.</span><span class="sxs-lookup"><span data-stu-id="09cc2-119">Create only the planning line with the current due date and quantity but without the routing and components.</span></span>  

-   <span data-ttu-id="09cc2-120">Sisällytä reititys: suunniteltu reititys asetellaan aloitus- ja lopetuspäivämäärät ja kellonajat mukaan lukien.</span><span class="sxs-lookup"><span data-stu-id="09cc2-120">Include routing: the planned routing is laid out including calculation of starting and ending dates and times.</span></span> <span data-ttu-id="09cc2-121">Tämä on vaativaa tietokannan käyttöoikeuksia ajatellen.</span><span class="sxs-lookup"><span data-stu-id="09cc2-121">This is demanding in terms of database accesses.</span></span> <span data-ttu-id="09cc2-122">Kun haluat määrittää loppupäivämäärän ja eräpäivän, tämä on ehkä laskettava, vaikka tarjontatapahtumaa ei ole suljettu (jos kyseessä on aikataulutus eteenpäin).</span><span class="sxs-lookup"><span data-stu-id="09cc2-122">To determine the ending and due dates, it may be necessary to calculate this even if the supply event has not been closed (in the case of forward scheduling).</span></span>  

-   <span data-ttu-id="09cc2-123">Sisällytä tuoterakenteen purku: tämä voi odottaa hetkeä ennen tarjontatapahtuman sulkemista.</span><span class="sxs-lookup"><span data-stu-id="09cc2-123">Include BOM explosion: this can wait until just before the supply event is closed.</span></span>  

 <span data-ttu-id="09cc2-124">Tämä päättää suunnittelujärjestelmän suorittaman kysynnän ja tarjonnan lataamisen, priorisoinnin ja täsmäytyksen kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="09cc2-124">This concludes the descriptions of how demand and supply is loaded, prioritized, and balanced by the planning system.</span></span> <span data-ttu-id="09cc2-125">Järjestelmän on varmistettava yhdessä tämän tarjonnan suunnittelutehtävän kanssa, että jokaisen suunnitellun nimikkeen vaadittava varastotaso säilytetään sen uusintatilauskäytännön mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="09cc2-125">In integration with this supply planning activity, the system must ensure that the required inventory level of each planned item is maintained according to its reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09cc2-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="09cc2-126">See Also</span></span>  
 <span data-ttu-id="09cc2-127">[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="09cc2-127">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="09cc2-128">[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="09cc2-128">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="09cc2-129">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="09cc2-129">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

