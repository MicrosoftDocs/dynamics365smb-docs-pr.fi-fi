---
title: Ennakkolaskumaksujen luominen | Microsoft Docs
description: "Lisätietoja tilanteiden käsittelyssä, jossa edellytät itse ennakkomaksua toimittajasi edellyttää sitä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dd090720943d0d7271200e087642a80157cbdbbd
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="2fb80-103">Ennakkomaksulaskujen luominen</span><span class="sxs-lookup"><span data-stu-id="2fb80-103">Create Prepayment Invoices</span></span>
<span data-ttu-id="2fb80-104">Jos haluat, että asiakkaat lähettävät maksun ennen kuin toimitat heille tilauksen tai jos toimittaja haluaa maksun ennen kuin toimitus lähetetään sinulle, voit käyttää Ennakkomaksu-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="2fb80-104">If you require your customers to submit payment before you ship an order to them, or if your vendor requires you to submit payment before they ship an order to you, you can use the prepayment functionality.</span></span>  

<span data-ttu-id="2fb80-105">Kun olet luonut myynti- tai ostotilauksen, voit luoda ennakkomaksun laskun.</span><span class="sxs-lookup"><span data-stu-id="2fb80-105">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="2fb80-106">Voit käyttää kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai voit muuttaa laskun summia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2fb80-106">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="2fb80-107">Voit määrittää esimerkiksi koko tilauksen yhteissumman.</span><span class="sxs-lookup"><span data-stu-id="2fb80-107">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="2fb80-108">Seuraavaksi käsitellään myyntitilausten ennakkomaksun laskuttamista.</span><span class="sxs-lookup"><span data-stu-id="2fb80-108">The following procedure describes how to invoice a prepayment for a sales orders.</span></span> <span data-ttu-id="2fb80-109">Ostotilausten vaiheet ovat vastaavanlaiset.</span><span class="sxs-lookup"><span data-stu-id="2fb80-109">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="2fb80-110">Ennakkomaksulaskun luominen</span><span class="sxs-lookup"><span data-stu-id="2fb80-110">To create a prepayment invoice</span></span>  
1. <span data-ttu-id="2fb80-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2fb80-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2fb80-112">Luo uusi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="2fb80-112">Create a new sales order.</span></span> <span data-ttu-id="2fb80-113">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="2fb80-113">For more information, see [sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="2fb80-114">**Ennakkomaksu**-pikavälilehden **Ennakkomaksuprosentti**-kenttä täytetään automaattisesti, jos asiakaskortissa on oletusennakkomaksuprosentti.</span><span class="sxs-lookup"><span data-stu-id="2fb80-114">On the **Prepayment** FastTab, the **Prepayment %** field will be filled in automatically if there is a default prepayment percentage on the customer card.</span></span> <span data-ttu-id="2fb80-115">Kentän sisältöä voidaan muuttaa.</span><span class="sxs-lookup"><span data-stu-id="2fb80-115">You can change the contents of the field.</span></span> <span data-ttu-id="2fb80-116">Ennakkomaksun osuus kopioidaan otsikosta vain niille riveille, jotka eivät kopioi ennakkomaksun vakio-osuutta nimikkeeltä.</span><span class="sxs-lookup"><span data-stu-id="2fb80-116">The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.</span></span>  

    <span data-ttu-id="2fb80-117">Jos **Tiivistä ennakkomaksu** -kenttä on valittuna, rivit yhdistetään laskussa, jos:</span><span class="sxs-lookup"><span data-stu-id="2fb80-117">If the **Compress Prepayment** field is selected, lines will be combined on the invoice if:</span></span>  
    - <span data-ttu-id="2fb80-118">Riveillä on sama KP-tili ennakkomaksuja varten (yleisten kirjausasetusten mukaisesti).</span><span class="sxs-lookup"><span data-stu-id="2fb80-118">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="2fb80-119">Riveillä on samat dimensiot.</span><span class="sxs-lookup"><span data-stu-id="2fb80-119">They have the same dimensions.</span></span>  

    <span data-ttu-id="2fb80-120">Jätä kenttä tyhjäksi, jos haluat määrittää ennakkomaksulaskun, jossa on yksi rivi kutakin ennakkomaksuprosentin sisältävää myyntitilausriviä varten.</span><span class="sxs-lookup"><span data-stu-id="2fb80-120">Leave the field blank if you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage.</span></span>  

3. <span data-ttu-id="2fb80-121">Täytä myyntirivit.</span><span class="sxs-lookup"><span data-stu-id="2fb80-121">Fill in the sales lines.</span></span>  

    <span data-ttu-id="2fb80-122">Jos nimikkeille on määritetty oletusennakkomaksuprosentit, ohjelma kopioi oletusarvon automaattisesti rivin **Ennakkomaksuprosentti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2fb80-122">If default prepayment percentages have been set up for your items, they are automatically copied to the **Prepayment %** field on the line.</span></span> <span data-ttu-id="2fb80-123">Muussa tapauksessa ennakkomaksuprosentti kopioidaan tunnistetiedoista.</span><span class="sxs-lookup"><span data-stu-id="2fb80-123">Otherwise, the prepayment percentage is copied from the header.</span></span> <span data-ttu-id="2fb80-124">Voit muuttaa rivin **Ennakkomaksuprosentti**-kentän sisällön.</span><span class="sxs-lookup"><span data-stu-id="2fb80-124">You can change the contents of the **Prepayment %** field on the line.</span></span>  
4. <span data-ttu-id="2fb80-125">Jos haluat kohdistaa yhden etumaksuprosentin koko tilaukseen, muuta tunnistetietojen **Ennakkomaksuprosentti**-kentän arvo rivien täyttämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="2fb80-125">If you want to apply one prepayment percentage to the entire order, change the **Prepayment %** field on the header after filling in the lines.</span></span>  
5. <span data-ttu-id="2fb80-126">Valitse **Tilastot**-toiminto, jos haluat tarkastella ennakkomaksun kokonaissummaa.</span><span class="sxs-lookup"><span data-stu-id="2fb80-126">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="2fb80-127">Jos haluat muuttaa ennakkomaksun kokonaissummaa, voit muuttaa **Myyntitilaustilastot**-ikkunan **Ennakkomaksun summa** -kentän sisältöä.</span><span class="sxs-lookup"><span data-stu-id="2fb80-127">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field in the **Sales Order Statistics** window.</span></span>  

    <span data-ttu-id="2fb80-128">Jos **Hinnat sisältävät ALV:n** -kenttä on valittuna, **Ennakkomaksun summa sis. ALV:a** -kenttää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="2fb80-128">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="2fb80-129">Jos muutat **Ennakkomaksun summa** -kentän sisältöä, summa jaetaan suhteellisesti muiden rivien kesken, paitsi niiden, joiden **Ennakkomaksuprosentti**-kentän arvo on **0**.</span><span class="sxs-lookup"><span data-stu-id="2fb80-129">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  
6. <span data-ttu-id="2fb80-130">Voit tulostaa testiraportin ennen ennakkomaksulaskun kirjaamista valitsemalla ensin **Ennakkomaksu**- ja sitten **Ennakkomaksun testiraportti** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="2fb80-130">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
7. <span data-ttu-id="2fb80-131">Voit kirjata ennakkomaksulaskun valitsemalla ensin **Ennakkomaksu**- ja sitten **Kirjaa ennakkomaksulasku** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="2fb80-131">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="2fb80-132">Voit kirjata ja tulostaa ennakkomaksulaskun valitsemalla **Kirjaa ja tulosta ennakkomaksulasku** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="2fb80-132">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="2fb80-133">Voit antaa lisää tilauksen ennakkomaksulaskuja.</span><span class="sxs-lookup"><span data-stu-id="2fb80-133">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="2fb80-134">Tee tämä nostamalla yhden tai useamman rivin ennakkomaksua ja muuttamalla tarvittaessa asiakirjan päivämäärää ja kirjaamalla ennakkomaksulasku.</span><span class="sxs-lookup"><span data-stu-id="2fb80-134">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="2fb80-135">Uusi lasku luodaan ennakkomaksun toistaiseksi laskutettujen summien ja uuden ennakkomaksun summan välisen eron vuoksi.</span><span class="sxs-lookup"><span data-stu-id="2fb80-135">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2fb80-136">Jos sijaintisi on Pohjois-Amerikassa, et voi muuttaa ennakkomaksun osuutta sen jälkeen, kun ennakkomaksulasku on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="2fb80-136">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="2fb80-137">Tämä on estetty pohjoisamerikkalaisessa [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa, koska arvonlisäveron laskutoimitus tuottaa muutoin väärän tuloksen.</span><span class="sxs-lookup"><span data-stu-id="2fb80-137">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="2fb80-138">Kun olet valmis kirjaamaan loput laskusta, kirjaa se kuten mikä tahansa lasku. Ennakkomaksusumma vähennetään automaattisesti erääntyvästä summasta.</span><span class="sxs-lookup"><span data-stu-id="2fb80-138">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2fb80-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2fb80-139">See Also</span></span>  
[<span data-ttu-id="2fb80-140">Ennakkomaksujen laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="2fb80-140">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="2fb80-141">Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="2fb80-141">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="2fb80-142">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="2fb80-142">Finance</span></span>](finance.md)  
<span data-ttu-id="2fb80-143">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2fb80-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

