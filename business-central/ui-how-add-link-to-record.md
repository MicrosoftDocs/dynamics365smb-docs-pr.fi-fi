---
title: Liitteiden, linkkien ja muistioiden lisääminen tietueisiin| Microsoft Docs
description: Liitä hyperlinkki asiakirjaan tai sivusto tiettyyn tietueeseen, kuten asiakkaaseen tai asiakirjaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 84d9c0768a457fd13a73b3d70d2b8c329098fe82
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953273"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="958a7-103">Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="958a7-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="958a7-104">Voit liittää useimpien korttien ja asiakirjojen tietoruudussa tiedostoja, lisätä linkkejä ja kirjoittaa muistioita.</span><span class="sxs-lookup"><span data-stu-id="958a7-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="958a7-105">Linkkejä ja muistioita voi kirjoittaa myös luettelosivulla sen jälkeen, kun olet valinnut liittyvän rivin.</span><span class="sxs-lookup"><span data-stu-id="958a7-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="958a7-106">Jos haluat tarkastella tai muuttaa näitä liitettyjä tietotyyppejä, sinun on avattava ensin tietoruudun **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="958a7-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="958a7-107">Välilehden otsikon takana oleva luku ilmaisee, kuinka monta liitettyä tiedostoa, linkkiä tai muistiinpanoa kortissa tai asiakirjassa on.</span><span class="sxs-lookup"><span data-stu-id="958a7-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="958a7-108">Liitteet, linkit ja muistiot pysyvät liitteinä, kun korttia tai asiakirjaa käsitellään muihin tiloihin, kuten siirtyminen jatkuvasta myyntitilauksesta kirjattuun myyntilaskuun.</span><span class="sxs-lookup"><span data-stu-id="958a7-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="958a7-109">Järjestelmä ei kuitenkaan käsittele mitään liitetyyppiä esimerkiksi tulostettaessa tai tallennettaessa tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="958a7-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="958a7-110">Kun toimitat ja laskutat myyntitilauksen tai ostotilauksen osittain, liite liitetään vain kyseisen tilauksen lopulliseen laskuun.</span><span class="sxs-lookup"><span data-stu-id="958a7-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="958a7-111">Samoin kun laskutat käyttämällä lykkäysominaisuutta, liite liitetään vain asiakirjan pääkirjanpidontapahtumiin, mutta ei lykkäystapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="958a7-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="958a7-112">Tiedoston liittäminen ostolaskuun</span><span class="sxs-lookup"><span data-stu-id="958a7-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="958a7-113">Korttiin tai asiakirjaan liitettävän tiedoston tyypillä ei ole merkitystä, ja se voi sisältää tekstiä, kuvan tai videon.</span><span class="sxs-lookup"><span data-stu-id="958a7-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="958a7-114">Tämä on kätevää esimerkiksi silloin, kun haluat tallentaa toimittajan laskun PDF-tiedostona liittyvään [!INCLUDE[d365fin](includes/d365fin_md.md)]in ostolaskuun.</span><span class="sxs-lookup"><span data-stu-id="958a7-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="958a7-115">Saapuvat asiakirjat -ominaisuudella liitetyt tiedostot eivät sisälly **Liitteet**-välilehteen. Lisätietoja on kohdassa [Saapuvat asiakirjat](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="958a7-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="958a7-116">Seuraava toimenpide perustuu myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="958a7-116">The following procedure is based on a sales order.</span></span> <span data-ttu-id="958a7-117">Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.</span><span class="sxs-lookup"><span data-stu-id="958a7-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="958a7-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="958a7-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="958a7-119">Avaa myyntitilaus, johon haluat liittää tiedoston.</span><span class="sxs-lookup"><span data-stu-id="958a7-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="958a7-120">Avaa **Liitteet**-välilehti tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="958a7-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="958a7-121">Valitse **Asiakirjat**-kentässä arvo, kuten 0.</span><span class="sxs-lookup"><span data-stu-id="958a7-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="958a7-122">Valitse **Liitetyt asiakirjat** -sivun **Liite**-kentässä **Valitse tiedosto** -painike.</span><span class="sxs-lookup"><span data-stu-id="958a7-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="958a7-123">Valitse tiedosto haluamastasi sijainnista ja valitse sitten **Avaa**-painike.</span><span class="sxs-lookup"><span data-stu-id="958a7-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="958a7-124">Tiedosto on nyt liitetty ostolaskuun.</span><span class="sxs-lookup"><span data-stu-id="958a7-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="958a7-125">Linkin lisääminen nimikekortista</span><span class="sxs-lookup"><span data-stu-id="958a7-125">To add a link from an item card</span></span>
<span data-ttu-id="958a7-126">Voit lisätä kortista tai asiakirjasta linkin mihin tahansa URL-osoitteeseen tai polkuun.</span><span class="sxs-lookup"><span data-stu-id="958a7-126">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="958a7-127">Tämä kätevää esimerkiksi silloin, kun haluat linkittää nimikekortin toimittajan nimikeluetteloon.</span><span class="sxs-lookup"><span data-stu-id="958a7-127">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="958a7-128">Seuraava toimenpide perustuu nimikekorttiin.</span><span class="sxs-lookup"><span data-stu-id="958a7-128">The following procedure is based on an item card.</span></span> <span data-ttu-id="958a7-129">Vaiheet ovat samanlaiset kaikissa tuetuissa korteissa ja asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="958a7-129">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="958a7-130">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="958a7-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="958a7-131">Valitse nimike, josta haluat lisätä linkin, ja valitse sitten tietoruudussa **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="958a7-131">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="958a7-132">Valitse **Linkit**-kohdassa **+**-kuvake.</span><span class="sxs-lookup"><span data-stu-id="958a7-132">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="958a7-133">Anna linkki **Linkin osoite** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="958a7-133">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="958a7-134">Linkin on oltava kelvollinen Internet- tai intranet-osoite.</span><span class="sxs-lookup"><span data-stu-id="958a7-134">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="958a7-135">Kirjoita **Kuvaus**-kenttään linkkiä koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="958a7-135">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="958a7-136">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="958a7-136">Choose the **OK** button.</span></span>

