---
title: Uusien asiakkaiden rekisteröinti asiakkaan kortin luonnin avulla | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten asiakkaan kortti luodaan rekisteröimään tietoja kustakin uudesta asiakkaasta, jolle myyt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 06/24/2020
ms.author: edupont
ms.openlocfilehash: 3e25756cff974e0db835f5e3ed3247dff6d7624a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780882"
---
# <a name="register-new-customers"></a><span data-ttu-id="8b41c-103">Uusien asiakkaiden rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="8b41c-103">Register New Customers</span></span>

<span data-ttu-id="8b41c-104">Asiakkaat ovat tulonlähteesi.</span><span class="sxs-lookup"><span data-stu-id="8b41c-104">Customers are the source of your income.</span></span> <span data-ttu-id="8b41c-105">Jokainen asiakas, jolle myyt, on rekisteröitävä asiakaskorttina.</span><span class="sxs-lookup"><span data-stu-id="8b41c-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="8b41c-106">Asiakkaan kortit sisältävät tietoja, jotka tarvitaan tuotteiden asiakkaalle myymistä varten.</span><span class="sxs-lookup"><span data-stu-id="8b41c-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="8b41c-107">Lisätietoja on kohdissa [Myynnin laskutus](sales-how-invoice-sales.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="8b41c-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="8b41c-108">Ennen kuin voit rekisteröidä uusia asiakkaita, sinun on määritettävä myyntikoodit, jotka voidaan valita asiakkaiden korttien täyttämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8b41c-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="8b41c-109">Lisätietoja on kohdassa [Myynnin määrittäminen](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="8b41c-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a><span data-ttu-id="8b41c-110">Uusien asiakkaiden lisääminen</span><span class="sxs-lookup"><span data-stu-id="8b41c-110">Adding new customers</span></span>

<span data-ttu-id="8b41c-111">Uusi asiakas rekisteröidään täyttämällä asiakaskortti.</span><span class="sxs-lookup"><span data-stu-id="8b41c-111">To register a new customer, you must fill in a customer card.</span></span> <span data-ttu-id="8b41c-112">Eri asiakasprofiileille voi luoda mallit tai asiakkaat voidaan lisätä ilman malleja.</span><span class="sxs-lookup"><span data-stu-id="8b41c-112">You can establish templates for different customer profiles, or you can add customers without templates.</span></span>  

> [!NOTE]  
> <span data-ttu-id="8b41c-113">Jos eri asiakastyypeille on olemassa asiakasmalleja, sivu avautuu, kun luot uuden asiakkaan kortin, jossa voit valita haluamasi mallin.</span><span class="sxs-lookup"><span data-stu-id="8b41c-113">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="8b41c-114">Jos vain yksi asiakasmalli on olemassa, uudet asiakaskortit käyttävät aina kyseistä mallia.</span><span class="sxs-lookup"><span data-stu-id="8b41c-114">If only one customer template exists, then new customer cards always use that template.</span></span>  

### <a name="to-create-a-new-customer-card"></a><span data-ttu-id="8b41c-115">Uuden asiakkaan kortin luominen</span><span class="sxs-lookup"><span data-stu-id="8b41c-115">To create a new customer card</span></span>

1. <span data-ttu-id="8b41c-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8b41c-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8b41c-117">Valitse **Asiakkaat** -sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="8b41c-117">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="8b41c-118">Jos vain yksi asiakasmalli on olemassa, uusi asiakkaan kortin avautuu. Osa kortin kentistä täytetty mallin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="8b41c-118">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="8b41c-119">Jos on olemassa useita asiakasmalleja, näyttöön avautuu automaattisesti sivu, jossa voit valita asiakasmallin.</span><span class="sxs-lookup"><span data-stu-id="8b41c-119">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="8b41c-120">Noudata tällaisessa tapauksessa kahta seuraavaa vaihetta.</span><span class="sxs-lookup"><span data-stu-id="8b41c-120">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="8b41c-121">Valitse **Valitse malli uudelle asiakkaalle** -sivulla malli, jota haluat käyttää uudessa asiakkaan kortissa.</span><span class="sxs-lookup"><span data-stu-id="8b41c-121">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="8b41c-122">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="8b41c-122">Choose the **OK** button.</span></span> <span data-ttu-id="8b41c-123">Uuden asiakkaan kortti avautuu. Osa kortin kentistä on täytetty mallin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="8b41c-123">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="8b41c-124">Voit täyttää asiakkaan kortin kenttiä tai muuttaa niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="8b41c-124">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="8b41c-125">**Myyntihinnat**-pikavälilehti sisältää erityiset hinnat tai alennukset, jotka haluat myöntää asiakkaalle, jos tietyt ehdot, kuten nimike, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="8b41c-125">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="8b41c-126">Kukin rivi edustaa erityistä hinnan alennusta tai rivialennusta.</span><span class="sxs-lookup"><span data-stu-id="8b41c-126">Each row represents a special price or line discount.</span></span> <span data-ttu-id="8b41c-127">Kukin sarake vastaa ehtoa, joka takaa **Yksikköhinta**-kenttään kirjoitetun erikoishinnan tai **Rivialennus-%**-kenttään kirjoitetun rivialennuksen.</span><span class="sxs-lookup"><span data-stu-id="8b41c-127">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="8b41c-128">Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="8b41c-128">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="8b41c-129">Asiakas on nyt rekisteröity, ja asiakkaan kortti on valmis käytettäväksi myyntiasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="8b41c-129">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="8b41c-130">Jos haluat käyttää tätä asiakkaan korttia mallina, kun luot uusia asiakkaan kortteja, tallenna se mallina.</span><span class="sxs-lookup"><span data-stu-id="8b41c-130">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="8b41c-131">Lisätietoja on seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="8b41c-131">For more information, see the following section.</span></span>  

### <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="8b41c-132">Asiakkaan kortin tallentaminen mallina</span><span class="sxs-lookup"><span data-stu-id="8b41c-132">To save the customer card as a template</span></span>

1. <span data-ttu-id="8b41c-133">Valitse **Asiakkaan kortti** -sivulla **Tallenna mallina** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="8b41c-133">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="8b41c-134">**Asiakasmalli**-sivu avautuu ja näyttää asiakaskortin mallina.</span><span class="sxs-lookup"><span data-stu-id="8b41c-134">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="8b41c-135">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="8b41c-135">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="8b41c-136">Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="8b41c-136">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="8b41c-137">**Dimensiomallit**-sivu avautuu. Se sisältää kaikki asiakkaalle määritetyt dimensiokoodit.</span><span class="sxs-lookup"><span data-stu-id="8b41c-137">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="8b41c-138">Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin asiakkaan kortteihin.</span><span class="sxs-lookup"><span data-stu-id="8b41c-138">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="8b41c-139">Kun olet määrittänyt uuden asiakasmallin, valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="8b41c-139">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="8b41c-140">Asiakasmalli lisätään asiakasmallien luetteloon niin, että sen avulla voit luoda uusia asiakkaiden kortteja.</span><span class="sxs-lookup"><span data-stu-id="8b41c-140">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="deleting-customer-cards"></a><span data-ttu-id="8b41c-141">Asiakaskorttien poistaminen</span><span class="sxs-lookup"><span data-stu-id="8b41c-141">Deleting customer cards</span></span>

<span data-ttu-id="8b41c-142">Jos olet kirjannut asiakkaalle tapahtuman, et voi poistaa korttia, koska nimiketapahtumia voi tarvita valvontaan.</span><span class="sxs-lookup"><span data-stu-id="8b41c-142">If you have posted a transaction for a customer, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="8b41c-143">Voit poistaa asiakaskortin, jossa on tapahtumakirjauksia ottamalla yhteyttä Microsoft-kumppaniin koodin avulla.</span><span class="sxs-lookup"><span data-stu-id="8b41c-143">To delete customer cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8b41c-144">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8b41c-144">See Also</span></span>

[<span data-ttu-id="8b41c-145">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8b41c-145">Defining Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="8b41c-146">Tietueiden kaksoiskappaleiden yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="8b41c-146">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="8b41c-147">Numerosarjojen luominen</span><span class="sxs-lookup"><span data-stu-id="8b41c-147">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="8b41c-148">Myynti</span><span class="sxs-lookup"><span data-stu-id="8b41c-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="8b41c-149">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8b41c-149">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="8b41c-150">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8b41c-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
