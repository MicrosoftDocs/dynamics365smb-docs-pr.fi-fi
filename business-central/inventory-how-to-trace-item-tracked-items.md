---
title: Nimikeseurannan nimikkeiden jäljittäminen
description: Näet, missä nimikeseurannassa olevaa nimikettä on käytetty, mukaan lukien kuinka ja missö se oli vastaanotettu tai tuotettu, siirretty, myyty, kulutettu tai palautettu. Voit myös etsiä kaikki nykyiset esiintymät tietystä sarja- tai eränumerosta tietokannassa. Voit tehdä tämän käyttämällä nimikkeen jäljitystä ja tapahtumien etsintätoimintoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbfe0237beb58f22d3be7bc388d7b2726f05d4ba
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214751"
---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="84559-105">Nimikeseurannan nimikkeiden jäljittäminen</span><span class="sxs-lookup"><span data-stu-id="84559-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="84559-106">Näet, missä nimikeseurannassa olevaa nimikettä on käytetty, mukaan lukien kuinka ja missä se oli vastaanotettu tai tuotettu, siirretty, myyty, kulutettu tai palautettu.</span><span class="sxs-lookup"><span data-stu-id="84559-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="84559-107">Voit myös etsiä kaikki nykyiset esiintymät tietystä sarja- tai eränumerosta tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="84559-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="84559-108">Voit tehdä tämän käyttämällä nimikkeen jäljitystä ja [Etsi tapahtumat](ui-find-entries.md) -toimintoja.</span><span class="sxs-lookup"><span data-stu-id="84559-108">You do this by using the Item Tracing and the [Find Entries](ui-find-entries.md) features.</span></span>  

<span data-ttu-id="84559-109">Nämä toiminnot ovat erityisen hyödyllisiä laaduntarkkailussa, kun haluat tietää, kuka asiakas vastaanotti tietyllä eränumerolla olevia tuotteita tai mihin erään viallinen komponentti kuuluu.</span><span class="sxs-lookup"><span data-stu-id="84559-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="84559-110">Voit jäljittää **Nimikkeen jäljitys** -sivulla sarja- tai eränumeron järjestyksessä eteenpäin ja taaksepäin kirjatuissa varastotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="84559-110">On the **Item Tracing** page, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="84559-111">**Etsi tapahtumat** -sivulla ei näy tapahtumien järjestystä, mutta näet kuitenkin sarja- tai eränumeron kaikki tietueet – sekä kirjatut tapahtumat että avatut tietueet.</span><span class="sxs-lookup"><span data-stu-id="84559-111">On the **Find Entries** page, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="84559-112">Kahta ominaisuutta voi käyttää yhdessä siirtämällä jäljitetty sarja- tai eränumero **Etsi tapahtumat** -sivulle viimeistelemään jäljitystilanne.</span><span class="sxs-lookup"><span data-stu-id="84559-112">The two features can be used in combination by transferring a traced serial or lot number to the **Find Entries** page to finish a complete trace scenario.</span></span> <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="84559-113">Nimikeseurannan nimikkeiden jäljittäminen</span><span class="sxs-lookup"><span data-stu-id="84559-113">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="84559-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeen jäljitys** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="84559-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="84559-115">Anna sivun yläosan suodatinkenttiin tietyt nimikenumerot tai niiden nimikenumeroiden suodatin, joita haluat jäljittää.</span><span class="sxs-lookup"><span data-stu-id="84559-115">In the filter fields at the top of the page, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="84559-116">Valitse **Näytä komponentit** -kentässä, haluatko tarkastaa myös sen, mistä nimikkeiden komponentit ovat lähtöisin.</span><span class="sxs-lookup"><span data-stu-id="84559-116">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="84559-117">Vaihtoehtosi tässä kentässä ovat seuraavat.</span><span class="sxs-lookup"><span data-stu-id="84559-117">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="84559-118">Kenttä</span><span class="sxs-lookup"><span data-stu-id="84559-118">Field</span></span>|<span data-ttu-id="84559-119">Description</span><span class="sxs-lookup"><span data-stu-id="84559-119">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="84559-120">**Nro**</span><span class="sxs-lookup"><span data-stu-id="84559-120">**No**</span></span>|<span data-ttu-id="84559-121">Valitse tämä vaihtoehto, jos et halua tarkastella komponentteja.</span><span class="sxs-lookup"><span data-stu-id="84559-121">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="84559-122">**Vain nimikeseuranta**</span><span class="sxs-lookup"><span data-stu-id="84559-122">**Item-tracked Only**</span></span>|<span data-ttu-id="84559-123">Valitse tämä vaihtoehto, jos haluat tarkastella vain niitä komponentteja, joilla on erä- tai sarjanumeroita.</span><span class="sxs-lookup"><span data-stu-id="84559-123">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="84559-124">**Kaikki**</span><span class="sxs-lookup"><span data-stu-id="84559-124">**All**</span></span>|<span data-ttu-id="84559-125">Valitse tämä vaihtoehto, jos haluat tarkastella kaikkia komponentteja.</span><span class="sxs-lookup"><span data-stu-id="84559-125">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="84559-126">Valitse **Jäljitysmenetelmä**-kentässä menetelmä, jota haluat ohjelman käyttävän nimikkeen jäljityksessä.</span><span class="sxs-lookup"><span data-stu-id="84559-126">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="84559-127">Käytettävissä ovat seuraavat vaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="84559-127">The options are as follows</span></span>  

    |<span data-ttu-id="84559-128">Kenttä</span><span class="sxs-lookup"><span data-stu-id="84559-128">Field</span></span>|<span data-ttu-id="84559-129">Description</span><span class="sxs-lookup"><span data-stu-id="84559-129">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="84559-130">**Käyttö->alkuperä**</span><span class="sxs-lookup"><span data-stu-id="84559-130">**Usage->Origin**</span></span>|<span data-ttu-id="84559-131">Tämä menetelmä jäljittää nimikettä lähtien siitä paikasta, josta sitä käytettiin, siihen paikkaan, josta se tuli.</span><span class="sxs-lookup"><span data-stu-id="84559-131">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="84559-132">Jos esimerkiksi valmistettu nimike myytiin asiakkaalle, **Nimikkeen jäljitys** -sivulla näkyvät nämä tiedot niin, että lähtevän toimituksen rivi on ensimmäisenä. Voit laajentaa näkymää, jos haluat nähdä, mistä tuotantotilauksesta se tuli.</span><span class="sxs-lookup"><span data-stu-id="84559-132">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="84559-133">**Alkuperä-> Käyttö**</span><span class="sxs-lookup"><span data-stu-id="84559-133">**Origin->Usage**</span></span>|<span data-ttu-id="84559-134">Tämä menetelmä jäljittää nimikettä lähtien siitä paikasta, josta se tuli varastoon, siihen paikkaan, jossa sitä käytettiin.</span><span class="sxs-lookup"><span data-stu-id="84559-134">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="84559-135">Jos esimerkiksi valmistettu nimike myytiin asiakkaalle, **Nimikkeen jäljitys** -sivulla näkyvät nämä tiedot niin, että valmis tuotantotilaus on ensimmäisenä. Voit laajentaa näkymää, jos haluat nähdä ne lähtevän toimituksen rivit, joissa nimikettä käytettiin.</span><span class="sxs-lookup"><span data-stu-id="84559-135">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="84559-136">Suorita jäljitys valitsemalla **Jäljitys**.</span><span class="sxs-lookup"><span data-stu-id="84559-136">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="84559-137">Jos olet vastaanottanut saman erän useissa tapahtumissa, kaikki tapahtumat eivät ehkä näy **Nimikkeen jäljitys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="84559-137">If you have received the same lot on more transactions, then the **Item Tracing** page may not show all transactions.</span></span> <span data-ttu-id="84559-138">Näytetään vain kohdistetut tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="84559-138">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="84559-139">Jos jäljitysrivin yläpuolinen rivi on jo jäljittänyt lisätapahtumahistorian, **Jo jäljitetty** -valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="84559-139">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="84559-140">Yksinkertaisemman näkymän tarjoavia alla olevia rivejä ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="84559-140">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="84559-141">Etsi kohteen jäljitysrivejä, joissa tapahtumahistoria on jo jäljitetty, ja valitse **Siirry jo jäljitetty** -painike.</span><span class="sxs-lookup"><span data-stu-id="84559-141">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="84559-142">Nimikkeen jäljitysrivi on valittu, ja kaikki pohjana olevat rivit on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="84559-142">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-find-entries"></a><span data-ttu-id="84559-143">Voit etsiä nimikeseurannassa olevia nimikkeitä Etsi tapahtumat -toiminnolla</span><span class="sxs-lookup"><span data-stu-id="84559-143">To find item-tracked items with Find Entries</span></span>  

