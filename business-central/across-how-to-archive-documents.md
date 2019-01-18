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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4827e25d97127faf691b96df9868320bb47dee39
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="archive-documents"></a><span data-ttu-id="614e5-103">Asiakirjojen arkistointi</span><span class="sxs-lookup"><span data-stu-id="614e5-103">Archive Documents</span></span>
<span data-ttu-id="614e5-104">Voit arkistoida myynti- ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Voit myös käyttää arkistoitua asiakirjaa ja luoda uudelleen asiakirjan, josta ne arkistoitiin.</span><span class="sxs-lookup"><span data-stu-id="614e5-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="614e5-105">Asiakirjojen automaattisen arkistoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="614e5-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="614e5-106">Voit määrittää myynti- ja ostotilausten, tarjousten, puitetilausten ja palautustilausten automaattisen arkistoinnin ennen asiakirjojen poistamista.</span><span class="sxs-lookup"><span data-stu-id="614e5-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="614e5-107">Seuraavassa kuvataan, miten myyntiasiakirjojen automaattinen arkistointi määritetään.</span><span class="sxs-lookup"><span data-stu-id="614e5-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="614e5-108">Vaiheet ovat samankaltaiset ostoasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="614e5-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="614e5-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="614e5-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="614e5-110">Täytä kentät **Myyntien ja myyntisaamisten asetukset** -sivulla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="614e5-110">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="614e5-111">Kenttä</span><span class="sxs-lookup"><span data-stu-id="614e5-111">Field</span></span>|<span data-ttu-id="614e5-112">Description</span><span class="sxs-lookup"><span data-stu-id="614e5-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="614e5-113">**Myyntitarjousten arkistointi**</span><span class="sxs-lookup"><span data-stu-id="614e5-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="614e5-114">**Ei koskaan**, jos myyntitarjouksia ei arkistoida koskaan poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="614e5-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="614e5-115">**Kysymys**, kun käyttäjältä kysytään myyntitarjousten arkistoinnista tarjousten poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="614e5-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="614e5-116">**Aina**, kun myyntitarjoukset arkistoidaan automaattisesti poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="614e5-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="614e5-117">**Puitemyyntitilausten arkistointi**</span><span class="sxs-lookup"><span data-stu-id="614e5-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="614e5-118">Puitemyyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="614e5-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="614e5-119">**Arkist. tilaukset ja pal.tilaukset**</span><span class="sxs-lookup"><span data-stu-id="614e5-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="614e5-120">Myyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="614e5-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="614e5-121">Myyntitilauksen arkistointi</span><span class="sxs-lookup"><span data-stu-id="614e5-121">To archive a sales order</span></span>
<span data-ttu-id="614e5-122">Seuraavassa kuvataan, miten myyntitilaus arkistoidaan.</span><span class="sxs-lookup"><span data-stu-id="614e5-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="614e5-123">Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.</span><span class="sxs-lookup"><span data-stu-id="614e5-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="614e5-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="614e5-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="614e5-125">Avaa myyntitilaus, jonka haluat arkistoida.</span><span class="sxs-lookup"><span data-stu-id="614e5-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="614e5-126">Valitse **Arkistoi asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="614e5-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="614e5-127">Myyntitilaus on arkistoitu.</span><span class="sxs-lookup"><span data-stu-id="614e5-127">The sales order is archived.</span></span> <span data-ttu-id="614e5-128">Voit tarkastella sitä **Arkistoidut myyntitilaukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="614e5-128">You can view it on the **Archived Sales orders** page.</span></span> <span data-ttu-id="614e5-129">Ikkunassa voit myös luoda uudelleen myyntitilauksen, josta se arkistoitiin.</span><span class="sxs-lookup"><span data-stu-id="614e5-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="614e5-130">Myyntitilauksen luominen uudelleen arkistosta</span><span class="sxs-lookup"><span data-stu-id="614e5-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="614e5-131">Seuraavassa kuvataan, miten myyntitilaus luodaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="614e5-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="614e5-132">Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.</span><span class="sxs-lookup"><span data-stu-id="614e5-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="614e5-133">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Arkistoidut myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="614e5-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="614e5-134">Valitse arkistoitu myyntitilaus, joka luodaan uudelleen, ja valitse sitten **Palauta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="614e5-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="614e5-135">Myyntitilaus luodaan ja lisätään **Myyntitilaukset**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="614e5-135">The sales order is created and added to the **Sales Orders** page.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="614e5-136">Arkistoitujen myyntitilausten poistaminen</span><span class="sxs-lookup"><span data-stu-id="614e5-136">To delete archived sales orders</span></span>
<span data-ttu-id="614e5-137">Seuraavassa kuvataan, miten arkistoidut myyntitilaukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="614e5-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="614e5-138">Vaiheet ovat samanlaiset muille arkistoiduille myynti- ja ostoasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="614e5-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="614e5-139">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista arkistoidut myyntitilausversiot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="614e5-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="614e5-140">Valitse **Poista arkistoidut myyntitilausversiot** -sivulla sopivat suodattimet.</span><span class="sxs-lookup"><span data-stu-id="614e5-140">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="614e5-141">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="614e5-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="614e5-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="614e5-142">See Also</span></span>
[<span data-ttu-id="614e5-143">Asiakirjarivien seuranta</span><span class="sxs-lookup"><span data-stu-id="614e5-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="614e5-144">Myynti</span><span class="sxs-lookup"><span data-stu-id="614e5-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="614e5-145">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="614e5-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="614e5-146">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="614e5-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

