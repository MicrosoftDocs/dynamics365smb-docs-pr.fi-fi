---
title: Kirjattujen myynti- ja ostoasiakirjojen muokkaaminen | Microsoft Docs
description: Lisätietoja ostoasiakirjojen kirjaamisessa käytetyistä kirjaustoiminnoista ja kirjattujen asiakirjojen päivittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6fbb4e458b0e4f9068b234748a3921dbca6b3222
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300591"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="5fe5e-103">Kirjattujen asiakirjojen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="5fe5e-103">Edit Posted Documents</span></span>
<span data-ttu-id="5fe5e-104">Joskus kirjattu asiakirja on päivitettävä, koska asiakirjaan liittyvät tiedot ovat muuttuneet.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="5fe5e-105">Kirjatussa asiakirjassa tällainen tieto voi olla esimerkiksi kuljetusliikkeen paketin seurantanumero.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="5fe5e-106">Kirjatussa ostoasiakirjassa tämä voi olla maksun viiteteksti.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="5fe5e-107">Voit muuttaa alkuperäisen asiakirjan muokattavaa versiota, jonka sivun otsikossa on **- Päivitä**-merkintä.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="5fe5e-108">Tämä sivu sisältää alkuperäisen asiakirjan kenttien alijoukon. Jotkin kentistä ovat ei-muokattavia kenttiä, jotka näytetään vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="5fe5e-109">Toiminto on käytettävissä seuraavissa asiakirjoissa kaikissa maaversioissa:</span><span class="sxs-lookup"><span data-stu-id="5fe5e-109">The functionality is available for the following documents in all country versions:</span></span>
- <span data-ttu-id="5fe5e-110">Kirjattu myyntitoimitus</span><span class="sxs-lookup"><span data-stu-id="5fe5e-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="5fe5e-111">Kirjattu ostolasku</span><span class="sxs-lookup"><span data-stu-id="5fe5e-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="5fe5e-112">Kirjattu palautustoimitus</span><span class="sxs-lookup"><span data-stu-id="5fe5e-112">Posted Return Shipment</span></span>
- <span data-ttu-id="5fe5e-113">Kirjattu palautusvastaanotto</span><span class="sxs-lookup"><span data-stu-id="5fe5e-113">Posted Return Receipt</span></span>

<span data-ttu-id="5fe5e-114">Seuraavia lisäasiakirjoja voi muokata valituissa maaversioissa:</span><span class="sxs-lookup"><span data-stu-id="5fe5e-114">The following additional documents can be edited in selected country versions:</span></span>
- <span data-ttu-id="5fe5e-115">ES: Kirjattu myyntilasku, kirjattu myyntihyvityslasku, kirjattu ostohyvityslasku</span><span class="sxs-lookup"><span data-stu-id="5fe5e-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="5fe5e-116">APAC: kirjattu myyntihyvityslasku, kirjattu ostohyvityslasku</span><span class="sxs-lookup"><span data-stu-id="5fe5e-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="5fe5e-117">RU: Kirjattu myyntihyvityslasku</span><span class="sxs-lookup"><span data-stu-id="5fe5e-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="5fe5e-118">IT: Kirjattu siirtotoimitus, kirjattu huoltotoimitus</span><span class="sxs-lookup"><span data-stu-id="5fe5e-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="5fe5e-119">Kirjatun myyntitoimituksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="5fe5e-119">To edit a posted sales shipment</span></span>
<span data-ttu-id="5fe5e-120">Seuraavassa kerrotaan, miten kirjattua myyntitoimitusta muokataan.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="5fe5e-121">Vaiheet ovat samanlaiset muissa tuetuissa asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="5fe5e-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntitoimitukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="5fe5e-123">Valitse muokattava asiakirja ja valitse sitten **Päivitä asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="5fe5e-124">Vaihtoehtoisesti voit avata asiakirjan ja valita sitten toiminnon.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="5fe5e-125">Muokkaa **Kirjattu myyntitoimitus - Päivitä** -sivulla esimerkiksi **Paketin seurantanumero**</span><span class="sxs-lookup"><span data-stu-id="5fe5e-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="5fe5e-126">-kenttää.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-126">field, for example.</span></span>
4. <span data-ttu-id="5fe5e-127">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-127">Choose the **OK** button.</span></span>

<span data-ttu-id="5fe5e-128">Kirjattu myyntitoimitus päivitetään.</span><span class="sxs-lookup"><span data-stu-id="5fe5e-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fe5e-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5fe5e-129">See Also</span></span>
[<span data-ttu-id="5fe5e-130">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="5fe5e-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="5fe5e-131">Osto</span><span class="sxs-lookup"><span data-stu-id="5fe5e-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="5fe5e-132">Asiakirjojen ja päiväkirjojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="5fe5e-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="5fe5e-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fe5e-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
