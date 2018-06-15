---
title: "Sekkien myöntäminen, tulostaminen, peruuttaminen ja mitätöiminen| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten sekit myönnetään maksupäiväkirjan avulla, tulostetaan ja mitätöidään tai miten sekkitapahtumia tarkastellaan Business Central -sovelluksessa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a><span data-ttu-id="b1f6b-103">Sekkimaksujen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="b1f6b-103">Make Check Payments</span></span>
<span data-ttu-id="b1f6b-104">Voit myöntää sähköisiä ja manuaalisia sekkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b1f6b-105">Molemmissa menetelmissä sekit myönnetään toimittajille maksupäiväkirjaa käyttäen.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="b1f6b-106">Ohjelman avulla voit myös mitätöidä sekkejä ja tarkastella sekkitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="b1f6b-107">Seuraavassa kuvataan, miten voit maksaa toimittajalle tietokonesekillä kohdistamalla maksun asianmukaiseen toimittajalaskuun, tulostamalla sekin ja kirjaamalla maksun maksetuksi.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-107">The following procedure shows how to pay a vendor with a computer checks by applying the payment to the relevant vendor invoice, printing the check, and then posting the payment as paid.</span></span> <span data-ttu-id="b1f6b-108">Näin saadaan positiivinen toimittajatapahtuma, joka kohdistetaan negatiiviseen pankkitilitapahtumaan sekä fyysinen sekki pankin käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-108">This results in positive vendor ledger entries, applied to negative bank ledger entries, and physical checks for processing in the bank.</span></span>

<span data-ttu-id="b1f6b-109">Voit maksaa kahdella eri tyyppisellä sekillä.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-109">You can pay with two types of checks.</span></span> <span data-ttu-id="b1f6b-110">Molemmissa tyypeissä **Vastatilin tyyppi**- tai **Tilityyppi** -kentässä täytyy olla **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-110">For both types, the **Bal. Account Type** or the **Account Type** field must contain **Bank Account**.</span></span>

- <span data-ttu-id="b1f6b-111">**Tietokonesekki**: Valitse tämä vaihtoehto, jos haluat tulostaa sekin maksupäiväkirjan tällä rivillä olevalle summalle.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-111">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="b1f6b-112">Tulosta sekit, ennen kuin kirjaat päiväkirjan rivit.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-112">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="b1f6b-113">Voit valita vain **Tietokonesekki**, jos</span><span class="sxs-lookup"><span data-stu-id="b1f6b-113">You can only select **Computer Check** if</span></span>
- <span data-ttu-id="b1f6b-114">**Manuaalinen sekki**: Valitse tämä vaihtoehto, jos olet luonut sekin manuaalisesti ja haluat luoda vastaavan sekkitapahtuman tälle summalle.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-114">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="b1f6b-115">Tämän vaihtoehdon avulla et voi tulostaa sekkiä.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-115">By using this option, you cannot print the check.</span></span>

