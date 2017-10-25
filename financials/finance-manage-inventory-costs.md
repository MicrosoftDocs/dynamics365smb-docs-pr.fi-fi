---
title: Varaston kustannusten hallinta | Microsoft Docs
description: "Kustannushallinta, jota kutsutaan myös \"arvostukseksi\", käsittelee liiketoiminnan toimintokustannusten tallennusta ja raportointia. Se sisältää tuotanto- ja varastointikustannusten eli nimikkeiden arvon raportoinnin.."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8da779426dfd06519507796c995adcedcd40ac81
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="managing-inventory-costs"></a><span data-ttu-id="d837b-104">Varaston kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="d837b-104">Managing Inventory Costs</span></span>
<span data-ttu-id="d837b-105">Kustannushallinta, jota kutsutaan myös arvostukseksi, käsittelee liiketoimintakustannusten kirjaamista ja raportointia.</span><span class="sxs-lookup"><span data-stu-id="d837b-105">Cost management, also referred to as “costing”, is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="d837b-106">Se sisältää tuotanto- ja varastointikustannusten eli nimikkeiden arvon raportoinnin..</span><span class="sxs-lookup"><span data-stu-id="d837b-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>   

<span data-ttu-id="d837b-107">Tärkeintä on ymmärtää, että arvostusmenetelmät määrittävät, miten nimikkeet arvostetaan varastosta lähdön jälkeen, että kustannusten muuttaminen päivittää myytyjen tuotteiden kustannukset liittyvillä myynnin jälkeen kirjatuilla ostokustannuksilla ja että varaston arvot on kirjattava säännöllisesti erityisille KP-tileille.</span><span class="sxs-lookup"><span data-stu-id="d837b-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>

<span data-ttu-id="d837b-108">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="d837b-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="d837b-109">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="d837b-109">**To**</span></span>|<span data-ttu-id="d837b-110">**Katso**</span><span class="sxs-lookup"><span data-stu-id="d837b-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="d837b-111">[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in varaston kustannuslaskennan toiminnot. Ohjeaihe sisältää käsitteellisiä tietoja toimintoja koskevista periaatteista ja määrityksistä.</span><span class="sxs-lookup"><span data-stu-id="d837b-111">Read various conceptual information to understand the principles and definitions that govern the inventory costing accounting functionality in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span>|[<span data-ttu-id="d837b-112">Tietoja varaston arvostuksesta</span><span class="sxs-lookup"><span data-stu-id="d837b-112">About Inventory Costing</span></span>](finance-learn-about-costing.md)|  
|<span data-ttu-id="d837b-113">Määritä varastokaudet, arvostusmenetelmät ja pyöristystavat.</span><span class="sxs-lookup"><span data-stu-id="d837b-113">Set up inventory periods, costing methods, and rounding methods.</span></span>|[<span data-ttu-id="d837b-114">Varastonarvostuksen ja kustannuslaskennan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d837b-114">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)|
|<span data-ttu-id="d837b-115">Nosta tai laske vähintään yhden varaston nimikkeen arvoa kirjaamalla nimikkeen nykyinen laskettu arvo.</span><span class="sxs-lookup"><span data-stu-id="d837b-115">Appreciate or depreciate the value of one or more items in inventory by posting their current, calculated value.</span></span>|[<span data-ttu-id="d837b-116">Toimintaohje: Varaston uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="d837b-116">How to: Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="d837b-117">Muuta nimikekustannuksia automaattisesti tai manuaalisesti, kun haluat siirtää saapuvien tapahtumien kustannusmuutokset liittyviin lähteviin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="d837b-117">Adjust item costs, either automatically or manually, to forward cost changes from inbound entries to their related outbound entries.</span></span>|[<span data-ttu-id="d837b-118">Toimintaohje: Nimikekustannusten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="d837b-118">How to: Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|
|<span data-ttu-id="d837b-119">Käytä erityisiä kustannuslaskentatoimintoja nimiketoimintojen päivittäisissä nimiketapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="d837b-119">Use special costing functions for every-day item transactions in the item operations.</span></span>|[<span data-ttu-id="d837b-120">Varaston ja tuotannon kustannusten käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="d837b-120">Handling Inventory and Manufacturing Costs</span></span>](finance-handle-inventory-and-manufacturing-costs.md)|  
|<span data-ttu-id="d837b-121">Kokoonpanon ja tuotannon tuoterakenteiden komponenttien vakiokustannukset on päivitettävä säännöllisesti ja uudet kustannukset on vyörytettävä päänimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="d837b-121">Periodically update the standard costs of components, in assembly or production BOMs, and roll the new costs up to the parent item.</span></span>|[<span data-ttu-id="d837b-122">Vakiokustannusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="d837b-122">How to: Update Standard Costs</span></span>](finance-how-to-update-standard-costs.md)|
|<span data-ttu-id="d837b-123">Kauden lopun hallinta- ja raportointitehtävien toteuttaminen. Näitä tehtäviä ovat esimerkiksi varaston arvon laskeminen ja kustannusten kirjaaminen pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="d837b-123">Perform period-end control and reporting tasks, such calculate the value of inventory and post costs to the general ledger.</span></span>|[<span data-ttu-id="d837b-124">Kustannusten raportointi ja täsmäyttäminen pääkirjanpidon kanssa</span><span class="sxs-lookup"><span data-stu-id="d837b-124">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="d837b-125">Lisätietoja kustannuslaskentajärjestelmän kaikista mekanismeista.</span><span class="sxs-lookup"><span data-stu-id="d837b-125">Learn about all mechanisms in the costing system.</span></span>|[<span data-ttu-id="d837b-126">Rakennetiedot: Varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="d837b-126">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  

## <a name="see-also"></a><span data-ttu-id="d837b-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d837b-127">See Also</span></span>  
 [<span data-ttu-id="d837b-128">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="d837b-128">Finance</span></span>](finance.md)  
 <span data-ttu-id="d837b-129">[Vaihto-omaisuus](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="d837b-129">[Inventory](inventory-manage-inventory.md) </span></span>  
 <span data-ttu-id="d837b-130">[Myynti](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="d837b-130">[Sales](sales-manage-sales.md) </span></span>  
 [<span data-ttu-id="d837b-131">Osto</span><span class="sxs-lookup"><span data-stu-id="d837b-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="d837b-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d837b-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

