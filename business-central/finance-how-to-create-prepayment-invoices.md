---
title: Ennakkolaskumaksujen luominen | Microsoft Docs
description: Lisätietoja tilanteiden käsittelyssä, jossa edellytät itse ennakkomaksua toimittajasi edellyttää sitä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2020
ms.author: edupont
ms.openlocfilehash: 85a5bbd3c1920aaac3e0560737f921c7518d1d32
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503592"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="81b4d-103">Ennakkomaksulaskujen luominen</span><span class="sxs-lookup"><span data-stu-id="81b4d-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="81b4d-104">Jos asiakkaiden on lähetettävä maksu, ennen kuin lähetät tilauksen heille, voit käyttää ennakkomaksutoimintoja.</span><span class="sxs-lookup"><span data-stu-id="81b4d-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="81b4d-105">Näin voi toimia myös silloin, jos toimittaja edellyttää, että lähetät maksun ennen tilauksen toimittamista.</span><span class="sxs-lookup"><span data-stu-id="81b4d-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="81b4d-106">Voit aloittaa ennakkomaksuprosessin, kun olet luonut ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="81b4d-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="81b4d-107">Jos kyseisellä asiakkaalla tai toimittajalla on oletusarvoinen ennakkomaksuprosentti, se sisällytetään automaattisesti tuloksena olevaan ennakkomaksulaskuun.</span><span class="sxs-lookup"><span data-stu-id="81b4d-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="81b4d-108">Voit määrittää ennakkomaksuprosentin myös koko asiakirjalle.</span><span class="sxs-lookup"><span data-stu-id="81b4d-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="81b4d-109">Kun olet luonut myynti- tai ostotilauksen, voit luoda ennakkomaksun laskun.</span><span class="sxs-lookup"><span data-stu-id="81b4d-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="81b4d-110">Voit käyttää kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai voit muuttaa laskun summia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="81b4d-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="81b4d-111">Voit määrittää esimerkiksi koko tilauksen yhteissumman.</span><span class="sxs-lookup"><span data-stu-id="81b4d-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="81b4d-112">Seuraavaksi käsitellään myyntitilauksen ennakkomaksun laskuttamista.</span><span class="sxs-lookup"><span data-stu-id="81b4d-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="81b4d-113">Ostotilausten vaiheet ovat vastaavanlaiset.</span><span class="sxs-lookup"><span data-stu-id="81b4d-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="81b4d-114">Ennakkomaksulaskun luominen</span><span class="sxs-lookup"><span data-stu-id="81b4d-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="81b4d-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="81b4d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="81b4d-116">Luo uusi myyntitilaus asianomaiselle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="81b4d-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="81b4d-117">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="81b4d-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="81b4d-118">**Ennakkomaksu**-pikavälilehden **Ennakkomaksuprosentti**-kenttä määrittää prosentin, jolla ennakkomaksun summa lasketaan.</span><span class="sxs-lookup"><span data-stu-id="81b4d-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="81b4d-119">Jos asiakaskortissa on oletusarvoinen ennakkomaksuprosentti, kenttä täytetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="81b4d-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="81b4d-120">Prosenttia voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="81b4d-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="81b4d-121">Valitse **Tiivistä ennakkomaksu** -kenttä, jos haluat luoda ennakkomaksulaskuun rivejä, jotka yhdistää myyntitilauksen rivejä seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="81b4d-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="81b4d-122">Riveillä on sama KP-tili ennakkomaksuja varten (yleisten kirjausasetusten mukaisesti).</span><span class="sxs-lookup"><span data-stu-id="81b4d-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="81b4d-123">Riveillä on samat dimensiot.</span><span class="sxs-lookup"><span data-stu-id="81b4d-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="81b4d-124">Jos haluat määrittää ennakkomaksulaskun, jossa on yksi rivi kutakin ennakkomaksuprosentin sisältävää myyntitilausriviä varten. älä valitse **Tiivistä ennakkomaksu** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="81b4d-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="81b4d-125">Ennakkomaksun eräpäivä lasketaan automaattisesti **Ennakkomaksun maksuehtojen koodi** -arvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="81b4d-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="81b4d-126">Täytä myyntirivit.</span><span class="sxs-lookup"><span data-stu-id="81b4d-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="81b4d-127">Jos olet määrittänyt oletusarvoisen ennakkomaksuprosentin joko asiakkaalle tai tämän asiakirjan **Ennakkomaksu**-pikavälilehdessä, tämä arvo kopioidaan kullekin riville.</span><span class="sxs-lookup"><span data-stu-id="81b4d-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="81b4d-128">Voit muuttaa rivin **Ennakkomaksuprosentti**-kentän sisällön.</span><span class="sxs-lookup"><span data-stu-id="81b4d-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="81b4d-129">Valitse **Tilastot**-toiminto, jos haluat tarkastella ennakkomaksun kokonaissummaa.</span><span class="sxs-lookup"><span data-stu-id="81b4d-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="81b4d-130">Jos haluat muuttaa ennakkomaksun kokonaissummaa, voit muuttaa **Myyntitilaustilastot**-sivun **Ennakkomaksun summa** -kentän sisältöä.</span><span class="sxs-lookup"><span data-stu-id="81b4d-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="81b4d-131">Jos **Hinnat sisältävät ALV:n** -kenttä on valittuna, **Ennakkomaksun summa sis. ALV:a** -kenttää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="81b4d-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="81b4d-132">Jos muutat **Ennakkomaksun summa** -kentän sisältöä, summa jaetaan suhteellisesti muiden rivien kesken, paitsi niiden, joiden **Ennakkomaksuprosentti**-kentän arvo on **0**.</span><span class="sxs-lookup"><span data-stu-id="81b4d-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="81b4d-133">Voit tulostaa testiraportin ennen ennakkomaksulaskun kirjaamista valitsemalla ensin **Ennakkomaksu**- ja sitten **Ennakkomaksun testiraportti** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="81b4d-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="81b4d-134">Voit kirjata ennakkomaksulaskun valitsemalla ensin **Ennakkomaksu**- ja sitten **Kirjaa ennakkomaksulasku** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="81b4d-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="81b4d-135">Voit kirjata ja tulostaa ennakkomaksulaskun valitsemalla **Kirjaa ja tulosta ennakkomaksulasku** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="81b4d-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="81b4d-136">Voit antaa lisää tilauksen ennakkomaksulaskuja.</span><span class="sxs-lookup"><span data-stu-id="81b4d-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="81b4d-137">Tee tämä nostamalla yhden tai useamman rivin ennakkomaksua ja muuttamalla tarvittaessa asiakirjan päivämäärää ja kirjaamalla ennakkomaksulasku.</span><span class="sxs-lookup"><span data-stu-id="81b4d-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="81b4d-138">Uusi lasku luodaan ennakkomaksun toistaiseksi laskutettujen summien ja uuden ennakkomaksun summan välisen eron vuoksi.</span><span class="sxs-lookup"><span data-stu-id="81b4d-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="81b4d-139">Jos sijaintisi on Pohjois-Amerikassa, et voi muuttaa ennakkomaksun osuutta sen jälkeen, kun ennakkomaksulasku on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="81b4d-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="81b4d-140">Tämä on estetty pohjoisamerikkalaisessa [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa, koska arvonlisäveron laskutoimitus tuottaa muutoin väärän tuloksen.</span><span class="sxs-lookup"><span data-stu-id="81b4d-140">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="81b4d-141">Kun olet valmis kirjaamaan loput laskusta, kirjaa se kuten mikä tahansa lasku. Ennakkomaksusumma vähennetään automaattisesti erääntyvästä summasta.</span><span class="sxs-lookup"><span data-stu-id="81b4d-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="81b4d-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="81b4d-142">See Also</span></span>

[<span data-ttu-id="81b4d-143">Ennakkomaksujen laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="81b4d-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="81b4d-144">Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="81b4d-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="81b4d-145">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="81b4d-145">Finance</span></span>](finance.md)  
<span data-ttu-id="81b4d-146">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81b4d-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
