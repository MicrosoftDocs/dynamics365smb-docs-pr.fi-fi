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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 80071e9fd584ad3232b8ae55169948f9a05d22be
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-service-items-and-service-item-components"></a><span data-ttu-id="4afeb-103">Toimintaohje: Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4afeb-103">How to: Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="4afeb-104">Huoltonimikkeiden käyttöä varten on määritettävä seuraavat asetukset</span><span class="sxs-lookup"><span data-stu-id="4afeb-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="4afeb-105">Huoltonimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="4afeb-105">Service item groups.</span></span> 
* <span data-ttu-id="4afeb-106">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="4afeb-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="4afeb-107">Huoltonimikeryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4afeb-107">To set up service item groups</span></span>
<span data-ttu-id="4afeb-108">Voit määrittää korjaus- ja ylläpitoehtoihin liittyvät nimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="4afeb-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="4afeb-109">Huoltonimikeryhmässä oleville huoltonimikkeille voi määritellä oletusarvoja, kuten vastausajan, sopimusalennus-%:n ja huoltohintaryhmän.</span><span class="sxs-lookup"><span data-stu-id="4afeb-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="4afeb-110">Huoltonimikeryhmässä olevien nimikkeiden osalta voi valita, halutaanko, että ne rekisteröidään automaattisesti huoltonimikkeiksi silloin, kun ne myydään.</span><span class="sxs-lookup"><span data-stu-id="4afeb-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  
  
<span data-ttu-id="4afeb-111">Huoltonimikeryhmiä määritetään **Nimike**-kortin nimikkeille ja **Huoltonimike**-kortin huoltonimikkeille.</span><span class="sxs-lookup"><span data-stu-id="4afeb-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  
  
1. <span data-ttu-id="4afeb-112">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltonimikeryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4afeb-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4afeb-113">Luo uusi huoltonimikeryhmä.</span><span class="sxs-lookup"><span data-stu-id="4afeb-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="4afeb-114">Täytä **Koodi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="4afeb-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="4afeb-115">Anna **Oletus sopimusalennus-%** -kenttään oletussopimusalennusprosentti, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="4afeb-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="4afeb-116">Anna **Oletus huoltohintaryhmän koodi** -kenttään oletushuoltohintaryhmän koodi, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="4afeb-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="4afeb-117">Anna **Oletusvastausaika (tuntia)** -kenttään oletusvastausaika tunneissa, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="4afeb-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="4afeb-118">Jos haluat rekisteröidä ryhmän nimikkeen huoltonimikkeiksi silloin, kun ne myydään, valitse **Luo huoltonimike** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="4afeb-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="4afeb-119">Huoltonimikkeen komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4afeb-119">To set up service item components</span></span>
<span data-ttu-id="4afeb-120">Huoltonimike voi koostua useista komponenteista, jotka voidaan korvata varaosilla nimikettä huollettaessa.</span><span class="sxs-lookup"><span data-stu-id="4afeb-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="4afeb-121">Nämä komponentit määritetään **Huoltonimikk. komponenttiluet.** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4afeb-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="4afeb-122">Jos lisäksi haluat määrittää komponentteja huoltonimikkeille, jotka ovat tuoterakenteita, tuoterakennenimikkeet voidaan kopioida ja luoda huoltonimikkeen komponentteina.</span><span class="sxs-lookup"><span data-stu-id="4afeb-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span> 
  
1. <span data-ttu-id="4afeb-123">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltonimikkeet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4afeb-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span> 
2. <span data-ttu-id="4afeb-124">Avaa huoltonimike, jolle haluat määrittää komponentteja.</span><span class="sxs-lookup"><span data-stu-id="4afeb-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="4afeb-125">Valitse **Komponentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4afeb-125">Choose the **Components** action.</span></span> <span data-ttu-id="4afeb-126">Näyttöön tulee **Huoltonimikk. komponenttiluet.** -ikkuna.</span><span class="sxs-lookup"><span data-stu-id="4afeb-126">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="4afeb-127">Uuden ryhmän lisääminen</span><span class="sxs-lookup"><span data-stu-id="4afeb-127">Add a new component.</span></span>  
5. <span data-ttu-id="4afeb-128">Valitse **Tyyppi** -kentässä **Huoltonimike**, jos itse komponentti on rekisteröity huoltonimike.</span><span class="sxs-lookup"><span data-stu-id="4afeb-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="4afeb-129">Muutoin valitse **Nimike**.</span><span class="sxs-lookup"><span data-stu-id="4afeb-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="4afeb-130">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="4afeb-130">In the **No.**</span></span> <span data-ttu-id="4afeb-131">nimike tai huoltonimike, joka on huoltonimikkeen komponentti.</span><span class="sxs-lookup"><span data-stu-id="4afeb-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="4afeb-132">Huoltonimikkeen komponenttien määrittäminen tuoterakenteista</span><span class="sxs-lookup"><span data-stu-id="4afeb-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="4afeb-133">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltonimikkeet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4afeb-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4afeb-134">Avaa huoltonimike, jolle haluat määrittää komponentteja huoltorakenteesta.</span><span class="sxs-lookup"><span data-stu-id="4afeb-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="4afeb-135">Valitse **Komponentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4afeb-135">Choose the **Components** action.</span></span> <span data-ttu-id="4afeb-136">**Huoltonimikk. komponenttiluet.** -ikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="4afeb-136">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="4afeb-137">Valitse **Kopioi tuoterakenteesta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="4afeb-137">Choose the **Copy from BOM** action.</span></span>  
  
    <span data-ttu-id="4afeb-138">Jos nimike, johon huoltonimike on linkitetty, on tuoterakenne, ohjelma luo automaattisesti komponentteja kaikille tuoterakenteessa oleville nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="4afeb-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="4afeb-139">Huoltohyllyn määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4afeb-139">To set up a service shelf</span></span>
<span data-ttu-id="4afeb-140">Voit määrittää huoltohyllyjä, jotka ilmaisevat, mihin huoltonimikkeet varastoidaan.</span><span class="sxs-lookup"><span data-stu-id="4afeb-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="4afeb-141">Huoltohyllyt määritetään huoltonimikkeille **Huoltotilaus**- ja **Huoltonimikkeen työkirja** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="4afeb-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  
  
1. <span data-ttu-id="4afeb-142">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltohyllyt** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4afeb-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="4afeb-143">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="4afeb-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="4afeb-144">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4afeb-144">See Also</span></span>
<span data-ttu-id="4afeb-145">[Toimintaohje: Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="4afeb-145">[How to: Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="4afeb-146">Toimintaohje: Vianetsinnän määrittäminen:</span><span class="sxs-lookup"><span data-stu-id="4afeb-146">How to: Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)
