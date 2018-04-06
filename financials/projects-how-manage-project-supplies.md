---
title: Projektin ostonimikkeiden tai palvelujen ostaminen ja tarvikkeiden hallinta| Microsoft Docs
description: "Ohjeaiheessa kerrotaan, miten tarvikkeita hallitaan sekä projekteille ostetaan materiaaleja ja palveluja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 498a9f7a1b95b5b27ad8cef55c8b558f5f3a718f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="manage-job-supplies"></a><span data-ttu-id="b4f37-103">Projektin tarvikkeiden hallinta</span><span class="sxs-lookup"><span data-stu-id="b4f37-103">Manage Job Supplies</span></span>
<span data-ttu-id="b4f37-104">Projektin nimikkeiden, palveluiden ja kulujen tarvikkeiden hallinta on olennainen ja tärkeä osa kaikkia projekteja.</span><span class="sxs-lookup"><span data-stu-id="b4f37-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="b4f37-105">Voit käyttää varastomääriä tai tehdä projektikohtaisia ostoja ostotilausten tai ostolaskujen avulla.</span><span class="sxs-lookup"><span data-stu-id="b4f37-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="b4f37-106">Oletetaan esimerkiksi, että tietokoneen huoltoprojektia varten tarvitaan uusi levy.</span><span class="sxs-lookup"><span data-stu-id="b4f37-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="b4f37-107">Tällöin luot ostolaskun uuden levyn ostamista varten ja kirjaat projektin, jossa sitä käytetään.</span><span class="sxs-lookup"><span data-stu-id="b4f37-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="b4f37-108">Jos ostoprosessi ei edellytä, että fyysinen tapahtuma kirjataan erikseen, osto voidaan käsitellä vain ostolaskussa tai **Projektin KP-päiväkirja** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="b4f37-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed in the **Job G/L Journal** window.</span></span> <span data-ttu-id="b4f37-109">Lisätietoja on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="b4f37-109">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="b4f37-110">Nimikkeiden tai palveluiden ostaminen projektille</span><span class="sxs-lookup"><span data-stu-id="b4f37-110">To purchase items or services for a job</span></span>
<span data-ttu-id="b4f37-111">Seuraavassa kerrotaan, miten projektille ostetaan tuotteita ostolaskun avulla.</span><span class="sxs-lookup"><span data-stu-id="b4f37-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="b4f37-112">Samat vaiheet toimivat myös silloin, kun käytetään ostotilausta.</span><span class="sxs-lookup"><span data-stu-id="b4f37-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="b4f37-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostolaskut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b4f37-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b4f37-114">Valitse **Uusi**-toiminto ja täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="b4f37-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="b4f37-115">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="b4f37-115">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="b4f37-116">Valitse **Projektinro**- ja **Projektitehtävän nro** -kentissä sen projektin tiedot, jolle haluat ostaa nimikkeitä tai huoltoja.</span><span class="sxs-lookup"><span data-stu-id="b4f37-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="b4f37-117">Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="b4f37-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="b4f37-118">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="b4f37-118">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

    <span data-ttu-id="b4f37-119">**Projektin rivityyppi** -kentässä valitsemasi arvo määrittää, luodaanko suunnittelurivi nimikkeen käytön kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b4f37-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="b4f37-120">Jos kentän arvo on **Laskutettava**, ne projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutettaviksi, luodaan.</span><span class="sxs-lookup"><span data-stu-id="b4f37-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="b4f37-121">Lisätietoja on kohdassa [Projektien laskutus](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="b4f37-121">For more information, see [Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="b4f37-122">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b4f37-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="b4f37-123">Projektin ostojen arvon tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="b4f37-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="b4f37-124">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b4f37-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="b4f37-125">Avaa sopiva projektikortti.</span><span class="sxs-lookup"><span data-stu-id="b4f37-125">Open a relevant job card.</span></span>

    <span data-ttu-id="b4f37-126">**Tehtävät**-pikavälilehden **Avoimet tilaukset** -kentässä näkyy projektin tehtävärivin ostoasiakirjojen varastonimikkeiden ja palveluiden avoin summa paikallisena valuuttana.</span><span class="sxs-lookup"><span data-stu-id="b4f37-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="b4f37-127">**Ei laskut. vast.ottojen summa** -kentässä näkyy ostoasiakirjoja vastaan toimitettujen, mutta vielä laskuttamattomien, nimikkeiden arvo.</span><span class="sxs-lookup"><span data-stu-id="b4f37-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="b4f37-128">Valitse jompikumpi kentistä ja avaa **Ostorivit**-ikkuna, jossa voit tarkastella liittyvien ostoasiakirjarivien tietoja sekä tietoa siitä, mitkä nimikkeet tai palvelut on vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="b4f37-128">Choose either of the fields to open the **Purchase Lines** window where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="b4f37-129">Projektiin liittyvän kulun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="b4f37-129">To post a job-related expense</span></span>
<span data-ttu-id="b4f37-130">Jos sisällytät satunnaisen tai kertaluontoisen projektin kulut, voit käyttää **Projektin KP-päiväkirja** -ikkunaa ja kirjata ne suoraan asianmukaiseen projektitiliin.</span><span class="sxs-lookup"><span data-stu-id="b4f37-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** window to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="b4f37-131">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektin KP-päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b4f37-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b4f37-132">Luo uusi rivi ja anna kulua koskevat tiedot, esimerkiksi **Projektinro**- ja **Projektitehtävän nro** -kenttien tiedot.</span><span class="sxs-lookup"><span data-stu-id="b4f37-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="b4f37-133">Kun päiväkirja on valmis, valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b4f37-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4f37-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b4f37-134">See Also</span></span>
[<span data-ttu-id="b4f37-135">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="b4f37-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="b4f37-136">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="b4f37-136">Finance</span></span>](finance.md)  
<span data-ttu-id="b4f37-137">[Osto](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="b4f37-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="b4f37-138">[Myynti](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="b4f37-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="b4f37-139">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b4f37-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

