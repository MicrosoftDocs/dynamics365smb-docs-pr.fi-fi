---
title: Rakennetiedot – dimensioyhdistelmän tapahtumat | Microsoft Docs
description: Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja dimensiotapahtuman tallennus- ja kirjaustoiminnon uudelleenmäärityksessä käytettävistä konsepteista ja periaatteista.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242742"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="3ff56-103">Rakennetiedot: dimensioyhdistelmä-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="3ff56-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="3ff56-104">Tässä ohjeistuksessa on yksityiskohtaisia teknisiä tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]in dimensiotapahtuman tallennus- ja kirjaustoiminnossa käytettävistä käsitteistä ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="3ff56-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3ff56-105">Ohjeistuksen alussa käsitellään käsitteellisiä yhteenvetoja.</span><span class="sxs-lookup"><span data-stu-id="3ff56-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="3ff56-106">Sen jälkeen käsitellään teknistä arkkitehtuuria.</span><span class="sxs-lookup"><span data-stu-id="3ff56-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="3ff56-107">Siinä on myös koodiesimerkkejä, joiden avulla voit varautua dimensiokoodin siirtoon ja päivitykseen Dynamics NAV 2013R2:ta edeltävistä versioista.</span><span class="sxs-lookup"><span data-stu-id="3ff56-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="3ff56-108">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="3ff56-108">In This Section</span></span>  
[<span data-ttu-id="3ff56-109">Dimensioyhdistelmätapahtumien yleiskuva</span><span class="sxs-lookup"><span data-stu-id="3ff56-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="3ff56-110">Rakennetiedot: dimensioyhdistelmien etsiminen</span><span class="sxs-lookup"><span data-stu-id="3ff56-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="3ff56-111">Rakennetiedot: taulukkorakenne</span><span class="sxs-lookup"><span data-stu-id="3ff56-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="3ff56-112">Rakennetiedot: koodiyksikön 408 dimension hallinta</span><span class="sxs-lookup"><span data-stu-id="3ff56-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="3ff56-113">Rakennetiedot: koodiesimerkkejä muuttuneista kuvioista muutoksissa</span><span class="sxs-lookup"><span data-stu-id="3ff56-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
