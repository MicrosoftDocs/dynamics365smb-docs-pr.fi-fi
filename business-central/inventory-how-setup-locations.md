---
title: Sijaintikortin ja siirtoreittien määrittäminen
description: Jokaisille varastoitavalle varastonimikkeelle luodaan sijaintikortti, kuten varasto tai jakelukeskus. Lisäksi sijaintien välille määritetään siirtoreitit.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184322"
---
# <a name="set-up-locations"></a><span data-ttu-id="d18d3-103">Sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d18d3-103">Set Up Locations</span></span>

<span data-ttu-id="d18d3-104">Jos ostat, varastoit tai myyt nimikkeitä useamman varaston avulla, sijaintikortti ja siirtoreitit on määritettävä jokaiselle sijainnille.</span><span class="sxs-lookup"><span data-stu-id="d18d3-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="d18d3-105">[!INCLUDE [prod_short](includes/prod_short.md)] käyttää sijainteja varaston seurannassa sekä yksinkertaisemmissa tapauksissa että monimutkaisemmissa varastoprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="d18d3-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="d18d3-106">Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen.</span><span class="sxs-lookup"><span data-stu-id="d18d3-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="d18d3-107">Lisätietoja on myös kohdassa [Varaston hallinta](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="d18d3-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="d18d3-108">Sijaintikortit</span><span class="sxs-lookup"><span data-stu-id="d18d3-108">Location cards</span></span>

<span data-ttu-id="d18d3-109">Sijaintikortissa määritetään tietoja sijainnista, esimerkiksi fyysisestä varastosta tai jakelukeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="d18d3-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="d18d3-110">Kullekin sijainnille annetaan sijaintia kuvaava nimi ja koodi.</span><span class="sxs-lookup"><span data-stu-id="d18d3-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="d18d3-111">Tämän jälkeen sijaintikoodin voi syöttää muualle ohjelmaan silloin, kun haluat tallentaa transaktioita tietylle sijainnille.</span><span class="sxs-lookup"><span data-stu-id="d18d3-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="d18d3-112">Voit syöttää tietoja varastopaikasta ja fyysisen varaston periaatteista jokaiselle sijainnille.</span><span class="sxs-lookup"><span data-stu-id="d18d3-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="d18d3-113">Valitsemiesi fyysisen varaston periaatteiden perusteella voit määrittää **Varastopaikat**-pikavälilehden vaihtoehtojen avulla varastopaikat, joita käytetään oletusvarastopaikkoina toteutettaessa tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="d18d3-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="d18d3-114">Jos käytät ohjattua hyllytystä ja poimintaa, voit määrittää **Var.paikkojen periaatteet** -pikavälilehden vaihtoehtojen avulla, miten haluat käyttää fyysisen varaston eri lisäominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="d18d3-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="d18d3-115">Jotkut vaihtoehtokentät ovat harmaana ja poissa käytöstä muiden asetusten vuoksi **Sijaintikortti**-sivulla. Tällä rajoitetaan asetusyhdistelmiä, joita ei tueta.</span><span class="sxs-lookup"><span data-stu-id="d18d3-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="d18d3-116">Valitse toiminto **Alueet** tai **Varastopaikat** nähdäksesi tiedot alueista ja varastopaikoista, jotka voidaan määrittää sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="d18d3-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="d18d3-117">Sijaintikortin luominen</span><span class="sxs-lookup"><span data-stu-id="d18d3-117">To create a location card</span></span>

1. <span data-ttu-id="d18d3-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sijainnit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d18d3-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="d18d3-119">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d18d3-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="d18d3-120">Täytä **Sijaintikortti**-sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="d18d3-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="d18d3-121">Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.</span><span class="sxs-lookup"><span data-stu-id="d18d3-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="d18d3-122">Monet sijaintikortin kentät viittaavat saapuvien ja lähtevien varastoprosessien nimikkeiden käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="d18d3-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="d18d3-123">Kentät eivät ole olennaisia yrityksille, jotka eivät tarvitse monimutkaisempaa varastotoimintoa.</span><span class="sxs-lookup"><span data-stu-id="d18d3-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="d18d3-124">Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d18d3-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="d18d3-125">Voit muuttaa sijainnin määritystä myöhemmin, mutta et voi muokata asetuksia niille sijainneille, joilla on kirjanpitotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="d18d3-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="d18d3-126">Jos sinulla on useampia sijainteja, seuraavaksi voit määrittää sijaintien välisiä siirtoreittejä.</span><span class="sxs-lookup"><span data-stu-id="d18d3-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="d18d3-127">Siirtoreittien luominen</span><span class="sxs-lookup"><span data-stu-id="d18d3-127">To create a transfer route</span></span>

