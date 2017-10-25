---
title: Kustannusbudjettitapahtumien poistaminen | Microsoft Docs
description: "Voit peruuttaa **Poista kustannusbudjettitapahtumat** -eräajolla kustannusbudjetin tapahtumat kustannusbudjetinrekisteristä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 79c9a58c7cb91ce922b81eec1d2ccad375943203
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-delete-cost-budget-entries"></a><span data-ttu-id="03b12-103">Kustannusbudjettitapahtumien poistaminen</span><span class="sxs-lookup"><span data-stu-id="03b12-103">How to: Delete Cost Budget Entries</span></span>
<span data-ttu-id="03b12-104">Voit käyttää **Poista kustannusbudjettitapahtumat** -eräajoa peruuttaaksesi kustannusbudjetin tapahtumat kustannusbudjetinrekisteristä.</span><span class="sxs-lookup"><span data-stu-id="03b12-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="03b12-105">Välttääksesi aukkoja kustannusbudjeteissa ja kustannusrekisteritapahtumissa et voi poistaa yhtä tapahtumaa tai tapahtumia keskellä rekisteritapahtumien luetteloa.</span><span class="sxs-lookup"><span data-stu-id="03b12-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="03b12-106">Poista kustannusbudjettitapahtumat</span><span class="sxs-lookup"><span data-stu-id="03b12-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="03b12-107">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista kustannusbudjettitapahtumat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="03b12-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="03b12-108">**Rekisteriin nro** -kentässä</span><span class="sxs-lookup"><span data-stu-id="03b12-108">The **To Register No.**</span></span> <span data-ttu-id="03b12-109">on viimeisen rekisteritapahtuman numero, eikä sitä voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="03b12-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="03b12-110">Voit käyttää **Rekisteristä nro** -kenttää</span><span class="sxs-lookup"><span data-stu-id="03b12-110">You can use the **From Register No.**</span></span> <span data-ttu-id="03b12-111">valitaksesi rekisteritapahtuman numeron, josta poisto pitäisi alkaa.</span><span class="sxs-lookup"><span data-stu-id="03b12-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="03b12-112">Valitse **OK** poistaaksesi valitut kustannusbudjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="03b12-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="03b12-113">Vältä kustannusbudjettien poistoa epähuomiossa ja sulje rekisteritapahtumat merkitsemällä rivit **Suljetuiksi** **Suljettu** -kentässä **Kustannusbudjettirekisterit** ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="03b12-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field in the **Cost Budget Registers** window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="03b12-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="03b12-114">See Also</span></span>  
<span data-ttu-id="03b12-115">[Kustannuslaskenta](finance-manage-cost-accounting.md)
[Kustannusbudjettien luominen](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="03b12-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="03b12-116">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="03b12-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

