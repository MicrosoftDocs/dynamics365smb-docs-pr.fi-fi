---
title: Rakennetiedot – Nimikkeen seuranta | Microsoft Docs
description: Tässä ohjeaiheessa on yleiskatsaus nimikeseurannan rakennetiedoista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6e5f20d2f450f3f544cc2f7023160e4e9babdf33
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772802"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="cce19-103">Rakennetiedot: nimikkeen seuranta</span><span class="sxs-lookup"><span data-stu-id="cce19-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="cce19-104">Samalla kun tämän hetkinen tarjontaketjun tavaravirta monimutkaistuu koko ajan, nimikkeiden seurannasta tulee yrityksille entistä tärkeämpää.</span><span class="sxs-lookup"><span data-stu-id="cce19-104">As the flow of goods in today's supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="cce19-105">Nimikkeen tapahtumatyönkulun valvonta on lakisääteinen vaatimus lääke- ja kemianteollisuuden toimituksissa, mutta muut yritykset haluavat ehkä tuotteiden takuita tai vanhentumispäiviä asiakaspalvelun vuoksi.</span><span class="sxs-lookup"><span data-stu-id="cce19-105">Monitoring an item's transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="cce19-106">Kohteen seurantajärjestelmän tulisi tarjota yritykselle helpon tavan käsitellä sarja- ja eränumeroita joka ottaa huomioon jokaisen kauppatavaran yksilöllisyyden: milloin ja missä vastaanotettu, minne tallennettu, milloin ja missä myyty.</span><span class="sxs-lookup"><span data-stu-id="cce19-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="cce19-107">on laajentanut asteittain tätä liiketoiminnan vaatimusta ja tarjoaa nyt koko sovelluksen kattavan toiminnallisuuden sekä vakaan ytimen, joka mahdollistaa laajennusten kehittämisen.</span><span class="sxs-lookup"><span data-stu-id="cce19-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="cce19-108">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="cce19-108">In This Section</span></span>  
[<span data-ttu-id="cce19-109">Rakennetiedot: nimikkeen seurannan rakenne</span><span class="sxs-lookup"><span data-stu-id="cce19-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="cce19-110">Rakennetiedot: nimikkeen seurannan kirjauksen rakenne</span><span class="sxs-lookup"><span data-stu-id="cce19-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="cce19-111">Rakennetiedot: aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin</span><span class="sxs-lookup"><span data-stu-id="cce19-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="cce19-112">Rakennetiedot: Nimikkeen seurantarivit -sivu</span><span class="sxs-lookup"><span data-stu-id="cce19-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="cce19-113">Rakennetiedot: nimikkeen seurannan saatavuus</span><span class="sxs-lookup"><span data-stu-id="cce19-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="cce19-114">Rakennetiedot: nimikkeen seuranta ja suunnittelu</span><span class="sxs-lookup"><span data-stu-id="cce19-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="cce19-115">Rakennetiedot: nimikkeen seuranta ja varaukset</span><span class="sxs-lookup"><span data-stu-id="cce19-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="cce19-116">Rakennetiedot: nimikkeen seuranta f. varastossa</span><span class="sxs-lookup"><span data-stu-id="cce19-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)

## <a name="see-also"></a><span data-ttu-id="cce19-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cce19-117">See Also</span></span>

[<span data-ttu-id="cce19-118">Sarja-, erä- ja pakettinumeroiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="cce19-118">Work with Serial, Lot, and Package Numbers</span></span>](inventory-how-work-item-tracking.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]