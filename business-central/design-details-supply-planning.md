---
title: Rakennetiedot – Toimitusten suunnittelu | Microsoft Docs
description: Tässä ohjeaiheessa on yleiskatsaus Business Central -sovelluksen toimitusten suunnitteluominaisuuksissa käytettävistä käsitteistä ja periaatteista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 154714e5fff91e4287895b8b447a179063530c10
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388572"
---
# <a name="design-details-supply-planning"></a><span data-ttu-id="c2339-103">Rakennetiedot: tarjonnan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="c2339-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="c2339-104">Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman tarjonnan suunnittelun toimintojen kanssa käytettävistä konsepteista ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="c2339-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="c2339-105">Se kuvaa, miten suunnittelujärjestelmä toimii, ja kuinka algoritmeja voidaan muuttaa eri ympäristöjen suunnitteluvaatimuksia vastaaviksi.</span><span class="sxs-lookup"><span data-stu-id="c2339-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="c2339-106">Se esittelee ensin keskitetyn ratkaisun käsitteet ja kuvaa sitten keskeisen mekanismin eli tarjonnan täsmäytyksen logiikan ennen sitä, kuinka varaston suunnittelu suoritetaan uusintatilaustapojen avulla.</span><span class="sxs-lookup"><span data-stu-id="c2339-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="c2339-107">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="c2339-107">In This Section</span></span>  
[<span data-ttu-id="c2339-108">Rakennetiedot: Suunnittelujärjestelmän keskeiset käsitteet</span><span class="sxs-lookup"><span data-stu-id="c2339-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="c2339-109">Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys</span><span class="sxs-lookup"><span data-stu-id="c2339-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="c2339-110">Rakennetiedot: kysynnän ja tarjonnan täsmäytys</span><span class="sxs-lookup"><span data-stu-id="c2339-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="c2339-111">Rakennetiedot: uusintatilauskäytäntöjen käsittely</span><span class="sxs-lookup"><span data-stu-id="c2339-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="c2339-112">Rakennetiedot: suunnittelun parametrit</span><span class="sxs-lookup"><span data-stu-id="c2339-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="c2339-113">Rakennetiedot: suunnittelun kohdistustaulukko</span><span class="sxs-lookup"><span data-stu-id="c2339-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="c2339-114">Rakennetiedot: kysyntä tyhjä-sijainnissa</span><span class="sxs-lookup"><span data-stu-id="c2339-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="c2339-115">Rakennetiedot: siirrot suunnittelussa</span><span class="sxs-lookup"><span data-stu-id="c2339-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]