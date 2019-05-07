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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 602381b34a057120cc53deca4dd293f939777dc5
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2019
ms.locfileid: "939009"
---
# <a name="revalue-inventory"></a><span data-ttu-id="afd21-103">Varaston uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="afd21-103">Revalue Inventory</span></span>
<span data-ttu-id="afd21-104">Jos haluat nostaa tai laskea nimikkeen tai tietyn nimiketapahtuman varastoarvoa, sinun tulee käyttää uudelleenarvostuspäiväkirjaa.</span><span class="sxs-lookup"><span data-stu-id="afd21-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="afd21-105">Varaston uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="afd21-105">To revalue inventory</span></span>
1. <span data-ttu-id="afd21-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Uudelleenarvostuspvk** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="afd21-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="afd21-107">Valitse **Laske varaston arvo** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="afd21-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="afd21-108">Täytä **Laske varaston arvo** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="afd21-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="afd21-109">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="afd21-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="afd21-110">Syötä uusi yksikkökustannus **Uudelleenarvostus pvk** -sivun kuhunkin **Yks.kust. (uudelleenarvostet.)** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="afd21-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="afd21-111">Vaihtoehtoisesti voit syöttää uuden kokonaissumman **Var. arvo (uudell.arvostettu)** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="afd21-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="afd21-112">Asianmukaiset kentät päivitetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="afd21-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="afd21-113">Huomaa että **Summa**-kentässä on varaston arvon todellinen muutos valitun nimiketapahtuman osalta.</span><span class="sxs-lookup"><span data-stu-id="afd21-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="afd21-114">Ohjelma laskee **Varaston arvo (laskettu)** -kentän ja **Var. arvo (uudell.arvostettu)** -kentän erotuksen.</span><span class="sxs-lookup"><span data-stu-id="afd21-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="afd21-115">Kun olet saanut kaikki uudelleenarvostuspäiväkirjan rivit valmiiksi, valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="afd21-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="afd21-116">Kirjaamiasi uudelleenarvostuksia vastaavat uudet arvotapahtumat on nyt luotu.</span><span class="sxs-lookup"><span data-stu-id="afd21-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="afd21-117">Uudet arvot näkyvät vastaavissa nimikekorteissa.</span><span class="sxs-lookup"><span data-stu-id="afd21-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="afd21-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="afd21-118">See Also</span></span>
[<span data-ttu-id="afd21-119">Rakennetiedot: uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="afd21-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="afd21-120">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="afd21-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="afd21-121">Myynti</span><span class="sxs-lookup"><span data-stu-id="afd21-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="afd21-122">Osto</span><span class="sxs-lookup"><span data-stu-id="afd21-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="afd21-123">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="afd21-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
