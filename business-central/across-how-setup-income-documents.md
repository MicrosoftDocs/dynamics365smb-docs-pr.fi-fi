---
title: Saapuvien asiakirjojen määrittäminen| Microsoft Docs
description: Voit käyttää saapuvien asiakirjojen toimintoa sähköisten asiakirjojen luomiseen, OCR-tehtävien hallintaan, laskujen tuontiin ja kuvatiedostojen muuntamiseen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 00bfa89376a361bedc71ba76630906d761989ead
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384597"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="f7a36-103">Määritä saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="f7a36-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="f7a36-104">Jos luot pääkirjan rivejä saapuvista asiakirjatietueista, **Saapuvien asiakirjojen asetukset** -sivulla on määritettävä käytettävä päiväkirjan malli sekä erä.</span><span class="sxs-lookup"><span data-stu-id="f7a36-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="f7a36-105">Jos haluat, etteivät käyttäjät voi luoda laskuja tai yleisen päiväkirjan rivejä saapuvista asiakirjatietueista ennen asiakirjojen hyväksymistä, sinun on määritettävä työkulun hyväksyjät.</span><span class="sxs-lookup"><span data-stu-id="f7a36-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="f7a36-106">Jos haluat muuntaa PDF- ja kuvatiedostoja sähköisiksi asiakirjoiksi, jotka voi muuntaa esimerkiksi ostolaskuiksi [!INCLUDE[prod_short](includes/prod_short.md)]issa, määritä ensin OCR-ominaisuus ja ota palvelu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f7a36-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[prod_short](includes/prod_short.md)], you must first set up the OCR feature and enable the service.</span></span> <span data-ttu-id="f7a36-107">Valitse organisaatiolle ja/tai maalle/alueelle sopiva huoltopaketti.</span><span class="sxs-lookup"><span data-stu-id="f7a36-107">Choose a service package that is appropriate for your organization and/or country/region.</span></span> <span data-ttu-id="f7a36-108">Voit myös luoda tapahtumia manuaalisesti edustamaan ulkoisia asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="f7a36-108">Alternatively, you can create entries manually to represent the external documents.</span></span>  

<span data-ttu-id="f7a36-109">Kun Saapuvat asiakirjat -ominaisuus on määritetty, voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille.</span><span class="sxs-lookup"><span data-stu-id="f7a36-109">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="f7a36-110">Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.</span><span class="sxs-lookup"><span data-stu-id="f7a36-110">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="f7a36-111">Lisätietoja on kohdassa [Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="f7a36-111">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="f7a36-112">Saapuvat asiakirjat -ominaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f7a36-112">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="f7a36-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Saapuvien asiakirjojen asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f7a36-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f7a36-114">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f7a36-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="f7a36-115">Määritysten osan päätettävä, onko saapuville asiakirjoille pyydettävä hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="f7a36-115">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="f7a36-116">Hyväksynnän pyytämäistä varten on määritettävä hyväksyjät ja hyväksymistyönkulut.</span><span class="sxs-lookup"><span data-stu-id="f7a36-116">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="f7a36-117">Jos organisaation tarkoituksena ei ole edellyttää hyväksyntää, seuraavan osan voi ohittaa.</span><span class="sxs-lookup"><span data-stu-id="f7a36-117">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="f7a36-118">Jos saapuvien asiakirjojen PDF- tai kuvatiedostojen muuntamiseen käytetään palvelua, myös se on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="f7a36-118">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="f7a36-119">Muussa tapauksessa kyseisen osan voi ohittaa.</span><span class="sxs-lookup"><span data-stu-id="f7a36-119">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="f7a36-120">Saapuvien asiakirjatietueiden hyväksyjien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f7a36-120">To set up approvers of incoming document records</span></span>

<span data-ttu-id="f7a36-121">Vaihtoehtoisesti voit määrittää saapuvien asiakirjojen hyväksymisprosessin.</span><span class="sxs-lookup"><span data-stu-id="f7a36-121">Optionally, set up an approval process for the incoming documents.</span></span> <span data-ttu-id="f7a36-122">Saapuvien asiakirjojen hyväksyjät on määritettävä hyväksymistyönkulun käyttäjiksi.</span><span class="sxs-lookup"><span data-stu-id="f7a36-122">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="f7a36-123">Ennen kuin voit luoda työnkulkuja, joihin liittyy hyväksyntävaiheita, sinun on määritettävä hyväksymisprosesseihin osallistuvat työnkulun käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="f7a36-123">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="f7a36-124">Voit myös määrittää **Hyväksynnän käyttäjäasetukset** -sivulla rajoituksia tietynlaisille pyynnöille sekä korvaavia hyväksyjiä, jotka voivat hyväksyä pyyntöjä alkuperäisen hyväksyjän ollessa poissa.</span><span class="sxs-lookup"><span data-stu-id="f7a36-124">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="f7a36-125">Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="f7a36-125">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="f7a36-126">OCR-palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f7a36-126">To set up an OCR service</span></span>

1. <span data-ttu-id="f7a36-127">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **OCR-huollon asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f7a36-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f7a36-128">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f7a36-128">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="f7a36-129">Sisäänkirjaustiedot salataan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="f7a36-129">You login data is automatically encrypted.</span></span>

<span data-ttu-id="f7a36-130">Lisätietoja on kohdassa [PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="f7a36-130">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7a36-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f7a36-131">See Also</span></span>

[<span data-ttu-id="f7a36-132">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="f7a36-132">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="f7a36-133">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="f7a36-133">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="f7a36-134">Osto</span><span class="sxs-lookup"><span data-stu-id="f7a36-134">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f7a36-135">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7a36-135">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]