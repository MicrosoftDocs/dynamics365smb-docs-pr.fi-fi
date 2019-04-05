---
title: Saapuvien asiakirjojen määrittäminen| Microsoft Docs
description: Voit käyttää saapuvien asiakirjojen toimintoa sähköisten asiakirjojen luomiseen, OCR-tehtävien hallintaan, laskujen tuontiin ja kuvatiedostojen muuntamiseen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 6072dcf536211ddad76c6423421033dd43f534b0
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795106"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="4cf28-103">Määritä saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="4cf28-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="4cf28-104">Jos luot pääkirjan rivejä saapuvista asiakirjatietueista, **Saapuvien asiakirjojen asetukset** -sivulla on määritettävä käytettävä päiväkirjan malli sekä erä.</span><span class="sxs-lookup"><span data-stu-id="4cf28-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="4cf28-105">Jos haluat, etteivät käyttäjät voi luoda laskuja tai yleisen päiväkirjan rivejä saapuvista asiakirjatietueista ennen asiakirjojen hyväksymistä, määritä hyväksyjät **Saapuvan asiakirjan hyväksyjät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4cf28-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers on the **Incoming Document Approvers** page.</span></span>

<span data-ttu-id="4cf28-106">Jos haluat muuntaa PDF- ja kuvatiedostoja sähköisiksi asiakirjoiksi, jotka voi muuntaa esimerkiksi ostolaskuiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, määritä ensin OCR-ominaisuus ja ota palvelu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4cf28-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="4cf28-107">Kun Saapuvat asiakirjat -ominaisuus on määritetty, voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille.</span><span class="sxs-lookup"><span data-stu-id="4cf28-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="4cf28-108">Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.</span><span class="sxs-lookup"><span data-stu-id="4cf28-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="4cf28-109">Lisätietoja on kohdassa [Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="4cf28-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="4cf28-110">Saapuvat asiakirjat -ominaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4cf28-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="4cf28-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvien asiakirjojen asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4cf28-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="4cf28-112">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="4cf28-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="4cf28-113">Saapuvien asiakirjatietueiden hyväksyjien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4cf28-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="4cf28-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvien asiakirjojen asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4cf28-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4cf28-115">Valitse **Saapuvien asiakirjojen asetukset** -sivulla **Hyväksyjät**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4cf28-115">On the **Incoming Documents Setup** page, choose the **Approvers** action.</span></span>

    <span data-ttu-id="4cf28-116">Kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]iin rekisteröityneet käyttäjät näkyvät **Saapuvan asiakirjan hyväksyjät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4cf28-116">The **Incoming Document Approvers** page shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="4cf28-117">Valitse vähintään yksi käyttäjä, joka voi hyväksyä saapuvan asiakirjan ennen liittyvän asiakirjan tai päiväkirjarivin luomista.</span><span class="sxs-lookup"><span data-stu-id="4cf28-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="4cf28-118">Kun hyväksyjät on määritetty **Saapuvien asiakirjojen hyväksyjät** -sivulla, vain kyseiset käyttäjät voivat hyväksyä saapuvan asiakirjan, jos **Saapuvien asiakirjojen asetukset** -sivun **Edellytä hyväksyntää luomista varten** -valintaruutu on valittu.</span><span class="sxs-lookup"><span data-stu-id="4cf28-118">When approvers have been set up on the **Incoming Document Approvers** page, only those users can approve an incoming document if the **Require Approval To Create** check box on the **Incoming Documents Setup** page is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4cf28-119">Nämä hyväksynnän asetukset eivät liity hyväksymistyönkulkuihin.</span><span class="sxs-lookup"><span data-stu-id="4cf28-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="4cf28-120">Lisätietoja on kohdassa [Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="4cf28-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="4cf28-121">OCR-palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4cf28-121">To set up an OCR service</span></span>
1. <span data-ttu-id="4cf28-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **OCR-palvelun asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4cf28-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="4cf28-123">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="4cf28-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="4cf28-124">Sisäänkirjaustiedot salataan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4cf28-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cf28-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4cf28-125">See Also</span></span>
[<span data-ttu-id="4cf28-126">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="4cf28-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="4cf28-127">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="4cf28-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="4cf28-128">Osto</span><span class="sxs-lookup"><span data-stu-id="4cf28-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4cf28-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4cf28-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
