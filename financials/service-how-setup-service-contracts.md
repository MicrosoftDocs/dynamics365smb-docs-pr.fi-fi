---
title: "Huoltosopimusten määrittäminen | Microsoft Docs"
description: "Lisätietoja huoltosopimusten määrittämisestä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3eea1854139de9bdfd5dc992159dbc060c79509d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-service-contracts"></a><span data-ttu-id="d006b-103">Toimintaohje: Huoltosopimusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d006b-103">How to: Set Up Service Contracts</span></span>
<span data-ttu-id="d006b-104">Seuraavat on määritettävä, ennen kuin sopimuksia voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="d006b-104">Before you can work with contracts, you must set up the following:</span></span> 

* <span data-ttu-id="d006b-105">**Huoltosopimusryhmät** kerää yhteen toisiinsa jollain tavoin liittyvät huoltosopimukset.</span><span class="sxs-lookup"><span data-stu-id="d006b-105">**Service contract groups**, which gather service contracts that are related in some way.</span></span>
* <span data-ttu-id="d006b-106">**Huoltosopimuksen tiliryhmiä** käytetään ryhmittelemään yhteen huoltosopimuksille luotujen huoltolaskujen huoltosopimustilit.</span><span class="sxs-lookup"><span data-stu-id="d006b-106">**Service contract account groups**, which are used to group the service contract accounts together for service invoices created for service contracts.</span></span> <span data-ttu-id="d006b-107">Voit määrittää nämä ryhmät huoltosopimuksille.</span><span class="sxs-lookup"><span data-stu-id="d006b-107">You assign these groups to service contracts.</span></span>  
* <span data-ttu-id="d006b-108">**Sopimusmallit** määrittävät sopimusten asettelut sopimuksille, jotka sisältävät yleisimmin käytetyt huoltosopimusten tiedot.</span><span class="sxs-lookup"><span data-stu-id="d006b-108">**Contract templates** that define contract layouts of contracts that include the most commonly used service contract details.</span></span> <span data-ttu-id="d006b-109">Kun luot huoltosopimustarjouksia, voit luoda ne käyttämällä malleja.</span><span class="sxs-lookup"><span data-stu-id="d006b-109">When you create service contract quotes, you can create them by using templates.</span></span> <span data-ttu-id="d006b-110">Kun luot sopimustarjouksen, kentissä on automaattisesti mallikenttien sisältö.</span><span class="sxs-lookup"><span data-stu-id="d006b-110">When you create a contract quote, the fields automatically contain the contents of the template fields.</span></span>
* <span data-ttu-id="d006b-111">**Asiakasmallien** avulla voit luoda tarjouksia yhteyshenkilöille tai mahdollisille asiakkaille, joita ei ole rekisteröity asiakkaiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="d006b-111">**Customer templates** that let you create quotes for contacts or potential customers who are not registered as customers in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-set-up-a-service-contract-group"></a><span data-ttu-id="d006b-112">Huoltosopimusryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d006b-112">To set up a service contract group</span></span>  
1. <span data-ttu-id="d006b-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltosopimuksen ryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d006b-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d006b-114">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="d006b-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d006b-115">Valitse **Alennus vain sopimustil.** -valintaruutu, jos haluat, että sopimus- tai huoltoalennukset ovat voimassa vain sopimushuoltotilauksille, kuten ylläpidolle.</span><span class="sxs-lookup"><span data-stu-id="d006b-115">Choose the **Disc. on Contr. Orders Only** check box if you want contract or service discounts to be valid only for contract service orders, such as maintenance.</span></span>  

## <a name="to-set-up-a-service-contract-account-group"></a><span data-ttu-id="d006b-116">Huoltosopimusten tiliryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d006b-116">To set up a service contract account group</span></span>  
1. <span data-ttu-id="d006b-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltosopimuksen tiliryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d006b-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Serv. Contract Account Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d006b-118">Luo uusi huoltosopimuksen tiliryhmä.</span><span class="sxs-lookup"><span data-stu-id="d006b-118">Create a new service contract account group.</span></span>   
3. <span data-ttu-id="d006b-119">Täytä **Koodi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="d006b-119">Fill in the **Code** and **Description** fields.</span></span> <span data-ttu-id="d006b-120">Nämä kentät muodostavat huoltotiliryhmän kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="d006b-120">These fields describe the service account group.</span></span>  
4. <span data-ttu-id="d006b-121">Täytä  **Ei ennak. maksettu sop. tili** -kenttä ja valitse muiden kuin ennakkoon maksettujen sopimusten tilin KP-tilinumero.</span><span class="sxs-lookup"><span data-stu-id="d006b-121">Fill in the **Non-Prepaid Contract Acc.** field, choose general ledger account number for the non-prepaid account.</span></span>  
5. <span data-ttu-id="d006b-122">Valitse **Ennak.maksetun sopimuksen tili** -kentässä ennakkoon maksettujen sopimusten tilin KP-tilinumero.</span><span class="sxs-lookup"><span data-stu-id="d006b-122">In the **Prepaid Contract Acc.** field, choose the general ledger account number for the prepaid account.</span></span>  

