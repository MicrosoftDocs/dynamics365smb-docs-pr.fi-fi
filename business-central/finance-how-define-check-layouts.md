---
title: Sekin asettelun määrittäminen| Microsoft Docs
description: Voit suunnitella ja tulostaa sekkisi eri muodoissa standardinmukaisia vaatimuksia noudattaen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ac980cb4b64a39b7ed912a49b06c179ffc7219d9
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386497"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="5afd6-103">Sekin asettelun valitseminen</span><span class="sxs-lookup"><span data-stu-id="5afd6-103">Select a Check Layout</span></span>
<span data-ttu-id="5afd6-104">Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja.</span><span class="sxs-lookup"><span data-stu-id="5afd6-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="5afd6-105">Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.</span><span class="sxs-lookup"><span data-stu-id="5afd6-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="5afd6-106">Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.</span><span class="sxs-lookup"><span data-stu-id="5afd6-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="5afd6-107">Sekin asettelun valitseminen</span><span class="sxs-lookup"><span data-stu-id="5afd6-107">To select a check layout</span></span>
1. <span data-ttu-id="5afd6-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Raporttivalintojen pankkitili** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5afd6-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="5afd6-109">Valitse **Raporttivalinta - Pankkitili** -sivun **Käyttö**-kentässä **Sekki**.</span><span class="sxs-lookup"><span data-stu-id="5afd6-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="5afd6-110">Valitse jompikumpi seuraavista raportin tunnuksista:</span><span class="sxs-lookup"><span data-stu-id="5afd6-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="5afd6-111">Raportin tunnus</span><span class="sxs-lookup"><span data-stu-id="5afd6-111">Report ID</span></span> | <span data-ttu-id="5afd6-112">Raportin nimi</span><span class="sxs-lookup"><span data-stu-id="5afd6-112">Report Name</span></span> | <span data-ttu-id="5afd6-113">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5afd6-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5afd6-114">1401</span><span class="sxs-lookup"><span data-stu-id="5afd6-114">1401</span></span> |<span data-ttu-id="5afd6-115">Sekki</span><span class="sxs-lookup"><span data-stu-id="5afd6-115">Check</span></span> |<span data-ttu-id="5afd6-116">Tämä on oletusraportti.</span><span class="sxs-lookup"><span data-stu-id="5afd6-116">This is the default report.</span></span> |
| <span data-ttu-id="5afd6-117">10411</span><span class="sxs-lookup"><span data-stu-id="5afd6-117">10411</span></span> |<span data-ttu-id="5afd6-118">Sekki (talonki/talonki/sekki)</span><span class="sxs-lookup"><span data-stu-id="5afd6-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="5afd6-119">Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki.</span><span class="sxs-lookup"><span data-stu-id="5afd6-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="5afd6-120">10412</span><span class="sxs-lookup"><span data-stu-id="5afd6-120">10412</span></span> |<span data-ttu-id="5afd6-121">Sekki (talonki/sekki/talonki)</span><span class="sxs-lookup"><span data-stu-id="5afd6-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="5afd6-122">Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/sekki/talonki.</span><span class="sxs-lookup"><span data-stu-id="5afd6-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="5afd6-123">10413</span><span class="sxs-lookup"><span data-stu-id="5afd6-123">10413</span></span> |<span data-ttu-id="5afd6-124">Kolme sekkiä sivulla</span><span class="sxs-lookup"><span data-stu-id="5afd6-124">Three Checks per Page</span></span> |<span data-ttu-id="5afd6-125">Tämä raportti on suunniteltu tulostamaan kolme sekkiä kullakin sivulla.</span><span class="sxs-lookup"><span data-stu-id="5afd6-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="5afd6-126">Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="5afd6-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="5afd6-127">Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="5afd6-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="5afd6-128">Voit muuttaa jotakin näistä sekkien oletusasetteluista käyttämällä joko Word- tai RDLC-integrointia.</span><span class="sxs-lookup"><span data-stu-id="5afd6-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="5afd6-129">Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="5afd6-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="using-micr-and-security-fonts"></a><span data-ttu-id="5afd6-130">MICR- ja suojausfonttien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="5afd6-130">Using MICR and Security Fonts</span></span>
<span data-ttu-id="5afd6-131">[!INCLUDE[prod_short](includes/prod_short.md)]:n online-versio sisältää valmiiksi asennetut fontit palvelimissa, joita voidaan käyttää sekin asettelujen määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="5afd6-131">The online version of [!INCLUDE[prod_short](includes/prod_short.md)] contains pre-installed fonts on the servers that can be used when defining check layouts.</span></span> <span data-ttu-id="5afd6-132">Seuraavassa on esitetty, mitkä fontit ovat käytettävissä, ja siinä on linkit kolmansien osapuolten fonttien toimittajien yksityiskohtaisiin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="5afd6-132">The following outlines which fonts are available and has links to detailed information by the 3rd-party suppliers of the fonts.</span></span>

