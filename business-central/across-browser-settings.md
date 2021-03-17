---
title: Selaimen määrittäminen
description: Tässä artikkelissa kuvataan, miten selaimet määritetään toimimaan Business Centralin ja siihen integroitavien tuotteiden kanssa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: b5083735be31b635cb3fc3ce404e7f182d04640f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384972"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="a79b6-103">Selaimen määrittäminen ja vianetsintä Business Central -verkkoasiakkaan kanssa työskentelyä varten</span><span class="sxs-lookup"><span data-stu-id="a79b6-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="a79b6-104">Tässä artikkelissa kerrotaan, miten selain määritetään niin, että [!INCLUDE[web_client](includes/web_client.md)] ja kaikki sen ominaisuudet toimivat oikein.</span><span class="sxs-lookup"><span data-stu-id="a79b6-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="a79b6-105">Lue tämä artikkeli, jos sinulla on ongelmia [!INCLUDE[web_client](includes/web_client.md)]:n avaamisessa, koska selaimen asetukset saattavat aiheuttaa joitakin ongelmia.</span><span class="sxs-lookup"><span data-stu-id="a79b6-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="a79b6-106">Artikkelissa on yksityiskohtaisia tietoja Microsoft Edgen määrityksestä, mutta JavaScriptin, evästeiden ja ponnahdusikkunoiden vaatimukset ovat samat kaikissa tuetuissa selaimissa.</span><span class="sxs-lookup"><span data-stu-id="a79b6-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="a79b6-107">Katso lisätietoja muista selaimista valmistajan tarjoamista ohjeista.</span><span class="sxs-lookup"><span data-stu-id="a79b6-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="a79b6-108">Käytä tuettua selainta</span><span class="sxs-lookup"><span data-stu-id="a79b6-108">Use a supported browser</span></span>

<span data-ttu-id="a79b6-109">Varmista, että käytät jotakin tuetuista selaimista.</span><span class="sxs-lookup"><span data-stu-id="a79b6-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="a79b6-110">Lisätietoja: [Business Central -sovelluksen käytön vähimmäisvaatimukset](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="a79b6-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="a79b6-111">Salli JavaScript Business Centralista</span><span class="sxs-lookup"><span data-stu-id="a79b6-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="a79b6-112">*Ongelma:*</span><span class="sxs-lookup"><span data-stu-id="a79b6-112">*Problem:*</span></span>

<span data-ttu-id="a79b6-113">Jos selain ei salli JavaScriptiä, näet osoite rivillä **Notsupported/DisabledJavaScript**-ilmoituksen ja **HTTP-virhe 404.0 – Ei löydy** -sanoman yritettäessä avata [!INCLUDE[prod_short](includes/prod_short.md)]ia ja</span><span class="sxs-lookup"><span data-stu-id="a79b6-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="a79b6-114">*Korjaus:*</span><span class="sxs-lookup"><span data-stu-id="a79b6-114">*Fix:*</span></span>

1. <span data-ttu-id="a79b6-115">Siirry Microsoft Edgessä kohtaan **Asetukset** > **Evästeet ja sivuston käyttöoikeudet** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="a79b6-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="a79b6-116">Tee jompikumpi seuraavista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="a79b6-116">Do one of the following steps.</span></span> <span data-ttu-id="a79b6-117">Valitse organisaatiosi suosittelema vaihe:</span><span class="sxs-lookup"><span data-stu-id="a79b6-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="a79b6-118">Siirrä **Sallittu**-valitsin vasemmalle (pois käytöstä).</span><span class="sxs-lookup"><span data-stu-id="a79b6-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="a79b6-119">Valitse sitten **Lisää** ja kirjoita [!INCLUDE[prod_short](includes/prod_short.md)]in osoite (URL-osoite) **Sivusto**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="a79b6-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="a79b6-120">Valitse **Lisää**, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="a79b6-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="a79b6-121">Siirrä **Sallittu**-valitsin oikealle (käytössä).</span><span class="sxs-lookup"><span data-stu-id="a79b6-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="a79b6-122">Salli evästeet Business Centralista</span><span class="sxs-lookup"><span data-stu-id="a79b6-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="a79b6-123">*Ongelma:*</span><span class="sxs-lookup"><span data-stu-id="a79b6-123">*Problem:*</span></span>

