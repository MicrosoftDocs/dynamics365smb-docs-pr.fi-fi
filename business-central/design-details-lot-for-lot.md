---
title: Rakennetiedot – erä-erästä | Microsoft Docs
description: Lisätietoja erä-erästä-käytännön käyttämisestä tarveperustaisen tilausmäärän laskemisesta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3b80738be6dfe9d171a3cad56edf56cfa4960180
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2019
ms.locfileid: "938132"
---
# <a name="design-details-lot-for-lot"></a><span data-ttu-id="08bb2-103">Rakennetiedot: erä-erästä</span><span class="sxs-lookup"><span data-stu-id="08bb2-103">Design Details: Lot-for-Lot</span></span>
<span data-ttu-id="08bb2-104">Erä erästä -toiminto on kaikkein joustavin, koska järjestelmä reagoi vain ajankohtaiseen kysyntään, ja se toimii ennakkokysyntänä ennusteesta ja kestotilauksista, ja ratkaisee sitten tilausmäärän perustuen kysyntään.</span><span class="sxs-lookup"><span data-stu-id="08bb2-104">The lot-for-lot policy is the most flexible because the system only reacts on actual demand, plus it acts on anticipated demand from forecast and blanket orders and then settles the order quantity based on the demand.</span></span> <span data-ttu-id="08bb2-105">Erä erästä -toiminto on kohdistettu A- ja B-nimikkeille, joissa varasto voidaan hyväksyä, mutta tätä tulee välttää.</span><span class="sxs-lookup"><span data-stu-id="08bb2-105">The lot-for-lot policy is aimed at A- and B-items where inventory can be accepted but should be avoided.</span></span>  

<span data-ttu-id="08bb2-106">Monilla tavoilla erä-erästä käytäntö näyttää tilauskäytännöltä, mutta sillä on yleinen lähestymistapa nimikkeisiin – se voi hyväksyä varastossa olevat määrät ja se kokoaa kysynnän ja vastaavan tarjonnan käyttäjän määrittämiin aikaväleihin.</span><span class="sxs-lookup"><span data-stu-id="08bb2-106">In some ways, the lot-for-lot policy looks like the Order policy, but it has a generic approach to items; it can accept quantities in inventory, and it bundles demand and corresponding supply in time buckets defined by the user.</span></span>  

<span data-ttu-id="08bb2-107">Aikaväli määritetään **Aikaväli**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="08bb2-107">The time bucket is defined in the **Time Bucket** field.</span></span> <span data-ttu-id="08bb2-108">Järjestelmän käyttämä pienin aikaväli on yksi päivä. Se on kysyntä- ja tarjontatapahtumien ajan pienin mittayksikkö järjestelmässä. Käytännössä tosin tuotantotilausten ja komponenttitarpeiden ajan mittayksikkö voidaan määrittää sekunteina.</span><span class="sxs-lookup"><span data-stu-id="08bb2-108">The system works with a minimum time bucket of one day, since this is the smallest time unit of measure on demand and supply events in the system (although, in practice, the time unit of measure on production orders and component needs can be seconds).</span></span>  

<span data-ttu-id="08bb2-109">Aikaväli määrittää myös rajat sille, milloin olemassa oleva toimitustilaus on ajoitettava uudelleen annettua kysyntää vastaavaksi.</span><span class="sxs-lookup"><span data-stu-id="08bb2-109">The time bucket also sets limits on when an existing supply order should be rescheduled to meet a given demand.</span></span> <span data-ttu-id="08bb2-110">Jos tarjonta sijoittuu aikavälille, se aikataulutetaan uudelleen sisään tai ulos kysynnän täyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="08bb2-110">If the supply lies within the time bucket, it will be rescheduled in or out to meet the demand.</span></span> <span data-ttu-id="08bb2-111">Muussa tapauksessa, jos se on aiemmin, se aiheuttaa tarpeetonta varaston kerääntymistä ja se tulisi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="08bb2-111">Otherwise, if it lies earlier, it will cause unnecessary build-up of inventory and should be canceled.</span></span> <span data-ttu-id="08bb2-112">Jos se on myöhemmin, uusi toimitustilaus luodaan sen sijaan.</span><span class="sxs-lookup"><span data-stu-id="08bb2-112">If it lies later, a new supply order will be created instead.</span></span>  

<span data-ttu-id="08bb2-113">Tämän käytännön avulla voi myös määrittää varmuusvaraston mahdollisten tarjonnan vaihteluiden kompensointia tai äkillisen kysynnän täyttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="08bb2-113">With this policy, it is also possible to define a safety stock in order to compensate for possible fluctuations in supply, or to meet sudden demand.</span></span>  

<span data-ttu-id="08bb2-114">Koska toimitustilauksen määrä perustuu todelliseen kysyntään, voi olla järkevää käyttää tilauksen muuttujakenttiä: pyöristä tilausmäärä ylös tietyn tilauskerrannaisen määrittämiseksi (tai mitan ostoyksikön), kasvata tilausta tiettyyn tilauksen vähimmäismäärään tai vähennä määrää määritettyyn enimmäismäärään (ja luo näin kaksi tai useampia toimituksia vaadittavan kokonaismäärän saavuttamiseksi).</span><span class="sxs-lookup"><span data-stu-id="08bb2-114">Because the supply order quantity is based on the actual demand it can make sense to use the order modifiers: round the order quantity up to meet a specified order multiple (or purchase unit of measure), increase the order to a specified minimum order quantity, or decrease the quantity to the specified maximum quantity (and thus create two or more supplies to reach the total needed quantity).</span></span>  

## <a name="see-also"></a><span data-ttu-id="08bb2-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="08bb2-115">See Also</span></span>  
<span data-ttu-id="08bb2-116">[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="08bb2-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="08bb2-117">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="08bb2-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="08bb2-118">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="08bb2-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="08bb2-119">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="08bb2-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
