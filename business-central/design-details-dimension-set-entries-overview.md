---
title: "Dimensioyhdistelmän tapahtumien yleiskatsaus | Microsoft Docs"
description: "Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan Dynamics 365:ssä."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1113f371caf00b693144d0ea6f74aed49bbbc9df
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="b83a5-103">Dimensioyhdistelmätapahtumien yleiskuva</span><span class="sxs-lookup"><span data-stu-id="b83a5-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="b83a5-104">Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b83a5-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
## <a name="dimension-sets"></a><span data-ttu-id="b83a5-105">Dimensioyhdistelmät</span><span class="sxs-lookup"><span data-stu-id="b83a5-105">Dimension Sets</span></span>  
<span data-ttu-id="b83a5-106">Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="b83a5-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="b83a5-107">Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="b83a5-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="b83a5-108">Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa.</span><span class="sxs-lookup"><span data-stu-id="b83a5-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="b83a5-109">Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="b83a5-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  
  
<span data-ttu-id="b83a5-110">Seuraavassa esimerkissä näytetään dimensioyhdistelmä, jolla on kolme dimensioyhdistelmätapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="b83a5-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="b83a5-111">Dimensioyhdistelmä tunnistetaan dimensioyhdistelmän tunnuksella, joka on 108.</span><span class="sxs-lookup"><span data-stu-id="b83a5-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  
  
|<span data-ttu-id="b83a5-112">Dimensioyhdistelmän tunnus</span><span class="sxs-lookup"><span data-stu-id="b83a5-112">Dimension Set ID</span></span>|<span data-ttu-id="b83a5-113">Dimensiokoodi</span><span class="sxs-lookup"><span data-stu-id="b83a5-113">Dimension Code</span></span>|<span data-ttu-id="b83a5-114">Dimension arvokoodi</span><span class="sxs-lookup"><span data-stu-id="b83a5-114">Dimension Value Code</span></span>|<span data-ttu-id="b83a5-115">Dimensioarvon nimi</span><span class="sxs-lookup"><span data-stu-id="b83a5-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="b83a5-116">108</span><span class="sxs-lookup"><span data-stu-id="b83a5-116">108</span></span>|<span data-ttu-id="b83a5-117">ALUE</span><span class="sxs-lookup"><span data-stu-id="b83a5-117">AREA</span></span>|<span data-ttu-id="b83a5-118">70</span><span class="sxs-lookup"><span data-stu-id="b83a5-118">70</span></span>|<span data-ttu-id="b83a5-119">Pohjois-Amerikka</span><span class="sxs-lookup"><span data-stu-id="b83a5-119">America North</span></span>|  
|<span data-ttu-id="b83a5-120">108</span><span class="sxs-lookup"><span data-stu-id="b83a5-120">108</span></span>|<span data-ttu-id="b83a5-121">YRITYSRYHMÄ</span><span class="sxs-lookup"><span data-stu-id="b83a5-121">BUSINESSGROUP</span></span>|<span data-ttu-id="b83a5-122">HOME</span><span class="sxs-lookup"><span data-stu-id="b83a5-122">HOME</span></span>|<span data-ttu-id="b83a5-123">Kotitalous</span><span class="sxs-lookup"><span data-stu-id="b83a5-123">Home</span></span>|  
|<span data-ttu-id="b83a5-124">108</span><span class="sxs-lookup"><span data-stu-id="b83a5-124">108</span></span>|<span data-ttu-id="b83a5-125">OSASTO</span><span class="sxs-lookup"><span data-stu-id="b83a5-125">DEPARTMENT</span></span>|<span data-ttu-id="b83a5-126">MYYNTI</span><span class="sxs-lookup"><span data-stu-id="b83a5-126">SALES</span></span>|<span data-ttu-id="b83a5-127">Myynti</span><span class="sxs-lookup"><span data-stu-id="b83a5-127">Sales</span></span>|  
  
## <a name="dimension-set-entries"></a><span data-ttu-id="b83a5-128">Dimensioyhdistelmän tapahtumat</span><span class="sxs-lookup"><span data-stu-id="b83a5-128">Dimension Set Entries</span></span>  
<span data-ttu-id="b83a5-129">Dimensioyhdistelmät tallennetaan **Dimensioyhdistelmän tapahtuma** -taulukkoon dimensioyhdistelmätapahtumina, joilla on sama dimensioyhdistelmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="b83a5-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  
  
<span data-ttu-id="b83a5-130">![Dimensiotapahtumien yleiskuvaus](media/dimensionentrynav7.png "DimensionEntryNAV7")</span><span class="sxs-lookup"><span data-stu-id="b83a5-130">![Dimension Entry overview](media/dimensionentrynav7.png "DimensionEntryNAV7")</span></span>  
  
<span data-ttu-id="b83a5-131">Kun luot uuden päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="b83a5-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="b83a5-132">Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="b83a5-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  
  
<span data-ttu-id="b83a5-133">Kun muokkaat ja suljet **Muokkaa dimensioyhdistelmän tapahtumia** -ikkunan, tarkastus on suoritettu nähdäksesi onko dimensioarvojen yhdistelmä olemassa dimensionyhdistelmänä taulukossa.</span><span class="sxs-lookup"><span data-stu-id="b83a5-133">When you edit and close the **Edit Dimension Set Entries** window, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="b83a5-134">Jos yhdistelmä tehdään taulukossa, vastaavan dimensioyhdistelmän tunnus liitetään päiväkirjariviin, asiakirjan otsikkoon tai asiakirjariville.</span><span class="sxs-lookup"><span data-stu-id="b83a5-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="b83a5-135">Muussa tapauksessa taulukkoon lisätään uusi dimensioyhdistelmä ja uuden dimensioyhdistelmä tunnus määritetään päiväkirjariville, asiakirjaotsikkoon tai asiakirjariville.</span><span class="sxs-lookup"><span data-stu-id="b83a5-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>  
  
## <a name="performance-improvement"></a><span data-ttu-id="b83a5-136">Suorituskyvyn parantaminen</span><span class="sxs-lookup"><span data-stu-id="b83a5-136">Performance Improvement</span></span>  
<span data-ttu-id="b83a5-137">Määrittämällä dimensioyhdistelmän kerran tietokannassa tietokannan tilaa säästyy ja yleinen suorituskyky on entistä parempi.</span><span class="sxs-lookup"><span data-stu-id="b83a5-137">By storing dimension sets once in the database, database space is preserved, and overall performance is improved.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b83a5-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b83a5-138">See Also</span></span>  
<span data-ttu-id="b83a5-139">[Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="b83a5-139">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="b83a5-140">[Rakennetiedot: taulukkorakenne](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="b83a5-140">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
<span data-ttu-id="b83a5-141">[Rakennetiedot: koodiyksikön 408 dimension hallinta](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="b83a5-141">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
<span data-ttu-id="b83a5-142">[Rakennetiedot: koodiesimerkkejä muuttuneista kuvioista muutoksissa](design-details-code-examples-of-changed-patterns-in-modifications.md) </span><span class="sxs-lookup"><span data-stu-id="b83a5-142">[Design Details: Code Examples of Changed Patterns in Modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span></span>  
[<span data-ttu-id="b83a5-143">Rakennetiedot: dimensioyhdistelmä-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="b83a5-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   

