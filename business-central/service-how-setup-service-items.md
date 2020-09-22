---
title: Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen | Microsoft Docs
description: Lisätietoja määrityksistä, jotka on tehtävä ennen huoltonimikkeiden käyttöä. Esimerkiksi oletusarvot, kuten vastausaika, sopimusalennusprosentti ja huoltohintaryhmä, on määritettävä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 067c1c95fd84adb10d042714a1fc9116b3503f36
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784532"
---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="2101e-103">Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2101e-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="2101e-104">Huoltonimikkeiden käyttöä varten on määritettävä seuraavat asetukset</span><span class="sxs-lookup"><span data-stu-id="2101e-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="2101e-105">Huoltonimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="2101e-105">Service item groups.</span></span>
* <span data-ttu-id="2101e-106">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="2101e-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="2101e-107">Huoltonimikeryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2101e-107">To set up service item groups</span></span>
<span data-ttu-id="2101e-108">Voit määrittää korjaus- ja ylläpitoehtoihin liittyvät nimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="2101e-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="2101e-109">Huoltonimikeryhmässä oleville huoltonimikkeille voi määritellä oletusarvoja, kuten vastausajan, sopimusalennus-%:n ja huoltohintaryhmän.</span><span class="sxs-lookup"><span data-stu-id="2101e-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="2101e-110">Huoltonimikeryhmässä olevien nimikkeiden osalta voi valita, halutaanko, että ne rekisteröidään automaattisesti huoltonimikkeiksi silloin, kun ne myydään.</span><span class="sxs-lookup"><span data-stu-id="2101e-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="2101e-111">Huoltonimikeryhmiä määritetään **Nimike**-kortin nimikkeille ja **Huoltonimike**-kortin huoltonimikkeille.</span><span class="sxs-lookup"><span data-stu-id="2101e-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="2101e-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltonimikeryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2101e-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2101e-113">Luo uusi huoltonimikeryhmä.</span><span class="sxs-lookup"><span data-stu-id="2101e-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="2101e-114">Täytä **Koodi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="2101e-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="2101e-115">Anna **Oletus sopimusalennus-%** -kenttään oletussopimusalennusprosentti, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="2101e-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="2101e-116">Anna **Oletus huoltohintaryhmän koodi** -kenttään oletushuoltohintaryhmän koodi, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="2101e-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="2101e-117">Anna **Oletusvastausaika (tuntia)** -kenttään oletusvastausaika tunneissa, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.</span><span class="sxs-lookup"><span data-stu-id="2101e-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="2101e-118">Jos haluat rekisteröidä ryhmän nimikkeen huoltonimikkeiksi silloin, kun ne myydään, valitse **Luo huoltonimike** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="2101e-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="2101e-119">Huoltonimikkeen komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2101e-119">To set up service item components</span></span>
<span data-ttu-id="2101e-120">Huoltonimike voi koostua useista komponenteista, jotka voidaan korvata varaosilla nimikettä huollettaessa.</span><span class="sxs-lookup"><span data-stu-id="2101e-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="2101e-121">Nämä komponentit määritetään **Huoltonimikk. komponenttiluet.** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2101e-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="2101e-122">Jos lisäksi haluat määrittää komponentteja huoltonimikkeille, jotka ovat tuoterakenteita, tuoterakennenimikkeet voidaan kopioida ja luoda huoltonimikkeen komponentteina.</span><span class="sxs-lookup"><span data-stu-id="2101e-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="2101e-123">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltonimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2101e-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="2101e-124">Avaa huoltonimike, jolle haluat määrittää komponentteja.</span><span class="sxs-lookup"><span data-stu-id="2101e-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="2101e-125">Valitse **Komponentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2101e-125">Choose the **Components** action.</span></span> <span data-ttu-id="2101e-126">Näyttöön tulee **Huoltonimikk. komponenttiluet.** -sivu.</span><span class="sxs-lookup"><span data-stu-id="2101e-126">The **Service Item Component List** page opens.</span></span>  
4. <span data-ttu-id="2101e-127">Uuden ryhmän lisääminen</span><span class="sxs-lookup"><span data-stu-id="2101e-127">Add a new component.</span></span>  
5. <span data-ttu-id="2101e-128">Valitse **Tyyppi** -kentässä **Huoltonimike**, jos itse komponentti on rekisteröity huoltonimike.</span><span class="sxs-lookup"><span data-stu-id="2101e-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="2101e-129">Muutoin valitse **Nimike**.</span><span class="sxs-lookup"><span data-stu-id="2101e-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="2101e-130">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="2101e-130">In the **No.**</span></span> <span data-ttu-id="2101e-131">nimike tai huoltonimike, joka on huoltonimikkeen komponentti.</span><span class="sxs-lookup"><span data-stu-id="2101e-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="2101e-132">Huoltonimikkeen komponenttien määrittäminen tuoterakenteista</span><span class="sxs-lookup"><span data-stu-id="2101e-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="2101e-133">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltonimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2101e-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2101e-134">Avaa huoltonimike, jolle haluat määrittää komponentteja huoltorakenteesta.</span><span class="sxs-lookup"><span data-stu-id="2101e-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="2101e-135">Valitse **Komponentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2101e-135">Choose the **Components** action.</span></span> <span data-ttu-id="2101e-136">Näyttöön tulee **Huoltonimikk. komponenttiluet.** -sivu.</span><span class="sxs-lookup"><span data-stu-id="2101e-136">The **Service Item Component List** page opens.</span></span>  
4. <span data-ttu-id="2101e-137">Valitse **Kopioi tuoterakenteesta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="2101e-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="2101e-138">Jos nimike, johon huoltonimike on linkitetty, on tuoterakenne, ohjelma luo automaattisesti komponentteja kaikille tuoterakenteessa oleville nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="2101e-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="2101e-139">Huoltohyllyn määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2101e-139">To set up a service shelf</span></span>
<span data-ttu-id="2101e-140">Voit määrittää huoltohyllyjä, jotka ilmaisevat, mihin huoltonimikkeet varastoidaan.</span><span class="sxs-lookup"><span data-stu-id="2101e-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="2101e-141">Huoltohyllyt määritetään huoltonimikkeille **Huoltotilaus**- ja **Huoltonimikkeen työkirja** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="2101e-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  

1. <span data-ttu-id="2101e-142">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltotarjoukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2101e-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="2101e-143">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="2101e-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="2101e-144">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2101e-144">See Also</span></span>
<span data-ttu-id="2101e-145">[Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="2101e-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="2101e-146">Vianmäärityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2101e-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)
