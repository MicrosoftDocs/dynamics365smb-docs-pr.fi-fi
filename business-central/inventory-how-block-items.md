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
ms.openlocfilehash: 8c98e4b893783c795a49e05ab04dc70b03161c6a
ms.sourcegitcommit: bf5f89dfaf5ad9f8f9902941cf3dac3e9f3553e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594247"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="04530-103">Nimikkeiden myynnin tai oston estäminen</span><span class="sxs-lookup"><span data-stu-id="04530-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="04530-104">Voit estää nimikkeen viennin myynti- tai ostoriveille estämällä sen kirjaamiseen kaikissa tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="04530-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="04530-105">Seuraava taulukko osoittaa, mitä tapahtuu, kun nimikkeet on estetty.</span><span class="sxs-lookup"><span data-stu-id="04530-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="04530-106">Asetus</span><span class="sxs-lookup"><span data-stu-id="04530-106">Option</span></span>|<span data-ttu-id="04530-107">Description</span><span class="sxs-lookup"><span data-stu-id="04530-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="04530-108">**Myynti estetty**</span><span class="sxs-lookup"><span data-stu-id="04530-108">**Sales Blocked**</span></span>|<span data-ttu-id="04530-109">Nimikettä ei voi viedä myyntiasiakirjaan tai myynnin nimikepäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="04530-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="04530-110">**Osto estetty**</span><span class="sxs-lookup"><span data-stu-id="04530-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="04530-111">Et voi viedä nimikettä ostoasiakirjaan, ostonimikepäiväkirjaan tai ostojen suunnitteluprosesseihin.</span><span class="sxs-lookup"><span data-stu-id="04530-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="04530-112">**Estetty**</span><span class="sxs-lookup"><span data-stu-id="04530-112">**Blocked**</span></span>|<span data-ttu-id="04530-113">Et voi käyttää nimikettä missä nimiketapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="04530-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="04530-114">Estetyt nimikkeet voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="04530-114">Blocked items can be returned.</span></span> <span data-ttu-id="04530-115">Tämä tarkoittaa sitä, etteivät mitkään yllämainitut asetukset päden, kun nimikettä käytetään palautustilauksissa ja hyvitysmaksuissa.</span><span class="sxs-lookup"><span data-stu-id="04530-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="04530-116">Nimikkeen myyntiriveille viennin estäminen</span><span class="sxs-lookup"><span data-stu-id="04530-116">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="04530-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="04530-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="04530-118">Valitse estettävä nimike ja valitse sitten **Myynti estetty** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="04530-118">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="04530-119">Jos yrität viedä nimikkeen myyntiasiakirjaan tai päiväkirjariville, saat virheilmoituksen, joka ilmoittaa, että nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="04530-119">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="04530-120">Nimikkeen ostoriveille viennin estäminen</span><span class="sxs-lookup"><span data-stu-id="04530-120">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="04530-121">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="04530-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="04530-122">Valitse estettävä nimike ja valitse sitten **Osto estetty** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="04530-122">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="04530-123">Jos yrität viedä nimikkeen ostoasiakirjaan tai päiväkirjariville, saat virheilmoituksen, joka ilmoittaa, että nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="04530-123">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="04530-124">Nimikkeen kirjaamisen estäminen</span><span class="sxs-lookup"><span data-stu-id="04530-124">To block an item from being posted</span></span>
1. <span data-ttu-id="04530-125">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="04530-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="04530-126">Valitse estettävä nimike ja valitse sitten **Estetty**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="04530-126">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="04530-127">Jos yrität kirjata nimikkeelle jonkin tapahtuman, saat virheilmoituksen, jonka mukaan nimike on estetty.</span><span class="sxs-lookup"><span data-stu-id="04530-127">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="04530-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="04530-128">See Also</span></span>  
[<span data-ttu-id="04530-129">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="04530-129">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="04530-130">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="04530-130">Inventory</span></span>](inventory-manage-inventory.md)  
