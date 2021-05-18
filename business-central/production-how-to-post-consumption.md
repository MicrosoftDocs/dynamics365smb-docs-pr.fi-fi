---
title: Kulutuksen eräkirjaus
description: Jos materiaalinottotapa on Manuaalinen, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b3ee6ca54e21605b4e9cf340b04656694c9801e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935184"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="a4388-103">Tuotannon kulutuksen eräkirjaus</span><span class="sxs-lookup"><span data-stu-id="a4388-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="a4388-104">Jos materiaalinottotapa on **Manuaalinen**, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="a4388-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="a4388-105">Jos olet lisännyt valintamerkin sijaintikortin **Vaadi poiminta** -kenttään osoittamaan, että sijainti vaatii varaston poimintakäsittelyä, sinun ei tarvitse käyttää tätä eräajoa.</span><span class="sxs-lookup"><span data-stu-id="a4388-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a4388-106">käsittelee kulutusta, kun varaston poiminta kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a4388-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="a4388-107">Lisätietoja on kohdassa [Tuotantopoiminta perusvarastointimäärityksissä](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="a4388-107">For more information, see [Pick for Production in Basic Warehouse Configurations](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span></span>  

<span data-ttu-id="a4388-108">Voit myös määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in kirjaamaan (*materiaalioton*) komponentit automaattisesti, kun aloitat tai päätät tuotantotilauksia.</span><span class="sxs-lookup"><span data-stu-id="a4388-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="a4388-109">Lisätietoja on kohdassa [Komponenttien materiaalinoton ottaminen käyttöön toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="a4388-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="a4388-110">Vähintään yhden tuotantotilausrivin kulutuksen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="a4388-110">To post consumption for one or more production order lines</span></span>

1. <span data-ttu-id="a4388-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kulutuskirjauskansio** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a4388-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a4388-112">Täytä kentät tuotantotilauksen tiedoilla ja kulutustiedoilla.</span><span class="sxs-lookup"><span data-stu-id="a4388-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="a4388-113">Käytä **Laskenta perustuu** -toimintoa luomaan päiväkirjarivejä tuotantotilauksista todellisen tuotoksen (raportoitujen, valmiiden tavaroiden määrän) vai oletetun tuotoksen (valmiiden tavaroiden määrän, jonka oletat tuottavasi) perusteella.</span><span class="sxs-lookup"><span data-stu-id="a4388-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4388-114">Jos sijaintikortti määritettiin edellyttämään fyysisen varaston poiminnan käsittelyä, vain jo varastotoiminnolla poimitut määrät voidaan antaa **Määrä**-kentässä **Kulutuskirjauskansio**-sivulla minkä tahansa lasketun määrän sijaan.</span><span class="sxs-lookup"><span data-stu-id="a4388-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="a4388-115">Lisätietoja on kohdassa [Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="a4388-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3. <span data-ttu-id="a4388-116">Kirjaa kulutus valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="a4388-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="a4388-117">Liittyviä varastoja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="a4388-117">The related inventories are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4388-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a4388-118">See Also</span></span>

[<span data-ttu-id="a4388-119">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="a4388-119">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="a4388-120">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a4388-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="a4388-121">Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="a4388-121">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="a4388-122">Varasto</span><span class="sxs-lookup"><span data-stu-id="a4388-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a4388-123">Osto</span><span class="sxs-lookup"><span data-stu-id="a4388-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a4388-124">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a4388-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]
