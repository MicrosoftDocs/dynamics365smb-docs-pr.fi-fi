---
title: Sähköisten asiakirjojen lähettäminen
description: Lisätietoja laskujen lähettämisestä sähköisesti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 43f61682a1068a8e1652fd28421f83d5291c8fe8
ms.sourcegitcommit: fe6943d410f5dca4e8b2986f95501009ae982d98
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/05/2021
ms.locfileid: "4827066"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="a88f0-103">Sähköisten asiakirjojen lähettäminen</span><span class="sxs-lookup"><span data-stu-id="a88f0-103">Send Electronic Documents</span></span>

<span data-ttu-id="a88f0-104">[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleinen versio tukee sähköisten laskujen ja hyvityslaskujen lähettämistä PEPPOL-muodossa. Suurimmat document exchange -palveluiden tarjoajat tukevat tätä muotoa.</span><span class="sxs-lookup"><span data-stu-id="a88f0-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="a88f0-105">Document exchange -palveluiden tarjoaja välittää sähköisiä asiakirjoja liikekumppaneiden välillä.</span><span class="sxs-lookup"><span data-stu-id="a88f0-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="a88f0-106">Käyttämällä tiedonsiirtokehystä voidaan tukea myös muita sähköisiä asiakirjamuotoja.</span><span class="sxs-lookup"><span data-stu-id="a88f0-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="a88f0-107">Document exchange -palvelu on esimääritetty [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleisessä versiossa, ja se on valmis määritettäväksi yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="a88f0-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="a88f0-108">Lisätietoja on kohdassa [Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="a88f0-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="a88f0-109">Joissakin tapauksissa sovellus on kuitenkin asennettava.</span><span class="sxs-lookup"><span data-stu-id="a88f0-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="a88f0-110">Lisätietoja on kohdassa [Sähköinen laskutus – usein kysytyt kysymykset](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="a88f0-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="a88f0-111">Lähettääksesi myyntilaskun sähköisenä PEPPOL-tiedostona voit valita **Sähköinen asiakirja** -vaihtoehdon **Kirjaa ja lähetä** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="a88f0-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="a88f0-112">Voit määrittää myös asiakkaan oletuslähettämisprofiilin kyseisessä valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="a88f0-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="a88f0-113">Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt.</span><span class="sxs-lookup"><span data-stu-id="a88f0-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="a88f0-114">Näitä käytetään liiketoimintakumppanien ja nimikkeiden tunnistamiseen, kun kenttien tietoja muutetaan. Lisätietoja on kohdassa [Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="a88f0-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="a88f0-115">Sähköisen myyntilaskun lähettäminen</span><span class="sxs-lookup"><span data-stu-id="a88f0-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="a88f0-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a88f0-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="a88f0-117">Luo uusi myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="a88f0-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="a88f0-118">Kun myyntilasku on valmis laskutettavaksi, valitse **Kirjaa ja lähetä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="a88f0-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="a88f0-119">Jos asiakkaan oletuslähetysprofiili on **Sähköinen asiakirja**, se näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="a88f0-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="a88f0-120">Tällä tavalla sinun tarvitsee vain valita **Kyllä**-painike kirjataksesi ja lähettääksesi laskun sähköisesti valitussa muodossa.</span><span class="sxs-lookup"><span data-stu-id="a88f0-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="a88f0-121">Valitse **Kirjaa ja lähetä vahvistus** -valintaikkunassa **Lähetä asiakirja vastaanottajalle** -kentän oikealla puolella oleva MuokkausApu-painike.</span><span class="sxs-lookup"><span data-stu-id="a88f0-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="a88f0-122">Valitse **Lähetä asiakirja kohteeseen** -valintaikkunassa **Sähköinen asiakirja** -kentässä **Document Exchange -palvelun kautta**.</span><span class="sxs-lookup"><span data-stu-id="a88f0-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="a88f0-123">Valitse **Muoto**-kentässä **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="a88f0-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="a88f0-124">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="a88f0-124">Choose the **OK** button.</span></span> <span data-ttu-id="a88f0-125">**Kirjaa ja lähetä vahvistus** -valintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="a88f0-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="a88f0-126">**Sähköinen asiakirja (PEPPOL)** lisätään **Lähetä asiakirja kohteeseen** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a88f0-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="a88f0-127">Valitse **Kyllä**-painike.</span><span class="sxs-lookup"><span data-stu-id="a88f0-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="a88f0-128">Myyntilasku kirjataan ja lähetetään asiakkaalle PEPPOL-muodossa.</span><span class="sxs-lookup"><span data-stu-id="a88f0-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a88f0-129">Voit myös lähettää kirjatun myyntilaskun sähköisenä asiakirjana.</span><span class="sxs-lookup"><span data-stu-id="a88f0-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="a88f0-130">Menettely on sama kuin joka on kuvattu tässä aiheessa kirjaamattomille myyntiasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="a88f0-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="a88f0-131">Valitse **Kirjattu myyntilasku** -sivun **Toimintoloki**-toiminto, kun haluat tarkastella sähköisen asiakirjan tilaa.</span><span class="sxs-lookup"><span data-stu-id="a88f0-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="a88f0-132">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="a88f0-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="a88f0-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a88f0-133">See Also</span></span>

[<span data-ttu-id="a88f0-134">Myynnin laskutus</span><span class="sxs-lookup"><span data-stu-id="a88f0-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="a88f0-135">Asiakirjan lähetysprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a88f0-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="a88f0-136">Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a88f0-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="a88f0-137">Document Exchange -palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a88f0-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="a88f0-138">Tietojenvaihtomääritysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a88f0-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="a88f0-139">Sähköinen tiedonsiirto</span><span class="sxs-lookup"><span data-stu-id="a88f0-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="a88f0-140">Sähköinen laskutus – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="a88f0-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="a88f0-141">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="a88f0-141">General Business Functionality</span></span>](ui-across-business-areas.md)  
