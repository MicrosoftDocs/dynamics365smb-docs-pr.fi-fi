---
title: "Vakiokustannusten päivittäminen | Microsoft Docs"
description: "Sinun täytyy säännöllisesti päivittää komponenttien vakiokustannukset ja vyöryttää uudet kustannukset päänimikkeelle."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 1c23e82736060670673e630f5eaa9de484083872
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-update-standard-costs"></a><span data-ttu-id="1ee4f-103">Vakiokustannusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="1ee4f-103">How to: Update Standard Costs</span></span>
<span data-ttu-id="1ee4f-104">Komponenttien vakiokustannukset on päivitettävä säännöllisesti ja uudet kustannukset on vyörytettävä päänimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="1ee4f-105">Prosessi sisältää yleensä seuraavat neljä vaihetta:</span><span class="sxs-lookup"><span data-stu-id="1ee4f-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="1ee4f-106">Päivitä kustannukset osa- ja kapasiteettitasolla.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="1ee4f-107">Lisätietoja on kohdassa **Ehdota nimikkeen vakiokust.** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="1ee4f-108">Yhdistä ja kokoa osa- ja kapasiteettikustannukset laskeaksesi nimikkeiden tuotannon tai kokoonpanon kokonaiskustannuksen.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="1ee4f-109">Ota käyttöön edellisten eräajojen aikana syötetyt vakiokustannukset.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="1ee4f-110">Vakiokustannukset eivät tule voimaan, ennen kuin ne on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="1ee4f-111">Lisätietoja on ohjeaiheessa Ota käyttöön vakiokustannusten muutokset.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="1ee4f-112">Ota muutokset käyttöön nimikkeen kortin **Yksikkökustannus**-kentän päivittämistä ja varaston uudelleenarvostuksen suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="1ee4f-113">Lisätietoja on kohdassa [Toimintaohje: Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="1ee4f-113">For more information, see [How to: Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="1ee4f-114">Lisätietoja on kohdassa [Tietoja vakiokustannusten laskennasta](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="1ee4f-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="1ee4f-115">Vakiokustannusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="1ee4f-115">To update standard costs</span></span>  
1.  <span data-ttu-id="1ee4f-116">Suorita **Muuta kustannuksia - Nimiketapahtumat** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="1ee4f-117">Suorita **Kirjaa varaston kust. KP:oon** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="1ee4f-118">Avaa **Vakiokust. työkirja** ja käytä vähintään yhtä seuraavista toiminnoista:</span><span class="sxs-lookup"><span data-stu-id="1ee4f-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="1ee4f-119">Suorita **Ehdota nimikkeen vakiokust.** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="1ee4f-120">Tarkasta tulokset ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="1ee4f-121">Suorita **Ehdota kapasiteetin vakiokustannusta** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="1ee4f-122">Tarkasta tulokset ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="1ee4f-123">Suorita **Vyörytä vakiokustannus** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="1ee4f-124">Tarkasta tulokset ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="1ee4f-125">Suorita **Ota käyttöön vakiokustannusten muutokset** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="1ee4f-126">Tarkasta ja kirjaa **Uudelleenarvostus pvk** -ikkuna, jonka tapahtumat on täytetty tämän prosessin aiemmissa vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="1ee4f-126">Review and post the **Revaluation Journal** window, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ee4f-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1ee4f-127">See Also</span></span>  
 <span data-ttu-id="1ee4f-128">[Tietoja standardikustannuksen laskemisesta](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="1ee4f-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="1ee4f-129">[Varaston kustannusten hallinta](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="1ee4f-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="1ee4f-130">[Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md) [[Rahoitus](finance.md)]</span><span class="sxs-lookup"><span data-stu-id="1ee4f-130">[Design Details: Costing Methods](design-details-costing-methods.md) [[Finance](finance.md)</span></span>  
 <span data-ttu-id="1ee4f-131">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ee4f-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

