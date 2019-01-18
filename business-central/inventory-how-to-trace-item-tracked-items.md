---
title: "Nimikeseurannan nimikkeiden jäljittäminen | Microsoft Docs"
description: "Näet, missä nimikeseurannassa olevaa nimikettä on käytetty, mukaan lukien kuinka ja missö se oli vastaanotettu tai tuotettu, siirretty, myyty, kulutettu tai palautettu. Voit myös etsiä kaikki nykyiset esiintymät tietystä sarja- tai eränumerosta tietokannassa. Voit tehdä tämän käyttämällä nimikkeen jäljitystä ja Navigoi-toimintoja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: bf16f61e5c3d6ee6af045ded8ec80e426ae6c20a
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="09e8d-105">Nimikeseurannan nimikkeiden jäljittäminen</span><span class="sxs-lookup"><span data-stu-id="09e8d-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="09e8d-106">Näet, missä nimikeseurannassa olevaa nimikettä on käytetty, mukaan lukien kuinka ja missö se oli vastaanotettu tai tuotettu, siirretty, myyty, kulutettu tai palautettu.</span><span class="sxs-lookup"><span data-stu-id="09e8d-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="09e8d-107">Voit myös etsiä kaikki nykyiset esiintymät tietystä sarja- tai eränumerosta tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="09e8d-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="09e8d-108">Voit tehdä tämän käyttämällä nimikkeen jäljitystä ja Navigoi-toimintoja.</span><span class="sxs-lookup"><span data-stu-id="09e8d-108">You do this by using the Item Tracing and the Navigate features.</span></span>  

 <span data-ttu-id="09e8d-109">Nämä toiminnot ovat erityisen hyödyllisiä laaduntarkkailussa, kun haluat tietää, kuka asiakas vastaanotti tietyllä eränumerolla olevia tuotteita tai mihin erään viallinen komponentti kuuluu.</span><span class="sxs-lookup"><span data-stu-id="09e8d-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="09e8d-110">Voit jäljittää **Nimikkeen jäljitys** -sivulla sarja- tai eränumeron järjestyksessä eteenpäin ja taaksepäin kirjatuissa varastotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="09e8d-110">On the **Item Tracing** page, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="09e8d-111">**Navigoi**-sivulla ei näy tapahtumien järjestystä, mutta näet kuitenkin sarja- tai eränumeron kaikki tietueet – sekä kirjatut tapahtumat että avatut tietueet.</span><span class="sxs-lookup"><span data-stu-id="09e8d-111">On the **Navigate** page, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="09e8d-112">Kahta ominaisuutta voi käyttää yhdessä siirtämällä jäljitetty sarja- tai eränumero **Navigoi**-sivulle viimeistelemään jäljitystilanne.</span><span class="sxs-lookup"><span data-stu-id="09e8d-112">The two features can be used in combination by transferring a traced serial or lot number to the **Navigate** page to finish a complete trace scenario.</span></span> <span data-ttu-id="09e8d-113">Lisätietoja on kohdassa [Vaihekuvaus: Sarja- ja eränumeroiden jäljitys](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="09e8d-113">For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>  

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="09e8d-114">Nimikeseurannan nimikkeiden jäljittäminen</span><span class="sxs-lookup"><span data-stu-id="09e8d-114">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="09e8d-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen jäljitys** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="09e8d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="09e8d-116">Anna sivun yläosan suodatinkenttiin tietyt nimikenumerot tai niiden nimikenumeroiden suodatin, joita haluat jäljittää.</span><span class="sxs-lookup"><span data-stu-id="09e8d-116">In the filter fields at the top of the page, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="09e8d-117">Valitse **Näytä komponentit** -kentässä, haluatko tarkastaa myös sen, mistä nimikkeiden komponentit ovat lähtöisin.</span><span class="sxs-lookup"><span data-stu-id="09e8d-117">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="09e8d-118">Vaihtoehtosi tässä kentässä ovat seuraavat.</span><span class="sxs-lookup"><span data-stu-id="09e8d-118">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="09e8d-119">Kenttä</span><span class="sxs-lookup"><span data-stu-id="09e8d-119">Field</span></span>|<span data-ttu-id="09e8d-120">Description</span><span class="sxs-lookup"><span data-stu-id="09e8d-120">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="09e8d-121">**Nro**</span><span class="sxs-lookup"><span data-stu-id="09e8d-121">**No**</span></span>|<span data-ttu-id="09e8d-122">Valitse tämä vaihtoehto, jos et halua tarkastella komponentteja.</span><span class="sxs-lookup"><span data-stu-id="09e8d-122">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="09e8d-123">**Vain nimikeseuranta**</span><span class="sxs-lookup"><span data-stu-id="09e8d-123">**Item-tracked Only**</span></span>|<span data-ttu-id="09e8d-124">Valitse tämä vaihtoehto, jos haluat tarkastella vain niitä komponentteja, joilla on erä- tai sarjanumeroita.</span><span class="sxs-lookup"><span data-stu-id="09e8d-124">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="09e8d-125">**Kaikki**</span><span class="sxs-lookup"><span data-stu-id="09e8d-125">**All**</span></span>|<span data-ttu-id="09e8d-126">Valitse tämä vaihtoehto, jos haluat tarkastella kaikkia komponentteja.</span><span class="sxs-lookup"><span data-stu-id="09e8d-126">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="09e8d-127">Valitse **Jäljitysmenetelmä**-kentässä menetelmä, jota haluat ohjelman käyttävän nimikkeen jäljityksessä.</span><span class="sxs-lookup"><span data-stu-id="09e8d-127">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="09e8d-128">Käytettävissä ovat seuraavat vaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="09e8d-128">The options are as follows</span></span>  

    |<span data-ttu-id="09e8d-129">Kenttä</span><span class="sxs-lookup"><span data-stu-id="09e8d-129">Field</span></span>|<span data-ttu-id="09e8d-130">Description</span><span class="sxs-lookup"><span data-stu-id="09e8d-130">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="09e8d-131">**Käyttö->alkuperä**</span><span class="sxs-lookup"><span data-stu-id="09e8d-131">**Usage->Origin**</span></span>|<span data-ttu-id="09e8d-132">Tämä menetelmä jäljittää nimikettä lähtien siitä paikasta, josta sitä käytettiin, siihen paikkaan, josta se tuli.</span><span class="sxs-lookup"><span data-stu-id="09e8d-132">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="09e8d-133">Jos esimerkiksi valmistettu nimike myytiin asiakkaalle, **Nimikkeen jäljitys** -sivulla näkyvät nämä tiedot niin, että lähtevän toimituksen rivi on ensimmäisenä. Voit laajentaa näkymää, jos haluat nähdä, mistä tuotantotilauksesta se tuli.</span><span class="sxs-lookup"><span data-stu-id="09e8d-133">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="09e8d-134">**Alkuperä-> Käyttö**</span><span class="sxs-lookup"><span data-stu-id="09e8d-134">**Origin->Usage**</span></span>|<span data-ttu-id="09e8d-135">Tämä menetelmä jäljittää nimikettä lähtien siitä paikasta, josta se tuli varastoon, siihen paikkaan, jossa sitä käytettiin.</span><span class="sxs-lookup"><span data-stu-id="09e8d-135">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="09e8d-136">Jos esimerkiksi valmistettu nimike myytiin asiakkaalle, **Nimikkeen jäljitys** -sivulla näkyvät nämä tiedot niin, että valmis tuotantotilaus on ensimmäisenä. Voit laajentaa näkymää, jos haluat nähdä ne lähtevän toimituksen rivit, joissa nimikettä käytettiin.</span><span class="sxs-lookup"><span data-stu-id="09e8d-136">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="09e8d-137">Suorita jäljitys valitsemalla **Jäljitys**.</span><span class="sxs-lookup"><span data-stu-id="09e8d-137">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="09e8d-138">Jos olet vastaanottanut saman erän useissa tapahtumissa, kaikki tapahtumat eivät ehkä näy **Nimikkeen jäljitys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="09e8d-138">If you have received the same lot on more transactions, then the **Item Tracing** page may not show all transactions.</span></span> <span data-ttu-id="09e8d-139">Näytetään vain kohdistetut tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="09e8d-139">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="09e8d-140">Jos jäljitysrivin yläpuolinen rivi on jo jäljittänyt lisätapahtumahistorian, **Jo jäljitetty** -valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="09e8d-140">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="09e8d-141">Yksinkertaisemman näkymän tarjoavia alla olevia rivejä ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="09e8d-141">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="09e8d-142">Etsi kohteen jäljitysrivejä, joissa tapahtumahistoria on jo jäljitetty, ja valitse **Siirry jo jäljitetty** -painike.</span><span class="sxs-lookup"><span data-stu-id="09e8d-142">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="09e8d-143">Nimikkeen jäljitysrivi on valittu, ja kaikki pohjana olevat rivit on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="09e8d-143">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-navigate"></a><span data-ttu-id="09e8d-144">Voit etsiä nimikeseurannassa olevia nimikkeitä Navigoi-toiminnolla</span><span class="sxs-lookup"><span data-stu-id="09e8d-144">To find item-tracked items with Navigate</span></span>  

