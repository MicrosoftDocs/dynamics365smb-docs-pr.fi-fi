---
title: Korvaavien huoltonimikkeiden lainaaminen | Microsoft Docs
description: "Voit lainata asiakkaille lainatavaroita väliaikaisesti niiden huoltonimikkeiden tilalle, jotka olet vastaanottanut huollettavaksi."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/28/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ab8ac8e4cdfda63ed797415fcd183b410feea6bc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-lend-and-receive-loaners"></a><span data-ttu-id="dea73-103">Toimintaohje: Lainatavaroiden lainaaminen ja vastaanottaminen</span><span class="sxs-lookup"><span data-stu-id="dea73-103">How to: Lend and Receive Loaners</span></span>
<span data-ttu-id="dea73-104">Asiakkaille voi lainata lainatavaroita väliaikaisesti niiden huoltonimikkeiden tilalle, jotka olet vastaanottanut huollettavaksi.</span><span class="sxs-lookup"><span data-stu-id="dea73-104">You can lend customers loaners to temporarily replace service items that you have received for servicing.</span></span>  
  
## <a name="to-lend-a-loaner-item"></a><span data-ttu-id="dea73-105">Lainanimikkeiden lainaaminen</span><span class="sxs-lookup"><span data-stu-id="dea73-105">To lend a loaner item</span></span>    
1. <span data-ttu-id="dea73-106">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="dea73-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dea73-107">Avaa haluamasi huoltotilauksen kortti.</span><span class="sxs-lookup"><span data-stu-id="dea73-107">Open the relevant service order card.</span></span>  
3. <span data-ttu-id="dea73-108">Napsauta huoltonimikeriviä, jolla lainatavaralla korvattava huoltonimike on.</span><span class="sxs-lookup"><span data-stu-id="dea73-108">Select the service item line with the service item you want to replace with a loaner.</span></span>  
4. <span data-ttu-id="dea73-109">Määritä **Lainatavaranro** -kenttään</span><span class="sxs-lookup"><span data-stu-id="dea73-109">In the **Loaner No.**</span></span> <span data-ttu-id="dea73-110">sopiva lainanimike.</span><span class="sxs-lookup"><span data-stu-id="dea73-110">field, choose the relevant loaner item.</span></span>  
5. <span data-ttu-id="dea73-111">Vahvista laina valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="dea73-111">Choose **Yes** to confirm the loan.</span></span>  

## <a name="to-receive-a-loaner"></a><span data-ttu-id="dea73-112">Lainatavaroiden vastaanottaminen</span><span class="sxs-lookup"><span data-stu-id="dea73-112">To receive a loaner</span></span>  
<span data-ttu-id="dea73-113">Kun asiakkaalta vastaanotetaan lainatavara, vastaanotto tulee rekisteröidä.</span><span class="sxs-lookup"><span data-stu-id="dea73-113">When you receive a loaner from a customer, you must register the receipt.</span></span> <span data-ttu-id="dea73-114">Tämä tehdään **Huoltotilaus**-, **Kirjattu huoltotoimitus**- ja **Lainatavarakortti**-ikkunoissa.</span><span class="sxs-lookup"><span data-stu-id="dea73-114">You do this in the **Service Order**, **Posted Service Shipment**, and **Loaner Card** windows.</span></span> <span data-ttu-id="dea73-115">Seuraavassa kuvataan, miten lainatavaroita vastaanotetaan **Huoltotilaus**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="dea73-115">This procedure shows how to receive loaners in the **Service Order** window.</span></span>  
  
1. <span data-ttu-id="dea73-116">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="dea73-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dea73-117">Avaa haluamasi huoltotilaus.</span><span class="sxs-lookup"><span data-stu-id="dea73-117">Open the relevant service order.</span></span>  
3. <span data-ttu-id="dea73-118">Valitse vastaanotettavan lainatavaran huoltonimikerivi.</span><span class="sxs-lookup"><span data-stu-id="dea73-118">Choose the service item line with the loaner you want to receive.</span></span>  
4. <span data-ttu-id="dea73-119">Valitse ensin **Toiminnot**, sitten **Toiminnot** ja lopuksi **Ota vastaan lainatavara**.</span><span class="sxs-lookup"><span data-stu-id="dea73-119">Choose **Actions**, choose **Functions**, and then choose **Receive Loaner**.</span></span>  

## <a name="to-register-loaner-comments"></a><span data-ttu-id="dea73-120">Lainatavaroiden kommenttien rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="dea73-120">To register loaner comments</span></span>  
<span data-ttu-id="dea73-121">**Yleinen huoltokommenttilomake** -ikkunaa voidaan käyttää rekisteröimään kommentteja rekisteröidyille lainatavaroille.</span><span class="sxs-lookup"><span data-stu-id="dea73-121">You can use the **General Service Comment Sheet** window to register comments on registered loaners.</span></span>  
  
1. <span data-ttu-id="dea73-122">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjota **Lainatavarat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="dea73-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Loaners**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dea73-123">Avaa haluamasi lainatavaran kortti.</span><span class="sxs-lookup"><span data-stu-id="dea73-123">Open the relevant loaner card.</span></span>  
3. <span data-ttu-id="dea73-124">Valitse **Kommentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="dea73-124">Choose the **Comments** action.</span></span> <span data-ttu-id="dea73-125">**Yleinen vikojen huoltokommenttilomake** -ikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="dea73-125">The **General Service Comment Sheet** window opens.</span></span>  
4. <span data-ttu-id="dea73-126">Napsauta **Asiakirjan pvm** -kenttää ja syötä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="dea73-126">In the **Date** field, enter a date.</span></span>  
5. <span data-ttu-id="dea73-127">Kirjoita **Kommentti**-kenttään kommentti.</span><span class="sxs-lookup"><span data-stu-id="dea73-127">In the **Comment** field, enter a comment.</span></span> <span data-ttu-id="dea73-128">Voit syöttää enintään 80 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="dea73-128">You can enter a maximum of 80 characters.</span></span> <span data-ttu-id="dea73-129">Jos sinun täytyy syöttää lisätekstiä, siirry seuraavalle riville.</span><span class="sxs-lookup"><span data-stu-id="dea73-129">If you need to enter additional text, go to the next line.</span></span> <span data-ttu-id="dea73-130">Rivejä voi täyttää niin monta kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="dea73-130">You can fill in as many lines as necessary.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dea73-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="dea73-131">See Also</span></span>  
[<span data-ttu-id="dea73-132">Toimintaohje: Lainatavaraohjelman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dea73-132">How to: Set Up a Loaner Program</span></span>](service-how-setup-loaner-program.md)   

