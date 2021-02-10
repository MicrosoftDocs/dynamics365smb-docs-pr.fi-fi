---
title: Kustannusbudjettitapahtumien poistaminen | Microsoft Docs
description: Voit käyttää Poista kustannusbudjettitapahtumat -eräajoa peruuttaaksesi kustannusbudjetin tapahtumat kustannusbudjetinrekisteristä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f7ea29f059c3d2ab54e35b731bfe72d42fffd1f1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750703"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="a212b-103">Poista kustannusbudjettitapahtumat</span><span class="sxs-lookup"><span data-stu-id="a212b-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="a212b-104">Voit käyttää **Poista kustannusbudjettitapahtumat** -eräajoa peruuttaaksesi kustannusbudjetin tapahtumat kustannusbudjetinrekisteristä.</span><span class="sxs-lookup"><span data-stu-id="a212b-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="a212b-105">Välttääksesi aukkoja kustannusbudjeteissa ja kustannusrekisteritapahtumissa et voi poistaa yhtä tapahtumaa tai tapahtumia keskellä rekisteritapahtumien luetteloa.</span><span class="sxs-lookup"><span data-stu-id="a212b-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="a212b-106">Poista kustannusbudjettitapahtumat</span><span class="sxs-lookup"><span data-stu-id="a212b-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="a212b-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poista kustannusbudjettitapahtumat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a212b-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="a212b-108">**Rekisteriin nro** -kentässä</span><span class="sxs-lookup"><span data-stu-id="a212b-108">The **To Register No.**</span></span> <span data-ttu-id="a212b-109">on viimeisen rekisteritapahtuman numero, eikä sitä voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="a212b-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="a212b-110">Voit käyttää **Rekisteristä nro** -kenttää</span><span class="sxs-lookup"><span data-stu-id="a212b-110">You can use the **From Register No.**</span></span> <span data-ttu-id="a212b-111">valitaksesi rekisteritapahtuman numeron, josta poisto pitäisi alkaa.</span><span class="sxs-lookup"><span data-stu-id="a212b-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="a212b-112">Valitse **OK** poistaaksesi valitut kustannusbudjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a212b-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a212b-113">Vältä kustannusbudjettien poistoa epähuomiossa ja sulje rekisteritapahtumat merkitsemällä rivit **Suljetuiksi** **Suljettu** -kentässä **Kustannusbudjettirekisterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a212b-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a212b-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a212b-114">See Also</span></span>  
<span data-ttu-id="a212b-115">[Kustannuslaskenta](finance-manage-cost-accounting.md)
[Kustannusbudjettien luominen](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="a212b-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="a212b-116">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a212b-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