<span data-ttu-id="958a7-137">Linkki on nyt liitetty nimikekorttiin.</span><span class="sxs-lookup"><span data-stu-id="958a7-137">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="958a7-138">Muistion kirjoittaminen myyntitilaukseen</span><span class="sxs-lookup"><span data-stu-id="958a7-138">To write a note on a sales order</span></span>
<span data-ttu-id="958a7-139">Voit kirjoittaa asiakirjaan tai korttiin muistion, jossa on esimerkiksi ohjeita muille asiakirjan tai kortin käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="958a7-139">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="958a7-140">Voit sisällyttää muistioihin tiedostolinkkejä ja URL-osoitteita.</span><span class="sxs-lookup"><span data-stu-id="958a7-140">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="958a7-141">**Liitteet**-välilehdessä olevat muistiot eivät liity sisäiseen muistiotoimintoon, jota käytetään lähinnä työnkulujen käyttäjien keskinäiseen viestintään.</span><span class="sxs-lookup"><span data-stu-id="958a7-141">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="958a7-142">Lisätietoja on kohdassa [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="958a7-142">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="958a7-143">Seuraava toimenpide perustuu myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="958a7-143">The following procedure is based on a sales order.</span></span> <span data-ttu-id="958a7-144">Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.</span><span class="sxs-lookup"><span data-stu-id="958a7-144">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="958a7-145">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="958a7-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="958a7-146">Valitse myyntitilaus, johon haluat kirjoittaa muistion, ja valitse sitten tietoruudussa **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="958a7-146">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="958a7-147">Valitse **Muistiot**-osassa **+**-kuvake.</span><span class="sxs-lookup"><span data-stu-id="958a7-147">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="958a7-148">Kirjoita **Huomautus**-kenttään tekstiä, kuten Tämä on kiireellinen tilaus.</span><span class="sxs-lookup"><span data-stu-id="958a7-148">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="958a7-149">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="958a7-149">Choose the **OK** button.</span></span>

<span data-ttu-id="958a7-150">Huomautus on nyt liitetty myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="958a7-150">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="958a7-151">Katso myös</span><span class="sxs-lookup"><span data-stu-id="958a7-151">See Also</span></span>  
<span data-ttu-id="958a7-152">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="958a7-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="958a7-153">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="958a7-153">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="958a7-154">Työnkulkuilmoitusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="958a7-154">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
