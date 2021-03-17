---
title: Kokoonpano tilausta varten -myynnin tarjous | Microsoft Docs
description: Voit mukauttaa kokoonpanonimikettä asiakkaan pyynnöstä myyntiprosessin kokoonpanon hallinnan avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 807c924e64764e7ac1932321603a415101e3bbf3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386647"
---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="35e73-103">Kokoonpano tilausta varten -myynnin tarjous</span><span class="sxs-lookup"><span data-stu-id="35e73-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="35e73-104">Voit mukauttaa kokoonpanonimikettä asiakkaan pyynnöstä myyntiprosessin kokoonpanon hallinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="35e73-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="35e73-105">Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="35e73-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="35e73-106">Kuin silloin, kun myyt minkä tahansa muun tyyppisen nimikkeen, voit myös luoda myyntitarjouksen muokatulle kokoonpanonimikkeelle ennen kuin se muunnetaan myyntitilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="35e73-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="35e73-107">Tähän toimenpiteeseen liittyy useita ylimääräisiä vaiheita tavallisen puitemyyntitarjouksen luomiseen verrattuna, ja siinä käytetään linkitetyn kokoonpanotilauksen versiota, joka on puitekokoonpanotarjous.</span><span class="sxs-lookup"><span data-stu-id="35e73-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="35e73-108">Kaikentyyppisten tarjousten tapaan kokoonpanotarjousten määriä ei käytetä saatavuusmäärissä, suunnittelussa eikä varauksissa.</span><span class="sxs-lookup"><span data-stu-id="35e73-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="35e73-109">Luo myyntitarjous kokoonpano tilausta varten -nimikkeelle</span><span class="sxs-lookup"><span data-stu-id="35e73-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="35e73-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitarjous** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="35e73-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="35e73-111">Luo uusi myyntitarjousrivi yhdellä kokoonpanonimikkeen rivillä.</span><span class="sxs-lookup"><span data-stu-id="35e73-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="35e73-112">Lisätietoja on kohdassa [Myyntitarjousten tekeminen](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="35e73-112">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="35e73-113">Anna **Kokoonpantava määrä tilausta varten** -kentässä koko määrä.</span><span class="sxs-lookup"><span data-stu-id="35e73-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="35e73-114">Älä tee tarjousta osatoimituksesta.</span><span class="sxs-lookup"><span data-stu-id="35e73-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="35e73-115">Sen vuoksi sinun täytyy syöttää sama määrä, jonka syötit myynnin puitetarjousrivin **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="35e73-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="35e73-116">Valitse **Rivit**-pikavalintalehdessä **Rivi**, valitse **Kokoonpano tilausta varten** ja valitse sitten **Kokoonpano tilausta varten -rivit**.</span><span class="sxs-lookup"><span data-stu-id="35e73-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="35e73-117">Voit myös valita rivin **Kokoonpantava määrä tilausta varten** -kentän.</span><span class="sxs-lookup"><span data-stu-id="35e73-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="35e73-118">Tarkastele tai muokkaa **Kokoonpano tilausta varten -rivit** -sivulla asiakkaan pyytämän tarjouksen mukaisia kokoonpanotilauksen rivejä.</span><span class="sxs-lookup"><span data-stu-id="35e73-118">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="35e73-119">Jos haluat tarkastella tietoja, avaa koko puitetarjoustilaus valitsemalla **Näytä asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="35e73-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="35e73-120">Useimpien kenttien sisältöä ei voi muuttaa etkä voi kirjata.</span><span class="sxs-lookup"><span data-stu-id="35e73-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="35e73-121">Kun olet muokannut kokoonpanotilauksen rivejä tarjouksen mukaisesti, sulje **Kokoonpano tilausta varten -rivit** -sivu palataksesi **Myyntitarjous** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="35e73-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** page to return to the **Sales Quote** page.</span></span>  
7.  <span data-ttu-id="35e73-122">Jos asiakas hyväksyy tarjouksen, luo tarjotusta kokoonpanon nimikkeestä myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="35e73-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="35e73-123">Lisätietoja on kohdassa [Myyntitarjousten tekeminen](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="35e73-123">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span> <span data-ttu-id="35e73-124">Linkitetty kokoonpanotarjous ja kaikki muokkaukset on linkitetty uuteen myyntitilaukseen kokoonpanon tai myynnin valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="35e73-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="35e73-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="35e73-125">See Also</span></span>  
[<span data-ttu-id="35e73-126">Kokoonpanon hallinta</span><span class="sxs-lookup"><span data-stu-id="35e73-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="35e73-127">Tuoterakenteen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="35e73-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="35e73-128">Varasto</span><span class="sxs-lookup"><span data-stu-id="35e73-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="35e73-129">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="35e73-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="35e73-130">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="35e73-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]