## <a name="to-set-up-a-contract-template"></a><span data-ttu-id="d006b-123">Sopimusmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d006b-123">To set up a contract template</span></span>  
1. <span data-ttu-id="d006b-124">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltosopimuksen mallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d006b-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d006b-125">Luo uusi huoltosopimusmalli.</span><span class="sxs-lookup"><span data-stu-id="d006b-125">Create a new service contract template.</span></span>  
3. <span data-ttu-id="d006b-126">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="d006b-126">In the **No.**</span></span> <span data-ttu-id="d006b-127">sopimusmallin numero.</span><span class="sxs-lookup"><span data-stu-id="d006b-127">field, enter a number for the contract template.</span></span>  
  
     <span data-ttu-id="d006b-128">Vaihtoehtoisesti, jos olet määrittänyt sopimusmalleille numerosarjan **Huoltohallinnon asetukset** -ikkunaan, voit painaa Enter-painiketta, niin ohjelma lisää seuraavan saatavilla olevan sopimusmallin numeron.</span><span class="sxs-lookup"><span data-stu-id="d006b-128">Alternatively, if you have set up number series for contract templates in the **Service Mgt. Setup** window, you can press the Enter key to enter the next available contract template number.</span></span> <span data-ttu-id="d006b-129">Täytä muut kentät tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d006b-129">Fill in the other fields if appropriate.</span></span>  
  
4. <span data-ttu-id="d006b-130">Täytä **Lasku**-pikavälilehden **Huoltosop. tilir.koodi** -kenttään **laskutuskausi** ja muut tiedot.</span><span class="sxs-lookup"><span data-stu-id="d006b-130">On the **Invoice** FastTab, fill in the **Serv. Contract Acc. Group Code** field, the **Invoice Period**, and so on.</span></span> <span data-ttu-id="d006b-131">Täytä muut kentät tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d006b-131">Fill in the other fields if appropriate.</span></span>  
5. <span data-ttu-id="d006b-132">Lisää sopimusalennukset valitsemalla **Huoltoalennukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d006b-132">Choose the **Service Discounts** action to add contract discounts.</span></span>  

## <a name="to-set-up-a-customer-template"></a><span data-ttu-id="d006b-133">Asiakasmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d006b-133">To set up a customer template</span></span>  
1. <span data-ttu-id="d006b-134">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakasmallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d006b-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d006b-135">Luo uusi asiakasmallin kortti.</span><span class="sxs-lookup"><span data-stu-id="d006b-135">Create a new customer template card.</span></span>  
3. <span data-ttu-id="d006b-136">Anna **Yleinen**-pikavälilehden **Koodi**- ja **Kuvaus**-kentissä asiakasmallin koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="d006b-136">On the **General** FastTab, enter a code and a description for the customer template in the **Code** and **Description** fields respectively.</span></span> 
4. <span data-ttu-id="d006b-137">Määritä hakuehdot täyttämällä muut kentät, kuten **Maa-/aluekoodi**, **Territorion koodi** ja **Kielikoodi**.</span><span class="sxs-lookup"><span data-stu-id="d006b-137">To define search criteria, fill in the other fields, such as **Country/Region Code**, **Territory Code**, and **Language Code**.</span></span>  
5. <span data-ttu-id="d006b-138">Täytä **Yleinen liiketoim. kirjausryhmä**- ja **Asiakkaan kirjausryhmä** -kentät.</span><span class="sxs-lookup"><span data-stu-id="d006b-138">Fill in the **Gen. Bus. Posting Group** and **Customer Posting Group** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d006b-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d006b-139">See Also</span></span>
[<span data-ttu-id="d006b-140">Huoltohallinnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d006b-140">Setting Up Service Management</span></span>](service-setup-service.md)
