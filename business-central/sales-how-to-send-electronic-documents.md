---
title: "Sähköisten tiedostojen lähettäminen | Microsoft Docs"
description: "Lisätietoja laskujen lähettämisestä sähköisesti."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: eac3422bade7b77ee0847d6a0f47fbcb4d41988a
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="send-electronic-documents"></a><span data-ttu-id="75c50-103">Sähköisten asiakirjojen lähettäminen</span><span class="sxs-lookup"><span data-stu-id="75c50-103">Send Electronic Documents</span></span>
<span data-ttu-id="75c50-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleinen versio tukee sähköisten laskujen ja hyvityslaskujen lähettämistä PEPPOL-muodossa. Suurimmat document exchange -palveluiden tarjoajat tukevat tätä muotoa.</span><span class="sxs-lookup"><span data-stu-id="75c50-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="75c50-105">Document exchange -palveluiden tarjoaja välittää sähköisiä asiakirjoja liikekumppaneiden välillä.</span><span class="sxs-lookup"><span data-stu-id="75c50-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="75c50-106">Käyttämällä tiedonsiirtokehystä voidaan tukea myös muita sähköisiä asiakirjamuotoja.</span><span class="sxs-lookup"><span data-stu-id="75c50-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="75c50-107">Document exchange -palvelu on esimääritetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleisessä versiossa, ja se on valmis määritettäväksi yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="75c50-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="75c50-108">Lisätietoja on kohdassa [Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="75c50-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="75c50-109">Jos haluat lähettää myyntilaskun sähköisenä PEPPOL-asiakirjana, valitse **Sähköinen asiakirja** -vaihtoehto **Kirjaa ja lähetä** -valintaikkunassa. Samassa valintaikkunassa voit määrittää sähköisen lähettämisen asiakkaan asiakirjojen oletuslähetysprofiiliksi.</span><span class="sxs-lookup"><span data-stu-id="75c50-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="75c50-110">Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt.</span><span class="sxs-lookup"><span data-stu-id="75c50-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="75c50-111">Näitä käytetään liiketoimintakumppanien ja nimikkeiden tunnistamiseen, kun kenttien tietoja muutetaan. Lisätietoja on kohdassa [Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="75c50-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="75c50-112">Sähköisen myyntilaskun lähettäminen</span><span class="sxs-lookup"><span data-stu-id="75c50-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="75c50-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="75c50-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="75c50-114">Luo uusi myyntilasku.</span><span class="sxs-lookup"><span data-stu-id="75c50-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="75c50-115">Kun myyntilasku on laskutusvalmis, valitse **Toiminnot**-välilehden **Kirjaaminen**-ryhmästä **Kirjaa ja lähetä**.</span><span class="sxs-lookup"><span data-stu-id="75c50-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="75c50-116">Jos asiakkaan oletuslähetysprofiili on **Sähköinen asiakirja**, tieto näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Lasku kirjataan ja lähetetään sähköisesti valitussa muodossa, kun valitset **Kyllä**-painikkeen.</span><span class="sxs-lookup"><span data-stu-id="75c50-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="75c50-117">Valitse **Kirjaa ja lähetä vahvistus** -valintaikkunassa **Lähetä asiakirja vastaanottajalle** -kentän oikealla puolella oleva MuokkausApu-painike.</span><span class="sxs-lookup"><span data-stu-id="75c50-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="75c50-118">Valitse **Lähetä asiakirja kohteeseen** -valintaikkunassa **Sähköinen asiakirja** -kentässä **Document Exchange -palvelun kautta**.</span><span class="sxs-lookup"><span data-stu-id="75c50-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="75c50-119">Valitse **Muoto**-kentässä **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="75c50-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="75c50-120">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="75c50-120">Choose the **OK** button.</span></span> <span data-ttu-id="75c50-121">**Kirjaa ja lähetä vahvistus** -valintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="75c50-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="75c50-122">**Sähköinen asiakirja (PEPPOL)** lisätään **Lähetä asiakirja kohteeseen** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75c50-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="75c50-123">Valitse **Kyllä**-painike.</span><span class="sxs-lookup"><span data-stu-id="75c50-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="75c50-124">Myyntilasku kirjataan ja lähetetään asiakkaalle sähköisenä asiakirjana PEPPOL-muodossa.</span><span class="sxs-lookup"><span data-stu-id="75c50-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="75c50-125">Voit myös lähettää kirjatun myyntilaskun sähköisenä asiakirjana.</span><span class="sxs-lookup"><span data-stu-id="75c50-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="75c50-126">Menettely on sama kuin joka on kuvattu tässä aiheessa kirjaamattomille myyntiasiakirjoille.</span><span class="sxs-lookup"><span data-stu-id="75c50-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="75c50-127">**Kirjattu myyntilasku** -ikkunassa **Toiminnot** välilehdessä **Yleiset**-ryhmässä valitse **Toimintoloki**, kun haluat tarkastella sähköisen asiakirjan tilaa.</span><span class="sxs-lookup"><span data-stu-id="75c50-127">In the **Posted Sales Invoice** window, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="75c50-128">Lisätietoja on myös kohdassa **Toimintoloki**</span><span class="sxs-lookup"><span data-stu-id="75c50-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="75c50-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="75c50-129">See Also</span></span>  
[<span data-ttu-id="75c50-130">Myynnin laskutus</span><span class="sxs-lookup"><span data-stu-id="75c50-130">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="75c50-131">Asiakirjan lähetysprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="75c50-131">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="75c50-132">Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="75c50-132">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="75c50-133">Document Exchange -palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="75c50-133">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="75c50-134">Tietojenvaihtomääritysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="75c50-134">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="75c50-135">Sähköinen tiedonsiirto</span><span class="sxs-lookup"><span data-stu-id="75c50-135">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="75c50-136">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="75c50-136">General Business Functionality</span></span>](ui-across-business-areas.md)  

