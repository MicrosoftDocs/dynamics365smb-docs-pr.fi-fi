---
title: "Vaihekuvaus – Toimitusten manuaalinen suunnittelu | Microsoft Docs"
description: "Tässä vaihekuvauksessa kuvataan toimitustilausten suunnitteluprosessi uuden kysynnän täyttämiseksi. Voit aloittaa tarjonnan suunnittelun tietyin välein, esimerkiksi joka aamu tai joka maanantai, tai kun myynti tai tuotanto ilmoittaa ne kysyntätyypin mukaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: de00ca393b5d2c28292ae3deba743ce3447b6145
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="d374e-104">Vaihekuvaus: Toimitusten manuaalinen suunnittelu</span><span class="sxs-lookup"><span data-stu-id="d374e-104">Walkthrough: Planning Supplies Manually</span></span>
<span data-ttu-id="d374e-105">Tässä vaihekuvauksessa käsitellään toimitustilausten suunnitteluprosessia uuden kysynnän täyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="d374e-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="d374e-106">Voit aloittaa tarjonnan suunnittelun tietyin välein, esimerkiksi joka aamu tai joka maanantai, tai kun myynti tai tuotanto ilmoittaa ne kysyntätyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="d374e-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="d374e-107">Tässä vaihekuvauksessa käytetään **Tilauksen suunnittelu** -ikkunaa. Se on yksinkertainen toimitusten suunnittelutyökalu, joka perustuu parametripohjaisen automaattisen suunnittelun asemesta manuaaliseen päätöksentekoon.</span><span class="sxs-lookup"><span data-stu-id="d374e-107">In this walkthrough you will use the **Order Planning** window, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="d374e-108">Tietoja tästä vaihekuvauksesta</span><span class="sxs-lookup"><span data-stu-id="d374e-108">About This Walkthrough</span></span>  
 <span data-ttu-id="d374e-109">Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="d374e-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="d374e-110">ostotilauksen suunnitteleminen valmistuskomponentteja varten</span><span class="sxs-lookup"><span data-stu-id="d374e-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="d374e-111">myyntikysynnän täyttäminen siirtotilauksia suunnittelemalla</span><span class="sxs-lookup"><span data-stu-id="d374e-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="d374e-112">monitasoisen nimikkeen tuotantotilauksen suunnitteleminen.</span><span class="sxs-lookup"><span data-stu-id="d374e-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="d374e-113">Roolit</span><span class="sxs-lookup"><span data-stu-id="d374e-113">Roles</span></span>  
 <span data-ttu-id="d374e-114">Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="d374e-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="d374e-115">Tuotantosuunnittelija</span><span class="sxs-lookup"><span data-stu-id="d374e-115">Production Planner</span></span>  
