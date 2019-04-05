---
title: Varastokausien käyttäminen | Microsoft Docs
description: Määrittämällä varastokauden voi hallita aikajaksoa, jolloin henkilöt voivat kirjata muutoksia varastoon.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 1aae1d32b86000ea8a5f867f1ee4c07d8bc1ff09
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796097"
---
# <a name="work-with-inventory-periods"></a><span data-ttu-id="6be36-103">Varastokausien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="6be36-103">Work with Inventory Periods</span></span>
<span data-ttu-id="6be36-104">Varastokaudet määrittävät aikajakson, jolloin voit kirjata varastoon muutoksia.</span><span class="sxs-lookup"><span data-stu-id="6be36-104">Inventory periods define a period of time in which you can post changes to inventory.</span></span> <span data-ttu-id="6be36-105">Lopetuspäivämäärä määrittää, milloin varastokausi loppuu.</span><span class="sxs-lookup"><span data-stu-id="6be36-105">An inventory period is defined by the date on which it ends, or the ending date.</span></span> <span data-ttu-id="6be36-106">Kun suljet varastokauden, et voi enää kirjata varastoon odotettuja tai laskutettuja muutoksia ennen tätä lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="6be36-106">When you close an inventory period, you cannot post any changes to inventory, either expected or invoiced, before this ending date.</span></span> <span data-ttu-id="6be36-107">Et voi kirjata varastoon uusia arvoja ennen lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="6be36-107">You cannot post any new values to inventory before the ending date.</span></span> <span data-ttu-id="6be36-108">Jos suljetulla kaudella on avoimia nimiketapahtumia eli positiivisia määriä, joita ei ole vielä kohdistettu lähteviin transaktioihin, voit yhä kohdistaa lähteviä määriä näihin transaktioihin, vaikka kausi on suljettu.</span><span class="sxs-lookup"><span data-stu-id="6be36-108">If you have open item entries in the closed period, meaning positive quantities that have not yet been applied to outbound transactions, you can still apply outbound quantities to these entries, even if the period is closed.</span></span>  

<span data-ttu-id="6be36-109">Seuraavissa luvuissa kerrotaan, miten</span><span class="sxs-lookup"><span data-stu-id="6be36-109">The following sections describe how to:</span></span>  

* <span data-ttu-id="6be36-110">varastokausia luodaan</span><span class="sxs-lookup"><span data-stu-id="6be36-110">Create inventory periods.</span></span>  
* <span data-ttu-id="6be36-111">varastokausia suljetaan</span><span class="sxs-lookup"><span data-stu-id="6be36-111">Close inventory periods.</span></span>  
* <span data-ttu-id="6be36-112">varastokausia avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6be36-112">Reopen inventory periods.</span></span>  

## <a name="to-create-an-inventory-period"></a><span data-ttu-id="6be36-113">Varastokauden luominen</span><span class="sxs-lookup"><span data-stu-id="6be36-113">To create an inventory period</span></span>  
1. <span data-ttu-id="6be36-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastokaudet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6be36-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6be36-115">Luo uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="6be36-115">Create a new line.</span></span>  
3. <span data-ttu-id="6be36-116">Syötä **Lopetuspvm**-kenttään viimeinen päivämäärä, jonka haluat varastokaudelle määrittää.</span><span class="sxs-lookup"><span data-stu-id="6be36-116">In the **Ending Date** field, enter the last date in the inventory period that you want to define.</span></span> <span data-ttu-id="6be36-117">Kun kausi suljetaan, et voi enää kirjata ennen tätä päivämäärää tapahtuneita varaston muutoksia.</span><span class="sxs-lookup"><span data-stu-id="6be36-117">When the period is closed, you will not be able to post inventory changes before this date.</span></span>  
4. <span data-ttu-id="6be36-118">Anna **Nimi**-kenttään kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="6be36-118">Enter a descriptive name in the **Name** field.</span></span> <span data-ttu-id="6be36-119">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="6be36-119">Choose the **OK** button.</span></span>  

