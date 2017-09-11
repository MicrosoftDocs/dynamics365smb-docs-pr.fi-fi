---
title: "Saapuvien asiakirjojen määrittäminen| Microsoft Docs"
description: "Voit käyttää saapuvien asiakirjojen toimintoa sähköisten asiakirjojen luomiseen, OCR-tehtävien hallintaan, laskujen tuontiin ja kuvatiedostojen muuntamiseen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 69cb1037da2f3873ecb9a3f498ce5fadfeabac1d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-incoming-documents"></a><span data-ttu-id="43e0d-103">Toimintaohje: Saapuvien asiakirjojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43e0d-103">How to: Set Up Incoming Documents</span></span>
<span data-ttu-id="43e0d-104">Jos luot pääkirjan rivejä saapuvista asiakirjatietueista, **Saapuvien asiakirjojen asetukset** -ikkunassa on määritettävä käytettävä päiväkirjan malli sekä erä.</span><span class="sxs-lookup"><span data-stu-id="43e0d-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="43e0d-105">Jos haluat, etteivät käyttäjät voi luoda laskuja tai yleisen päiväkirjan rivejä saapuvista asiakirjatietueista ennen asiakirjojen hyväksymistä, määritä hyväksyjät **Saapuvan asiakirjan hyväksyjät** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="43e0d-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="43e0d-106">Jos haluat muuntaa PDF- ja kuvatiedostoja sähköisiksi asiakirjoiksi, jotka voi muuntaa esimerkiksi ostolaskuiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, määritä ensin OCR-ominaisuus ja ota palvelu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="43e0d-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="43e0d-107">Kun Saapuvat asiakirjat -ominaisuus on määritetty, voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille.</span><span class="sxs-lookup"><span data-stu-id="43e0d-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="43e0d-108">Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.</span><span class="sxs-lookup"><span data-stu-id="43e0d-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="43e0d-109">Lisätietoja on kohdassa [Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="43e0d-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="43e0d-110">Saapuvat asiakirjat -ominaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43e0d-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="43e0d-111">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Saapuvien asiakirjojen asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="43e0d-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="43e0d-112">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="43e0d-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="43e0d-113">Saapuvien asiakirjatietueiden hyväksyjien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43e0d-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="43e0d-114">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Saapuvien asiakirjojen asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="43e0d-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="43e0d-115">Valitse **Saapuvien asiakirjojen asetukset** -ikkunassa **Hyväksyjät**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="43e0d-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="43e0d-116">Kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]iin rekisteröityneet käyttäjät näkyvät **Saapuvan asiakirjan hyväksyjät** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="43e0d-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="43e0d-117">Valitse vähintään yksi käyttäjä, joka voi hyväksyä saapuvan asiakirjan ennen liittyvän asiakirjan tai päiväkirjarivin luomista.</span><span class="sxs-lookup"><span data-stu-id="43e0d-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="43e0d-118">Kun hyväksyjät on määritetty **Saapuvien asiakirjojen hyväksyjät** -ikkunassa, vain kyseiset käyttäjät voivat hyväksyä saapuvan asiakirjan, jos **Saapuvien asiakirjojen asetukset** -ikkunan **Edellytä hyväksyntää luomista varten** -valintaruutu on valittu.</span><span class="sxs-lookup"><span data-stu-id="43e0d-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="43e0d-119">Nämä hyväksynnän asetukset eivät liity hyväksymistyönkulkuihin.</span><span class="sxs-lookup"><span data-stu-id="43e0d-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="43e0d-120">Lisätietoja on kohdassa [Toimintaohje: Hyväksyntätyönkulkujen käyttäminen](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="43e0d-120">For more information, see [How to: Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="43e0d-121">OCR-palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43e0d-121">To set up an OCR service</span></span>
1. <span data-ttu-id="43e0d-122">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **OCR-palvelun asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="43e0d-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="43e0d-123">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="43e0d-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a><span data-ttu-id="43e0d-124">Kirjautumistietojen salaaminen</span><span class="sxs-lookup"><span data-stu-id="43e0d-124">To encrypt your login information</span></span>
<span data-ttu-id="43e0d-125">Suosittelemme, että suojaat **OCR-palvelun asetukset** -ikkunaan kirjoittamasi kirjautumistiedot.</span><span class="sxs-lookup"><span data-stu-id="43e0d-125">It is recommended that you protect the logon information that you enter in the **OCR Service Setup** window.</span></span> <span data-ttu-id="43e0d-126">Palvelimen tiedot voi salata luomalla uusia salausavaimia tai tuomalla olemassa olevia salausavaimia, jotka otetaan käyttöön tietokantayhteyden muodostavassa palvelininstanssissa.</span><span class="sxs-lookup"><span data-stu-id="43e0d-126">You can encrypt data on the server by generating new or importing existing encryption keys that you enable on the server instance that connects to the database.</span></span>

1. <span data-ttu-id="43e0d-127">Valitse **OCR-palvelun asetukset** -ikkunassa **Salauksen hallinta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="43e0d-127">In the **OCR Service Setup** window, choose the **Encryption Management** action.</span></span>
2. <span data-ttu-id="43e0d-128">Ota tietojen salaus käyttöön **Tietojen salauksen hallinta** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="43e0d-128">In the **Data Encryption Management** window, enable encryption of your data.</span></span>

## <a name="see-also"></a><span data-ttu-id="43e0d-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="43e0d-129">See Also</span></span>
[<span data-ttu-id="43e0d-130">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="43e0d-130">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="43e0d-131">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="43e0d-131">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="43e0d-132">Osto</span><span class="sxs-lookup"><span data-stu-id="43e0d-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="43e0d-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43e0d-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

