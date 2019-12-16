---
title: Varastokausien käyttäminen | Microsoft Docs
description: Määrittämällä varastokauden voi hallita aikajaksoa, jolloin henkilöt voivat kirjata muutoksia varastoon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8b2a34db5d4e40f99fceb844150312d6c6dffc55
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879630"
---
# <a name="work-with-inventory-periods"></a><span data-ttu-id="78468-103">Varastokausien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="78468-103">Work with Inventory Periods</span></span>
<span data-ttu-id="78468-104">Varastokaudet määrittävät aikajakson, jolloin voit kirjata varastoon muutoksia.</span><span class="sxs-lookup"><span data-stu-id="78468-104">Inventory periods define a period of time in which you can post changes to inventory.</span></span> <span data-ttu-id="78468-105">Lopetuspäivämäärä määrittää, milloin varastokausi loppuu.</span><span class="sxs-lookup"><span data-stu-id="78468-105">An inventory period is defined by the date on which it ends, or the ending date.</span></span> <span data-ttu-id="78468-106">Kun suljet varastokauden, et voi enää kirjata varastoon odotettuja tai laskutettuja muutoksia ennen tätä lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="78468-106">When you close an inventory period, you cannot post any changes to inventory, either expected or invoiced, before this ending date.</span></span> <span data-ttu-id="78468-107">Et voi kirjata varastoon uusia arvoja ennen lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="78468-107">You cannot post any new values to inventory before the ending date.</span></span> <span data-ttu-id="78468-108">Jos suljetulla kaudella on avoimia nimiketapahtumia eli positiivisia määriä, joita ei ole vielä kohdistettu lähteviin transaktioihin, voit yhä kohdistaa lähteviä määriä näihin transaktioihin, vaikka kausi on suljettu.</span><span class="sxs-lookup"><span data-stu-id="78468-108">If you have open item entries in the closed period, meaning positive quantities that have not yet been applied to outbound transactions, you can still apply outbound quantities to these entries, even if the period is closed.</span></span>  

<span data-ttu-id="78468-109">Seuraavissa luvuissa kerrotaan, miten</span><span class="sxs-lookup"><span data-stu-id="78468-109">The following sections describe how to:</span></span>

* <span data-ttu-id="78468-110">varastokausia luodaan</span><span class="sxs-lookup"><span data-stu-id="78468-110">Create inventory periods.</span></span>  
* <span data-ttu-id="78468-111">varastokausia suljetaan</span><span class="sxs-lookup"><span data-stu-id="78468-111">Close inventory periods.</span></span>  
* <span data-ttu-id="78468-112">varastokausia avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="78468-112">Reopen inventory periods.</span></span>  

## <a name="to-create-an-inventory-period"></a><span data-ttu-id="78468-113">Varastokauden luominen</span><span class="sxs-lookup"><span data-stu-id="78468-113">To create an inventory period</span></span>  
1. <span data-ttu-id="78468-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastokaudet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="78468-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="78468-115">Luo uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="78468-115">Create a new line.</span></span>  
3. <span data-ttu-id="78468-116">Syötä **Lopetuspvm**-kenttään viimeinen päivämäärä, jonka haluat varastokaudelle määrittää.</span><span class="sxs-lookup"><span data-stu-id="78468-116">In the **Ending Date** field, enter the last date in the inventory period that you want to define.</span></span> <span data-ttu-id="78468-117">Kun kausi suljetaan, et voi enää kirjata ennen tätä päivämäärää tapahtuneita varaston muutoksia.</span><span class="sxs-lookup"><span data-stu-id="78468-117">When the period is closed, you will not be able to post inventory changes before this date.</span></span>  
4. <span data-ttu-id="78468-118">Anna **Nimi**-kenttään kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="78468-118">Enter a descriptive name in the **Name** field.</span></span> <span data-ttu-id="78468-119">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="78468-119">Choose the **OK** button.</span></span>  

