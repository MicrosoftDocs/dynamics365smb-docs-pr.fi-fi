---
title: Puitemyyntitilauksien luominen | Microsoft Docs
description: "Käytä puitetilauksia, kun asiakas on päättänyt ostaa suuria määriä, jotka toimitetaan useissa pienissä toimituserissä määritetyn aikajakson sisällä."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 89db93227222d79e535f2d18400330aa30566f2f
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-blanket-sales-orders"></a><span data-ttu-id="f5949-103">Puitemyyntitilausten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f5949-103">Work with Blanket Sales Orders</span></span>
<span data-ttu-id="f5949-104">Puitemyyntitilaus kuvastaa yrityksesi ja asiakkaan välisen pitkäaikaisen sopimuksen runkoa.</span><span class="sxs-lookup"><span data-stu-id="f5949-104">A blanket sales order represents a framework for a long-term agreement between you and your customer.</span></span>

<span data-ttu-id="f5949-105">Puitetilaus tehdään yleensä silloin, kun asiakas on päättänyt ostaa suuria määriä, jotka toimitetaan useissa pienissä toimituserissä määritetyn aikajakson sisällä.</span><span class="sxs-lookup"><span data-stu-id="f5949-105">A blanket order is typically made when a customer has committed to purchasing large quantities that are to be delivered in several smaller shipments over a certain period of time.</span></span> <span data-ttu-id="f5949-106">Puitetilaukset kattavat usein vain yhden nimikkeen ja ennalta määritetyt toimituspäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="f5949-106">Often blanket orders cover only one item with predetermined delivery dates.</span></span> <span data-ttu-id="f5949-107">Pääsyy puitetilauksen käytölle myyntitilauksen käytön sijaan on se, että puitetilaukseen syötetyt määrät eivät vaikuta nimikkeen saatavuuteen, eli niitä voidaan käyttää valvonnan, ennustamisen ja suunnittelun lomakkeina.</span><span class="sxs-lookup"><span data-stu-id="f5949-107">The main reason for using a blanket order rather than a sales order is that quantities entered on a blanket order do not affect item availability and thus can be used as a worksheet for monitoring, forecasting, and planning purposes.</span></span>

<span data-ttu-id="f5949-108">Puitetilauksen jokainen erillinen toimitus voidaan määrittää tilausriviksi, joka voidaan toimitushetkellä muuntaa myyntitilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="f5949-108">On the blanket order, each separate shipment can be set up as an order line, which can then be converted into a sales order at the time of shipping.</span></span>

<span data-ttu-id="f5949-109">Esimerkki puitetilauksen käytöstä: Asiakas soittaa ja tilaa nimikettä 1 000 yksikköä. Asiakas haluaa, että nimikkeet toimitetaan 250 yksikön viikkoerissä seuraavan kuukauden aikana.</span><span class="sxs-lookup"><span data-stu-id="f5949-109">An example of when a blanket sales order could be used is if a customer calls and places an order of 1000 units of an item and they want the items to be delivered in 250 units every week over the next month.</span></span>

> [!NOTE]
> <span data-ttu-id="f5949-110">Puiteostotilaukset toimivat samoin kuin puitemyyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="f5949-110">Blanket purchase orders work in a similar way as blanket sales orders.</span></span> <span data-ttu-id="f5949-111">Näissä ohjeissa ei käsitellä puiteostotilauksia.</span><span class="sxs-lookup"><span data-stu-id="f5949-111">This documentation does not cover blanket purchase orders.</span></span>

## <a name="to-create-a-blanket-sales-order"></a><span data-ttu-id="f5949-112">Uuden puitemyyntitilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="f5949-112">To create a blanket sales order</span></span>  
1. <span data-ttu-id="f5949-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Puitemyyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f5949-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f5949-114">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f5949-114">Choose the **New** action.</span></span>  
3. <span data-ttu-id="f5949-115">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f5949-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="f5949-116">Jätä **Tilauspvm**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f5949-116">Leave the **Order Date** field blank.</span></span> <span data-ttu-id="f5949-117">Kun puitetilauksesta luodaan erillisiä myyntitilauksia, ohjelma määrittää myyntitilauksen tilauspäivämääräksi todellisen käsittelypäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="f5949-117">When the separate sales orders are created from the blanket order, the order date of the sales order is set to equal the actual work date.</span></span>
5. <span data-ttu-id="f5949-118">Luo **Rivit**-pikavälilehdessä erilliset rivit jokaista toimitusta varten.</span><span class="sxs-lookup"><span data-stu-id="f5949-118">On the **Lines** FastTab, create separate lines for each shipment.</span></span> <span data-ttu-id="f5949-119">Jos asiakas haluaa esim. 1 000 yksikköä niin, että ne on jaettu tasaisesti neljälle viikolle, sinun on syötettävä neljä erillistä riviä, joilla jokaisella on 250 yksikköä.</span><span class="sxs-lookup"><span data-stu-id="f5949-119">For instance, if your customer wants 1000 units split out equally between four weeks, you would enter four separate lines of 250 units each.</span></span>   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a><span data-ttu-id="f5949-120">Myyntitilauksen luominen puitemyyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="f5949-120">To create a sales order from a blanket sales order</span></span>  