> [!NOTE]  
> <span data-ttu-id="b1f6b-116">Voit varmistaa lähettämällä toimittaja-, sekki- ja maksutiedot sisältävän tiedoston, että pankki vahvistaa vain tarkistetut sekit ja summat.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-116">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="b1f6b-117">Lisätietoja on kohdassa [Positive Pay -tiedostojen vieminen](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="b1f6b-117">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="b1f6b-118">Tulostin on määritettävä oikein sekkimuotoja varten. Myös käytettävä sekkien asettelu on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-118">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="b1f6b-119">Lisätietoja on kohdassa [Sekkien asetteluiden määrittäminen](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="b1f6b-119">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a><span data-ttu-id="b1f6b-120">Maksaaksesi toimittajalaskun tietokonesekillä</span><span class="sxs-lookup"><span data-stu-id="b1f6b-120">To pay a vendor invoice with a computer check</span></span>
<span data-ttu-id="b1f6b-121">Seuraavassa kuvataan, miten toimittajalle maksetaan sekillä.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-121">The following describes how to pay a vendor by check.</span></span> <span data-ttu-id="b1f6b-122">Vaiheet ovat samankaltaiset kuin hyvitettäessä asiakkaalle sekkimaksuna.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-122">The steps are similar to refund a customer by check.</span></span>

1. <span data-ttu-id="b1f6b-123">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="b1f6b-124">Täytä maksupäiväkirjan rivit.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-124">Fill in the payment journal lines.</span></span> <span data-ttu-id="b1f6b-125">Lisätietoja on ohjeaiheessa [Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md).</span><span class="sxs-lookup"><span data-stu-id="b1f6b-125">For more information, see [Record Payments and Refunds](payables-how-post-payments-refunds.md).</span></span>
3. <span data-ttu-id="b1f6b-126">Valitse **Maksutavan koodi** -kentässä **Sekki**.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-126">In the **Payment Method Code** field, select **Check**.</span></span>
4. <span data-ttu-id="b1f6b-127">Valitse **Pankkimaksun tyyppi** -kentässä **Tietokonesekki**.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-127">In the **Bank Payment Type** field, select **Computer Check**.</span></span>
5. <span data-ttu-id="b1f6b-128">Valitse **Tulosta sekki** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-128">Choose the **Print Check** action.</span></span>
6. <span data-ttu-id="b1f6b-129">Täytä **Sekki**-ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-129">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="b1f6b-130">Valitse **Lähetä kohteeseen** -painike, sitten **PDF-tiedosto**-asetus ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-130">Choose the **Send to** button, select the **PDF Document** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="b1f6b-131">Fyysiset sekit voidaan nyt viedä pankkiin käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-131">The physical checks can now be brought to the bank for processing.</span></span> <span data-ttu-id="b1f6b-132">Jatka maksun kirjaamiseen kohdistuksen mukaan toimittajalle ja maksun suorittamiseksi järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-132">Proceed to post the payment as applied to the vendor and thereby paid in the system.</span></span>
8. <span data-ttu-id="b1f6b-133">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-133">Choose the **Post** action.</span></span>

<span data-ttu-id="b1f6b-134">Täysin kohdistetut toimittajatapahtumat ja pankkitilitapahtumat luodaan.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-134">Fully applied vendor ledger entries and bank ledger entries are created.</span></span>

> [!NOTE]  
> <span data-ttu-id="b1f6b-135">Jos sekkejä täytyy tulostaa ja maksaa monessa valuutassa eri pankkitileiltä, sinun täytyy suorittaa **Tulosta sekki** -eräajo erikseen kullekin valuutalle ja määrittää sopivat pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-135">If you want to print and pay checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="b1f6b-136">Kirjaamattomien ja tulostettujen sekkien peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="b1f6b-136">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="b1f6b-137">Voit peruuttaa kirjaamattomat sekit niiden tulostamisen jälkeen **Maksupäiväkirja**-ikkunan **Mitätöi sekki** -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-137">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="b1f6b-138">Valitse **Maksupäiväkirja**-ikkunassa **Mitätöi sekki** ja valitse peruutettavat sekit.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-138">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="b1f6b-139">Sekkien mitätöiminen</span><span class="sxs-lookup"><span data-stu-id="b1f6b-139">To void checks</span></span>
<span data-ttu-id="b1f6b-140">Kun sekkimaksu on kirjattu, voit peruuttaa (mitätöidä) sekit vain tuloksena syntyvistä pankkitapahtumista.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-140">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="b1f6b-141">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="b1f6b-142">Valitse oikea pankkitili, valitse **Muokkaa**-toiminto ja valitse sitten **Sekkitapahtumat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-142">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="b1f6b-143">Valitse **Sekkitapahtumat**-ikkunassa **Mitätöi sekki** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-143">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="b1f6b-144">Valitse **Mitätöi vain sekki** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-144">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="b1f6b-145">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-145">Choose the **OK** button.</span></span>

## <a name="to-view-a-summary-of-posted-checks"></a><span data-ttu-id="b1f6b-146">Voit tarkastella kirjattujen sekkien yhteenvetoa</span><span class="sxs-lookup"><span data-stu-id="b1f6b-146">To view a summary of posted checks</span></span>
<span data-ttu-id="b1f6b-147">Jos haluat tarkistaa kirjatuttuja sekkejä, esimerkiksi yhdelle toimittajalle maksetut useat sekit, voit käyttää **Pankkitili – sekin tiedot** -raporttia.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-147">If you want to review posted checks, for example to verify multiple checks paid to one vendor, you can use the **Bank Account - Check Details** report.</span></span>
1. <span data-ttu-id="b1f6b-148">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankkitili – sekin tiedot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-148">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Account - Check Details**, and then choose the related link.</span></span>
2. <span data-ttu-id="b1f6b-149">Aseta haluamasi suodattimet ja valitse sitten **Esikatselu**-painike.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-149">Set filters as relevant, and then choose the **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1f6b-150">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b1f6b-150">See Also</span></span>
[<span data-ttu-id="b1f6b-151">Maksujen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="b1f6b-151">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="b1f6b-152">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="b1f6b-152">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="b1f6b-153">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b1f6b-153">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="b1f6b-154">Positive Pay -tiedoston vienti</span><span class="sxs-lookup"><span data-stu-id="b1f6b-154">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="b1f6b-155">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b1f6b-155">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

