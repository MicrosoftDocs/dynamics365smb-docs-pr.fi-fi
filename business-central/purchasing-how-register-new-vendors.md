---
title: "Uuden toimittajan rekisteröinti toimittajan kortin luonnin avulla | Microsoft Docs"
description: "Lisätietoja uuden toimittajan rekisteröinnistä toimittajan kortin luonnin avulla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ea9b4a6310df319df06d02c53b9d6156caaee24f
ms.openlocfilehash: d17ed41b7beb6ba342c17e007496314d9be743f0
ms.contentlocale: fi-fi
ms.lasthandoff: 03/28/2018

---
# <a name="register-new-vendors"></a><span data-ttu-id="96fd3-103">Uusien toimittajien rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="96fd3-103">Register New Vendors</span></span>
<span data-ttu-id="96fd3-104">Toimittajat tarjoavat tuotteita, jotka myydään.</span><span class="sxs-lookup"><span data-stu-id="96fd3-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="96fd3-105">Jokainen toimittaja, jolta ostat, täytyy rekisteröidä toimittajakorttina.</span><span class="sxs-lookup"><span data-stu-id="96fd3-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="96fd3-106">Ennen kuin voit rekisteröidä uusia toimittajia, sinun on määritettävä ostokoodeja, joita valitaan toimittajien korttien täyttämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="96fd3-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="96fd3-107">Kun kaikki tarvittavat päätiedot on luotu, voit tehdä muita toimittajaa koskevia määrityksiä, kuten priorisoida toimittajan maksutilanteita varten sekä eritellä nimikkeitä, joita toimittaja ja muut toimittajat voivat toimittaa.</span><span class="sxs-lookup"><span data-stu-id="96fd3-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="96fd3-108">Kokonaan erillinen toimittajia koskevien määritystehtävien joukko on alennuksia, hintoja ja maksutapoja koskevien sopimusten tallentaminen.</span><span class="sxs-lookup"><span data-stu-id="96fd3-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="96fd3-109">Lisätietoja on kohdassa [Ostojen määrittäminen](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="96fd3-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="96fd3-110">Toimittajan kortti sisältää tiedot, joita tarvitaan tuotteiden ostamiseksi toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="96fd3-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="96fd3-111">Lisätietoja on kohdissa [Ostojen kirjaaminen](purchasing-how-record-purchases.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="96fd3-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="96fd3-112">Jos eri toimittajan tyypeille on olemassa toimittajamalleja, ikkuna avautuu, kun luot uuden toimittajan kortin, jossa voit valita haluamasi mallin.</span><span class="sxs-lookup"><span data-stu-id="96fd3-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="96fd3-113">Jos vain yksi toimittajamalli on olemassa, uudet toimittajan kortit käyttävät aina kyseistä mallia.</span><span class="sxs-lookup"><span data-stu-id="96fd3-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="96fd3-114">Uuden toimittajan kortin luominen</span><span class="sxs-lookup"><span data-stu-id="96fd3-114">To create a new vendor card</span></span>
1. <span data-ttu-id="96fd3-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="96fd3-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="96fd3-116">Valitse **Toimittajat**-ikkunassa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="96fd3-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="96fd3-117">Jos on olemassa useita toimittajamalleja, näyttöön avautuu automaattisesti ikkuna, jossa voit valita toimittajamallin.</span><span class="sxs-lookup"><span data-stu-id="96fd3-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="96fd3-118">Noudata tällaisessa tapauksessa kahta seuraavaa vaihetta.</span><span class="sxs-lookup"><span data-stu-id="96fd3-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="96fd3-119">Valitse **Valitse malli uudelle toimittajalle** -ikkunassa malli, jota haluat käyttää uudessa toimittajan kortissa.</span><span class="sxs-lookup"><span data-stu-id="96fd3-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="96fd3-120">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="96fd3-120">Choose the **OK** button.</span></span> <span data-ttu-id="96fd3-121">Uuden toimittajan kortti avautuu. Jotkin sen kentät on täytetty mallin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="96fd3-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="96fd3-122">Voit täyttää toimittajan kortin kenttiä tai muuttaa niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="96fd3-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="96fd3-123">Jos et tiedä laskutusosoitetta, jota käytetään kaikissa toimittajan laskuissa, älä täytä **Tavaran laskuttaja** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="96fd3-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="96fd3-124">Valitse sen sijaan tavaran laskuttajan numeron sen jälkeen, kun olet määrittänyt ostotarjouksen, -tilauksen, -laskun otsikon.</span><span class="sxs-lookup"><span data-stu-id="96fd3-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="96fd3-125">Toimittaja on nyt rekisteröity, ja toimittajan kortti on valmis käytettäväksi ostoasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="96fd3-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="96fd3-126">Jos haluat käyttää tätä toimittajan korttia mallina, kun luot uusia toimittajan kortteja, tallenna se toimittajamallina.</span><span class="sxs-lookup"><span data-stu-id="96fd3-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="96fd3-127">Lisätietoja on seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="96fd3-127">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="96fd3-128">Toimittajan kortin tallentaminen mallina</span><span class="sxs-lookup"><span data-stu-id="96fd3-128">To save the vendor card as a template</span></span>
1. <span data-ttu-id="96fd3-129">Valitse **Toimittajan kortti** -ikkunassa **Tallenna mallina** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="96fd3-129">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="96fd3-130">**Toimittajamalli**-ikkuna avautuu ja näyttää toimittajan kortin mallina.</span><span class="sxs-lookup"><span data-stu-id="96fd3-130">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="96fd3-131">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="96fd3-131">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="96fd3-132">Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="96fd3-132">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="96fd3-133">**Dimensiomallit**-ikkuna avautuu. Se sisältää kaikki toimittajalle määritetyt dimensiokoodit.</span><span class="sxs-lookup"><span data-stu-id="96fd3-133">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="96fd3-134">Muokkaa tai syötä dimensiokoodeja, joita käytetään mallin avulla luotuihin uusiin toimittajan kortteihin.</span><span class="sxs-lookup"><span data-stu-id="96fd3-134">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="96fd3-135">Kun olet määrittänyt uuden toimittajamallin, valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="96fd3-135">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="96fd3-136">Toimittajamalli lisätään toimittajamallien luetteloon niin, että sen avulla voit luoda uusia toimittajan kortteja.</span><span class="sxs-lookup"><span data-stu-id="96fd3-136">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="96fd3-137">Katso myös</span><span class="sxs-lookup"><span data-stu-id="96fd3-137">See Also</span></span>
[<span data-ttu-id="96fd3-138">Numerosarjojen luominen</span><span class="sxs-lookup"><span data-stu-id="96fd3-138">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="96fd3-139">Osto</span><span class="sxs-lookup"><span data-stu-id="96fd3-139">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="96fd3-140">[Ostojen kirjaus](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="96fd3-140">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="96fd3-141">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="96fd3-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

