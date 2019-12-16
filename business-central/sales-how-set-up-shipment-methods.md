---
title: Toimitusehtojen määrittäminen | Microsoft Docs
description: Voit määrittää koodin jokaiselle tarjotulle toimitusehdolle, ja syöttää niitä koskevia tietoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 75a3e689083e64f446e84b2bc3b1d26961e3d898
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877541"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="3551d-103">Toimitusehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3551d-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="3551d-104">Toimitusehdot, joita kutsutaan myös incoterms-toimitusehdoiksi, määräytyvät usein nimikkeiden, asiakkaiden ja toimittajien mukaan.</span><span class="sxs-lookup"><span data-stu-id="3551d-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="3551d-105">Jos asiakas asuu esimerkiksi saarella, hän voi valita, että nimikkeet toimitetaan aina lentoteitse tai aina meriteitse.</span><span class="sxs-lookup"><span data-stu-id="3551d-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="3551d-106">Jotkin asiakkaat saattavat haluta toimituksen seuraavana päivänä.</span><span class="sxs-lookup"><span data-stu-id="3551d-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="3551d-107">Jotkin asiakkaat taas haluavat noutaa tilauksen.</span><span class="sxs-lookup"><span data-stu-id="3551d-107">Some may want to pick up the order.</span></span> <span data-ttu-id="3551d-108">Asiakas- ja toimittajakortteihin voit määrittää, kuinka toimitus toteutetaan.</span><span class="sxs-lookup"><span data-stu-id="3551d-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="3551d-109">Kullekin toimitusehdolle määritetään kuvaus ja koodi **Toimitusehto**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="3551d-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="3551d-110">Voit esimerkiksi määrittää koodiksi FOB ja syöttää **Kuvaus**-kenttään Vapaasti aluksessa.</span><span class="sxs-lookup"><span data-stu-id="3551d-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="3551d-111">Voit syöttää koodin **Toimitusehtokoodi**-kenttään myös muualla järjestelmässä, esimerkiksi asiakaskortissa.</span><span class="sxs-lookup"><span data-stu-id="3551d-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="3551d-112">Kun tämän jälkeen luot esimerkiksi uusia tilauksia, laskuja ja hyvityslaskuja, järjestelmä syöttää koodin kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="3551d-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="3551d-113">Voit muuttaa kuvausta tarvittaessa asiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="3551d-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="3551d-114">Toimituskoodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3551d-114">To set up a shipment code</span></span>
1. <span data-ttu-id="3551d-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimitustavat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3551d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="3551d-116">Valitse **Toimitusehdot**-sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="3551d-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="3551d-117">Määritä uudella rivillä toimitusehdon koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="3551d-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="3551d-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3551d-118">See Also</span></span>
[<span data-ttu-id="3551d-119">Incoterms-toimituslausekkeet</span><span class="sxs-lookup"><span data-stu-id="3551d-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="3551d-120">Kuljetusliikkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3551d-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="3551d-121">[Kollien seuraaminen](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="3551d-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="3551d-122">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="3551d-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="3551d-123">Varasto</span><span class="sxs-lookup"><span data-stu-id="3551d-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="3551d-124">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="3551d-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="3551d-125">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="3551d-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="3551d-126">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="3551d-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="3551d-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3551d-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
