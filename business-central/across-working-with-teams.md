---
title: Business Central -tietojen käyttäminen Microsoft Teamsissa | Microsoft Docs
description: Microsoft Teamsin Business Central -sovelluksen käyttäminen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 0f7c1e8016a1bc1915d7d6a54a183aa0e8cea2ea
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046452"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="2dcf4-103">Business Centralin tietojen käyttäminen Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="2dcf4-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="2dcf4-104">[!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa sovelluksen, joka yhdistää Microsoft Teamsin yrityksen tietoihin [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa, joten voit jakaa tiedot nopeasti tiimin jäsenten kesken ja reagoida nopeammin kyselyihin.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="2dcf4-105">Tässä artikkelissa kerrotaan, miten sovellusta käytetään [!INCLUDE [prod_short](includes/prod_short.md)] -tietojen jakamiseen työtovereiden kanssa Teams-keskusteluissa.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="2dcf4-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="2dcf4-106">Overview</span></span>

<span data-ttu-id="2dcf4-107">[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen avulla voit:</span><span class="sxs-lookup"><span data-stu-id="2dcf4-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="2dcf4-108">Kopioida linkin mihin tahansa Business Central -tietueeseen ja liittää sen Teams-keskusteluun, jonka haluat jakaa työtovereidesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="2dcf4-109">Sovellus laajentaa linkin kompaktiksi ja vuorovaikutteiseksi kortiksi, joka näyttää tietoja tietueesta.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="2dcf4-110">Keskustelun aikana sinä ja työtoverisi voitte tarkastella lisätietoja tietueesta, muokata tietoja ja toimia – poistumatta Teamsista.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="2dcf4-111">[![Teamsin ja Business Centralin integrointi](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="2dcf4-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2dcf4-112">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="2dcf4-112">Prerequisites</span></span>

- <span data-ttu-id="2dcf4-113">Sinulla on Microsoft Teamsin käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="2dcf4-114">Olet asentanut [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="2dcf4-115">Lisätietoja, katso [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsiin](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="2dcf4-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="2dcf4-116">Kaikki Teams-keskustelun osallistujat voivat tarkastella keskusteluun lähetettäviä Business Central -tietueiden kortteja.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="2dcf4-117">Mutta halutessaan tarkastella lisätietoja tietueista käyttämällä **Tiedot**- tai **Ponnahdusikkuna**-painikkeita, he tarvitsevat käyttöoikeuden [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2dcf4-118">Lisätietoja on kohdassa [Microsoft Teams -integraation hallinta](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="2dcf4-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="2dcf4-119">Sisällytä Business Central -kortti Teams-keskusteluun</span><span class="sxs-lookup"><span data-stu-id="2dcf4-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="2dcf4-120">Kirjaudu [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan käyttämällä selainta.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="2dcf4-121">Avaa tietue, jonka haluat jakaa.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="2dcf4-122">Sovellus on suunniteltu näyttämään korttityyppisivut [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmasta.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2dcf4-123">Avaa siis sivu, jossa näkyy yksittäinen tietue, esimerkiksi nimike, asiakas tai myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="2dcf4-124">Sitä ei voi käyttää roolikeskuksissa tai sivuissa, jotka näyttävät useita tietueita luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="2dcf4-125">Kopioi koko URL-osoite selaimen osoiteriviltä.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Business Centralin URL-osoitteen kopioiminen selaimesta](media/teams-url-v2.png)
4. <span data-ttu-id="2dcf4-127">Siirry Teamsiin ja aloita keskustelu, joka voi olla keskustelu henkilön, henkilöryhmän tai tiimikanavan kanssa.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="2dcf4-128">Liitä URL-osoite viestiruutuun, johon kirjoitat viestin.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Liitä Business Central-URL-osoite Teamsiin](media/teams-paste-url-v2.png)
6. <span data-ttu-id="2dcf4-130">Kun liität linkin keskusteluun ensimmäistä kertaa, sinua pyydetään kirjautumaan sisään [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan ja antamaan suostumus siihen, että sovellus hakee tiedot.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="2dcf4-131">Seuraa vain näytön ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2dcf4-132">Tämä vaihe tarvitsee tehdä vain kerran.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="2dcf4-133">Odota hetki, kun kortti luodaan sanomaruutuun.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="2dcf4-134">Kun kortti tulee näkyviin, tarkista kortin sisältö huolellisesti, ennen kuin lähetät viestin.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="2dcf4-135">Tämä vaihe on tärkeä, koska kun lähetät viestin, kaikki keskusteluun osallistuvat voivat nähdä kortin.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="2dcf4-136">Jos kortti näyttää hyvältä, lähetä se keskusteluun valitsemalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="2dcf4-137">Kun kortti tulee näyttöön ja ennen kuin valitset **Lähetä**, voit halutessasi poistaa liitetyn URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="2dcf4-138">Jos haluat tarkastella lisätietoja tai tehdä kortissa näytettyyn tietueeseen muutoksia, valitse **Tiedot**.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="2dcf4-139">Lisätietoja on seuraavassa osassa.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="2dcf4-140">Näytä kortin tiedot</span><span class="sxs-lookup"><span data-stu-id="2dcf4-140">View card details</span></span>

<span data-ttu-id="2dcf4-141">Kun kortti on lähetetty keskusteluun, kaikki osallistujat, joilla on [asianmukaiset käyttöoikeudet](admin-teams-integration.md#permissions), voivat valita **Tiedot** ja avata ikkunan, jossa näkyy lisätietoja tietueesta – ja mahdollisesti tehdä muutoksia tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="2dcf4-142">Ei ole merkitystä, oletko kortin lähettäjä vai vastaanottaja.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="2dcf4-143">**Tiedot**-ominaisuudesta on hyötyä erityisesti vastaanottajille, koska se antaa heille nopeasti ytimekkäitä ja kohdennettuja tietoja tietueesta tarvitsematta tutkia koko tietuetta.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="2dcf4-144">Tietoikkuna on samankaltainen kuin [!INCLUDE [prod_short](includes/prod_short.md)] -tietueen näkymä.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="2dcf4-145">Mutta sitä on hieman muokattu Teamsia varten.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="2dcf4-146">Kun olet lopettanut muutosten tarkastelemisen ja tekemisen, sulje ikkuna palataksesi Teams-keskusteluun.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="2dcf4-147">Seuraavassa on muutamia asioita, jotka pitää muistaa, kun käsittelet kortin tietoja:</span><span class="sxs-lookup"><span data-stu-id="2dcf4-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="2dcf4-148">Avatakseen kortin tiedot käyttäjillä on oltava sivun ja sen tietojen lukuoikeus [!INCLUDE [prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="2dcf4-149">Teams-keskustelujen kortteja ei päivitetä automaattisesti muutoksien mukaan.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="2dcf4-150">Tiedot-ikkunan tietueeseen tallentamasi muutokset tallennetaan [!INCLUDE [prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2dcf4-151">Mutta Teamsissa kortti ei näytä muutoksia keskustelussa, ennen kuin liität linkin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="2dcf4-152">Lisätietoja korttien ja korttiietojen käyttämisestä on kohdassa [Teams – usein kysytyt kysymykset](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="2dcf4-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2dcf4-153">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2dcf4-153">See Also</span></span>

[<span data-ttu-id="2dcf4-154">Business Centralin ja Microsoft Teamsin integraation yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2dcf4-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="2dcf4-155">[Asenna [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="2dcf4-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="2dcf4-156">Teams – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="2dcf4-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="2dcf4-157">Vianetsintä – Teams</span><span class="sxs-lookup"><span data-stu-id="2dcf4-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="2dcf4-158">Teamsin integroinnin kehittäminen</span><span class="sxs-lookup"><span data-stu-id="2dcf4-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
