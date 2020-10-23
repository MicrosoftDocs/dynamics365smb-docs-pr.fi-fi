---
title: Uusien arvotapahtumien luominen varastossa oleville nimikkeille| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten vähintään yhden varaston nimikkeen arvotapahtumaa nostetaan tai lasketaan kirjaamalla nimikkeen nykyinen laskettu arvo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b29e93d248e939eb9eb1cea97e53cd1718304e80
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923793"
---
# <a name="revalue-inventory"></a><span data-ttu-id="26acb-103">Varaston uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="26acb-103">Revalue Inventory</span></span>
<span data-ttu-id="26acb-104">Jos haluat nostaa tai laskea nimikkeen tai tietyn nimiketapahtuman varastoarvoa, sinun tulee käyttää uudelleenarvostuspäiväkirjaa.</span><span class="sxs-lookup"><span data-stu-id="26acb-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="26acb-105">Varaston uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="26acb-105">To revalue inventory</span></span>
1. <span data-ttu-id="26acb-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Uudelleenarvostus pvk** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="26acb-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="26acb-107">Valitse **Laske varaston arvo** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="26acb-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="26acb-108">Täytä **Laske varaston arvo** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="26acb-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="26acb-109">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="26acb-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="26acb-110">Syötä uusi yksikkökustannus **Uudelleenarvostus pvk** -sivun kuhunkin **Yks.kust. (uudelleenarvostet.)** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="26acb-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="26acb-111">Vaihtoehtoisesti voit syöttää uuden kokonaissumman **Var. arvo (uudell.arvostettu)** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="26acb-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="26acb-112">Asianmukaiset kentät päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="26acb-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="26acb-113">Huomaa että **Summa**-kentässä on varaston arvon todellinen muutos valitun nimiketapahtuman osalta.</span><span class="sxs-lookup"><span data-stu-id="26acb-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="26acb-114">Ohjelma laskee **Varaston arvo (laskettu)** -kentän ja **Var. arvo (uudell.arvostettu)** -kentän erotuksen.</span><span class="sxs-lookup"><span data-stu-id="26acb-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="26acb-115">Kun olet saanut kaikki uudelleenarvostuspäiväkirjan rivit valmiiksi, valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="26acb-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="26acb-116">Kirjaamiasi uudelleenarvostuksia vastaavat uudet arvotapahtumat on nyt luotu.</span><span class="sxs-lookup"><span data-stu-id="26acb-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="26acb-117">Uudet arvot näkyvät vastaavissa nimikekorteissa.</span><span class="sxs-lookup"><span data-stu-id="26acb-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="26acb-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="26acb-118">See Also</span></span>
[<span data-ttu-id="26acb-119">Rakennetiedot: uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="26acb-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="26acb-120">Varasto</span><span class="sxs-lookup"><span data-stu-id="26acb-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="26acb-121">Myynti</span><span class="sxs-lookup"><span data-stu-id="26acb-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="26acb-122">Osto</span><span class="sxs-lookup"><span data-stu-id="26acb-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="26acb-123">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26acb-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
