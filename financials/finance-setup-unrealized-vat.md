---
title: "Ei-realisoituneen arvonlisäveron määrittäminen | Microsoft Docs"
description: "Jos käytät kassaperusteista kirjanpitoa, voit määrittää, miten myynnin ja ostojen ei-realisoitunut ALV käsitellään."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b8bbfac583e1e7ec7eedae9e412b4fd3ac956d0f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a><span data-ttu-id="1f8c8-103">Ei-realisoituneen arvonlisäveron määrittäminen kassaperusteista kirjanpitoa varten</span><span class="sxs-lookup"><span data-stu-id="1f8c8-103">Set Up Unrealized VAT for Cash-Based Accounting</span></span>
<span data-ttu-id="1f8c8-104">Jos käytät kassaperusteista kirjanpitoa, voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in käsittelemään ei-realisoidun arvonlisäveron.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-104">If you're using cash-based accounting methods, you can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] to handle unrealized VAT.</span></span>

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a><span data-ttu-id="1f8c8-105">Pääkirjanpidon tilien käyttäminen ei-realisoitunutta arvonlisäveroa varten</span><span class="sxs-lookup"><span data-stu-id="1f8c8-105">To use general ledger accounts for unrealized VAT</span></span>
<span data-ttu-id="1f8c8-106">ALV-summat voidaan laskea ja kirjata väliaikaiselle kirjanpitotilille laskun kirjaamisen yhteydessä. Sen jälkeen ne voidaan kirjata oikealle kirjanpitotilille ja sisällyttää ALV-ilmoituksiin laskun maksun kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-106">You can choose to have VAT amounts calculated and posted to a temporary general ledger account when an invoice is posted, and then posted to the correct general ledger account and included in VAT statements when the actual payment of the invoice is posted.</span></span> <span data-ttu-id="1f8c8-107">Ennen sitä sinun täytyy määrittää ALV-kirjausasetukset.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-107">Before you can do this, you must complete the VAT posting setup.</span></span>

<span data-ttu-id="1f8c8-108">Käytä ei-realisoituneen arvonlisäveron tilejä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1f8c8-108">To use accounts for unrealized VAT, follow these steps:</span></span>
1. <span data-ttu-id="1f8c8-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake ja anna **Pääkirjanpidon asetukset**.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, and enter **General Ledger Setup**.</span></span>
2. <span data-ttu-id="1f8c8-110">Valitse **Pääkirjanpidon asetukset** -sivun **Yleiset**-pikavälilehdessä **Näytä lisää** ja valitse sitten **Ei-realisoitunut ALV** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-110">On the **General Ledger Setup** page, on the **General** FastTab, choose **Show More**, and then choose the **Unrealized VAT** check box.</span></span>
3. <span data-ttu-id="1f8c8-111">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-111">Close the page.</span></span>
4. <span data-ttu-id="1f8c8-112">Valitse **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") ja kirjoita **ALV-kirjausten asetukset**.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-112">choose the **Search for Page or Report** icon ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon"), and enter **VAT Posting Setup**.</span></span>
5. <span data-ttu-id="1f8c8-113">Valitse ensin **ALV-kirjausten asetukset** -sivulla ALV-kirjausryhmä ja sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-113">On the **VAT Posting Setup** page, choose the VAT posting group, and then choose **Edit**.</span></span>
6. <span data-ttu-id="1f8c8-114">Valitse **Ei-realisoituneen ALV:n tyyppi** -kentässä vaihtoehto määrittämään maksujen kohdistus laskun summalle (ilman ALV:tä) ja itse ALV-summalle, ja miten ALV-summat siirretään ei-realisoituneen ALV:n tililtä realisoituneelle tilille.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-114">In the **Unrealized VAT Type** field, choose an option to specify how to allocate payments to the invoice amount (excluding VAT) and the VAT amount itself, and how to transfer VAT amounts from the unrealized VAT account to the realized account.</span></span> <span data-ttu-id="1f8c8-115">Asetukset kuvaillaan seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-115">The following table describes the options.</span></span>

