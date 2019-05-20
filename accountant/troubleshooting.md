---
title: Ongelmien määritys- ja ratkaisutavat | Microsoft Docs
description: Lisätietoja Dynamics 365:n Accountant Hubin ongelmien ratkaisemisesta.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.openlocfilehash: 0ebd99e9097e4c701038f3b8be7a07d1e80a4b31
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1237978"
---
# <a name="troubleshooting-include-d365acclongincludesd365acclongmdmd"></a><span data-ttu-id="1d48a-103">[!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]in vianmääritys</span><span class="sxs-lookup"><span data-stu-id="1d48a-103">Troubleshooting [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="1d48a-104">[!INCLUDE [d365acc](includes/d365acc_md.md)]iin rekisteröityminen on helppoa ja nopeaa.</span><span class="sxs-lookup"><span data-stu-id="1d48a-104">Signing up for [!INCLUDE [d365acc](includes/d365acc_md.md)] is easy and can be done very quickly.</span></span> <span data-ttu-id="1d48a-105">Vaikka asiakkaiden lisääminen koontinäyttöön on helppoa, tässä artikkelissa käsitellään mahdollisesti esiin tulevia ongelmia.</span><span class="sxs-lookup"><span data-stu-id="1d48a-105">Adding clients to the dashboard is also easy, but this article addresses issues that you may have on the way.</span></span>

## <a name="what-email-address-can-i-use-with-include-d365accincludesd365accmdmd"></a><span data-ttu-id="1d48a-106">Mitä sähköpostiosoitetta käytetään [!INCLUDE [d365acc](includes/d365acc_md.md)]in kanssa?</span><span class="sxs-lookup"><span data-stu-id="1d48a-106">What email address can I use with [!INCLUDE [d365acc](includes/d365acc_md.md)]?</span></span>
<span data-ttu-id="1d48a-107">[!INCLUDE [d365acc](includes/d365acc_md.md)] edellyttää kirjautumista työ- tai opiskelupaikan antamalla sähköpostiosoitteella.</span><span class="sxs-lookup"><span data-stu-id="1d48a-107">[!INCLUDE [d365acc](includes/d365acc_md.md)] requires that you use a work or school email address to sign up.</span></span> <span data-ttu-id="1d48a-108">[!INCLUDE [d365acc](includes/d365acc_md.md)] ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita.</span><span class="sxs-lookup"><span data-stu-id="1d48a-108">[!INCLUDE [d365acc](includes/d365acc_md.md)] does not support email addresses provided by consumer email services or telecommunication providers.</span></span> <span data-ttu-id="1d48a-109">Näitä ovat esimerkiksi outlook.com, hotmail.com ja gmail.com.</span><span class="sxs-lookup"><span data-stu-id="1d48a-109">This includes outlook.com, hotmail.com, gmail.com, and others.</span></span>  

<span data-ttu-id="1d48a-110">Jos yrität rekisteröityä käyttämällä henkilökohtaista sähköpostiosoitetta, saat viestin, jossa pyydetään käyttämään työ- tai opiskelupaikan antamaa sähköpostiosoitetta.</span><span class="sxs-lookup"><span data-stu-id="1d48a-110">If you try to sign up with a personal email address, you will get a message indicating to use a work or school email address.</span></span>  

## <a name="why-cant-i-connect-to-my-clients-data"></a><span data-ttu-id="1d48a-111">Miksi en voi muodostaa yhteyttä asiakkaani tietoihin?</span><span class="sxs-lookup"><span data-stu-id="1d48a-111">Why can't I connect to my client's data?</span></span>
<span data-ttu-id="1d48a-112">Syy voi olla esimerkiksi jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="1d48a-112">There can be a couple of reasons, including the following:</span></span>

- <span data-ttu-id="1d48a-113">**Asiakkaan URL-osoite** -kentässä annettu URL-osoite ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="1d48a-113">The URL in the **Client URL** field is not valid</span></span>  

  <span data-ttu-id="1d48a-114">Valitse **Asiakkaiden hallinta** ja avaa asiakas, johon et voi muodostaa yhteyttä. Valitse sitten **Testaa asiakkaan URL-osoite**.</span><span class="sxs-lookup"><span data-stu-id="1d48a-114">Go to **Manage Clients**, open the client that you cannot connect to, and then choose **Test Client URL**.</span></span>  
