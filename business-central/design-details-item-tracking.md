---
title: Rakennetiedot – Nimikkeen seuranta | Microsoft Docs
description: Tässä ohjeaiheessa on yleiskatsaus nimikeseurannan rakennetiedoista.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b263abf09a3d74bbac4f8b94c4dde61644702bfc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303194"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="7c422-103">Rakennetiedot: nimikkeen seuranta</span><span class="sxs-lookup"><span data-stu-id="7c422-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="7c422-104">Kun päivän tarjontaketjun tavaravirta monimutkaistuu, nimikkeiden seuraamisesta tulee osallistuville yrityksille tärkeämpää.</span><span class="sxs-lookup"><span data-stu-id="7c422-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="7c422-105">Nimikkeen tapahtuman virtauksen valvonta on lakisääteinen vaatimus lääketieteellisessä ja kemiallisessa tarjonnassa, mutta muut yritykset saattavat haluta valvoa tuotteita, joilla on takuut tai vanhenemispäivämäärät asiakaspalvelun vuoksi.</span><span class="sxs-lookup"><span data-stu-id="7c422-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="7c422-106">Kohteen seurantajärjestelmän tulisi tarjota yritykselle helpon tavan käsitellä sarja- ja eränumeroita joka ottaa huomioon jokaisen kauppatavaran yksilöllisyyden: milloin ja missä vastaanotettu, minne tallennettu, milloin ja missä myyty.</span><span class="sxs-lookup"><span data-stu-id="7c422-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7c422-107">on laajentanut asteittain tätä liiketoiminnan vaatimusta ja tarjoaa nyt koko sovelluksen kattavan toiminnallisuuden sekä vakaan ytimen, joka mahdollistaa laajennusten kehittämisen.</span><span class="sxs-lookup"><span data-stu-id="7c422-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="7c422-108">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="7c422-108">In This Section</span></span>  
[<span data-ttu-id="7c422-109">Rakennetiedot: nimikkeen seurannan rakenne</span><span class="sxs-lookup"><span data-stu-id="7c422-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="7c422-110">Rakennetiedot: nimikkeen seurannan kirjauksen rakenne</span><span class="sxs-lookup"><span data-stu-id="7c422-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="7c422-111">Rakennetiedot: aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin</span><span class="sxs-lookup"><span data-stu-id="7c422-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="7c422-112">Rakennetiedot: Nimikkeen seurantarivit -sivu</span><span class="sxs-lookup"><span data-stu-id="7c422-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="7c422-113">Rakennetiedot: nimikkeen seurannan saatavuus</span><span class="sxs-lookup"><span data-stu-id="7c422-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="7c422-114">Rakennetiedot: nimikkeen seuranta ja suunnittelu</span><span class="sxs-lookup"><span data-stu-id="7c422-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="7c422-115">Rakennetiedot: nimikkeen seuranta ja varaukset</span><span class="sxs-lookup"><span data-stu-id="7c422-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="7c422-116">Rakennetiedot: nimikkeen seuranta f. varastossa</span><span class="sxs-lookup"><span data-stu-id="7c422-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)
