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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d4b7f90ac533b3071a8c520eefacf98eddd1faba
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919111"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="6cbfa-103">Tuotannon kulutuksen eräkirjaus</span><span class="sxs-lookup"><span data-stu-id="6cbfa-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="6cbfa-104">Jos materiaalinottotapa on **Manuaalinen**, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="6cbfa-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="6cbfa-105">Voit määrittää järjestelmän myös kirjaamaan (*materiaalioton*) komponentit automaattisesti, kun aloitat tai päätät tuotantotilauksia.</span><span class="sxs-lookup"><span data-stu-id="6cbfa-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="6cbfa-106">Lisätietoja on kohdassa [Komponenttien materiaalinoton ottaminen käyttöön toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="6cbfa-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="6cbfa-107">Vähintään yhden tuotantotilausrivin kulutuksen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="6cbfa-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="6cbfa-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kulutuskirjauskansio** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6cbfa-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6cbfa-109">Täytä kentät tuotantotilauksen tiedoilla ja kulutustiedoilla.</span><span class="sxs-lookup"><span data-stu-id="6cbfa-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="6cbfa-110">Jos komponentteja säilyttävä fyysisen varaston sijainti on määritetty käyttämään varastopaikkoja, mutta ei vaadi poimintaa, määritä päiväkirjan riville varastopaikkakoodi osoittamaan, mistä nimikkeet otetaan fyysisen varaston sisällä.</span><span class="sxs-lookup"><span data-stu-id="6cbfa-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="6cbfa-111">Lisätietoja on kohdassa [Tuotannon tai kokoonpanon poiminta](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="6cbfa-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="6cbfa-112">Kirjaa kulutus valitsemalla **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="6cbfa-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="6cbfa-113">Liittyviä nimiketapahtumia vähennetään.</span><span class="sxs-lookup"><span data-stu-id="6cbfa-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cbfa-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6cbfa-114">See Also</span></span>  
<span data-ttu-id="6cbfa-115">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="6cbfa-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="6cbfa-116">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6cbfa-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="6cbfa-117">[Suunnittelu](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="6cbfa-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="6cbfa-118">Varasto</span><span class="sxs-lookup"><span data-stu-id="6cbfa-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6cbfa-119">Osto</span><span class="sxs-lookup"><span data-stu-id="6cbfa-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6cbfa-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6cbfa-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
