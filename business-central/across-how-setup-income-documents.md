---
title: Saapuvien asiakirjojen määrittäminen| Microsoft Docs
description: Voit käyttää saapuvien asiakirjojen toimintoa sähköisten asiakirjojen luomiseen, OCR-tehtävien hallintaan, laskujen tuontiin ja kuvatiedostojen muuntamiseen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/23/2020
ms.author: sgroespe
ms.openlocfilehash: 09047315c701bd2076f59b6c3f4840ba95eb06cc
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503542"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="d66f0-103">Määritä saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="d66f0-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="d66f0-104">Jos luot pääkirjan rivejä saapuvista asiakirjatietueista, **Saapuvien asiakirjojen asetukset** -sivulla on määritettävä käytettävä päiväkirjan malli sekä erä.</span><span class="sxs-lookup"><span data-stu-id="d66f0-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="d66f0-105">Jos haluat, etteivät käyttäjät voi luoda laskuja tai yleisen päiväkirjan rivejä saapuvista asiakirjatietueista ennen asiakirjojen hyväksymistä, sinun on määritettävä työkulun hyväksyjät.</span><span class="sxs-lookup"><span data-stu-id="d66f0-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="d66f0-106">Jos haluat muuntaa PDF- ja kuvatiedostoja sähköisiksi asiakirjoiksi, jotka voi muuntaa esimerkiksi ostolaskuiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, määritä ensin OCR-ominaisuus ja ota palvelu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d66f0-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="d66f0-107">Kun Saapuvat asiakirjat -ominaisuus on määritetty, voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille.</span><span class="sxs-lookup"><span data-stu-id="d66f0-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="d66f0-108">Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.</span><span class="sxs-lookup"><span data-stu-id="d66f0-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="d66f0-109">Lisätietoja on kohdassa [Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="d66f0-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="d66f0-110">Saapuvat asiakirjat -ominaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d66f0-110">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="d66f0-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Saapuvien asiakirjojen asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d66f0-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="d66f0-112">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="d66f0-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="d66f0-113">Määritysten osan päätettävä, onko saapuville asiakirjoille pyydettävä hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="d66f0-113">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="d66f0-114">Hyväksynnän pyytämäistä varten on määritettävä hyväksyjät ja hyväksymistyönkulut.</span><span class="sxs-lookup"><span data-stu-id="d66f0-114">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="d66f0-115">Jos organisaation tarkoituksena ei ole edellyttää hyväksyntää, seuraavan osan voi ohittaa.</span><span class="sxs-lookup"><span data-stu-id="d66f0-115">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="d66f0-116">Jos saapuvien asiakirjojen PDF- tai kuvatiedostojen muuntamiseen käytetään palvelua, myös se on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="d66f0-116">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="d66f0-117">Muussa tapauksessa kyseisen osan voi ohittaa.</span><span class="sxs-lookup"><span data-stu-id="d66f0-117">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="d66f0-118">Saapuvien asiakirjatietueiden hyväksyjien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d66f0-118">To set up approvers of incoming document records</span></span>

<span data-ttu-id="d66f0-119">Saapuvien asiakirjojen hyväksyjät on määritettävä hyväksymistyönkulun käyttäjiksi.</span><span class="sxs-lookup"><span data-stu-id="d66f0-119">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="d66f0-120">Ennen kuin voit luoda työnkulkuja, joihin liittyy hyväksyntävaiheita, sinun on määritettävä hyväksymisprosesseihin osallistuvat työnkulun käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="d66f0-120">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="d66f0-121">Voit myös määrittää **Hyväksynnän käyttäjäasetukset** -sivulla rajoituksia tietynlaisille pyynnöille sekä korvaavia hyväksyjiä, jotka voivat hyväksyä pyyntöjä alkuperäisen hyväksyjän ollessa poissa.</span><span class="sxs-lookup"><span data-stu-id="d66f0-121">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="d66f0-122">Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="d66f0-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="d66f0-123">OCR-palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d66f0-123">To set up an OCR service</span></span>

1. <span data-ttu-id="d66f0-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **OCR-huollon asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d66f0-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="d66f0-125">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="d66f0-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="d66f0-126">Sisäänkirjaustiedot salataan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d66f0-126">You login data is automatically encrypted.</span></span>

<span data-ttu-id="d66f0-127">Lisätietoja on kohdassa [PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="d66f0-127">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d66f0-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d66f0-128">See Also</span></span>

[<span data-ttu-id="d66f0-129">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="d66f0-129">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="d66f0-130">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="d66f0-130">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d66f0-131">Osto</span><span class="sxs-lookup"><span data-stu-id="d66f0-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d66f0-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d66f0-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
