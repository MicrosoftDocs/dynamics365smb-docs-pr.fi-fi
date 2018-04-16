---
title: "Varastoyksikköjen määrittäminen | Microsoft Docs"
description: "Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: aa25b3b809b27160f1493408fc8f61f14b651b67
ms.contentlocale: fi-fi
ms.lasthandoff: 04/16/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="0ee26-103">Varastointiyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0ee26-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="0ee26-104">Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.</span><span class="sxs-lookup"><span data-stu-id="0ee26-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="0ee26-105">Varastointiyksiköt ovat lisätietona nimikekorteille.</span><span class="sxs-lookup"><span data-stu-id="0ee26-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="0ee26-106">Ne eivät korvaa niitä, vaikka liittyvätkin niihin.</span><span class="sxs-lookup"><span data-stu-id="0ee26-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="0ee26-107">Varastointiyksiköt mahdollistavat nimikkeen tietojen erittelemisen tietyn sijainnin osalta (esimerkiksi fyysisen varaston tai jakelupaikan osalta) tai saman nimikkeen tietyn variantin osalta (esimerkiksi eri hyllynumeroiden ja eri täydennystietojen osalta).</span><span class="sxs-lookup"><span data-stu-id="0ee26-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="0ee26-108">Varastointiyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0ee26-108">To set up a stockkeeping unit</span></span>  

1. <span data-ttu-id="0ee26-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Varastointiyksiköt** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0ee26-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0ee26-110">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="0ee26-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="0ee26-111">Syötä kortin kentät.</span><span class="sxs-lookup"><span data-stu-id="0ee26-111">Fill in the fields on the card.</span></span> <span data-ttu-id="0ee26-112">Seuraavat kentät ovat pakollisia: **Nimikkeen nro**, **Paikkakoodi**, ja **Varianttikoodi**.</span><span class="sxs-lookup"><span data-stu-id="0ee26-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="0ee26-113">Kun olet määrittänyt nimikkeen ensimmäisen varastointiyksikön, **Nimike**-kortin **Varastointiyks. on olemassa** -valintaruutu on valittu.</span><span class="sxs-lookup"><span data-stu-id="0ee26-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="0ee26-114">Käytä **Luo varastointiyksikkö** -eräajoa, kun haluat luoda nimikkeelle useita varastointiyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="0ee26-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0ee26-115">**Varastointiyksikön** kortin tiedoilla on korkeampi prioriteetti kuin **nimikkeen** kortilla.</span><span class="sxs-lookup"><span data-stu-id="0ee26-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0ee26-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0ee26-116">See Also</span></span>  
[<span data-ttu-id="0ee26-117">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="0ee26-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="0ee26-118">Varastoinninhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0ee26-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="0ee26-119">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="0ee26-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0ee26-120">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="0ee26-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0ee26-121">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="0ee26-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="0ee26-122">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="0ee26-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0ee26-123">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ee26-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