1. <span data-ttu-id="d18d3-128">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Siirtoreitit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d18d3-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="d18d3-129">Voit myös valita **Siirtoreitit**-toiminnon miltä tahansa **Sijaintikortti**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="d18d3-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="d18d3-130">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d18d3-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="d18d3-131">Täytä **Sijaintikortti**-sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="d18d3-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="d18d3-132">Voit nyt siirtää varastonimikkeitä sijaintien välillä.</span><span class="sxs-lookup"><span data-stu-id="d18d3-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="d18d3-133">Lisätietoja on kohdassa [Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="d18d3-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="d18d3-134">Varastopaikat</span><span class="sxs-lookup"><span data-stu-id="d18d3-134">Bins</span></span>

<span data-ttu-id="d18d3-135">Varastopaikkat edustavat varastoinnin perusrakennetta ja niitä käytetään ehdotusten tekemiseksi nimikkeiden sijoittelusta.</span><span class="sxs-lookup"><span data-stu-id="d18d3-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="d18d3-136">Kun olet luonut varastopaikat, voit määrittää tarkasti sisällön, jonka haluat ohjelman sijoittavan kuhunkin varastopaikkaan, tai varastopaikka voi toimia määrittelemättömänä varastopaikkana, jolla ei ole määritettyä sisältöä.</span><span class="sxs-lookup"><span data-stu-id="d18d3-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="d18d3-137">Varastopaikkoja käytetään pääasiassa varaston perus- ja lisäoperaatioissa.</span><span class="sxs-lookup"><span data-stu-id="d18d3-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="d18d3-138">Jos hallitset varastoa yksinkertaisemmassa asetelmassa, et todennäköisesti tarvitse varastopaikkoja.</span><span class="sxs-lookup"><span data-stu-id="d18d3-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="d18d3-139">Jos haluat käyttää varastopaikkatoimintoa sijainnissa, aktivoi toiminto ensin **Sijainti**-kortissa valitsemalla **Varastopaikat pakollisia** -kenttä **Fyysinen varastointi**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d18d3-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="d18d3-140">Sitten voi suunnitella nimikevirran sijainnissa määrittämällä varastopaikkakoodit määrityskentistä, jotka edustavat eri virtoja.</span><span class="sxs-lookup"><span data-stu-id="d18d3-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="d18d3-141">Ennen kuin voit määrittää varastopaikkakoodeja sijaintikortissa, on luotava varastopaikkakoodit.</span><span class="sxs-lookup"><span data-stu-id="d18d3-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="d18d3-142">Lisätietoja on kohdissa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md) ja [Varastopaikkatyyppien määrittäminen](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="d18d3-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="d18d3-143">Alueet</span><span class="sxs-lookup"><span data-stu-id="d18d3-143">Zones</span></span>

<span data-ttu-id="d18d3-144">Jos haluat jäsentää varastopaikat alueiden alla, voit tehdä sen **Alueet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d18d3-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="d18d3-145">[!INCLUDE [prod_short](includes/prod_short.md)] kopioi tietylle alueelle asetetut kentät alueessa oleville varastopaikoille.</span><span class="sxs-lookup"><span data-stu-id="d18d3-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="d18d3-146">Voit määritellä alueen varastopaikalle tai varastopaikkamallille (varastopaikan luontisuodatus), ja sitten muita kenttiä täytetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d18d3-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="d18d3-147">Voit kuitenkin määrittää vain yhden alueen ja järjestellä fyysisen varaston vain varastopaikkojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d18d3-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="d18d3-148">Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d18d3-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d18d3-149">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d18d3-149">See Also</span></span>

[<span data-ttu-id="d18d3-150">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="d18d3-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d18d3-151">Varastonimikkeiden siirtäminen sijaintien välillä</span><span class="sxs-lookup"><span data-stu-id="d18d3-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="d18d3-152">Varastopaikkojen luominen</span><span class="sxs-lookup"><span data-stu-id="d18d3-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="d18d3-153">Varastopaikkojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d18d3-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="d18d3-154">Varastoinninhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d18d3-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="d18d3-155">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d18d3-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d18d3-156">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="d18d3-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="d18d3-157">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="d18d3-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]