---
title: "Varastonarvostuksen ja kustannuslaskennan määrittäminen | Microsoft Docs"
description: "Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6d1d0da42bbc6bf186845648552eb639731759f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="30db3-103">Varastonarvostuksen ja kustannuslaskennan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="30db3-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="30db3-104">Voit varmistaa, että varastokustannukset kirjataan oikein, määrittämällä tietyt kentät ja ikkunat ennen nimiketapahtumien tekemistä.</span><span class="sxs-lookup"><span data-stu-id="30db3-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="30db3-105">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="30db3-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="30db3-106">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="30db3-106">**To**</span></span>|<span data-ttu-id="30db3-107">**Katso**</span><span class="sxs-lookup"><span data-stu-id="30db3-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="30db3-108">Kustannuslaskentamenetelmän määrittäminen kullekin nimikkeelle. Valitun menetelmän mukaan määräytyy, miten nimikkeen saapuvia kustannuksia käytetään varaston arvon ja myytyjen tuotteiden kustannusten laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="30db3-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="30db3-109">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="30db3-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="30db3-110">Varmistaminen, että kustannus kirjataan automaattisesti pääkirjanpitoon aina, kun varastotapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="30db3-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="30db3-111">**Varastonhallinnan asetukset** -ikkunan **Automaattinen kustann. kirjaus** -kenttä</span><span class="sxs-lookup"><span data-stu-id="30db3-111">**Automatic Cost Posting** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="30db3-112">Varmistaminen, että oletetut kustannukset kirjataan pääkirjanpitoon, jotta väliaikaisilla KP-tileillä näkyy arvio erääntyvistä summista ja kaupattujen nimikkeiden kustannuksista ennen nimikkeiden varsinaista laskuttamista.</span><span class="sxs-lookup"><span data-stu-id="30db3-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="30db3-113">**Varastonhallinnan asetukset** -ikkunan **Oletettu kust. kirjaus KP:toon** -kenttä</span><span class="sxs-lookup"><span data-stu-id="30db3-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="30db3-114">Järjestelmän määrittäminen siten, että kustannusmuutokset päivittyvät automaattisesti aina varastotapahtumien kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="30db3-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="30db3-115">Nimikekustannusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="30db3-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="30db3-116">Määrittä, lasketaanko keskimääräinen hinta vain nimikettä kohden vai kutakin nimikettä kohden kussakin varastointiyksikössä ja kutakin nimikevarianttia kohden.</span><span class="sxs-lookup"><span data-stu-id="30db3-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="30db3-117">**Varastonhallinnan asetukset** -sivun **Keskim. kust. laskentatyyppi** -kenttä</span><span class="sxs-lookup"><span data-stu-id="30db3-117">**Average Cost Calc. Type** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="30db3-118">Keskimääräisen kustannuksen laskentamenetelmää käyttävien nimikkeiden painotetun keskimääräisen kustannuksen laskemiseen käytettävän ajanjakson valitseminen.</span><span class="sxs-lookup"><span data-stu-id="30db3-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="30db3-119">**Varastonhallinnan asetukset** -sivun **Keskimääräisen kustannuksen jakso** -kenttä</span><span class="sxs-lookup"><span data-stu-id="30db3-119">**Average Cost Period** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="30db3-120">Varastokausien määrittäminen varaston arvon pitkäaikaista hallintaa varten kieltämällä kirjaukset suljettuihin varastokausiin.</span><span class="sxs-lookup"><span data-stu-id="30db3-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="30db3-121">Varastokausien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="30db3-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="30db3-122">Varmista, että myyntipalautukset kohdistetaan alkuperäiseen lähtevään tapahtumaan varaston arvon säilyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="30db3-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="30db3-123">**Myynnit ja myyntisaamiset** -ikkunan **Todellisen kust. peruutt. pakollinen** -kenttä</span><span class="sxs-lookup"><span data-stu-id="30db3-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** page</span></span>|  
|<span data-ttu-id="30db3-124">Varmista, että ostopalautukset kohdistetaan alkuperäiseen saapuvaan tapahtumaan varaston arvon säilyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="30db3-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="30db3-125">**Ostot ja ostovelat** -ikkunan **Todellisen kust. peruutt. pakollinen** -kenttä</span><span class="sxs-lookup"><span data-stu-id="30db3-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** page</span></span>|
|<span data-ttu-id="30db3-126">Nimikehintojen ja vakiokustannusten muuttamisessa tai ehdottamisessa käytettävien pyöristyssääntöjen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="30db3-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="30db3-127">**Pyöristystapa**-sivu</span><span class="sxs-lookup"><span data-stu-id="30db3-127">**Rounding Method** page</span></span>|  

## <a name="see-also"></a><span data-ttu-id="30db3-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="30db3-128">See Also</span></span>  
[<span data-ttu-id="30db3-129">Varaston kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="30db3-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="30db3-130">Finance and Operations, Business editionin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="30db3-130">Working with Finance and Operations, Business edition</span></span>](ui-work-product.md)  
[<span data-ttu-id="30db3-131">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="30db3-131">Finance</span></span>](finance.md)  

