---
title: Fyysisen varaston siirtojen suunnitteleminen työkirjassa | Microsoft Docs
description: Varastosiirrot suunnitellaan työkirjassa käyttämällä varastopaikan täydennystoimintoa tai suunnittelemalla manuaalisesti rivit, jotka haluat luoda siirto-ohjeiksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 58bfedd22d072a90eef0e3f678a34de29e7f9582
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192889"
---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="31375-103">Fyysisen varaston siirtojen suunnitteleminen työkirjoissa</span><span class="sxs-lookup"><span data-stu-id="31375-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="31375-104">Varastosiirrot suunnitellaan työkirjassa käyttämällä varastopaikan täydennystoimintoa tai suunnittelemalla manuaalisesti rivit, jotka haluat luoda siirto-ohjeiksi.</span><span class="sxs-lookup"><span data-stu-id="31375-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="31375-105">Täydennyssiirtojen laskeminen</span><span class="sxs-lookup"><span data-stu-id="31375-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="31375-106">Kun fyysinen varasto toimittaa nimikkeitä asiakkaille, varastopaikoista, joilla on korkein varastopaikan luokittelu, nimikkeiden määrä vähenee jatkuvasti.</span><span class="sxs-lookup"><span data-stu-id="31375-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="31375-107">Voit täyttää näitä korkean luokittelun poimintavarastopaikkoja muiden varastopaikkojen nimikkeillä, suorittamalla **Laske var.paikan täydennys** -toiminto **Siirtotyökirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="31375-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function on the **Movement Worksheet** page</span></span>

1.  <span data-ttu-id="31375-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Siirtotyökirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="31375-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="31375-109">Valitse **Laske var.paikan täydennys**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="31375-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="31375-110">luo rivejä, joissa ohjataan tarkasti, miten nimikkeet on siirrettävä matalan luokittelun varastopaikoista korkean luokittelun varastopaikkoihin.</span><span class="sxs-lookup"><span data-stu-id="31375-110">creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="31375-111">Varaston siirtoa ehdotetaan FEFO:n mukaan, kun aktivoit  **Luo siirto** -toiminnon, jos seuraavat edellytykset täyttyvät kohteelle:</span><span class="sxs-lookup"><span data-stu-id="31375-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="31375-112">Nimikkeellä on vanhenemispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="31375-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="31375-113">Sijaintikortin **FEFO-poiminta**-valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="31375-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="31375-114">Sijaintikortin **Var.paikka pakollinen** -valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="31375-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="31375-115">**Alue koodista**- ja **Var.paikasta**-kentät ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="31375-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="31375-116">Lisätietoja on kohdassa [FEFO-poiminta](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="31375-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="31375-117">Tarkasta rivit ja muuta niitä tarvittaessa tai poista joitain niistä, jos kaikkien niiden suorittamiseen ei ole aikaa.</span><span class="sxs-lookup"><span data-stu-id="31375-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="31375-118">Valitse **Luo siirto** -toiminto, jos haluat tehdä fyysisen varastoinnin ohjeen työntekijöiden toiminnoksi.</span><span class="sxs-lookup"><span data-stu-id="31375-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="31375-119">Voit siirtää yhden varastopaikan tai useiden varastopaikkojen koko sisällön Hae var.paikan sisältö -toiminnon avulla seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="31375-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="31375-120">Voit myös käyttää muiden siirtojen suunnitteluun fyysisessä varastossa varastosiirtotyökirjaa.</span><span class="sxs-lookup"><span data-stu-id="31375-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="31375-121">Kun haluat esimerkiksi sijoittaa nimikkeitä varastopaikkaan laaduntarkastusta varten, voit käyttää tämän toiminnon suunnittelemiseen varastosiirtotyökirjaa. Muodosta sitten ohjeet työntekijälle luomalla varastosiirto.</span><span class="sxs-lookup"><span data-stu-id="31375-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="31375-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Siirtotyökirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="31375-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="31375-123">Valitse **Hae var.paikan sisältö** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="31375-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="31375-124">Pyyntösivun avulla voit suodattaa varastopaikat ja nimikkeet, jotka näkyvät varastosiirtotyökirjan riveillä.</span><span class="sxs-lookup"><span data-stu-id="31375-124">Use the request page to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="31375-125">Kirjoita eräajon pyyntösivulla asianmukaisten kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="31375-125">Fill in the relevant fields in the batch job request page.</span></span> <span data-ttu-id="31375-126">Jos haluat esimerkiksi nähdä sijainnin tietyn alueen kaikkien varastopaikkojen sisällön, kirjoita arvo **Alueen koodi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="31375-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="31375-127">Jos haluat hakea tietyn nimikkeen sisältävien varastopaikkojen rivit, kirjoita arvo **Nimikkeen nro** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="31375-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="31375-128">Nimikkeitä ei voi siirtää manuaalisesti Vastaanotto-tyyppiseen varastopaikkaan eikä myöskään pois tällaisesta varastopaikasta. Tämä johtuu siitä, että Vastaanotto-tyyppisen varastopaikan nimikkeet on rekisteröitävä hyllytettäviksi, ennen kuin ne voivat olla osa saatavilla olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="31375-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="31375-129">Jos haet useita rivejä, valitse **Lajittele**, valitse haluamasi työkirjan rivien lajittelutapa ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="31375-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="31375-130">Siirtorivit noudetaan FEFO:n mukaan, kun aktivoit **Hae var.paikan sisältö** -toiminnon, jos seuraavat edellytykset täyttyvät kohteelle:</span><span class="sxs-lookup"><span data-stu-id="31375-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="31375-131">Nimikkeellä on vanhenemispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="31375-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="31375-132">Sijaintikortin **FEFO-poiminta**-valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="31375-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="31375-133">Sijaintikortin **Var.paikka pakollinen** -valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="31375-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="31375-134">**Alue koodista**- ja **Var.paikasta**-kentät ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="31375-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="31375-135">Tee haluamasi muutokset täydentämällä haettuja rivejä.</span><span class="sxs-lookup"><span data-stu-id="31375-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="31375-136">Kullakin siirrettävällä nimikkeellä on oltava arvo **Nimikkeen nro**-, **Var.paikasta**-, **Varastopaikkakoodiin**- ja  **Määrä**-kentissä.</span><span class="sxs-lookup"><span data-stu-id="31375-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="31375-137">Poista epätäydelliset rivit, joita olet käyttänyt viitetietoina.</span><span class="sxs-lookup"><span data-stu-id="31375-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="31375-138">Kun varastosiirtotyökirjan rivit vastaavat tapaa, jolla haluat varastotyöntekijän tekevän siirron, luo ohjeet työntekijälle valitsemalla **Luo siirto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="31375-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="31375-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="31375-139">See Also</span></span>  
[<span data-ttu-id="31375-140">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="31375-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="31375-141">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="31375-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="31375-142">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="31375-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="31375-143">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="31375-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="31375-144">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="31375-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="31375-145">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="31375-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