> [!Important]
> <span data-ttu-id="5afd6-133">MICR- ja sekki-suojausfontit Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] on lisensoitu IDAutomation.com, Inc:n fonttipaketissa. Näitä tuotteita saa käyttää vain Microsoft Dynamicsin osana- ja yhteydessä [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="5afd6-133">MICR and check security fonts in Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] are licensed in a font package from IDAutomation.com, Inc. These products may only be used as part of and in connection with Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="5afd6-134">Päivityksessä 15.3 ja uudemmissa on asennettu magneettisten merkkien tunnistuksen (MICR) fontteja, jotka ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5afd6-134">In update 15.3 and newer, Magnetic Ink Character Recognition (MICR) fonts are installed and available to use.</span></span> <span data-ttu-id="5afd6-135">Sekä E-13B- että CMC-7-standardit ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="5afd6-135">Both the E-13B and the CMC-7 standards are supported.</span></span> <span data-ttu-id="5afd6-136">MICR-fonttien lisäksi käytettävissä on erityisiä suojausfontteja, joiden avulla voidaan luoda tekstiä, nimiä, summia ja valuuttasymboleita: dollari, euro, punta ja jeni, joita on vaikea väärentää, kun sekki on tulostettu.</span><span class="sxs-lookup"><span data-stu-id="5afd6-136">In addition to MICR fonts, special security fonts are available to generate text, names, amounts, and the currency symbols Dollar, Euro, Pound, and Yen, which are hard to tamper with once a check has been printed.</span></span>

> [!NOTE]
> <span data-ttu-id="5afd6-137">Suojaus- ja oikeudellisista syistä mukautettuja fontteja ei voi ladata [!INCLUDE[prod_short](includes/prod_short.md)]-ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="5afd6-137">For security and legal reasons, you cannot upload custom fonts to the [!INCLUDE[prod_short](includes/prod_short.md)] environment.</span></span>

