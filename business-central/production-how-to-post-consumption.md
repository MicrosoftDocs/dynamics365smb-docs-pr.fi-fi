---
title: Kulutuksen eräkirjaus | Microsoft Docs
description: Jos materiaalinottotapa on **Manuaalinen**, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9200256cec074e547bc594950b1eb2d975a8ad9b
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877881"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="61e59-103">Tuotannon kulutuksen eräkirjaus</span><span class="sxs-lookup"><span data-stu-id="61e59-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="61e59-104">Jos materiaalinottotapa on **Manuaalinen**, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="61e59-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="61e59-105">Voit määrittää järjestelmän myös kirjaamaan (*materiaalioton*) komponentit automaattisesti, kun aloitat tai päätät tuotantotilauksia.</span><span class="sxs-lookup"><span data-stu-id="61e59-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="61e59-106">Lisätietoja on kohdassa [Komponenttien materiaalinoton ottaminen käyttöön toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="61e59-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="61e59-107">Vähintään yhden tuotantotilausrivin kulutuksen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="61e59-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="61e59-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kulutuskirjauskansio** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="61e59-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="61e59-109">Täytä kentät tuotantotilauksen tiedoilla ja kulutustiedoilla.</span><span class="sxs-lookup"><span data-stu-id="61e59-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="61e59-110">Jos komponentteja säilyttävä fyysisen varaston sijainti on määritetty käyttämään varastopaikkoja, mutta ei vaadi poimintaa, määritä päiväkirjan riville varastopaikkakoodi osoittamaan, mistä nimikkeet otetaan fyysisen varaston sisällä.</span><span class="sxs-lookup"><span data-stu-id="61e59-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="61e59-111">Lisätietoja on kohdassa [Tuotannon tai kokoonpanon poiminta](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="61e59-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="61e59-112">Kirjaa kulutus valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="61e59-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="61e59-113">Liittyviä nimiketapahtumia vähennetään.</span><span class="sxs-lookup"><span data-stu-id="61e59-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="61e59-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="61e59-114">See Also</span></span>  
<span data-ttu-id="61e59-115">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="61e59-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="61e59-116">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="61e59-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="61e59-117">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="61e59-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="61e59-118">Varasto</span><span class="sxs-lookup"><span data-stu-id="61e59-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="61e59-119">Osto</span><span class="sxs-lookup"><span data-stu-id="61e59-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="61e59-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61e59-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
