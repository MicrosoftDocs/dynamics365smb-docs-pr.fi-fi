---
title: "Rakennetiedot – Enimmäismäärä | Microsoft Docs"
description: "Maksimimääräohjeet on tapa ylläpitää varastoa käyttämällä jälkitilauspistettä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 21ae51ecf28458f9b09be6461243f31641a0aaef
ms.contentlocale: fi-fi
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-maximum-qty"></a><span data-ttu-id="01d29-103">Rakennetiedot: enimmäismäärä</span><span class="sxs-lookup"><span data-stu-id="01d29-103">Design Details: Maximum Qty.</span></span>
<span data-ttu-id="01d29-104">Enimmäismääräkäytäntö on tapa ylläpitää varastoa uudelleentilauspisteen avulla.</span><span class="sxs-lookup"><span data-stu-id="01d29-104">The Maximum Quantity policy is a way to maintain inventory using a reorder point.</span></span>  

 <span data-ttu-id="01d29-105">Kaikki kiinteää uusintatilausmäärän käytäntöä koskeva koskee myös tätä käytäntöä.</span><span class="sxs-lookup"><span data-stu-id="01d29-105">Everything regarding the Fixed Reorder Qty. policy also applies to this policy.</span></span> <span data-ttu-id="01d29-106">Ainoa ero on ehdotetun tarjonnan määrä.</span><span class="sxs-lookup"><span data-stu-id="01d29-106">The only difference is the quantity of the suggested supply.</span></span> <span data-ttu-id="01d29-107">Kun käytetään enimmäismääräkäytäntöä, uusintatilausmäärä määritetään dynaamisesti oletetun varaston tason perusteella. Sen vuoksi se yleensä on eri kuin tilausten välinen määrä.</span><span class="sxs-lookup"><span data-stu-id="01d29-107">When using the maximum quantity policy, the reorder quantity will be defined dynamically based on the projected inventory level and will therefore usually differ from order to order.</span></span>  

## <a name="calculated-per-time-bucket"></a><span data-ttu-id="01d29-108">Laskettu aikavälikohtaisesti</span><span class="sxs-lookup"><span data-stu-id="01d29-108">Calculated per Time Bucket</span></span>  
 <span data-ttu-id="01d29-109">Jälkitilausmäärä määritetään siihen ajankohtaan (ajanjakson loppu), kun suunnittelujärjestelmä havaitsee, että jälkitilauspiste on ylitetty.</span><span class="sxs-lookup"><span data-stu-id="01d29-109">The reorder quantity is determined at the point of time (the end of a time bucket) when the planning system detects that the reorder point has been crossed.</span></span> <span data-ttu-id="01d29-110">Tällä hetkellä järjestelmä mittaa välin nykyisestä arvioidusta varastotasosta määritettyyn enimmäisvarastoon asti.</span><span class="sxs-lookup"><span data-stu-id="01d29-110">At this time, the system measures the gap from the current projected inventory level up to the specified maximum inventory.</span></span> <span data-ttu-id="01d29-111">Tämä kuvaa määrää, joka tulisi järjestää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="01d29-111">This constitutes the quantity that should be reordered.</span></span> <span data-ttu-id="01d29-112">Järjestelmä tarkistaa, onko tarjonta jo tilattu muualle vastaanotettavaksi nimikkeen toimitusaikana. Jos näin on, järjestelmä pienentää uuden toimitustilauksen määrää jo tilattujen määrien verran.</span><span class="sxs-lookup"><span data-stu-id="01d29-112">The system then checks if supply has already been ordered elsewhere to be received within the lead time and, if so, reduces the quantity of the new supply order by already ordered quantities.</span></span>  

 <span data-ttu-id="01d29-113">Järjestelmä varmistaa, että oletettu varasto saavuttaa vähintään uusintatilauspisteen tason. Tämä tehdään siltä varalta, että käyttäjä unohtaa määrittää varaston enimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="01d29-113">The system will ensure that the projected inventory at least reaches the reorder point level – in case the user has forgotten to specify a maximum inventory quantity.</span></span>  

## <a name="combines-with-order-modifiers"></a><span data-ttu-id="01d29-114">Yhdistää tilausmääritteiden kanssa</span><span class="sxs-lookup"><span data-stu-id="01d29-114">Combines with Order Modifiers</span></span>  
 <span data-ttu-id="01d29-115">Asetuksesta riippuen saattaa olla parasta yhdistää enimmäismäärän käytäntö tilauksen muuttujien kanssa, jotta varmistetaan tilauksen vähimmäismäärä tai sen pyöristäminen oston mittayksikön kokonaislukuun, tai jotta se jaetaan useampiin eriin tilauksen enimmäismäärän määrityksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="01d29-115">Depending on the setup, it may be best to combine the Maximum Quantity policy with order modifiers to ensure a minimum order quantity or round it to an integer number of purchase units of measure, or split it into more lots as defined by the maximum order quantity.</span></span>  

## <a name="combines-with-calendars"></a><span data-ttu-id="01d29-116">Yhdistäminen kalentereihin</span><span class="sxs-lookup"><span data-stu-id="01d29-116">Combines with Calendars</span></span>  
 <span data-ttu-id="01d29-117">Ennen kuin uusintatilauspisteen täyttämiseen ehdotetaan uutta toimitustilausta, suunnittelujärjestelmä tarkistaa, onko tilaus ajoitettu **Yritystiedot**- ja **Sijaintikortti**-sivujen **Peruskalenterin koodi** -kentässä määritettyjen kalenterien mukaiselle ei-työskentelypäivälle.</span><span class="sxs-lookup"><span data-stu-id="01d29-117">Before suggesting a new supply order to meet a reorder point, the planning system checks if the order is scheduled for a non-working day, according to any calendars that are  defined in the **Base Calendar Code** field in the **Company Information** and **Location Card** pages.</span></span>  

 <span data-ttu-id="01d29-118">Jos suunniteltu päivämäärä ei ole työpäivä, suunnittelujärjestelmä siirtää tilauksen seuraavalle työpäivälle.</span><span class="sxs-lookup"><span data-stu-id="01d29-118">If the scheduled date is a non-working day, the planning system moves the order forward to the nearest working date.</span></span> <span data-ttu-id="01d29-119">Tämä voi johtaa tilaukseen, joka täyttää uusintatilauspisteen, mutta ei täytä mitään tiettyä kysyntää.</span><span class="sxs-lookup"><span data-stu-id="01d29-119">This may result in an order that meets a reorder point but does not meet some specific demand.</span></span> <span data-ttu-id="01d29-120">Suunnittelujärjestelmä luo ylimääräisen tarjonnan vastaamaan epätasapainoiseen kysyntään.</span><span class="sxs-lookup"><span data-stu-id="01d29-120">For such unbalanced demand, the planning system creates an extra supply.</span></span>  

## <a name="see-also"></a><span data-ttu-id="01d29-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="01d29-121">See Also</span></span>  
 <span data-ttu-id="01d29-122">[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="01d29-122">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="01d29-123">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="01d29-123">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="01d29-124">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="01d29-124">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="01d29-125">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="01d29-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