1.  <span data-ttu-id="f5949-121">Voit luoda tilauksen mille tahansa puitekokoonpanotilauksen riveille poistamalla kaikkien niiden rivien **Toimitettava määrä** -kentän määrä, joita ET halua toimittaa tällä kertaa.</span><span class="sxs-lookup"><span data-stu-id="f5949-121">To create an order for any of the lines in the blanket assembly order, remove the quantity in the **Qty. to Ship** field on all the lines that you DO NOT wish to ship at this time.</span></span>  
2.  <span data-ttu-id="f5949-122">Kun olet valmis luomaan tilauksia, valitse ensin **Tee tilaus** -toiminto ja sitten **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f5949-122">When you are ready to create orders, choose the **Make Order**m action, and then choose **Yes**.</span></span> <span data-ttu-id="f5949-123">Näyttöön tulee sanoma, jossa kerrotaan puitetilauksen määrityksestä tilausnumeroon.</span><span class="sxs-lookup"><span data-stu-id="f5949-123">A message appears informing you that the blanket order has been assigned an order number.</span></span> <span data-ttu-id="f5949-124">Huomaa, että puitetilausta ei ole poistettu.</span><span class="sxs-lookup"><span data-stu-id="f5949-124">Note that the blanket order has not been deleted.</span></span>  
3.  <span data-ttu-id="f5949-125">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="f5949-125">Choose the **OK** button.</span></span>  
4.  <span data-ttu-id="f5949-126">Voit tuoda edellisten vaiheiden tulokset näkyviin valitsemalla ensin **Rivi**-toiminnon, sitten **Kirjaamattomat rivit** -toiminnon ja lopuksi **Tilaukset**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="f5949-126">To see the results of the preceding steps, choose the **Line** action, choose the **Unposted Lines** action, and then choose the **Orders** action.</span></span>  
5.  <span data-ttu-id="f5949-127">Valitse ensin oikea myyntitilaus **Myyntirivit**-ikkunassa, sitten **Rivit**-toiminto ja lopuksi **Näytä asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f5949-127">In the **Sales Lines** window, select the appropriate sales order, choose the **Line** action, and then choose the **Show Document** action.</span></span>  

<span data-ttu-id="f5949-128">Seuraava koskee myyntitilauksia sen jälkeen, kun ne on luotu puitemyyntitilauksista.</span><span class="sxs-lookup"><span data-stu-id="f5949-128">The following applies to sales orders after they have been created from blanket sales orders:</span></span>  

