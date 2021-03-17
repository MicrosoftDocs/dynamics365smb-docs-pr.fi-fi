---
title: Liitteiden, linkkien ja muistioiden lisääminen tietueisiin| Microsoft Docs
description: Liitä hyperlinkki asiakirjaan tai sivusto tiettyyn tietueeseen, kuten asiakkaaseen tai asiakirjaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6aa7018a43db8c663c209894e118518c3de2f7cf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393879"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="11718-103">Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="11718-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="11718-104">Voit liittää useimpien korttien ja asiakirjojen tietoruudussa tiedostoja, lisätä linkkejä ja kirjoittaa muistioita.</span><span class="sxs-lookup"><span data-stu-id="11718-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="11718-105">Linkkejä ja muistioita voi kirjoittaa myös luettelosivulla sen jälkeen, kun olet valinnut liittyvän rivin.</span><span class="sxs-lookup"><span data-stu-id="11718-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="11718-106">Jos haluat tarkastella tai muuttaa näitä liitettyjä tietotyyppejä, sinun on avattava ensin tietoruudun **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="11718-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="11718-107">Välilehden otsikon takana oleva luku ilmaisee, kuinka monta liitettyä tiedostoa, linkkiä tai muistiinpanoa kortissa tai asiakirjassa on.</span><span class="sxs-lookup"><span data-stu-id="11718-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="11718-108">Liitteet, linkit ja muistiot pysyvät liitteinä, kun korttia tai asiakirjaa käsitellään muihin tiloihin, kuten siirtyminen jatkuvasta myyntitilauksesta kirjattuun myyntilaskuun.</span><span class="sxs-lookup"><span data-stu-id="11718-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="11718-109">Järjestelmä ei kuitenkaan käsittele mitään liitetyyppiä esimerkiksi tulostettaessa tai tallennettaessa tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="11718-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="11718-110">Kun toimitat ja laskutat myyntitilauksen tai ostotilauksen osittain, liite liitetään vain kyseisen tilauksen lopulliseen laskuun.</span><span class="sxs-lookup"><span data-stu-id="11718-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="11718-111">Samoin kun laskutat käyttämällä lykkäysominaisuutta, liite liitetään vain asiakirjan pääkirjanpidontapahtumiin, mutta ei lykkäystapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="11718-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="11718-112">Tiedoston liittäminen ostolaskuun</span><span class="sxs-lookup"><span data-stu-id="11718-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="11718-113">Korttiin tai asiakirjaan liitettävän tiedoston tyypillä ei ole merkitystä, ja se voi sisältää tekstiä, kuvan tai videon.</span><span class="sxs-lookup"><span data-stu-id="11718-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="11718-114">Tämä on kätevää esimerkiksi silloin, kun haluat tallentaa toimittajan laskun PDF-tiedostona liittyvään [!INCLUDE[prod_short](includes/prod_short.md)]in ostolaskuun.</span><span class="sxs-lookup"><span data-stu-id="11718-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="11718-115">Saapuvat asiakirjat -ominaisuudella liitetyt tiedostot eivät sisälly **Liitteet**-välilehteen. Lisätietoja on kohdassa [Saapuvat asiakirjat](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="11718-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="11718-116">Seuraava toimenpide perustuu ostolaskuun.</span><span class="sxs-lookup"><span data-stu-id="11718-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="11718-117">Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.</span><span class="sxs-lookup"><span data-stu-id="11718-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="11718-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="11718-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="11718-119">Avaa myyntitilaus, johon haluat liittää tiedoston.</span><span class="sxs-lookup"><span data-stu-id="11718-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="11718-120">Avaa **Liitteet**-välilehti tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="11718-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="11718-121">Valitse **Asiakirjat**-kentässä arvo, kuten 0.</span><span class="sxs-lookup"><span data-stu-id="11718-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="11718-122">Valitse **Liitetyt asiakirjat** -sivun **Liite**-kentässä **Valitse tiedosto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="11718-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="11718-123">Valitse tiedosto haluamastasi sijainnista ja valitse sitten **Avaa**-painike.</span><span class="sxs-lookup"><span data-stu-id="11718-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="11718-124">Tiedosto on nyt liitetty ostolaskuun.</span><span class="sxs-lookup"><span data-stu-id="11718-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="11718-125">Tarkastele liitettyä tiedostoa</span><span class="sxs-lookup"><span data-stu-id="11718-125">To view an attached file</span></span>
1. <span data-ttu-id="11718-126">Avaa **Liitteet**-välilehti tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="11718-126">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="11718-127">Valitse **Asiakirjat**-kentässä arvo, kuten 1.</span><span class="sxs-lookup"><span data-stu-id="11718-127">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="11718-128">Valitse **Liitetyt asiakirjat** -sivulla **Esikatselu**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="11718-128">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="11718-129">Ladatun tiedoston avaaminen.</span><span class="sxs-lookup"><span data-stu-id="11718-129">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="11718-130">Asiakirjan tallentaminen PDF-liitteenä</span><span class="sxs-lookup"><span data-stu-id="11718-130">To save a document as a PDF attachment</span></span>
<span data-ttu-id="11718-131">Kun asiakirja on tallennettava tiedostoksi, voit käyttää **Liitä PDF-tiedostona** -toimintoa ja tallentaa nykyisen asiakirjan sisällön PDF-tiedostoksi, joka on liitetty asiakirjan tietoruutuun.</span><span class="sxs-lookup"><span data-stu-id="11718-131">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="11718-132">Tämä on hyödyllistä esimerkiksi silloin, kun asiakirjat noudattavat useita vaiheita prosessissa, kuten esimerkiksi myyntiprosessissa ja hyväksynnän työnkulussa, ja haluat viitata edellisen vaiheen tulostukseen.</span><span class="sxs-lookup"><span data-stu-id="11718-132">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="11718-133">Seuraava toimenpide perustuu myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="11718-133">The following procedure is based on a sales order.</span></span> <span data-ttu-id="11718-134">Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="11718-134">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="11718-135">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="11718-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="11718-136">Valitse ensin myyntitilaus ja valitse sitten **Liitä PDF-tiedostona** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="11718-136">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="11718-137">PDF-tiedosto ja sen sisältö myyntitilauksesta lisätään **Liitteet**-välilehteen tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="11718-137">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="11718-138">Linkin lisääminen nimikekortista</span><span class="sxs-lookup"><span data-stu-id="11718-138">To add a link from an item card</span></span>
<span data-ttu-id="11718-139">Voit lisätä kortista tai asiakirjasta linkin mihin tahansa URL-osoitteeseen tai polkuun.</span><span class="sxs-lookup"><span data-stu-id="11718-139">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="11718-140">Tämä kätevää esimerkiksi silloin, kun haluat linkittää nimikekortin toimittajan nimikeluetteloon.</span><span class="sxs-lookup"><span data-stu-id="11718-140">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="11718-141">Seuraava toimenpide perustuu nimikekorttiin.</span><span class="sxs-lookup"><span data-stu-id="11718-141">The following procedure is based on an item card.</span></span> <span data-ttu-id="11718-142">Vaiheet ovat samanlaiset kaikissa tuetuissa korteissa ja asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="11718-142">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="11718-143">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="11718-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="11718-144">Valitse nimike, josta haluat lisätä linkin, ja valitse sitten tietoruudussa **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="11718-144">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="11718-145">Valitse **Linkit**-kohdassa **+**-kuvake.</span><span class="sxs-lookup"><span data-stu-id="11718-145">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="11718-146">Anna linkki **Linkin osoite** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="11718-146">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="11718-147">Linkin on oltava kelvollinen Internet- tai intranet-osoite.</span><span class="sxs-lookup"><span data-stu-id="11718-147">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="11718-148">Kirjoita **Kuvaus**-kenttään linkkiä koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="11718-148">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="11718-149">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="11718-149">Choose the **OK** button.</span></span>

