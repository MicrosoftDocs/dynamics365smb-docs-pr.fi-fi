---
title: Ostojen päivämäärälaskenta | Microsoft Docs
description: Sovellus laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon. Tämä on päivämäärä, jona voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 22153df1e56d274256b53d426e2dff30cad3e4bc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758590"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="9bc8a-104">Ostojen päivämäärälaskenta</span><span class="sxs-lookup"><span data-stu-id="9bc8a-104">Date Calculation for Purchases</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="9bc8a-105">laskee automaattisesti päivämäärän, jona nimike on tilattava sen saamiseksi tietyn päivän varastoon.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="9bc8a-106">Tämä on päivämäärä, jona voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="9bc8a-107">Jos määrität ostotilauksen otsikolle pyydetyn vastaanottopäivämäärän, laskettu tilauspäivämäärä on päivämäärä, jona tilaus on asetettava vastaanottamaan nimikkeet pyytämänäsi päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="9bc8a-108">Sitten lasketaan päivämäärä, jolloin nimikkeet ovat poimittavissa, ja syötetään se **Oletettu vastaanottopvm** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="9bc8a-109">Jos et määritä pyydettyä vastaanottopäivämäärää, ohjelma käyttää rivillä olevaa tilauspäivämäärää lähtökohtana laskiessaan päivämäärän, jona voit olettaa vastaanottavasi nimikkeet, ja päivämäärän, jona nimikkeet ovat poimittavissa.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="9bc8a-110">Laskeminen pyydetyn vastaanottopäivämäärän avulla</span><span class="sxs-lookup"><span data-stu-id="9bc8a-110">Calculating with a requested receipt date</span></span>

<span data-ttu-id="9bc8a-111">Jos ostotilausrivillä on pyydetty vastaanottopäivämäärä, ohjelma käyttää tätä päivämäärää lähtökohtana seuraaville laskennoille:</span><span class="sxs-lookup"><span data-stu-id="9bc8a-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="9bc8a-112">Pyydetty vast.ottopvm - Toimitusajan laskenta = Tilauspvm</span><span class="sxs-lookup"><span data-stu-id="9bc8a-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="9bc8a-113">Pyydetty vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm</span><span class="sxs-lookup"><span data-stu-id="9bc8a-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="9bc8a-114">Jos syötit ostotilauksen otsikkoon pyydetyn vastaanottopäivämäärän, ohjelma kopioi tämän päivämäärän kaikkien tilausrivien vastaavaan kenttään.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="9bc8a-115">Päivämäärää voi muuttaa tarpeen mukaan millä tahansa rivillä, tai rivillä olevan päivämäärän voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!NOTE]
> <span data-ttu-id="9bc8a-116">Jos prosessi perustuu taaksepäin laskentaan ja esimerkiksi tilauspäivä saadaan käyttämällä pyydettyä vastaanottopäivää, on suositeltavaa käyttää päivämääräkaavoja, joiden kesto on kiinteä. Sellainen on esimerkiksi 5P viidelle päivälle tai 1V yhdelle viikolle.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="9bc8a-117">Päivämääräkaava, jonka kesto ei ole kiinteä, kuten KV kuluvalle viikolle tai KK kuluvalle kuukaudelle, voi aiheuttaa virheellisiä päivämäärälaskelmia.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="9bc8a-118">Lisätietoja päivämääräkaavoista on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="9bc8a-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="9bc8a-119">Laskeminen ilman pyydettyä toimituspäivämäärää</span><span class="sxs-lookup"><span data-stu-id="9bc8a-119">Calculating without a requested delivery date</span></span>

<span data-ttu-id="9bc8a-120">Jos lisäät ostotilausrivin ilman pyydettyä toimituspäivämäärää, ohjelma lisää rivin **Tilauspvm**-kenttään ostotilauksen tunnistetietojen **Tilauspvm**-kentän päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="9bc8a-121">Tällöin tilauspäivämäärä on joko lisäämäsi päivämäärä tai käsittelypäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="9bc8a-122">Ohjelma laskee sen jälkeen seuraavat päivämäärät ostotilausriville käyttäen tilauspäivämäärää lähtökohtana:</span><span class="sxs-lookup"><span data-stu-id="9bc8a-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="9bc8a-123">tilauspvm + toimitusajan laskenta = suunniteltu vast.ottopvm.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="9bc8a-124">Suunniteltu vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm</span><span class="sxs-lookup"><span data-stu-id="9bc8a-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="9bc8a-125">Jos muutat rivillä olevaa tilauspäivämäärää (esimerkiksi siitä syystä, että nimikkeet eivät ole saatavilla toimittajallasi ennen kuin myöhempänä ajankohtana), ohjelma laskee automaattisesti uudelleen riville asianmukaiset päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="9bc8a-126">Jos muutat tilauspäivämäärää tunnistetiedoissa, ohjelma kopioi tämän päivämäärän kaikkien rivien **Tilauspvm**-kenttiin, ja tämän jälkeen se laskee kaikki asiaan liittyvät päivämääräkentät uudelleen.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="default-values-for-lead-time-calculation"></a><span data-ttu-id="9bc8a-127">Toimitusajan laskennan oletusarvot</span><span class="sxs-lookup"><span data-stu-id="9bc8a-127">Default values for lead time calculation</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="9bc8a-128">laskee tilauksen ja oletetut vastaanottopäivämäärät käyttäen ostotilausrivin **Toimitusajan laskenta** -kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-128">uses the value from the **Lead Time Calculation** field on the purchase order line to calculate the order and the expected receipt dates.</span></span>  

<span data-ttu-id="9bc8a-129">Voit määrittää manuaalisesti rivin arvon tai antaa ohjelman käyttää arvoja, jotka on määritetty toimittajan kortissa, nimikkeen kortissa, varastointiyksiköiden kortissa tai nimikkeen toimittajakatalogissa.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-129">You can manually specify the value on the line or let the program use values that are defined on the vendor card, item card, stockkeeping unit card, or the item vendor catalog.</span></span>
<span data-ttu-id="9bc8a-130">Toimittajan kortin toimitusajan arvoa käytetään kuitenkin vain, jos toimitusajan nimikettä ei ole määritetty nimikkeen kortissa, varastointiyksiköiden kortissa tai nimikkeen toimittajakatalogissa.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-130">However, the lead time value on the vendor card is used only if a lead time is not specified on the item card, stockkeeping unit card, or the item vendor catalog for the item.</span></span> <span data-ttu-id="9bc8a-131">Tämä on myös näiden arvojen priorisointijärjestys.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-131">This is also the escalating order of priority for these values.</span></span> <span data-ttu-id="9bc8a-132">Jos ne ovat kaikki käytettävissä, toimittajan kortin toimitusajalla on alhaisin prioriteetti, ja nimikkeen toimittajakatalogin toimitusajalla on korkein prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="9bc8a-132">If they are all provided, the lead time from the vendor card has the lowest priority, and the lead time from the item vendor catalog has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bc8a-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9bc8a-133">See Also</span></span>

<span data-ttu-id="9bc8a-134">[Myynnin päivämäärälaskenta](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="9bc8a-134">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
[<span data-ttu-id="9bc8a-135">Toimituksen lupaamisen päivämäärien laskeminen</span><span class="sxs-lookup"><span data-stu-id="9bc8a-135">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
<span data-ttu-id="9bc8a-136">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9bc8a-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
