---
title: Myynti- ja ostoasiakirjojen arkistointi | Microsoft Docs
description: "Voit arkistoida myynti- ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Voit myös käyttää arkistoitua asiakirjaa ja luoda uudelleen asiakirjan, josta ne arkistoitiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a><span data-ttu-id="651bb-103">Asiakirjojen arkistointi</span><span class="sxs-lookup"><span data-stu-id="651bb-103">Archive Documents</span></span>
<span data-ttu-id="651bb-104">Voit arkistoida myynti- ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Voit myös käyttää arkistoitua asiakirjaa ja luoda uudelleen asiakirjan, josta ne arkistoitiin.</span><span class="sxs-lookup"><span data-stu-id="651bb-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="651bb-105">Asiakirjojen automaattisen arkistoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="651bb-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="651bb-106">Voit määrittää myynti- ja ostotilausten, tarjousten, puitetilausten ja palautustilausten automaattisen arkistoinnin ennen asiakirjojen poistamista.</span><span class="sxs-lookup"><span data-stu-id="651bb-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="651bb-107">Seuraavassa kuvataan, miten myyntiasiakirjojen automaattinen arkistointi määritetään.</span><span class="sxs-lookup"><span data-stu-id="651bb-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="651bb-108">Vaiheet ovat samankaltaiset ostoasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="651bb-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="651bb-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntien ja myyntisaamisten asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="651bb-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="651bb-110">Täytä kentät **Myyntien ja myyntisaamisten asetukset** -ikkunassa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="651bb-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="651bb-111">Kenttä</span><span class="sxs-lookup"><span data-stu-id="651bb-111">Field</span></span>|<span data-ttu-id="651bb-112">Description</span><span class="sxs-lookup"><span data-stu-id="651bb-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="651bb-113">**Myyntitarjousten arkistointi**</span><span class="sxs-lookup"><span data-stu-id="651bb-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="651bb-114">**Ei koskaan**, jos myyntitarjouksia ei arkistoida koskaan poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="651bb-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="651bb-115">**Kysymys**, kun käyttäjältä kysytään myyntitarjousten arkistoinnista tarjousten poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="651bb-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="651bb-116">**Aina**, kun myyntitarjoukset arkistoidaan automaattisesti poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="651bb-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="651bb-117">**Puitemyyntitilausten arkistointi**</span><span class="sxs-lookup"><span data-stu-id="651bb-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="651bb-118">Puitemyyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="651bb-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="651bb-119">**Arkist. tilaukset ja pal.tilaukset**</span><span class="sxs-lookup"><span data-stu-id="651bb-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="651bb-120">Myyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="651bb-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="651bb-121">Myyntitilauksen arkistointi</span><span class="sxs-lookup"><span data-stu-id="651bb-121">To archive a sales order</span></span>
<span data-ttu-id="651bb-122">Seuraavassa kuvataan, miten myyntitilaus arkistoidaan.</span><span class="sxs-lookup"><span data-stu-id="651bb-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="651bb-123">Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.</span><span class="sxs-lookup"><span data-stu-id="651bb-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="651bb-124">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="651bb-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="651bb-125">Avaa myyntitilaus, jonka haluat arkistoida.</span><span class="sxs-lookup"><span data-stu-id="651bb-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="651bb-126">Valitse **Arkistoi asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="651bb-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="651bb-127">Myyntitilaus on arkistoitu.</span><span class="sxs-lookup"><span data-stu-id="651bb-127">The sales order is archived.</span></span> <span data-ttu-id="651bb-128">Voit tarkastella sitä **Arkistoidut myyntitilaukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="651bb-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="651bb-129">Ikkunassa voit myös luoda uudelleen myyntitilauksen, josta se arkistoitiin.</span><span class="sxs-lookup"><span data-stu-id="651bb-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="651bb-130">Myyntitilauksen luominen uudelleen arkistosta</span><span class="sxs-lookup"><span data-stu-id="651bb-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="651bb-131">Seuraavassa kuvataan, miten myyntitilaus luodaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="651bb-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="651bb-132">Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.</span><span class="sxs-lookup"><span data-stu-id="651bb-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="651bb-133">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Arkistoidut myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="651bb-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="651bb-134">Valitse arkistoitu myyntitilaus, joka luodaan uudelleen, ja valitse sitten **Palauta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="651bb-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="651bb-135">Myyntitilaus luodaan ja lisätään **Myyntitilaukset**-ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="651bb-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="651bb-136">Arkistoitujen myyntitilausten poistaminen</span><span class="sxs-lookup"><span data-stu-id="651bb-136">To delete archived sales orders</span></span>
<span data-ttu-id="651bb-137">Seuraavassa kuvataan, miten arkistoidut myyntitilaukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="651bb-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="651bb-138">Vaiheet ovat samanlaiset muille arkistoiduille myynti- ja ostoasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="651bb-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="651bb-139">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista arkistoidut myyntitilausversiot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="651bb-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="651bb-140">Valitse **Poista arkistoidut myyntitilausversiot** -ikkunassa sopivat suodattimet.</span><span class="sxs-lookup"><span data-stu-id="651bb-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="651bb-141">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="651bb-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="651bb-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="651bb-142">See Also</span></span>
[<span data-ttu-id="651bb-143">Asiakirjarivien seuranta</span><span class="sxs-lookup"><span data-stu-id="651bb-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="651bb-144">Myynti</span><span class="sxs-lookup"><span data-stu-id="651bb-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="651bb-145">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="651bb-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="651bb-146">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="651bb-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