- <span data-ttu-id="f5949-129">Puitetilauksen myyntitilaukseksi muuntamisen jälkeen myyntitilaus sisältää kaikki puitetilauksen rivit.</span><span class="sxs-lookup"><span data-stu-id="f5949-129">After the blanket order is converted into a sales order, the sales order contains all the lines from the blanket order.</span></span> <span data-ttu-id="f5949-130">Rivit, joiden **Toimitettava määrä** -kentän määrä poistettiin, tulevat näkyviin, mutta niiden **Määrä**-kentät ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="f5949-130">The lines where the quantity in the **Qty. to Ship** field was deleted appear, but with blank **Quantity** fields.</span></span> <span data-ttu-id="f5949-131">Voit jättää tai poistaa rivit tai muokata niitä.</span><span class="sxs-lookup"><span data-stu-id="f5949-131">You may choose to leave, edit, or delete the lines.</span></span>  
- <span data-ttu-id="f5949-132">On tärkeä muistaa, että myyntitilausrivin määrä ei saa ylittää liitetyn puitetilausrivin määrää.</span><span class="sxs-lookup"><span data-stu-id="f5949-132">It is important to remember that the sales order line quantity must not exceed the quantity of the associated blanket order line.</span></span> <span data-ttu-id="f5949-133">Muussa tapauksessa myyntitilauksen kirjaus ei onnistu.</span><span class="sxs-lookup"><span data-stu-id="f5949-133">Otherwise, posting of the sales order will not be possible.</span></span>  
- <span data-ttu-id="f5949-134">Kun myyntitilaus on kirjattu toimitettuna ja/tai laskutettuna, ohjelma päivittää liittyvän puitetilauksen **Toimitettu määrä**- ja **Laskutettu määrä** -kentät.</span><span class="sxs-lookup"><span data-stu-id="f5949-134">When the sales order is posted as shipped and/or invoiced, the **Quantity Shipped** and **Quantity Invoiced** fields are updated on the related blanket order.</span></span>  
- <span data-ttu-id="f5949-135">Ohjelma tallentaa puitetilausnumeron ja rivinumeron ominaisuuksina myyntiriveille, kun ne luodaan puitetilauksesta.</span><span class="sxs-lookup"><span data-stu-id="f5949-135">The blanket order number and line number are recorded as properties of the sales lines when created from a blanket order.</span></span>  
- <span data-ttu-id="f5949-136">Jos myyntitilauksia ei luoda suoraan puitetilauksesta, mutta se liittyy puitetilaukseen, myyntitilauksen ja puitetilauksen välille voidaan muodostaa linkki syöttämällä liittyvän puitetilauksen numero myyntitilausrivin **Puitetilauksen nro**</span><span class="sxs-lookup"><span data-stu-id="f5949-136">When sales orders are not created directly from the blanket order but still relate to it, a link between a sales order and a blanket order can be established by entering the associated blanket order number in the **Blanket Order No.**</span></span> <span data-ttu-id="f5949-137">-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f5949-137">field on the sales order line.</span></span>  
- <span data-ttu-id="f5949-138">Kun myyntitilaus on luotu puitetilauksen rivien kokonaismäärällä, muita myyntitilauksia ei voi luoda samalle riville.</span><span class="sxs-lookup"><span data-stu-id="f5949-138">After the sales order has been created for the total quantity of a blanket order line, no other sales order can be created for the same line.</span></span> <span data-ttu-id="f5949-139">Käyttäjät eivät voi syöttää määrää **Toimitettava määrä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f5949-139">Users are prevented from entering a quantity in the **Qty. to Ship** field.</span></span> <span data-ttu-id="f5949-140">Jos puitetilaukseen täytyy kuitenkin lisätä määriä, voit kasvattaa **Määrä**-kentän arvoa. Sen jälkeen voit luoda lisätilauksia.</span><span class="sxs-lookup"><span data-stu-id="f5949-140">If, however, additional quantities need to be added to a blanket order, the value in the **Quantity** field can be increased and additional orders can then be created.</span></span>  
- <span data-ttu-id="f5949-141">Laskutettu puitemyyntitilaus säilytetään järjestelmässä, kunnes se poistetaan yksittäisiä puitemyyntitilauksia poistettaessa tai suoritettaessa **Poista virheelliset puitemyyntitilaukset** -eräajo.</span><span class="sxs-lookup"><span data-stu-id="f5949-141">The invoiced blanket sales order remains in the system until it is deleted, either by deleting individual blanket orders or by running the **Delete Invoiced Blanket Sales Orders** batch job.</span></span>  
- <span data-ttu-id="f5949-142">Jos asiakas on tallennettu myös kontaktina Markkinointi-kohdistusalueeseen ja jos olet määrittänyt puitemyyntitilauksille vuorovaikutusmallin koodin  **Kontaktienhallinnan asetukset** -ikkunassa, ohjelma tallentaa vuorovaikutuksen automaattisesti, kun tulostat puitemyyntitilauksen valitsemalla Vuorovaikutuslokin tapahtuma -taulukossa **Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="f5949-142">If a customer is also recorded as a contact in the Marketing application area, and if you have specified an interaction template code for blanket sales order in the **Marketing Setup** window, an interaction is recorded in the Interaction Log Entry table when you select **Print** to print the blanket sales order.</span></span>

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a><span data-ttu-id="f5949-143">Puiteostotilausten tilan katsominen</span><span class="sxs-lookup"><span data-stu-id="f5949-143">To view the status of a blanket purchase order</span></span>  
<span data-ttu-id="f5949-144">Voit nähdä puiteostotilauksen tilan **Ostopuitetilauksen tilastot** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="f5949-144">You can see the status of a blanket sales order in the **Purchase Blanket Order Statistics** window.</span></span> <span data-ttu-id="f5949-145">Tällä voi olla merkitystä, kun aletaan laskuttaa tilausta, joka luotiin puiteostotilauksesta.</span><span class="sxs-lookup"><span data-stu-id="f5949-145">This may be relevant when you start to invoice the order that is created from the blanket purchase order.</span></span>  