1.  <span data-ttu-id="09e8d-145">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Navigoi** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="09e8d-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Navigate**, and then select the related link.</span></span>  
2.  <span data-ttu-id="09e8d-146">Anna **Nimikeseuranta**-pikavälilehden **Sarjanumero**- ja **Eränro**-kenttiin nimikeseurantanumerot, joita haluat seurata.</span><span class="sxs-lookup"><span data-stu-id="09e8d-146">On the **Item Tracking** FastTab, in the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
3.  <span data-ttu-id="09e8d-147">Etsi kaikki sarja- tai eränumeron ilmentymät tietokannasta valitsemalla **Etsi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="09e8d-147">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09e8d-148">Katso myös</span><span class="sxs-lookup"><span data-stu-id="09e8d-148">See Also</span></span>  
[<span data-ttu-id="09e8d-149">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="09e8d-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="09e8d-150">[Rakennetiedot: Nimikkeen seuranta](design-details-item-tracking.md)
[Rakennetiedot: Nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md)</span><span class="sxs-lookup"><span data-stu-id="09e8d-150">[Design Details: Item Tracking](design-details-item-tracking.md)
[Design Details - Item Tracking and Reservations](design-details-item-tracking-and-reservations.md)</span></span>  
[<span data-ttu-id="09e8d-151">Nimikkeiden varaaminen</span><span class="sxs-lookup"><span data-stu-id="09e8d-151">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="09e8d-152">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)
[Vaihekuvaus: Sarja- ja eränumeroiden jäljitys](walkthrough-tracing-serial-lot-numbers.md)</span><span class="sxs-lookup"><span data-stu-id="09e8d-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)</span></span>

