---
title: Myynnin päivämäärälaskenta | Microsoft Docs
description: Sovellus laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon. Tämä on päivämäärä, jolloin voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0fa1f07b5da450a2e6f634bda07752efd0e35889
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312242"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="e6af1-104">Myynnin päivämäärälaskenta</span><span class="sxs-lookup"><span data-stu-id="e6af1-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e6af1-105">laskee automaattisesti varhaisimman mahdollisen päivämäärän, jolloin myyntitilausrivin nimike voidaan toimittaa.</span><span class="sxs-lookup"><span data-stu-id="e6af1-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="e6af1-106">Jos asiakas on pyytänyt tietyn toimituspäivämäärän, ohjelma laskee päivämäärän, jolloin nimikkeiden tulee olla poimittavissa, jotta toimitus onnistuu sinä päivänä.</span><span class="sxs-lookup"><span data-stu-id="e6af1-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="e6af1-107">Jos asiakas ei pyydä tiettyä toimituspäivämäärää, ohjelma laskee päivämäärän, jolloin nimikkeet voidaan toimittaa alkaen siitä päivästä, jolloin nimikkeet ovat poimittavissa.</span><span class="sxs-lookup"><span data-stu-id="e6af1-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="e6af1-108">Laskeminen ilman pyydettyä toimituspäivämäärää</span><span class="sxs-lookup"><span data-stu-id="e6af1-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="e6af1-109">Jos myyntitilausrivillä on pyydetty toimitusottopäivämäärä, ohjelma käyttää tätä päivämäärää lähtökohtana seuraaville laskennoille:</span><span class="sxs-lookup"><span data-stu-id="e6af1-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="e6af1-110">Pyydetty toimituspvm - Toimitusaika = Suunniteltu lähetyspvm</span><span class="sxs-lookup"><span data-stu-id="e6af1-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="e6af1-111">Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika = Toimituspäivä</span><span class="sxs-lookup"><span data-stu-id="e6af1-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="e6af1-112">Jos nimikkeet ovat poimittavissa lähetyspäivämääränä, myyntiprosessi voi jatkua.</span><span class="sxs-lookup"><span data-stu-id="e6af1-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="e6af1-113">Muussa tapauksessa näytetään varaston loppumisvaroitus.</span><span class="sxs-lookup"><span data-stu-id="e6af1-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="e6af1-114">Jos prosessi perustuu taaksepäin laskentaan ja esimerkiksi toimituspäivä saadaan käyttämällä suunniteltua toimituspäivää, on suositeltavaa käyttää päivämääräkaavoja, joiden kesto on kiinteä. Sellainen on esimerkiksi 5P viidelle päivälle tai 1V yhdelle viikolle.</span><span class="sxs-lookup"><span data-stu-id="e6af1-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="e6af1-115">Päivämääräkaava, jonka kesto ei ole kiinteä, kuten KV kuluvalle viikolle tai KK kuluvalle kuukaudelle, voi aiheuttaa virheellisiä päivämäärälaskelmia.</span><span class="sxs-lookup"><span data-stu-id="e6af1-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="e6af1-116">Lisätietoja päivämääräkaavoista on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="e6af1-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="e6af1-117">Varhaisimman mahdollisen toimituspäivämäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="e6af1-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="e6af1-118">Jos myyntitilausrivillä ei ole pyydettyä toimituspäivämäärää, tai jos toimitus ei onnistu pyydettynä toimituspäivämääränä, ohjelma etsii varhaisimman päivämäärän, jolloin nimikkeet ovat saatavilla.</span><span class="sxs-lookup"><span data-stu-id="e6af1-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="e6af1-119">Sen jälkeen ohjelma syöttää tämän päivämäärän rivin Toimituspvm -kenttään ja laskee päivämäärän, jolloin nimikkeet suunnitellaan lähetettävän, ja päivämäärän, jolloin ne toimitetaan asiakkaalle, seuraavien laskukaavojen mukaan:</span><span class="sxs-lookup"><span data-stu-id="e6af1-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="e6af1-120">Suunniteltu toimituspvm = lähtevä f.var. käsittelyaika + toimituspäivä</span><span class="sxs-lookup"><span data-stu-id="e6af1-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="e6af1-121">Suunniteltu toimituspvm + toimitusaika = suunniteltu toimituspvm</span><span class="sxs-lookup"><span data-stu-id="e6af1-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="e6af1-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e6af1-122">See Also</span></span>  
 <span data-ttu-id="e6af1-123">[Ostojen päivämäärälaskenta](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="e6af1-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="e6af1-124">Toimituksen lupaamisen päivämäärien laskeminen</span><span class="sxs-lookup"><span data-stu-id="e6af1-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="e6af1-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e6af1-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
