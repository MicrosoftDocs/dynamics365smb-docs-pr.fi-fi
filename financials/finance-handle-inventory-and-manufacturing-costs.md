---
title: "Varaston ja tuotannon kustannusten käsitteleminen | Microsoft Docs"
description: "Vaikka useat kustannuslaskennan toiminnot (kuten tapahtuman kohdistus ja automaattinen kustannusten muuttaminen) tapahtuvat taustalla olevissa prosesseissa ilman käyttäjän toimia, useat kentät, ikkunat ja raportit on tarkoitettu käyttäjille, jotka hallitsevat nimikkeiden tai toimintojen kustannuksia suoraan tai epäsuorasti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7f607e36c9201304d9777cebf4a4418914252768
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="handling-inventory-and-manufacturing-costs"></a><span data-ttu-id="409b9-103">Varaston ja tuotannon kustannusten käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="409b9-103">Handling Inventory and Manufacturing Costs</span></span>
<span data-ttu-id="409b9-104">Vaikka useat kustannuslaskennan toiminnot (kuten tapahtuman kohdistus ja automaattinen kustannusten muuttaminen) tapahtuvat taustalla olevissa prosesseissa ilman käyttäjän toimia, useat kentät, ikkunat ja raportit on tarkoitettu käyttäjille, jotka hallitsevat nimikkeiden tai toimintojen kustannuksia suoraan tai epäsuorasti.</span><span class="sxs-lookup"><span data-stu-id="409b9-104">Although much of the cost accounting functionality is expressed in underlying processes with no user interaction, such as entry application and automatic cost adjustment, a number of fields, windows, and reports are aimed at users who directly or indirectly manage the cost of items or operations.</span></span>  

 <span data-ttu-id="409b9-105">Nimikekulujen liittäminen ostoasiakirjoihin on esimerkki epäsuorasta kustannuslaskentatehtävästä.</span><span class="sxs-lookup"><span data-stu-id="409b9-105">Assigning item charges to purchase documents is an example of an indirect cost accounting task.</span></span> <span data-ttu-id="409b9-106">Kokoonpanon tai tuotannon tuoterakenteen yksikkökustannuksen päivittäminen on esimerkki suorahkosta kustannuslaskentatehtävästä.</span><span class="sxs-lookup"><span data-stu-id="409b9-106">Updating the unit cost of assembly or production BOM item is an example of a more direct cost accounting task.</span></span>  

 <span data-ttu-id="409b9-107">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="409b9-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="409b9-108">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="409b9-108">**To**</span></span>|<span data-ttu-id="409b9-109">**Katso**</span><span class="sxs-lookup"><span data-stu-id="409b9-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="409b9-110">Nimikkeiden yksikkökustannusten kausittainen tai automaattinen päivittäminen mahdollisten kustannusmuutosten välittämiseksi saapuvista tapahtumista, esimerkiksi ostojen tai tuotannon tulostuksesta, vastaaviin lähteviin tapahtumiin, kuten kulutukseen tai siirtoihin.</span><span class="sxs-lookup"><span data-stu-id="409b9-110">Periodically or automatically update the unit cost of one or multiple items to forward any cost changes from inbound entries, such as those for purchases or production output, to the related outbound entries, such as consumption or transfers.</span></span>|[<span data-ttu-id="409b9-111">Nimikekustannusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="409b9-111">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="409b9-112">Keskimääräisen kustannuksen dynamiikan hyödyntäminen hinnoittelupäätösten tekemisessä tai tietojen syöttövirheiden aiheuttamien kustannusvaihteluiden seuraamisessa.</span><span class="sxs-lookup"><span data-stu-id="409b9-112">Get insight into average cost dynamics to make pricing decisions or to track cost fluctuations caused by data entry errors.</span></span>|[<span data-ttu-id="409b9-113">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="409b9-113">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="409b9-114">Tuotantonimikkeen vakiokustannuksen luominen määrittämällä kolme kustannuselementtiä: materiaalikustannus, kapasiteettikustannus ja alihankkijan kustannus.</span><span class="sxs-lookup"><span data-stu-id="409b9-114">Create a manufacturing item's standard cost by entering the three cost elements: material cost, capacity cost, and subcontractor cost.</span></span>|[<span data-ttu-id="409b9-115">Tietoja standardikustannuksen laskemisesta</span><span class="sxs-lookup"><span data-stu-id="409b9-115">About Calculating Standard Cost</span></span>](finance-about-calculating-standard-cost.md)|  
|<span data-ttu-id="409b9-116">Tuoterakenteen nimikkeen yksikkökustannuksen laskeminen sen komponenttien yksikkökustannusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="409b9-116">Calculate the unit cost of a BOM item based on the unit costs of its underlying components.</span></span>|[<span data-ttu-id="409b9-117">Tuoterakenteen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="409b9-117">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)|  
|<span data-ttu-id="409b9-118">Tuotetun nimikkeen kustannuslaskentaelinkaaren päättäminen muuttamalla kustannuksia ja täsmäyttämällä arvotapahtumat pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="409b9-118">Complete the costing life cycle of a produced item by adjusting the costs and reconciling the value entries with the general ledger.</span></span>|[<span data-ttu-id="409b9-119">Tietoja valmiin tuotantotilauksen kustannuksista</span><span class="sxs-lookup"><span data-stu-id="409b9-119">About Finished Production Order Costs</span></span>](finance-about-finished-production-order-costs.md)|  
|<span data-ttu-id="409b9-120">Varastossa olevan nimikkeen tai yksittäisen nimiketapahtuman, kuten ostotapahtuman, arvon muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="409b9-120">Change the value of an item in inventory or the value of one item ledger entry, such as a purchase transaction.</span></span>|[<span data-ttu-id="409b9-121">Varaston uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="409b9-121">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="409b9-122">Nimikkeen kohdistuksen peruuttaminen manuaalisesti tai ohjelman luomien nimiketapahtumien kohdistaminen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="409b9-122">Manually undo an item application or reapply item ledger entries created by the program.</span></span>|[<span data-ttu-id="409b9-123">Nimiketapahtumien poistaminen ja uudelleenkohdistaminen</span><span class="sxs-lookup"><span data-stu-id="409b9-123">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)|  
|<span data-ttu-id="409b9-124">Luo nimikepäiväkirjan **Kohdistukset tapahtumista** -kentän avulla manuaalisesti kiinteä kohdistus saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille.</span><span class="sxs-lookup"><span data-stu-id="409b9-124">Use the **Applies-from Entry** field in the item journal to manually create a fixed application between an inbound transaction and the original outbound transaction.</span></span>|[<span data-ttu-id="409b9-125">Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="409b9-125">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a><span data-ttu-id="409b9-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="409b9-126">See Also</span></span>  
<span data-ttu-id="409b9-127">[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)</span><span class="sxs-lookup"><span data-stu-id="409b9-127">[Manage Inventory Costs](finance-manage-inventory-costs.md)
[Design Details: Inventory Costing](design-details-inventory-costing.md)</span></span>

