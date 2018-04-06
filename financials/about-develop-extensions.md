---
title: Microsoft Dynamics 365 for Finance and Operations, Business editionin mukauttaminen | Microsoft Docs
description: Finance and Operations, Business editionin sovellusten ja laajennusten luonti, esittely ja markkinointi.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 72e0a33326eaff03250b448275fa10715eb56e95
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="ca9ca-103">[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -järjestelmän laajentaminen</span><span class="sxs-lookup"><span data-stu-id="ca9ca-103">Extending [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="ca9ca-104">[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in käytöstä alustana on monia etuja sovellusten muodostajille:</span><span class="sxs-lookup"><span data-stu-id="ca9ca-104">There are plenty of benefits of using [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] as a platform for App builders:</span></span>

* <span data-ttu-id="ca9ca-105">[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] on todistetusti toimiva Microsoftin verkkoratkaisu, jota voit täydentää omalla osaamisellasi.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-105">Enrich [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], a proven Microsoft online solution, with your expertise</span></span>  
* <span data-ttu-id="ca9ca-106">Voit hyödyntää Finance and Operations, Business edition -brändiä, jonka miljoonat käyttäjät tuntevat ja johon he luottavat.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-106">Leverage the Finance and Operations, Business edition brand – a brand that millions of users know and trust</span></span>  
* <span data-ttu-id="ca9ca-107">Liiketoimintasovelluksesi tavoittavat entistä enemmän asiakkaita [Microsoft AppSourcen](https://appsource.microsoft.com/) kautta.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-107">Reach more customers for your business apps with [Microsoft AppSource](https://appsource.microsoft.com/)</span></span>  
* <span data-ttu-id="ca9ca-108">Modernien käyttökokemuksen tarjoava skaalautuva alusta parantaa tuloksia.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-108">Achieve more with a platform that delivers a modern experience and offers scale</span></span>  
* <span data-ttu-id="ca9ca-109">Yhdistäminen älykkäisiin liiketoimintasovelluksiin, kuten PowerApps, Flow, Power BI ja Cortana Intelligence, on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-109">Bundle with intelligent business apps such as PowerApps, Flow, Power BI, Cortana Intelligence, and many more</span></span>  

## <a name="to-bring-your-included365finincludesd365finmdmd-app-into-appsource"></a><span data-ttu-id="ca9ca-110">Oman [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen tuominen AppSourceen:</span><span class="sxs-lookup"><span data-stu-id="ca9ca-110">To bring your [!INCLUDE[d365fin](includes/d365fin_md.md)] app into AppSource:</span></span>
+ <span data-ttu-id="ca9ca-111">Omien tilien luominen</span><span class="sxs-lookup"><span data-stu-id="ca9ca-111">Create your accounts</span></span>  
<span data-ttu-id="ca9ca-112">Haluamme, että kaikki tarvittavat työkalut ovat käytössäsi.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-112">We want you to have access to all the necessary tools!</span></span> <span data-ttu-id="ca9ca-113">Sinulla on oltava Microsoftin kumppaniverkoston tunnus, kehittäjätili ja PSBC-tili.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-113">You must have a Microsoft Partner Network ID, a Developer account, and a PSBC account.</span></span>
<span data-ttu-id="ca9ca-114">Lisätietoja tilien asetuksista on Download Centerin [Tilien luonti.pdf](https://go.microsoft.com/fwlink/?linkid=841514) -tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-114">For more information about how you can get your accounts in place, get the [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) document from the Download Center.</span></span>

+ <span data-ttu-id="ca9ca-115">Sovellusideaa koskeva keskustelu</span><span class="sxs-lookup"><span data-stu-id="ca9ca-115">Engage with us about your app idea</span></span>  
<span data-ttu-id="ca9ca-116">Jaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellusta koskeva ideasi Microsoft AppSourcessa.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-116">Share your [!INCLUDE[d365fin](includes/d365fin_md.md)] app idea with us on Microsoft AppSource!</span></span> <span data-ttu-id="ca9ca-117">Kun olet lähettänyt ideasi, aloitamme vuoropuhelun kanssasi ja saat käyttöösi kaiken, mitä tarvitset sovelluksen työstämisen aloittamiseen.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-117">After submitting your idea, we will engage with you and provide you with everything you need to start working on your app.</span></span>
<span data-ttu-id="ca9ca-118">Lisätietoja näistä vaiheista on Download Centerin [Sovellusideaa koskeva keskustelu.pdf](https://go.microsoft.com/fwlink/?linkid=841515) -tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-118">For more information about all the steps, get the [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) document from the Download Center.</span></span>

+ <span data-ttu-id="ca9ca-119">Sovelluksen teknisten ominaisuuksien kehittäminen</span><span class="sxs-lookup"><span data-stu-id="ca9ca-119">Develop the technical aspects of your app</span></span>    
<span data-ttu-id="ca9ca-120">Voit kehittää sovellusta sen jälkeen, kun olet määrittänyt oman sovelluskehitysympäristösi.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-120">After you have set up your own app development environment, you can develop your app.</span></span>
<span data-ttu-id="ca9ca-121">Lisätietoja kaikesta siitä, mitä tarvitset [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen teknisten ominaisuuksien kehittämiseen, on Download Centerin [Sovelluksen teknisten ominaisuuksien kehittäminen.pdf](https://go.microsoft.com/fwlink/?linkid=841516) -tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-121">For more information about everything you need to know about how to develop the technical aspects of your [!INCLUDE[d365fin](includes/d365fin_md.md)] app, get the [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) document from the Download Center.</span></span>

+ <span data-ttu-id="ca9ca-122">Sovelluksen markkinointitapojen kehittäminen</span><span class="sxs-lookup"><span data-stu-id="ca9ca-122">Develop the marketing aspects of your app</span></span>  
<span data-ttu-id="ca9ca-123">Sovelluksen ominaisuuksien ja toimintojen mainitseminen ei riitä houkuttelemaan ostajia.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-123">Simply listing your app's features and functionality will not convert prospects to buyers.</span></span> <span data-ttu-id="ca9ca-124">Lisätietoja parhaista tavoista markkinoida sovellusta AppSource-kaupassa on Download Centerin [Sovelluksen markkinointitapojen kehittäminen.pdf](https://go.microsoft.com/fwlink/?linkid=841518) -tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-124">For more information about how to best market your app in the AppSource marketplace, get the [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) from the Download Center.</span></span>

+ <span data-ttu-id="ca9ca-125">Sovelluksen julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="ca9ca-125">Publish your app</span></span>  
<span data-ttu-id="ca9ca-126">Varmistamme ennen julkaisua, että sovellus on näkyvästi esillä Microsoft AppSource -kaupassa ja omalla saapumissivullasi.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-126">Before we publish, we will collaborate with you to ensure that your app stands out on Microsoft AppSource and on your own landing page!</span></span> <span data-ttu-id="ca9ca-127">Meidän on tarkistettava sovellus, jotta voimme varmistaa, että sitä markkinoidaan hyvin, että se on luotettava ja että se on ajan tasalla.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-127">We need to validate your app to ensure it is marketed well, trustworthy, and up to date.</span></span>
<span data-ttu-id="ca9ca-128">Lisätietoja tarkistusprosessista ja sovelluksen julkaisemista on Download Centerin [Sovelluksen julkaisu.pdf](https://go.microsoft.com/fwlink/?linkid=841517) -tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-128">For more information about the validation process and how to publish your app, get the [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) document from the Download Center.</span></span>

## <a name="learn-more-about-extensions-v20"></a><span data-ttu-id="ca9ca-129">Lisätietoja laajennusversiosta 2.0</span><span class="sxs-lookup"><span data-stu-id="ca9ca-129">Learn more about extensions v2.0</span></span>
<span data-ttu-id="ca9ca-130">Laajennusversion 2.0 muodostamisen mahdollistavat uudet kehitystyökalut ovat tällä hetkellä saatavana esiversiona, ja ne otetaan käyttöön pian Finance and Operations, Business edition -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-130">The new development tools, which enable to you to build extensions v2.0, are currently in preview and will be enabled in the Finance and Operations, Business edition  service soon.</span></span> <span data-ttu-id="ca9ca-131">Voit halutessasi tutustua uusiin työkaluihin tai katsoa lisätietoja laajennusversiosta 2.0 osoitteessa [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span><span class="sxs-lookup"><span data-stu-id="ca9ca-131">If you already want to familiarize yourself with the new tools or learn more about extensions 2.0, have a look at [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span></span>  

## <a name="need-help"></a><span data-ttu-id="ca9ca-132">Tarvitsetko apua?</span><span class="sxs-lookup"><span data-stu-id="ca9ca-132">Need help?</span></span>
<span data-ttu-id="ca9ca-133">Jos haluat yksityiskohtaisempaa opastusta, voit ottaa yhteyttä seuraavassa luettelossa olevaan sovelluksen aihealueen asiantuntijaan:</span><span class="sxs-lookup"><span data-stu-id="ca9ca-133">If you would like some coaching, you can contact an app subject matter expert from the following list:</span></span>

* <span data-ttu-id="ca9ca-134">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span><span class="sxs-lookup"><span data-stu-id="ca9ca-134">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span></span>  
* <span data-ttu-id="ca9ca-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span><span class="sxs-lookup"><span data-stu-id="ca9ca-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span></span>

<span data-ttu-id="ca9ca-136">Tässä luettelossa olevat kumppanit</span><span class="sxs-lookup"><span data-stu-id="ca9ca-136">Partners in this list:</span></span>

* <span data-ttu-id="ca9ca-137">on lueteltu aakkosjärjestyksessä</span><span class="sxs-lookup"><span data-stu-id="ca9ca-137">Are listed alphabetically</span></span>  
* <span data-ttu-id="ca9ca-138">avustavat tai ovat avustaneet vähintään kolmea kumppania tuomaan sovelluksia Microsoft AppSourceen</span><span class="sxs-lookup"><span data-stu-id="ca9ca-138">Are assisting or have assisted a minimum of three partners with bringing apps into Microsoft AppSource</span></span>  
* <span data-ttu-id="ca9ca-139">tarjoavat sovellusohjausta pakettipalveluina (ja ne on mainittu sivustossa).</span><span class="sxs-lookup"><span data-stu-id="ca9ca-139">Have a packaged service available (and listed on their website) about the app guidance that they provide</span></span>  

<span data-ttu-id="ca9ca-140">Jos sovellut mielestäsi sovelluspalvelukumppaniksi, ota yhteys osoitteeseen [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ca9ca-140">If you believe you should be listed as an app service partner, don't hesitate to reach out to [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="questions"></a><span data-ttu-id="ca9ca-141">Kysyttävää?</span><span class="sxs-lookup"><span data-stu-id="ca9ca-141">Questions?</span></span>
<span data-ttu-id="ca9ca-142">[Usein kysytyissä kysymyksissä](https://go.microsoft.com/fwlink/?linkid=841520) on vastauksia yleisiin [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -sovelluksia koskeviin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="ca9ca-142">This [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) responds to the most common questions you might have about apps for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ca9ca-143">Jos sinulla on lisää kysyttävää, ota yhteys paikalliseen Microsoftin edustajaan tai lähetä sähköpostia osoitteeseen [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ca9ca-143">If you have further questions, don't hesitate to contact your local Microsoft representative or email [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="further-resources"></a><span data-ttu-id="ca9ca-144">Muita resursseja</span><span class="sxs-lookup"><span data-stu-id="ca9ca-144">Further Resources</span></span>
<span data-ttu-id="ca9ca-145">Sovelluskehitystä koskevia lisäresursseja on DLP-aihesivulla [DLP-aihesivu](https://mbspartner.microsoft.com/BFI/Topic/76).</span><span class="sxs-lookup"><span data-stu-id="ca9ca-145">Please find further resources for app development on our [DLP topic page](https://mbspartner.microsoft.com/BFI/Topic/76) DLP topic page.</span></span> <span data-ttu-id="ca9ca-146">Seuraavassa on valittu muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="ca9ca-146">Some selected ones are available below:</span></span>
-   [<span data-ttu-id="ca9ca-147">Käyttäjän rekisteröinti ja sitä seuraava laskutus </span><span class="sxs-lookup"><span data-stu-id="ca9ca-147">User Registration and Subsequent Billing </span></span>](http://download.microsoft.com/download/3/2/0/320D0286-8810-4A8F-B7DD-523ED87D441B/FAQ on apps for Dynamics 365 for Financials.pdf)



## <a name="see-also"></a><span data-ttu-id="ca9ca-148">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ca9ca-148">See Also</span></span>
<span data-ttu-id="ca9ca-149">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="ca9ca-149">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="ca9ca-150">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="ca9ca-150">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[https://appsource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

