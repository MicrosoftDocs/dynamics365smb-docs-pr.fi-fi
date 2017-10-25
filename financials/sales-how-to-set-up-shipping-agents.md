---
title: "Kuljetusliikkeiden määrittäminen | Microsoft Docs"
description: "Voit määrittää koodin jokaiselle kuljetusliikkeelle, ja syöttää tietoja niistä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84a5d9eb8757dc82834c17327ffbb510cd15fa1a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shipping-agents"></a><span data-ttu-id="1015a-103">Kuljetusliikkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1015a-103">How to: Set Up Shipping Agents</span></span>
<span data-ttu-id="1015a-104">Voit määrittää koodin jokaiselle kuljetusliikkeelle ja antaa niitä koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="1015a-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="1015a-105">Jos syötät Internet-osoitteen kuljetusliikkeen kohdalle, ja jos kuljetusliike tarjoaa kollinseurantapalveluja Internetissä, voit käyttää ohjelman automaattista kollin seuranta -ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="1015a-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="1015a-106">Lisätietoja on kohdassa [Toimintaohje: Kollien seuraaminen](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="1015a-106">For more information, see [How to: Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="1015a-107">Kun määrität kuljetusliikkeitä myyntitilauksillesi, voit määrittää myös kunkin kuljetusliikkeen tarjoamat palvelut.</span><span class="sxs-lookup"><span data-stu-id="1015a-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="1015a-108">Voit määrittää rajoittamattoman määrän palveluita jokaiselle kuljetusliikkeelle ja voit määrittää toimitusajan jokaiselle palvelulle.</span><span class="sxs-lookup"><span data-stu-id="1015a-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="1015a-109">Kun olet määrittänyt kuljetusliikkeen palvelun myyntitilausriville, palvelun toimitusaika sisällytetään sille riville toimituksen lupaamisen laskentaan.</span><span class="sxs-lookup"><span data-stu-id="1015a-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="1015a-110">Lisätietoja on kohdassa [Toimintaohje: Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="1015a-110">For more information, see [How to: Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="1015a-111">Kuljetusliikkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1015a-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="1015a-112">Valitse ![Etsiä sivu tai raportti](media/ui-search/search_small.png "Etsiä sivu tai raportti -kuvake") -kuvake, kirjoita **Kuljetusliikkeet** ja valitse sitten aiheeseen liittyvät linkki.</span><span class="sxs-lookup"><span data-stu-id="1015a-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1015a-113">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="1015a-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="1015a-114">.</span><span class="sxs-lookup"><span data-stu-id="1015a-114">.</span></span>  
3.  <span data-ttu-id="1015a-115">Valitse **Kuljetusliikkeen palvelut** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1015a-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="1015a-116">Täytä tarvittavat **Kuljetusliikkeen palvelut** -kentät.</span><span class="sxs-lookup"><span data-stu-id="1015a-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="1015a-117">Jos poistat kuljetusliikkeen tilausriviltä, ohjelma poistaa riviltä myös kuljetusliikkeen palvelukoodin.</span><span class="sxs-lookup"><span data-stu-id="1015a-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="1015a-118">Ohjelma laskee sen jälkeen uudelleen kenttien tiedot, jotka perustuivat osittain kuljetusliikkeiden palveluihin.</span><span class="sxs-lookup"><span data-stu-id="1015a-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1015a-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1015a-119">See Also</span></span>
<span data-ttu-id="1015a-120">[Kollien seuraaminen](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="1015a-120">[How to: Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="1015a-121">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="1015a-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="1015a-122">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="1015a-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="1015a-123">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="1015a-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="1015a-124">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="1015a-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="1015a-125">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="1015a-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="1015a-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1015a-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

