---
title: "Uusien asiakkaiden rekisteröinti asiakkaan kortin luonnin avulla | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten asiakkaan kortti luodaan rekisteröimään tietoja kustakin uudesta asiakkaasta, jolle myyt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6dcd375cc687e74783cadc2cf50fbf804377d3ca
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="register-new-customers"></a><span data-ttu-id="0c731-103">Uusien asiakkaiden rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="0c731-103">Register New Customers</span></span>
<span data-ttu-id="0c731-104">Asiakkaat ovat tulonlähteesi.</span><span class="sxs-lookup"><span data-stu-id="0c731-104">Customers are the source of your income.</span></span> <span data-ttu-id="0c731-105">Jokainen asiakas, jolle myyt, on rekisteröitävä asiakaskorttina.</span><span class="sxs-lookup"><span data-stu-id="0c731-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="0c731-106">Asiakkaan kortit sisältävät tietoja, jotka tarvitaan tuotteiden asiakkaalle myymistä varten.</span><span class="sxs-lookup"><span data-stu-id="0c731-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="0c731-107">Lisätietoja on kohdissa [Myynnin laskutus](sales-how-invoice-sales.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="0c731-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="0c731-108">Ennen kuin voit rekisteröidä uusia asiakkaita, sinun on määritettävä myyntikoodit, jotka voidaan valita asiakkaiden korttien täyttämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="0c731-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="0c731-109">Lisätietoja on kohdassa [Myynnin määrittäminen](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="0c731-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="0c731-110">Jos eri asiakastyypeille on olemassa asiakasmalleja, ikkuna avautuu, kun luot uuden asiakkaan kortin, jossa voit valita haluamasi mallin.</span><span class="sxs-lookup"><span data-stu-id="0c731-110">If customer templates exist for different customer types, then a window appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="0c731-111">Jos vain yksi asiakasmalli on olemassa, uudet asiakaskortit käyttävät aina kyseistä mallia.</span><span class="sxs-lookup"><span data-stu-id="0c731-111">If only one customer template exists, then new customer cards always use that template.</span></span>

## <a name="to-create-a-new-customer-card"></a><span data-ttu-id="0c731-112">Uuden asiakkaan kortin luominen</span><span class="sxs-lookup"><span data-stu-id="0c731-112">To create a new customer card</span></span>
1. <span data-ttu-id="0c731-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0c731-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0c731-114">Valitse **Asiakkaat**-ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="0c731-114">In the **Customers** window, choose the **New** action.</span></span>

    <span data-ttu-id="0c731-115">Jos vain yksi asiakasmalli on olemassa, uusi asiakkaan kortin avautuu. Osa kortin kentistä täytetty mallin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="0c731-115">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="0c731-116">Jos on olemassa useita asiakasmalleja, näyttöön avautuu automaattisesti ikkuna, jossa voit valita asiakasmallin.</span><span class="sxs-lookup"><span data-stu-id="0c731-116">If more than one customer template exists, then a window opens from which you can select a customer template.</span></span> <span data-ttu-id="0c731-117">Noudata tällaisessa tapauksessa kahta seuraavaa vaihetta.</span><span class="sxs-lookup"><span data-stu-id="0c731-117">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="0c731-118">Valitse **Valitse malli uudelle asiakkaalle** -ikkunassa malli, jota haluat käyttää uudessa asiakkaan kortissa.</span><span class="sxs-lookup"><span data-stu-id="0c731-118">In the **Select a template for a new customer** window, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="0c731-119">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="0c731-119">Choose the **OK** button.</span></span> <span data-ttu-id="0c731-120">Uuden asiakkaan kortti avautuu. Osa kortin kentistä on täytetty mallin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="0c731-120">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="0c731-121">Voit täyttää asiakkaan kortin kenttiä tai muuttaa niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="0c731-121">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="0c731-122">**Myyntihinnat**-pikavälilehti sisältää erityiset hinnat tai alennukset, jotka haluat myöntää asiakkaalle, jos tietyt ehdot, kuten nimike, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="0c731-122">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="0c731-123">Kukin rivi edustaa erityistä hinnan alennusta tai rivialennusta.</span><span class="sxs-lookup"><span data-stu-id="0c731-123">Each row represents a special price or line discount.</span></span> <span data-ttu-id="0c731-124">Kukin sarake vastaa ehtoa, joka takaa **Yksikköhinta**-kenttään kirjoitetun erikoishinnan tai **Rivialennus-%**-kenttään kirjoitetun rivialennuksen.</span><span class="sxs-lookup"><span data-stu-id="0c731-124">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="0c731-125">Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="0c731-125">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="0c731-126">Asiakas on nyt rekisteröity, ja asiakkaan kortti on valmis käytettäväksi myyntiasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="0c731-126">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="0c731-127">Jos haluat käyttää tätä asiakkaan korttia mallina, kun luot uusia asiakkaan kortteja, tallenna se mallina.</span><span class="sxs-lookup"><span data-stu-id="0c731-127">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="0c731-128">Lisätietoja on seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="0c731-128">For more information, see the following section.</span></span>

## <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="0c731-129">Asiakkaan kortin tallentaminen mallina</span><span class="sxs-lookup"><span data-stu-id="0c731-129">To save the customer card as a template</span></span>
1. <span data-ttu-id="0c731-130">Valitse **Asiakkaan kortti** -ikkunassa **Tallenna mallina** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="0c731-130">In the **Customer Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="0c731-131">**Asiakasmalli**-ikkuna avautuu ja näyttää asiakaskortin mallina.</span><span class="sxs-lookup"><span data-stu-id="0c731-131">The **Customer Template** window opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="0c731-132">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="0c731-132">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="0c731-133">Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="0c731-133">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="0c731-134">**Dimensiomallit**-ikkuna avautuu. Se sisältää kaikki asiakkaalle määritetyt dimensiokoodit.</span><span class="sxs-lookup"><span data-stu-id="0c731-134">The **Dimension Templates** window opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="0c731-135">Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin asiakkaan kortteihin.</span><span class="sxs-lookup"><span data-stu-id="0c731-135">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="0c731-136">Kun olet määrittänyt uuden asiakasmallin, valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="0c731-136">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="0c731-137">Asiakasmalli lisätään asiakasmallien luetteloon niin, että sen avulla voit luoda uusia asiakkaiden kortteja.</span><span class="sxs-lookup"><span data-stu-id="0c731-137">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c731-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0c731-138">See Also</span></span>
<span data-ttu-id="0c731-139">[Myynti](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="0c731-139">[Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="0c731-140">[Myynnin määrittäminen](sales-setup-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="0c731-140">[Setting Up Sales](sales-setup-sales.md)  </span></span>  
<span data-ttu-id="0c731-141">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c731-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

