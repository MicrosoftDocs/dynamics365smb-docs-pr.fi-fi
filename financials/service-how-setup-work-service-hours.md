---
title: "Työ- ja huoltotuntien määrittäminen | Microsoft Docs"
description: "Voit määrittää yrityksesi normaalit huoltotunnit. Huoltotuntien avulla lasketaan huoltotilausten ja -tarjousten vastauspäivämäärä ja -aika osalta ja vastausaikavaroitusten lähettäminen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 630875f80f4107522962c79734284569cbc2b6f7
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-work-hours-and-service-hours"></a><span data-ttu-id="947a4-104">Työ- ja huoltotuntien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="947a4-104">Set Up Work Hours and Service Hours</span></span>
<span data-ttu-id="947a4-105">Tavallisesti huoltohallintojärjestelmässä seurataan resurssin tunteja ja huoltotilauksen tilaa kuormituksen ja huollon tarpeiden ennustamista varten.</span><span class="sxs-lookup"><span data-stu-id="947a4-105">Typically, a service management system tracks resource hours and service order status in order to forecast workloads and service needs.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="947a4-106">in sisäiset työkalut voi mukauttaa tallentamaan tällaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="947a4-106"> has built-in tools that you can customize to record this kind of information.</span></span>  
  
<span data-ttu-id="947a4-107">Kun olet määrittänyt yrityksen oletushuoltotunnit, voit laskea huoltotilausten vastausajat tai lähettää varoituksia hälytyksiä huoltokutsun saapuessa.</span><span class="sxs-lookup"><span data-stu-id="947a4-107">After you set the default service hours of your company, you can calculate response times for service orders or send warnings or alerts when service calls come in.</span></span> <span data-ttu-id="947a4-108">Hälytystoiminto otetaan käyttöön yhdessä työn aikataulutuksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="947a4-108">The alert feature is implemented together with the job scheduler.</span></span>   
  
<span data-ttu-id="947a4-109">Huoltotilausta käsiteltäessä tilan päivittäminen antaa mahdollisuuden seurata edistymistä.</span><span class="sxs-lookup"><span data-stu-id="947a4-109">As you work on a service order, you will want to update it's status so that you can monitor progress.</span></span> <span data-ttu-id="947a4-110">Huoltotilauksen tila kuvastaa kaikkien huoltotilauksessa olevien huoltonimikkeiden korjauksen tilaa.</span><span class="sxs-lookup"><span data-stu-id="947a4-110">The service order status reflects the repair status of all the service items in the service order.</span></span> <span data-ttu-id="947a4-111">Lisätietoja on kohdassa [Tietoja huoltotilauksesta ja korjauksen tilasta](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="947a4-111">For more information, see [Understanding Service Order and Repair Status](service-order-repair-status.md).</span></span> 

## <a name="to-set-up-default-service-hours"></a><span data-ttu-id="947a4-112">Oletushuoltotuntien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="947a4-112">To set up default service hours</span></span>  
<span data-ttu-id="947a4-113">**Oletus huoltotunnit** -ikkunaa käytetään määrittämään yrityksesi tavallisia huoltotunteja.</span><span class="sxs-lookup"><span data-stu-id="947a4-113">You use the **Default Service Hours** window to set up the usual service working hours in your company.</span></span> <span data-ttu-id="947a4-114">Ohjelma käyttää huoltotunteja silloin, kun se laskee vastauspäivämäärää ja -aikaa huoltotilausten ja -tarjousten osalta ja kun se lähettää vastausajan varoituksia.</span><span class="sxs-lookup"><span data-stu-id="947a4-114">These service hours are used to calculate the response date and time for service orders and quotes and to send response time warnings.</span></span> <span data-ttu-id="947a4-115">Ohjelma käyttää huoltosopimuksissa oletushuoltotunteja, ellei sopimukselle määritetä erityishuoltotunteja.</span><span class="sxs-lookup"><span data-stu-id="947a4-115">The default service hours are used for service contracts unless you specify special service hours for a contract.</span></span>  
  
1. <span data-ttu-id="947a4-116">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Oletushuoltotunnit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="947a4-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Default Service Hours**, and then choose the related link.</span></span>  
2. <span data-ttu-id="947a4-117">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="947a4-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  <span data-ttu-id="947a4-118">Jos **Oletus huoltotunnit** -ikkunan rivit jätetään tyhjiksi, ohjelma käyttää oletuksena 24 tuntia kaikkina kalenterityöpäivinä.</span><span class="sxs-lookup"><span data-stu-id="947a4-118">If you leave the lines in the **Default Service Hours** window empty, the default value is 24 hours, valid only for calendar working days.</span></span>  
  
