---
title: Huoltotilausten ja -korjausten tilan määrittäminen | Microsoft Docs
description: Sinun on määritettävä yhdeksän korjauksen tilan vaihtoehtoa, jotka ilmaisevat huoltotilauksissa olevien huoltonimikkeiden korjauksen edistymisen ja ylläpidon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 87eb71de29a32b033bf8a7f372f1adfe70ab38e6
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777539"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="b1370-103">Huoltotilausten ja -korjausten tilan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b1370-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="b1370-104">Sinun on määritettävä korjauksen tilan vaihtoehdot, jotka ilmaisevat huoltotilauksissa olevien huoltonimikkeiden korjauksen edistymisen ja ylläpidon.</span><span class="sxs-lookup"><span data-stu-id="b1370-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="b1370-105">Sinun on määritettävä vähintään yhdeksän korjauksen tilan vaihtoehtoa, jotka ilmaisevat tilanteet tai suoritettavat toimenpiteet huoltonimikkeiden huoltamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="b1370-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="b1370-106">Voit määrittää huoltotilauksen tilavaihtoehtojen prioriteettitasot.</span><span class="sxs-lookup"><span data-stu-id="b1370-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="b1370-107">Prioriteetteja on neljä: Matala, Melko matala, Melko korkea ja Korkea.</span><span class="sxs-lookup"><span data-stu-id="b1370-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  

<span data-ttu-id="b1370-108">Kun huoltotilauksessa olevan huoltonimikkeen korjauksen tilaa muutetaan, ohjelma päivittää huoltotilauksen tilan.</span><span class="sxs-lookup"><span data-stu-id="b1370-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="b1370-109">Kunkin huoltonimikkeen korjauksen tila on linkitetty huoltotilauksen tilaan.</span><span class="sxs-lookup"><span data-stu-id="b1370-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="b1370-110">Jos huoltonimikkeet on linkitetty kahteen tai useampaan huoltotilauksen tilan vaihtoehtoon, ohjelma valitsee huoltotilauksen tilan, jolla on korkein prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="b1370-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="b1370-111">Korjauksen tilan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b1370-111">To set up a repair status</span></span>  
1. <span data-ttu-id="b1370-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Korjauksen tila** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b1370-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="b1370-113">Luo uusi korjauksen tila.</span><span class="sxs-lookup"><span data-stu-id="b1370-113">Create a new repair status.</span></span>  
3. <span data-ttu-id="b1370-114">Täytä **Koodi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="b1370-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="b1370-115">Valitse **Huoltotilauksen tila** -kentässä tilauksen tila, johon korjaus linkitetään.</span><span class="sxs-lookup"><span data-stu-id="b1370-115">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="b1370-116">Valitsemasi huoltotilauksen tilan prioriteetti näkyy **Prioriteetti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b1370-116">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="b1370-117">Valitse korjauksen tila.</span><span class="sxs-lookup"><span data-stu-id="b1370-117">Choose a repair status.</span></span> <span data-ttu-id="b1370-118">Voit valita vain yhden tilan.</span><span class="sxs-lookup"><span data-stu-id="b1370-118">You can choose only one.</span></span>  
6. <span data-ttu-id="b1370-119">Valitse **Kirjaaminen sallittu** -kenttä, jos sallit huoltotilausten, myös huoltonimikkeiden kirjaamisen tämän korjauksen tilan yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b1370-119">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="b1370-120">Valitse **Odottava-tila sallittu** -valintaruutu, jos haluat sallia, että sellaisten huoltonimikkeitä sisältävän huoltotilauksien tilaksi voidaan manuaalisesti vaihtaa **Odottava**, joiden korjaustila se on.</span><span class="sxs-lookup"><span data-stu-id="b1370-120">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="b1370-121">Valitse **Työn alla -tila sallittu**-, **Valmis-tila sallittu**- ja **Estossa-tila sallittu**-valintaruudut samalla tavoin.</span><span class="sxs-lookup"><span data-stu-id="b1370-121">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="b1370-122">Huoltotilan prioriteettien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b1370-122">To set up service status priorities</span></span>  
1. <span data-ttu-id="b1370-123">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltotilauksen tila** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b1370-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b1370-124">Valitse huoltotilauksen tila, jolle haluat määrittää prioriteetin.</span><span class="sxs-lookup"><span data-stu-id="b1370-124">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="b1370-125">Valitse **Prioriteetti**-kentässä kyseisen huoltotilauksen tilan prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="b1370-125">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="b1370-126">Toista tämä vaihe kunkin tilan kohdalla.</span><span class="sxs-lookup"><span data-stu-id="b1370-126">Repeat this step for each status.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b1370-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b1370-127">See Also</span></span>  
[<span data-ttu-id="b1370-128">Huoltotilauksen tila ja korjauksen tila</span><span class="sxs-lookup"><span data-stu-id="b1370-128">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="b1370-129">Huoltohallinnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b1370-129">Setting Up Service Management</span></span>](service-setup-service.md)  
