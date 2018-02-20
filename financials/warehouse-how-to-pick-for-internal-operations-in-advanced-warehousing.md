---
title: "Poiminta sisäisissä toiminnoissa laajennetuissa varastomäärityksissä | Microsoft-asiakirjat"
description: "Jos sijainti on määritetty laajennetuissa varastomäärityksissä käyttämään sekä poimintaa että toimitusta, tuotannon ja kokoonpanon toimintojen komponentteja voi poimia **F.varastoinnin poiminta** -ikkunassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0a18e88ae9bb34b3cf5aa9d4a28e1d087ba9aa40
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="pick-for-assembly-or-production-in-advanced-warehouse-configurations"></a><span data-ttu-id="cf07e-103">Kokoonpano- tai tuotantopoiminta laajennetuissa varastointimäärityksissä</span><span class="sxs-lookup"><span data-stu-id="cf07e-103">Pick for Assembly or Production in Advanced Warehouse Configurations</span></span>
<span data-ttu-id="cf07e-104">Jos sijainti on määritetty laajennetuissa varastomäärityksissä käyttämään sekä poimintaa että toimitusta, tuotannon ja kokoonpanon toimintojen komponentteja voi poimia **F.varastoinnin poiminta** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="cf07e-104">In advanced warehouse configurations where the location is set up to use picking as well as shipping, you can pick components for production and assembly activities with the **Warehouse Pick** window.</span></span>  