1.  <span data-ttu-id="f5949-146">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Puiteostotilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f5949-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f5949-147">Valitse ensin puiteostotilaus ja valitse sitten **Tilastot**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f5949-147">Select a blanket purchase order, and then choose the **Statistics** action.</span></span>  
3.  <span data-ttu-id="f5949-148">**Ostopuitetilauksen tilastot** -ikkunan **Yleinen**-pikavälilehdessä voit tarkastella koko tilauksen yhteenvetotietoja puiteostotilauksen rivien eri **Määrä-kenttien** yhteismäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="f5949-148">In the **Purchase Blanket Order Statistics** window, on the **General** FastTab, you can see summary information about the entire order based on the total quantity in the various **Quantity fields** on the blanket purchase order lines.</span></span>  

    - <span data-ttu-id="f5949-149">**Laskutus**-pikavälilehdessä voit tarkastella yhteenvetotietoja puiteostotilauksen rivien **Laskutettava määrä** -kenttien yhteismäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="f5949-149">On the **Invoicing** FastTab, you can see summary information based on the total quantity in the **Qty. to Invoice** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="f5949-150">**Toimitus**-pikavälilehdessä voit tarkastella yhteenvetotietoja puiteostotilauksen rivien **Vastaanotettava määrä** -kenttien yhteismäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="f5949-150">On the **Shipping** FastTab, you can see summary information based on the total quantity in the **Qty. to Receive** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="f5949-151">**Ennakkomaksu**-pikavälilehdessä voit tarkastella yhteenvetotietoja mahdollisista ennakkoon maksetuista summista.</span><span class="sxs-lookup"><span data-stu-id="f5949-151">On the **Prepayment** FastTab, you can see summary information about any prepaid amounts.</span></span>  
    - <span data-ttu-id="f5949-152">**Toimittaja**-pikavälilehdessä voit tarkastella toimittajaa koskevia perustietoja.</span><span class="sxs-lookup"><span data-stu-id="f5949-152">On the **Vendor** FastTab, you can see certain basic information about the vendor.</span></span>    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a><span data-ttu-id="f5949-153">Kirjaamattomien ja kirjattujen puitemyyntitilausrivien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="f5949-153">To view unposted and posted blanket sales order lines</span></span>   
<span data-ttu-id="f5949-154">Linkki puitemyyntitilauksen ja alkuperäisen myyntiasiakirjan, sekä kaikkien muiden myyntiasiakirjojen välillä säilytetään kirjaamisen jälkeen luettelona kirjatuista ja kirjaamattomista myyntitilauksen laskuriveistä.</span><span class="sxs-lookup"><span data-stu-id="f5949-154">The link between the blanket sales order and the originating sales order, and any other sales document, is retained after posting as a list of posted and unposted sales order invoice lines.</span></span>  

