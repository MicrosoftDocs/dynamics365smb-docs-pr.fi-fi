---
title: Puitekokoonpanotilauksien luominen | Microsoft Docs
description: "Jos nimikkeen kortin **Täydennysjärjestelmä**-kenttä sisältää **kokoonpanon**, nimikkeen toimituksen oletustapa on koota nimike määritetyistä komponenteista ja mahdollisesti määritetyn resurssin toimesta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 12/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 5801fcc1284edfe1b8578518c084455c336d5a40
ms.openlocfilehash: 8796ccf6ce73ded327fad35573a2268e249fb7a7
ms.contentlocale: fi-fi
ms.lasthandoff: 12/27/2018

---
# <a name="create-blanket-assembly-orders"></a><span data-ttu-id="43c40-103">Puitekokoonpanotilausten luominen</span><span class="sxs-lookup"><span data-stu-id="43c40-103">Create Blanket Assembly Orders</span></span>
<span data-ttu-id="43c40-104">Voit mukauttaa kokoonpanonimikettä asiakkaan pyynnöstä myyntiprosessin kokoonpanon hallinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="43c40-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="43c40-105">Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="43c40-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

 <span data-ttu-id="43c40-106">Samalla tavalla kuin minkä tahansa nimiketyypin kohdalla, voit myös luoda puitemyyntitilauksia mukautetun kokoonpanon osille ennen kuin teet säännöllisesti todelliset myyntitilaukset puitetilauksen sopimuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="43c40-106">As with any other type of item, you can also create blanket sales orders for customized assembly items before periodically making the actual sales orders according to the blanket order agreement.</span></span> <span data-ttu-id="43c40-107">Tähän toimenpiteeseen liittyy useita ylimääräisiä vaiheita tavallisen puitemyyntitilauksen luomiseen verrattuna, ja siinä käytetään linkitetyn kokoonpanotilauksen versiota, joka on puitekokoonpanotilaus.</span><span class="sxs-lookup"><span data-stu-id="43c40-107">This process involves several extra steps when you compare it to creating a regular blanket sales order, and it uses a variation of a linked assembly order, which is a blanket assembly order.</span></span>

