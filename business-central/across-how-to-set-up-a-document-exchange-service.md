---
title: Document Exchange -palvelun määrittäminen | Microsoft Docs
description: Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0217f077c9c38603b9e3ff945fd47394c5b943bb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384372"
---
# <a name="set-up-a-document-exchange-service"></a><span data-ttu-id="bf364-103">Document Exchange -palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf364-103">Set Up a Document Exchange Service</span></span>
<span data-ttu-id="bf364-104">Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="bf364-104">You use an external service provider to exchange electronic documents with your trading partners.</span></span> <span data-ttu-id="bf364-105">Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="bf364-105">For more information, see [Exchanging Data Electronically](across-data-exchange.md).</span></span>  

## <a name="to-set-up-a-document-exchange-service"></a><span data-ttu-id="bf364-106">Document Exchange -palvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf364-106">To set up a document exchange service</span></span>  
1. <span data-ttu-id="bf364-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Document Exchange -palvelun asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="bf364-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Doc. Exch. Service Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bf364-108">Täytä kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="bf364-108">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="bf364-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="bf364-109">Field</span></span>|<span data-ttu-id="bf364-110">Description</span><span class="sxs-lookup"><span data-stu-id="bf364-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="bf364-111">**Käyttäjäagentti**</span><span class="sxs-lookup"><span data-stu-id="bf364-111">**User Agent**</span></span>|<span data-ttu-id="bf364-112">Anna teksti, jolla voidaan tunnistaa yrityksesi asiakirjan vaihtoprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="bf364-112">Enter any text that can be used to identify your company in document exchange processes.</span></span>|  
    |<span data-ttu-id="bf364-113">**Document Exchange -palvelun vuokraajatunnus**</span><span class="sxs-lookup"><span data-stu-id="bf364-113">**Doc. Exch. Tenant ID**</span></span>|<span data-ttu-id="bf364-114">Anna vuokraaja document exchange -palvelussa, joka edustaa yritystäsi.</span><span class="sxs-lookup"><span data-stu-id="bf364-114">Enter the tenant in the document exchange service that represents your company.</span></span> <span data-ttu-id="bf364-115">Document exchange -palvelun tarjoaja tarjoaa tämän.</span><span class="sxs-lookup"><span data-stu-id="bf364-115">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="bf364-116">**Käytössä**</span><span class="sxs-lookup"><span data-stu-id="bf364-116">**Enabled**</span></span>|<span data-ttu-id="bf364-117">Määritä, onko palvelu käytössä.</span><span class="sxs-lookup"><span data-stu-id="bf364-117">Specify if the service is enabled.</span></span> <span data-ttu-id="bf364-118">**Huomautus:** heti, kun palvelu otetaan käyttöön, ainakin kaksi työjonon tapahtumaa luodaan käsittelemään sähköisten asiakirjojen liikenne sisään ja ulos [!INCLUDE[prod_short](includes/prod_short.md)]:sta.</span><span class="sxs-lookup"><span data-stu-id="bf364-118">**Note:**  As soon as you enable the service, at least two job queue entries are created to process the traffic of electronic documents in and out of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="bf364-119">Kun palvelu poistetaan käytöstä, työjonon tapahtumat poistetaan.</span><span class="sxs-lookup"><span data-stu-id="bf364-119">When you disable the service, the job queue entries are deleted.</span></span>|  
    |<span data-ttu-id="bf364-120">**Rekisteröinnin URL-osoite**</span><span class="sxs-lookup"><span data-stu-id="bf364-120">**Signup URL**</span></span>|<span data-ttu-id="bf364-121">Määritä verkkosivu, jossa document exchange -palvelu rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="bf364-121">Specify the web page where you sign up for the document exchange service.</span></span>|  
    |<span data-ttu-id="bf364-122">**Palvelun URL-osoite**</span><span class="sxs-lookup"><span data-stu-id="bf364-122">**Service URL**</span></span>|<span data-ttu-id="bf364-123">Määritä sen document exchange -palvelun osoite, joka kutsutaan, kun lähetät ja vastaanotat sähköisiä asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="bf364-123">Specify the address of the document exchange service, which will be called when you send and receive electronic documents.</span></span>|  
    |<span data-ttu-id="bf364-124">**Sisäänkirjautumisen osoite**</span><span class="sxs-lookup"><span data-stu-id="bf364-124">**Login URL**</span></span>|<span data-ttu-id="bf364-125">Määritä document exchange -palvelun kirjautumissivu, johon kirjoitat yrityksesi käyttäjänimen ja salasanan kirjautuessasi palveluun.</span><span class="sxs-lookup"><span data-stu-id="bf364-125">Specify the logon page for the document exchange service, which is where you enter your company’s user name and password to log on to the service.</span></span>|  
    |<span data-ttu-id="bf364-126">**Kuluttajan avain**</span><span class="sxs-lookup"><span data-stu-id="bf364-126">**Consumer Key**</span></span>|<span data-ttu-id="bf364-127">Anna kolmen osapuolen OAuth-avain kuluttaja-avaimelle.</span><span class="sxs-lookup"><span data-stu-id="bf364-127">Enter the 3-legged OAuth key for the consumer key.</span></span> <span data-ttu-id="bf364-128">Document exchange -palvelun tarjoaja tarjoaa tämän.</span><span class="sxs-lookup"><span data-stu-id="bf364-128">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="bf364-129">**Kuluttajan salainen avain**</span><span class="sxs-lookup"><span data-stu-id="bf364-129">**Consumer Secret**</span></span>|<span data-ttu-id="bf364-130">Anna piilokoodi, joka suojaa kuluttaja-avainta.</span><span class="sxs-lookup"><span data-stu-id="bf364-130">Enter the secret that protects the consumer key.</span></span> <span data-ttu-id="bf364-131">Saat sen Document exchange -palveluntarjoajalta.</span><span class="sxs-lookup"><span data-stu-id="bf364-131">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="bf364-132">**Tunnus**</span><span class="sxs-lookup"><span data-stu-id="bf364-132">**Token**</span></span>|<span data-ttu-id="bf364-133">Anna kolmen osapuolen OAuth-avain tunnukselle.</span><span class="sxs-lookup"><span data-stu-id="bf364-133">Enter the 3-legged OAuth key for the token.</span></span> <span data-ttu-id="bf364-134">Saat sen Document exchange -palveluntarjoajalta.</span><span class="sxs-lookup"><span data-stu-id="bf364-134">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="bf364-135">**Tunnuksen salainen avain**</span><span class="sxs-lookup"><span data-stu-id="bf364-135">**Token Secret**</span></span>|<span data-ttu-id="bf364-136">Anna piilokoodi, joka suojaa tunnusta.</span><span class="sxs-lookup"><span data-stu-id="bf364-136">Enter the secret that protects the token.</span></span> <span data-ttu-id="bf364-137">Saat sen Document exchange -palveluntarjoajalta.</span><span class="sxs-lookup"><span data-stu-id="bf364-137">This is provided by the document exchange service provider.</span></span>|  

    > [!NOTE]  
    > <span data-ttu-id="bf364-138">Sisäänkirjaustiedot salataan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="bf364-138">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf364-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="bf364-139">See Also</span></span>  
[<span data-ttu-id="bf364-140">Tiedonsiirron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf364-140">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)  
[<span data-ttu-id="bf364-141">Sähköinen tiedonsiirto</span><span class="sxs-lookup"><span data-stu-id="bf364-141">Exchanging Data Electronically</span></span>](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]