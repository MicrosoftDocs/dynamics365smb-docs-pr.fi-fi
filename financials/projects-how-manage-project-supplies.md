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
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 46cae53022ba5d65a370694c9818f52a7bf45525
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-job-supplies"></a><span data-ttu-id="ee703-103">Toimintaohje: Projektin tarvikkeiden hallinta</span><span class="sxs-lookup"><span data-stu-id="ee703-103">How to: Manage Job Supplies</span></span>
<span data-ttu-id="ee703-104">Projektin nimikkeiden, palveluiden ja kulujen tarvikkeiden hallinta on olennainen ja tärkeä osa kaikkia projekteja.</span><span class="sxs-lookup"><span data-stu-id="ee703-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="ee703-105">Voit käyttää varastomääriä tai tehdä projektikohtaisia ostoja ostotilausten tai ostolaskujen avulla.</span><span class="sxs-lookup"><span data-stu-id="ee703-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="ee703-106">Oletetaan esimerkiksi, että tietokoneen huoltoprojektia varten tarvitaan uusi levy.</span><span class="sxs-lookup"><span data-stu-id="ee703-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="ee703-107">Tällöin luot ostolaskun uuden levyn ostamista varten ja kirjaat projektin, jossa sitä käytetään.</span><span class="sxs-lookup"><span data-stu-id="ee703-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="ee703-108">Jos ostoprosessi ei edellytä, että fyysinen tapahtuma kirjataan erikseen, osto voidaan käsitellä vain ostolaskussa tai **Projektin KP-päiväkirja** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="ee703-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed in the **Job G/L Journal** window.</span></span> <span data-ttu-id="ee703-109">Lisätietoja on kohdassa [Toimintaohje: Projektien käytön kirjaaminen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="ee703-109">For more information, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="ee703-110">Nimikkeiden tai palveluiden ostaminen projektille</span><span class="sxs-lookup"><span data-stu-id="ee703-110">To purchase items or services for a job</span></span>
<span data-ttu-id="ee703-111">Seuraavassa kerrotaan, miten projektille ostetaan tuotteita ostolaskun avulla.</span><span class="sxs-lookup"><span data-stu-id="ee703-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="ee703-112">Samat vaiheet toimivat myös silloin, kun käytetään ostotilausta.</span><span class="sxs-lookup"><span data-stu-id="ee703-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="ee703-113">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Ostolaskut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ee703-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ee703-114">Valitse **Uusi**-toiminto ja täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="ee703-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="ee703-115">Lisätietoja on kohdassa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="ee703-115">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="ee703-116">Valitse **Projektinro**- ja **Projektitehtävän nro** -kentissä sen projektin tiedot, jolle haluat ostaa nimikkeitä tai huoltoja.</span><span class="sxs-lookup"><span data-stu-id="ee703-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="ee703-117">Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="ee703-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="ee703-118">Lisätietoja on kohdassa [Käyttäjän mukautus](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="ee703-118">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

    <span data-ttu-id="ee703-119">**Projektin rivityyppi** -kentässä valitsemasi arvo määrittää, luodaanko suunnittelurivi nimikkeen käytön kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ee703-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="ee703-120">Jos kentän arvo on **Laskutettava**, ne projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutettaviksi, luodaan.</span><span class="sxs-lookup"><span data-stu-id="ee703-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="ee703-121">Lisätietoja on kohdassa [Toimintaohje: Projektien laskuttaminen](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="ee703-121">For more information, see [How to: Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="ee703-122">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ee703-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="ee703-123">Projektin ostojen arvon tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="ee703-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="ee703-124">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ee703-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="ee703-125">Avaa sopiva projektikortti.</span><span class="sxs-lookup"><span data-stu-id="ee703-125">Open a relevant job card.</span></span>

    <span data-ttu-id="ee703-126">**Tehtävät**-pikavälilehden **Avoimet tilaukset** -kentässä näkyy projektin tehtävärivin ostoasiakirjojen varastonimikkeiden ja palveluiden avoin summa paikallisena valuuttana.</span><span class="sxs-lookup"><span data-stu-id="ee703-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="ee703-127">**Ei laskut. vast.ottojen summa** -kentässä näkyy ostoasiakirjoja vastaan toimitettujen, mutta vielä laskuttamattomien, nimikkeiden arvo.</span><span class="sxs-lookup"><span data-stu-id="ee703-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="ee703-128">Valitse jompikumpi kentistä ja avaa **Ostorivit**-ikkuna, jossa voit tarkastella liittyvien ostoasiakirjarivien tietoja sekä tietoa siitä, mitkä nimikkeet tai palvelut on vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="ee703-128">Choose either of the fields to open the **Purchase Lines** window where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="ee703-129">Projektiin liittyvän kulun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="ee703-129">To post a job-related expense</span></span>
<span data-ttu-id="ee703-130">Jos sisällytät satunnaisen tai kertaluontoisen projektin kulut, voit käyttää **Projektin KP-päiväkirja** -ikkunaa ja kirjata ne suoraan asianmukaiseen projektitiliin.</span><span class="sxs-lookup"><span data-stu-id="ee703-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** window to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="ee703-131">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektin KP-päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ee703-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ee703-132">Luo uusi rivi ja anna kulua koskevat tiedot, esimerkiksi **Projektinro**- ja **Projektitehtävän nro** -kenttien tiedot.</span><span class="sxs-lookup"><span data-stu-id="ee703-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="ee703-133">Kun päiväkirja on valmis, valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ee703-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee703-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ee703-134">See Also</span></span>
[<span data-ttu-id="ee703-135">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="ee703-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="ee703-136">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="ee703-136">Finance</span></span>](finance.md)  
<span data-ttu-id="ee703-137">[Osto](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="ee703-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="ee703-138">[Myynti](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="ee703-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="ee703-139">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ee703-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