-   <span data-ttu-id="d374e-116">Ostaja</span><span class="sxs-lookup"><span data-stu-id="d374e-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="d374e-117">myyntitilausten käsittelijä</span><span class="sxs-lookup"><span data-stu-id="d374e-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="d374e-118">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="d374e-118">Prerequisites</span></span>  
 <span data-ttu-id="d374e-119">Ennen kuin aloitat tämän vaihekohtaisen ohjeen, sinun on asennettava [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d374e-119">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d374e-120">Tietokantaan on tehtävä seuraavat muutokset:</span><span class="sxs-lookup"><span data-stu-id="d374e-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="d374e-121">Poista kaikki aiemmat polkupyörien myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="d374e-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="d374e-122">Luo kymmenelle polkupyörälle yksi myyntitilaus SININEN-sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="d374e-122">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="d374e-123">Poista kaikki suunnitellut ja sitovasti suunnitellut tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="d374e-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="d374e-124">Älä poista aloitettuja tilauksia, joissa on aiemmin kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="d374e-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="d374e-125">Tässä vaihekuvauksessa kannattaa käyttää ehdotettuja tietoja, koska näissä tiedoissa on tarvittavat tietueet.</span><span class="sxs-lookup"><span data-stu-id="d374e-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="d374e-126">Taustatietoja</span><span class="sxs-lookup"><span data-stu-id="d374e-126">Story</span></span>  
 <span data-ttu-id="d374e-127">Pienen teollisuusyhtiön tuotantosuunnittelija Karl aikoo suunnitella tuotanto- ja ostotilaukset uuden myyntikysynnän täyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="d374e-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="d374e-128">Koska tuotteissa ei ole useaa tuoterakennetasoa eikä tilauksia ole paljon, Karl luo toimitustilaukset manuaalisesti **Tilauksen suunnittelu** -ikkunassa yksi tuotetaso kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="d374e-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** window to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="d374e-129">Monimutkaisemmissa tuotantoympäristöissä suunnittelutyökirjaa käytetään toimitusten suunnitteluun, joka perustuu nimikeparametreihin, kuten uudelleenajoitusjaksoon, toimitusajan varmistukseen ja uusintatilauspisteeseen, sekä kaikkien tuotetasojen yhdistetyn kysynnän erälaskentaan.</span><span class="sxs-lookup"><span data-stu-id="d374e-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="d374e-130">Esimerkkitietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d374e-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="d374e-131">Tavallisessa CRONUS-esimerkkiyrityksessä on tällä hetkellä paljon suunnittelematonta kysyntää.</span><span class="sxs-lookup"><span data-stu-id="d374e-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="d374e-132">Tämän vaihekuvauksen suunnittelutehtävien aikana realistisesta liiketoimintojen työnkulusta täytyy poiketa. Siitä poiketaan jättämällä huomiotta kysyntä, jonka eräpäivät ovat lähellä, ja käyttämällä sen sijaan kysyntää, jonka eräpäivät ovat myöhäisempiä.</span><span class="sxs-lookup"><span data-stu-id="d374e-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-window"></a><span data-ttu-id="d374e-133">Tilauksen suunnittelu -ikkunan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="d374e-133">Using the Order Planning Window</span></span>  
 <span data-ttu-id="d374e-134">**Tilauksen suunnittelu** -ikkunaa voi käyttää siirtymisruudun **Osastot**-valikosta useasta eri sijainnista:</span><span class="sxs-lookup"><span data-stu-id="d374e-134">The **Order Planning** window can be accessed from several different locations on the **Departments** menu in the navigation pane:</span></span>  

-   <span data-ttu-id="d374e-135">Tuotanto, Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="d374e-135">Manufacturing, Planning</span></span>  
-   <span data-ttu-id="d374e-136">Myynti ja markkinointi, Tilauksen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="d374e-136">Sales & Marketing, Order Processing</span></span>  
-   <span data-ttu-id="d374e-137">Osto, Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="d374e-137">Purchase, Planning</span></span>  
-   <span data-ttu-id="d374e-138">Lisäksi voit avata tämän tietyn tuotantotilauksen ikkunan valitsemalla **Suunnittelu**-kohdan **Navigoi**-välilehdessä **Tilaus**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="d374e-138">In addition, you can open this window for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.</span></span>  

### <a name="to-use-the-order-planning-window"></a><span data-ttu-id="d374e-139">Tilauksen suunnittelu -ikkunan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="d374e-139">To use the Order Planning window</span></span>  

1.  <span data-ttu-id="d374e-140">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tilauksen suunnittelu** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d374e-140">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="d374e-141">Kun **Tilauksen suunnittelu** -ikkuna aukeaa, suunnitelma on laskettava, jotta uusi, edellisen laskennan jälkeinen kysyntä tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="d374e-141">When the **Order Planning** window first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="d374e-142">Valitse **Laske suunnitelma** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-142">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="d374e-143">Suunnittelujärjestelmä analysoi mahdollisen uuden kysynnän, kuten uuden myynnin, muuttuneen myynnin tai tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="d374e-143">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="d374e-144">Kunkin kysyntärivin tarvittu määrä lasketaan kokonaissaatavuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="d374e-144">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="d374e-145">Nämä laskelmat tehdään tilauskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="d374e-145">This calculation is performed order-by-order.</span></span> <span data-ttu-id="d374e-146">Toisin sanoin ensin lasketaan kysyntärivin sisältävä tilaus, jolla on varhaisin eräpäivä tai lähetyksen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d374e-146">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="d374e-147">Tämän jälkeen muut kysyntärivit lasketaan samassa järjestyksessä eräpäivästä ja lähetyksen päivämäärästä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="d374e-147">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="d374e-148">Varmista, että **Tilauksen suunnittelu** -ikkuna on suurennettu ja että sarakkeen kenttien kokoa on muutettu siten, että kaikki oletuskenttänimet näkyvät.</span><span class="sxs-lookup"><span data-stu-id="d374e-148">Be sure that the **Order Planning** window is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="d374e-149">Kun laskutoimitukset on suoritettu, täyttämätön kysyntä näkyy ikkunassa supistettuina tilauksen otsikkoriveinä, jotka on lajiteltu varhaisimman mahdollisen kysyntäpäivämäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="d374e-149">When the calculation is completed, the window displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="d374e-150">Huomaa, että CRONUSilla on useita tilauksia, joissa on täyttämätöntä kysyntää.</span><span class="sxs-lookup"><span data-stu-id="d374e-150">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="d374e-151">Jokainen lihavoitu suunnittelurivi vastaa tilausta &mdash; myyntitilausta tai tuotantotilausta &mdash; ja mukana on vähintään yksi tilausrivi, jossa saatavuus on riittämätön.</span><span class="sxs-lookup"><span data-stu-id="d374e-151">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="d374e-152">Valitse **Näytä kysyntä muodossa** -kentän **Kaikki kysyntä** -suodatin.</span><span class="sxs-lookup"><span data-stu-id="d374e-152">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="d374e-153">**Kysyntätyyppi**-kentän avulla voit valita, mitkä tilaustyypit on tarkoitus tuoda näkyviin.</span><span class="sxs-lookup"><span data-stu-id="d374e-153">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="d374e-154">Tilaukset, joissa ei ole saatavuusongelmia, eivät näy.</span><span class="sxs-lookup"><span data-stu-id="d374e-154">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="d374e-155">Jos suunnitelman laskemisen jälkeen ei ole tilauksia, näyttöön tulee sanoma, mutta ei suunnittelurivejä.</span><span class="sxs-lookup"><span data-stu-id="d374e-155">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="d374e-156">Ostotilauksen suunnitteleminen komponenttien kysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="d374e-156">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="d374e-157">Näissä toimintaohjeissa luodaan ostotilaus tarvittavia valmistuskomponentteja varten.</span><span class="sxs-lookup"><span data-stu-id="d374e-157">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="d374e-158">Ostotilauksen suunnitteleminen täyttämään tuotannon komponenttitarve</span><span class="sxs-lookup"><span data-stu-id="d374e-158">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="d374e-159">Laajenna ensimmäinen rivi (napsauta plusmerkkiä).</span><span class="sxs-lookup"><span data-stu-id="d374e-159">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="d374e-160">Valitse ensimmäinen kysyntärivi, jossa on nimike **LSU-15**, ja valitse sitten **Näytä asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-160">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="d374e-161">Siirry takaisin **Tilauksen suunnittelu** -ikkunaan sulkemalla avattu tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="d374e-161">Close the opened production order to return to the **Order Planning** window.</span></span>  
4.  <span data-ttu-id="d374e-162">Valitse **Täydennysjärjestelmä**-kentässä **Osto**.</span><span class="sxs-lookup"><span data-stu-id="d374e-162">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="d374e-163">Oletusarvo on nimikkeen kortti (tai varastoyksikön kortti), mutta sen voi vaihtaa yhdeksi kolmesta vaihtoehdosta:</span><span class="sxs-lookup"><span data-stu-id="d374e-163">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="d374e-164">**Osto** – luodaan ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="d374e-164">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="d374e-165">**Siirto** – Siirtotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="d374e-165">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="d374e-166">**Tuot.til.** – luodaan tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="d374e-166">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="d374e-167">Valitse **Tarjonta kohteesta** -kentässä jokin seuraavista vaihtoehdoista valitun täydennysjärjestelmän mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d374e-167">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="d374e-168">**Toimittaja** – ostoille</span><span class="sxs-lookup"><span data-stu-id="d374e-168">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="d374e-169">**Sijainti** – Siirrot</span><span class="sxs-lookup"><span data-stu-id="d374e-169">**Location** – For transfers</span></span>  

     <span data-ttu-id="d374e-170">Jos kentän tietoja ei täytetä, näkyviin tulee virhesanoma toimitustilauksia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="d374e-170">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d374e-171">Jos komponenteille on määritetty toimittajan oletusnumero nimikkeen kortteihin, rivit on määritetty ennalta.</span><span class="sxs-lookup"><span data-stu-id="d374e-171">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="d374e-172">Valitse **Tarjonta kohteesta** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="d374e-172">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="d374e-173">Valitse **Nimikkeen toimittajaluettelo** -ikkunassa **Uusi**-toiminto ja valitse toimittaja **30000**.</span><span class="sxs-lookup"><span data-stu-id="d374e-173">In the **Item Vendor Catalogue** window, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="d374e-174">Valitse **OK**-painike palataksesi **Tilauksen suunnittelu** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="d374e-174">Choose the **OK** button to return to the **Order Planning** window.</span></span>  
9. <span data-ttu-id="d374e-175">Kopioi toimittajan numero **30000** tämän tuotantotilauksen kaiutinkomponenttien muihin riveihin.</span><span class="sxs-lookup"><span data-stu-id="d374e-175">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="d374e-176">Nyt voit luoda ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="d374e-176">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="d374e-177">Valitse **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-177">Choose the **Make Orders** action.</span></span> <span data-ttu-id="d374e-178">**Tee toimitustilaukset** -ikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="d374e-178">The **Make Supply Orders** window opens.</span></span>  
11. <span data-ttu-id="d374e-179">Valitse **Tee tilaukset** -kentän **Tilauksen suunnittelu** -pikavälilehdessä **Aktiivinen tilaus**.</span><span class="sxs-lookup"><span data-stu-id="d374e-179">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="d374e-180">Valitse **Vaihtoehdot**-pikavälilehden **Luo ostotilaus** -kentästä **Tee ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d374e-180">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="d374e-181">Luo ostotilaukset tilauksen kaikille komponenteille valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d374e-181">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="d374e-182">Ostotilaukset luodaan ja tallennetaan viimeisiksi tilauksiksi ostotilausten luetteloon.</span><span class="sxs-lookup"><span data-stu-id="d374e-182">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="d374e-183">Siirtotilauksen suunnitteleminen myyntikysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="d374e-183">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="d374e-184">Näissä toimintaohjeissa kysyntää varten laaditaan suunnitelma myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="d374e-184">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="d374e-185">Kysyntärivit vastaavat myyntirivejä, eivät komponenttirivejä, kuten tuotantokysynnässä.</span><span class="sxs-lookup"><span data-stu-id="d374e-185">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="d374e-186">Siirtotilauksen suunnitteleminen myyntikysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="d374e-186">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="d374e-187">Siirrä kohdistin tilauksen numero **2008** suunnitteluriville.</span><span class="sxs-lookup"><span data-stu-id="d374e-187">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="d374e-188">Laajenna rivi ja siirrä kohdistin kysyntäriville.</span><span class="sxs-lookup"><span data-stu-id="d374e-188">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="d374e-189">Myyntitilaus numero **2008** koskee kymmentä kaiutinta, joiden tyyppi on **LS-120** ja jotka on tilannut Vakuutusyhtiö Meri.</span><span class="sxs-lookup"><span data-stu-id="d374e-189">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="d374e-190">Näkyviin tulevat nimikkeen määritetty täydennysjärjestelmä ja oletustoimittaja.</span><span class="sxs-lookup"><span data-stu-id="d374e-190">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d374e-191">Ikkunan alaosassa on neljä tietokenttää.</span><span class="sxs-lookup"><span data-stu-id="d374e-191">At the bottom of the window, there are four information fields.</span></span> <span data-ttu-id="d374e-192">**Varhaisin mahdollinen päivämäärä** -kentässä näkyy, että tarvittavat kymmenen kappaletta tulevat saataville saapuvassa toimitustilauksessa yhdeksän päivää nykyisen eräpäivän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d374e-192">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="d374e-193">Jos tämä on asiakkaalle liian myöhäinen ajankohta, **Siirtoon saatavilla** -kentässä näkyy, että nimikettä on 13 kappaletta toisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="d374e-193">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="d374e-194">Tätä tavaraa varten on tarkoitus laatia suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="d374e-194">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="d374e-195">Avaa **Hae vaihtoehtoinen tarjonta** -ikkuna napsauttamalla **Siirtoon saatavilla** -kentän hakupainiketta.</span><span class="sxs-lookup"><span data-stu-id="d374e-195">Choose the **Available for Transfer** field to open the **Get Alternative Supply** window.</span></span>  
4.  <span data-ttu-id="d374e-196">Varaa kymmenen saatavilla olevaa nimikettä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d374e-196">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d374e-197">Siirto VIHREÄ-sijainnista on vaihdettu ehdotetun oston tilalle kysyntäriville.</span><span class="sxs-lookup"><span data-stu-id="d374e-197">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="d374e-198">**Tee tilaukset** -toiminto luo siirtotilauksen VIHREÄ-sijainnista vaadittuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="d374e-198">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="d374e-199">**Korvaavia olemassa** -kenttä toimii samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="d374e-199">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="d374e-200">Valitse **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-200">Choose the **Make Orders** action.</span></span> <span data-ttu-id="d374e-201">**Tee toimitustilaukset** -ikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="d374e-201">The **Make Supply Orders** window opens.</span></span>  
6.  <span data-ttu-id="d374e-202">Valitse **Tee tilaukset** -kentän **Tilauksen suunnittelu** -pikavälilehdessä **Aktiivinen tilaus**.</span><span class="sxs-lookup"><span data-stu-id="d374e-202">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="d374e-203">Valitse **Vaihtoehdot**-pikavälilehden **Luo siirtotilaus** -kentässä **Tee siirtotilaukset** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="d374e-203">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="d374e-204">Luo siirtotilaus myyntitilauksen toimittamista varten valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d374e-204">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="d374e-205">Siirtotilaus luodaan ja tallennetaan luetteloon avointen siirtotilausten luettelon viimeiseksi tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="d374e-205">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="d374e-206">Monitasoisen tuotantotilauksen suunnitteleminen myyntikysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="d374e-206">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="d374e-207">Näissä toimintaohjeissa laaditaan suunnitelma, jossa tuotetun nimikkeen myyntikysyntä täytetään usealla tuotetasolla. Jokainen taso luo riippuvaisen tuotantokysynnän.</span><span class="sxs-lookup"><span data-stu-id="d374e-207">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="d374e-208">Monitasoisen tuotannon suunnitteleminen myyntikysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="d374e-208">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="d374e-209">Valitse tilauksen numero **1001** suunnittelurivi, jolla on myyntikysyntää (se luotiin aiemmin vaihekuvauksen valmistavissa toimissa).</span><span class="sxs-lookup"><span data-stu-id="d374e-209">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="d374e-210">Tämä kysyntä on myyntirivi, mutta nimikkeelle on määritetty täydennysjärjestelmäksi **Tuotantotilaus**.</span><span class="sxs-lookup"><span data-stu-id="d374e-210">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="d374e-211">Lisää ylimääräinen kello kunkin polkupyörän komponenttitarpeeseen.</span><span class="sxs-lookup"><span data-stu-id="d374e-211">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="d374e-212">Avaa **Suunnittelu komponentit**-ikkuna valitsemalla **Komponentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-212">Choose the **Components** action to open the **Planning Components** window.</span></span>  
3.  <span data-ttu-id="d374e-213">Vaihda Kello-nimikkeen rivillä **Määrä per** -kentän arvo **1** arvoksi **2**.</span><span class="sxs-lookup"><span data-stu-id="d374e-213">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="d374e-214">Harkitse suunnitteluvaihtoehtoja **Tilauksen suunnittelu** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="d374e-214">In the **Order Planning** window, consider your planning alternatives.</span></span> <span data-ttu-id="d374e-215">Tässä tilanteessa vaihtoehtoisia toimitustapoja &mdash; siirtoa tai korvaavaa tai myöhempää toimitusta &mdash; ei ole.</span><span class="sxs-lookup"><span data-stu-id="d374e-215">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="d374e-216">Ehdotettu toimitustilaus, tuotantotilaus, on luotava.</span><span class="sxs-lookup"><span data-stu-id="d374e-216">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="d374e-217">Luo tuotantotilaus valitsemalla **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-217">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="d374e-218">Huomaa, että myyntitilauksen **1001** suunnitteluriviä ei enää ole **Tilauksen suunnittelu** -ikkunassa. Alustava myyntikysyntä on täytetty.</span><span class="sxs-lookup"><span data-stu-id="d374e-218">In the **Order Planning** window, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="d374e-219">Sulje **Tilauksen suunnittelu** -ikkuna.</span><span class="sxs-lookup"><span data-stu-id="d374e-219">Close the **Order Planning** window.</span></span>  

     <span data-ttu-id="d374e-220">Tässä vaiheessa kaikki suunnittelutehtävät voitaisiin jäädä suorittamaan tähän näkymään.</span><span class="sxs-lookup"><span data-stu-id="d374e-220">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="d374e-221">Nyt kuitenkin omaksutaan tuotantosuunnittelijan rooli, siirrytään äsken luotuun tuotantotilaukseen ja käytetään **Tilauksen suunnittelu** -ikkunaa.</span><span class="sxs-lookup"><span data-stu-id="d374e-221">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** window.</span></span>  

 <span data-ttu-id="d374e-222">Tuotantosuunnittelijan täytyy nyt suunnitella tietty tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="d374e-222">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="d374e-223">Tietyn tuotantotilauksen suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="d374e-223">To plan a specific production order</span></span>  

1.  <span data-ttu-id="d374e-224">Avaa tuotantotilaus **101001** (kymmenen polkupyörää), joka luotiin aiemmin **Tee tilaukset**-toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="d374e-224">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="d374e-225">Avaa **Tuot.til. komponentit** -ikkunassa ja varmista, että ylimääräinen kello näkyy tuotantotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="d374e-225">Open the **Prod. Order Components** window to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="d374e-226">Valitse **Suunnittelu**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-226">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="d374e-227">**Tilauksen suunnittelu** -ikkuna avautuu näkymään, joka on suodatetaan aina tiettyyn tuotannon kysyntään.</span><span class="sxs-lookup"><span data-stu-id="d374e-227">The **Order Planning** window opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="d374e-228">Myyntikysyntä ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="d374e-228">Sales demand is not displayed.</span></span> <span data-ttu-id="d374e-229">Suunnitelma on laskettava, ennen kuin lisäkysyntä tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="d374e-229">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="d374e-230">Valitse **Laske suunnitelma** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-230">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="d374e-231">Huomaa, että neljä uutta tuotantotilausta näkyy tilauksesta **101001** johdettuna suunnittelemattomana tuotantokysyntänä.</span><span class="sxs-lookup"><span data-stu-id="d374e-231">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="d374e-232">Uudet rivit vastaavat niiden alikokoonpanojen uutta tuotantokysyntää, joka täytyy luoda tilauksen tuottamista varten.</span><span class="sxs-lookup"><span data-stu-id="d374e-232">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="d374e-233">Valitse **Laajenna kaikki** -toiminto, jos haluat nähdä yleiskuvauksen tuotantotilausten koko tuotantokysynnästä.</span><span class="sxs-lookup"><span data-stu-id="d374e-233">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="d374e-234">Antaaksesi lisätietoja kysyntäriveistä, saatat haluta lisätä **Kysyntämäärä** ja **Käytettävissä oleva kysyntämäärä** -kenttiä näkymääsi.</span><span class="sxs-lookup"><span data-stu-id="d374e-234">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="d374e-235">Seuraavaksi kutakin komponenttia on toimitettava kymmenen kappaletta.</span><span class="sxs-lookup"><span data-stu-id="d374e-235">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="d374e-236">Huomaa, että neljällä kysyntärivillä on täydennysjärjestelmä Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="d374e-236">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="d374e-237">Nämä neljä osakokoonpanoa edustavat polkupyörän toista tuotantotasoa.</span><span class="sxs-lookup"><span data-stu-id="d374e-237">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="d374e-238">Oletustäydennysasetukset on täytetty valmiiksi, ja voit aloittaa tilausten tekemisen.</span><span class="sxs-lookup"><span data-stu-id="d374e-238">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="d374e-239">Valitse **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-239">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="d374e-240">Ennen kuin painat **OK**-painiketta, huomioi teksti **Tilauksen suunnittelu**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d374e-240">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="d374e-241">Tämä teksti on tärkeä, koska polkupyörän tuoterakenteessa tiedetään olevan joitakin tuotettuja komponentteja eli alikokoonpanoja, joilla voisi olla kysyntää, kun luot tämän tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="d374e-241">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="d374e-242">Valitse **Tee toimitustilaukset** -ikkunan **Tee tilaukset**-kentässä **Kaikki rivit** ja valitse sitten **OK**, jos haluat luoda tuotantotilaukset tilauksen toiselle tuotetasolle.</span><span class="sxs-lookup"><span data-stu-id="d374e-242">In the **Make Supply Order** window, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="d374e-243">Huomaa, että tuotantotilauksella 101001 ei enää ole ylätason tuotantokysyntää.</span><span class="sxs-lookup"><span data-stu-id="d374e-243">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="d374e-244">Se merkitsee, että alikokoonpanojen alustava tuotantokysyntä on otettu huomioon suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="d374e-244">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="d374e-245">Suunnitelma lasketaan uudelleen **Tilauksen suunnittelu** -ikkunassa, jotta polkupyörän rakenne voidaan suunnitella.</span><span class="sxs-lookup"><span data-stu-id="d374e-245">In the **Order Planning** window, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="d374e-246">Laske suunnitelma uudelleen upotetun ohjetekstin ohjeiden mukaisesti valitsemalla **Laske suunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="d374e-246">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="d374e-247">Kaksi uutta riviä vastaavat ylimääräistä tuotantokysyntää, joka on johdettu edellisissä vaiheissa suunnitelluista alikokoonpanoista.</span><span class="sxs-lookup"><span data-stu-id="d374e-247">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="d374e-248">Pyörän napojen toimittamiseksi ehdotetaan kahta tuotantotilausta, yhtä kymmenelle etupyörän navalle ja niin ikään yhtä kymmenelle takapyörän navalle.</span><span class="sxs-lookup"><span data-stu-id="d374e-248">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="d374e-249">Valitse **Laajenna kaikki** -toiminto, jos haluat nähdä yleiskuvauksen kahden tuotantotilauksen koko tuotantokysynnästä.</span><span class="sxs-lookup"><span data-stu-id="d374e-249">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="d374e-250">Ehdotettu toimitussuunnitelma osoittaa, että komponenteille luodaan yhteensä neljä ostotilausta.</span><span class="sxs-lookup"><span data-stu-id="d374e-250">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="d374e-251">Ehdotetut tilaukset päätetään tehdä.</span><span class="sxs-lookup"><span data-stu-id="d374e-251">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="d374e-252">Valitse **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-252">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="d374e-253">Valitse **Tee tilaukset** -kentässä **Kaikki rivit** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d374e-253">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="d374e-254">Tarkista, onko päänimikkeen eli polkupyörän (myydään myyntitilauksella 1001) tuotannolla lisäkysyntää.</span><span class="sxs-lookup"><span data-stu-id="d374e-254">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="d374e-255">Valitse **Laske suunnitelma** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d374e-255">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="d374e-256">Sanomassa ilmoitetaan, että kaikki vaaditut nimikkeet on nyt toimitettu.</span><span class="sxs-lookup"><span data-stu-id="d374e-256">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="d374e-257">Varmista sitovasti suunnitellut tuotantotilaukset, jotka on luotu.</span><span class="sxs-lookup"><span data-stu-id="d374e-257">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="d374e-258">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sitovasti suunn. tuotantotil.** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d374e-258">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="d374e-259">Tarkista **Sitovasti suunn. tuotantotil.** -ikkunassa, miten yksittäisten tilausten aloitus- ja päättymisajat on ajoitettu tuoterakenteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d374e-259">In the **Firm Planned Prod. Orders** window review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="d374e-260">Alimman tason komponentit tuotetaan ensin.</span><span class="sxs-lookup"><span data-stu-id="d374e-260">The lowest-level components are produced first.</span></span> <span data-ttu-id="d374e-261">Monitasoisten tilausten suunnitteleminen onkin tärkeää, kuten tässä suunnittelun työnkulussa on havainnollistettu.</span><span class="sxs-lookup"><span data-stu-id="d374e-261">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d374e-262">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d374e-262">See Also</span></span>  
 <span data-ttu-id="d374e-263">[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="d374e-263">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="d374e-264">Vaihekuvaus: Toimitusten automaattinen suunnittelu</span><span class="sxs-lookup"><span data-stu-id="d374e-264">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)

