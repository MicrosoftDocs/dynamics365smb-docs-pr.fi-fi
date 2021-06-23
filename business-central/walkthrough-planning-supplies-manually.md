---
title: Vaihekuvaus – Toimitusten manuaalinen suunnittelu | Microsoft Docs
description: Tässä vaihekuvauksessa kuvataan toimitustilausten suunnitteluprosessi uuden kysynnän täyttämiseksi. Voit aloittaa tarjonnan suunnittelun tietyin välein, esimerkiksi joka aamu tai joka maanantai, tai kun myynti tai tuotanto ilmoittaa ne kysyntätyypin mukaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c1ab3c48ae09b75ab9e54e0c9fe9afd49b833f09
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214676"
---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="e3c89-104">Vaihekuvaus: Toimitusten manuaalinen suunnittelu</span><span class="sxs-lookup"><span data-stu-id="e3c89-104">Walkthrough: Planning Supplies Manually</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

<span data-ttu-id="e3c89-105">Tässä vaihekuvauksessa kuvataan toimitustilausten suunnitteluprosessi uuden kysynnän täyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="e3c89-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="e3c89-106">Voit aloittaa tarjonnan suunnittelun tietyin välein, esimerkiksi joka aamu tai joka maanantai, tai kun myynti tai tuotanto ilmoittaa ne kysyntätyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="e3c89-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="e3c89-107">Tässä vaihekuvauksessa käytetään **Tilauksen suunnittelu** -sivua. Se on yksinkertainen toimitusten suunnittelutyökalu, joka perustuu parametripohjaisen automaattisen suunnittelun asemesta manuaaliseen päätöksentekoon.</span><span class="sxs-lookup"><span data-stu-id="e3c89-107">In this walkthrough you will use the **Order Planning** page, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="e3c89-108">Tietoja tästä vaihekuvauksesta</span><span class="sxs-lookup"><span data-stu-id="e3c89-108">About This Walkthrough</span></span>  
 <span data-ttu-id="e3c89-109">Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="e3c89-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="e3c89-110">ostotilauksen suunnitteleminen valmistuskomponentteja varten</span><span class="sxs-lookup"><span data-stu-id="e3c89-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="e3c89-111">myyntikysynnän täyttäminen siirtotilauksia suunnittelemalla</span><span class="sxs-lookup"><span data-stu-id="e3c89-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="e3c89-112">monitasoisen nimikkeen tuotantotilauksen suunnitteleminen.</span><span class="sxs-lookup"><span data-stu-id="e3c89-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="e3c89-113">Roolit</span><span class="sxs-lookup"><span data-stu-id="e3c89-113">Roles</span></span>  
 <span data-ttu-id="e3c89-114">Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="e3c89-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="e3c89-115">Tuotantosuunnittelija</span><span class="sxs-lookup"><span data-stu-id="e3c89-115">Production Planner</span></span>  
