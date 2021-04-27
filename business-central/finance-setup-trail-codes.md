---
title: Kirjausketjujen määrittäminen | Microsoft Docs
description: Lue lisää kirjausketjujen seurantaan käytettävien lähdekoodien ja syykoodien määrittämisestä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6c20c57f05d17b0b52fcc1d4c9b1234cf03c6e97
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773837"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="8f486-103">Kirjausketjujen lähdekoodien ja syykoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8f486-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="8f486-104">Kaikille kirjatuille tapahtumille määritetään automaattisesti lähdekoodi niin, että tapahtumien alkuperä voidaan jäljittää.</span><span class="sxs-lookup"><span data-stu-id="8f486-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="8f486-105">Jos haluat antaa tapahtumille lisälähdekoodin, voit käyttää syykoodeja.</span><span class="sxs-lookup"><span data-stu-id="8f486-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="8f486-106">Syykoodien avulla ilmaistaan, miksi tapahtuma on luotu.</span><span class="sxs-lookup"><span data-stu-id="8f486-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="8f486-107">Syykoodit voidaan määrittää luomisen yhteydessä koko päiväkirjan malliin ja erään sekä yksittäisiin päiväkirjan riveihin ja asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="8f486-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="8f486-108">Käytä koodeja, jotka on helppo muistaa ja jotka ovat kuvaavia, käyttämällä sekä lähdekoodeja että syykoodeja.</span><span class="sxs-lookup"><span data-stu-id="8f486-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="8f486-109">Koodin tulee olla yksilöivä, ja voit määrittää niin monta koodia kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="8f486-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="8f486-110">Lähdekoodien määrittely</span><span class="sxs-lookup"><span data-stu-id="8f486-110">Define source codes</span></span>

<span data-ttu-id="8f486-111">Joskus haluat saada selville, miten tietty tapahtuma on syntynyt: esimerkiksi onko tapahtuma syntynyt yleisen päiväkirjan kirjauksen vai ostolaskun kirjauksen tuloksena.</span><span class="sxs-lookup"><span data-stu-id="8f486-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="8f486-112">Lähdekoodi ilmaisee, missä tapahtuma on syntynyt.</span><span class="sxs-lookup"><span data-stu-id="8f486-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="8f486-113">Tapahtumia syntyy, kun päiväkirja tai lasku kirjataan ja kun tietyt eräajot suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="8f486-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="8f486-114">Jokaisella kirjaustyypillä on oma lähdekoodinsa, joka liitetään, kun yksittäinen tapahtuma luodaan.</span><span class="sxs-lookup"><span data-stu-id="8f486-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="8f486-115">Päiväkirjojen, tilausten, laskujen ja hyvityslaskujen kirjaaminen, sekä eräajojen suorittaminen luovat tapahtumia taloudellisiin raportteihin.</span><span class="sxs-lookup"><span data-stu-id="8f486-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="8f486-116">**Lähdekoodiasetukset**-sivulla on useita pikavälilehtiä, yksi kutakin sovellusaluetta varten.</span><span class="sxs-lookup"><span data-stu-id="8f486-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="8f486-117">Jokaisessa pikavälilehdessä on asianomaisen sovellusalueen lähdekoodit.</span><span class="sxs-lookup"><span data-stu-id="8f486-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="8f486-118">Kun kirjaat tai suoritat eräajon, ohjelma liittää tapahtumaan automaattisesti oikean lähdekoodin.</span><span class="sxs-lookup"><span data-stu-id="8f486-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="8f486-119">Kun esimerkiksi kirjaat yleisestä päiväkirjasta, ohjelma antaa tapahtumalle koodin *YLEINENPVK*.</span><span class="sxs-lookup"><span data-stu-id="8f486-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="8f486-120">Tämän jälkeen voit suodattaa **Pääkirjanpidon tapahtumat** -sivun näyttämään, mitkä tapahtumat on kirjattu yleisestä päivä kirjasta tai myynti asiakirjoista, esimerkiksi</span><span class="sxs-lookup"><span data-stu-id="8f486-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="8f486-121">Lähdekoodien määrittely</span><span class="sxs-lookup"><span data-stu-id="8f486-121">To define source codes</span></span>

1. <span data-ttu-id="8f486-122">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Lähdekoodin määrittely** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8f486-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="8f486-123">Määritä **lähdekoodin määrittely** -ikkunassa kunkin kirjaustyypin ja eräajon osalta asianmukainen lähdekoodi.</span><span class="sxs-lookup"><span data-stu-id="8f486-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="8f486-124">Kentän sisältöä voi muuttaa myöhemmin, ja muutos vaikuttaa tuleviin kirjauksiin.</span><span class="sxs-lookup"><span data-stu-id="8f486-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="8f486-125">Lähdekoodien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="8f486-125">Change source codes</span></span>

