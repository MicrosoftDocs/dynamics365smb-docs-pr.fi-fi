---
title: Rakennetiedot – aikavälin rooli | Microsoft Docs
description: Aikavälin tarkoitus on kerätä kysyntätapahtumia aikaikkunan sisällä, jotta yhteinen toimitustilaus voidaan tehdä.
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
ms.openlocfilehash: 54d4a4aed94b562b82d94d6a5a75a3050c054fc3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239312"
---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="69a44-103">Rakennetiedot: aikavälin rooli</span><span class="sxs-lookup"><span data-stu-id="69a44-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="69a44-104">Aikavälin tarkoitus on kerätä kysyntätapahtumia aikaikkunan sisällä, jotta yhteinen toimitustilaus voidaan tehdä.</span><span class="sxs-lookup"><span data-stu-id="69a44-104">The purpose of the time bucket is to collect demand events within the time page in order to make a joint supply order.</span></span>  

 <span data-ttu-id="69a44-105">Uusintatilauspistettä käyttävien uusintatilaustapojen kohdalla voit määrittää aikavälin.</span><span class="sxs-lookup"><span data-stu-id="69a44-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="69a44-106">Tämä varmistaa, että saman ajanjakson kysyntä kertyy, ennen vaikutuksen oletettuun varastoon ja uusintatilauspisteen mahdollisen ohituksen tarkistusta.</span><span class="sxs-lookup"><span data-stu-id="69a44-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="69a44-107">Jos uusintatilauspiste on ohitettu, uusi toimitustilaus ajoitetaan eteenpäin aikavälin määrittämän jakson lopusta.</span><span class="sxs-lookup"><span data-stu-id="69a44-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="69a44-108">Aikavälit alkavat suunnittelun aloituspäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="69a44-108">The time buckets begin on the planning starting date.</span></span>  

 <span data-ttu-id="69a44-109">Konsepti, jolle on määritetty aikavälit, osoittaa manuaalisen varastotason tarkistuksen prosessin säännöllisin väliajoin, ei jokaisen tapahtuman kohdalla.</span><span class="sxs-lookup"><span data-stu-id="69a44-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="69a44-110">Käyttäjän on määritettävä toistoväli (aikaväli).</span><span class="sxs-lookup"><span data-stu-id="69a44-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="69a44-111">Esimerkiksi käyttäjä kerää kaikki nimikkeen tarpeet yhdeltä toimittajalta viikoittaisen tilauksen asettamiseksi.</span><span class="sxs-lookup"><span data-stu-id="69a44-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  

 <span data-ttu-id="69a44-112">![Esimerkki ajanjaksosta suunnittelussa](media/nav_app_supply_planning_2_reorder_cycle.png "Esimerkki ajanjaksosta suunnittelussa")</span><span class="sxs-lookup"><span data-stu-id="69a44-112">![Example of time bucket in planning](media/nav_app_supply_planning_2_reorder_cycle.png "Example of time bucket in planning")</span></span>  

 <span data-ttu-id="69a44-113">Aikaväliä käytetään yleensä limittäisyyden välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="69a44-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="69a44-114">Esimerkiksi täsmäytetty kysynnän ja tarjonnan rivi, jossa aikainen kysyntä on peruutettu tai uusi luodaan.</span><span class="sxs-lookup"><span data-stu-id="69a44-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="69a44-115">Tuloksena on, että jokainen toimitustilaus (paitsi viimeisin) aikataulutetaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="69a44-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="69a44-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="69a44-116">See Also</span></span>  
 <span data-ttu-id="69a44-117">[Rakennetiedot: Uusintatilauskäytännöt](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="69a44-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="69a44-118">[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="69a44-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="69a44-119">[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="69a44-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="69a44-120">Rakennetiedot: Tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="69a44-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