| <span data-ttu-id="1f8c8-116">Asetus</span><span class="sxs-lookup"><span data-stu-id="1f8c8-116">Option</span></span> | <span data-ttu-id="1f8c8-117">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="1f8c8-117">Description</span></span> |
| --- | --- |
| <span data-ttu-id="1f8c8-118">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="1f8c8-118">Blank</span></span> | <span data-ttu-id="1f8c8-119">Valitse tämä vaihtoehto, jos et halua käyttää ei-realisoitunuttu ALV-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-119">Choose this option if you don't want to use the unrealized VAT feature.</span></span> |
| <span data-ttu-id="1f8c8-120">Prosentti</span><span class="sxs-lookup"><span data-stu-id="1f8c8-120">Percentage</span></span> | <span data-ttu-id="1f8c8-121">Maksut kattavat sekä ALV-summan että laskun summan siinä suhteessa, kuinka suuri osa kyseinen maksu on jäljellä olevasta laskun summasta.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-121">Payments covers both VAT and the invoice amount in proportion to the payment's percentage of the remaining invoice amount.</span></span> <span data-ttu-id="1f8c8-122">Maksettu ALV-summa siirretään ei-realisoituneen ALV:n tililtä realisoituneen ALV:n tilille.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-122">The paid VAT amount is transferred from the unrealized VAT account to the realized VAT account.</span></span> |
| <span data-ttu-id="1f8c8-123">Ensimmäinen</span><span class="sxs-lookup"><span data-stu-id="1f8c8-123">First</span></span> | <span data-ttu-id="1f8c8-124">Maksut kattavat ensin ALV:n ja sitten laskun summat.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-124">Payments cover VAT first and then invoice amounts.</span></span> <span data-ttu-id="1f8c8-125">Tässä tapauksessa ei-realisoituneen ALV:in tililtä siirretään ALV-tilille yhtä suuri summa kuin maksun summa kunnes ALV on kokonaisuudessaan maksettu.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-125">In this case, the amount transferred from the unrealized VAT account to the VAT account will equal the amount of the payment until the total VAT has been paid.</span></span> |
| <span data-ttu-id="1f8c8-126">Viimeinen</span><span class="sxs-lookup"><span data-stu-id="1f8c8-126">Last</span></span> | <span data-ttu-id="1f8c8-127">Maksut kattavat ensin laskun summan ja sitten ALV:n.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-127">Payments cover the invoice amount first and then VAT.</span></span> <span data-ttu-id="1f8c8-128">Tässä tapauksessa mitään summaa ei siirretä ei-realisoituneen ALV:in tililtä ALV-tilille ennen kuin koko laskun summa, ilman ALV:tä, on maksettu.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-128">In this case, no amount will be transferred from the unrealized VAT account to the VAT account until the total amount of the invoice, excluding VAT, has been paid.</span></span> |
| <span data-ttu-id="1f8c8-129">Ensimmäinen (kokonaan maksettu)</span><span class="sxs-lookup"><span data-stu-id="1f8c8-129">First (Fully Paid)</span></span> | <span data-ttu-id="1f8c8-130">Maksut kattavat ensin ALV:n (kuten _Ensimmäinen_-vaihtoehdossa), mutta mitään summaa ei siirretä ALV-tilille ennen kuin koko ALV-summa on maksettu.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-130">Payments will cover VAT first (like the _First_ option), but no amount will be transferred to the VAT account until the full amount of VAT has been paid.</span></span> |
| <span data-ttu-id="1f8c8-131">Viimeinen (kokonaan maksettu)</span><span class="sxs-lookup"><span data-stu-id="1f8c8-131">Last (Fully Paid)</span></span> | <span data-ttu-id="1f8c8-132">Maksut kattavat ensin laskun summan (kuten _Viimeinen_-vaihtoehdossa), mutta mitään summaa ei siirretä ALV-tilille ennen kuin koko ALV-summa on maksettu.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-132">Payments will cover invoice amount first (like the _Last_ option), but no amount will be transferred to the VAT account until the full amount of VAT has been paid.</span></span> |

6. <span data-ttu-id="1f8c8-133">Valitse myynnin ei-realisoituneen ALV:n tili **Ei-real. myynti-ALV:n tili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-133">In the **Sales VAT Unreal. Account** field, choose the account for unrealized sales VAT.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="1f8c8-134">ALV-summa kirjataan tälle tilille, jossa se on asiakkaan maksun kirjaamisen saakka.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-134">The VAT amount will be posted to this account, and stay there until the customer payment is posted.</span></span> <span data-ttu-id="1f8c8-135">Summa siirretään sitten myynnin ALV-tilille.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-135">The amount is then transferred to the account for sales VAT.</span></span>
7. <span data-ttu-id="1f8c8-136">Määritä ostojen ei-realisoituneen ALV:n KP-tili **Ostojen ei-realis. ALV:n tili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-136">In the **Purch. VAT Unreal. Account** field, enter the general ledger account for unrealized purchase VAT.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="1f8c8-137">ALV-summa kirjataan tälle tilille, jossa se on asiakkaan maksun kirjaamisen saakka.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-137">The VAT amount will be posted to this account, and stay there until the customer payment is posted.</span></span> <span data-ttu-id="1f8c8-138">Summa siirretään sitten oston ALV-tilille.</span><span class="sxs-lookup"><span data-stu-id="1f8c8-138">The amount is then transferred to the account for purchase VAT.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f8c8-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1f8c8-139">See Also</span></span>
[<span data-ttu-id="1f8c8-140">Arvolisäveron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1f8c8-140">Setting Up Value Added Tax</span></span>](finance-setup-vat.md)

