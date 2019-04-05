---
title: Esimerkkiskenaario – dynaamisten kohdistamisten määrittäminen myytyjen nimikkeiden perusteella | Microsoft Docs
description: Tässä aiheessa kuvataan esimerkki siitä, kuinka kohdistuksia määritetään käyttämällä dynaamista kohdistustapaa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 3103583c9781c283479c5f66e90f0e875faf46cc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795541"
---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="e549f-103">Esimerkkiskenaario: Dynaamisten kohdistamisten määrittäminen myytyjen nimikkeiden perusteella</span><span class="sxs-lookup"><span data-stu-id="e549f-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="e549f-104">Tässä aiheessa kuvataan esimerkki siitä, kuinka kohdistuksia määritetään käyttämällä dynaamista kohdistustapaa.</span><span class="sxs-lookup"><span data-stu-id="e549f-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="e549f-105">Esimerkissä muutetaan MYYNTI-kustannuspaikan kustannusten dynaaminen kohdistaminen tukemaan uutta IT-LAITTEISTO -kustannuskohdetta.</span><span class="sxs-lookup"><span data-stu-id="e549f-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="e549f-106">IT-LAITTEISTO-paketeissa ovat nimikenumerot välilä 8904-W – 8924-W.</span><span class="sxs-lookup"><span data-stu-id="e549f-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="e549f-107">Osuus lasketaan edellisen vuoden myyntilukujen avulla.</span><span class="sxs-lookup"><span data-stu-id="e549f-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="e549f-108">Kohdistus kirjataan apukustannuslajiin 9903.</span><span class="sxs-lookup"><span data-stu-id="e549f-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e549f-109">Esimerkissä käytetään demodataa [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta.</span><span class="sxs-lookup"><span data-stu-id="e549f-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="e549f-110">Märitä edellisvuonna myyytihin nimikkeisiin perustuvat dynaamiset kohdistukset</span><span class="sxs-lookup"><span data-stu-id="e549f-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="e549f-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kustannusten kohdistukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e549f-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e549f-112">Valitse **Kustannusten kohdistaminen** -sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e549f-112">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="e549f-113">Paina **Tunnus**-kentässä Enter tai kirjoita tunnus.</span><span class="sxs-lookup"><span data-stu-id="e549f-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="e549f-114">Syötä **Taso**-kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="e549f-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="e549f-115">Syötä arvot **Voimassaolo alkaa**- ja **Voimassaolo päättyy** -kenttiin.</span><span class="sxs-lookup"><span data-stu-id="e549f-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="e549f-116">Syötä **Kustannuspaikkakoodi**-kenttään **MYYNTI**.</span><span class="sxs-lookup"><span data-stu-id="e549f-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="e549f-117">Syötä **Luotto kustannustyyppiin** -kenttään kustannustyyppi **9903**.</span><span class="sxs-lookup"><span data-stu-id="e549f-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="e549f-118">Syötä **Kohdekustannustyyppi** -kenttään kustannustyyppi **9903**.</span><span class="sxs-lookup"><span data-stu-id="e549f-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="e549f-119">Valitse **Kohdekustannuskohde**-kentässä **Uusi**, luo uusi kustannuskohde IT-LAITTEISTO ja täytä kentät tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e549f-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="e549f-120">Valitse **IT-LAITTEET**.</span><span class="sxs-lookup"><span data-stu-id="e549f-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="e549f-121">Jätä **Kohdekustannuspaikka**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="e549f-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="e549f-122">Valitse **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki kertyneet kustannukset kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="e549f-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="e549f-123">Valitse **Peruste**-kentässä kohdistusperuste **Nimikkeitä myyty (summa)**.</span><span class="sxs-lookup"><span data-stu-id="e549f-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="e549f-124">Syötä **Nro suodatus** -kenttään **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="e549f-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="e549f-125">Syötä **Päivämäärän suodatuskoodi** -kenttään **Edellinen vuosi**.</span><span class="sxs-lookup"><span data-stu-id="e549f-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="e549f-126">Valitse **Laske kohdistusavain** -toiminto ja laske osuus.</span><span class="sxs-lookup"><span data-stu-id="e549f-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e549f-127">käyttää edellisen vuoden myyntilukuja laskettaessa 1596.50 PVA:n 100 prosentin osuus IT-LAITTEISTO -paketteja varten.</span><span class="sxs-lookup"><span data-stu-id="e549f-127">uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="e549f-128">Tämä tarkoittaa sitä, että kaikki viime vuonna myydyt nimikkeet kohdennetaan kustannuskohteelle IT-LAITTEISTO.</span><span class="sxs-lookup"><span data-stu-id="e549f-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e549f-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e549f-129">See Also</span></span>  
[<span data-ttu-id="e549f-130">Kustannusten määrittäminen ja kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="e549f-130">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="e549f-131">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="e549f-131">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="e549f-132">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="e549f-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)
