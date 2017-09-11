---
title: Positive Pay -tiedostojen vieminen| Microsoft Docs
description: "Voit varmistaa toimittaja- ja maksutiedot sisältävän Positive Pay -tiedoston viennin avulla, että pankki vahvistaa vain tarkistetut sekit ja summat."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dfae1975a78c9380b5b6d4086569d63fe3793832
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-export-a-positive-pay-file"></a><span data-ttu-id="ab0a1-103">Toimintaohje: Positive Pay -tiedoston vieminen</span><span class="sxs-lookup"><span data-stu-id="ab0a1-103">How to: Export a Positive Pay file</span></span>
<span data-ttu-id="ab0a1-104">Kun viet toimittajan tiedot, sekin numeron ja maksun summan sisältävän Positive Pay -tiedoston, jonka sitten lähetät viitetiedoiksi pankkiin maksuja käsitellessäsi, voit varmistaa, että pankki vahvistaa vain tarkistetut sekit ja summat.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ab0a1-105"> on määritetty tukemaan Bank of American ja City Bankin Positive Pay -tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-105"> is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="ab0a1-106">Positive Pay -pankkitilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ab0a1-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="ab0a1-107">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ab0a1-108">Avaa sen pankin kortti, jossa haluat käyttää Positive Pay -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="ab0a1-109">Kirjoita **Positive Pay -vientikoodi** -kenttään POSPAYBANK.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="ab0a1-110">Sulje ikkuna.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-110">Close the window.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="ab0a1-111">Positive Pay -tiedoston vienti</span><span class="sxs-lookup"><span data-stu-id="ab0a1-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="ab0a1-112">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ab0a1-113">Valitse pankkitili, johon haluat viedä Positive Pay -tiedoston.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="ab0a1-114">Valitse **Positive Pay, vienti** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="ab0a1-115">**Positive Pay, vienti** -ikkuna avautuu ja näkyvissä on maksut, jotka on tehty pankkitilille edellisen latauspäivän jälkeen (**Edellinen latauspvm**- ja **Edellinen latausaika** -kentät).</span><span class="sxs-lookup"><span data-stu-id="ab0a1-115">The **Positive Pay Export** window opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="ab0a1-116">Määrittää**Latauksen katkaisupvm** -kenttää päivämäärä, jota edeltäviä maksuja ei sisällytetä vientitiedostoon.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="ab0a1-117">Valitse **Vie**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="ab0a1-118">Valitse **Vie tiedosto** -ikkunassa **Tallenna**-painike ja tallenna tiedosto sopivaan paikkaan.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-118">In the **Export File** window, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="ab0a1-119">Lataa tiedosto sähköisen pankin sivustoon.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="ab0a1-120">Kirjoita muistiin tai kopioi vahvistusnumero, joka näkyy, kun tiedoston lataus on onnistunut.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="ab0a1-121">Vietyjen Positive Pay -tietueiden näyttäminen</span><span class="sxs-lookup"><span data-stu-id="ab0a1-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="ab0a1-122">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ab0a1-123">Valitse pankkitili, jonka Positive Pay -vientitietueet haluat näyttää.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="ab0a1-124">Valitse **Positive Pay -tapahtumat** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="ab0a1-125">Kaikki pankkitilin Positive Pay -vientitietueet näkyvät **Positive Pay -tapahtumat** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-125">In the **Positive Pay Entries** window, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="ab0a1-126">Anna kunkin vientitietueen **Vahvistusnumero**-kenttään numero, jonka sait, kun tiedoston lataus pankkiin onnistui.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="ab0a1-127">Voit tarkastella liittyviä maksurivejä valitsemalla **Positive Pay -tapahtuman tiedot** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="ab0a1-128">Positive Pay -tiedostojen uudelleenvienti</span><span class="sxs-lookup"><span data-stu-id="ab0a1-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="ab0a1-129">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ab0a1-130">Valitse pankkitili, johon haluat viedä Positive Pay -tiedostot uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="ab0a1-131">Valitse **Positive Pay -tapahtumat** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="ab0a1-132">Valitse uudelleenvietävä Positive Pay -vientitiedoston rivi.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="ab0a1-133">Valitse **Positive Pay -tapahtumat** -ikkunassa **Vie Positive Pay -maksu uudelleen tiedostoon** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="ab0a1-133">In the **Positive Pay Entries** window, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab0a1-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ab0a1-134">See Also</span></span>
[<span data-ttu-id="ab0a1-135">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="ab0a1-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="ab0a1-136">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ab0a1-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="ab0a1-137">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="ab0a1-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="ab0a1-138">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ab0a1-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

