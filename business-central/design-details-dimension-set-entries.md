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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 5563241784aaf8bfa1a29f8568411be657647cf7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795728"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="729e7-103">Rakennetiedot: dimensioyhdistelmä-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="729e7-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="729e7-104">Tässä dokumentaatiossa on yksityiskohtaisia teknisiä tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman dimensiotapahtuman tallennus- ja kirjaustoiminnon uudelleenmäärityksessä käytettävistä konsepteista ja periaatteista.</span><span class="sxs-lookup"><span data-stu-id="729e7-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the dimension entry storing and posting feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="729e7-105">Dokumentointi alkaa kuvailemalla uudelleensuunnittelun käsitteelliset yhteenvedot.</span><span class="sxs-lookup"><span data-stu-id="729e7-105">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="729e7-106">Tämän jälkeen kerrotaan teknisestä arkkitehtuurista ja näytetään, miten uudelleensuunnittelu tehdään.</span><span class="sxs-lookup"><span data-stu-id="729e7-106">Then it explains the technical architecture to show how the redesign is made.</span></span> <span data-ttu-id="729e7-107">Lopuksi se tarjoaa koodiesimerkkejä, joiden avulla voit varautua dimensiokoodin siirtoon ja päivitykseen.</span><span class="sxs-lookup"><span data-stu-id="729e7-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="729e7-108">Tämän osan sisältö</span><span class="sxs-lookup"><span data-stu-id="729e7-108">In This Section</span></span>  
[<span data-ttu-id="729e7-109">Dimensioyhdistelmätapahtumien yleiskuva</span><span class="sxs-lookup"><span data-stu-id="729e7-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="729e7-110">Rakennetiedot: dimensioyhdistelmien etsiminen</span><span class="sxs-lookup"><span data-stu-id="729e7-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="729e7-111">Rakennetiedot: taulukkorakenne</span><span class="sxs-lookup"><span data-stu-id="729e7-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="729e7-112">Rakennetiedot: koodiyksikön 408 dimension hallinta</span><span class="sxs-lookup"><span data-stu-id="729e7-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="729e7-113">Rakennetiedot: koodiesimerkkejä muuttuneista kuvioista muutoksissa</span><span class="sxs-lookup"><span data-stu-id="729e7-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
