---
title: "Sekkien myöntäminen, tulostaminen, peruuttaminen ja mitätöiminen| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten sekit myönnetään maksupäiväkirjan avulla, tulostetaan ja mitätöidään tai miten sekkitapahtumia tarkastellaan Business Central -sovelluksessa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 0c1b37616b4aafc9535f2d3fbf60b915c490dd0b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-checks"></a><span data-ttu-id="4ca9a-103">Sekkien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="4ca9a-103">Work With Checks</span></span>
<span data-ttu-id="4ca9a-104">Voit myöntää sähköisiä ja manuaalisia sekkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4ca9a-105">Molemmissa menetelmissä sekit myönnetään toimittajille maksupäiväkirjaa käyttäen.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="4ca9a-106">Ohjelman avulla voit myös mitätöidä sekkejä ja tarkastella sekkitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="4ca9a-107">Sekkien myöntämiskäsittelyyn kuuluvat maksujen ehdottaminen, tapahtumien luominen ja tietokonesekkien tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4ca9a-108">Voit varmistaa lähettämällä toimittaja-, sekki- ja maksutiedot sisältävän tiedoston, että pankki vahvistaa vain tarkistetut sekit ja summat.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="4ca9a-109">Lisätietoja on kohdassa [Positive Pay -tiedostojen vieminen](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="4ca9a-109">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="4ca9a-110">Tulostin on määritettävä oikein sekkimuotoja varten. Myös käytettävä sekkien asettelu on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="4ca9a-111">Lisätietoja on kohdassa [Sekkien asetteluiden määrittäminen](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="4ca9a-111">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="4ca9a-112">Sekkien myöntäminen</span><span class="sxs-lookup"><span data-stu-id="4ca9a-112">To issue checks</span></span>
1. <span data-ttu-id="4ca9a-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="4ca9a-114">Täytä asianmukaisten maksujen tiedot päiväkirjaan esimerkiksi Ehdota toimittajamaksuja -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="4ca9a-115">Lisätietoja on kohdassa [Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="4ca9a-115">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="4ca9a-116">Valitse sekkien avulla tehtävän maksun päiväkirjan rivillä **Pankkimaksun tyyppi** -kentässä jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="4ca9a-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="4ca9a-117">**Tietokonesekki**: Valitse tämä vaihtoehto, jos haluat tulostaa sekin maksupäiväkirjan tällä rivillä olevalle summalle.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="4ca9a-118">Tulosta sekit, ennen kuin kirjaat päiväkirjan rivit.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="4ca9a-119">Voit valita **Tietokonesekki**-kohdan vain, jos **Vastatilin tyyppi** tai **Tilin tyyppi** on **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="4ca9a-120">**Manuaalinen sekki**: Valitse tämä vaihtoehto, jos olet luonut sekin manuaalisesti ja haluat luoda vastaavan sekkitapahtuman tälle summalle.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="4ca9a-121">Tämän vaihtoehdon avulla et voi tulostaa sekkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]ista.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4ca9a-122">Voit valita **Manuaalinen sekki** -kohdan vain, jos **Vastatilin tyyppi** tai **Tilin tyyppi** on **Pankkitili**.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
     >   <span data-ttu-id="4ca9a-123">Tulosta tietokonesekit, ennen kuin kirjaat liittyvät päiväkirjan rivit.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="4ca9a-124">Jos kyseessä on tietokonesekki, valitse **Tulosta sekki**.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="4ca9a-125">Täytä **Sekki**-ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="4ca9a-126">Valitse **Tulosta**-painike.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4ca9a-127">Jos sekkejä täytyy tulostaa monessa valuutassa eri pankkitileiltä, sinun täytyy suorittaa **Tulosta sekki** -eräajo erikseen kullekin valuutalle ja määrittää sopivat pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="4ca9a-128">Kirjaamattomien ja tulostettujen sekkien peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="4ca9a-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="4ca9a-129">Voit peruuttaa kirjaamattomat sekit niiden tulostamisen jälkeen **Maksupäiväkirja**-ikkunan **Mitätöi sekki** -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="4ca9a-130">Valitse **Maksupäiväkirja**-ikkunassa **Mitätöi sekki** ja valitse peruutettavat sekit.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="4ca9a-131">Sekkien mitätöiminen</span><span class="sxs-lookup"><span data-stu-id="4ca9a-131">To void checks</span></span>
<span data-ttu-id="4ca9a-132">Kun sekkimaksu on kirjattu, voit peruuttaa (mitätöidä) sekit vain tuloksena syntyvistä pankkitapahtumista.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="4ca9a-133">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="4ca9a-134">Valitse oikea pankkitili, valitse **Muokkaa**-toiminto ja valitse sitten **Sekkitapahtumat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="4ca9a-135">Valitse **Sekkitapahtumat**-ikkunassa **Mitätöi sekki** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="4ca9a-136">Valitse **Mitätöi vain sekki** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="4ca9a-137">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="4ca9a-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ca9a-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4ca9a-138">See Also</span></span>
[<span data-ttu-id="4ca9a-139">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="4ca9a-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="4ca9a-140">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4ca9a-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="4ca9a-141">Positive Pay -tiedoston vienti</span><span class="sxs-lookup"><span data-stu-id="4ca9a-141">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="4ca9a-142">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4ca9a-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

