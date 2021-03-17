---
title: Kustannusbudjettitapahtumien poistaminen | Microsoft Docs
description: Voit käyttää Poista kustannusbudjettitapahtumat -eräajoa peruuttaaksesi kustannusbudjetin tapahtumat kustannusbudjetinrekisteristä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b4c81aa62f3548819db3451130c49fd11984b33a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387372"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="d6544-103">Poista kustannusbudjettitapahtumat</span><span class="sxs-lookup"><span data-stu-id="d6544-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="d6544-104">Voit käyttää **Poista kustannusbudjettitapahtumat** -eräajoa peruuttaaksesi kustannusbudjetin tapahtumat kustannusbudjetinrekisteristä.</span><span class="sxs-lookup"><span data-stu-id="d6544-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="d6544-105">Välttääksesi aukkoja kustannusbudjeteissa ja kustannusrekisteritapahtumissa et voi poistaa yhtä tapahtumaa tai tapahtumia keskellä rekisteritapahtumien luetteloa.</span><span class="sxs-lookup"><span data-stu-id="d6544-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="d6544-106">Poista kustannusbudjettitapahtumat</span><span class="sxs-lookup"><span data-stu-id="d6544-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="d6544-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poista kustannusbudjettitapahtumat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d6544-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="d6544-108">**Rekisteriin nro** -kentässä</span><span class="sxs-lookup"><span data-stu-id="d6544-108">The **To Register No.**</span></span> <span data-ttu-id="d6544-109">on viimeisen rekisteritapahtuman numero, eikä sitä voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="d6544-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="d6544-110">Voit käyttää **Rekisteristä nro** -kenttää</span><span class="sxs-lookup"><span data-stu-id="d6544-110">You can use the **From Register No.**</span></span> <span data-ttu-id="d6544-111">valitaksesi rekisteritapahtuman numeron, josta poisto pitäisi alkaa.</span><span class="sxs-lookup"><span data-stu-id="d6544-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="d6544-112">Valitse **OK** poistaaksesi valitut kustannusbudjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="d6544-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d6544-113">Vältä kustannusbudjettien poistoa epähuomiossa ja sulje rekisteritapahtumat merkitsemällä rivit **Suljetuiksi** **Suljettu** -kentässä **Kustannusbudjettirekisterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d6544-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6544-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d6544-114">See Also</span></span>  
<span data-ttu-id="d6544-115">[Kustannuslaskenta](finance-manage-cost-accounting.md)
[Kustannusbudjettien luominen](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="d6544-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="d6544-116">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6544-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]