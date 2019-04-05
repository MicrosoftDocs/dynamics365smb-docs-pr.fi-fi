---
title: Tilikartan kustannuspaikkojen ja kustannuskohteiden määrittäminen | Microsoft Docs
description: Voit siirtää kulu- ja tuottotapahtumat automaattisesti pääkirjanpidosta kustannuslaskentaan joko jokaisen pääkirjanpidon kirjauksen tai eräajon yhteydessä. Kun teet siirron, järjestelmä siirtää vain tapahtumat, jotka on jo linkitetty kustannuspaikkaan tai kustannuskohteeseen. Muodosta mielekäs siirto varmistamalla, että kustannuspaikat ja kustannuskohdeet on asianmukaisesti määritetty.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: b3ca863a9f4969046695e0cec16fedf6f5ac7aec
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795885"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="423d6-105">Kustannuspaikkojen ja kustannuskohteiden määrittäminen tilikarttaan</span><span class="sxs-lookup"><span data-stu-id="423d6-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="423d6-106">Voit siirtää kulu- ja tuottotapahtumat automaattisesti pääkirjanpidosta kustannuslaskentaan joko jokaisen pääkirjanpidon kirjauksen tai eräajon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="423d6-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="423d6-107">Kun teet siirron, [!INCLUDE[d365fin](includes/d365fin_md.md)] vain siirtää tapahtumat, jotka on jo linkitetty kustannuspaikkaan tai kustannuskohteeseen.</span><span class="sxs-lookup"><span data-stu-id="423d6-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="423d6-108">Muodosta mielekäs siirto varmistamalla, että kustannuspaikat ja kustannuskohdeet on asianmukaisesti määritetty.</span><span class="sxs-lookup"><span data-stu-id="423d6-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="423d6-109">Dimension oletusarvojen määrittäminen pääkirjanpitotilejä varten</span><span class="sxs-lookup"><span data-stu-id="423d6-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="423d6-110">Voit määrittää kunkin pääkirjanpidon tilin dimension oletusarvot **Oletusdimensio**-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="423d6-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="423d6-111">Seuraavassa esimerkissä näytetään, miten määritetään, että KP-tilin kirjauksia tehdessä tulee aina olla OSASTO-kustannuspaikka eikä koskaan PROJEKTI-kustannuskohde.</span><span class="sxs-lookup"><span data-stu-id="423d6-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="423d6-112">**Dimensiokoodi**</span><span class="sxs-lookup"><span data-stu-id="423d6-112">**Dimension Code**</span></span>|<span data-ttu-id="423d6-113">**Arvon kirjaaminen**</span><span class="sxs-lookup"><span data-stu-id="423d6-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="423d6-114">Osaston</span><span class="sxs-lookup"><span data-stu-id="423d6-114">Department</span></span>|<span data-ttu-id="423d6-115">Koodi pakollinen</span><span class="sxs-lookup"><span data-stu-id="423d6-115">Code Mandatory</span></span>|  
|<span data-ttu-id="423d6-116">Projektin</span><span class="sxs-lookup"><span data-stu-id="423d6-116">Project</span></span>|<span data-ttu-id="423d6-117">Ei koodia</span><span class="sxs-lookup"><span data-stu-id="423d6-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="423d6-118">Dimensioarvojen määrittäminen yleiskustannuksille ja suorille kustannuksille</span><span class="sxs-lookup"><span data-stu-id="423d6-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="423d6-119">Voit siirtää yleiskustannukset kustannuspaikkaan ja suorat kustannukset kustannuskohteeseen.</span><span class="sxs-lookup"><span data-stu-id="423d6-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="423d6-120">Seuraavassa taulukossa näytetään dimension asetusarvojen optimaalinen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="423d6-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="423d6-121">Siirrä kohteeseen</span><span class="sxs-lookup"><span data-stu-id="423d6-121">Transfer To</span></span>|<span data-ttu-id="423d6-122">Kustannuspaikan kirjaus</span><span class="sxs-lookup"><span data-stu-id="423d6-122">Cost Center Posting</span></span>|<span data-ttu-id="423d6-123">Kustannuskohteen kirjaus</span><span class="sxs-lookup"><span data-stu-id="423d6-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="423d6-124">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="423d6-124">Cost Center</span></span>|<span data-ttu-id="423d6-125">Koodi pakollinen</span><span class="sxs-lookup"><span data-stu-id="423d6-125">Code Mandatory</span></span>|<span data-ttu-id="423d6-126">Ei koodia</span><span class="sxs-lookup"><span data-stu-id="423d6-126">No Code</span></span>|  
|<span data-ttu-id="423d6-127">Kustannuskohde</span><span class="sxs-lookup"><span data-stu-id="423d6-127">Cost Object</span></span>|<span data-ttu-id="423d6-128">Ei koodia</span><span class="sxs-lookup"><span data-stu-id="423d6-128">No Code</span></span>|<span data-ttu-id="423d6-129">Koodi pakollinen</span><span class="sxs-lookup"><span data-stu-id="423d6-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="423d6-130">Varmista, että kirjanpitoon ennalta määritetty kustannuspaikka ja kustannusobjekti siirretään automaattisesti kustannuslaskentaan, valitsemalla **Tarkista KP-kirjaukset** -valintaruutu Kustannuslaskennan asetukset -sivulla.</span><span class="sxs-lookup"><span data-stu-id="423d6-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="423d6-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="423d6-131">See Also</span></span>  
[<span data-ttu-id="423d6-132">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="423d6-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="423d6-133">Kustannuslaskennan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="423d6-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="423d6-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="423d6-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
