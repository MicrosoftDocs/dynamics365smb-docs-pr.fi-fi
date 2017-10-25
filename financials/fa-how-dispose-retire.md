---
title: "Käyttöomaisuuden käytöstä poistaminen| Microsoft Docs"
description: "Käyttöomaisuudelle on kirjattava poistoarvo, kun se hävitetään, myydään tai poistetaan käytöstä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 5fc65c97e7c95a37d54b4084aaf8616169b625db
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="ba609-103">Toimintaohje: Käyttöomaisuuden luovuttaminen tai poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="ba609-103">How to: Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="ba609-104">Kun myyt tai muuten luovutat käyttöomaisuuden, luovutusarvo on kirjattava voiton tai tappion laskemista ja tallentamista varten.</span><span class="sxs-lookup"><span data-stu-id="ba609-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="ba609-105">Luovutustapahtuman tulee olla viimeinen tapahtuma, joka käyttöomaisuudelle on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="ba609-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="ba609-106">Osittain luovutetun käyttöomaisuuden osalta voidaan kirjata useampi kuin yksi luovutustapahtuma.</span><span class="sxs-lookup"><span data-stu-id="ba609-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="ba609-107">Kaikkien kirjattujen luovutussummien kokonaissumman tulee olla kredit-summa.</span><span class="sxs-lookup"><span data-stu-id="ba609-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ba609-108">Jos käyttöomaisuuserä vaihdetaan toiseen, sekä vanhan käyttöomaisuuserän myynti (luovutus) että uuden käyttöomaisuuserän osto (hankinta) tulee tallentaa.</span><span class="sxs-lookup"><span data-stu-id="ba609-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="ba609-109">Lisätietoja on kohdassa [Toimintaohje: Käyttöomaisuuden hankinta](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="ba609-109">For more information, see [How to: Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="ba609-110">Luovutuksen kirjaaminen käyttöomaisuuden KP-päiväkirjasta</span><span class="sxs-lookup"><span data-stu-id="ba609-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="ba609-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ba609-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ba609-112">Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ba609-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="ba609-113">Valitse **KO:n kirjaustyyppi** -kentässä **Luovutus**.</span><span class="sxs-lookup"><span data-stu-id="ba609-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="ba609-114">Valitse **Syötä KO-vastatili** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="ba609-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="ba609-115">Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty luovutuksen kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="ba609-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="ba609-116">Vaihe 4 toimii vain, jos seuraavat arvot on määritetty: Käyttöomaisuuden kirjausryhmän **KO:n kirjausryhmän kortti** -ikkunan **Luovutustili**-kenttä sisältää pääkirjanpidon debet-tilin ja **Luovutuksen vastatili** -kenttä sisältää sen pääkirjanpitotilin, jolle vastatilitapahtumien arvonkorotus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="ba609-116">Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="ba609-117">Lisätietoja on "Käyttöomaisuuden kirjausryhmien määrittäminen" -osassa kohdassa [Toimintaohje: Käyttöomaisuuden yleisten tietojen määrittäminen](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="ba609-117">For more information, see the "To set up fixed asset posting groups" section in [How to: Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>  
5. <span data-ttu-id="ba609-118">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ba609-118">Choose the **Post** action.</span></span>  

    <span data-ttu-id="ba609-119">Jos myyt osan käyttöomaisuudesta tai muuten luovut osasta käyttöomaisuutta, omaisuuserä tulee jakaa ennen kuin luovutustransaktion voi tallentaa.</span><span class="sxs-lookup"><span data-stu-id="ba609-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="ba609-120">Lisätietoja on kohdassa [Toimintaohje: Käyttöomaisuuden siirtäminen, jakaminen tai yhdistäminen](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="ba609-120">For more information, see [How to: Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="ba609-121">Luovutustapahtumien katsominen</span><span class="sxs-lookup"><span data-stu-id="ba609-121">To view disposal ledger entries</span></span>
<span data-ttu-id="ba609-122">Kun myyt tai luovutat käyttöomaisuutta, luovutusarvo kirjataan pääkirjanpitoon, jossa tulosta voi tarkastella.</span><span class="sxs-lookup"><span data-stu-id="ba609-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="ba609-123">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Käyttöomaisuus** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ba609-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ba609-124">Valitse käyttöomaisuus, jonka tapahtumia haluat tarkastella. Valitse sitten **Poistokirjat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ba609-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="ba609-125">Valitse poistokirja, jonka tapahtumia haluat tarkastella. Valitse sitten **Tapahtumakirjaukset**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ba609-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="ba609-126">Valitse **KO:n kirjausluokka** -kentässä rivi, joka sisältää **luovutuksen**. Valitse sitten **Navigoi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ba609-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="ba609-127">Valitse **Navigointi**-ikkunassa pääkirjanpidon tapahtuman rivi ja valitse sitten **Näytä**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ba609-127">In the **Navigate** window, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="ba609-128">Näyttöön tulee **Pääkirjanpidon tapahtumat** -ikkuna, jossa näkyvät tapahtumat, joiden tuloksena on luovutuksen kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="ba609-128">The **General Ledger Entries** window opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ba609-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ba609-129">See Also</span></span>
[<span data-ttu-id="ba609-130">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="ba609-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="ba609-131">Käyttöomaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ba609-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="ba609-132">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="ba609-132">Finance</span></span>](finance.md)  
<span data-ttu-id="ba609-133">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="ba609-133">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="ba609-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ba609-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