## <a name="closing-inventory-periods"></a><span data-ttu-id="6be36-120">Varastokausien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="6be36-120">Closing Inventory Periods</span></span>  
<span data-ttu-id="6be36-121">**Suljettu**-kenttä osoittaa, onko varastokausi suljettu varaston arvon muutoksilta.</span><span class="sxs-lookup"><span data-stu-id="6be36-121">The **Closed** field indicates whether or not the inventory period is closed to inventory value changes.</span></span> <span data-ttu-id="6be36-122">Et voi muokata tätä kenttää.</span><span class="sxs-lookup"><span data-stu-id="6be36-122">You cannot edit this field.</span></span>  

<span data-ttu-id="6be36-123">Voit sulkea minkä tahansa varastokauden, jos seuraavat kohdat toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="6be36-123">You can close any inventory period, provided that the following is true:</span></span>  

* <span data-ttu-id="6be36-124">Kaudella ei ole avoimia lähteviä nimiketapahtumia eli negatiivista varastoa.</span><span class="sxs-lookup"><span data-stu-id="6be36-124">There are no open outbound item ledger entries, meaning negative inventory, in that period.</span></span>  
* <span data-ttu-id="6be36-125">Kaikkien nimikkeiden kustannus on muutettu **Muuta kustannuksia - Nimiketapahtumat** -eräajon avulla.</span><span class="sxs-lookup"><span data-stu-id="6be36-125">The cost of all items has been adjusted using the **Adjust Cost – Item Entries** batch job.</span></span>  

<span data-ttu-id="6be36-126">Tällöin kaikki lähtevät transaktiot, kuten myyntitilausten, lähtevien siirtojen, myyntilaskujen, ostopalautusten ja ostohyvityslaskujen transaktiot, on kohdistettava varastomäärään.</span><span class="sxs-lookup"><span data-stu-id="6be36-126">This means that all outbound transaction quantities, such as those from sales orders, outbound transfers, sales invoices, purchase returns, or purchase credit memos, must be applied to existing quantity in inventory.</span></span>  

### <a name="to-close-an-inventory-period"></a><span data-ttu-id="6be36-127">Sulje varastokausi</span><span class="sxs-lookup"><span data-stu-id="6be36-127">To close an inventory period</span></span>  
1. <span data-ttu-id="6be36-128">Suorita  **Muuta kustannuksia - Nimiketapahtumat** -eräajo ennen varastokauden sulkemista. Näin voit varmistaa, että kaikkien kustannusten muutokset on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="6be36-128">Before closing an inventory period, run the **Adjust Cost – Item Entries** batch job to ensure that all cost adjustments are posted.</span></span> <span data-ttu-id="6be36-129">Valitse **Toiminnot**-välilehden **Funktiot**-ryhmästä **Muuta kustann. - Nimiketapaht.**.</span><span class="sxs-lookup"><span data-stu-id="6be36-129">On the **Actions** tab, in the **Functions** group, choose **Adjust Cost – Item Entries**.</span></span>  

     <span data-ttu-id="6be36-130">Suorittamalla **Sulje varastokausi - Testaa** -raportin voit määrittää, onko varastokaudella avoimia lähteviä transaktioita tai nimikkeitä, joiden kustannuksia ei ole vielä muutettu.</span><span class="sxs-lookup"><span data-stu-id="6be36-130">Run the **Close Inventory Period – Test** report to determine if there are any open outbound item entries within the inventory period or any items whose cost has not yet been adjusted.</span></span>  
2. <span data-ttu-id="6be36-131">Valitse **Sulje varastokausi – Testaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="6be36-131">Choose the **Close Inventory Period – Test** action.</span></span>  

     <span data-ttu-id="6be36-132">Suorittamalla **Kirjaa varaston kustannus KP:oon** -eräajon voit varmistaa, että kaikki kustannukset on viety pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="6be36-132">Run the **Post Inventory Cost to G/L** batch job to ensure that all costs are posted to the general ledger.</span></span>  
