---
title: Nimikkeiden myynnin tai oston estäminen
description: Nimike voidaan merkitä Business Centralissa estetyksi myynnin tai oston osalta tai kaikkia tarkoituksia varten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e13d59e939e71a252e08afc26d2fb1ec76b247c9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238530"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="f4cef-103">Nimikkeiden myynnin tai oston estäminen</span><span class="sxs-lookup"><span data-stu-id="f4cef-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="f4cef-104">Voit estää nimikkeen viennin myynti- tai ostoriveille estämällä sen kirjaamiseen kaikissa tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="f4cef-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="f4cef-105">Seuraava taulukko osoittaa, mitä tapahtuu, kun nimikkeet on estetty.</span><span class="sxs-lookup"><span data-stu-id="f4cef-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="f4cef-106">Asetus</span><span class="sxs-lookup"><span data-stu-id="f4cef-106">Option</span></span>|<span data-ttu-id="f4cef-107">Description</span><span class="sxs-lookup"><span data-stu-id="f4cef-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="f4cef-108">**Myynti estetty**</span><span class="sxs-lookup"><span data-stu-id="f4cef-108">**Sales Blocked**</span></span>|<span data-ttu-id="f4cef-109">Nimikettä ei voi viedä myyntiasiakirjaan tai myynnin nimikepäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="f4cef-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="f4cef-110">**Osto estetty**</span><span class="sxs-lookup"><span data-stu-id="f4cef-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="f4cef-111">Et voi viedä nimikettä ostoasiakirjaan, ostonimikepäiväkirjaan tai ostojen suunnitteluprosesseihin.</span><span class="sxs-lookup"><span data-stu-id="f4cef-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="f4cef-112">**Estetty**</span><span class="sxs-lookup"><span data-stu-id="f4cef-112">**Blocked**</span></span>|<span data-ttu-id="f4cef-113">Et voi käyttää nimikettä missä nimiketapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="f4cef-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="f4cef-114">Lisätietoja nimikkeen estämisestä kaikissa tarkoituksissa on Nimikekortti-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="f4cef-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="f4cef-115">Nimikkeen myyntiriveille viennin estäminen</span><span class="sxs-lookup"><span data-stu-id="f4cef-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="f4cef-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f4cef-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f4cef-117">Valitse estettävä nimike ja valitse sitten **Myynti estetty** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f4cef-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="f4cef-118">Jos yrität viedä nimikkeen myyntiasiakirjaan tai päiväkirjariville, saat virheilmoituksen, joka ilmoittaa, että nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="f4cef-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="f4cef-119">Nimikkeen ostoriveille viennin estäminen</span><span class="sxs-lookup"><span data-stu-id="f4cef-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="f4cef-120">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f4cef-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f4cef-121">Valitse estettävä nimike ja valitse sitten **Osto estetty** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f4cef-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="f4cef-122">Jos yrität viedä nimikkeen ostoasiakirjaan tai päiväkirjariville, saat virheilmoituksen, joka ilmoittaa, että nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="f4cef-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="f4cef-123">Nimikkeen kirjaamisen estäminen</span><span class="sxs-lookup"><span data-stu-id="f4cef-123">To block an item from being posted</span></span>
1. <span data-ttu-id="f4cef-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f4cef-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="f4cef-125">Valitse estettävä nimike ja valitse sitten **Estetty**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f4cef-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="f4cef-126">Jos yrität kirjata nimikkeelle jonkin tapahtuman, saat virheilmoituksen, jonka mukaan nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="f4cef-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4cef-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f4cef-127">See Also</span></span>  
[<span data-ttu-id="f4cef-128">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="f4cef-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="f4cef-129">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="f4cef-129">Inventory</span></span>](inventory-manage-inventory.md)  
