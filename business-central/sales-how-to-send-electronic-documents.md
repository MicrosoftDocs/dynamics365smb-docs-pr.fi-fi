---
title: Sähköisten tiedostojen lähettäminen | Microsoft Docs
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
ms.openlocfilehash: 8875cdcc7ad13f72c9cf131061b301dac1dcff2b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910578"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="12f36-103">Sähköisten asiakirjojen lähettäminen</span><span class="sxs-lookup"><span data-stu-id="12f36-103">Send Electronic Documents</span></span>
<span data-ttu-id="12f36-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleinen versio tukee sähköisten laskujen ja hyvityslaskujen lähettämistä PEPPOL-muodossa. Suurimmat document exchange -palveluiden tarjoajat tukevat tätä muotoa.</span><span class="sxs-lookup"><span data-stu-id="12f36-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="12f36-105">Document exchange -palveluiden tarjoaja välittää sähköisiä asiakirjoja liikekumppaneiden välillä.</span><span class="sxs-lookup"><span data-stu-id="12f36-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="12f36-106">Käyttämällä tiedonsiirtokehystä voidaan tukea myös muita sähköisiä asiakirjamuotoja.</span><span class="sxs-lookup"><span data-stu-id="12f36-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="12f36-107">Document exchange -palvelu on esimääritetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleisessä versiossa, ja se on valmis määritettäväksi yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="12f36-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="12f36-108">Lisätietoja on kohdassa [Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="12f36-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="12f36-109">Jos haluat lähettää myyntilaskun sähköisenä PEPPOL-asiakirjana, valitse **Sähköinen asiakirja** -vaihtoehto **Kirjaa ja lähetä** -valintaikkunassa. Samassa valintaikkunassa voit määrittää sähköisen lähettämisen asiakkaan asiakirjojen oletuslähetysprofiiliksi.</span><span class="sxs-lookup"><span data-stu-id="12f36-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="12f36-110">Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt.</span><span class="sxs-lookup"><span data-stu-id="12f36-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="12f36-111">Näitä käytetään liiketoimintakumppanien ja nimikkeiden tunnistamiseen, kun kenttien tietoja muutetaan. Lisätietoja on kohdassa [Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="12f36-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="12f36-112">Sähköisen myyntilaskun lähettäminen</span><span class="sxs-lookup"><span data-stu-id="12f36-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="12f36-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="12f36-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="12f36-114">Luo uusi myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="12f36-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="12f36-115">Kun myyntilasku on valmis laskutettavaksi, valitse **Kirjaa ja lähetä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="12f36-115">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="12f36-116">Jos asiakkaan oletuslähetysprofiili on **Sähköinen asiakirja**, tieto näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Lasku kirjataan ja lähetetään sähköisesti valitussa muodossa, kun valitset **Kyllä**-painikkeen.</span><span class="sxs-lookup"><span data-stu-id="12f36-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="12f36-117">Valitse **Kirjaa ja lähetä vahvistus** -valintaikkunassa **Lähetä asiakirja vastaanottajalle** -kentän oikealla puolella oleva MuokkausApu-painike.</span><span class="sxs-lookup"><span data-stu-id="12f36-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="12f36-118">Valitse **Lähetä asiakirja kohteeseen** -valintaikkunassa **Sähköinen asiakirja** -kentässä **Document Exchange -palvelun kautta**.</span><span class="sxs-lookup"><span data-stu-id="12f36-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="12f36-119">Valitse **Muoto**-kentässä **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="12f36-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="12f36-120">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="12f36-120">Choose the **OK** button.</span></span> <span data-ttu-id="12f36-121">**Kirjaa ja lähetä vahvistus** -valintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="12f36-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="12f36-122">**Sähköinen asiakirja (PEPPOL)** lisätään **Lähetä asiakirja kohteeseen** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="12f36-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="12f36-123">Valitse **Kyllä**-painike.</span><span class="sxs-lookup"><span data-stu-id="12f36-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="12f36-124">Myyntilasku kirjataan ja lähetetään asiakkaalle sähköisenä asiakirjana PEPPOL-muodossa.</span><span class="sxs-lookup"><span data-stu-id="12f36-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="12f36-125">Voit myös lähettää kirjatun myyntilaskun sähköisenä asiakirjana.</span><span class="sxs-lookup"><span data-stu-id="12f36-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="12f36-126">Menettely on sama kuin joka on kuvattu tässä aiheessa kirjaamattomille myyntiasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="12f36-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="12f36-127">Valitse **Kirjattu myyntilasku** -sivun **Toimintoloki**-toiminto, kun haluat tarkastella sähköisen asiakirjan tilaa.</span><span class="sxs-lookup"><span data-stu-id="12f36-127">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span> <span data-ttu-id="12f36-128">Lisätietoja on myös kohdassa **Toimintoloki**</span><span class="sxs-lookup"><span data-stu-id="12f36-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="12f36-129">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="12f36-129">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="12f36-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="12f36-130">See Also</span></span>  
[<span data-ttu-id="12f36-131">Myynnin laskutus</span><span class="sxs-lookup"><span data-stu-id="12f36-131">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="12f36-132">Asiakirjan lähetysprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="12f36-132">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="12f36-133">Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="12f36-133">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="12f36-134">Document Exchange -palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="12f36-134">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="12f36-135">Tietojenvaihtomääritysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="12f36-135">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="12f36-136">Sähköinen tiedonsiirto</span><span class="sxs-lookup"><span data-stu-id="12f36-136">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="12f36-137">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="12f36-137">General Business Functionality</span></span>](ui-across-business-areas.md)  
