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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c961d15d04da5fcad18a460adc269f3099962f6a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182130"
---
# <a name="revalue-inventory"></a><span data-ttu-id="36912-103">Varaston uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="36912-103">Revalue Inventory</span></span>
<span data-ttu-id="36912-104">Jos haluat nostaa tai laskea nimikkeen tai tietyn nimiketapahtuman varastoarvoa, sinun tulee käyttää uudelleenarvostuspäiväkirjaa.</span><span class="sxs-lookup"><span data-stu-id="36912-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="36912-105">Varaston uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="36912-105">To revalue inventory</span></span>
1. <span data-ttu-id="36912-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Uudelleenarvostus pvk** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="36912-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="36912-107">Valitse **Laske varaston arvo** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="36912-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="36912-108">Täytä **Laske varaston arvo** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="36912-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="36912-109">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="36912-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="36912-110">Syötä uusi yksikkökustannus **Uudelleenarvostus pvk** -sivun kuhunkin **Yks.kust. (uudelleenarvostet.)** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36912-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="36912-111">Vaihtoehtoisesti voit syöttää uuden kokonaissumman **Var. arvo (uudell.arvostettu)** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36912-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="36912-112">Asianmukaiset kentät päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="36912-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="36912-113">Huomaa että **Summa**-kentässä on varaston arvon todellinen muutos valitun nimiketapahtuman osalta.</span><span class="sxs-lookup"><span data-stu-id="36912-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="36912-114">Ohjelma laskee **Varaston arvo (laskettu)** -kentän ja **Var. arvo (uudell.arvostettu)** -kentän erotuksen.</span><span class="sxs-lookup"><span data-stu-id="36912-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="36912-115">Kun olet saanut kaikki uudelleenarvostuspäiväkirjan rivit valmiiksi, valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="36912-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="36912-116">Kirjaamiasi uudelleenarvostuksia vastaavat uudet arvotapahtumat on nyt luotu.</span><span class="sxs-lookup"><span data-stu-id="36912-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="36912-117">Uudet arvot näkyvät vastaavissa nimikekorteissa.</span><span class="sxs-lookup"><span data-stu-id="36912-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="36912-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="36912-118">See Also</span></span>
[<span data-ttu-id="36912-119">Rakennetiedot: uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="36912-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="36912-120">Varasto</span><span class="sxs-lookup"><span data-stu-id="36912-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="36912-121">Myynti</span><span class="sxs-lookup"><span data-stu-id="36912-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="36912-122">Osto</span><span class="sxs-lookup"><span data-stu-id="36912-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="36912-123">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="36912-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