## <a name="closing-inventory-periods"></a><span data-ttu-id="78468-120">Varastokausien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="78468-120">Closing Inventory Periods</span></span>  
<span data-ttu-id="78468-121">**Suljettu**-kenttä osoittaa, onko varastokausi suljettu varaston arvon muutoksilta.</span><span class="sxs-lookup"><span data-stu-id="78468-121">The **Closed** field indicates whether or not the inventory period is closed to inventory value changes.</span></span> <span data-ttu-id="78468-122">Et voi muokata tätä kenttää.</span><span class="sxs-lookup"><span data-stu-id="78468-122">You cannot edit this field.</span></span>  

<span data-ttu-id="78468-123">Voit sulkea minkä tahansa varastokauden, jos seuraavat kohdat toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="78468-123">You can close any inventory period, provided that the following is true:</span></span>  

* <span data-ttu-id="78468-124">Kaudella ei ole avoimia lähteviä nimiketapahtumia eli negatiivista varastoa.</span><span class="sxs-lookup"><span data-stu-id="78468-124">There are no open outbound item ledger entries, meaning negative inventory, in that period.</span></span>  
* <span data-ttu-id="78468-125">Kaikkien nimikkeiden kustannus on muutettu **Muuta kustannuksia - Nimiketapahtumat** -eräajon avulla.</span><span class="sxs-lookup"><span data-stu-id="78468-125">The cost of all items has been adjusted using the **Adjust Cost – Item Entries** batch job.</span></span>  

<span data-ttu-id="78468-126">Tällöin kaikki lähtevät transaktiot, kuten myyntitilausten, lähtevien siirtojen, myyntilaskujen, ostopalautusten ja ostohyvityslaskujen transaktiot, on kohdistettava varastomäärään.</span><span class="sxs-lookup"><span data-stu-id="78468-126">This means that all outbound transaction quantities, such as those from sales orders, outbound transfers, sales invoices, purchase returns, or purchase credit memos, must be applied to existing quantity in inventory.</span></span>  

### <a name="to-close-an-inventory-period"></a><span data-ttu-id="78468-127">Sulje varastokausi</span><span class="sxs-lookup"><span data-stu-id="78468-127">To close an inventory period</span></span>  
1. <span data-ttu-id="78468-128">Valitse **Muuta kustannuksia - Nimiketapahtumat** -toiminto ennen varastokauden sulkemista. Näin voit varmistaa, että kaikkien kustannusten muutokset on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="78468-128">Before closing an inventory period, choose the **Adjust Cost – Item Entries** action to ensure that all cost adjustments are posted.</span></span>

     <span data-ttu-id="78468-129">Suorittamalla **Sulje varastokausi - Testaa** -raportin voit määrittää, onko varastokaudella avoimia lähteviä transaktioita tai nimikkeitä, joiden kustannuksia ei ole vielä muutettu.</span><span class="sxs-lookup"><span data-stu-id="78468-129">Run the **Close Inventory Period – Test** report to determine if there are any open outbound item entries within the inventory period or any items whose cost has not yet been adjusted.</span></span>  
2. <span data-ttu-id="78468-130">Valitse **Sulje varastokausi – Testaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="78468-130">Choose the **Close Inventory Period – Test** action.</span></span>  

     <span data-ttu-id="78468-131">Suorittamalla **Kirjaa varaston kustannus KP:oon** -eräajon voit varmistaa, että kaikki kustannukset on viety pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="78468-131">Run the **Post Inventory Cost to G/L** batch job to ensure that all costs are posted to the general ledger.</span></span>  
