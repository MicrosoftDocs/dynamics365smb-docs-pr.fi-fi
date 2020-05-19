---
title: Kuinka varaston poimintaluettelo tulostetaan myyntitilauksesta
description: Voit tulostaa varaston poimintaluettelon suoraan myyntitilauksesta, myynnistä, laskusta ja muista lähtevistä myyntiasiakirjoista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: d5eaad5279445375ec00fdf42dd48bffa5d03645
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324463"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="28bd2-103">Tulosta poimintaluettelo</span><span class="sxs-lookup"><span data-stu-id="28bd2-103">Print the Picking List</span></span>
<span data-ttu-id="28bd2-104">Voit tulostaa varaston poimintaluettelon suoraan myyntitilauksesta, myyntilaskusta tai mistä tahansa muusta asiakirjasta, joka aloittaa tavaroiden lähettämisen.</span><span class="sxs-lookup"><span data-stu-id="28bd2-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="28bd2-105">Tätä raporttia käytetään tyypillisesti yrityksissä, joissa ei ole erillisiä toimintoja varastoinnin hallintaan, joten varastotyöntekijä voi yksinkertaisesti tarkastella tai tulostaa poimintaluetteloa asiaan liittyvällä myyntiasiakirjalla.</span><span class="sxs-lookup"><span data-stu-id="28bd2-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="28bd2-106">Yrityksissä, joiden prosessit ovat suurempia tai monimutkaisempia, poiminta suunnitellaan ja suoritetaan erityisen fyysisen varastoinnin asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="28bd2-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="28bd2-107">Lisätietoja on kohdassa [Nimikkeiden poimiminen](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="28bd2-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="28bd2-108">Varaston poimintaluettelon tulostaminen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="28bd2-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="28bd2-109">Seuraava toimenpide perustuu myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="28bd2-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="28bd2-110">Vaiheet ovat samanlaiset kaikissa myyntiasiakirjoissa, joita voidaan käyttää nimikkeiden toimituksen käynnistämiseen.</span><span class="sxs-lookup"><span data-stu-id="28bd2-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="28bd2-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="28bd2-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="28bd2-112">Avaa myyntitilaus, johon haluat poimia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="28bd2-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="28bd2-113">Valitse **Raportti**-toiminto ja valitse sitten **Poimintaluettelo tilauksen mukaan**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="28bd2-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="28bd2-114">Valitse **Tulosta**-painike, jos haluat tulostaa poimintaluettelon, tai valitse **Esikatselu**, jos haluat katsella raporttia näytössä.</span><span class="sxs-lookup"><span data-stu-id="28bd2-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="28bd2-115">Voit myös tallentaa poimintaluettelon asiakirjana, esimerkiksi lähettääksesi sen jollekulle tai lisätäksesi sen liitteenä myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="28bd2-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="28bd2-116">Lue lisätietoja kohteesta [Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta](ui-how-add-link-to-record.md)</span><span class="sxs-lookup"><span data-stu-id="28bd2-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="28bd2-117">Jos käytit myyntitilauksessa **Pura tuoterakenne** -toimintoa, vain asiaan liittyvän kokoonpanonimikkeen komponentit näkyvät raportissa.</span><span class="sxs-lookup"><span data-stu-id="28bd2-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="28bd2-118">Lisätietoja on kohdassa [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="28bd2-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="28bd2-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="28bd2-119">See Also</span></span>  
[<span data-ttu-id="28bd2-120">Varasto</span><span class="sxs-lookup"><span data-stu-id="28bd2-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="28bd2-121">Nimikkeiden poiminta</span><span class="sxs-lookup"><span data-stu-id="28bd2-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="28bd2-122">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="28bd2-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>   