### <a name="micr-e-13b-specifications"></a><span data-ttu-id="5afd6-138">MICR E-13B -määritykset</span><span class="sxs-lookup"><span data-stu-id="5afd6-138">MICR E-13B Specifications</span></span>
<span data-ttu-id="5afd6-139">Seuraavassa on yhteenveto MICR E-13B -fonteista, joista voi olla hyötyä, kun fontteja kalibroidaan sekkiasetteluissa tiettyjen MICR-tulostimien avulla.</span><span class="sxs-lookup"><span data-stu-id="5afd6-139">The following summarizes specifications for the MICR E-13B fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="5afd6-140">![MICR E-13B -määritykset](media/font_MICR_E-13B_Specifications.png "MICR E-13B -määritykset")</span><span class="sxs-lookup"><span data-stu-id="5afd6-140">![MICR E-13B Specifications](media/font_MICR_E-13B_Specifications.png "MICR E-13B Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="5afd6-141">Erottimen merkit</span><span class="sxs-lookup"><span data-stu-id="5afd6-141">Delimiter characters</span></span>
<span data-ttu-id="5afd6-142">![Erottimen merkit](media/font-micr-letters.png "Erottimen merkit")</span><span class="sxs-lookup"><span data-stu-id="5afd6-142">![Delimiter characters](media/font-micr-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="5afd6-143">MICR E-13B -fonttien kokomääritys löytyy toimittajan dokumentaatiosta täältä: (https://www.idautomation.com/micr-fonts/e13b/).</span><span class="sxs-lookup"><span data-stu-id="5afd6-143">The full specification of MICR E-13B fonts can be found in the supplier's documentation here: (https://www.idautomation.com/micr-fonts/e13b/).</span></span>

### <a name="micr-cmc-7-specifications"></a><span data-ttu-id="5afd6-144">MICR CMC-7 -määritykset</span><span class="sxs-lookup"><span data-stu-id="5afd6-144">MICR CMC-7 Specifications</span></span>
<span data-ttu-id="5afd6-145">Seuraavat CMC-7 -fontit ovat käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)] -online-käytössä:</span><span class="sxs-lookup"><span data-stu-id="5afd6-145">The following CMC-7 fonts are available in [!INCLUDE[prod_short](includes/prod_short.md)] online:</span></span>

- <span data-ttu-id="5afd6-146">IDAutomationCMC7</span><span class="sxs-lookup"><span data-stu-id="5afd6-146">IDAutomationCMC7</span></span>
- <span data-ttu-id="5afd6-147">IDAutomationCMC7n10</span><span class="sxs-lookup"><span data-stu-id="5afd6-147">IDAutomationCMC7n10</span></span>
- <span data-ttu-id="5afd6-148">IDAutomationCMC7n25</span><span class="sxs-lookup"><span data-stu-id="5afd6-148">IDAutomationCMC7n25</span></span>
-   <span data-ttu-id="5afd6-149">IDAutomationCMC7n40</span><span class="sxs-lookup"><span data-stu-id="5afd6-149">IDAutomationCMC7n40</span></span>

<span data-ttu-id="5afd6-150">Seuraavassa on yhteenveto MICR CMC-7 -fonteista, joista voi olla hyötyä, kun fontteja kalibroidaan sekkiasetteluissa tiettyjen MICR-tulostimien avulla.</span><span class="sxs-lookup"><span data-stu-id="5afd6-150">The following summarizes specifications for the MICR CMC-7 fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="5afd6-151">![MICR CMC-7 -määritykset](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 -määritykset")</span><span class="sxs-lookup"><span data-stu-id="5afd6-151">![MICR CMC-7 Specifications](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="5afd6-152">Erottimen merkit</span><span class="sxs-lookup"><span data-stu-id="5afd6-152">Delimiter characters</span></span>
<span data-ttu-id="5afd6-153">![Erottimen merkit](media/font-cmc7-letters.png "Erottimen merkit")</span><span class="sxs-lookup"><span data-stu-id="5afd6-153">![Delimiter characters](media/font-cmc7-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="5afd6-154">MICR CMC-7 -fonttien kokomääritys löytyy toimittajan dokumentaatiosta täältä: (http://www.idautomation.com/micr-fonts/cmc7/).</span><span class="sxs-lookup"><span data-stu-id="5afd6-154">The full specification of MICR CMC-7 fonts can be found in the supplier's documentation here: (http://www.idautomation.com/micr-fonts/cmc7/).</span></span>

### <a name="secure-font-specifications"></a><span data-ttu-id="5afd6-155">Suojattujen fonttien määritykset</span><span class="sxs-lookup"><span data-stu-id="5afd6-155">Secure Font Specifications</span></span>
<span data-ttu-id="5afd6-156">Seuraavassa on yhteenveto sekkisuojausfonteista, joista voi olla hyötyä, kun fontteja kalibroidaan sekkiasetteluissa tiettyjen MICR-tulostimien avulla.</span><span class="sxs-lookup"><span data-stu-id="5afd6-156">The following summarizes specifications for check security fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="5afd6-157">![Suojausfonttien määritysten tarkistaminen](media/font_check-security-font_Specifications.png "Suojausfonttien määritysten tarkistaminen")</span><span class="sxs-lookup"><span data-stu-id="5afd6-157">![Check Security Font Specifications](media/font_check-security-font_Specifications.png "Check Security Font Specifications")</span></span>

<span data-ttu-id="5afd6-158">Sekkisuojausfonttien kokomääritys löytyy toimittajan dokumentaatiosta täältä: (https://www.idautomation.com/security-fonts/).</span><span class="sxs-lookup"><span data-stu-id="5afd6-158">The full specification of check security fonts can be found in the supplier's documentation here: (https://www.idautomation.com/security-fonts/).</span></span>

<span data-ttu-id="5afd6-159">Fontit muihin tarkoituksiin ovat myös saatavilla [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="5afd6-159">Fonts for other purposes are also available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="5afd6-160">Lisätietoja on kohdassa [Käytettävissä olevat fontit](ui-fonts.md)</span><span class="sxs-lookup"><span data-stu-id="5afd6-160">For more information, see [Available Fonts](ui-fonts.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="5afd6-161">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5afd6-161">See Also</span></span>
[<span data-ttu-id="5afd6-162">Raporttien mukautettujen asettelujen luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="5afd6-162">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="5afd6-163">Fontit Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="5afd6-163">Fonts in Business Central</span></span>](ui-fonts.md)  
[<span data-ttu-id="5afd6-164">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="5afd6-164">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="5afd6-165">[Pankkitilien täsmäytys](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="5afd6-165">[Reconciling Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="5afd6-166">Kauden lopun prosessien viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="5afd6-166">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="5afd6-167">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5afd6-167">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5afd6-168">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="5afd6-168">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]