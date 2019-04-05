---
title: Myynti- ja ostoasiakirjojen arkistointi | Microsoft Docs
description: Voit arkistoida myynti- ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Voit myös käyttää arkistoitua asiakirjaa ja luoda uudelleen asiakirjan, josta ne arkistoitiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/14/2018
ms.author: sgroespe
ms.openlocfilehash: 2f05313d30aede255e4ef49065f0189d649ce93c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796164"
---
# <a name="archive-documents"></a><span data-ttu-id="8a162-103">Asiakirjojen arkistointi</span><span class="sxs-lookup"><span data-stu-id="8a162-103">Archive Documents</span></span>
<span data-ttu-id="8a162-104">Voit arkistoida osto- ja myyntitilauksia, tarjouksia, palautustilauksia ja puitetilauksia esimerkiksi siksi, että haluat tallentaa asiakirjan kopion käytettäväksi myöhemmin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8a162-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="8a162-105">Voit arkistoida myynti- tai ostoasiakirjan useita kertoja ja tallentaa kullakin kerralla erilaisen arkistoidun version.</span><span class="sxs-lookup"><span data-stu-id="8a162-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="8a162-106">Jos kyse on asiakirjoista, joiden alkuperäinen versio on vielä olemassa eikä sitä ole kirjattu, voit korvata alkuperäisen asiakirjan arkistoidulla versiolla **Palauta**-toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="8a162-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="8a162-107">Tämä on kätevää, jos asiakirjaan halutaan palauttaa aiempi sisältö.</span><span class="sxs-lookup"><span data-stu-id="8a162-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="8a162-108">Jos kyse on arkistoiduista asiakirjoista, joiden alkuperäinen versio on poistettu, voit käyttää sisällön uudelleen ainoastaan kopioimalla tiedot esimerkiksi **Kopioi asiakirja** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="8a162-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="8a162-109">Asiakirjojen automaattisen arkistoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8a162-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="8a162-110">Voit määrittää myynti- ja ostotilausten, tarjousten, puitetilausten ja palautustilausten automaattisen arkistoinnin ennen asiakirjojen poistamista.</span><span class="sxs-lookup"><span data-stu-id="8a162-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="8a162-111">Seuraavassa kuvataan, miten myyntiasiakirjojen automaattinen arkistointi määritetään.</span><span class="sxs-lookup"><span data-stu-id="8a162-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="8a162-112">Vaiheet ovat samankaltaiset ostoasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="8a162-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="8a162-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8a162-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="8a162-114">Täytä kentät **Myyntien ja myyntisaamisten asetukset** -sivulla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8a162-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="8a162-115">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8a162-115">Field</span></span>|<span data-ttu-id="8a162-116">Description</span><span class="sxs-lookup"><span data-stu-id="8a162-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="8a162-117">**Myyntitarjousten arkistointi**</span><span class="sxs-lookup"><span data-stu-id="8a162-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="8a162-118">**Ei koskaan**, jos myyntitarjouksia ei arkistoida koskaan poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8a162-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="8a162-119">**Kysymys**, kun käyttäjältä kysytään myyntitarjousten arkistoinnista tarjousten poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8a162-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="8a162-120">**Aina**, kun myyntitarjoukset arkistoidaan automaattisesti poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8a162-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="8a162-121">**Puitemyyntitilausten arkistointi**</span><span class="sxs-lookup"><span data-stu-id="8a162-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="8a162-122">Puitemyyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8a162-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="8a162-123">**Arkist. tilaukset ja pal.tilaukset**</span><span class="sxs-lookup"><span data-stu-id="8a162-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="8a162-124">Myyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8a162-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="8a162-125">Myyntitilauksen arkistointi</span><span class="sxs-lookup"><span data-stu-id="8a162-125">To archive a sales order</span></span>
<span data-ttu-id="8a162-126">Seuraavassa kuvataan, miten myyntitilaus arkistoidaan.</span><span class="sxs-lookup"><span data-stu-id="8a162-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="8a162-127">Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.</span><span class="sxs-lookup"><span data-stu-id="8a162-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="8a162-128">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8a162-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8a162-129">Avaa myyntitilaus, jonka haluat arkistoida.</span><span class="sxs-lookup"><span data-stu-id="8a162-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="8a162-130">Valitse **Arkistoi asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="8a162-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="8a162-131">Myyntitilaus on arkistoitu.</span><span class="sxs-lookup"><span data-stu-id="8a162-131">The sales order is archived.</span></span> <span data-ttu-id="8a162-132">Voit tarkastella sitä **Arkistoidut myyntitilaukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8a162-132">You can view it on the **Archived Sales orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="8a162-133">Kirjaamattomien myyntitilausten palauttaminen arkistosta</span><span class="sxs-lookup"><span data-stu-id="8a162-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="8a162-134">Seuraavaksi käsitellään menetelmä, jolla arkistoidun myyntitilauksen sisältö tuodaan takaisin alkuperäiseen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="8a162-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="8a162-135">Tämä on mahdollista vain, jos alkuperäistä tiedostoa ei ole kirjattu.</span><span class="sxs-lookup"><span data-stu-id="8a162-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="8a162-136">Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.</span><span class="sxs-lookup"><span data-stu-id="8a162-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="8a162-137">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Arkistoidut myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8a162-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="8a162-138">Valitse palautettava arkistoitu myyntitilaus tai sen versio ja valitse sitten **Palauta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="8a162-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="8a162-139">Alkuperäisen myyntitilauksen sisältö korvataan valitun arkistoidun version sisällöllä.</span><span class="sxs-lookup"><span data-stu-id="8a162-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="8a162-140">Arkistoitujen myyntitilausten poistaminen</span><span class="sxs-lookup"><span data-stu-id="8a162-140">To delete archived sales orders</span></span>
<span data-ttu-id="8a162-141">Seuraavassa kuvataan, miten arkistoidut myyntitilaukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="8a162-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="8a162-142">Vaiheet ovat samanlaiset muille arkistoiduille myynti- ja ostoasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="8a162-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="8a162-143">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista arkistoidut myyntitilausversiot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8a162-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8a162-144">Valitse **Poista arkistoidut myyntitilausversiot** -sivulla sopivat suodattimet.</span><span class="sxs-lookup"><span data-stu-id="8a162-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="8a162-145">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="8a162-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a162-146">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8a162-146">See Also</span></span>
[<span data-ttu-id="8a162-147">Asiakirjarivien seuranta</span><span class="sxs-lookup"><span data-stu-id="8a162-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="8a162-148">Myynti</span><span class="sxs-lookup"><span data-stu-id="8a162-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="8a162-149">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="8a162-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="8a162-150">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8a162-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