-   <span data-ttu-id="e3c89-116">Ostaja</span><span class="sxs-lookup"><span data-stu-id="e3c89-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="e3c89-117">myyntitilausten käsittelijä</span><span class="sxs-lookup"><span data-stu-id="e3c89-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="e3c89-118">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="e3c89-118">Prerequisites</span></span>  
 <span data-ttu-id="e3c89-119">Ennen kuin aloitat tämän vaihekohtaisen ohjeen, sinun on asennettava [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e3c89-119">Before you begin this walkthrough, you must install the [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e3c89-120">Tietokantaan on tehtävä seuraavat muutokset:</span><span class="sxs-lookup"><span data-stu-id="e3c89-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="e3c89-121">Poista kaikki aiemmat polkupyörien myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="e3c89-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="e3c89-122">Luo kymmenelle polkupyörälle yksi myyntitilaus ITÄ-sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="e3c89-122">Create one sales order for 10 bicycles at EAST location.</span></span>  
-   <span data-ttu-id="e3c89-123">Poista kaikki suunnitellut ja sitovasti suunnitellut tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="e3c89-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="e3c89-124">Älä poista aloitettuja tilauksia, joissa on aiemmin kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e3c89-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="e3c89-125">Tässä vaihekuvauksessa kannattaa käyttää ehdotettuja tietoja, koska näissä tiedoissa on tarvittavat tietueet.</span><span class="sxs-lookup"><span data-stu-id="e3c89-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="e3c89-126">Taustatietoja</span><span class="sxs-lookup"><span data-stu-id="e3c89-126">Story</span></span>  
 <span data-ttu-id="e3c89-127">Pienen teollisuusyhtiön tuotantosuunnittelija Karl aikoo suunnitella tuotanto- ja ostotilaukset uuden myyntikysynnän täyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="e3c89-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="e3c89-128">Koska tuotteissa ei ole useaa tuoterakennetasoa eikä tilauksia ole paljon, Karl luo toimitustilaukset manuaalisesti **Tilauksen suunnittelu** -sivulla yksi tuotetaso kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="e3c89-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** page to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="e3c89-129">Monimutkaisemmissa tuotantoympäristöissä suunnittelutyökirjaa käytetään toimitusten suunnitteluun, joka perustuu nimikeparametreihin, kuten uudelleenajoitusjaksoon, toimitusajan varmistukseen ja uusintatilauspisteeseen, sekä kaikkien tuotetasojen yhdistetyn kysynnän erälaskentaan.</span><span class="sxs-lookup"><span data-stu-id="e3c89-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="e3c89-130">Esimerkkitietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e3c89-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="e3c89-131">Tavallisessa CRONUS esimerkkiyrityksessä on tällä hetkellä paljon suunnittelematonta kysyntää.</span><span class="sxs-lookup"><span data-stu-id="e3c89-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="e3c89-132">Tämän vaihekuvauksen suunnittelutehtävien aikana realistisesta liiketoimintojen työnkulusta täytyy poiketa. Siitä poiketaan jättämällä huomiotta kysyntä, jonka eräpäivät ovat lähellä, ja käyttämällä sen sijaan kysyntää, jonka eräpäivät ovat myöhäisempiä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-page"></a><span data-ttu-id="e3c89-133">Tilauksen suunnittelu -sivun käyttäminen</span><span class="sxs-lookup"><span data-stu-id="e3c89-133">Using the Order Planning Page</span></span>  

<span data-ttu-id="e3c89-134">**Tilauksen valmistelu** -sivua voi käyttää useista eri sijainneista:</span><span class="sxs-lookup"><span data-stu-id="e3c89-134">The **Order Planning** page can be accessed from several different locations:</span></span>  

-   <span data-ttu-id="e3c89-135">Tuotanto, Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="e3c89-135">Manufacturing, Planning</span></span>  
-   <span data-ttu-id="e3c89-136">Myynti ja markkinointi, Tilauksen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="e3c89-136">Sales & Marketing, Order Processing</span></span>  
-   <span data-ttu-id="e3c89-137">Osto, Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="e3c89-137">Purchase, Planning</span></span>  
-   <span data-ttu-id="e3c89-138">Lisäksi voit avata tämän sivun tietylle tuotantotilaukselle valitsemalla **Suunnitelma**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="e3c89-138">In addition, you can open this page for a specific production order by choosing the **Planning** action.</span></span>

### <a name="to-use-the-order-planning-page"></a><span data-ttu-id="e3c89-139">Tilauksen suunnittelu -sivun käyttäminen</span><span class="sxs-lookup"><span data-stu-id="e3c89-139">To use the Order Planning page</span></span>  

1.  <span data-ttu-id="e3c89-140">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tilauksen suunnittelu** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e3c89-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="e3c89-141">Kun **Tilauksen suunnittelu** -sivu avautuu, suunnitelma on laskettava, jotta uusi, edellisen laskennan jälkeinen kysyntä tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="e3c89-141">When the **Order Planning** page first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="e3c89-142">Valitse **Laske suunnitelma** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-142">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="e3c89-143">Suunnittelujärjestelmä analysoi mahdollisen uuden kysynnän, kuten uuden myynnin, muuttuneen myynnin tai tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="e3c89-143">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="e3c89-144">Kunkin kysyntärivin tarvittu määrä lasketaan kokonaissaatavuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="e3c89-144">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="e3c89-145">Nämä laskelmat tehdään tilauskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="e3c89-145">This calculation is performed order-by-order.</span></span> <span data-ttu-id="e3c89-146">Toisin sanoin ensin lasketaan kysyntärivin sisältävä tilaus, jolla on varhaisin eräpäivä tai lähetyksen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-146">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="e3c89-147">Tämän jälkeen muut kysyntärivit lasketaan samassa järjestyksessä eräpäivästä ja lähetyksen päivämäärästä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="e3c89-147">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="e3c89-148">Varmista, että **Tilauksen suunnittelu** -sivu on suurennettu ja että sarakkeen kenttien kokoa on muutettu siten, että kaikki oletuskenttänimet näkyvät.</span><span class="sxs-lookup"><span data-stu-id="e3c89-148">Be sure that the **Order Planning** page is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="e3c89-149">Kun laskutoimitukset on suoritettu, täyttämätön kysyntä näkyy sivulla supistettuina tilauksen otsikkoriveinä, jotka on lajiteltu varhaisimman mahdollisen kysyntäpäivämäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="e3c89-149">When the calculation is completed, the page displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="e3c89-150">Huomaa, että CRONUS -ohjelmalla on useita tilauksia, joissa on täyttämätöntä kysyntää.</span><span class="sxs-lookup"><span data-stu-id="e3c89-150">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="e3c89-151">Jokainen lihavoitu suunnittelurivi vastaa tilausta &mdash; myyntitilausta tai tuotantotilausta &mdash; ja mukana on vähintään yksi tilausrivi, jossa saatavuus on riittämätön.</span><span class="sxs-lookup"><span data-stu-id="e3c89-151">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="e3c89-152">Valitse **Näytä kysyntä muodossa** -kentän **Kaikki kysyntä** -suodatin.</span><span class="sxs-lookup"><span data-stu-id="e3c89-152">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="e3c89-153">**Kysyntätyyppi**-kentän avulla voit valita, mitkä tilaustyypit on tarkoitus tuoda näkyviin.</span><span class="sxs-lookup"><span data-stu-id="e3c89-153">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="e3c89-154">Tilaukset, joissa ei ole saatavuusongelmia, eivät näy.</span><span class="sxs-lookup"><span data-stu-id="e3c89-154">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="e3c89-155">Jos suunnitelman laskemisen jälkeen ei ole tilauksia, näyttöön tulee sanoma, mutta ei suunnittelurivejä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-155">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="e3c89-156">Ostotilauksen suunnitteleminen komponenttien kysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="e3c89-156">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="e3c89-157">Näissä toimintaohjeissa luodaan ostotilaus tarvittavia valmistuskomponentteja varten.</span><span class="sxs-lookup"><span data-stu-id="e3c89-157">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="e3c89-158">Ostotilauksen suunnitteleminen täyttämään tuotannon komponenttitarve</span><span class="sxs-lookup"><span data-stu-id="e3c89-158">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="e3c89-159">Laajenna ensimmäinen rivi (napsauta plusmerkkiä).</span><span class="sxs-lookup"><span data-stu-id="e3c89-159">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="e3c89-160">Valitse ensimmäinen kysyntärivi, jossa on nimike **LSU-15**, ja valitse sitten **Näytä asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-160">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="e3c89-161">Siirry takaisin **Tilauksen suunnittelu** -sivulle sulkemalla avattu tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="e3c89-161">Close the opened production order to return to the **Order Planning** page.</span></span>  
4.  <span data-ttu-id="e3c89-162">Valitse **Täydennysjärjestelmä**-kentässä **Osto**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-162">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="e3c89-163">Oletusarvo on nimikkeen kortti (tai varastoyksikön kortti), mutta sen voi vaihtaa yhdeksi kolmesta vaihtoehdosta:</span><span class="sxs-lookup"><span data-stu-id="e3c89-163">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="e3c89-164">**Osto** – luodaan ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="e3c89-164">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="e3c89-165">**Siirto** – Siirtotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="e3c89-165">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="e3c89-166">**Tuot.til.** – luodaan tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="e3c89-166">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="e3c89-167">Valitse **Tarjonta kohteesta** -kentässä jokin seuraavista vaihtoehdoista valitun täydennysjärjestelmän mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e3c89-167">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="e3c89-168">**Toimittaja** – ostoille</span><span class="sxs-lookup"><span data-stu-id="e3c89-168">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="e3c89-169">**Sijainti** – Siirrot</span><span class="sxs-lookup"><span data-stu-id="e3c89-169">**Location** – For transfers</span></span>  

     <span data-ttu-id="e3c89-170">Jos kentän tietoja ei täytetä, näkyviin tulee virhesanoma toimitustilauksia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="e3c89-170">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e3c89-171">Jos komponenteille on määritetty toimittajan oletusnumero nimikkeen kortteihin, rivit on määritetty ennalta.</span><span class="sxs-lookup"><span data-stu-id="e3c89-171">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="e3c89-172">Valitse **Tarjonta kohteesta** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-172">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="e3c89-173">Valitse **Nimikkeen toimittajaluettelo** -sivulla **Uusi**-toiminto ja valitse toimittaja **30000**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-173">On the **Item Vendor Catalogue** page, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="e3c89-174">Valitse **OK**-painike palataksesi **Tilauksen suunnittelu** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="e3c89-174">Choose the **OK** button to return to the **Order Planning** page.</span></span>  
9. <span data-ttu-id="e3c89-175">Kopioi toimittajan numero **30000** tämän tuotantotilauksen kaiutinkomponenttien muihin riveihin.</span><span class="sxs-lookup"><span data-stu-id="e3c89-175">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="e3c89-176">Nyt voit luoda ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="e3c89-176">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="e3c89-177">Valitse **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-177">Choose the **Make Orders** action.</span></span> <span data-ttu-id="e3c89-178">**Tee toimitustilaukset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="e3c89-178">The **Make Supply Orders** page opens.</span></span>  
11. <span data-ttu-id="e3c89-179">Valitse **Tee tilaukset** -kentän **Tilauksen suunnittelu** -pikavälilehdessä **Aktiivinen tilaus**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-179">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="e3c89-180">Valitse **Vaihtoehdot**-pikavälilehden **Luo ostotilaus** -kentästä **Tee ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-180">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="e3c89-181">Luo ostotilaukset tilauksen kaikille komponenteille valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-181">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="e3c89-182">Ostotilaukset luodaan ja tallennetaan viimeisiksi tilauksiksi ostotilausten luetteloon.</span><span class="sxs-lookup"><span data-stu-id="e3c89-182">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="e3c89-183">Siirtotilauksen suunnitteleminen myyntikysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="e3c89-183">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="e3c89-184">Näissä toimintaohjeissa kysyntää varten laaditaan suunnitelma myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="e3c89-184">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="e3c89-185">Kysyntärivit vastaavat myyntirivejä, eivät komponenttirivejä, kuten tuotantokysynnässä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-185">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="e3c89-186">Siirtotilauksen suunnitteleminen myyntikysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="e3c89-186">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="e3c89-187">Siirrä kohdistin tilauksen numero **2008** suunnitteluriville.</span><span class="sxs-lookup"><span data-stu-id="e3c89-187">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="e3c89-188">Laajenna rivi ja siirrä kohdistin kysyntäriville.</span><span class="sxs-lookup"><span data-stu-id="e3c89-188">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="e3c89-189">Myyntitilaus numero **2008** koskee kymmentä kaiutinta, joiden tyyppi on **LS-120** ja jotka on tilannut Vakuutusyhtiö Meri.</span><span class="sxs-lookup"><span data-stu-id="e3c89-189">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="e3c89-190">Näkyviin tulevat nimikkeen määritetty täydennysjärjestelmä ja oletustoimittaja.</span><span class="sxs-lookup"><span data-stu-id="e3c89-190">The item's defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e3c89-191">Sivun alaosassa on neljä tietokenttää.</span><span class="sxs-lookup"><span data-stu-id="e3c89-191">At the bottom of the page, there are four information fields.</span></span> <span data-ttu-id="e3c89-192">**Varhaisin mahdollinen päivämäärä** -kentässä näkyy, että tarvittavat kymmenen kappaletta tulevat saataville saapuvassa toimitustilauksessa yhdeksän päivää nykyisen eräpäivän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e3c89-192">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="e3c89-193">Jos tämä on asiakkaalle liian myöhäinen ajankohta, **Siirtoon saatavilla** -kentässä näkyy, että nimikettä on 13 kappaletta toisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="e3c89-193">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="e3c89-194">Tätä tavaraa varten on tarkoitus laatia suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="e3c89-194">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="e3c89-195">Avaa **Hae vaihtoehtoinen tarjonta** -sivu napsauttamalla **Siirtoon saatavilla** -kentän hakupainiketta.</span><span class="sxs-lookup"><span data-stu-id="e3c89-195">Choose the **Available for Transfer** field to open the **Get Alternative Supply** page.</span></span>  
4.  <span data-ttu-id="e3c89-196">Varaa kymmenen saatavilla olevaa nimikettä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-196">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e3c89-197">Siirto PÄÄ-sijainnista on vaihdettu ehdotetun oston tilalle kysyntäriville.</span><span class="sxs-lookup"><span data-stu-id="e3c89-197">In the demand line, the suggested purchase has been exchanged with a transfer from MAIN location.</span></span> <span data-ttu-id="e3c89-198">**Tee tilaukset** -toiminto luo siirtotilauksen PÄÄ-sijainnista vaadittuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="e3c89-198">The **Make Orders** function creates a transfer order from MAIN to the demanded location.</span></span> <span data-ttu-id="e3c89-199">**Korvaavia olemassa** -kenttä toimii samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e3c89-199">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="e3c89-200">Valitse **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-200">Choose the **Make Orders** action.</span></span> <span data-ttu-id="e3c89-201">**Tee toimitustilaukset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="e3c89-201">The **Make Supply Orders** page opens.</span></span>  
6.  <span data-ttu-id="e3c89-202">Valitse **Tee tilaukset** -kentän **Tilauksen suunnittelu** -pikavälilehdessä **Aktiivinen tilaus**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-202">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="e3c89-203">Valitse **Vaihtoehdot**-pikavälilehden **Luo siirtotilaus** -kentässä **Tee siirtotilaukset** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-203">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="e3c89-204">Luo siirtotilaus myyntitilauksen toimittamista varten valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-204">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="e3c89-205">Siirtotilaus luodaan ja tallennetaan luetteloon avointen siirtotilausten luettelon viimeiseksi tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="e3c89-205">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="e3c89-206">Monitasoisen tuotantotilauksen suunnitteleminen myyntikysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="e3c89-206">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="e3c89-207">Näissä toimintaohjeissa laaditaan suunnitelma, jossa tuotetun nimikkeen myyntikysyntä täytetään usealla tuotetasolla. Jokainen taso luo riippuvaisen tuotantokysynnän.</span><span class="sxs-lookup"><span data-stu-id="e3c89-207">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="e3c89-208">Monitasoisen tuotannon suunnitteleminen myyntikysynnän täyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="e3c89-208">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="e3c89-209">Valitse tilauksen numero **1001** suunnittelurivi, jolla on myyntikysyntää (se luotiin aiemmin vaihekuvauksen valmistavissa toimissa).</span><span class="sxs-lookup"><span data-stu-id="e3c89-209">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="e3c89-210">Tämä kysyntä on myyntirivi, mutta nimikkeelle on määritetty täydennysjärjestelmäksi **Tuotantotilaus**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-210">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="e3c89-211">Lisää ylimääräinen kello kunkin polkupyörän komponenttitarpeeseen.</span><span class="sxs-lookup"><span data-stu-id="e3c89-211">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="e3c89-212">Avaa **Suunnittelukomponentit**-sivu valitsemalla **Komponentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-212">Choose the **Components** action to open the **Planning Components** page.</span></span>  
3.  <span data-ttu-id="e3c89-213">Vaihda Kello-nimikkeen rivillä **Määrä per** -kentän arvo **1** arvoksi **2**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-213">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="e3c89-214">Harkitse suunnitteluvaihtoehtoja **Tilauksen suunnittelu** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e3c89-214">On the **Order Planning** page, consider your planning alternatives.</span></span> <span data-ttu-id="e3c89-215">Tässä tilanteessa vaihtoehtoisia toimitustapoja &mdash; siirtoa tai korvaavaa tai myöhempää toimitusta &mdash; ei ole.</span><span class="sxs-lookup"><span data-stu-id="e3c89-215">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="e3c89-216">Ehdotettu toimitustilaus, tuotantotilaus, on luotava.</span><span class="sxs-lookup"><span data-stu-id="e3c89-216">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="e3c89-217">Luo tuotantotilaus valitsemalla **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-217">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="e3c89-218">Huomaa, että myyntitilauksen **1001** suunnitteluriviä ei enää ole **Tilauksen suunnittelu** -sivulla. Alustava myyntikysyntä on täytetty.</span><span class="sxs-lookup"><span data-stu-id="e3c89-218">On the **Order Planning** page, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="e3c89-219">Sulje **Tilauksen suunnittelu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e3c89-219">Close the **Order Planning** page.</span></span>  

     <span data-ttu-id="e3c89-220">Tässä vaiheessa kaikki suunnittelutehtävät voitaisiin jäädä suorittamaan tähän näkymään.</span><span class="sxs-lookup"><span data-stu-id="e3c89-220">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="e3c89-221">Nyt kuitenkin omaksutaan tuotantosuunnittelijan rooli, siirrytään äsken luotuun tuotantotilaukseen ja käytetään **Tilauksen suunnittelu** -sivua.</span><span class="sxs-lookup"><span data-stu-id="e3c89-221">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** page.</span></span>  

 <span data-ttu-id="e3c89-222">Tuotantosuunnittelijan täytyy nyt suunnitella tietty tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="e3c89-222">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="e3c89-223">Tietyn tuotantotilauksen suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="e3c89-223">To plan a specific production order</span></span>  

1.  <span data-ttu-id="e3c89-224">Avaa tuotantotilaus **101001** (kymmenen polkupyörää), joka luotiin aiemmin **Tee tilaukset**-toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="e3c89-224">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="e3c89-225">Avaa **Tuot.til. komponentit** -sivu ja varmista, että ylimääräinen kello näkyy tuotantotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="e3c89-225">Open the **Prod. Order Components** page to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="e3c89-226">Valitse **Suunnittelu**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-226">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="e3c89-227">**Tilauksen suunnittelu** -sivu avautuu näkymään, joka suodatetaan aina tiettyyn tuotannon kysyntään.</span><span class="sxs-lookup"><span data-stu-id="e3c89-227">The **Order Planning** page opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="e3c89-228">Myyntikysyntä ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-228">Sales demand is not displayed.</span></span> <span data-ttu-id="e3c89-229">Suunnitelma on laskettava, ennen kuin lisäkysyntä tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="e3c89-229">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="e3c89-230">Valitse **Laske suunnitelma** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-230">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="e3c89-231">Huomaa, että neljä uutta tuotantotilausta näkyy tilauksesta **101001** johdettuna suunnittelemattomana tuotantokysyntänä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-231">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="e3c89-232">Uudet rivit vastaavat niiden alikokoonpanojen uutta tuotantokysyntää, joka täytyy luoda tilauksen tuottamista varten.</span><span class="sxs-lookup"><span data-stu-id="e3c89-232">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="e3c89-233">Valitse **Laajenna kaikki** -toiminto, jos haluat nähdä yleiskuvauksen tuotantotilausten koko tuotantokysynnästä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-233">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="e3c89-234">Antaaksesi lisätietoja kysyntäriveistä, saatat haluta lisätä **Kysyntämäärä** ja **Käytettävissä oleva kysyntämäärä** -kenttiä näkymääsi.</span><span class="sxs-lookup"><span data-stu-id="e3c89-234">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="e3c89-235">Seuraavaksi kutakin komponenttia on toimitettava kymmenen kappaletta.</span><span class="sxs-lookup"><span data-stu-id="e3c89-235">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="e3c89-236">Huomaa, että neljällä kysyntärivillä on täydennysjärjestelmä Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="e3c89-236">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="e3c89-237">Nämä neljä osakokoonpanoa edustavat polkupyörän toista tuotantotasoa.</span><span class="sxs-lookup"><span data-stu-id="e3c89-237">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="e3c89-238">Oletustäydennysasetukset on täytetty valmiiksi, ja voit aloittaa tilausten tekemisen.</span><span class="sxs-lookup"><span data-stu-id="e3c89-238">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="e3c89-239">Valitse **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-239">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="e3c89-240">Ennen kuin painat **OK**-painiketta, huomioi teksti **Tilauksen suunnittelu**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-240">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="e3c89-241">Tämä teksti on tärkeä, koska polkupyörän tuoterakenteessa tiedetään olevan joitakin tuotettuja komponentteja eli alikokoonpanoja, joilla voisi olla kysyntää, kun luot tämän tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="e3c89-241">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="e3c89-242">Valitse **Tee toimitustilaukset** -sivun **Tee tilaukset**-kentässä **Kaikki rivit** ja valitse sitten **OK**, jos haluat luoda tuotantotilaukset tilauksen toiselle tuotetasolle.</span><span class="sxs-lookup"><span data-stu-id="e3c89-242">On the **Make Supply Order** page, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="e3c89-243">Huomaa, että tuotantotilauksella 101001 ei enää ole ylätason tuotantokysyntää.</span><span class="sxs-lookup"><span data-stu-id="e3c89-243">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="e3c89-244">Se merkitsee, että alikokoonpanojen alustava tuotantokysyntä on otettu huomioon suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="e3c89-244">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="e3c89-245">Suunnitelma lasketaan uudelleen **Tilauksen suunnittelu** -sivulla, jotta polkupyörän rakenne voidaan suunnitella.</span><span class="sxs-lookup"><span data-stu-id="e3c89-245">On the **Order Planning** page, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="e3c89-246">Laske suunnitelma uudelleen upotetun ohjetekstin ohjeiden mukaisesti valitsemalla **Laske suunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-246">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="e3c89-247">Kaksi uutta riviä vastaavat ylimääräistä tuotantokysyntää, joka on johdettu edellisissä vaiheissa suunnitelluista alikokoonpanoista.</span><span class="sxs-lookup"><span data-stu-id="e3c89-247">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="e3c89-248">Pyörän napojen toimittamiseksi ehdotetaan kahta tuotantotilausta, yhtä kymmenelle etupyörän navalle ja niin ikään yhtä kymmenelle takapyörän navalle.</span><span class="sxs-lookup"><span data-stu-id="e3c89-248">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="e3c89-249">Valitse **Laajenna kaikki** -toiminto, jos haluat nähdä yleiskuvauksen kahden tuotantotilauksen koko tuotantokysynnästä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-249">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="e3c89-250">Ehdotettu toimitussuunnitelma osoittaa, että komponenteille luodaan yhteensä neljä ostotilausta.</span><span class="sxs-lookup"><span data-stu-id="e3c89-250">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="e3c89-251">Ehdotetut tilaukset päätetään tehdä.</span><span class="sxs-lookup"><span data-stu-id="e3c89-251">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="e3c89-252">Valitse **Tee tilaukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-252">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="e3c89-253">Valitse **Tee tilaukset** -kentässä **Kaikki rivit** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3c89-253">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="e3c89-254">Tarkista, onko päänimikkeen eli polkupyörän (myydään myyntitilauksella 1001) tuotannolla lisäkysyntää.</span><span class="sxs-lookup"><span data-stu-id="e3c89-254">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="e3c89-255">Valitse **Laske suunnitelma** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e3c89-255">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="e3c89-256">Sanomassa ilmoitetaan, että kaikki vaaditut nimikkeet on nyt toimitettu.</span><span class="sxs-lookup"><span data-stu-id="e3c89-256">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="e3c89-257">Varmista sitovasti suunnitellut tuotantotilaukset, jotka on luotu.</span><span class="sxs-lookup"><span data-stu-id="e3c89-257">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="e3c89-258">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e3c89-258">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="e3c89-259">Tarkista **Sitovasti suunn. tuotantotil.** -sivulla, miten yksittäisten tilausten aloitus- ja päättymisajat on ajoitettu tuoterakenteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e3c89-259">On the **Firm Planned Prod. Orders** page review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="e3c89-260">Alimman tason komponentit tuotetaan ensin.</span><span class="sxs-lookup"><span data-stu-id="e3c89-260">The lowest-level components are produced first.</span></span> <span data-ttu-id="e3c89-261">Monitasoisten tilausten suunnitteleminen onkin tärkeää, kuten tässä suunnittelun työnkulussa on havainnollistettu.</span><span class="sxs-lookup"><span data-stu-id="e3c89-261">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e3c89-262">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e3c89-262">See Also</span></span>  
 <span data-ttu-id="e3c89-263">[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="e3c89-263">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]