## <a name="to-set-up-work-hour-templates"></a><span data-ttu-id="947a4-119">Työtuntimallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="947a4-119">To set up work-hour templates</span></span>
<span data-ttu-id="947a4-120">**Työtuntimalli** -ikkunaa käytetään määrittämään malleja, jotka sisältävät yrityksen tavalliset työtunnit.</span><span class="sxs-lookup"><span data-stu-id="947a4-120">You can use the **Work-Hour Template** window to set up templates that contain the typical working hours in your company.</span></span> <span data-ttu-id="947a4-121">Malleja voi luoda esimerkiksi kokoaikaisille teknikoille ja osa-aikaisille teknikoille.</span><span class="sxs-lookup"><span data-stu-id="947a4-121">For example, you can create templates for full time technicians and part time technicians.</span></span> <span data-ttu-id="947a4-122">Työtunnin malleja voi käyttää silloin, kun lisäät kapasiteettia resursseille.</span><span class="sxs-lookup"><span data-stu-id="947a4-122">You can use work-hour templates when you add capacity to resources.</span></span>  
  
1. <span data-ttu-id="947a4-123">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työntuntimallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="947a4-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Hour Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="947a4-124">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="947a4-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> <span data-ttu-id="947a4-125">Kun kunkin päivän työtunnit on annettu, **Yhteensä per viikko** -kentän arvo lasketaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="947a4-125">After you enter work hours for each day, the value in the **Total per Week** field is calculated automatically.</span></span>  

## <a name="to-set-up-contract-specific-service-hours"></a><span data-ttu-id="947a4-126">Sopimuskohtaisten huoltotuntien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="947a4-126">To set up contract specific service hours</span></span>  
<span data-ttu-id="947a4-127">**Huoltotunnit**-ikkunaa voidaan käyttää erityisten huoltotuntien määrittämiseen huoltosopimuksen omistavalle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="947a4-127">You can use the **Service Hours** window to set up specific service hours for the customer that owns the service contract.</span></span> <span data-ttu-id="947a4-128">Ohjelma käyttää huoltotunteja silloin, kun se laskee vastauspäivämäärää ja -aikaa huoltotilauksiin ja tarjouksiin, jotka kuuluvat kyseiseen huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="947a4-128">Service hours are used to calculate the response date and time for service orders and quotes that belong to the service contract.</span></span>  
  
<span data-ttu-id="947a4-129">Jos huoltosopimukselle ei määritetä erityisiä huoltotunteja, ohjelma käyttää huoltosopimusten oletusarvoisia huoltotunteja.</span><span class="sxs-lookup"><span data-stu-id="947a4-129">If you do not set up specific service hours for the service contract, the default service hours for service contracts are used.</span></span>  
  
1. <span data-ttu-id="947a4-130">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltosopimukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="947a4-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contracts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="947a4-131">Avaa huoltosopimus, jolle haluat määrittää huoltotunnit, ja valitse **Huoltotunnit**.</span><span class="sxs-lookup"><span data-stu-id="947a4-131">Open the service contract you want to set up specific service hours for, and choose **Service Hours**.</span></span>  
4. <span data-ttu-id="947a4-132">Voit määrittää oletushuoltotunteihin perustuvat huoltotunnit valitsemalla **Kopioi oletushuoltotunnit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="947a4-132">To set up service hours based on default service hours, choose the **Copy Default Service Hours** action.</span></span>  
5. <span data-ttu-id="947a4-133">Muokkaa huoltotuntitapahtumien kenttiä.</span><span class="sxs-lookup"><span data-stu-id="947a4-133">Edit the fields in the service hours entries.</span></span> <span data-ttu-id="947a4-134">Lisää tai poista tapahtumat sopimuksen huoltotuntien määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="947a4-134">Insert or delete entries to set up the service hours for the contract.</span></span> <span data-ttu-id="947a4-135">Huomaa, että kentät **Päivä**, **Aloitusaika** ja **Lopetusaika** tarvitaan jokaiselle riville.</span><span class="sxs-lookup"><span data-stu-id="947a4-135">Note that the fields **Day**, **Starting Time** and **Ending Time** are required for each line.</span></span>  
6. <span data-ttu-id="947a4-136">Jos haluat huoltotuntien olevan voimassa tietystä päivästä alkaen, anna päivä **Aloituspvm**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="947a4-136">If you want the service hours to be valid from a specific date, fill in the **Starting Date** field.</span></span>  
7. <span data-ttu-id="947a4-137">Jos haluat huoltotuntien olevan voimassa loma-aikoina, valitse **Voimassa loma-aikoina** -kentän valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="947a4-137">If you want the service hours to be valid on holidays, select the check box in the **Valid on Holidays** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="947a4-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="947a4-138">See Also</span></span>  
[<span data-ttu-id="947a4-139">Tietoja kohdistuksen tilasta ja korjauksen tilasta</span><span class="sxs-lookup"><span data-stu-id="947a4-139">Understanding Allocation Status and Repair Status</span></span>](service-allocation-status-and-repair-status.md)  
[<span data-ttu-id="947a4-140">Huoltohallinnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="947a4-140">Setting Up Service Management</span></span>](service-setup-service.md)  
[<span data-ttu-id="947a4-141">Tietoja huoltotilauksen ja korjauksen tilasta</span><span class="sxs-lookup"><span data-stu-id="947a4-141">Understanding Service Order and Repair Status</span></span>](service-order-repair-status.md)  