<span data-ttu-id="8f486-126">Haluat ehkä muuttaa lähdekoodia.</span><span class="sxs-lookup"><span data-stu-id="8f486-126">You may want to change a source code.</span></span> <span data-ttu-id="8f486-127">Saatat haluta muuttaa lähdekoodin *YLEINENPVK* koodiksi *YLEINEN*.</span><span class="sxs-lookup"><span data-stu-id="8f486-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="8f486-128">Lähdekoodien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="8f486-128">To change source codes</span></span>

1. <span data-ttu-id="8f486-129">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Lähdekoodit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8f486-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="8f486-130">Valitse sillä rivillä, jolla muutettava koodi on, koodi **Koodi**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="8f486-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="8f486-131">Syötä uusi koodi ja napsauta sitten **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8f486-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="8f486-132">Voit myös muuttaa **Kuvaus**-kentän sisältöä.</span><span class="sxs-lookup"><span data-stu-id="8f486-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="8f486-133">Kaikilla uusilla kirjauksilla, jotka jatkossa kirjataan yleisestä päiväkirjasta, tulee olemaan tämä uusi lähdekoodi.</span><span class="sxs-lookup"><span data-stu-id="8f486-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="8f486-134">Syykoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8f486-134">Define reason codes</span></span>

<span data-ttu-id="8f486-135">Syykoodit täydentävät lähdekoodeja, ja niiden avulla ilmaistaan, miksi tapahtuma luotiin.</span><span class="sxs-lookup"><span data-stu-id="8f486-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="8f486-136">Voit määritellä syykoodeja yksittäisissä merkinnöissä ja voit liittää pysyvät koodit tiettyihin päiväkirjan malleihin ja päiväkirjan eriin.</span><span class="sxs-lookup"><span data-stu-id="8f486-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="8f486-137">Kun syykoodi on linkitetty päiväkirjan riviin tai myyntien tai ostojen otsikkoon, ohjelma merkitsee kaikkiin tapahtumiin syykoodin kirjatessaan tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="8f486-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="8f486-138">Syykoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8f486-138">To set up reason codes</span></span>

1. <span data-ttu-id="8f486-139">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Syykoodit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8f486-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="8f486-140">Anna **Syykoodit**-ikkunan **Koodi**-kenttään ensimmäinen koodi.</span><span class="sxs-lookup"><span data-stu-id="8f486-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="8f486-141">Syötä **Kuvaus**-kenttään selittävä teksti.</span><span class="sxs-lookup"><span data-stu-id="8f486-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="8f486-142">Toista nämä vaiheet kaikkien niiden koodien osalta, joita haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="8f486-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="8f486-143">Voit määrittää niin monta koodia kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="8f486-143">You can set up any number of codes.</span></span>

<span data-ttu-id="8f486-144">Seuraavassa kuvataan, miten syykoodi lisätään päiväkirjan malliin, mutta vastaavat vaiheet koskevat syykoodin lisäämistä päiväkirjan riville tai päiväkirjan erään.</span><span class="sxs-lookup"><span data-stu-id="8f486-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="8f486-145">Syykoodien määrittäminen päiväkirjan malleissa</span><span class="sxs-lookup"><span data-stu-id="8f486-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="8f486-146">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Yleinen päiväkirjamalli** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8f486-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="8f486-147">Määritä haluamasi koodi valitsemasi päiväkirjan mallin sisältävän rivin **Syykoodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8f486-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="8f486-148">Sulje päiväkirjan malli.</span><span class="sxs-lookup"><span data-stu-id="8f486-148">Close the journal template.</span></span>

<span data-ttu-id="8f486-149">Valittu syykoodi kopioituu niihin uusiin päiväkirjan eriin, jotka on luotu tämän päiväkirjan mallin avulla.</span><span class="sxs-lookup"><span data-stu-id="8f486-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="8f486-150">Syykoodeja liitetään päiväkirjan malleihin samalla tavalla muilla sovellusalueilla.</span><span class="sxs-lookup"><span data-stu-id="8f486-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="8f486-151">Syykoodien käyttäminen myynti- ja ostoasiakirjoissa</span><span class="sxs-lookup"><span data-stu-id="8f486-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="8f486-152">Avaa asianomainen myynti- tai ostoasiakirja.</span><span class="sxs-lookup"><span data-stu-id="8f486-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="8f486-153">Kirjoita koodi myynti- tai osto-otsikon **Syykoodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8f486-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="8f486-154">Kun lasku on kirjattu, syykoodi kopioituu kaikkiin KP-, asiakas- ja toimittajatapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="8f486-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="8f486-155">Et voi liittää erilaisia syykoodeja yksittäisille osto- ja myyntiriveille, koska kaikki rivit kirjataan yhtenä tapahtumana.</span><span class="sxs-lookup"><span data-stu-id="8f486-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="8f486-156">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="8f486-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="8f486-157">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8f486-157">See Also</span></span>

[<span data-ttu-id="8f486-158">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="8f486-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="8f486-159">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="8f486-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="8f486-160">Dimensioiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="8f486-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="8f486-161">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="8f486-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="8f486-162">Yrityksen kassavirran analysoiminen</span><span class="sxs-lookup"><span data-stu-id="8f486-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="8f486-163">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f486-163">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]