<span data-ttu-id="11718-150">Linkki on nyt liitetty nimikekorttiin.</span><span class="sxs-lookup"><span data-stu-id="11718-150">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="11718-151">Muistion kirjoittaminen myyntitilaukseen</span><span class="sxs-lookup"><span data-stu-id="11718-151">To write a note on a sales order</span></span>
<span data-ttu-id="11718-152">Voit kirjoittaa asiakirjaan tai korttiin muistion, jossa on esimerkiksi ohjeita muille asiakirjan tai kortin käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="11718-152">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="11718-153">Voit sisällyttää muistioihin tiedostolinkkejä ja URL-osoitteita.</span><span class="sxs-lookup"><span data-stu-id="11718-153">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="11718-154">**Liitteet**-välilehdessä olevat muistiot eivät liity sisäiseen muistiotoimintoon, jota käytetään lähinnä työnkulujen käyttäjien keskinäiseen viestintään.</span><span class="sxs-lookup"><span data-stu-id="11718-154">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="11718-155">Lisätietoja on kohdassa [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="11718-155">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="11718-156">Seuraava toimenpide perustuu myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="11718-156">The following procedure is based on a sales order.</span></span> <span data-ttu-id="11718-157">Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.</span><span class="sxs-lookup"><span data-stu-id="11718-157">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="11718-158">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="11718-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="11718-159">Valitse myyntitilaus, johon haluat kirjoittaa muistion, ja valitse sitten tietoruudussa **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="11718-159">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="11718-160">Valitse **Muistiot**-osassa **+**-kuvake.</span><span class="sxs-lookup"><span data-stu-id="11718-160">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="11718-161">Kirjoita **Huomautus**-kenttään tekstiä, kuten Tämä on kiireellinen tilaus.</span><span class="sxs-lookup"><span data-stu-id="11718-161">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="11718-162">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="11718-162">Choose the **OK** button.</span></span>

<span data-ttu-id="11718-163">Huomautus on nyt liitetty myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="11718-163">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="11718-164">Katso myös</span><span class="sxs-lookup"><span data-stu-id="11718-164">See Also</span></span>  
<span data-ttu-id="11718-165">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="11718-165">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="11718-166">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="11718-166">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="11718-167">Työnkulkuilmoitusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="11718-167">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]