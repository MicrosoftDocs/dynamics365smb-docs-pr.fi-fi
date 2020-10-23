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
ms.openlocfilehash: 2ff0ede7bd5d90607a04b1037f5b6c6d092c1c33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916141"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="00e77-103">Poista kustannusbudjettitapahtumat</span><span class="sxs-lookup"><span data-stu-id="00e77-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="00e77-104">Voit käyttää **Poista kustannusbudjettitapahtumat** -eräajoa peruuttaaksesi kustannusbudjetin tapahtumat kustannusbudjetinrekisteristä.</span><span class="sxs-lookup"><span data-stu-id="00e77-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="00e77-105">Välttääksesi aukkoja kustannusbudjeteissa ja kustannusrekisteritapahtumissa et voi poistaa yhtä tapahtumaa tai tapahtumia keskellä rekisteritapahtumien luetteloa.</span><span class="sxs-lookup"><span data-stu-id="00e77-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="00e77-106">Poista kustannusbudjettitapahtumat</span><span class="sxs-lookup"><span data-stu-id="00e77-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="00e77-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poista kustannusbudjettitapahtumat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="00e77-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="00e77-108">**Rekisteriin nro** -kentässä</span><span class="sxs-lookup"><span data-stu-id="00e77-108">The **To Register No.**</span></span> <span data-ttu-id="00e77-109">on viimeisen rekisteritapahtuman numero, eikä sitä voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="00e77-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="00e77-110">Voit käyttää **Rekisteristä nro** -kenttää</span><span class="sxs-lookup"><span data-stu-id="00e77-110">You can use the **From Register No.**</span></span> <span data-ttu-id="00e77-111">valitaksesi rekisteritapahtuman numeron, josta poisto pitäisi alkaa.</span><span class="sxs-lookup"><span data-stu-id="00e77-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="00e77-112">Valitse **OK** poistaaksesi valitut kustannusbudjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="00e77-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="00e77-113">Vältä kustannusbudjettien poistoa epähuomiossa ja sulje rekisteritapahtumat merkitsemällä rivit **Suljetuiksi** **Suljettu** -kentässä **Kustannusbudjettirekisterit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="00e77-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="00e77-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="00e77-114">See Also</span></span>  
<span data-ttu-id="00e77-115">[Kustannuslaskenta](finance-manage-cost-accounting.md)
[Kustannusbudjettien luominen](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="00e77-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="00e77-116">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="00e77-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
