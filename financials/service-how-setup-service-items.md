---
title: "Yleiskatsaus huoltonimikkeiden ja huoltonimikkeen komponenttien määrityksistä | Microsoft Docs"
description: "Lisätietoja määrityksistä, jotka on tehtävä ennen huoltonimikkeiden käyttöä. Esimerkiksi oletusarvot, kuten vastausaika, sopimusalennusprosentti ja huoltohintaryhmä, on määritettävä."
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
ms.openlocfilehash: 068d141ee8490cc34e8b2092b7dcfda36139660d
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="37649-103">Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="37649-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="37649-104">Huoltonimikkeiden käyttöä varten on määritettävä seuraavat asetukset</span><span class="sxs-lookup"><span data-stu-id="37649-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="37649-105">Huoltonimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="37649-105">Service item groups.</span></span> 
* <span data-ttu-id="37649-106">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="37649-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="37649-107">Huoltonimikeryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="37649-107">To set up service item groups</span></span>
<span data-ttu-id="37649-108">Voit määrittää korjaus- ja ylläpitoehtoihin liittyvät nimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="37649-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="37649-109">Huoltonimikeryhmässä oleville huoltonimikkeille voi määritellä oletusarvoja, kuten vastausajan, sopimusalennus-%:n ja huoltohintaryhmän.</span><span class="sxs-lookup"><span data-stu-id="37649-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="37649-110">Huoltonimikeryhmässä olevien nimikkeiden osalta voi valita, halutaanko, että ne rekisteröidään automaattisesti huoltonimikkeiksi silloin, kun ne myydään.</span><span class="sxs-lookup"><span data-stu-id="37649-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  
  
<span data-ttu-id="37649-111">Huoltonimikeryhmiä määritetään **Nimike**-kortin nimikkeille ja **Huoltonimike**-kortin huoltonimikkeille.</span><span class="sxs-lookup"><span data-stu-id="37649-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  
  
1. <span data-ttu-id="37649-112">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltonimikeryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="37649-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37649-113">Luo uusi huoltonimikeryhmä.</span><span class="sxs-lookup"><span data-stu-id="37649-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="37649-114">Täytä **Koodi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="37649-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="37649-115">Anna **Oletus sopimusalennus-%** -kenttään oletussopimusalennusprosentti, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="37649-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="37649-116">Anna **Oletus huoltohintaryhmän koodi** -kenttään oletushuoltohintaryhmän koodi, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="37649-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="37649-117">Anna **Oletusvastausaika (tuntia)** -kenttään oletusvastausaika tunneissa, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="37649-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="37649-118">Jos haluat rekisteröidä ryhmän nimikkeen huoltonimikkeiksi silloin, kun ne myydään, valitse **Luo huoltonimike** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="37649-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="37649-119">Huoltonimikkeen komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="37649-119">To set up service item components</span></span>
<span data-ttu-id="37649-120">Huoltonimike voi koostua useista komponenteista, jotka voidaan korvata varaosilla nimikettä huollettaessa.</span><span class="sxs-lookup"><span data-stu-id="37649-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="37649-121">Nämä komponentit määritetään **Huoltonimikk. komponenttiluet.** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="37649-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="37649-122">Jos lisäksi haluat määrittää komponentteja huoltonimikkeille, jotka ovat tuoterakenteita, tuoterakennenimikkeet voidaan kopioida ja luoda huoltonimikkeen komponentteina.</span><span class="sxs-lookup"><span data-stu-id="37649-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span> 
  
1. <span data-ttu-id="37649-123">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltonimikkeet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="37649-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span> 
2. <span data-ttu-id="37649-124">Avaa huoltonimike, jolle haluat määrittää komponentteja.</span><span class="sxs-lookup"><span data-stu-id="37649-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="37649-125">Valitse **Komponentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="37649-125">Choose the **Components** action.</span></span> <span data-ttu-id="37649-126">Näyttöön tulee **Huoltonimikk. komponenttiluet.** -ikkuna.</span><span class="sxs-lookup"><span data-stu-id="37649-126">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="37649-127">Uuden ryhmän lisääminen</span><span class="sxs-lookup"><span data-stu-id="37649-127">Add a new component.</span></span>  
5. <span data-ttu-id="37649-128">Valitse **Tyyppi** -kentässä **Huoltonimike**, jos itse komponentti on rekisteröity huoltonimike.</span><span class="sxs-lookup"><span data-stu-id="37649-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="37649-129">Muutoin valitse **Nimike**.</span><span class="sxs-lookup"><span data-stu-id="37649-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="37649-130">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="37649-130">In the **No.**</span></span> <span data-ttu-id="37649-131">nimike tai huoltonimike, joka on huoltonimikkeen komponentti.</span><span class="sxs-lookup"><span data-stu-id="37649-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="37649-132">Huoltonimikkeen komponenttien määrittäminen tuoterakenteista</span><span class="sxs-lookup"><span data-stu-id="37649-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="37649-133">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltonimikkeet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="37649-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37649-134">Avaa huoltonimike, jolle haluat määrittää komponentteja huoltorakenteesta.</span><span class="sxs-lookup"><span data-stu-id="37649-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="37649-135">Valitse **Komponentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="37649-135">Choose the **Components** action.</span></span> <span data-ttu-id="37649-136">**Huoltonimikk. komponenttiluet.** -ikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="37649-136">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="37649-137">Valitse **Kopioi tuoterakenteesta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="37649-137">Choose the **Copy from BOM** action.</span></span>  
  
    <span data-ttu-id="37649-138">Jos nimike, johon huoltonimike on linkitetty, on tuoterakenne, ohjelma luo automaattisesti komponentteja kaikille tuoterakenteessa oleville nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="37649-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="37649-139">Huoltohyllyn määrittäminen</span><span class="sxs-lookup"><span data-stu-id="37649-139">To set up a service shelf</span></span>
<span data-ttu-id="37649-140">Voit määrittää huoltohyllyjä, jotka ilmaisevat, mihin huoltonimikkeet varastoidaan.</span><span class="sxs-lookup"><span data-stu-id="37649-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="37649-141">Huoltohyllyt määritetään huoltonimikkeille **Huoltotilaus**- ja **Huoltonimikkeen työkirja** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="37649-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  
  
1. <span data-ttu-id="37649-142">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltohyllyt** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="37649-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="37649-143">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="37649-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="37649-144">Katso myös</span><span class="sxs-lookup"><span data-stu-id="37649-144">See Also</span></span>
<span data-ttu-id="37649-145">[Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="37649-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="37649-146">Vianmäärityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="37649-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)
