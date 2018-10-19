---
title: "Varastonarvostuksen ja kustannuslaskennan määrittäminen | Microsoft Docs"
description: "Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 296f660f2ca4dfe7a605d2990e18567c5062a482
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="6d95a-103">Varastonarvostuksen ja kustannuslaskennan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6d95a-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="6d95a-104">Voit varmistaa, että varastokustannukset kirjataan oikein, määrittämällä tietyt kentät ja ikkunat ennen nimiketapahtumien tekemistä.</span><span class="sxs-lookup"><span data-stu-id="6d95a-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="6d95a-105">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="6d95a-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="6d95a-106">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="6d95a-106">**To**</span></span>|<span data-ttu-id="6d95a-107">**Katso**</span><span class="sxs-lookup"><span data-stu-id="6d95a-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="6d95a-108">Kustannuslaskentamenetelmän määrittäminen kullekin nimikkeelle. Valitun menetelmän mukaan määräytyy, miten nimikkeen saapuvia kustannuksia käytetään varaston arvon ja myytyjen tuotteiden kustannusten laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="6d95a-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="6d95a-109">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="6d95a-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="6d95a-110">Varmistaminen, että kustannus kirjataan automaattisesti pääkirjanpitoon aina, kun varastotapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="6d95a-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="6d95a-111">**Varastonhallinnan asetukset** -ikkunan **Automaattinen kustann. kirjaus** -ikkuna</span><span class="sxs-lookup"><span data-stu-id="6d95a-111">**Automatic Cost Posting** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="6d95a-112">Varmistaminen, että oletetut kustannukset kirjataan pääkirjanpitoon, jotta väliaikaisilla KP-tileillä näkyy arvio erääntyvistä summista ja kaupattujen nimikkeiden kustannuksista ennen nimikkeiden varsinaista laskuttamista.</span><span class="sxs-lookup"><span data-stu-id="6d95a-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="6d95a-113">**Varastonhallinnan asetukset** -ikkunan **Oletettu kust. kirjaus KP:toon** -ikkuna</span><span class="sxs-lookup"><span data-stu-id="6d95a-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="6d95a-114">Järjestelmän määrittäminen siten, että kustannusmuutokset päivittyvät automaattisesti aina varastotapahtumien kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6d95a-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="6d95a-115">Nimikekustannusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="6d95a-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="6d95a-116">Määrittä, lasketaanko keskimääräinen hinta vain nimikettä kohden vai kutakin nimikettä kohden kussakin varastointiyksikössä ja kutakin nimikevarianttia kohden.</span><span class="sxs-lookup"><span data-stu-id="6d95a-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="6d95a-117">**Varastonhallinnan asetukset** -sivun **Keskim. kust. laskentatyyppi** -ikkuna</span><span class="sxs-lookup"><span data-stu-id="6d95a-117">**Average Cost Calc. Type** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="6d95a-118">Keskimääräisen kustannuksen laskentamenetelmää käyttävien nimikkeiden painotetun keskimääräisen kustannuksen laskemiseen käytettävän ajanjakson valitseminen.</span><span class="sxs-lookup"><span data-stu-id="6d95a-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="6d95a-119">**Varastonhallinnan asetukset** -sivun **Keskimääräisen kustannuksen jakso** -ikkuna</span><span class="sxs-lookup"><span data-stu-id="6d95a-119">**Average Cost Period** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="6d95a-120">Varastokausien määrittäminen varaston arvon pitkäaikaista hallintaa varten kieltämällä kirjaukset suljettuihin varastokausiin.</span><span class="sxs-lookup"><span data-stu-id="6d95a-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="6d95a-121">Varastokausien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="6d95a-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="6d95a-122">Varmista, että myyntipalautukset kohdistetaan alkuperäiseen lähtevään tapahtumaan varaston arvon säilyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="6d95a-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="6d95a-123">**Myynnit ja myyntisaamiset** -ikkunan **Todellisen kust. peruutt. pakollinen** -ikkuna</span><span class="sxs-lookup"><span data-stu-id="6d95a-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** window</span></span>|  
|<span data-ttu-id="6d95a-124">Varmista, että ostopalautukset kohdistetaan alkuperäiseen saapuvaan tapahtumaan varaston arvon säilyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="6d95a-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="6d95a-125">**Ostot ja ostovelat** -ikkunan **Todellisen kust. peruutt. pakollinen** -ikkuna</span><span class="sxs-lookup"><span data-stu-id="6d95a-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** window</span></span>|
|<span data-ttu-id="6d95a-126">Nimikehintojen ja vakiokustannusten muuttamisessa tai ehdottamisessa käytettävien pyöristyssääntöjen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="6d95a-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="6d95a-127">**Pyöristystapa**-ikkuna</span><span class="sxs-lookup"><span data-stu-id="6d95a-127">**Rounding Method** window</span></span>|  

## <a name="see-also"></a><span data-ttu-id="6d95a-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6d95a-128">See Also</span></span>  
[<span data-ttu-id="6d95a-129">Varaston kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="6d95a-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="6d95a-130">Business Central -sovelluksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6d95a-130">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="6d95a-131">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="6d95a-131">Finance</span></span>](finance.md)  

