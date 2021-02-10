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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 47ae132d862d2c05bef4ea0d0af26688bdd16588
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758215"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="f9c23-103">Tulosta poimintaluettelo</span><span class="sxs-lookup"><span data-stu-id="f9c23-103">Print the Picking List</span></span>
<span data-ttu-id="f9c23-104">Voit tulostaa varaston poimintaluettelon suoraan myyntitilauksesta, myyntilaskusta tai mistä tahansa muusta asiakirjasta, joka aloittaa tavaroiden lähettämisen.</span><span class="sxs-lookup"><span data-stu-id="f9c23-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="f9c23-105">Tätä raporttia käytetään tyypillisesti yrityksissä, joissa ei ole erillisiä toimintoja varastoinnin hallintaan, joten varastotyöntekijä voi yksinkertaisesti tarkastella tai tulostaa poimintaluetteloa asiaan liittyvällä myyntiasiakirjalla.</span><span class="sxs-lookup"><span data-stu-id="f9c23-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="f9c23-106">Yrityksissä, joiden prosessit ovat suurempia tai monimutkaisempia, poiminta suunnitellaan ja suoritetaan erityisen fyysisen varastoinnin asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="f9c23-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="f9c23-107">Lisätietoja on kohdassa [Nimikkeiden poimiminen](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="f9c23-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="f9c23-108">Varaston poimintaluettelon tulostaminen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="f9c23-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="f9c23-109">Seuraava toimenpide perustuu myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f9c23-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="f9c23-110">Vaiheet ovat samanlaiset kaikissa myyntiasiakirjoissa, joita voidaan käyttää nimikkeiden toimituksen käynnistämiseen.</span><span class="sxs-lookup"><span data-stu-id="f9c23-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="f9c23-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f9c23-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f9c23-112">Avaa myyntitilaus, johon haluat poimia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="f9c23-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="f9c23-113">Valitse **Raportti**-toiminto ja valitse sitten **Poimintaluettelo tilauksen mukaan**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f9c23-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="f9c23-114">Valitse **Tulosta**-painike, jos haluat tulostaa poimintaluettelon, tai valitse **Esikatselu**, jos haluat katsella raporttia näytössä.</span><span class="sxs-lookup"><span data-stu-id="f9c23-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="f9c23-115">Voit myös tallentaa poimintaluettelon asiakirjana, esimerkiksi lähettääksesi sen jollekulle tai lisätäksesi sen liitteenä myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f9c23-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="f9c23-116">Lue lisätietoja kohteesta [Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta](ui-how-add-link-to-record.md)</span><span class="sxs-lookup"><span data-stu-id="f9c23-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f9c23-117">Jos käytit myyntitilauksessa **Pura tuoterakenne** -toimintoa, vain asiaan liittyvän kokoonpanonimikkeen komponentit näkyvät raportissa.</span><span class="sxs-lookup"><span data-stu-id="f9c23-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="f9c23-118">Lisätietoja on kohdassa [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="f9c23-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f9c23-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f9c23-119">See Also</span></span>  
[<span data-ttu-id="f9c23-120">Varasto</span><span class="sxs-lookup"><span data-stu-id="f9c23-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f9c23-121">Nimikkeiden poiminta</span><span class="sxs-lookup"><span data-stu-id="f9c23-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="f9c23-122">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f9c23-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>   
