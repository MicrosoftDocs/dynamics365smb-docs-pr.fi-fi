---
title: Dimensioyhdistelmän tapahtumien yleiskatsaus | Microsoft Docs
description: Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan Dynamics 365:ssä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b9b69b539228e92776e1a7ee4c2fb491b20c1a15
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787994"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="9f29e-103">Dimensioyhdistelmätapahtumien yleiskuva</span><span class="sxs-lookup"><span data-stu-id="9f29e-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="9f29e-104">Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9f29e-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="9f29e-105">Dimensioyhdistelmät</span><span class="sxs-lookup"><span data-stu-id="9f29e-105">Dimension Sets</span></span>  
<span data-ttu-id="9f29e-106">Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="9f29e-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="9f29e-107">Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="9f29e-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="9f29e-108">Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa.</span><span class="sxs-lookup"><span data-stu-id="9f29e-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="9f29e-109">Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="9f29e-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="9f29e-110">Seuraavassa esimerkissä näytetään dimensioyhdistelmä, jolla on kolme dimensioyhdistelmätapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="9f29e-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="9f29e-111">Dimensioyhdistelmä tunnistetaan dimensioyhdistelmän tunnuksella, joka on 108.</span><span class="sxs-lookup"><span data-stu-id="9f29e-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="9f29e-112">Dimensioyhdistelmän tunnus</span><span class="sxs-lookup"><span data-stu-id="9f29e-112">Dimension Set ID</span></span>|<span data-ttu-id="9f29e-113">Dimensiokoodi</span><span class="sxs-lookup"><span data-stu-id="9f29e-113">Dimension Code</span></span>|<span data-ttu-id="9f29e-114">Dimension arvokoodi</span><span class="sxs-lookup"><span data-stu-id="9f29e-114">Dimension Value Code</span></span>|<span data-ttu-id="9f29e-115">Dimensioarvon nimi</span><span class="sxs-lookup"><span data-stu-id="9f29e-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="9f29e-116">108</span><span class="sxs-lookup"><span data-stu-id="9f29e-116">108</span></span>|<span data-ttu-id="9f29e-117">ALUE</span><span class="sxs-lookup"><span data-stu-id="9f29e-117">AREA</span></span>|<span data-ttu-id="9f29e-118">70</span><span class="sxs-lookup"><span data-stu-id="9f29e-118">70</span></span>|<span data-ttu-id="9f29e-119">Pohjois-Amerikka</span><span class="sxs-lookup"><span data-stu-id="9f29e-119">America North</span></span>|  
|<span data-ttu-id="9f29e-120">108</span><span class="sxs-lookup"><span data-stu-id="9f29e-120">108</span></span>|<span data-ttu-id="9f29e-121">YRITYSRYHMÄ</span><span class="sxs-lookup"><span data-stu-id="9f29e-121">BUSINESSGROUP</span></span>|<span data-ttu-id="9f29e-122">HOME</span><span class="sxs-lookup"><span data-stu-id="9f29e-122">HOME</span></span>|<span data-ttu-id="9f29e-123">Kotitalous</span><span class="sxs-lookup"><span data-stu-id="9f29e-123">Home</span></span>|  
|<span data-ttu-id="9f29e-124">108</span><span class="sxs-lookup"><span data-stu-id="9f29e-124">108</span></span>|<span data-ttu-id="9f29e-125">OSASTO</span><span class="sxs-lookup"><span data-stu-id="9f29e-125">DEPARTMENT</span></span>|<span data-ttu-id="9f29e-126">MYYNTI</span><span class="sxs-lookup"><span data-stu-id="9f29e-126">SALES</span></span>|<span data-ttu-id="9f29e-127">Myynti</span><span class="sxs-lookup"><span data-stu-id="9f29e-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="9f29e-128">Dimensioyhdistelmän tapahtumat</span><span class="sxs-lookup"><span data-stu-id="9f29e-128">Dimension Set Entries</span></span>  
<span data-ttu-id="9f29e-129">Dimensioyhdistelmät tallennetaan **Dimensioyhdistelmän tapahtuma** -taulukkoon dimensioyhdistelmätapahtumina, joilla on sama dimensioyhdistelmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="9f29e-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="9f29e-130">![Dimensiojoukon tapahtumien prosessi](media/dimensionentrynav7.png "Dimensiojoukon tapahtumien prosessi")</span><span class="sxs-lookup"><span data-stu-id="9f29e-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="9f29e-131">Kun luot uuden päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="9f29e-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="9f29e-132">Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="9f29e-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="9f29e-133">Kun muokkaat **Muokkaa dimensioyhdistelmän tapahtumia** -sivua ja suljet sen, tarkastus on suoritettu nähdäksesi onko dimensioarvojen yhdistelmä olemassa dimensionyhdistelmänä taulukossa.</span><span class="sxs-lookup"><span data-stu-id="9f29e-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="9f29e-134">Jos yhdistelmä tehdään taulukossa, vastaavan dimensioyhdistelmän tunnus liitetään päiväkirjariviin, asiakirjan otsikkoon tai asiakirjariville.</span><span class="sxs-lookup"><span data-stu-id="9f29e-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="9f29e-135">Muussa tapauksessa taulukkoon lisätään uusi dimensioyhdistelmä ja uuden dimensioyhdistelmä tunnus määritetään päiväkirjariville, asiakirjaotsikkoon tai asiakirjariville.</span><span class="sxs-lookup"><span data-stu-id="9f29e-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="9f29e-136">Codeunit 408 -dimension hallinta</span><span class="sxs-lookup"><span data-stu-id="9f29e-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="9f29e-137">Codeunit 408, dimension hallinta, on toimintokirjasto, joka käsittelee yleiset dimensioihin liittyvät tehtävät, kuten kopioinnin taulukosta toiseen tai yhdestä asiakirjasta toiseen.</span><span class="sxs-lookup"><span data-stu-id="9f29e-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="9f29e-138">Suorituskyvyn parantaminen</span><span class="sxs-lookup"><span data-stu-id="9f29e-138">Performance Improvement</span></span>  
<span data-ttu-id="9f29e-139">Määrittämällä dimensioyhdistelmän kerran tietokannassa tietokannan tilaa säästyy ja yleinen suorituskyky on entistä parempi.</span><span class="sxs-lookup"><span data-stu-id="9f29e-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9f29e-140">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9f29e-140">See Also</span></span>  
<span data-ttu-id="9f29e-141">[Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="9f29e-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="9f29e-142">[Rakennetiedot: taulukkorakenne](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="9f29e-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="9f29e-143">Rakennetiedot: Dimensioyhdistelmä-tapahtumat</span><span class="sxs-lookup"><span data-stu-id="9f29e-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   
