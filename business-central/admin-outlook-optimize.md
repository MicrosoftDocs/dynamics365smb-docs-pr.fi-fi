---
title: Outlookin optimointi yrityssähköpostia varten
description: Tutustu siihen, miten voit parantaa yrityssähköpostin käyttökokemusta Microsoft Outlookissa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064854"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="56d2e-103">Outlookin optimointi yrityssähköpostia varten</span><span class="sxs-lookup"><span data-stu-id="56d2e-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="56d2e-104">Tässä artikkelissa käsitellään sitä, miten voit saada yrityssähköpostin parhaan mahdollisen käyttökokemuksen Microsoft Outlookissa.</span><span class="sxs-lookup"><span data-stu-id="56d2e-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="56d2e-105">Päivitä Outlook</span><span class="sxs-lookup"><span data-stu-id="56d2e-105">Update Outlook</span></span>

<span data-ttu-id="56d2e-106">Päivitä Outlook-versioon 2012 tai uudempaan.</span><span class="sxs-lookup"><span data-stu-id="56d2e-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="56d2e-107">Jos et pysty päivittämään Outlookia versioon 2012 tai uudempaan, varmista, että päivität ainakin versioon 1905.</span><span class="sxs-lookup"><span data-stu-id="56d2e-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="56d2e-108">Se estää Outlook-apuohjelmaa käyttämästä vanhoja Internet Explorer -komponentteja</span><span class="sxs-lookup"><span data-stu-id="56d2e-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="56d2e-109">Outlook-versiosi tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="56d2e-109">How to check your version of Outlook</span></span>

<span data-ttu-id="56d2e-110">Käytät sitten Office 2019:ää tai Microsoft 365:tä, seuraa tätä Microsoft tukiopasta ja tarkista, mikä Outlook-versio sinulla on:</span><span class="sxs-lookup"><span data-stu-id="56d2e-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="56d2e-111">Tietoja Officesta: mikä Officen versio minulla on käytössä?</span><span class="sxs-lookup"><span data-stu-id="56d2e-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="56d2e-112">Outlookin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="56d2e-112">How to update Outlook</span></span>

<span data-ttu-id="56d2e-113">Jos haluat päivittää Outlookin uusimpaan versioon, noudata tätä Microsoft-tukiopasta tai ota yhteyttä järjestelmänvalvojaan:</span><span class="sxs-lookup"><span data-stu-id="56d2e-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="56d2e-114">Office-päivitysten asentaminen</span><span class="sxs-lookup"><span data-stu-id="56d2e-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="56d2e-115">Microsoft Edge WebView2:n asentaminen</span><span class="sxs-lookup"><span data-stu-id="56d2e-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="56d2e-116">Varmista, että Microsoft Edge WebView2 on asennettu laitteeseesi.</span><span class="sxs-lookup"><span data-stu-id="56d2e-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="56d2e-117">Microsoft Edge WebView2 -asennuksen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="56d2e-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="56d2e-118">Voit tarkistaa Microsoft Edge WebView2 -asennuksen tietokoneeltasi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="56d2e-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="56d2e-119">Käynnistä-valikosta:</span><span class="sxs-lookup"><span data-stu-id="56d2e-119">From Start menu:</span></span>

1. <span data-ttu-id="56d2e-120">Valitse **Käynnistä** ![Windowsin käynnistys](media/windows-start-icon.png "Windowsin Käynnistä-kuvake") > **Asetukset** ![Windowsin asetukset](media/windows-settings-icon.png "Windowsin Asetukset-kuvake") > **Sovellukset ja ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="56d2e-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="56d2e-121">Kirjoita hakukenttään **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="56d2e-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="56d2e-122">Jos Microsoft Edge WebView2 on asennettuna, näet merkinnän nimeltä **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="56d2e-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="56d2e-123">Ohjauspaneelista:</span><span class="sxs-lookup"><span data-stu-id="56d2e-123">From Control Panel:</span></span>

1. <span data-ttu-id="56d2e-124">Kirjoita kohdan **Käynnistä** ![Windowsin käynnistys](media/windows-start-icon.png "Windowsin Käynnistä-kuvake") vieressä olevaan hakukenttään **Ohjauspaneeli** ja valitse sitten tulos.</span><span class="sxs-lookup"><span data-stu-id="56d2e-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="56d2e-125">Valitse **Ohjelmat** > **Ohjelmat ja ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="56d2e-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="56d2e-126">Kirjoita hakukenttään **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="56d2e-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="56d2e-127">Jos Microsoft Edge WebView2 on asennettuna, näet merkinnän nimeltä **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="56d2e-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="56d2e-128">Microsoft Edge WebView2:n asentaminen</span><span class="sxs-lookup"><span data-stu-id="56d2e-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="56d2e-129">Siirry selaimen avulla kohteeseen [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="56d2e-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="56d2e-130">Valitse **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="56d2e-130">Choose **Download**.</span></span>
3. <span data-ttu-id="56d2e-131">Aseta **Valitse arkkitehtuuri** järjestelmääsi vastaavaksi.</span><span class="sxs-lookup"><span data-stu-id="56d2e-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="56d2e-132">Valitse **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="56d2e-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="56d2e-133">Organisaatiosi saattaa rajoittaa sitä, mitä komponentteja laitteeseesi voi asentaa.</span><span class="sxs-lookup"><span data-stu-id="56d2e-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="56d2e-134">Pyydä apua järjestelmänvalvojalta.</span><span class="sxs-lookup"><span data-stu-id="56d2e-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="56d2e-135">Käytä tuettua selainta</span><span class="sxs-lookup"><span data-stu-id="56d2e-135">Use a supported browser</span></span>

<span data-ttu-id="56d2e-136">Harkitse Outlookin verkkoversion käyttämistä jossakin Business Centralin tukemassa selaimessa.</span><span class="sxs-lookup"><span data-stu-id="56d2e-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="56d2e-137">Luettelo tuetuista selaimista on kohdassa [Business Centralin käyttämisen vähimmäisvaatimukset](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="56d2e-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="56d2e-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="56d2e-138">See Also</span></span>

[<span data-ttu-id="56d2e-139">Valmistautuminen liiketoimintaan</span><span class="sxs-lookup"><span data-stu-id="56d2e-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="56d2e-140">Business Centralin hakeminen omaan mobiililaitteeseen</span><span class="sxs-lookup"><span data-stu-id="56d2e-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="56d2e-141">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="56d2e-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="56d2e-142">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="56d2e-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="56d2e-143">Myynti</span><span class="sxs-lookup"><span data-stu-id="56d2e-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="56d2e-144">Osto</span><span class="sxs-lookup"><span data-stu-id="56d2e-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="56d2e-145">Outlookin vähimmäisvaatimukset</span><span class="sxs-lookup"><span data-stu-id="56d2e-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="56d2e-146">Apuohjelmien käyttäminen Outlookin verkkoversiossa</span><span class="sxs-lookup"><span data-stu-id="56d2e-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]