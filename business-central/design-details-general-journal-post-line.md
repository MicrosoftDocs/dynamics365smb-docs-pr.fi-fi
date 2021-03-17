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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e7e61b572b2a7a1538d58430cbbcbb19d7cda999
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390072"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="a83e5-103">Rakenteen tiedot: Yleisen päiväkirjan kirjausrivi</span><span class="sxs-lookup"><span data-stu-id="a83e5-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="a83e5-104">Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleisen päiväkirjan kirjausriviominaisuuden uudelleenmäärityksessä käytettävistä konsepteista ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="a83e5-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a83e5-105">Uudelleensuunnittelu tekee codeunit 12:sta yksinkertaisemman ja ylläpidettävämmän.</span><span class="sxs-lookup"><span data-stu-id="a83e5-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="a83e5-106">Dokumentointi alkaa kuvailemalla uudelleensuunnittelun käsitteelliset yhteenvedot.</span><span class="sxs-lookup"><span data-stu-id="a83e5-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="a83e5-107">Tämän jälkeen kerrotaan teknisestä arkkitehtuurista ja näytetään muutokset, jotka uudelleensuunnittelu aiheuttaa.</span><span class="sxs-lookup"><span data-stu-id="a83e5-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="a83e5-108">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="a83e5-108">In This Section</span></span>  
[<span data-ttu-id="a83e5-109">Yleisen päiväkirjan kirjausrivin yleiskuva</span><span class="sxs-lookup"><span data-stu-id="a83e5-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="a83e5-110">Rakenteen tiedot: Kirjausliittymän rakenne</span><span class="sxs-lookup"><span data-stu-id="a83e5-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="a83e5-111">Rakenteen tiedot: Kirjausohjelman rakenne</span><span class="sxs-lookup"><span data-stu-id="a83e5-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="a83e5-112">Codeunitin 12 muutokset: Yleisten muuttujien linkitys yleisen päiväkirjan kirjausriviin</span><span class="sxs-lookup"><span data-stu-id="a83e5-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="a83e5-113">Codeunitin 12 muutokset: Päiväkirjakirjausten menettelytapojen muutokset</span><span class="sxs-lookup"><span data-stu-id="a83e5-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="a83e5-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a83e5-114">See Also</span></span>  
[<span data-ttu-id="a83e5-115">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="a83e5-115">Working with General Journals</span></span>](ui-work-general-journals.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]