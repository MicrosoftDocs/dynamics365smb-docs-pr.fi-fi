---
title: "Ongelmien määritys- ja ratkaisutavat | Microsoft Docs"
description: "Lisätietoja Dynamics 365:n Accountant Hubin ongelmien ratkaisemisesta."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a><span data-ttu-id="67a24-103">[!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]in vianmääritys</span><span class="sxs-lookup"><span data-stu-id="67a24-103">Troubleshooting [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="67a24-104">[!INCLUDE[d365acc](includes/d365acc_md.md)]iin rekisteröityminen on helppoa ja nopeaa.</span><span class="sxs-lookup"><span data-stu-id="67a24-104">Signing up for [!INCLUDE[d365acc](includes/d365acc_md.md)] is easy and can be done very quickly.</span></span> <span data-ttu-id="67a24-105">Vaikka asiakkaiden lisääminen koontinäyttöön on helppoa, tässä artikkelissa käsitellään mahdollisesti esiin tulevia ongelmia.</span><span class="sxs-lookup"><span data-stu-id="67a24-105">Adding clients to the dashboard is also easy, but this article addresses issues that you may have on the way.</span></span>

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a><span data-ttu-id="67a24-106">Mitä sähköpostiosoitetta käytetään [!INCLUDE[d365acc](includes/d365acc_md.md)]in kanssa?</span><span class="sxs-lookup"><span data-stu-id="67a24-106">What email address can I use with [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span></span>
[!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="67a24-107"> edellyttää kirjautumista työ- tai opiskelupaikan antamalla sähköpostiosoitteella.</span><span class="sxs-lookup"><span data-stu-id="67a24-107"> requires that you use a work or school email address to sign up.</span></span> [!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="67a24-108"> ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita.</span><span class="sxs-lookup"><span data-stu-id="67a24-108"> does not support email addresses provided by consumer email services or telecommunication providers.</span></span> <span data-ttu-id="67a24-109">Näitä ovat esimerkiksi outlook.com, hotmail.com ja gmail.com.</span><span class="sxs-lookup"><span data-stu-id="67a24-109">This includes outlook.com, hotmail.com, gmail.com, and others.</span></span>  

<span data-ttu-id="67a24-110">Jos yrität rekisteröityä käyttämällä henkilökohtaista sähköpostiosoitetta, saat viestin, jossa pyydetään käyttämään työ- tai opiskelupaikan antamaa sähköpostiosoitetta.</span><span class="sxs-lookup"><span data-stu-id="67a24-110">If you try to sign up with a personal email address, you will get a message indicating to use a work or school email address.</span></span>  

## <a name="why-cant-i-connect-to-my-clients-data"></a><span data-ttu-id="67a24-111">Miksi en voi muodostaa yhteyttä asiakkaani tietoihin?</span><span class="sxs-lookup"><span data-stu-id="67a24-111">Why can't I connect to my client's data?</span></span>
<span data-ttu-id="67a24-112">Syy voi olla esimerkiksi jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="67a24-112">There can be a couple of reasons, including the following:</span></span>

- <span data-ttu-id="67a24-113">**Asiakkaan URL-osoite** -kentässä annettu URL-osoite ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="67a24-113">The URL in the **Client URL** field is not valid</span></span>  

  <span data-ttu-id="67a24-114">Valitse **Asiakkaiden hallinta** ja avaa asiakas, johon et voi muodostaa yhteyttä. Valitse sitten **Testaa asiakkaan URL-osoite**.</span><span class="sxs-lookup"><span data-stu-id="67a24-114">Go to **Manage Clients**, open the client that you cannot connect to, and then choose **Test Client URL**.</span></span>  
- <span data-ttu-id="67a24-115">Asiakkaan yritys on offline-tilassa esimerkiksi päivityksen vuoksi</span><span class="sxs-lookup"><span data-stu-id="67a24-115">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="67a24-116">Valitse koontinäytössä ensin **Työkalut**-valikkovaihtoehto ja sitten **Tarkista virheet**.</span><span class="sxs-lookup"><span data-stu-id="67a24-116">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="67a24-117">Jos avautuvassa teknisten tietojen luettelossa näkyy virheitä, järjestelmänvalvojaan on ehkä syytä ottaa yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="67a24-117">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="67a24-118">Jos virhesanoma esimerkiksi ilmoittaa, että palvelin on hylännyt asiakkaan tunnistetiedot, syynä on todennäköisesti puuttuvat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="67a24-118">For example, the error message "The server has rejected the client credentials" suggests that you do not have access.</span></span>  
- <span data-ttu-id="67a24-119">Et ole saanut asiakkaalta [!INCLUDE[d365fin](includes/d365fin_md.md)]:n käyttäjäksi kutsuvaa sähköpostiviestiä, et ole avannut sähköpostissa olevaa linkkiä tai et ole hyväksynyt kutsua</span><span class="sxs-lookup"><span data-stu-id="67a24-119">You have not received an email from your client that invites them to their [!INCLUDE[d365fin](includes/d365fin_md.md)], or you did not open the link in the email, or you did not accept the invitation</span></span>

  <span data-ttu-id="67a24-120">Sinun on avattava kutsussa oleva linkki ja hyväksyttävä vaiheet, joilla sinut lisätään asiakkaan [!INCLUDE[d365fin](includes/d365fin_md.md)]:een.</span><span class="sxs-lookup"><span data-stu-id="67a24-120">You must open the link in the invitation and accept the steps that adds you to your client's [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="67a24-121">Pääset käyttämään asiakkaan tietoja vasta tämän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="67a24-121">Until then, you do not have access to their data.</span></span>  
- <span data-ttu-id="67a24-122">Sinulla ei ole kaikkien asiakkaan [!INCLUDE[d365fin](includes/d365fin_md.md)]:n yritysten käyttöoikeutta</span><span class="sxs-lookup"><span data-stu-id="67a24-122">You do not have access to all companies in your client's [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>

  <span data-ttu-id="67a24-123">Asiakkaalla voi olla [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä useita liiketoimintayksiköitä tai yrityksiä, eivätkä kaikki yritykset aina sisälly kutsuun.</span><span class="sxs-lookup"><span data-stu-id="67a24-123">Your client can have multiple business units or companies in [!INCLUDE[d365fin](includes/d365fin_md.md)], and your invitation does not always include all companies.</span></span> <span data-ttu-id="67a24-124">Varmista yhdessä asiakkaan kanssa, että sinulla on kaikkien niiden yritysten käyttöoikeudet, joita asiakas haluaa sinun käsittelevän.</span><span class="sxs-lookup"><span data-stu-id="67a24-124">Work with your client to make sure that you have access to the companies that the client wants you to work in.</span></span>  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a><span data-ttu-id="67a24-125">Miksi koontinäytön tiedot eivät päivity?</span><span class="sxs-lookup"><span data-stu-id="67a24-125">Why doesn't the data refresh in my dashboard?</span></span>
<span data-ttu-id="67a24-126">Kun lisäät asiakkaat tai pyydät tietojen päivittämistä, [!INCLUDE[d365acc](includes/d365acc_md.md)] noutaa tiedot.</span><span class="sxs-lookup"><span data-stu-id="67a24-126">When you add a client or request a refresh of the data, [!INCLUDE[d365acc](includes/d365acc_md.md)] fetches the data.</span></span> <span data-ttu-id="67a24-127">Sinun on kuitenkin päivitettävä näyttö itse valitsemalla esimerkiksi Näytä kaikki yritykset uudelleen -toiminnon, päivittämällä selainikkunan tai poistumalla koontinäytöstä ja palaamalla siihen takaisin.</span><span class="sxs-lookup"><span data-stu-id="67a24-127">But you must refresh the window yourself, such as choosing the "Redisplay all companies" action, refresh the browser window, navigate away from the dashboard and then back again, or similar.</span></span> <span data-ttu-id="67a24-128">Tämä on tunnettu ongelma, jota korjataan parhaillaan myöhempää päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="67a24-128">This is a known issue that we are working on improving in a later update.</span></span>  

## <a name="see-also"></a><span data-ttu-id="67a24-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="67a24-129">See Also</span></span>
<span data-ttu-id="67a24-130">[[!INCLUDE[d365acc](includes/d365acc_md.md)]in käytön aloittaminen](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="67a24-130">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="67a24-131">[Asiakkaiden lisääminen [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)in koontinäyttöön</span><span class="sxs-lookup"><span data-stu-id="67a24-131">[Add Clients to Your Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span></span>  

