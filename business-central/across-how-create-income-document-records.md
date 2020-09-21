---
title: Tietueiden luominen saapuvista asiakirjoista| Microsoft Docs
description: Voit luoda tietueita saapuvista asiakirjoista, kuten sähköisistä laskuista, ja hallita OCR-tehtäviä, sähköistä kaupankäyntiä ja asiakirjojen vaihtopalvelua.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 163b352e55ca85644bc833093f39ea8c422e5030
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780583"
---
# <a name="create-incoming-document-records"></a><span data-ttu-id="62e69-103">Saapuvien asiakirjatietueiden luominen</span><span class="sxs-lookup"><span data-stu-id="62e69-103">Create Incoming Document Records</span></span>
<span data-ttu-id="62e69-104">**Saapuvat asiakirjat** -sivulla voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille.</span><span class="sxs-lookup"><span data-stu-id="62e69-104">On the **Incoming Documents** page, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="62e69-105">Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.</span><span class="sxs-lookup"><span data-stu-id="62e69-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="62e69-106">Voit tallentaa ulkoisen asiakirjan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa luomalla tai suorittamalla ensin saapuvan tiedostotietueen.</span><span class="sxs-lookup"><span data-stu-id="62e69-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="62e69-107">Voit tehdä tämän manuaalisesti tai ottaa valokuvan ulkoisesta asiakirjasta ja luoda sitten saapuva asiakirjatietue, johon on liitetty kuvatiedosto.</span><span class="sxs-lookup"><span data-stu-id="62e69-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="62e69-108">Ennen kuin voit käyttää Saapuvat asiakirjat -ominaisuutta, sinun on tehtävä tarvittavat asetukset.</span><span class="sxs-lookup"><span data-stu-id="62e69-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="62e69-109">Lisätietoja on kohdassa [Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="62e69-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="62e69-110">Saapuvan asiakirjan hyväksyminen tai hylkääminen</span><span class="sxs-lookup"><span data-stu-id="62e69-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="62e69-111">Jos haluat, että käyttäjät voivat luoda laskuja tai yleisen päiväkirjan rivejä saapuvista asiakirjatietueista vasta, kun ne on hyväksytty, voit määrittää hyväksyjät, joiden on hyväksyttävä tietueet ennen niiden käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="62e69-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="62e69-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Saapuvat asiakirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="62e69-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="62e69-113">Valitse rivi, jolla hyväksyttävä tai hylättävä asiakirja on, ja valitse sitten **Hyväksy**- tai **Hylkää**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="62e69-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="62e69-114">Jos hyväksyt saapuvan asiakirjatietueen, saapuvan asiakirjan rivin **Vapautettu**-valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="62e69-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="62e69-115">Esimerkiksi ostolaskujen luonnista vastaava henkilö voi nyt aloittaa tietueen käsittelemisen.</span><span class="sxs-lookup"><span data-stu-id="62e69-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="62e69-116">Saapuvien asiakirjatietueiden luominen valokuva ottamalla</span><span class="sxs-lookup"><span data-stu-id="62e69-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="62e69-117">Seuraavat toimet koskevat vain [!INCLUDE[d365fin](includes/d365fin_md.md)]in tabletti- ja puhelinasiakasohjelmia.</span><span class="sxs-lookup"><span data-stu-id="62e69-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="62e69-118">Valitse sovellusriviltä **luo saapuva asiakirja kamerasta** ruutu ja siirry sitten vaiheeseen 4.</span><span class="sxs-lookup"><span data-stu-id="62e69-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="62e69-119">Voit myös valita sovellusrivin, valita asetukset-painikkeen, valita **saapuvat asiakirjat**, ja valita sitten **kaikki**.</span><span class="sxs-lookup"><span data-stu-id="62e69-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="62e69-120">Valitse **Saapuvat asiakirjat** -sivulla ellipsipainike ja valitse sitten **Luo kamerasta**.</span><span class="sxs-lookup"><span data-stu-id="62e69-120">On the **Incoming Documents** page, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="62e69-121">Tabletin tai puhelimen kamera ativoituu.</span><span class="sxs-lookup"><span data-stu-id="62e69-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="62e69-122">Ota valokuva asiakirjasta, kuten tavaran vastaanotto, jonka haluat käsitellä saapuvana asiakirjana,ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="62e69-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="62e69-123">Luo uuden saapuvan asiakirjan tietueen ja liittää kuvan.</span><span class="sxs-lookup"><span data-stu-id="62e69-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="62e69-124">Kuvan liittäminen saapuvien asiakirjatietueiden tietueeseen valokuva ottamalla</span><span class="sxs-lookup"><span data-stu-id="62e69-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="62e69-125">Seuraavat toimet koskevat vain [!INCLUDE[d365fin](includes/d365fin_md.md)]in tabletti- ja puhelinasiakasohjelmia.</span><span class="sxs-lookup"><span data-stu-id="62e69-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="62e69-126">Voit valita sovellusrivin, valita asetukset-painikkeen, valita **saapuvat asiakirjat**, ja valita sitten **kaikki**.</span><span class="sxs-lookup"><span data-stu-id="62e69-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="62e69-127">Avaa aiemmin luotu saapuvan asiakirjan tietue kortti.</span><span class="sxs-lookup"><span data-stu-id="62e69-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="62e69-128">Valitse **Saapuva asiakirja** -sivulla ellipsipainike ja valitse sitten **Liitä kuva kamerasta**.</span><span class="sxs-lookup"><span data-stu-id="62e69-128">On the **Incoming Document** page, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="62e69-129">Tabletin tai puhelimen kamera ativoituu.</span><span class="sxs-lookup"><span data-stu-id="62e69-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="62e69-130">Ota valokuva asiakirjasta, kuten tavaran vastaanotto, jonka haluat käsitellä saapuvana asiakirjana,ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="62e69-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="62e69-131">Kuva liitetään saapuvan asiakirjan tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="62e69-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="62e69-132">Saapuvan asiakirjatietueen luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="62e69-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="62e69-133">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Saapuvat asiakirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="62e69-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="62e69-134">Valitse **Luo tiedostosta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="62e69-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="62e69-135">**Lisää tiedosto** -sivulla valitse tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="62e69-135">On the **Insert File** page, select a file, and then choose **Open**.</span></span> <span data-ttu-id="62e69-136">Tiedosto liitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="62e69-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="62e69-137">Vaihtoehtoisesti voit valita **Uusi**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="62e69-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="62e69-138">Voit liittää tiedoston valitsemalla **Liitä tiedosto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="62e69-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="62e69-139">Valitse **Lisää tiedosto** -sivulla tiedosto, joka vastaa kyseistä saapuvaa asiakirjaa, ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="62e69-139">On the **Insert File** page, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="62e69-140">Täytä **Saapuva asiakirja** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="62e69-140">On the **Incoming Document** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="62e69-141">Katso myös</span><span class="sxs-lookup"><span data-stu-id="62e69-141">See Also</span></span>
[<span data-ttu-id="62e69-142">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="62e69-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="62e69-143">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="62e69-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="62e69-144">Osto</span><span class="sxs-lookup"><span data-stu-id="62e69-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="62e69-145">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="62e69-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
