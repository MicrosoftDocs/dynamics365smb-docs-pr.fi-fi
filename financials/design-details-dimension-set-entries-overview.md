---
title: "Dimensioyhdistelmän tapahtumien yleiskatsaus | Microsoft Docs"
description: "Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan Dynamics 365:ssä."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 78e98bcbc88ffb38d5da3f5089d124d915585d91
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="1ecb1-103">Dimensioyhdistelmätapahtumien yleiskuva</span><span class="sxs-lookup"><span data-stu-id="1ecb1-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="1ecb1-104">Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1ecb1-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
## <a name="dimension-sets"></a><span data-ttu-id="1ecb1-105">Dimensioyhdistelmät</span><span class="sxs-lookup"><span data-stu-id="1ecb1-105">Dimension Sets</span></span>  
<span data-ttu-id="1ecb1-106">Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="1ecb1-107">Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="1ecb1-108">Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="1ecb1-109">Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  
  
<span data-ttu-id="1ecb1-110">Seuraavassa esimerkissä näytetään dimensioyhdistelmä, jolla on kolme dimensioyhdistelmätapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="1ecb1-111">Dimensioyhdistelmä tunnistetaan dimensioyhdistelmän tunnuksella, joka on 108.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  
  
|<span data-ttu-id="1ecb1-112">Dimensioyhdistelmän tunnus</span><span class="sxs-lookup"><span data-stu-id="1ecb1-112">Dimension Set ID</span></span>|<span data-ttu-id="1ecb1-113">Dimensiokoodi</span><span class="sxs-lookup"><span data-stu-id="1ecb1-113">Dimension Code</span></span>|<span data-ttu-id="1ecb1-114">Dimension arvokoodi</span><span class="sxs-lookup"><span data-stu-id="1ecb1-114">Dimension Value Code</span></span>|<span data-ttu-id="1ecb1-115">Dimensioarvon nimi</span><span class="sxs-lookup"><span data-stu-id="1ecb1-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="1ecb1-116">108</span><span class="sxs-lookup"><span data-stu-id="1ecb1-116">108</span></span>|<span data-ttu-id="1ecb1-117">ALUE</span><span class="sxs-lookup"><span data-stu-id="1ecb1-117">AREA</span></span>|<span data-ttu-id="1ecb1-118">70</span><span class="sxs-lookup"><span data-stu-id="1ecb1-118">70</span></span>|<span data-ttu-id="1ecb1-119">Pohjois-Amerikka</span><span class="sxs-lookup"><span data-stu-id="1ecb1-119">America North</span></span>|  
|<span data-ttu-id="1ecb1-120">108</span><span class="sxs-lookup"><span data-stu-id="1ecb1-120">108</span></span>|<span data-ttu-id="1ecb1-121">YRITYSRYHMÄ</span><span class="sxs-lookup"><span data-stu-id="1ecb1-121">BUSINESSGROUP</span></span>|<span data-ttu-id="1ecb1-122">HOME</span><span class="sxs-lookup"><span data-stu-id="1ecb1-122">HOME</span></span>|<span data-ttu-id="1ecb1-123">Kotitalous</span><span class="sxs-lookup"><span data-stu-id="1ecb1-123">Home</span></span>|  
|<span data-ttu-id="1ecb1-124">108</span><span class="sxs-lookup"><span data-stu-id="1ecb1-124">108</span></span>|<span data-ttu-id="1ecb1-125">OSASTO</span><span class="sxs-lookup"><span data-stu-id="1ecb1-125">DEPARTMENT</span></span>|<span data-ttu-id="1ecb1-126">MYYNTI</span><span class="sxs-lookup"><span data-stu-id="1ecb1-126">SALES</span></span>|<span data-ttu-id="1ecb1-127">Myynti</span><span class="sxs-lookup"><span data-stu-id="1ecb1-127">Sales</span></span>|  
  
## <a name="dimension-set-entries"></a><span data-ttu-id="1ecb1-128">Dimensioyhdistelmän tapahtumat</span><span class="sxs-lookup"><span data-stu-id="1ecb1-128">Dimension Set Entries</span></span>  
<span data-ttu-id="1ecb1-129">Dimensioyhdistelmät tallennetaan **Dimensioyhdistelmän tapahtuma** -taulukkoon dimensioyhdistelmätapahtumina, joilla on sama dimensioyhdistelmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  
  
<span data-ttu-id="1ecb1-130">![Dimensiotapahtumien yleiskuvaus](media/dimensionentrynav7.png "DimensionEntryNAV7")</span><span class="sxs-lookup"><span data-stu-id="1ecb1-130">![Dimension Entry overview](media/dimensionentrynav7.png "DimensionEntryNAV7")</span></span>  
  
<span data-ttu-id="1ecb1-131">Kun luot uuden päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="1ecb1-132">Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  
  
<span data-ttu-id="1ecb1-133">Kun muokkaat ja suljet **Muokkaa dimensioyhdistelmän tapahtumia** -ikkunan, tarkastus on suoritettu nähdäksesi onko dimensioarvojen yhdistelmä olemassa dimensionyhdistelmänä taulukossa.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-133">When you edit and close the **Edit Dimension Set Entries** window, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="1ecb1-134">Jos yhdistelmä tehdään taulukossa, vastaavan dimensioyhdistelmän tunnus liitetään päiväkirjariviin, asiakirjan otsikkoon tai asiakirjariville.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="1ecb1-135">Muussa tapauksessa taulukkoon lisätään uusi dimensioyhdistelmä ja uuden dimensioyhdistelmä tunnus määritetään päiväkirjariville, asiakirjaotsikkoon tai asiakirjariville.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>  
  
## <a name="performance-improvement"></a><span data-ttu-id="1ecb1-136">Suorituskyvyn parantaminen</span><span class="sxs-lookup"><span data-stu-id="1ecb1-136">Performance Improvement</span></span>  
<span data-ttu-id="1ecb1-137">Määrittämällä dimensioyhdistelmän kerran tietokannassa tietokannan tilaa säästyy ja yleinen suorituskyky on entistä parempi.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-137">By storing dimension sets once in the database, database space is preserved, and overall performance is improved.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ecb1-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1ecb1-138">See Also</span></span>  
<span data-ttu-id="1ecb1-139">[Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="1ecb1-139">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="1ecb1-140">[Rakennetiedot: taulukkorakenne](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="1ecb1-140">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
<span data-ttu-id="1ecb1-141">[Rakennetiedot: koodiyksikön 408 dimension hallinta](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="1ecb1-141">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
<span data-ttu-id="1ecb1-142">[Rakennetiedot: koodiesimerkkejä muuttuneista kuvioista muutoksissa](design-details-code-examples-of-changed-patterns-in-modifications.md) </span><span class="sxs-lookup"><span data-stu-id="1ecb1-142">[Design Details: Code Examples of Changed Patterns in Modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span></span>  
[<span data-ttu-id="1ecb1-143">Rakennetiedot: dimensioyhdistelmä-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="1ecb1-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   