<span data-ttu-id="cf07e-105">Vaihtoehtoisesti voit siirtää kohteita varastopaikasta toiseen **Siirtotyökirja**-ikkunassa ilman viittausta lähdeasiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="cf07e-105">Alternatively, you can use the **Movement Worksheet** window to move items between bins ad hoc, meaning without reference to a source document.</span></span> <span data-ttu-id="cf07e-106">Lisätietoja on kohdassa [Nimikkeiden siirtäminen laajennetussa varastointimäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="cf07e-106">For more information, see [Move Items in advanced warehouse configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

<span data-ttu-id="cf07e-107">Lisätietoja nimikkeiden poiminnasta sisäisiä toimintoja varten niissä fyysisen varaston perussijainneissa, jotka on määritetty vain poimintaa varten, on kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin määrityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="cf07e-107">For information about picking items for internal operations in basic warehouse locations that are set up for picking only, see [Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>  

<span data-ttu-id="cf07e-108">Fyysisen varastoinnin poiminta-asiakirjaa voi luoda alusta alkaen, koska poiminta-aktiviteetti on aina osa työnkulkua sekä veto- että työntötilanteessa.</span><span class="sxs-lookup"><span data-stu-id="cf07e-108">You cannot create a warehouse pick document from scratch because a pick activity is always part of a workflow, either in a pull or a push scenario.</span></span>  

<span data-ttu-id="cf07e-109">Voit luoda fyysisen varastoinnin poiminta-asiakirjan valitsemalla push-muodissa **Luo F.var. poiminta** lähdeasiakirjassa, kuten julkaistu kokoonpanotilaus tai fyysisen varaston toimitus.</span><span class="sxs-lookup"><span data-stu-id="cf07e-109">You can create the warehouse pick document in a push fashion by selecting **Create Whse. Pick** on the source document, such as a released assembly order or warehouse shipment.</span></span> <span data-ttu-id="cf07e-110">Lisätietoja on kohdassa [Nimikkeiden poiminta fyysisen varaston poiminnassa](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="cf07e-110">For more information, see [Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>  

<span data-ttu-id="cf07e-111">Vaihtoehtoisesti voit luoda varastopoiminta-asiakirjan tunnistamalla sekä toimitusten että sisäisten toimintojen poimintapyynnöt **Poimi työkirja** -ikkunassa ja luomalla sitten tarvittavat varastopoiminta-asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="cf07e-111">Alternatively, you can create the warehouse pick document in a pull fashion by using the **Pick Worksheet** window to detect pick requests, both for shipment and internal operations, and then create the required warehouse pick documents.</span></span>  

<span data-ttu-id="cf07e-112">Seuraavassa ohjeissa selitetään vetotilanne, jossa **Valitse työkirja** -ikkunassa poimitaan komponentteja vapautetulle tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="cf07e-112">The following procedure explains a pull scenario where you pick components for a released production order through the **Pick Worksheet** window.</span></span> <span data-ttu-id="cf07e-113">Menettely koskee myös kokoonpanotilauksia.</span><span class="sxs-lookup"><span data-stu-id="cf07e-113">The procedure also applies for an assembly order.</span></span>  

<span data-ttu-id="cf07e-114">Luodaksesi poimintapyynnöt sekä veto- että työntötilanteille, kyseiset lähdeasiakirjat on vapautettava.</span><span class="sxs-lookup"><span data-stu-id="cf07e-114">To create pick requests, both for pull and for push scenarios, the source documents in question must be released.</span></span> <span data-ttu-id="cf07e-115">Vapauta sisäisten toimintojen lähdeasiakirjat seuraavilla tavoilla.</span><span class="sxs-lookup"><span data-stu-id="cf07e-115">Release source documents for internal operations in the following ways.</span></span>  

|<span data-ttu-id="cf07e-116">Lähdeasiakirja</span><span class="sxs-lookup"><span data-stu-id="cf07e-116">Source Document</span></span>|<span data-ttu-id="cf07e-117">Vapautustapa</span><span class="sxs-lookup"><span data-stu-id="cf07e-117">Release Method</span></span>|  
|---------------------|--------------------|  
|<span data-ttu-id="cf07e-118">Tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="cf07e-118">Production Order</span></span>|<span data-ttu-id="cf07e-119">Muuta tilauksen tyypiksi vapautettu tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="cf07e-119">Change order type to released production order.</span></span>|  
|<span data-ttu-id="cf07e-120">Kokoonpanotilaus</span><span class="sxs-lookup"><span data-stu-id="cf07e-120">Assembly Order</span></span>|<span data-ttu-id="cf07e-121">Muuta tilaksi Vapautettu.</span><span class="sxs-lookup"><span data-stu-id="cf07e-121">Change status to Released.</span></span>|  

## <a name="to-pick-components-using-the-pick-worksheet"></a><span data-ttu-id="cf07e-122">Komponenttien poiminta poimintatyökirjoista</span><span class="sxs-lookup"><span data-stu-id="cf07e-122">To pick components using the pick worksheet</span></span>  
1.  <span data-ttu-id="cf07e-123">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poimintatyökirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="cf07e-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Pick Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cf07e-124">Valitse ensin **Hae f. varastoinnin asiakirjat** -toiminto ja sitten komponenttirivit vapautetusta tuotantotilauksesta.</span><span class="sxs-lookup"><span data-stu-id="cf07e-124">Choose the **Get Warehouse Documents** action, and then select the component lines from the released production order.</span></span>  
3.  <span data-ttu-id="cf07e-125">Käy rivit läpi, järjestele ne tehokkaaksi poimintakierrokseksi ja yhdistele niitä tarpeen mukaan muiden työkirjarivien kanssa siten, että työntekijän aika käytetään mahdollisimman tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="cf07e-125">Inspect the lines, sort them to ensure an efficient picking round, and combine them with other worksheet lines if necessary to make best use of employee time.</span></span>  
4.  <span data-ttu-id="cf07e-126">Valitse **Luo poiminta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="cf07e-126">Choose the **Create Pick** action.</span></span>  
5.  <span data-ttu-id="cf07e-127">Määritä, miten voit luoda fyysisen varastoinnin poiminta-asiakirjat ja lajitella poimintarivit täyttämällä kentät **Luo poiminta** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="cf07e-127">Define how to create the warehouse pick documents and how to sort pick lines by filling fields in the **Create Pick** window.</span></span>  
6.  <span data-ttu-id="cf07e-128">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="cf07e-128">Choose the **OK** button.</span></span> <span data-ttu-id="cf07e-129">Varastopoiminta-asiakirjat on luotu poimintarivien kanssa jokaiselle osalle, jota tarvitaan sisäisessäl toiminnassa.</span><span class="sxs-lookup"><span data-stu-id="cf07e-129">Warehouse pick documents are created with pick lines for each component that is required in the internal operation.</span></span>  

<span data-ttu-id="cf07e-130">Jos sisäiselle toimintoalueelle, kuten tuotantokerrokselle, määritetään oletusvarastopaikka toiminnossa käytettävien komponenttien sijoitusta varten, tämä varastopaikkakoodi lisätään fyysisen varaston poiminta-asiakirjan Aseta-riveille. Se ohjaa varastotyöntekijöitä nimikkeiden sijoittamisessa paikoilleen.</span><span class="sxs-lookup"><span data-stu-id="cf07e-130">If the internal operation area, such as a production shop floor, is set up with a default bin for placement of components to be used in the operation, then that bin code is inserted in the Place lines on the warehouse pick document to instruct warehouse workers where to place the items.</span></span> <span data-ttu-id="cf07e-131">Lisätietoja on **Tuotannon valmisteluvarastopaikkakoodi** tai **Kokoonpanoon-varastop.koodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cf07e-131">For more information, see the **To-Production Bin Code** or the **To-Assembly Bin Code** field.</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="cf07e-132">Kulutuksen varastopaikan täyttäminen</span><span class="sxs-lookup"><span data-stu-id="cf07e-132">Filling the Consumption Bin</span></span>
<span data-ttu-id="cf07e-133">Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien**Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="cf07e-133">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="cf07e-134">![Varastopaikkojen vuokaavio](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="cf07e-134">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf07e-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cf07e-135">See Also</span></span>
[<span data-ttu-id="cf07e-136">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="cf07e-136">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="cf07e-137">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="cf07e-137">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="cf07e-138">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="cf07e-138">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="cf07e-139">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="cf07e-139">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="cf07e-140">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="cf07e-140">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="cf07e-141">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf07e-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

