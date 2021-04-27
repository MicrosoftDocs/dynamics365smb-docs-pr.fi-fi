---
title: Toimitusehtojen määrittäminen
description: Voit määrittää koodin jokaiselle tarjotulle toimitusehdolle, ja syöttää niitä koskevia tietoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8390c95083eb02c208e97f0309a725e8ec4d7730
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778570"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="ce3ce-103">Toimitusehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ce3ce-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="ce3ce-104">Toimitusehdot määräytyvät usein nimikkeiden, asiakkaiden ja toimittajien mukaan.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="ce3ce-105">Jos asiakas asuu esimerkiksi saarella, hän voi valita, että nimikkeet toimitetaan aina lentoteitse tai aina meriteitse.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="ce3ce-106">Jotkin asiakkaat saattavat haluta toimituksen seuraavana päivänä.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="ce3ce-107">Jotkin asiakkaat taas haluavat noutaa tilauksen.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-107">Some may want to pick up the order.</span></span> <span data-ttu-id="ce3ce-108">Asiakas- ja toimittajakortteihin voit määrittää, kuinka toimitus toteutetaan.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="ce3ce-109">Kullekin toimitusehdolle määritetään kuvaus ja koodi **Toimitusehto**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="ce3ce-110">Voit esimerkiksi määrittää koodiksi FOB ja syöttää **Kuvaus**-kenttään Vapaasti aluksessa.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="ce3ce-111">Voit syöttää koodin **Toimitusehtokoodi**-kenttään myös muualla järjestelmässä, esimerkiksi asiakaskortissa.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="ce3ce-112">Kun tämän jälkeen luot esimerkiksi uusia tilauksia, laskuja ja hyvityslaskuja, järjestelmä syöttää koodin kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="ce3ce-113">Voit muuttaa kuvausta tarvittaessa asiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="ce3ce-114">Toimitustapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ce3ce-114">To set up a shipment method</span></span>

1. <span data-ttu-id="ce3ce-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimitustavat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="ce3ce-116">Valitse **Toimitusehdot**-sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="ce3ce-117">Määritä uudella rivillä toimitusehdon koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="ce3ce-118">Jos käytät Incotermsiä, määritä toimitustavat edustamaan asianmukaisia Incoterms-sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce3ce-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ce3ce-119">See Also</span></span>

[<span data-ttu-id="ce3ce-120">Kuljetusliikkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ce3ce-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="ce3ce-121">Kollien seuraaminen</span><span class="sxs-lookup"><span data-stu-id="ce3ce-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="ce3ce-122">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="ce3ce-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ce3ce-123">Varasto</span><span class="sxs-lookup"><span data-stu-id="ce3ce-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ce3ce-124">Varastoinninhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ce3ce-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="ce3ce-125">Kokoonpanon hallinta</span><span class="sxs-lookup"><span data-stu-id="ce3ce-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="ce3ce-126">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="ce3ce-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ce3ce-127">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ce3ce-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ce3ce-128">Incoterms osoitteessa iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="ce3ce-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]