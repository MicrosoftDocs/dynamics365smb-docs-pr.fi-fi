---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788531"
---
<span data-ttu-id="ca71f-101">Kun syötät päivämääriä ja aikoja, joissa päivämäärä ja aika on yhdistetty yhdeksi kentäksi, päivämäärän ja ajan välissä on oltava välilyönti.</span><span class="sxs-lookup"><span data-stu-id="ca71f-101">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="ca71f-102">Päivämääräosa voi sisältää välilyöntejä vain alueasetusten virallisen päivämääräerottimen muodossa.</span><span class="sxs-lookup"><span data-stu-id="ca71f-102">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="ca71f-103">Ajan välilyönnit voivat olla AM/PM-osoittimen ympärillä soveltuvissa alueasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="ca71f-103">The time can contain spaces around the AM/PM indicator in relevant regional settings.</span></span>

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

<span data-ttu-id="ca71f-104">Seuraavassa taulukossa on luettelo eri tavoista, joilla päivämääriä ja aikoja voi syöttää ja miten niitä tulkitaan:</span><span class="sxs-lookup"><span data-stu-id="ca71f-104">The following table lists the various ways in which you can enter datetimes and how they're interpreted.</span></span>  

|<span data-ttu-id="ca71f-105">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="ca71f-105">Entry</span></span>|<span data-ttu-id="ca71f-106">Tulkinta</span><span class="sxs-lookup"><span data-stu-id="ca71f-106">Interpretation</span></span>|
|---------------|------------------------|
|<span data-ttu-id="ca71f-107">08-01-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="ca71f-107">08-01-2022 05:48:12 PM</span></span>|<span data-ttu-id="ca71f-108">08\-01\-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="ca71f-108">08\-01\-2022 05:48:12 PM</span></span>|
|<span data-ttu-id="ca71f-109">131222 132455</span><span class="sxs-lookup"><span data-stu-id="ca71f-109">131222 132455</span></span>|<span data-ttu-id="ca71f-110">13-12-22 13:24:55</span><span class="sxs-lookup"><span data-stu-id="ca71f-110">13-12-22 13:24:55</span></span>|
|<span data-ttu-id="ca71f-111">1-12-22 10</span><span class="sxs-lookup"><span data-stu-id="ca71f-111">1-12-22 10</span></span>|<span data-ttu-id="ca71f-112">01-12-22 10:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-112">01-12-22 10:00:00</span></span>|
|<span data-ttu-id="ca71f-113">1.12.22 5</span><span class="sxs-lookup"><span data-stu-id="ca71f-113">1.12.22 5</span></span>|<span data-ttu-id="ca71f-114">01-12-22 05:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-114">01-12-22 05:00:00</span></span>|
|<span data-ttu-id="ca71f-115">1.12.22</span><span class="sxs-lookup"><span data-stu-id="ca71f-115">1.12.22</span></span>|<span data-ttu-id="ca71f-116">01-12-22 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-116">01-12-22 00:00:00</span></span>|
|<span data-ttu-id="ca71f-117">11 12</span><span class="sxs-lookup"><span data-stu-id="ca71f-117">11 12</span></span>|<span data-ttu-id="ca71f-118">11.nykyinen kuukausi.nykyinen vuosi 12:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-118">11-current month-current year 12:00:00</span></span>|
|<span data-ttu-id="ca71f-119">1112 12</span><span class="sxs-lookup"><span data-stu-id="ca71f-119">1112 12</span></span>|<span data-ttu-id="ca71f-120">11.12.nykyinen vuosi 12:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-120">11-12-current year 12:00:00</span></span>|
|<span data-ttu-id="ca71f-121">t tai tänään</span><span class="sxs-lookup"><span data-stu-id="ca71f-121">t or today</span></span>|<span data-ttu-id="ca71f-122">tämän päivän päivämäärä 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-122">today's date 00:00:00</span></span>|
|<span data-ttu-id="ca71f-123">a aika</span><span class="sxs-lookup"><span data-stu-id="ca71f-123">t time</span></span>|<span data-ttu-id="ca71f-124">tämän päivän pvm tämänhetkinen aika</span><span class="sxs-lookup"><span data-stu-id="ca71f-124">today's date actual time</span></span>|
|<span data-ttu-id="ca71f-125">t 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-125">t 10:30</span></span>|<span data-ttu-id="ca71f-126">tämän päivän päivämäärä 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-126">today's date 10:30:00</span></span>|
|<span data-ttu-id="ca71f-127">t 3:3:3</span><span class="sxs-lookup"><span data-stu-id="ca71f-127">t 3:3:3</span></span>|<span data-ttu-id="ca71f-128">tämän päivän päivämäärä 03:03:03</span><span class="sxs-lookup"><span data-stu-id="ca71f-128">today's date 03:03:03</span></span>|
|<span data-ttu-id="ca71f-129">k tai käsittelypvm</span><span class="sxs-lookup"><span data-stu-id="ca71f-129">w or workdate</span></span>|<span data-ttu-id="ca71f-130">käsittelypvm 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-130">the working date 00:00:00</span></span>|
|<span data-ttu-id="ca71f-131">ma tai maanantai</span><span class="sxs-lookup"><span data-stu-id="ca71f-131">m or Monday</span></span>|<span data-ttu-id="ca71f-132">nykyisen viikon maanantai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-132">Monday of the current week 00:00:00</span></span>|
|<span data-ttu-id="ca71f-133">ti tai tiistai</span><span class="sxs-lookup"><span data-stu-id="ca71f-133">tu or Tuesday</span></span>|<span data-ttu-id="ca71f-134">nykyisen viikon tiistai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-134">Tuesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="ca71f-135">ke tai keskiviikko</span><span class="sxs-lookup"><span data-stu-id="ca71f-135">we or Wednesday</span></span>|<span data-ttu-id="ca71f-136">nykyisen viikon keskiviikko 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-136">Wednesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="ca71f-137">to tai torstai</span><span class="sxs-lookup"><span data-stu-id="ca71f-137">th or Thursday</span></span>|<span data-ttu-id="ca71f-138">nykyisen viikon torstai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-138">Thursday of the current week 00:00:00</span></span>|
|<span data-ttu-id="ca71f-139">pe tai perjantai</span><span class="sxs-lookup"><span data-stu-id="ca71f-139">f or Friday</span></span>|<span data-ttu-id="ca71f-140">nykyisen viikon perjantai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-140">Friday of the current week 00:00:00</span></span>|
|<span data-ttu-id="ca71f-141">la tai lauantai</span><span class="sxs-lookup"><span data-stu-id="ca71f-141">s or Saturday</span></span>|<span data-ttu-id="ca71f-142">nykyisen viikon lauantai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-142">Saturday of the current week 00:00:00</span></span>|
|<span data-ttu-id="ca71f-143">su tai sunnuntai</span><span class="sxs-lookup"><span data-stu-id="ca71f-143">su or Sunday</span></span>|<span data-ttu-id="ca71f-144">nykyisen viikon sunnuntai 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-144">Sunday of the current week 00:00:00</span></span>|
|<span data-ttu-id="ca71f-145">ti 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-145">tu 10:30</span></span>|<span data-ttu-id="ca71f-146">nykyisen viikon tiistai 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-146">Tuesday of the current week 10:30:00</span></span>|
|<span data-ttu-id="ca71f-147">ti 3:3:3</span><span class="sxs-lookup"><span data-stu-id="ca71f-147">tu 3:3:3</span></span>|<span data-ttu-id="ca71f-148">nykyisen viikon tiistai 03:03:03</span><span class="sxs-lookup"><span data-stu-id="ca71f-148">Tuesday of the current week 03:03:03</span></span>|
|<span data-ttu-id="ca71f-149">t23 t</span><span class="sxs-lookup"><span data-stu-id="ca71f-149">t23 t</span></span>|<span data-ttu-id="ca71f-150">Käsittelypvm:n vuoden viikon 23 tiistai, nykyinen aika</span><span class="sxs-lookup"><span data-stu-id="ca71f-150">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="ca71f-151">t23</span><span class="sxs-lookup"><span data-stu-id="ca71f-151">t23</span></span>|<span data-ttu-id="ca71f-152">Käsittelypvm:n vuoden viikon 23 tiistai</span><span class="sxs-lookup"><span data-stu-id="ca71f-152">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="ca71f-153">t 23</span><span class="sxs-lookup"><span data-stu-id="ca71f-153">t 23</span></span>|<span data-ttu-id="ca71f-154">Tänään 23:00:00</span><span class="sxs-lookup"><span data-stu-id="ca71f-154">Today 23:00:00</span></span>|
|<span data-ttu-id="ca71f-155">t-1</span><span class="sxs-lookup"><span data-stu-id="ca71f-155">t-1</span></span>|<span data-ttu-id="ca71f-156">Käsittelypvm:n vuoden viikon 1 tiistai</span><span class="sxs-lookup"><span data-stu-id="ca71f-156">Tuesday of week 1 of the work date year</span></span>|


