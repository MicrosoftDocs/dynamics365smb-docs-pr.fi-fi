---
title: Tuotannon nimikeperheiden käyttäminen | Microsoft Docs
description: Päätehtävä peruskalenterin räätälöimisessä yrityksellesi tai yhdelle sen liiketoimintakumppaneista on syöttää kaikki työskentely- ja ei-työskentelypäivätilan muutokset.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4c926b8f7663c805f07bcd7c85339b109f85a7ff
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383198"
---
# <a name="work-with-production-families"></a><span data-ttu-id="68327-103">Tuotantoperheiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="68327-103">Work with Production Families</span></span>
<span data-ttu-id="68327-104">Tuoteperhe on ryhmä yksittäisiä nimikkeitä, joiden suhde perustuu niiden tuotantoprosessien samankaltaisuuteen.</span><span class="sxs-lookup"><span data-stu-id="68327-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="68327-105">Tuoteperheitä muodostamalla joitain nimikkeitä voidaan tuottaa kaksi kertaa tai useammin yhdessä tuotannossa, joka optimoi materiaalinkulutusta.</span><span class="sxs-lookup"><span data-stu-id="68327-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="68327-106">Anna **Tuoteperhe**-sivun **Määrä**-kentässä määrä, joka tuotetaan, kun koko tuoteperhe on tuotettu kerran.</span><span class="sxs-lookup"><span data-stu-id="68327-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="68327-107">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="68327-107">Example</span></span>
<span data-ttu-id="68327-108">Lävistysprosessissa saman nimikkeen neljä kappaletta voidaan tuottaa yhdestä lomakkeesta ja toisen, eri nimikkeen, 10 kappaletta yhtä aikaa.</span><span class="sxs-lookup"><span data-stu-id="68327-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="68327-109">Lävistyskone lävistää kaikki 14 kappaletta saman työvaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="68327-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="68327-110">Tuoteperheiden muodostamisella vähennetään hukkatavaran määrää, koska se, mikä olisi tavallisesti hylättyä tavaraa isojen kappaleiden tuotannossa, käytetäänkin pienempien nimikkeiden tuottamisessa.</span><span class="sxs-lookup"><span data-stu-id="68327-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="68327-111">Tuotantoperheen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="68327-111">To set up a production family</span></span>
1. <span data-ttu-id="68327-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Perheet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="68327-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="68327-113">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="68327-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="68327-114">Tuotanto tuoteperheen perusteella</span><span class="sxs-lookup"><span data-stu-id="68327-114">To produce based on a production family</span></span>
1. <span data-ttu-id="68327-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="68327-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="68327-116">Luo uusi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="68327-116">Create a new production order.</span></span> <span data-ttu-id="68327-117">Lisätietoja on kohdassa [Tuotantotilausten luominen](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="68327-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="68327-118">Valitse **Lähdetyyppi**-kentässä **Tuoteperhe**.</span><span class="sxs-lookup"><span data-stu-id="68327-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="68327-119">Valitse **Lähdenro** -kentässä käsiteltävä tuotantoperhe.</span><span class="sxs-lookup"><span data-stu-id="68327-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="68327-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="68327-120">See Also</span></span>
[<span data-ttu-id="68327-121">Tuotannon tuoterakenteiden luominen</span><span class="sxs-lookup"><span data-stu-id="68327-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="68327-122">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="68327-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="68327-123">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="68327-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="68327-124">[Suunnittelu](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="68327-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="68327-125">Varasto</span><span class="sxs-lookup"><span data-stu-id="68327-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="68327-126">Osto</span><span class="sxs-lookup"><span data-stu-id="68327-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="68327-127">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="68327-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]