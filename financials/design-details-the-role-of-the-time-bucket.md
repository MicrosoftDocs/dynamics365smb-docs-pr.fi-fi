---
title: "Rakennetiedot – aikavälin rooli | Microsoft Docs"
description: "Ajanjakson tarkoitus on kerätä kysyntätapahtumia aikaikkunan sisällä, jotta voidaan tehdä yhteinen toimitustilaus."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: eb1b1a401dabe09a77c44558e9f5a83388078aaa
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="15ec4-103">Rakennetiedot: aikavälin rooli</span><span class="sxs-lookup"><span data-stu-id="15ec4-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="15ec4-104">Aikavälin tarkoitus on kerätä kysyntätapahtumia aikaikkunan sisällä, jotta yhteinen toimitustilaus voidaan tehdä.</span><span class="sxs-lookup"><span data-stu-id="15ec4-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  
  
 <span data-ttu-id="15ec4-105">Uusintatilauspistettä käyttävien uusintatilaustapojen kohdalla voit määrittää aikavälin.</span><span class="sxs-lookup"><span data-stu-id="15ec4-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="15ec4-106">Tämä varmistaa, että saman ajanjakson kysyntä kertyy, ennen vaikutuksen oletettuun varastoon ja uusintatilauspisteen mahdollisen ohituksen tarkistusta.</span><span class="sxs-lookup"><span data-stu-id="15ec4-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="15ec4-107">Jos uusintatilauspiste on ohitettu, uusi toimitustilaus ajoitetaan eteenpäin aikavälin määrittämän jakson lopusta.</span><span class="sxs-lookup"><span data-stu-id="15ec4-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="15ec4-108">Aikavälit alkavat suunnittelun aloituspäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="15ec4-108">The time buckets begin on the planning starting date.</span></span>  
  
 <span data-ttu-id="15ec4-109">Konsepti, jolle on määritetty aikavälit, osoittaa manuaalisen varastotason tarkistuksen prosessin säännöllisin väliajoin, ei jokaisen tapahtuman kohdalla.</span><span class="sxs-lookup"><span data-stu-id="15ec4-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="15ec4-110">Käyttäjän on määritettävä toistoväli (aikaväli).</span><span class="sxs-lookup"><span data-stu-id="15ec4-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="15ec4-111">Esimerkiksi käyttäjä kerää kaikki nimikkeen tarpeet yhdeltä toimittajalta viikoittaisen tilauksen asettamiseksi.</span><span class="sxs-lookup"><span data-stu-id="15ec4-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  
  
 <span data-ttu-id="15ec4-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span><span class="sxs-lookup"><span data-stu-id="15ec4-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span></span>  
  
 <span data-ttu-id="15ec4-113">Aikaväliä käytetään yleensä limittäisyyden välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="15ec4-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="15ec4-114">Esimerkiksi täsmäytetty kysynnän ja tarjonnan rivi, jossa aikainen kysyntä on peruutettu tai uusi luodaan.</span><span class="sxs-lookup"><span data-stu-id="15ec4-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="15ec4-115">Tuloksena on, että jokainen toimitustilaus (paitsi viimeisin) aikataulutetaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="15ec4-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15ec4-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="15ec4-116">See Also</span></span>  
 <span data-ttu-id="15ec4-117">[Rakennetiedot: Uusintatilauskäytännöt](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="15ec4-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="15ec4-118">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="15ec4-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="15ec4-119">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="15ec4-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="15ec4-120">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="15ec4-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
