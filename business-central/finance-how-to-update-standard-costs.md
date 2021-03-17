---
title: Vakiokustannusten päivittäminen | Microsoft Docs
description: Komponenttien vakiokustannukset on päivitettävä säännöllisesti ja uudet kustannukset on vyörytettävä päänimikkeelle.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: feeeae5202cfc5ab0bccf1552ce74f74708445d3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391522"
---
# <a name="update-standard-costs"></a><span data-ttu-id="1469d-103">Vakiokustannusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="1469d-103">Update Standard Costs</span></span>
<span data-ttu-id="1469d-104">Komponenttien vakiokustannukset on päivitettävä säännöllisesti ja uudet kustannukset on vyörytettävä päänimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="1469d-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="1469d-105">Prosessi sisältää yleensä seuraavat neljä vaihetta:</span><span class="sxs-lookup"><span data-stu-id="1469d-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="1469d-106">Päivitä kustannukset osa- ja kapasiteettitasolla.</span><span class="sxs-lookup"><span data-stu-id="1469d-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="1469d-107">Lisätietoja on kohdassa **Ehdota nimikkeen vakiokust.** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1469d-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="1469d-108">Yhdistä ja kokoa osa- ja kapasiteettikustannukset laskeaksesi nimikkeiden tuotannon tai kokoonpanon kokonaiskustannuksen.</span><span class="sxs-lookup"><span data-stu-id="1469d-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="1469d-109">Ota käyttöön edellisten eräajojen aikana syötetyt vakiokustannukset.</span><span class="sxs-lookup"><span data-stu-id="1469d-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="1469d-110">Vakiokustannukset eivät tule voimaan, ennen kuin ne on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1469d-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="1469d-111">Lisätietoja on ohjeaiheessa Ota käyttöön vakiokustannusten muutokset.</span><span class="sxs-lookup"><span data-stu-id="1469d-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="1469d-112">Ota muutokset käyttöön nimikkeen kortin **Yksikkökustannus**-kentän päivittämistä ja varaston uudelleenarvostuksen suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="1469d-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="1469d-113">Lisätietoja on kohdassa [Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="1469d-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="1469d-114">Lisätietoja on kohdassa [Tietoja vakiokustannusten laskennasta](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="1469d-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="1469d-115">Vakiokustannusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="1469d-115">To update standard costs</span></span>  
1.  <span data-ttu-id="1469d-116">Suorita **Muuta kustannuksia - Nimiketapahtumat** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1469d-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="1469d-117">Suorita **Kirjaa varaston kust. KP:oon** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1469d-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="1469d-118">Avaa **Vakiokust. työkirja** ja käytä vähintään yhtä seuraavista toiminnoista:</span><span class="sxs-lookup"><span data-stu-id="1469d-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="1469d-119">Suorita **Ehdota nimikkeen vakiokust.** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1469d-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="1469d-120">Tarkasta tulokset ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="1469d-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="1469d-121">Suorita **Ehdota kapasiteetin vakiokustannusta** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1469d-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="1469d-122">Tarkasta tulokset ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="1469d-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="1469d-123">Suorita **Vyörytä vakiokustannus** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1469d-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="1469d-124">Tarkasta tulokset ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="1469d-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="1469d-125">Suorita **Ota käyttöön vakiokustannusten muutokset** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1469d-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="1469d-126">Tarkasta ja kirjaa **Uudelleenarvostus pvk** -sivu, jonka tapahtumat on täytetty tämän prosessin aiemmissa vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="1469d-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1469d-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1469d-127">See Also</span></span>  
 <span data-ttu-id="1469d-128">[Tietoja standardikustannuksen laskemisesta](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="1469d-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="1469d-129">[Varaston kustannusten hallinta](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="1469d-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="1469d-130">[Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md) [Rahoitus](finance.md)</span><span class="sxs-lookup"><span data-stu-id="1469d-130">[Design Details: Costing Methods](design-details-costing-methods.md) [Finance](finance.md)</span></span>  
 <span data-ttu-id="1469d-131">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1469d-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]