---
title: Näytä taulukon tiedot
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2020
ms.author: jswymer
ms.openlocfilehash: de93063a60e6b64405b1491a67489c8bfa4657ad
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275316"
---
# <a name="viewing-table-information"></a><span data-ttu-id="ac335-102">Näyttää taulukon tiedot</span><span class="sxs-lookup"><span data-stu-id="ac335-102">Viewing Table Information</span></span>

<span data-ttu-id="ac335-103">Sivun **8700 taulukossa on tietoja** kaikista Business Central -ratkaisun järjestelmä- ja liiketoimintataulukoista.</span><span class="sxs-lookup"><span data-stu-id="ac335-103">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="ac335-104">Sivulla on tietoja erityisesti taulukoiden sisältämien tietojen määrästä.</span><span class="sxs-lookup"><span data-stu-id="ac335-104">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="ac335-105">Näistä tiedoista on hyötyä suorituskykyongelmien vianmäärityksessä, sillä se näyttää tietojen koon jakautumisen eri taulukoissa.</span><span class="sxs-lookup"><span data-stu-id="ac335-105">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="ac335-106">Näyttää taulukon tiedot</span><span class="sxs-lookup"><span data-stu-id="ac335-106">Viewing table information</span></span>

<span data-ttu-id="ac335-107">Avataksesi tämän sivun, valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Taulukon tiedot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ac335-107">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="ac335-108">Seuraavassa taulukossa kuvataan kunkin taulukon tiedot:</span><span class="sxs-lookup"><span data-stu-id="ac335-108">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="ac335-109">Sarake</span><span class="sxs-lookup"><span data-stu-id="ac335-109">Column</span></span>|<span data-ttu-id="ac335-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ac335-110">Description</span></span>|
|------|-----------|
|<span data-ttu-id="ac335-111">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="ac335-111">Company Name</span></span>|<span data-ttu-id="ac335-112">Sen yrityksen nimi, jos sellainen on, johon taulukko kuuluu.</span><span class="sxs-lookup"><span data-stu-id="ac335-112">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="ac335-113">Taulukon nimi</span><span class="sxs-lookup"><span data-stu-id="ac335-113">Table Name</span></span>|<span data-ttu-id="ac335-114">Taulukon nimi.</span><span class="sxs-lookup"><span data-stu-id="ac335-114">The name of the table.</span></span>|
|<span data-ttu-id="ac335-115">Taulukon nro</span><span class="sxs-lookup"><span data-stu-id="ac335-115">Table No.</span></span>|<span data-ttu-id="ac335-116">Taulukon tunnus</span><span class="sxs-lookup"><span data-stu-id="ac335-116">The ID of the table</span></span>|
|<span data-ttu-id="ac335-117">Ei.</span><span class="sxs-lookup"><span data-stu-id="ac335-117">No.</span></span> <span data-ttu-id="ac335-118">tietuetta</span><span class="sxs-lookup"><span data-stu-id="ac335-118">of Records</span></span>|<span data-ttu-id="ac335-119">Taulukkoon tallennettujen tietueiden kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="ac335-119">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="ac335-120">Tietueen koko</span><span class="sxs-lookup"><span data-stu-id="ac335-120">Record Size</span></span>|<span data-ttu-id="ac335-121">Tietueiden keskimääräinen koko kilotavuina/tietueessa.</span><span class="sxs-lookup"><span data-stu-id="ac335-121">The average record size in KB/record.</span></span> <span data-ttu-id="ac335-122">Arvo lasketaan seuraavan kaavan avulla: 1024 (koko)/(Tietueiden</span><span class="sxs-lookup"><span data-stu-id="ac335-122">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="ac335-123">määrä).</span><span class="sxs-lookup"><span data-stu-id="ac335-123">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ac335-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ac335-124">See Also</span></span>

[<span data-ttu-id="ac335-125">Sivujen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="ac335-125">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="ac335-126">Suorituskykyartikkelit kehittäjille</span><span class="sxs-lookup"><span data-stu-id="ac335-126">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
