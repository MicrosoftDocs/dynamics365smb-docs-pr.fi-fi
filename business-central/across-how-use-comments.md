---
title: Kommenttien lisääminen kortteihin ja asiakirjoihin | Microsoft Docs
description: Lisää tietoja tileihin, asiakkaiden kortteihin tai myyntitilauksiin ja jaa muille käyttäjille tietoja sopimuksista, kuten erikoishinnoista tai toimitustavasta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ef6d7a5882829bb12620337c5985c31f85d69c5c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787205"
---
# <a name="add-comments-to-cards-and-documents"></a><span data-ttu-id="4e7b1-103">Kommenttien lisääminen kortteihin ja asiakirjoihin</span><span class="sxs-lookup"><span data-stu-id="4e7b1-103">Add Comments to Cards and Documents</span></span>
<span data-ttu-id="4e7b1-104">Voit lisätä tietoja KP-tileihin, asiakkaiden kortteihin tai myyntitilauksiin ja jakaa muille käyttäjille tietoja poikkeuksista tai erikoissopimuksista.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-104">You can add extra information to G/L accounts, customers cards, or sales orders to communicate exceptions or special agreements to other users.</span></span>
<span data-ttu-id="4e7b1-105">Käytännössä kaikissa korteissa ja asiakirjoissa on **Kommentit**-toiminto. Se avaa **Kommenttilomake**-sivun, jossa voi kirjoittaa ja lukea kommentteja.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-105">Practically all cards and document have a **Comments** action, which opens the **Comment Sheet** page where you can write or read comments.</span></span> <span data-ttu-id="4e7b1-106">Asiakirjoissa voi lisätä kommentteja myös yksittäisille riveille.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-106">On documents, you can also add comments to individual lines.</span></span>

<span data-ttu-id="4e7b1-107">Jatkuvien asiakirjojen kommentit siirretään liittyvään kirjattuun asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-107">Comments on ongoing documents are transferred to the related posted document.</span></span> <span data-ttu-id="4e7b1-108">Esimerkiksi myyntitilauksen kommentti siirretään tuloksena saatavaan kirjattuun myyntitoimitukseen.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-108">For example, a comment on a sales order is transferred to a resulting posted sales shipment.</span></span>

<span data-ttu-id="4e7b1-109">Voit määrittää myös, haluatko, että kommentit siirretään yhdestä asiakirjatyypistä toiseen asiakirjatulostyyppiin, kuten myyntitilauksesta myyntilaskuun.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-109">In addition, you can specify if you want comments to be transferred from one type of document to another resulting type of document, such as from a sales order to a sales invoice.</span></span> <span data-ttu-id="4e7b1-110">Voit tehdä tämän **Myynnit ja myyntisaamiset**- ja **Ostot ja ostovelat** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-110">You do this in the **Sales & Receivables** and the **Purchases & Payables** pages respectively.</span></span>

> [!NOTE]
> <span data-ttu-id="4e7b1-111">Kommentteja ei tulosteta raportteihin tai ulkoisiin asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-111">Comments are not printed or output to reports or externally-facing documents.</span></span>

<span data-ttu-id="4e7b1-112">Seuraavassa kerrotaan, miten kommentti lisätään nimikkeen korttiin.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-112">The following describes how to add a comment to an item card.</span></span> <span data-ttu-id="4e7b1-113">Vaiheet ovat samanlaiset kaikissa korteissa ja asiakirjoissa asiakirjan rivejä lukuun ottamatta. Niillä **Kommentit**-toiminto on rivien toimintovalikossa.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-113">The steps are similar for all other cards and documents, except on document lines, the **Comments** action is placed on a lines action menu.</span></span>

## <a name="to-add-a-comments-to-an-item-card"></a><span data-ttu-id="4e7b1-114">Kommenttien lisääminen nimikkeen korttiin</span><span class="sxs-lookup"><span data-stu-id="4e7b1-114">To add a comments to an item card</span></span>
1. <span data-ttu-id="4e7b1-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4e7b1-116">Avaa oikea nimikkeen kortti.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-116">Open the relevant item card.</span></span>
3. <span data-ttu-id="4e7b1-117">Valitse **Kommentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-117">Choose the **Comments** action.</span></span>
4. <span data-ttu-id="4e7b1-118">Kirjoita **Kommenttilomake**-sivulla tekstiä ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-118">On the **Comment Sheet** page, enter any text, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e7b1-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4e7b1-119">See Also</span></span>
<span data-ttu-id="4e7b1-120">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e7b1-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4e7b1-121">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="4e7b1-121">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]