---
title: Ostojen päivämäärälaskenta | Microsoft Docs
description: Ohjelma laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon. Tämä on päivämäärä, jona voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi.
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
ms.openlocfilehash: e7dfe565fc533ca5a724675c925cf6a415c49b94
ms.sourcegitcommit: 8c0d734c7202fec81da79c7db382243aa49e37f6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/10/2019
ms.locfileid: "1737095"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="590d2-104">Ostojen päivämäärälaskenta</span><span class="sxs-lookup"><span data-stu-id="590d2-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="590d2-105">laskee automaattisesti päivämäärän, jona nimike on tilattava sen saamiseksi tietyn päivän varastoon.</span><span class="sxs-lookup"><span data-stu-id="590d2-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="590d2-106">Tämä on päivämäärä, jona voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi.</span><span class="sxs-lookup"><span data-stu-id="590d2-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="590d2-107">Jos määrität ostotilauksen otsikolle pyydetyn vastaanottopäivämäärän, laskettu tilauspäivämäärä on päivämäärä, jona tilaus on asetettava vastaanottamaan nimikkeet pyytämänäsi päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="590d2-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="590d2-108">Sitten lasketaan päivämäärä, jolloin nimikkeet ovat poimittavissa, ja syötetään se **Oletettu vastaanottopvm** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="590d2-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="590d2-109">Jos et määritä pyydettyä vastaanottopäivämäärää, ohjelma käyttää rivillä olevaa tilauspäivämäärää lähtökohtana laskiessaan päivämäärän, jona voit olettaa vastaanottavasi nimikkeet, ja päivämäärän, jona nimikkeet ovat poimittavissa.</span><span class="sxs-lookup"><span data-stu-id="590d2-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="590d2-110">Laskeminen pyydetyn vastaanottopäivämäärän avulla</span><span class="sxs-lookup"><span data-stu-id="590d2-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="590d2-111">Jos ostotilausrivillä on pyydetty vastaanottopäivämäärä, ohjelma käyttää tätä päivämäärää lähtökohtana seuraaville laskennoille:</span><span class="sxs-lookup"><span data-stu-id="590d2-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="590d2-112">Pyydetty vast.ottopvm - Toimitusajan laskenta = Tilauspvm</span><span class="sxs-lookup"><span data-stu-id="590d2-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="590d2-113">Pyydetty vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm</span><span class="sxs-lookup"><span data-stu-id="590d2-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="590d2-114">Jos syötit ostotilauksen otsikkoon pyydetyn vastaanottopäivämäärän, ohjelma kopioi tämän päivämäärän kaikkien tilausrivien vastaavaan kenttään.</span><span class="sxs-lookup"><span data-stu-id="590d2-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="590d2-115">Päivämäärää voi muuttaa tarpeen mukaan millä tahansa rivillä, tai rivillä olevan päivämäärän voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="590d2-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!Note]
> <span data-ttu-id="590d2-116">Jos prosessi perustuu taaksepäin laskentaan ja esimerkiksi tilauspäivä saadaan käyttämällä pyydettyä vastaanottopäivää, on suositeltavaa käyttää päivämääräkaavoja, joiden kesto on kiinteä. Sellainen on esimerkiksi 5P viidelle päivälle tai 1V yhdelle viikolle.</span><span class="sxs-lookup"><span data-stu-id="590d2-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="590d2-117">Päivämääräkaava, jonka kesto ei ole kiinteä, kuten KV kuluvalle viikolle tai KK kuluvalle kuukaudelle, voi aiheuttaa virheellisiä päivämäärälaskelmia.</span><span class="sxs-lookup"><span data-stu-id="590d2-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="590d2-118">Lisätietoja päivämääräkaavoista on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="590d2-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="590d2-119">Laskeminen ilman pyydettyä toimituspäivämäärää</span><span class="sxs-lookup"><span data-stu-id="590d2-119">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="590d2-120">Jos lisäät ostotilausrivin ilman pyydettyä toimituspäivämäärää, ohjelma lisää rivin **Tilauspvm**-kenttään ostotilauksen tunnistetietojen **Tilauspvm**-kentän päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="590d2-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="590d2-121">Tällöin tilauspäivämäärä on joko lisäämäsi päivämäärä tai käsittelypäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="590d2-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="590d2-122">Ohjelma laskee sen jälkeen seuraavat päivämäärät ostotilausriville käyttäen tilauspäivämäärää lähtökohtana:</span><span class="sxs-lookup"><span data-stu-id="590d2-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="590d2-123">tilauspvm + toimitusajan laskenta = suunniteltu vast.ottopvm.</span><span class="sxs-lookup"><span data-stu-id="590d2-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="590d2-124">Suunniteltu vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm</span><span class="sxs-lookup"><span data-stu-id="590d2-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="590d2-125">Jos muutat rivillä olevaa tilauspäivämäärää (esimerkiksi siitä syystä, että nimikkeet eivät ole saatavilla toimittajallasi ennen kuin myöhempänä ajankohtana), ohjelma laskee automaattisesti uudelleen riville asianmukaiset päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="590d2-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="590d2-126">Jos muutat tilauspäivämäärää tunnistetiedoissa, ohjelma kopioi tämän päivämäärän kaikkien rivien **Tilauspvm**-kenttiin, ja tämän jälkeen se laskee kaikki asiaan liittyvät päivämääräkentät uudelleen.</span><span class="sxs-lookup"><span data-stu-id="590d2-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="590d2-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="590d2-127">See Also</span></span>  
 <span data-ttu-id="590d2-128">[Myynnin päivämäärälaskenta](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="590d2-128">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="590d2-129">Toimituksen lupaamisen päivämäärien laskeminen</span><span class="sxs-lookup"><span data-stu-id="590d2-129">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="590d2-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="590d2-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