> [!NOTE]  
>  <span data-ttu-id="43c40-108">Kuten kaikissa puitetilauksissa, kokoonpanon joukkotilausten määrät ovat vain ennusteita, eikä niitä käytetä, ennen kuin ne muunnetaan todellisiksi kokoonpanotilauksiksi.</span><span class="sxs-lookup"><span data-stu-id="43c40-108">Like all blanket orders, quantities on assembly blanket orders are only forecasts and are not operational until they are converted to actual assembly orders.</span></span> <span data-ttu-id="43c40-109">Tämän vuoksi tilaustoiminnot, kuten saatavuus, laskenta, varaus ja nimikeseuranta, eivät ole aktiivisia kokoonpanon puitetilauksissa.</span><span class="sxs-lookup"><span data-stu-id="43c40-109">Therefore, order functionality, such as availability calculation, reservation, and item tracking, is not active on blanket assembly orders.</span></span>  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a><span data-ttu-id="43c40-110">Luo puitekokokoonpanotilaus kokoonpano tilausta varten -nimikkeelle</span><span class="sxs-lookup"><span data-stu-id="43c40-110">To create a blanket assembly order for an assemble\-to\-order item</span></span>  
1. <span data-ttu-id="43c40-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Puitemyyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="43c40-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="43c40-112">Luo uusi puitemyyntitilaus yhdellä kokoonpanonimikkeen rivillä.</span><span class="sxs-lookup"><span data-stu-id="43c40-112">Create a new blanket sales order with one line for an assembly item.</span></span> <span data-ttu-id="43c40-113">Lisätietoja on kohdassa [Puitemyyntitilausten luominen](sales-how-to-create-blanket-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="43c40-113">For more information, see [Create Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>  
3. <span data-ttu-id="43c40-114">Kirjoita koko määrä puitekokoonpanotilausrivin **Kokoonpantava määrä tilausta varten** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="43c40-114">In the **Qty. to Assemble to Order** field on the blanket assembly order line, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="43c40-115">Sinun ei pitäisi luoda puitetilaussopimusta osittaiselle määrälle.</span><span class="sxs-lookup"><span data-stu-id="43c40-115">You should not create blanket order agreements for a partial quantity.</span></span> <span data-ttu-id="43c40-116">Tämän vuoksi täytyy syöttää sama määrä, joka on syötetty myynnin puitetilausrivin **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="43c40-116">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the blanket sales order line.</span></span>  

4. <span data-ttu-id="43c40-117">Valitse **Kokoonpano tilausta varten** -toiminto ja valitse sitten **Kokoonpano tilausta varten -rivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="43c40-117">Choose the **Assemble to Order** action, and then choose the **Assemble-to-Order Lines** action.</span></span> <span data-ttu-id="43c40-118">Vaihtoehtoisesti voit valita rivin **Kokoonpantava määrä tilausta varten** -kentän.</span><span class="sxs-lookup"><span data-stu-id="43c40-118">Alternatively, choose the **Qty. to Assemble to Order)** field on the line.</span></span>  
5. <span data-ttu-id="43c40-119">Tarkastele tai muokkaa **Kokoonpano tilausta varten -rivit** -sivulla asiakkaan kanssa tekemäsi puitetilaussopimuksen mukaisia kokoonpanotilauksen rivejä.</span><span class="sxs-lookup"><span data-stu-id="43c40-119">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the blanket order agreement that you have made with the customer.</span></span> <span data-ttu-id="43c40-120">Jos haluat tarkastella tietoja, avaa koko puitekokoonpanotilaus valitsemalla **Näytä asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="43c40-120">If you want to view more information, choose the **Show Document** action to open the complete blanket assembly order.</span></span> <span data-ttu-id="43c40-121">Useimpien kenttien sisältöä ei voi muuttaa etkä voi kirjata.</span><span class="sxs-lookup"><span data-stu-id="43c40-121">You cannot change the contents of most fields, and you cannot post.</span></span>  
6. <span data-ttu-id="43c40-122">Kun olet muokannut kokoonpanotilauksen rivejä puitetilauksen sopimuksen mukaisesti, sulje **Kokoonpano tilausta varten -rivit** -sivu ja palaa **Puitemyyntitilaus** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="43c40-122">When you have adjusted the assembly order lines according to the blanket order agreement, close the **Assemble-to-Order Lines** page to return to the **Blanket Sales Order** page.</span></span>  
7. <span data-ttu-id="43c40-123">Kun asiakas pyytää puitemyyntitilaukseen perustuvan myyntitilauksen luomista, luo myyntitilaus sovitulle kokoonpanon nimikkeelle tai nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="43c40-123">When the customer requests to create a sales order based on the agreed blanket sales order, create a sales order for the agreed assembly item or items.</span></span> <span data-ttu-id="43c40-124">Lisätietoja on kohdassa [Puitemyyntitilausten luominen](sales-how-to-create-blanket-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="43c40-124">For more information, see [Create Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>

<span data-ttu-id="43c40-125">Linkitetty puitekokoonpanotilaus ja kaikki muokkaukset on linkitetty uuteen myyntitilaukseen kokoonpanon tai myynnin valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="43c40-125">The linked blanket assembly order and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43c40-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="43c40-126">See Also</span></span>
[<span data-ttu-id="43c40-127">Puitemyyntitilausten luominen</span><span class="sxs-lookup"><span data-stu-id="43c40-127">Create Blanket Sales Orders</span></span>](sales-how-to-create-blanket-sales-orders.md)  
[<span data-ttu-id="43c40-128">Kokoonpanon hallinta</span><span class="sxs-lookup"><span data-stu-id="43c40-128">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="43c40-129">Tuoterakenteen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="43c40-129">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="43c40-130">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="43c40-130">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="43c40-131">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="43c40-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="43c40-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43c40-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