1. <span data-ttu-id="f5949-155">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Puitemyyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f5949-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon enter **Blanket Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="f5949-156">Avaa tarkasteltava puitemyyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="f5949-156">Open the blanket sales order you want to view.</span></span>
3. <span data-ttu-id="f5949-157">Näytä kirjaamattomat tapahtumat valitsemalla ensin kyseinen rivi, sitten **Rivi**-toiminto ja lopuksi **Kirjaamattomat rivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f5949-157">To view unposted entries, select the line in question, choose the **Line** action, and then choose the **Unposted Lines** action.</span></span> <span data-ttu-id="f5949-158">Valitse yksi seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="f5949-158">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="f5949-159">Asetus</span><span class="sxs-lookup"><span data-stu-id="f5949-159">Option</span></span></th>
    <th><span data-ttu-id="f5949-160">Description</span><span class="sxs-lookup"><span data-stu-id="f5949-160">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="f5949-161">**Tilaukset**</span><span class="sxs-lookup"><span data-stu-id="f5949-161">**Orders**</span></span></td>
    <td><span data-ttu-id="f5949-162">Määrittää avoimet tilaukset, jotka on merkitty liittyviksi valittuun riviin.</span><span class="sxs-lookup"><span data-stu-id="f5949-162">Specifies open orders associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f5949-163">**Laskut**</span><span class="sxs-lookup"><span data-stu-id="f5949-163">**Invoices**</span></span></td>
    <td><span data-ttu-id="f5949-164">Määrittää avoimet laskut, jotka on merkitty liittyviksi valittuun riviin.</span><span class="sxs-lookup"><span data-stu-id="f5949-164">Specifies open invoices that have been associated with the selected line.</span></span> <span data-ttu-id="f5949-165">Avoimet laskut on liitetty manuaalisesti puitetilaukseen syöttämällä puitetilauksen numero myyntilaskuriville.</span><span class="sxs-lookup"><span data-stu-id="f5949-165">Open invoices are manually associated with a blanket order by entering the blanket order number on the sales invoice line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f5949-166">**Palautustilaukset**</span><span class="sxs-lookup"><span data-stu-id="f5949-166">**Return Orders**</span></span></td>
    <td><span data-ttu-id="f5949-167">Määrittää avoimet palautustilaukset, jotka on merkitty liittyviksi valittuun riviin.</span><span class="sxs-lookup"><span data-stu-id="f5949-167">Specifies open return orders that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f5949-168">**Hyvityslaskut**</span><span class="sxs-lookup"><span data-stu-id="f5949-168">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="f5949-169">Määrittää avoimet hyvityslaskut, jotka on merkitty liittyviksi valittuun riviin.</span><span class="sxs-lookup"><span data-stu-id="f5949-169">Specifies open credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="f5949-170">
4. Näytä kirjatut tapahtumat valitsemalla ensin kyseinen rivi, sitten **Rivi**-toiminto ja lopuksi **Kirjatut rivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f5949-170">
4. To view posted entries, select the line in question, choose the **Line** action, and then choose the **Posted Lines** action.</span></span> <span data-ttu-id="f5949-171">Valitse yksi seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="f5949-171">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="f5949-172">Asetus</span><span class="sxs-lookup"><span data-stu-id="f5949-172">Option</span></span></th>
    <th><span data-ttu-id="f5949-173">Description</span><span class="sxs-lookup"><span data-stu-id="f5949-173">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="f5949-174">**Toimitukset**</span><span class="sxs-lookup"><span data-stu-id="f5949-174">**Shipments**</span></span></td>
    <td><span data-ttu-id="f5949-175">Valittuun riviin liitetyt kirjatut toimitukset.</span><span class="sxs-lookup"><span data-stu-id="f5949-175">Posted shipments associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f5949-176">**Laskut**</span><span class="sxs-lookup"><span data-stu-id="f5949-176">**Invoices**</span></span></td>
    <td><span data-ttu-id="f5949-177">Valittuun riviin liitetyt kirjatut laskut.</span><span class="sxs-lookup"><span data-stu-id="f5949-177">Posted invoices associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f5949-178">**Palautusvast.otot**</span><span class="sxs-lookup"><span data-stu-id="f5949-178">**Return Receipts**</span></span></td>
    <td><span data-ttu-id="f5949-179">Valittuun riviin liitetyt kirjatut palautusvastaanotot.</span><span class="sxs-lookup"><span data-stu-id="f5949-179">Posted return receipts that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f5949-180">**Hyvityslaskut**</span><span class="sxs-lookup"><span data-stu-id="f5949-180">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="f5949-181">Valittuun riviin liitetyt kirjatut hyvityslaskut.</span><span class="sxs-lookup"><span data-stu-id="f5949-181">Posted credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="f5949-182">
5. Näytä tapahtuma valitsemalla **Näytä asiakirja** -toiminto **Myyntirivit**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="f5949-182">
5. In the **Sales Lines** window, choose the **Show Document** action to view the entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5949-183">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f5949-183">See Also</span></span>
[<span data-ttu-id="f5949-184">Myynti</span><span class="sxs-lookup"><span data-stu-id="f5949-184">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="f5949-185">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f5949-185">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="f5949-186">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f5949-186">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

