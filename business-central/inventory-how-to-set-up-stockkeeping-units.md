---
title: Varastoyksikköjen määrittäminen | Microsoft Docs
description: Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 18923708fdad1b88714d2dcb2c61bfd2e4259f4b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785710"
---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="c945a-103">Varastointiyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c945a-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="c945a-104">Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.</span><span class="sxs-lookup"><span data-stu-id="c945a-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="c945a-105">Varastointiyksiköt ovat lisätietona nimikekorteille.</span><span class="sxs-lookup"><span data-stu-id="c945a-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="c945a-106">Ne eivät korvaa niitä, vaikka liittyvätkin niihin.</span><span class="sxs-lookup"><span data-stu-id="c945a-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="c945a-107">Varastointiyksiköt mahdollistavat nimikkeen tietojen erittelemisen tietyn sijainnin osalta (esimerkiksi fyysisen varaston tai jakelupaikan osalta) tai saman nimikkeen tietyn variantin osalta (esimerkiksi eri hyllynumeroiden ja eri täydennystietojen osalta).</span><span class="sxs-lookup"><span data-stu-id="c945a-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="c945a-108">Varastointiyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c945a-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="c945a-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastointiyksiköt** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c945a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c945a-110">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="c945a-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="c945a-111">Syötä kortin kentät.</span><span class="sxs-lookup"><span data-stu-id="c945a-111">Fill in the fields on the card.</span></span> <span data-ttu-id="c945a-112">Seuraavat kentät ovat pakollisia: **Nimikkeen nro**, **Paikkakoodi**, ja **Varianttikoodi**.</span><span class="sxs-lookup"><span data-stu-id="c945a-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="c945a-113">Kun olet määrittänyt nimikkeen ensimmäisen varastointiyksikön, **Nimike**-kortin **Varastointiyks. on olemassa** -valintaruutu on valittu.</span><span class="sxs-lookup"><span data-stu-id="c945a-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="c945a-114">Käytä **Luo varastointiyksikkö** -eräajoa, kun haluat luoda nimikkeelle useita varastointiyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="c945a-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c945a-115">**Varastointiyksikön** kortin tiedoilla on korkeampi prioriteetti kuin **nimikkeen** kortilla.</span><span class="sxs-lookup"><span data-stu-id="c945a-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="c945a-116">Jos varastointiyksikkö toimitetaan tuotannon välityksellä, **Vakiokustannus**-kenttää ei käytetä tuotetun nimikkeen todellisten kustannusten laskutuksessa ja oikaisussa.</span><span class="sxs-lookup"><span data-stu-id="c945a-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="c945a-117">Sen sijaan käytetään pohjana olevan nimikekortin **Vakiokustannus**-kenttää, ja kaikki varianssit lasketaan nimikkeen kustannusjakaumia kohden.</span><span class="sxs-lookup"><span data-stu-id="c945a-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="c945a-118">Koska tuotannon tuoterakenteita ja reititystä ei voida määrittää SKU:ihin, koottu yksikkökustannus ja liittyvät kustannusjakauman laskennat eivät myöskään ole käytettävissä SKU:issa.</span><span class="sxs-lookup"><span data-stu-id="c945a-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="c945a-119">Lisätietoja on kohdassa [Tietoja vakiokustannusten laskennasta](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="c945a-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="c945a-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c945a-120">See Also</span></span>  
[<span data-ttu-id="c945a-121">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="c945a-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c945a-122">Varastoinninhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c945a-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="c945a-123">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="c945a-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="c945a-124">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="c945a-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c945a-125">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="c945a-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="c945a-126">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="c945a-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c945a-127">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c945a-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]