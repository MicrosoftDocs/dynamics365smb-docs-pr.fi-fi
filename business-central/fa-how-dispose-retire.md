---
title: Käyttöomaisuuden käytöstä poistaminen| Microsoft Docs
description: Käyttöomaisuudelle on kirjattava poistoarvo, kun se hävitetään, myydään tai poistetaan käytöstä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9a155c5b2f616963da34c4d512bcc0f52623f58b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920720"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="2bfb4-103">Käyttöomaisuuden käytöstä poistaminen</span><span class="sxs-lookup"><span data-stu-id="2bfb4-103">Dispose of or Retire Fixed Assets</span></span>

<span data-ttu-id="2bfb4-104">Kun myyt tai muuten luovutat käyttöomaisuuden, luovutusarvo on kirjattava voiton tai tappion laskemista ja tallentamista varten.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="2bfb4-105">Luovutustapahtuman tulee olla viimeinen tapahtuma, joka käyttöomaisuudelle on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="2bfb4-106">Osittain luovutetun käyttöomaisuuden osalta voidaan kirjata useampi kuin yksi luovutustapahtuma.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="2bfb4-107">Kaikkien kirjattujen luovutussummien kokonaissumman tulee olla kredit-summa.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="2bfb4-108">Jos käyttöomaisuuserä vaihdetaan toiseen, sekä vanhan käyttöomaisuuserän myynti (luovutus) että uuden käyttöomaisuuserän osto (hankinta) tulee tallentaa.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="2bfb4-109">Lisätietoja on kohdassa [Käyttöomaisuuden hankinta](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="2bfb4-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

<span data-ttu-id="2bfb4-110">Seuraavissa vaiheissa oletetaan, että asianmukaiset kirjausryhmät on jo määritetty **KO:n kirjausryhmät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-110">The following steps assume that you have already set up the relevant posting groups in the **FA Posting Groups** page.</span></span> <span data-ttu-id="2bfb4-111">Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="2bfb4-111">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="2bfb4-112">Luovutuksen kirjaaminen käyttöomaisuuden KP-päiväkirjasta</span><span class="sxs-lookup"><span data-stu-id="2bfb4-112">To post a disposal from the fixed asset G/L journal</span></span>

1. <span data-ttu-id="2bfb4-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuuden KP-päiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2bfb4-114">Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-114">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="2bfb4-115">Valitse **KO:n kirjaustyyppi** -kentässä **Luovutus**.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-115">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="2bfb4-116">Valitse **Syötä KO-vastatili** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-116">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="2bfb4-117">Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty luovutuksen kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-117">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="2bfb4-118">Vaihe 4 toimii vain, jos seuraavat arvot on määritetty: Käyttöomaisuuden kirjausryhmän **KO:n kirjausryhmän kortti** -sivun **Luovutustili**-kenttä sisältää pääkirjanpidon debet-tilin ja **Luovutuksen vastatili** -kenttä sisältää sen pääkirjanpitotilin, jolle vastatilitapahtumien arvonkorotus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-118">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="2bfb4-119">Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="2bfb4-119">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="2bfb4-120">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-120">Choose the **Post** action.</span></span>  

<span data-ttu-id="2bfb4-121">Jos myyt osan käyttöomaisuudesta tai muuten luovut osasta käyttöomaisuutta, omaisuuserä tulee jakaa ennen kuin luovutustransaktion voi tallentaa.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-121">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="2bfb4-122">Lisätietoja on kohdassa [Käyttöomaisuuden siirtäminen, jakaminen tai yhdistäminen](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="2bfb4-122">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="2bfb4-123">Luovutustapahtumien katsominen</span><span class="sxs-lookup"><span data-stu-id="2bfb4-123">To view disposal ledger entries</span></span>
<span data-ttu-id="2bfb4-124">Kun myyt tai luovutat käyttöomaisuutta, luovutusarvo kirjataan pääkirjanpitoon, jossa tulosta voi tarkastella.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-124">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="2bfb4-125">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2bfb4-126">Valitse käyttöomaisuus, jonka tapahtumia haluat tarkastella. Valitse sitten **Poistokirjat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-126">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="2bfb4-127">Valitse poistokirja, jonka tapahtumia haluat tarkastella. Valitse sitten **Tapahtumakirjaukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-127">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="2bfb4-128">Valitse **KO:n kirjausluokka** -kentässä rivi, joka sisältää **luovutuksen**. Valitse sitten **Etsi kirjaukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-128">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Find Entries** action.</span></span>  
5. <span data-ttu-id="2bfb4-129">Valitse **Etsi kirjaukset**-sivulla pääkirjanpidon tapahtuman rivi ja valitse sitten **Näytä liittyvät kirjaukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-129">On the **Find Entries** page, select the general ledger entry line, and then choose the **Show Related Entries** action.</span></span>  

<span data-ttu-id="2bfb4-130">Näyttöön tulee **Pääkirjanpidon tapahtumat** -sivu, jossa näkyvät tapahtumat, joiden tuloksena on luovutuksen kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="2bfb4-130">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2bfb4-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2bfb4-131">See Also</span></span>

[<span data-ttu-id="2bfb4-132">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="2bfb4-132">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="2bfb4-133">Käyttöomaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2bfb4-133">Setting Up Fixed Assets</span></span>](fa-setup.md)  
<span data-ttu-id="2bfb4-134">[Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="2bfb4-134">[To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
[<span data-ttu-id="2bfb4-135">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="2bfb4-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="2bfb4-136">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="2bfb4-136">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="2bfb4-137">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2bfb4-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2bfb4-138">Etsi tapahtumat</span><span class="sxs-lookup"><span data-stu-id="2bfb4-138">Find Entries</span></span>](ui-find-entries.md)  
