---
title: "Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin | Microsoft Docs"
description: "On tärkeää ymmärtää ehdot, joiden mukaan pääkirjanpidon tapahtumat siirretään kustannustapahtumiin. **Siirrä KP-tapahtumat kustannuslaskentaan** -eräajo käyttää määrittää siirron aikana seuraavien kriteerien avulla, siirretäänkö pääkirjanpidon tapahtumat ja milloin ne mahdollisesti siirretään."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 59faad50504bff05e6cdb1c78d00553e85faf47e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="3a386-104">Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin</span><span class="sxs-lookup"><span data-stu-id="3a386-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="3a386-105">On tärkeää ymmärtää ehdot, joiden mukaan pääkirjanpidon tapahtumat siirretään kustannustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="3a386-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="3a386-106">Siirron aikana **Siirrä KP-tapahtumat kustannuslaskentaan** -eräajo käyttää seuraavia kriteerejä määrittääkseen, jos ja miten pääkirjanpidon tapahtumat siirretään.</span><span class="sxs-lookup"><span data-stu-id="3a386-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="3a386-107">Kirjanpitotapahtumat siirretään, jos:</span><span class="sxs-lookup"><span data-stu-id="3a386-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="3a386-108">Tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa tai kustannuskohdetta.</span><span class="sxs-lookup"><span data-stu-id="3a386-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="3a386-109">Tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta.</span><span class="sxs-lookup"><span data-stu-id="3a386-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="3a386-110">Kustannuspaikka ratkaisee asian näiden tapahtumien kohdalla.</span><span class="sxs-lookup"><span data-stu-id="3a386-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="3a386-111">Näin vältetään tilanne, jossa kustannustyyppi näkyy sekä kustannuskohteessa että kustannuspaikassa ja näin ollen ne lasketaan tilastoihin kahdesti.</span><span class="sxs-lookup"><span data-stu-id="3a386-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="3a386-112">Asiakirjan numeroa ei ole tapahtumissa, joten kustannustapahtumissa näytetään asiakirjanumeron kohdalla 0000.</span><span class="sxs-lookup"><span data-stu-id="3a386-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="3a386-113">Tapahtumat siirretään kustannustyypille, jolla yhdistettyjä tapahtumia voidaan käsitellä, ja tapahtumat siirretään yhdistettynä joko kuukausittain tai päivittäin.</span><span class="sxs-lookup"><span data-stu-id="3a386-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="3a386-114">Kirjanpitotapahtumia ei siirretä, jos:</span><span class="sxs-lookup"><span data-stu-id="3a386-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="3a386-115">Tapahtumilla on dimensioarvot, jotka eivät vastaa kustannuspaikkaa tai kustannuskohdetta.</span><span class="sxs-lookup"><span data-stu-id="3a386-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="3a386-116">Tapahtumien summa on nolla.</span><span class="sxs-lookup"><span data-stu-id="3a386-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="3a386-117">Tapahtumissa on poistettu KP-tili.</span><span class="sxs-lookup"><span data-stu-id="3a386-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="3a386-118">Tapahtumissa on KP-tili, joka ei ole **Tuloslaskelma**-tyyppiä</span><span class="sxs-lookup"><span data-stu-id="3a386-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="3a386-119">Tapahtumissa on KP-tili, jolle ei ole määritetty kustannustyyppiä.</span><span class="sxs-lookup"><span data-stu-id="3a386-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="3a386-120">Tapahtumien kirjauspäivämäärä on ennen **KP-siirron alkamispäivämäärää**.</span><span class="sxs-lookup"><span data-stu-id="3a386-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="3a386-121">Tapahtumille on kirjattu sulkemispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="3a386-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="3a386-122">Tässä on tyypillisiä tapahtumia, jotka palauttavat tuloslaskelman saldon vuoden lopussa.</span><span class="sxs-lookup"><span data-stu-id="3a386-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3a386-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3a386-123">See Also</span></span>  
[<span data-ttu-id="3a386-124">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="3a386-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="3a386-125">[Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="3a386-125">[How to: Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="3a386-126">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="3a386-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="3a386-127">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="3a386-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="3a386-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3a386-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

