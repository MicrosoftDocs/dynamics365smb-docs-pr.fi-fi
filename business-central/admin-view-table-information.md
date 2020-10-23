---
title: Näytä taulukon tiedot
description: Lue miten voit tarkastella tietokantataulukoiden tietoja suoraan Business Centralin asiakasliittymästä.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 72e220aa310515c665ce85bd43f4ebd3aac157d0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922265"
---
# <a name="viewing-table-information"></a><span data-ttu-id="625f9-103">Näyttää taulukon tiedot</span><span class="sxs-lookup"><span data-stu-id="625f9-103">Viewing Table Information</span></span>

<span data-ttu-id="625f9-104">Sivun **8700 taulukossa on tietoja** kaikista Business Central -ratkaisun järjestelmä- ja liiketoimintataulukoista.</span><span class="sxs-lookup"><span data-stu-id="625f9-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="625f9-105">Sivulla on tietoja erityisesti taulukoiden sisältämien tietojen määrästä.</span><span class="sxs-lookup"><span data-stu-id="625f9-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="625f9-106">Näistä tiedoista on hyötyä suorituskykyongelmien vianmäärityksessä, sillä se näyttää tietojen koon jakautumisen eri taulukoissa.</span><span class="sxs-lookup"><span data-stu-id="625f9-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="625f9-107">Näyttää taulukon tiedot</span><span class="sxs-lookup"><span data-stu-id="625f9-107">Viewing table information</span></span>

<span data-ttu-id="625f9-108">Avataksesi tämän sivun, valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Taulukon tiedot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="625f9-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="625f9-109">Seuraavassa taulukossa kuvataan kunkin taulukon tiedot:</span><span class="sxs-lookup"><span data-stu-id="625f9-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="625f9-110">Sarake</span><span class="sxs-lookup"><span data-stu-id="625f9-110">Column</span></span>|<span data-ttu-id="625f9-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="625f9-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="625f9-112">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="625f9-112">Company Name</span></span>|<span data-ttu-id="625f9-113">Sen yrityksen nimi, jos sellainen on, johon taulukko kuuluu.</span><span class="sxs-lookup"><span data-stu-id="625f9-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="625f9-114">Taulukon nimi</span><span class="sxs-lookup"><span data-stu-id="625f9-114">Table Name</span></span>|<span data-ttu-id="625f9-115">Taulukon nimi.</span><span class="sxs-lookup"><span data-stu-id="625f9-115">The name of the table.</span></span>|
|<span data-ttu-id="625f9-116">Taulukon nro</span><span class="sxs-lookup"><span data-stu-id="625f9-116">Table No.</span></span>|<span data-ttu-id="625f9-117">Taulukon tunnus</span><span class="sxs-lookup"><span data-stu-id="625f9-117">The ID of the table</span></span>|
|<span data-ttu-id="625f9-118">Ei.</span><span class="sxs-lookup"><span data-stu-id="625f9-118">No.</span></span> <span data-ttu-id="625f9-119">tietuetta</span><span class="sxs-lookup"><span data-stu-id="625f9-119">of Records</span></span>|<span data-ttu-id="625f9-120">Taulukkoon tallennettujen tietueiden kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="625f9-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="625f9-121">Tietueen koko</span><span class="sxs-lookup"><span data-stu-id="625f9-121">Record Size</span></span>|<span data-ttu-id="625f9-122">Tietueiden keskimääräinen koko kilotavuina/tietueessa.</span><span class="sxs-lookup"><span data-stu-id="625f9-122">The average record size in KB/record.</span></span> <span data-ttu-id="625f9-123">Arvo lasketaan seuraavan kaavan avulla: 1024 (koko)/(Tietueiden</span><span class="sxs-lookup"><span data-stu-id="625f9-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="625f9-124">määrä).</span><span class="sxs-lookup"><span data-stu-id="625f9-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="625f9-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="625f9-125">See Also</span></span>

[<span data-ttu-id="625f9-126">Sivujen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="625f9-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="625f9-127">Suorituskykyartikkelit kehittäjille</span><span class="sxs-lookup"><span data-stu-id="625f9-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
