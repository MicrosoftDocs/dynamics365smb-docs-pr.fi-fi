---
title: Rakennetiedot – Nimikkeen seuranta | Microsoft Docs
description: Tässä ohjeaiheessa on yleiskatsaus nimikeseurannan rakennetiedoista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 50ae6f2f3538269cc7c82dd2d84644a1a31d7f56
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751353"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="3bcd0-103">Rakennetiedot: nimikkeen seuranta</span><span class="sxs-lookup"><span data-stu-id="3bcd0-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="3bcd0-104">Kun päivän tarjontaketjun tavaravirta monimutkaistuu, nimikkeiden seuraamisesta tulee osallistuville yrityksille tärkeämpää.</span><span class="sxs-lookup"><span data-stu-id="3bcd0-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="3bcd0-105">Nimikkeen tapahtuman virtauksen valvonta on lakisääteinen vaatimus lääketieteellisessä ja kemiallisessa tarjonnassa, mutta muut yritykset saattavat haluta valvoa tuotteita, joilla on takuut tai vanhenemispäivämäärät asiakaspalvelun vuoksi.</span><span class="sxs-lookup"><span data-stu-id="3bcd0-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="3bcd0-106">Kohteen seurantajärjestelmän tulisi tarjota yritykselle helpon tavan käsitellä sarja- ja eränumeroita joka ottaa huomioon jokaisen kauppatavaran yksilöllisyyden: milloin ja missä vastaanotettu, minne tallennettu, milloin ja missä myyty.</span><span class="sxs-lookup"><span data-stu-id="3bcd0-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="3bcd0-107">on laajentanut asteittain tätä liiketoiminnan vaatimusta ja tarjoaa nyt koko sovelluksen kattavan toiminnallisuuden sekä vakaan ytimen, joka mahdollistaa laajennusten kehittämisen.</span><span class="sxs-lookup"><span data-stu-id="3bcd0-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="3bcd0-108">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="3bcd0-108">In This Section</span></span>  
[<span data-ttu-id="3bcd0-109">Rakennetiedot: nimikkeen seurannan rakenne</span><span class="sxs-lookup"><span data-stu-id="3bcd0-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="3bcd0-110">Rakennetiedot: nimikkeen seurannan kirjauksen rakenne</span><span class="sxs-lookup"><span data-stu-id="3bcd0-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="3bcd0-111">Rakennetiedot: aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin</span><span class="sxs-lookup"><span data-stu-id="3bcd0-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="3bcd0-112">Rakennetiedot: Nimikkeen seurantarivit -sivu</span><span class="sxs-lookup"><span data-stu-id="3bcd0-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="3bcd0-113">Rakennetiedot: nimikkeen seurannan saatavuus</span><span class="sxs-lookup"><span data-stu-id="3bcd0-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="3bcd0-114">Rakennetiedot: nimikkeen seuranta ja suunnittelu</span><span class="sxs-lookup"><span data-stu-id="3bcd0-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="3bcd0-115">Rakennetiedot: nimikkeen seuranta ja varaukset</span><span class="sxs-lookup"><span data-stu-id="3bcd0-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="3bcd0-116">Rakennetiedot: nimikkeen seuranta f. varastossa</span><span class="sxs-lookup"><span data-stu-id="3bcd0-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)
