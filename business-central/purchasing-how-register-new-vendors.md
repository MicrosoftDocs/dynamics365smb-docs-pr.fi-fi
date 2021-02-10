---
title: Uuden toimittajan rekisteröinti toimittajan kortin luonnin avulla | Microsoft Docs
description: Lisätietoja uuden toimittajan rekisteröinnistä toimittajan kortin luonnin avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8efd74c3ae6962a383e5b127056d744dd7c1892f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748791"
---
# <a name="register-new-vendors"></a><span data-ttu-id="f0fd7-103">Uusien toimittajien rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="f0fd7-103">Register New Vendors</span></span>

<span data-ttu-id="f0fd7-104">Toimittajat tarjoavat tuotteita, jotka myydään.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="f0fd7-105">Jokainen toimittaja, jolta ostat, täytyy rekisteröidä toimittajakorttina.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="f0fd7-106">Ennen kuin voit rekisteröidä uusia toimittajia, sinun on määritettävä ostokoodeja, joita valitaan toimittajien korttien täyttämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="f0fd7-107">Kun kaikki tarvittavat päätiedot on luotu, voit tehdä muita toimittajaa koskevia määrityksiä, kuten priorisoida toimittajan maksutilanteita varten sekä eritellä nimikkeitä, joita toimittaja ja muut toimittajat voivat toimittaa.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="f0fd7-108">Kokonaan erillinen toimittajia koskevien määritystehtävien joukko on alennuksia, hintoja ja maksutapoja koskevien sopimusten tallentaminen.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="f0fd7-109">Lisätietoja on kohdassa [Ostojen määrittäminen](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="f0fd7-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="f0fd7-110">Toimittajan kortti sisältää tiedot, joita tarvitaan tuotteiden ostamiseksi toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="f0fd7-111">Lisätietoja on kohdissa [Ostojen kirjaaminen](purchasing-how-record-purchases.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="f0fd7-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="f0fd7-112">Jos eri toimittajan tyypeille on olemassa toimittajamalleja, sivu avautuu, kun luot uuden toimittajan kortin, jossa voit valita haluamasi mallin.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="f0fd7-113">Jos vain yksi toimittajamalli on olemassa, uudet toimittajan kortit käyttävät aina kyseistä mallia.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="f0fd7-114">Uuden toimittajan kortin luominen</span><span class="sxs-lookup"><span data-stu-id="f0fd7-114">To create a new vendor card</span></span>

1. <span data-ttu-id="f0fd7-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimittajat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f0fd7-116">Valitse **Toimittajat**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-116">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="f0fd7-117">Jos on olemassa useita toimittajamalleja, näyttöön avautuu automaattisesti sivu, jossa voit valita toimittajamallin.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-117">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="f0fd7-118">Noudata tällaisessa tapauksessa kahta seuraavaa vaihetta.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="f0fd7-119">Valitse **Valitse malli uudelle toimittajalle** -sivulla malli, jota haluat käyttää uudessa toimittajan kortissa.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-119">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="f0fd7-120">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-120">Choose the **OK** button.</span></span> <span data-ttu-id="f0fd7-121">Uuden toimittajan kortti avautuu. Jotkin sen kentät on täytetty mallin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="f0fd7-122">Voit täyttää toimittajan kortin kenttiä tai muuttaa niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="f0fd7-123">Jos et tiedä laskutusosoitetta, jota käytetään kaikissa toimittajan laskuissa, älä täytä **Toimittajan nro** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Vendor No.** field.</span></span> <span data-ttu-id="f0fd7-124">Valitse sen sijaan tavaran laskuttajan numeron sen jälkeen, kun olet määrittänyt ostotarjouksen, -tilauksen, -laskun otsikon.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="f0fd7-125">Toimittaja on nyt rekisteröity, ja toimittajan kortti on valmis käytettäväksi ostoasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="f0fd7-126">Jos haluat käyttää tätä toimittajan korttia mallina, kun luot uusia toimittajan kortteja, tallenna se toimittajamallina.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="f0fd7-127">Lisätietoja on seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-127">For more information, see the following section.</span></span>

### <a name="deleting-vendor-cards"></a><span data-ttu-id="f0fd7-128">Toimittajakorttien poistaminen</span><span class="sxs-lookup"><span data-stu-id="f0fd7-128">Deleting Vendor Cards</span></span>
<span data-ttu-id="f0fd7-129">Jos olet kirjannut toimittajalle tapahtuman, et voi poistaa korttia, koska nimiketapahtumia voi tarvita valvontaan.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-129">If you have posted a transaction for a vendor, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="f0fd7-130">Voit poistaa toimittajakortteja, joissa on tapahtumakirjauksia ottamalla yhteyttä Microsoft-kumppaniin koodin avulla.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-130">To delete vendor cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="f0fd7-131">Toimittajan kortin tallentaminen mallina</span><span class="sxs-lookup"><span data-stu-id="f0fd7-131">To save the vendor card as a template</span></span>
1. <span data-ttu-id="f0fd7-132">Valitse **Toimittajakortti**-sivulla **Tallenna mallina** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-132">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="f0fd7-133">**Toimittajamalli**-sivu avautuu ja näyttää toimittajan kortin mallina.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-133">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="f0fd7-134">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-134">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="f0fd7-135">Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-135">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="f0fd7-136">**Dimensiomallit**-sivu avautuu. Se sisältää kaikki toimittajalle määritetyt dimensiokoodit.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-136">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="f0fd7-137">Muokkaa tai syötä dimensiokoodeja, joita käytetään mallin avulla luotuihin uusiin toimittajan kortteihin.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-137">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="f0fd7-138">Kun olet määrittänyt uuden toimittajamallin, valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-138">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="f0fd7-139">Toimittajamalli lisätään toimittajamallien luetteloon niin, että sen avulla voit luoda uusia toimittajan kortteja.</span><span class="sxs-lookup"><span data-stu-id="f0fd7-139">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0fd7-140">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f0fd7-140">See Also</span></span>
[<span data-ttu-id="f0fd7-141">Tietueiden kaksoiskappaleiden yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="f0fd7-141">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="f0fd7-142">Numerosarjojen luominen</span><span class="sxs-lookup"><span data-stu-id="f0fd7-142">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="f0fd7-143">Osto</span><span class="sxs-lookup"><span data-stu-id="f0fd7-143">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f0fd7-144">[Ostojen kirjaus](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="f0fd7-144">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="f0fd7-145">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f0fd7-145">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
