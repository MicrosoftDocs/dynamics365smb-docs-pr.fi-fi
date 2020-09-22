---
title: Tuotannon nimikeperheiden käyttäminen | Microsoft Docs
description: Päätehtävä peruskalenterin räätälöimisessä yrityksellesi tai yhdelle sen liiketoimintakumppaneista on syöttää kaikki työskentely- ja ei-työskentelypäivätilan muutokset.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 9400e2cc52501b333f71368af556fdeacb1f10c5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784030"
---
# <a name="work-with-production-families"></a><span data-ttu-id="290d6-103">Tuotantoperheiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="290d6-103">Work with Production Families</span></span>
<span data-ttu-id="290d6-104">Tuoteperhe on ryhmä yksittäisiä nimikkeitä, joiden suhde perustuu niiden tuotantoprosessien samankaltaisuuteen.</span><span class="sxs-lookup"><span data-stu-id="290d6-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="290d6-105">Tuoteperheitä muodostamalla joitain nimikkeitä voidaan tuottaa kaksi kertaa tai useammin yhdessä tuotannossa, joka optimoi materiaalinkulutusta.</span><span class="sxs-lookup"><span data-stu-id="290d6-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="290d6-106">Anna **Tuoteperhe**-sivun **Määrä**-kentässä määrä, joka tuotetaan, kun koko tuoteperhe on tuotettu kerran.</span><span class="sxs-lookup"><span data-stu-id="290d6-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="290d6-107">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="290d6-107">Example</span></span>
<span data-ttu-id="290d6-108">Lävistysprosessissa saman nimikkeen neljä kappaletta voidaan tuottaa yhdestä lomakkeesta ja toisen, eri nimikkeen, 10 kappaletta yhtä aikaa.</span><span class="sxs-lookup"><span data-stu-id="290d6-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="290d6-109">Lävistyskone lävistää kaikki 14 kappaletta saman työvaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="290d6-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="290d6-110">Tuoteperheiden muodostamisella vähennetään hukkatavaran määrää, koska se, mikä olisi tavallisesti hylättyä tavaraa isojen kappaleiden tuotannossa, käytetäänkin pienempien nimikkeiden tuottamisessa.</span><span class="sxs-lookup"><span data-stu-id="290d6-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="290d6-111">Tuotantoperheen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="290d6-111">To set up a production family</span></span>
1. <span data-ttu-id="290d6-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Perheet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="290d6-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="290d6-113">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="290d6-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="290d6-114">Tuotanto tuoteperheen perusteella</span><span class="sxs-lookup"><span data-stu-id="290d6-114">To produce based on a production family</span></span>
1. <span data-ttu-id="290d6-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="290d6-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="290d6-116">Luo uusi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="290d6-116">Create a new production order.</span></span> <span data-ttu-id="290d6-117">Lisätietoja on kohdassa [Tuotantotilausten luominen](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="290d6-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="290d6-118">Valitse **Lähdetyyppi**-kentässä **Tuoteperhe**.</span><span class="sxs-lookup"><span data-stu-id="290d6-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="290d6-119">Valitse **Lähdenro** -kentässä käsiteltävä tuotantoperhe.</span><span class="sxs-lookup"><span data-stu-id="290d6-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="290d6-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="290d6-120">See Also</span></span>
[<span data-ttu-id="290d6-121">Tuotannon tuoterakenteiden luominen</span><span class="sxs-lookup"><span data-stu-id="290d6-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="290d6-122">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="290d6-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="290d6-123">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="290d6-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="290d6-124">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="290d6-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="290d6-125">Varasto</span><span class="sxs-lookup"><span data-stu-id="290d6-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="290d6-126">Osto</span><span class="sxs-lookup"><span data-stu-id="290d6-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="290d6-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="290d6-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
