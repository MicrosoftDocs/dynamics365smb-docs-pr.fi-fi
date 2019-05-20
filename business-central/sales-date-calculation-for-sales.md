---
title: Myynnin päivämäärälaskenta | Microsoft Docs
description: Ohjelma laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon. Tämä on päivämäärä, jolloin voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a620b7ed9d06cdd8adf7b12bea2b55aecea32bcc
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251123"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="ee90f-104">Myynnin päivämäärälaskenta</span><span class="sxs-lookup"><span data-stu-id="ee90f-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ee90f-105">laskee automaattisesti varhaisimman mahdollisen päivämäärän, jolloin myyntitilausrivin nimike voidaan toimittaa.</span><span class="sxs-lookup"><span data-stu-id="ee90f-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="ee90f-106">Jos asiakas on pyytänyt tietyn toimituspäivämäärän, ohjelma laskee päivämäärän, jolloin nimikkeiden tulee olla poimittavissa, jotta toimitus onnistuu sinä päivänä.</span><span class="sxs-lookup"><span data-stu-id="ee90f-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="ee90f-107">Jos asiakas ei pyydä tiettyä toimituspäivämäärää, ohjelma laskee päivämäärän, jolloin nimikkeet voidaan toimittaa alkaen siitä päivästä, jolloin nimikkeet ovat poimittavissa.</span><span class="sxs-lookup"><span data-stu-id="ee90f-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="ee90f-108">Laskeminen ilman pyydettyä toimituspäivämäärää</span><span class="sxs-lookup"><span data-stu-id="ee90f-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="ee90f-109">Jos myyntitilausrivillä on pyydetty toimitusottopäivämäärä, ohjelma käyttää tätä päivämäärää lähtökohtana seuraaville laskennoille:</span><span class="sxs-lookup"><span data-stu-id="ee90f-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="ee90f-110">Pyydetty toimituspvm - Toimitusaika = Suunniteltu lähetyspvm</span><span class="sxs-lookup"><span data-stu-id="ee90f-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="ee90f-111">Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika = Toimituspäivä</span><span class="sxs-lookup"><span data-stu-id="ee90f-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="ee90f-112">Jos nimikkeet ovat poimittavissa lähetyspäivämääränä, myyntiprosessi voi jatkua.</span><span class="sxs-lookup"><span data-stu-id="ee90f-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="ee90f-113">Jos nimikkeet eivät ole poimittavissa lähetyspäivämääränä, näyttöön tulee varastoloppu-varoitus.</span><span class="sxs-lookup"><span data-stu-id="ee90f-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="ee90f-114">Varhaisimman mahdollisen toimituspäivämäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="ee90f-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="ee90f-115">Jos myyntitilausrivillä ei ole pyydettyä toimituspäivämäärää, tai jos toimitus ei onnistu pyydettynä toimituspäivämääränä, ohjelma etsii varhaisimman päivämäärän, jolloin nimikkeet ovat saatavilla.</span><span class="sxs-lookup"><span data-stu-id="ee90f-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="ee90f-116">Sen jälkeen ohjelma syöttää tämän päivämäärän rivin Toimituspvm -kenttään ja laskee päivämäärän, jolloin nimikkeet suunnitellaan lähetettävän, ja päivämäärän, jolloin ne toimitetaan asiakkaalle, seuraavien laskukaavojen mukaan:</span><span class="sxs-lookup"><span data-stu-id="ee90f-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="ee90f-117">Suunniteltu toimituspvm = lähtevä f.var. käsittelyaika + toimituspäivä</span><span class="sxs-lookup"><span data-stu-id="ee90f-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="ee90f-118">Suunniteltu toimituspvm + toimitusaika = suunniteltu toimituspvm</span><span class="sxs-lookup"><span data-stu-id="ee90f-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="ee90f-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ee90f-119">See Also</span></span>  
 <span data-ttu-id="ee90f-120">[Ostojen päivämäärälaskenta](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="ee90f-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="ee90f-121">Toimituksen lupaamisen päivämäärien laskeminen</span><span class="sxs-lookup"><span data-stu-id="ee90f-121">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="ee90f-122">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ee90f-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