1. <span data-ttu-id="84559-144">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Etsi tapahtumat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="84559-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then select the related link.</span></span>  
2. <span data-ttu-id="84559-145">Valitse **Toiminnot** > **Etsi perusteella** > **Nimike viittauksen mukaan**.</span><span class="sxs-lookup"><span data-stu-id="84559-145">Choose **Actions** > **Find by** > **Find by Item Reference**.</span></span>
3. <span data-ttu-id="84559-146">Anna **Sarjanumero**- ja **Eränro**-kenttiin nimikeseurantanumerot, joita haluat seurata.</span><span class="sxs-lookup"><span data-stu-id="84559-146">In the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
4. <span data-ttu-id="84559-147">Etsi kaikki sarja- tai eränumeron ilmentymät tietokannasta valitsemalla **Etsi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="84559-147">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="84559-148">Katso myös</span><span class="sxs-lookup"><span data-stu-id="84559-148">See Also</span></span>

[<span data-ttu-id="84559-149">Varasto</span><span class="sxs-lookup"><span data-stu-id="84559-149">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="84559-150">Sarja-, erä- ja pakettinumeroiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="84559-150">Work with Serial, Lot, and Package Numbers</span></span>](inventory-how-work-item-tracking.md)  
[<span data-ttu-id="84559-151">Rakennetiedot: Nimikkeen seuranta</span><span class="sxs-lookup"><span data-stu-id="84559-151">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="84559-152">Rakennetiedot – nimikkeen seuranta ja varaukset</span><span class="sxs-lookup"><span data-stu-id="84559-152">Design Details - Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="84559-153">Nimikkeiden varaaminen</span><span class="sxs-lookup"><span data-stu-id="84559-153">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="84559-154">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="84559-154">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[<span data-ttu-id="84559-155">Etsi tapahtumat</span><span class="sxs-lookup"><span data-stu-id="84559-155">Find Entries</span></span>](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]