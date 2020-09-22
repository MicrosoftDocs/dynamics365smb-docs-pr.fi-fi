---
title: Nimikkeiden myynnin tai oston estäminen
description: Voit estää nimikkeen käytön esimerkiksi myynti- tai ostoasiakirjoissa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: fb80cecd119cf061b3102d94f586da4c103bd21c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784811"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="1d802-103">Nimikkeiden myynnin tai oston estäminen</span><span class="sxs-lookup"><span data-stu-id="1d802-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="1d802-104">Voit estää tuotteen syöttämisen myynti- tai ostoasiakirjojen riveille ja estää sen kirjaamiseen kaikissa tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="1d802-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="1d802-105">Tämä on hyödyllistä esimerkiksi silloin, kun nimikkeellä on tunnettu vika.</span><span class="sxs-lookup"><span data-stu-id="1d802-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="1d802-106">Jos joku valitsee myynti- tai ostoasiakirjassa estetyn nimikkeen, viesti ilmoittaa heille, että nimike on suljettu.</span><span class="sxs-lookup"><span data-stu-id="1d802-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="1d802-107">Seuraava taulukko kuvaa, mitä tapahtuu, kun nimikkeet on estetty.</span><span class="sxs-lookup"><span data-stu-id="1d802-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="1d802-108">Asetus</span><span class="sxs-lookup"><span data-stu-id="1d802-108">Option</span></span>|<span data-ttu-id="1d802-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="1d802-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="1d802-110">**Myynti estetty**</span><span class="sxs-lookup"><span data-stu-id="1d802-110">**Sales Blocked**</span></span>|<span data-ttu-id="1d802-111">Nimikettä ei voi viedä myyntiasiakirjaan tai myynnin nimikepäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="1d802-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="1d802-112">**Osto estetty**</span><span class="sxs-lookup"><span data-stu-id="1d802-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="1d802-113">Et voi viedä nimikettä ostoasiakirjaan, ostonimikepäiväkirjaan tai ostojen suunnitteluprosesseihin.</span><span class="sxs-lookup"><span data-stu-id="1d802-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="1d802-114">**Estetty**</span><span class="sxs-lookup"><span data-stu-id="1d802-114">**Blocked**</span></span>|<span data-ttu-id="1d802-115">Et voi käyttää nimikettä missä nimiketapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="1d802-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="1d802-116">Estetyt nimikkeet voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="1d802-116">Blocked items can be returned.</span></span> <span data-ttu-id="1d802-117">Tämä tarkoittaa sitä, etteivät mitkään yllämainitut asetukset päden, kun nimikettä käytetään palautustilauksissa ja hyvitysmaksuissa.</span><span class="sxs-lookup"><span data-stu-id="1d802-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="1d802-118">Kun luot uusia asiakirjoja aiemmin luotujen asiakirjojen perusteella **Kopioi asiakirjasta** -toiminnolla, saat ilmoituksen, jos lähdeasiakirjan riveillä olevia nimikkeitä on estetty.</span><span class="sxs-lookup"><span data-stu-id="1d802-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="1d802-119">Estetyt asiakirjarivit jätetään pois uudesta asiakirjasta, ja ilmoitus sisältää yhteenvedon kaikista lähdeasiakirjassa estetyistä asiakirjariveistä.</span><span class="sxs-lookup"><span data-stu-id="1d802-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="1d802-120">Nimikkeen myyntiriveille viennin estäminen</span><span class="sxs-lookup"><span data-stu-id="1d802-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="1d802-121">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1d802-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1d802-122">Valitse estettävä nimike ja valitse sitten **Myynti estetty** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1d802-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="1d802-123">Nimikkeen ostoriveille viennin estäminen</span><span class="sxs-lookup"><span data-stu-id="1d802-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="1d802-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1d802-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1d802-125">Valitse estettävä nimike ja valitse sitten **Osto estetty** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1d802-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="1d802-126">Nimikkeen kirjaamisen estäminen</span><span class="sxs-lookup"><span data-stu-id="1d802-126">To block an item from being posted</span></span>
1. <span data-ttu-id="1d802-127">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1d802-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="1d802-128">Valitse estettävä nimike ja valitse sitten **Estetty**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1d802-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d802-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1d802-129">See Also</span></span>  
[<span data-ttu-id="1d802-130">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="1d802-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="1d802-131">Varasto</span><span class="sxs-lookup"><span data-stu-id="1d802-131">Inventory</span></span>](inventory-manage-inventory.md)  
