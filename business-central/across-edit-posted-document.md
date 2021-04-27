---
title: Kirjattujen myynti- ja ostoasiakirjojen muokkaaminen | Microsoft Docs
description: Lisätietoja ostoasiakirjojen kirjaamisessa käytetyistä kirjaustoiminnoista ja kirjattujen asiakirjojen päivittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ef23d98aaeeb63c17e836fd25b547703787264da
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776195"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="f33fd-103">Kirjattujen asiakirjojen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="f33fd-103">Edit Posted Documents</span></span>

<span data-ttu-id="f33fd-104">Joskus kirjattu asiakirja on päivitettävä, koska asiakirjaan liittyvät tiedot ovat muuttuneet.</span><span class="sxs-lookup"><span data-stu-id="f33fd-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="f33fd-105">Kirjatussa asiakirjassa tällainen tieto voi olla esimerkiksi kuljetusliikkeen paketin seurantanumero.</span><span class="sxs-lookup"><span data-stu-id="f33fd-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="f33fd-106">Kirjatussa ostoasiakirjassa tämä voi olla maksun viiteteksti.</span><span class="sxs-lookup"><span data-stu-id="f33fd-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="f33fd-107">Voit muuttaa alkuperäisen asiakirjan muokattavaa versiota, jonka sivun otsikossa on **- Päivitä**-merkintä.</span><span class="sxs-lookup"><span data-stu-id="f33fd-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="f33fd-108">Tämä sivu sisältää alkuperäisen asiakirjan kenttien alijoukon. Jotkin kentistä ovat ei-muokattavia kenttiä, jotka näytetään vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="f33fd-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="f33fd-109">Toiminto on käytettävissä seuraavissa asiakirjoissa kaikilla tuetuilla markkinoilla:</span><span class="sxs-lookup"><span data-stu-id="f33fd-109">The functionality is available for the following documents across all supported markets:</span></span>

- <span data-ttu-id="f33fd-110">Kirjattu myyntitoimitus</span><span class="sxs-lookup"><span data-stu-id="f33fd-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="f33fd-111">Kirjattu ostolasku</span><span class="sxs-lookup"><span data-stu-id="f33fd-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="f33fd-112">Kirjattu palautustoimitus</span><span class="sxs-lookup"><span data-stu-id="f33fd-112">Posted Return Shipment</span></span>
- <span data-ttu-id="f33fd-113">Kirjattu palautusvastaanotto</span><span class="sxs-lookup"><span data-stu-id="f33fd-113">Posted Return Receipt</span></span>

<span data-ttu-id="f33fd-114">Seuraavia lisäasiakirjoja voi muokata tietyissä maissa ja alueilla:</span><span class="sxs-lookup"><span data-stu-id="f33fd-114">The following additional documents can be edited in the specified countries or regions:</span></span>

- <span data-ttu-id="f33fd-115">ES: Kirjattu myyntilasku, kirjattu myyntihyvityslasku, kirjattu ostohyvityslasku</span><span class="sxs-lookup"><span data-stu-id="f33fd-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="f33fd-116">APAC: kirjattu myyntihyvityslasku, kirjattu ostohyvityslasku</span><span class="sxs-lookup"><span data-stu-id="f33fd-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="f33fd-117">RU: Kirjattu myyntihyvityslasku</span><span class="sxs-lookup"><span data-stu-id="f33fd-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="f33fd-118">IT: Kirjattu siirtotoimitus, kirjattu huoltotoimitus</span><span class="sxs-lookup"><span data-stu-id="f33fd-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="f33fd-119">Kirjatun myyntitoimituksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="f33fd-119">To edit a posted sales shipment</span></span>

<span data-ttu-id="f33fd-120">Seuraavassa kerrotaan, miten kirjattua myyntitoimitusta muokataan.</span><span class="sxs-lookup"><span data-stu-id="f33fd-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="f33fd-121">Vaiheet ovat samanlaiset muissa tuetuissa asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="f33fd-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="f33fd-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut myyntitoimitukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f33fd-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="f33fd-123">Valitse muokattava asiakirja ja valitse sitten **Päivitä asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f33fd-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="f33fd-124">Vaihtoehtoisesti voit avata asiakirjan ja valita sitten toiminnon.</span><span class="sxs-lookup"><span data-stu-id="f33fd-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="f33fd-125">Muokkaa **Kirjattu myyntitoimitus - Päivitä** -sivulla esimerkiksi **Paketin seurantanumero**</span><span class="sxs-lookup"><span data-stu-id="f33fd-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="f33fd-126">-kenttää.</span><span class="sxs-lookup"><span data-stu-id="f33fd-126">field, for example.</span></span>
4. <span data-ttu-id="f33fd-127">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="f33fd-127">Choose the **OK** button.</span></span>

<span data-ttu-id="f33fd-128">Kirjattu myyntitoimitus päivitetään.</span><span class="sxs-lookup"><span data-stu-id="f33fd-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="f33fd-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f33fd-129">See Also</span></span>

[<span data-ttu-id="f33fd-130">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="f33fd-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="f33fd-131">Osto</span><span class="sxs-lookup"><span data-stu-id="f33fd-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="f33fd-132">Asiakirjojen ja päiväkirjojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="f33fd-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="f33fd-133">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f33fd-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]