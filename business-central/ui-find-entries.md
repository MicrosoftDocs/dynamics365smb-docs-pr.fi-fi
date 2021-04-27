---
title: Tapahtumien etsiminen | Microsoft Docs
description: Tässä artikkelissa kuvataan, miten asiakirjoihin ja tapahtumiin liittyvät
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5f8ddd7176e69c9d1eb3b8d8ff98c93695d50993
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771159"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="96ae2-103">Liittyvien tapahtumien etsiminen kirjatuista asiakirjoista</span><span class="sxs-lookup"><span data-stu-id="96ae2-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="96ae2-104">Tässä artikkelissa opit etsimään toisiinsa liittyviä asiakirjoja ja tapahtumia yhteisten tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="96ae2-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="96ae2-105">Asiakirjan numero tai kirjauspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="96ae2-105">Document number or posting date</span></span>
- <span data-ttu-id="96ae2-106">Työyhteyshenkilön tyyppi, numero tai ulkoisen asiakirjan numero</span><span class="sxs-lookup"><span data-stu-id="96ae2-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="96ae2-107">Nimikkeen sarjanumero tai eränumero</span><span class="sxs-lookup"><span data-stu-id="96ae2-107">Item serial number or lot number</span></span>

<span data-ttu-id="96ae2-108">Tämä ominaisuus on hyödyllinen etsittäessä tietyistä tapahtumista syntyneitä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="96ae2-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="96ae2-109">Kun etsit asiakirjan numeroiden perusteella, voit myös tulostaa yhteenvedon Asiakirjatapahtumat-raportista.</span><span class="sxs-lookup"><span data-stu-id="96ae2-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="96ae2-110">Aloitus</span><span class="sxs-lookup"><span data-stu-id="96ae2-110">Get started</span></span>

<span data-ttu-id="96ae2-111">Etsi tapahtumat -toiminto on helposti saatavilla useimmilla sivuilla, joilla näkyvät kirjatut asiakirjat tai kirjattujen asiakirjojen tapahtumat – sekä luettelot että kortit.</span><span class="sxs-lookup"><span data-stu-id="96ae2-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="96ae2-112">Joten ensimmäinen askel on avata yksi näistä sivuista.</span><span class="sxs-lookup"><span data-stu-id="96ae2-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="96ae2-113">Valitse sitten **Etsi tapahtumat** -toiminto tai paina Alt+G-näppäimiä.</span><span class="sxs-lookup"><span data-stu-id="96ae2-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="96ae2-114">**Etsi tapahtumat** -sivu sisältää kaikki asiaan liittyvät asiakirjat ja tapahtumat asiakirjan nro-kentän ja kirjauspäivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="96ae2-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="96ae2-115">Sivu jakautuu kolmeen osaan:</span><span class="sxs-lookup"><span data-stu-id="96ae2-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="96ae2-116">Yläosassa näkyy kentät ja toiminnot, joita käytetään hakujen suodattamiseen.</span><span class="sxs-lookup"><span data-stu-id="96ae2-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="96ae2-117">Keskimmäisessä osassa näkyvät hakuun perustuvat asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="96ae2-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="96ae2-118">Alemmassa osassa on tietoja hakuohjelman löytämästä lähdeasiakirjasta.</span><span class="sxs-lookup"><span data-stu-id="96ae2-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="96ae2-119">Hae tapahtumia</span><span class="sxs-lookup"><span data-stu-id="96ae2-119">Search for entries</span></span>

<span data-ttu-id="96ae2-120">Voit hakea tapahtumia joko asiakirjan, työyhteyshenkilön tai nimikeviittauksen tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="96ae2-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="96ae2-121">Voit muuttaa hakua valitsemalla **Toiminnot**, **Etsi** ja jonkin seuraavista toiminnoista:</span><span class="sxs-lookup"><span data-stu-id="96ae2-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="96ae2-122">Toiminto</span><span class="sxs-lookup"><span data-stu-id="96ae2-122">Action</span></span>|<span data-ttu-id="96ae2-123">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="96ae2-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="96ae2-124">Hae asiakirjan mukaan</span><span class="sxs-lookup"><span data-stu-id="96ae2-124">Find by Document</span></span>|<span data-ttu-id="96ae2-125">Tarkastele tapahtumia tietyn asiakirjanumeron tai kirjauspäivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="96ae2-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="96ae2-126">Liiketoiminnan kontakti</span><span class="sxs-lookup"><span data-stu-id="96ae2-126">Business Contact</span></span> |<span data-ttu-id="96ae2-127">Tarkastele tapahtumia tietyn kontaktityypin, kontaktinumeron, tai ulkoisen asiakirjanumeron perusteella.</span><span class="sxs-lookup"><span data-stu-id="96ae2-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="96ae2-128">Voit syöttää asiakirjaan liittyviä, toimittajalta tai asiakkaalta tulleita tietoja.</span><span class="sxs-lookup"><span data-stu-id="96ae2-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="96ae2-129">Käytä saatavilla olevia kenttiä, kun haluat hakea toimittajan asiakirjoja - käyttäen niitä numeroita, jotka toimittaja on asiakirjoille antanut.</span><span class="sxs-lookup"><span data-stu-id="96ae2-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="96ae2-130">Nimikeviittaus</span><span class="sxs-lookup"><span data-stu-id="96ae2-130">Item reference</span></span>|<span data-ttu-id="96ae2-131">Näytä tapahtumia sarjanumeron tai eränumeron perusteella.</span><span class="sxs-lookup"><span data-stu-id="96ae2-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="96ae2-132">Voit syöttää sarja- tai eränumeron tai suodattaa sarja- tai eränumeroilla, joita haluat hakea.</span><span class="sxs-lookup"><span data-stu-id="96ae2-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="96ae2-133">Tämä toiminto on hyödyllinen, kun haluat nähdä, missä jonkin tietyn nimikkeen seurantanumeroa käytettiin, miltä toimittajalta se saapui tai mille asiakkaalle se myytiin.</span><span class="sxs-lookup"><span data-stu-id="96ae2-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="96ae2-134">Kun olet tehnyt valinnan, syötä asianmukaiset hakutiedot yläreunan kenttiin.</span><span class="sxs-lookup"><span data-stu-id="96ae2-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="96ae2-135">Käytä ohjeen työkaluvihjeitä.</span><span class="sxs-lookup"><span data-stu-id="96ae2-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="96ae2-136">Kun olet valmis, aloita haku valitsemalla **Etsi**.</span><span class="sxs-lookup"><span data-stu-id="96ae2-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="96ae2-137">Jos muutat suodattimia, sinun täytyy valita **Etsi** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="96ae2-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="96ae2-138">Pari esimerkkiä **Hae tapahtumia** -toiminnon käyttämisestä on kohdassa [Jäljitä nimike-seuratut nimikkeet](inventory-how-to-trace-item-tracked-items.md) ja [vaihekuvaus: sarja-eränumeroiden jäljittäminen](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="96ae2-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md) and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="96ae2-139">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="96ae2-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="96ae2-140">Katso myös</span><span class="sxs-lookup"><span data-stu-id="96ae2-140">See Also</span></span>

[<span data-ttu-id="96ae2-141">Business Centralin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="96ae2-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="96ae2-142">Sivutoiminnon lisääminen roolikeskukseen</span><span class="sxs-lookup"><span data-stu-id="96ae2-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="96ae2-143">Nimikeseurannan nimikkeiden jäljittäminen</span><span class="sxs-lookup"><span data-stu-id="96ae2-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]