<span data-ttu-id="a79b6-124">Jos selain ei salli evästeitä, saat seuraavan virheilmoituksen:</span><span class="sxs-lookup"><span data-stu-id="a79b6-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="a79b6-125">**Sivua ei valitettavasti löytynyt. Tarkista osoite ja yritä uudelleen.**</span><span class="sxs-lookup"><span data-stu-id="a79b6-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="a79b6-126">*Korjaus:*</span><span class="sxs-lookup"><span data-stu-id="a79b6-126">*Fix:*</span></span>

1. <span data-ttu-id="a79b6-127">Siirry Microsoft Edgessä kohtaan **Asetukset** > **Evästeet ja sivuston käyttöoikeudet** > **Evästeet ja sivuston tiedot**.</span><span class="sxs-lookup"><span data-stu-id="a79b6-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="a79b6-128">Siirrä **Salli sivustojen tallentaa ja lukea evästetietoja** -valitsin oikealle (päällä).</span><span class="sxs-lookup"><span data-stu-id="a79b6-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="a79b6-129">Salli ponnahdusikkunat Business Centralista</span><span class="sxs-lookup"><span data-stu-id="a79b6-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a79b6-130">integroituu useisiin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="a79b6-130">integrates with several products.</span></span> <span data-ttu-id="a79b6-131">Joissakin tapauksissa, kuten Microsoft Teamsin kanssa, [!INCLUDE[prod_short](includes/prod_short.md)] avaa tai "ponnauttaa" ponnahdusikkunan tuotteen sisällä.</span><span class="sxs-lookup"><span data-stu-id="a79b6-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="a79b6-132">Tämä ominaisuus edellyttää, että selain sallii ponnahdusikkunat [!INCLUDE[prod_short](includes/prod_short.md)]ista.</span><span class="sxs-lookup"><span data-stu-id="a79b6-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="a79b6-133">*Ongelma:*</span><span class="sxs-lookup"><span data-stu-id="a79b6-133">*Problem:*</span></span>

<span data-ttu-id="a79b6-134">Jos [!INCLUDE[prod_short](includes/prod_short.md)]in ponnahdusikkunat estetään, näyttöön tulee seuraavankaltainen sanoma:</span><span class="sxs-lookup"><span data-stu-id="a79b6-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="a79b6-135">**Jokin meni pieleen. Selaimesi saattaa estää Business Centralin tarvitsemat ponnahdusikkunat.**</span><span class="sxs-lookup"><span data-stu-id="a79b6-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="a79b6-136">*Korjaus:*</span><span class="sxs-lookup"><span data-stu-id="a79b6-136">*Fix:*</span></span>

1. <span data-ttu-id="a79b6-137">Siirry Microsoft Edgessä kohtaan **Asetukset** > **Evästeet ja sivuston käyttöoikeudet** > **Ponnahdusikkunat ja uudelleenohjaukset**.</span><span class="sxs-lookup"><span data-stu-id="a79b6-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="a79b6-138">Siirrä **Estetty**-valitsin oikealle (käytössä).</span><span class="sxs-lookup"><span data-stu-id="a79b6-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="a79b6-139">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a79b6-139">Select **Add**.</span></span> <span data-ttu-id="a79b6-140">Kirjoita **Sivusto**- ruutuun `https://businesscentral.dynamics.com` ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a79b6-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a79b6-141">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a79b6-141">See Also</span></span>

[<span data-ttu-id="a79b6-142">Vianetsintä – Teams</span><span class="sxs-lookup"><span data-stu-id="a79b6-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]