3. <span data-ttu-id="6be36-133">Valitse **Kirjaa varasto kirjanpitoon** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="6be36-133">Choose the **Post Inventory to G/L** action.</span></span>  
4. <span data-ttu-id="6be36-134">Valitse suljettava varastokausi **Varastokaudet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6be36-134">On the **Inventory Periods** page, select the inventory period you want to close.</span></span>  
5. <span data-ttu-id="6be36-135">Valitse **Sulje varastokausi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="6be36-135">Choose the **Close Period** action.</span></span> <span data-ttu-id="6be36-136">Varastokauden sulkeuduttua et voi enää kirjata varaston muutoksia ennen lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="6be36-136">After the inventory period has been closed, you cannot post inventory changes before the ending date.</span></span> <span data-ttu-id="6be36-137">Kaikkien nimikkeiden kustannus on muutettava **Muuta kustannuksia - Nimiketapahtumat** -eräajolla ennen varastokauden sulkemista.</span><span class="sxs-lookup"><span data-stu-id="6be36-137">The cost of all items must be adjusted with the **Adjust Cost – Item Entries** batch job before you close the inventory period.</span></span>  
6. <span data-ttu-id="6be36-138">Valitse **Kyllä** voit sulkea kauden tai valitse **Ei**, jos haluat peruuttaa sulkemisen.</span><span class="sxs-lookup"><span data-stu-id="6be36-138">Choose the **Yes** button to confirm that you want to close the period, or choose **No** to cancel the closing.</span></span>  
7. <span data-ttu-id="6be36-139">Ohjelma sulkee varastokauden ja tuo näyttöön vahvistussanoman, kun kausi on suljettu.</span><span class="sxs-lookup"><span data-stu-id="6be36-139">The inventory period is closed and a confirmation message is displayed when it is finished.</span></span>  

## <a name="reopening-inventory-periods"></a><span data-ttu-id="6be36-140">Varastokausien avaaminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="6be36-140">Reopening Inventory Periods</span></span>  
<span data-ttu-id="6be36-141">Kun varastokausi on suljettu kerran, et voi poistaa sitä.</span><span class="sxs-lookup"><span data-stu-id="6be36-141">After you have closed the inventory period, you cannot delete the inventory period.</span></span> <span data-ttu-id="6be36-142">Voit kuitenkin avata sen uudelleen, jos haluat sallia kirjaukset ennen varastokauden lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="6be36-142">You can, however, reopen it, if you would like to allow posting before the ending date of the inventory period.</span></span> <span data-ttu-id="6be36-143">Kauden avaaminen uudelleen avaa myös kaikki varastokaudet, joilla on avattua kautta myöhäisemmät lopetuspäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="6be36-143">Reopening a period also reopens all inventory periods with ending dates later than the period you reopen.</span></span>  

### <a name="to-reopen-an-inventory-period"></a><span data-ttu-id="6be36-144">Avaa varastokausi uudelleen</span><span class="sxs-lookup"><span data-stu-id="6be36-144">To reopen an inventory period</span></span>  
1. <span data-ttu-id="6be36-145">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastokaudet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6be36-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6be36-146">Valitse uudelleen avattava varastokausi.</span><span class="sxs-lookup"><span data-stu-id="6be36-146">Select the inventory period you want to reopen.</span></span>  
3. <span data-ttu-id="6be36-147">Valitse **Avaa kausi uudelleen** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="6be36-147">Choose the **Reopen Period** period action.</span></span> <span data-ttu-id="6be36-148">Vahvista, että haluat avata kauden uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6be36-148">Confirm that you want to reopen the period.</span></span>  
4. <span data-ttu-id="6be36-149">Kaikki varastojaksot, joiden lopetuspäivämäärät ovat valittua myöhäisemmät, avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6be36-149">All inventory periods with ending dates later than the period you selected are reopened.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6be36-150">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6be36-150">See Also</span></span>  
[<span data-ttu-id="6be36-151">Rakennetiedot: varastokausi</span><span class="sxs-lookup"><span data-stu-id="6be36-151">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="6be36-152">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="6be36-152">Finance</span></span>](finance.md)  
[<span data-ttu-id="6be36-153">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="6be36-153">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6be36-154">Financialsin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6be36-154">Working with Financials</span></span>](ui-work-product.md)
