---
title: Nimikkeiden myynnin tai oston estäminen
description: Nimike voidaan merkitä Business Centralissa estetyksi myynnin tai oston osalta tai kaikkia tarkoituksia varten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c453a10f30d2a45f6d4641bda8b24ee3659b1a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182298"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="7cf12-103">Nimikkeiden myynnin tai oston estäminen</span><span class="sxs-lookup"><span data-stu-id="7cf12-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="7cf12-104">Voit estää nimikkeen viennin myynti- tai ostoriveille estämällä sen kirjaamiseen kaikissa tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="7cf12-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="7cf12-105">Seuraava taulukko osoittaa, mitä tapahtuu, kun nimikkeet on estetty.</span><span class="sxs-lookup"><span data-stu-id="7cf12-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="7cf12-106">Asetus</span><span class="sxs-lookup"><span data-stu-id="7cf12-106">Option</span></span>|<span data-ttu-id="7cf12-107">Description</span><span class="sxs-lookup"><span data-stu-id="7cf12-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="7cf12-108">**Myynti estetty**</span><span class="sxs-lookup"><span data-stu-id="7cf12-108">**Sales Blocked**</span></span>|<span data-ttu-id="7cf12-109">Nimikettä ei voi viedä myyntiasiakirjaan tai myynnin nimikepäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="7cf12-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="7cf12-110">**Osto estetty**</span><span class="sxs-lookup"><span data-stu-id="7cf12-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="7cf12-111">Et voi viedä nimikettä ostoasiakirjaan, ostonimikepäiväkirjaan tai ostojen suunnitteluprosesseihin.</span><span class="sxs-lookup"><span data-stu-id="7cf12-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="7cf12-112">**Estetty**</span><span class="sxs-lookup"><span data-stu-id="7cf12-112">**Blocked**</span></span>|<span data-ttu-id="7cf12-113">Et voi käyttää nimikettä missä nimiketapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="7cf12-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="7cf12-114">Estetyt nimikkeet voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="7cf12-114">Blocked items can be returned.</span></span> <span data-ttu-id="7cf12-115">Tämä tarkoittaa sitä, etteivät mitkään yllämainitut asetukset päden, kun nimikettä käytetään palautustilauksissa ja hyvitysmaksuissa.</span><span class="sxs-lookup"><span data-stu-id="7cf12-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="7cf12-116">Kun luot uusia asiakirjoja aiemmin luotujen asiakirjojen perusteella **Kopioi asiakirjasta** -toiminnolla, saat ilmoituksen, jos lähdeasiakirjan riveillä olevia nimikkeitä on estetty.</span><span class="sxs-lookup"><span data-stu-id="7cf12-116">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="7cf12-117">Estetyt asiakirjarivit jätetään pois uudesta asiakirjasta, ja ilmoitus sisältää yhteenvedon kaikista lähdeasiakirjassa estetyistä asiakirjariveistä.</span><span class="sxs-lookup"><span data-stu-id="7cf12-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="7cf12-118">Nimikkeen myyntiriveille viennin estäminen</span><span class="sxs-lookup"><span data-stu-id="7cf12-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="7cf12-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7cf12-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7cf12-120">Valitse estettävä nimike ja valitse sitten **Myynti estetty** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7cf12-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="7cf12-121">Jos yrität viedä nimikkeen myyntiasiakirjaan tai päiväkirjariville, saat virheilmoituksen, joka ilmoittaa, että nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="7cf12-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="7cf12-122">Nimikkeen ostoriveille viennin estäminen</span><span class="sxs-lookup"><span data-stu-id="7cf12-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="7cf12-123">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7cf12-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7cf12-124">Valitse estettävä nimike ja valitse sitten **Osto estetty** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7cf12-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="7cf12-125">Jos yrität viedä nimikkeen ostoasiakirjaan tai päiväkirjariville, saat virheilmoituksen, joka ilmoittaa, että nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="7cf12-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="7cf12-126">Nimikkeen kirjaamisen estäminen</span><span class="sxs-lookup"><span data-stu-id="7cf12-126">To block an item from being posted</span></span>
1. <span data-ttu-id="7cf12-127">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7cf12-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="7cf12-128">Valitse estettävä nimike ja valitse sitten **Estetty**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7cf12-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="7cf12-129">Jos yrität kirjata nimikkeelle jonkin tapahtuman, saat virheilmoituksen, jonka mukaan nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="7cf12-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cf12-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7cf12-130">See Also</span></span>  
[<span data-ttu-id="7cf12-131">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="7cf12-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="7cf12-132">Varasto</span><span class="sxs-lookup"><span data-stu-id="7cf12-132">Inventory</span></span>](inventory-manage-inventory.md)  