- <span data-ttu-id="1d48a-115">Asiakkaan yritys on offline-tilassa esimerkiksi päivityksen vuoksi</span><span class="sxs-lookup"><span data-stu-id="1d48a-115">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="1d48a-116">Valitse koontinäytössä ensin **Työkalut**-valikkovaihtoehto ja sitten **Tarkista virheet**.</span><span class="sxs-lookup"><span data-stu-id="1d48a-116">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="1d48a-117">Jos avautuvassa teknisten tietojen luettelossa näkyy virheitä, järjestelmänvalvojaan on ehkä syytä ottaa yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="1d48a-117">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="1d48a-118">Jos virhesanoma esimerkiksi ilmoittaa, että palvelin on hylännyt asiakkaan tunnistetiedot, syynä on todennäköisesti puuttuvat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="1d48a-118">For example, the error message "The server has rejected the client credentials" suggests that you do not have access.</span></span>  
- <span data-ttu-id="1d48a-119">Et ole saanut asiakkaalta [!INCLUDE [d365fin](includes/d365fin_md.md)]:n käyttäjäksi kutsuvaa sähköpostiviestiä, et ole avannut sähköpostissa olevaa linkkiä tai et ole hyväksynyt kutsua</span><span class="sxs-lookup"><span data-stu-id="1d48a-119">You have not received an email from your client that invites them to their [!INCLUDE [d365fin](includes/d365fin_md.md)], or you did not open the link in the email, or you did not accept the invitation</span></span>

  <span data-ttu-id="1d48a-120">Sinun on avattava kutsussa oleva linkki ja hyväksyttävä vaiheet, joilla sinut lisätään asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]:een.</span><span class="sxs-lookup"><span data-stu-id="1d48a-120">You must open the link in the invitation and accept the steps that adds you to your client's [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1d48a-121">Pääset käyttämään asiakkaan tietoja vasta tämän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1d48a-121">Until then, you do not have access to their data.</span></span>  
- <span data-ttu-id="1d48a-122">Sinulla ei ole kaikkien asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]:n yritysten käyttöoikeutta</span><span class="sxs-lookup"><span data-stu-id="1d48a-122">You do not have access to all companies in your client's [!INCLUDE [d365fin](includes/d365fin_md.md)]</span></span>

  <span data-ttu-id="1d48a-123">Asiakkaalla voi olla [!INCLUDE [d365fin](includes/d365fin_md.md)]:ssä useita liiketoimintayksiköitä tai yrityksiä, eivätkä kaikki yritykset aina sisälly kutsuun.</span><span class="sxs-lookup"><span data-stu-id="1d48a-123">Your client can have multiple business units or companies in [!INCLUDE [d365fin](includes/d365fin_md.md)], and your invitation does not always include all companies.</span></span> <span data-ttu-id="1d48a-124">Varmista yhdessä asiakkaan kanssa, että sinulla on kaikkien niiden yritysten käyttöoikeudet, joita asiakas haluaa sinun käsittelevän.</span><span class="sxs-lookup"><span data-stu-id="1d48a-124">Work with your client to make sure that you have access to the companies that the client wants you to work in.</span></span>  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a><span data-ttu-id="1d48a-125">Miksi koontinäytön tiedot eivät päivity?</span><span class="sxs-lookup"><span data-stu-id="1d48a-125">Why doesn't the data refresh in my dashboard?</span></span>
<span data-ttu-id="1d48a-126">Kun lisäät asiakkaat tai pyydät tietojen päivittämistä, [!INCLUDE [d365acc](includes/d365acc_md.md)] noutaa tiedot.</span><span class="sxs-lookup"><span data-stu-id="1d48a-126">When you add a client or request a refresh of the data, [!INCLUDE [d365acc](includes/d365acc_md.md)] fetches the data.</span></span> <span data-ttu-id="1d48a-127">Sinun on kuitenkin päivitettävä sivu itse valitsemalla esimerkiksi Näytä kaikki yritykset uudelleen -toiminnon, päivittämällä selaimen sivu tai poistumalla koontinäytöstä ja palaamalla siihen takaisin.</span><span class="sxs-lookup"><span data-stu-id="1d48a-127">But you must refresh the page yourself, such as choosing the "Redisplay all companies" action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span> <span data-ttu-id="1d48a-128">Tämä on tunnettu ongelma, jota korjataan parhaillaan myöhempää päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="1d48a-128">This is a known issue that we are working on improving in a later update.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d48a-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1d48a-129">See Also</span></span>
<span data-ttu-id="1d48a-130">[[!INCLUDE[d365acc](includes/d365acc_md.md)]in käytön aloittaminen](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="1d48a-130">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="1d48a-131">[Asiakkaiden lisääminen [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)in koontinäyttöön</span><span class="sxs-lookup"><span data-stu-id="1d48a-131">[Add Clients to Your Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span></span>  