3. <span data-ttu-id="78468-132">Valitse **Kirjaa varasto kirjanpitoon** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="78468-132">Choose the **Post Inventory to G/L** action.</span></span>  
4. <span data-ttu-id="78468-133">Valitse suljettava varastokausi **Varastokaudet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="78468-133">On the **Inventory Periods** page, select the inventory period you want to close.</span></span>  
5. <span data-ttu-id="78468-134">Valitse **Sulje varastokausi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="78468-134">Choose the **Close Period** action.</span></span> <span data-ttu-id="78468-135">Varastokauden sulkeuduttua et voi enää kirjata varaston muutoksia ennen lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="78468-135">After the inventory period has been closed, you cannot post inventory changes before the ending date.</span></span> <span data-ttu-id="78468-136">Kaikkien nimikkeiden kustannus on muutettava **Muuta kustannuksia - Nimiketapahtumat** -eräajolla ennen varastokauden sulkemista.</span><span class="sxs-lookup"><span data-stu-id="78468-136">The cost of all items must be adjusted with the **Adjust Cost – Item Entries** batch job before you close the inventory period.</span></span>  
6. <span data-ttu-id="78468-137">Valitse **Kyllä** voit sulkea kauden tai valitse **Ei**, jos haluat peruuttaa sulkemisen.</span><span class="sxs-lookup"><span data-stu-id="78468-137">Choose the **Yes** button to confirm that you want to close the period, or choose **No** to cancel the closing.</span></span>  
7. <span data-ttu-id="78468-138">Ohjelma sulkee varastokauden ja tuo näyttöön vahvistussanoman, kun kausi on suljettu.</span><span class="sxs-lookup"><span data-stu-id="78468-138">The inventory period is closed and a confirmation message is displayed when it is finished.</span></span>  

## <a name="reopening-inventory-periods"></a><span data-ttu-id="78468-139">Varastokausien avaaminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="78468-139">Reopening Inventory Periods</span></span>  
<span data-ttu-id="78468-140">Kun varastokausi on suljettu kerran, et voi poistaa sitä.</span><span class="sxs-lookup"><span data-stu-id="78468-140">After you have closed the inventory period, you cannot delete the inventory period.</span></span> <span data-ttu-id="78468-141">Voit kuitenkin avata sen uudelleen, jos haluat sallia kirjaukset ennen varastokauden lopetuspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="78468-141">You can, however, reopen it, if you would like to allow posting before the ending date of the inventory period.</span></span> <span data-ttu-id="78468-142">Kauden avaaminen uudelleen avaa myös kaikki varastokaudet, joilla on avattua kautta myöhäisemmät lopetuspäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="78468-142">Reopening a period also reopens all inventory periods with ending dates later than the period you reopen.</span></span>  

### <a name="to-reopen-an-inventory-period"></a><span data-ttu-id="78468-143">Avaa varastokausi uudelleen</span><span class="sxs-lookup"><span data-stu-id="78468-143">To reopen an inventory period</span></span>  
1. <span data-ttu-id="78468-144">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastokaudet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="78468-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="78468-145">Valitse uudelleen avattava varastokausi.</span><span class="sxs-lookup"><span data-stu-id="78468-145">Select the inventory period you want to reopen.</span></span>  
3. <span data-ttu-id="78468-146">Valitse **Avaa kausi uudelleen** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="78468-146">Choose the **Reopen Period** period action.</span></span> <span data-ttu-id="78468-147">Vahvista, että haluat avata kauden uudelleen.</span><span class="sxs-lookup"><span data-stu-id="78468-147">Confirm that you want to reopen the period.</span></span>  
4. <span data-ttu-id="78468-148">Kaikki varastojaksot, joiden lopetuspäivämäärät ovat valittua myöhäisemmät, avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="78468-148">All inventory periods with ending dates later than the period you selected are reopened.</span></span>  

## <a name="see-also"></a><span data-ttu-id="78468-149">Katso myös</span><span class="sxs-lookup"><span data-stu-id="78468-149">See Also</span></span>  
[<span data-ttu-id="78468-150">Rakennetiedot: varastokausi</span><span class="sxs-lookup"><span data-stu-id="78468-150">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="78468-151">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="78468-151">Finance</span></span>](finance.md)  
[<span data-ttu-id="78468-152">Varasto</span><span class="sxs-lookup"><span data-stu-id="78468-152">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="78468-153">Financialsin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="78468-153">Working with Financials</span></span>](ui-work-product.md)
