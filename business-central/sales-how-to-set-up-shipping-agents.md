---
title: Kuljetusliikkeiden määrittäminen | Microsoft Docs
description: Voit määrittää koodin jokaiselle kuljetusliikkeelle, ja syöttää tietoja niistä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2ea5d9fce1c10cf3c07c833efbe19b208f0c5a7c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788873"
---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="0c61b-103">Kuljetusliikkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0c61b-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="0c61b-104">Voit määrittää koodin jokaiselle kuljetusliikkeelle, ja syöttää tietoja niistä.</span><span class="sxs-lookup"><span data-stu-id="0c61b-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="0c61b-105">Jos syötät Internet-osoitteen kuljetusliikkeen kohdalle, ja jos kuljetusliike tarjoaa kollinseurantapalveluja Internetissä, voit käyttää ohjelman automaattista kollin seuranta -ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="0c61b-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="0c61b-106">Lisätietoja on kohdassa [Kollien seuraaminen](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="0c61b-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="0c61b-107">Kun määrität kuljetusliikkeitä myyntitilauksillesi, voit määrittää myös kunkin kuljetusliikkeen tarjoamat palvelut.</span><span class="sxs-lookup"><span data-stu-id="0c61b-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="0c61b-108">Voit määrittää rajoittamattoman määrän palveluita jokaiselle kuljetusliikkeelle ja voit määrittää toimitusajan jokaiselle palvelulle.</span><span class="sxs-lookup"><span data-stu-id="0c61b-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="0c61b-109">Kun olet määrittänyt kuljetusliikkeen palvelun myyntitilausriville, palvelun toimitusaika sisällytetään sille riville toimituksen lupaamisen laskentaan.</span><span class="sxs-lookup"><span data-stu-id="0c61b-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="0c61b-110">Lisätietoja on kohdassa [Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="0c61b-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="0c61b-111">Kuljetusliikkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0c61b-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="0c61b-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kuljetusliikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0c61b-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0c61b-113">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="0c61b-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="0c61b-114">.</span><span class="sxs-lookup"><span data-stu-id="0c61b-114">.</span></span>  
3.  <span data-ttu-id="0c61b-115">Valitse **Kuljetusliikkeen palvelut** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="0c61b-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="0c61b-116">Täytä tarvittavat **Kuljetusliikkeen palvelut** -kentät.</span><span class="sxs-lookup"><span data-stu-id="0c61b-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="0c61b-117">Jos poistat kuljetusliikkeen tilausriviltä, ohjelma poistaa riviltä myös kuljetusliikkeen palvelukoodin.</span><span class="sxs-lookup"><span data-stu-id="0c61b-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="0c61b-118">Ohjelma laskee sen jälkeen uudelleen kenttien tiedot, jotka perustuivat osittain kuljetusliikkeiden palveluihin.</span><span class="sxs-lookup"><span data-stu-id="0c61b-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c61b-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0c61b-119">See Also</span></span>
[<span data-ttu-id="0c61b-120">Toimitusehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0c61b-120">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)  
<span data-ttu-id="0c61b-121">[Kollien seuraaminen](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="0c61b-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="0c61b-122">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="0c61b-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0c61b-123">Varasto</span><span class="sxs-lookup"><span data-stu-id="0c61b-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0c61b-124">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="0c61b-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="0c61b-125">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="0c61b-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="0c61b-126">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="0c61b-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0c61b-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c61b-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
