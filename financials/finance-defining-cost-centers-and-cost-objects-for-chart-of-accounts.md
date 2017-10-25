---
title: "Tilikartan kustannuspaikkojen ja kustannuskohteiden määrittäminen | Microsoft Docs"
description: "Voit siirtää kulu- ja tuottotapahtumat automaattisesti pääkirjanpidosta kustannuslaskentaan joko jokaisen pääkirjanpidon kirjauksen tai eräajon yhteydessä. Kun teet siirron, järjestelmä siirtää vain tapahtumat, jotka on jo linkitetty kustannuspaikkaan tai kustannuskohteeseen. Muodosta mielekäs siirto varmistamalla, että kustannuspaikat ja kustannuskohdeet on asianmukaisesti määritetty."
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
ms.openlocfilehash: 0a3b89e2d2a59aa3434e747976437f24860be408
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="244f4-105">Kustannuspaikkojen ja kustannuskohteiden määrittäminen tilikarttaan</span><span class="sxs-lookup"><span data-stu-id="244f4-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="244f4-106">Voit siirtää kulu- ja tuottotapahtumat automaattisesti pääkirjanpidosta kustannuslaskentaan joko jokaisen pääkirjanpidon kirjauksen tai eräajon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="244f4-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="244f4-107">Kun teet siirron, [!INCLUDE[d365fin](includes/d365fin_md.md)] vain siirtää tapahtumat, jotka on jo linkitetty kustannuspaikkaan tai kustannuskohteeseen.</span><span class="sxs-lookup"><span data-stu-id="244f4-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="244f4-108">Muodosta mielekäs siirto varmistamalla, että kustannuspaikat ja kustannuskohdeet on asianmukaisesti määritetty.</span><span class="sxs-lookup"><span data-stu-id="244f4-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="244f4-109">Dimension oletusarvojen määrittäminen pääkirjanpitotilejä varten</span><span class="sxs-lookup"><span data-stu-id="244f4-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="244f4-110">Voit määrittää kunkin pääkirjanpidon tilin dimension oletusarvot **Oletusdimensio**-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="244f4-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="244f4-111">Seuraavassa esimerkissä näytetään, miten määritetään, että KP-tilin kirjauksia tehdessä tulee aina olla OSASTO-kustannuspaikka eikä koskaan PROJEKTI-kustannuskohde.</span><span class="sxs-lookup"><span data-stu-id="244f4-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="244f4-112">**Dimensiokoodi**</span><span class="sxs-lookup"><span data-stu-id="244f4-112">**Dimension Code**</span></span>|<span data-ttu-id="244f4-113">**Arvon kirjaaminen**</span><span class="sxs-lookup"><span data-stu-id="244f4-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="244f4-114">Osaston</span><span class="sxs-lookup"><span data-stu-id="244f4-114">Department</span></span>|<span data-ttu-id="244f4-115">Koodi pakollinen</span><span class="sxs-lookup"><span data-stu-id="244f4-115">Code Mandatory</span></span>|  
|<span data-ttu-id="244f4-116">Projektin</span><span class="sxs-lookup"><span data-stu-id="244f4-116">Project</span></span>|<span data-ttu-id="244f4-117">Ei koodia</span><span class="sxs-lookup"><span data-stu-id="244f4-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="244f4-118">Dimensioarvojen määrittäminen yleiskustannuksille ja suorille kustannuksille</span><span class="sxs-lookup"><span data-stu-id="244f4-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="244f4-119">Voit siirtää yleiskustannukset kustannuspaikkaan ja suorat kustannukset kustannuskohteeseen.</span><span class="sxs-lookup"><span data-stu-id="244f4-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="244f4-120">Seuraavassa taulukossa näytetään dimension asetusarvojen optimaalinen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="244f4-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="244f4-121">Siirrä kohteeseen</span><span class="sxs-lookup"><span data-stu-id="244f4-121">Transfer To</span></span>|<span data-ttu-id="244f4-122">Kustannuspaikan kirjaus</span><span class="sxs-lookup"><span data-stu-id="244f4-122">Cost Center Posting</span></span>|<span data-ttu-id="244f4-123">Kustannuskohteen kirjaus</span><span class="sxs-lookup"><span data-stu-id="244f4-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="244f4-124">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="244f4-124">Cost Center</span></span>|<span data-ttu-id="244f4-125">Koodi pakollinen</span><span class="sxs-lookup"><span data-stu-id="244f4-125">Code Mandatory</span></span>|<span data-ttu-id="244f4-126">Ei koodia</span><span class="sxs-lookup"><span data-stu-id="244f4-126">No Code</span></span>|  
|<span data-ttu-id="244f4-127">Kustannuskohde</span><span class="sxs-lookup"><span data-stu-id="244f4-127">Cost Object</span></span>|<span data-ttu-id="244f4-128">Ei koodia</span><span class="sxs-lookup"><span data-stu-id="244f4-128">No Code</span></span>|<span data-ttu-id="244f4-129">Koodi pakollinen</span><span class="sxs-lookup"><span data-stu-id="244f4-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="244f4-130">Varmista, että kirjanpitoon ennalta määritetty kustannuspaikka ja kustannusobjekti siirretään automaattisesti kustannuslaskentaan, valitsemalla **Tarkista KP-kirjaukset** -valintaruutu Kustannuslaskennan asetukset -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="244f4-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="244f4-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="244f4-131">See Also</span></span>  
[<span data-ttu-id="244f4-132">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="244f4-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="244f4-133">[Kustannuspaikkojen luominen](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="244f4-133">[How to: Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="244f4-134">Kustannuskohteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="244f4-134">How to: Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="244f4-135">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="244f4-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

