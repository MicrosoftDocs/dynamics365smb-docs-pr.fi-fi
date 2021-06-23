---
title: Rakenteen tiedot – Yleisen päiväkirjan kirjausrivi | Microsoft Docs
description: Tässä aiheessa on tietoja Business Central -sovelluksen yleisen päiväkirjan kirjausriviominaisuuden uudelleenmäärityksessä käytettävistä käsitteistä ja periaatteista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215226"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="006c5-103">Rakenteen tiedot: Yleisen päiväkirjan kirjausrivi</span><span class="sxs-lookup"><span data-stu-id="006c5-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="006c5-104">Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleisen päiväkirjan kirjausriviominaisuuden uudelleenmäärityksessä käytetyistä käsitteistä ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="006c5-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="006c5-105">Uudelleensuunnittelu teki codeunit 12:sta yksinkertaisemman ja ylläpidettävämmän.</span><span class="sxs-lookup"><span data-stu-id="006c5-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="006c5-106">Dokumentointi alkaa kuvailemalla uudelleensuunnittelun käsitteelliset yhteenvedot.</span><span class="sxs-lookup"><span data-stu-id="006c5-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="006c5-107">Tämän jälkeen kerrotaan teknisestä arkkitehtuurista ja näytetään muutokset, jotka uudelleensuunnittelu aiheuttaa.</span><span class="sxs-lookup"><span data-stu-id="006c5-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="006c5-108">Tämän osan tiedot koskevat tuotteen aiemman version, Microsoft Dynamics NAV 2013 R2:n, uudelleensuunnittelua.</span><span class="sxs-lookup"><span data-stu-id="006c5-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="006c5-109">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="006c5-109">In This Section</span></span>

[<span data-ttu-id="006c5-110">Yleisen päiväkirjan kirjausrivin yleiskuva</span><span class="sxs-lookup"><span data-stu-id="006c5-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="006c5-111">Rakenteen tiedot: Kirjausliittymän rakenne</span><span class="sxs-lookup"><span data-stu-id="006c5-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="006c5-112">Rakenteen tiedot: Kirjausohjelman rakenne</span><span class="sxs-lookup"><span data-stu-id="006c5-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="006c5-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="006c5-113">See Also</span></span>

<span data-ttu-id="006c5-114">[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)
[Rakenteen tiedot: Yleisen päiväkirjan kirjausrivi (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="006c5-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]