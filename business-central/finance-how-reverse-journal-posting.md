---
title: Kirjauksen kumoaminen kirjaamalla palautustapahtuma| Microsoft Docs
description: Jos olet tehnyt virheellisen kirjauksen yleiseen päiväkirjaan, Peruuta tapahtuma -toiminnolla kumottu kirjaus luo oikean kirjausketjun.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f2767fca96e1f3689fc4806d878381d02622f261
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2019
ms.locfileid: "938589"
---
# <a name="reverse-postings"></a><span data-ttu-id="1703f-103">Kirjausten peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="1703f-103">Reverse Postings</span></span>
<span data-ttu-id="1703f-104">Voit kumota virheellisen kirjauksen päiväkirjaan valitsemalla tapahtuman luomalla peruutustapahtuman (alkuperäistä tapahtumaa vastaava tapahtuma, jossa summakentässä on vastakkainen etumerkki), jossa on sama asiakirjanumero ja kirjauspäivämäärä kuin alkuperäisessä tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="1703f-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="1703f-105">Kun olet peruuttanut tapahtuman, lisää tapahtuma korjattuna.</span><span class="sxs-lookup"><span data-stu-id="1703f-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="1703f-106">Vain yleisen päiväkirjan riviltä kirjatut tapahtumat voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="1703f-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="1703f-107">Tapahtuman voi peruuttaa vain kerran.</span><span class="sxs-lookup"><span data-stu-id="1703f-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="1703f-108">Lisätietoja yleisestä päiväkirjasta tehtävistä kirjauksista on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="1703f-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="1703f-109">Jos olet tehnyt virheellinen negatiivisen määräkirjauksen, kuten kirjannut ostotilaukselle väärän määrän vastaanotetuksi mutta ei laskutetuksi, voit kumota kirjauksen.</span><span class="sxs-lookup"><span data-stu-id="1703f-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="1703f-110">Jos olet tehnyt virheellinen positiivisen määräkirjauksen, kuten kirjannut ostopalautustilaukselle väärän määrän toimitetuksi mutta ei laskutetuksi, voit kumota kirjauksen.</span><span class="sxs-lookup"><span data-stu-id="1703f-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="1703f-111">Pääkirjanpidon tapahtuman päiväkirjakirjauksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="1703f-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="1703f-112">Tapahtumia voi peruuttaa kaikista **Tapahtumakirjaukset**-sivuilta.</span><span class="sxs-lookup"><span data-stu-id="1703f-112">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="1703f-113">Seuraava menettely perustuu **Pääkirjanpidon tapahtumat** -sivuun.</span><span class="sxs-lookup"><span data-stu-id="1703f-113">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="1703f-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon tapahtumat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1703f-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="1703f-115">Valitse ensin peruutettava tapahtuma ja sitten **Peruuta tapahtuma** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1703f-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="1703f-116">Huomaa, että sen on oltava peräisin päiväkirjan kirjauksesta.</span><span class="sxs-lookup"><span data-stu-id="1703f-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="1703f-117">Valitse **Peruuta tapahtumat** -sivulla käsiteltävä tapahtuma ja valitse sitten **Peruuta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="1703f-117">On the **Reverse Transaction Entries** page, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="1703f-118">Valitse vahvistusviestissä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="1703f-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="1703f-119">Kirjatun ostovastaanoton määrän kirjauksen kumoaminen</span><span class="sxs-lookup"><span data-stu-id="1703f-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="1703f-120">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostovastaanotot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1703f-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1703f-121">Avaa kirjattu vastaanotto, jonka haluat kumota.</span><span class="sxs-lookup"><span data-stu-id="1703f-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="1703f-122">Valitse kumottavat rivit.</span><span class="sxs-lookup"><span data-stu-id="1703f-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="1703f-123">Valitse **Peruuta vast.otto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1703f-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="1703f-124">Korjaava rivi lisätään valitun kuittirivin alle.</span><span class="sxs-lookup"><span data-stu-id="1703f-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="1703f-125">Jos määrä vastaanotettiin fyysisen varastoinnin vastaanottona, korjaava rivi lisätään kirjattuun fyysisen varastoinnin vastaanottoon.</span><span class="sxs-lookup"><span data-stu-id="1703f-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="1703f-126">**Vastaanotettu määrä** ja **Vast.otettu laskuttamaton määrä** -kenttien arvoiksi liittyvällä ostotilauksella asetetaan nolla.</span><span class="sxs-lookup"><span data-stu-id="1703f-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="1703f-127">Kirjatun palautustoimituksen määrän kirjauksen kumoaminen ja tekeminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="1703f-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="1703f-128">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut palautustoimitukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1703f-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1703f-129">Avaa kumottava kirjattu palautustoimitus.</span><span class="sxs-lookup"><span data-stu-id="1703f-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="1703f-130">Valitse kumottavat rivit.</span><span class="sxs-lookup"><span data-stu-id="1703f-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="1703f-131">Valitse **Peruuta palautustoimitus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1703f-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="1703f-132">Ohjelma syöttää korjaavan rivin kirjatulle asiakirjalle ja **Toimitettu palautusmäärä** ja **Pal.määrä toimitettu ei laskutettu** -kentät palautustilauksella asetetaan nollaksi.</span><span class="sxs-lookup"><span data-stu-id="1703f-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="1703f-133">Palaa nyt ostopalautustilaukseen ja tee kirjaus uudelleen.</span><span class="sxs-lookup"><span data-stu-id="1703f-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="1703f-134">Kirjoita muistiin numero, joka on **Kirjattu palautustoimitus** -sivun **Palautustilauksen nro**</span><span class="sxs-lookup"><span data-stu-id="1703f-134">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="1703f-135">-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1703f-135">field.</span></span>  
6.  <span data-ttu-id="1703f-136">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostopalautustilaus** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1703f-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="1703f-137">Avaa kyseinen palautustilaus ja valitse **Avaa uudelleen** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1703f-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="1703f-138">Korjaa tapahtuma **Määrä**-kentässä ja kirjaa ostopalautustilaus uudelleen.</span><span class="sxs-lookup"><span data-stu-id="1703f-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="1703f-139">Negatiivisen tapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="1703f-139">To post a negative entry</span></span>  
<span data-ttu-id="1703f-140">**Korjaus**-kentän avulla voit kirjata tilille negatiivisen debetin kreditin sijaan tai negatiivisen kreditin debetin sijaan.</span><span class="sxs-lookup"><span data-stu-id="1703f-140">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="1703f-141">Tämä kenttä näkyy oletusarvoisesti kaikissa kirjauskansioissa, jotta lainsäädännölliset vaatimukset täytetään.</span><span class="sxs-lookup"><span data-stu-id="1703f-141">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="1703f-142">**Debet-summa**- ja **Kredit-summa**-kentät sisältävät sekä alkuperäisen että korjatun tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="1703f-142">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="1703f-143">Kentät eivät vaikuta tilin saldoon.</span><span class="sxs-lookup"><span data-stu-id="1703f-143">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="1703f-144">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki</span><span class="sxs-lookup"><span data-stu-id="1703f-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="1703f-145">Valitse haluttu erän nimi **Erän nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1703f-145">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="1703f-146">Lisää tiedot asianmukaisiin kenttiin.</span><span class="sxs-lookup"><span data-stu-id="1703f-146">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="1703f-147">Valitse **Korjaus**-valintaruutu sen kirjauskansion rivillä, jonka haluat ottaa käyttöön negatiivisia tapahtumia varten.</span><span class="sxs-lookup"><span data-stu-id="1703f-147">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="1703f-148">Kirjaa kirjauskansio valitsemalla **Kirjaa**-toiminto ja valitsemalla sitten **Kyllä**-painike.</span><span class="sxs-lookup"><span data-stu-id="1703f-148">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="1703f-149">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1703f-149">See Also</span></span>
[<span data-ttu-id="1703f-150">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="1703f-150">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="1703f-151">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="1703f-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="1703f-152">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="1703f-152">Finance</span></span>](finance.md)  
<span data-ttu-id="1703f-153">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1703f-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
