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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 84d58193fa7ee272b372403d63702348fbfb1f77
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315274"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="5909e-103">Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="5909e-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="5909e-104">Voit liittää useimpien korttien ja asiakirjojen tietoruudussa tiedostoja, lisätä linkkejä ja kirjoittaa muistioita.</span><span class="sxs-lookup"><span data-stu-id="5909e-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="5909e-105">Linkkejä ja muistioita voi kirjoittaa myös luettelosivulla sen jälkeen, kun olet valinnut liittyvän rivin.</span><span class="sxs-lookup"><span data-stu-id="5909e-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="5909e-106">Jos haluat tarkastella tai muuttaa näitä liitettyjä tietotyyppejä, sinun on avattava ensin tietoruudun **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5909e-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="5909e-107">Välilehden otsikon takana oleva luku ilmaisee, kuinka monta liitettyä tiedostoa, linkkiä tai muistiinpanoa kortissa tai asiakirjassa on.</span><span class="sxs-lookup"><span data-stu-id="5909e-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="5909e-108">Liitteet, linkit ja muistiot pysyvät liitteinä, kun korttia tai asiakirjaa käsitellään muihin tiloihin, kuten siirtyminen jatkuvasta myyntitilauksesta kirjattuun myyntilaskuun.</span><span class="sxs-lookup"><span data-stu-id="5909e-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="5909e-109">Huomaa kuitenkin, että järjestelmä ei käsittele mitään liitetyyppiä esimerkiksi tulostettaessa tai tallennettaessa tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="5909e-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="5909e-110">Tiedoston liittäminen ostolaskuun</span><span class="sxs-lookup"><span data-stu-id="5909e-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="5909e-111">Korttiin tai asiakirjaan liitettävän tiedoston tyypillä ei ole merkitystä, ja se voi sisältää tekstiä, kuvan tai videon.</span><span class="sxs-lookup"><span data-stu-id="5909e-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="5909e-112">Tämä on kätevää esimerkiksi silloin, kun haluat tallentaa toimittajan laskun PDF-tiedostona liittyvään [!INCLUDE[d365fin](includes/d365fin_md.md)]in ostolaskuun.</span><span class="sxs-lookup"><span data-stu-id="5909e-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="5909e-113">Saapuvat asiakirjat -ominaisuudella liitetyt tiedostot eivät sisälly **Liitteet**-välilehteen. Lisätietoja on kohdassa [Saapuvat asiakirjat](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="5909e-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="5909e-114">Seuraava toimenpide perustuu myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="5909e-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="5909e-115">Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.</span><span class="sxs-lookup"><span data-stu-id="5909e-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="5909e-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5909e-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="5909e-117">Avaa myyntitilaus, johon haluat liittää tiedoston.</span><span class="sxs-lookup"><span data-stu-id="5909e-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="5909e-118">Avaa **Liitteet**-välilehti tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="5909e-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="5909e-119">Valitse **Asiakirjat**-kentässä arvo, kuten 0.</span><span class="sxs-lookup"><span data-stu-id="5909e-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="5909e-120">Valitse **Liitetyt asiakirjat** -sivun **Liite**-kentässä **Valitse tiedosto** -painike.</span><span class="sxs-lookup"><span data-stu-id="5909e-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="5909e-121">Valitse tiedosto haluamastasi sijainnista ja valitse sitten **Avaa**-painike.</span><span class="sxs-lookup"><span data-stu-id="5909e-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="5909e-122">Tiedosto on nyt liitetty ostolaskuun.</span><span class="sxs-lookup"><span data-stu-id="5909e-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="5909e-123">Linkin lisääminen nimikekortista</span><span class="sxs-lookup"><span data-stu-id="5909e-123">To add a link from an item card</span></span>
<span data-ttu-id="5909e-124">Voit lisätä kortista tai asiakirjasta linkin mihin tahansa URL-osoitteeseen tai polkuun.</span><span class="sxs-lookup"><span data-stu-id="5909e-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="5909e-125">Tämä kätevää esimerkiksi silloin, kun haluat linkittää nimikekortin toimittajan nimikeluetteloon.</span><span class="sxs-lookup"><span data-stu-id="5909e-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="5909e-126">Seuraava toimenpide perustuu nimikekorttiin.</span><span class="sxs-lookup"><span data-stu-id="5909e-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="5909e-127">Vaiheet ovat samanlaiset kaikissa tuetuissa korteissa ja asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="5909e-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="5909e-128">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5909e-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="5909e-129">Valitse nimike, josta haluat lisätä linkin, ja valitse sitten tietoruudussa **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5909e-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="5909e-130">Valitse **Linkit**-kohdassa **+**-kuvake.</span><span class="sxs-lookup"><span data-stu-id="5909e-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="5909e-131">Anna linkki **Linkin osoite** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="5909e-131">In the **Link Address** field, enter the link.</span></span>

    - <span data-ttu-id="5909e-132">Jos haluat linkittää tietokoneessa tai verkossa olevan tiedoston, anna tiedostopolun ja tiedoston koko nimi, kuten **C:\Omat tiedostot\lasku1.doc**.</span><span class="sxs-lookup"><span data-stu-id="5909e-132">To link to a file on your computer or network, enter the full path and file name, such as **C:\My Documents\invoice1.doc**.</span></span>
    - <span data-ttu-id="5909e-133">Luo linkki sivustoon antamalla verkko- eli URL-osoite, kuten **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="5909e-133">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    - <span data-ttu-id="5909e-134">Luo linkki ohjelmaan antamalla ohjelmaan avaava merkkijono.</span><span class="sxs-lookup"><span data-stu-id="5909e-134">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="5909e-135">Jos haluat esimerkiksi että uusi tyhjä, tietylle sähköpostitunnukselle osoitettu Outlook-sähköpostiviesti avautuu, anna **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="5909e-135">For example, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5. <span data-ttu-id="5909e-136">Kirjoita **Kuvaus**-kenttään linkkiä koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="5909e-136">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="5909e-137">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="5909e-137">Choose the **OK** button.</span></span>

<span data-ttu-id="5909e-138">Linkki on nyt liitetty nimikekorttiin.</span><span class="sxs-lookup"><span data-stu-id="5909e-138">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="5909e-139">Muistion kirjoittaminen myyntitilaukseen</span><span class="sxs-lookup"><span data-stu-id="5909e-139">To write a note on a sales order</span></span>
<span data-ttu-id="5909e-140">Voit kirjoittaa asiakirjaan tai korttiin muistion, jossa on esimerkiksi ohjeita muille asiakirjan tai kortin käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="5909e-140">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="5909e-141">Voit sisällyttää muistioihin tiedostolinkkejä ja URL-osoitteita.</span><span class="sxs-lookup"><span data-stu-id="5909e-141">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="5909e-142">**Liitteet**-välilehdessä olevat muistiot eivät liity sisäiseen muistiotoimintoon, jota käytetään lähinnä työnkulujen käyttäjien keskinäiseen viestintään.</span><span class="sxs-lookup"><span data-stu-id="5909e-142">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="5909e-143">Lisätietoja on kohdassa [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="5909e-143">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="5909e-144">Seuraava toimenpide perustuu myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="5909e-144">The following procedure is based on a sales order.</span></span> <span data-ttu-id="5909e-145">Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.</span><span class="sxs-lookup"><span data-stu-id="5909e-145">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="5909e-146">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5909e-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5909e-147">Valitse myyntitilaus, johon haluat kirjoittaa muistion, ja valitse sitten tietoruudussa **Liitteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5909e-147">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="5909e-148">Valitse **Muistiot**-osassa **+**-kuvake.</span><span class="sxs-lookup"><span data-stu-id="5909e-148">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="5909e-149">Kirjoita **Huomautus**-kenttään tekstiä, kuten Tämä on kiireellinen tilaus.</span><span class="sxs-lookup"><span data-stu-id="5909e-149">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="5909e-150">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="5909e-150">Choose the **OK** button.</span></span>

<span data-ttu-id="5909e-151">Huomautus on nyt liitetty myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="5909e-151">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="5909e-152">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5909e-152">See Also</span></span>  
<span data-ttu-id="5909e-153">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5909e-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5909e-154">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="5909e-154">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="5909e-155">Työnkulkuilmoitusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5909e-155">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
