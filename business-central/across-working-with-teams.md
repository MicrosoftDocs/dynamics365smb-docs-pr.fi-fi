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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989416"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="d063b-103">Business Centralin tietojen käyttäminen Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="d063b-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="d063b-104">[!INCLUDE [prodshort](includes/prodshort.md)] tarjoaa sovelluksen, joka yhdistää Microsoft Teamsin yrityksen tietoihin [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa, joten voit jakaa tiedot nopeasti tiimin jäsenten kesken ja reagoida nopeammin kyselyihin.</span><span class="sxs-lookup"><span data-stu-id="d063b-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="d063b-105">Tässä artikkelissa kerrotaan, miten sovellusta käytetään [!INCLUDE [prodshort](includes/prodshort.md)] -tietojen jakamiseen työtovereiden kanssa Teams-keskusteluissa.</span><span class="sxs-lookup"><span data-stu-id="d063b-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="d063b-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d063b-106">Overview</span></span>

<span data-ttu-id="d063b-107">[!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen avulla voit:</span><span class="sxs-lookup"><span data-stu-id="d063b-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="d063b-108">Kopioida linkin mihin tahansa Business Central -tietueeseen ja liittää sen Tems-keskusteluun, jonka haluat jakaa työtovereidesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="d063b-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="d063b-109">Linkki laajentaa sen kompaktiksi ja vuorovaikutteiseksi kortiksi, joka näyttää tietoja tietueesta.</span><span class="sxs-lookup"><span data-stu-id="d063b-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="d063b-110">Keskustelun aikana sinä ja työtoverisi voitte tarkastella lisätietoja tietueesta, muokata tietoja ja toimia - poistumatta Teamsista.</span><span class="sxs-lookup"><span data-stu-id="d063b-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="d063b-111">[![Teamsin ja Business Centralin integrointi](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="d063b-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d063b-112">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="d063b-112">Prerequisites</span></span>

- <span data-ttu-id="d063b-113">Sinulla on Microsoft Teamsin käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="d063b-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="d063b-114">Olet asentanut [!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="d063b-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="d063b-115">Lisätietoja, katso [[!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen asentaminen Microsoft Teamsiin](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="d063b-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="d063b-116">Kaikki Teams-keskustelun osallistujat voivat tarkastella keskusteluun lähetettäviä Business Central -tietueiden kortteja.</span><span class="sxs-lookup"><span data-stu-id="d063b-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="d063b-117">Mutta halutessaan tarkastella lisätietoja tietueista käyttämällä **Tiedot**- tai **Ponnahdusikkuna**-painikkeita, he tarvitsevat käyttöoikeuden [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="d063b-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="d063b-118">Lisätietoja on kohdassa [Microsoft Teams -integraation hallinta](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="d063b-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="d063b-119">Sisällytä Business Central -kortti Teams-keskusteluun</span><span class="sxs-lookup"><span data-stu-id="d063b-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="d063b-120">Kirjaudu [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmaan käyttämällä selainta.</span><span class="sxs-lookup"><span data-stu-id="d063b-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="d063b-121">Avaa tietue, jonka haluat jakaa.</span><span class="sxs-lookup"><span data-stu-id="d063b-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="d063b-122">Sovellus on suunniteltu näyttämään korttityyppisivut [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmasta.</span><span class="sxs-lookup"><span data-stu-id="d063b-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="d063b-123">Avaa siis sivu, jossa näkyy yksittäinen tietue, esimerkiksi nimike, asiakas tai myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="d063b-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="d063b-124">Sitä ei voi käyttää roolikeskuksissa tai sivuissa, jotka näyttävät useita tietueita luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d063b-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="d063b-125">Kopioi koko URL-osoite selaimen osoiteriviltä.</span><span class="sxs-lookup"><span data-stu-id="d063b-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Business Centralin URL-osoitteen kopioiminen selaimesta](media/teams-url.png)
4. <span data-ttu-id="d063b-127">Siirry Teamsiin ja aloita keskustelu, joka voi olla keskustelu henkilön, henkilöryhmän tai tiimikanavan kanssa.</span><span class="sxs-lookup"><span data-stu-id="d063b-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="d063b-128">Liitä URL-osoite ruutuun, johon lisäät viestin.</span><span class="sxs-lookup"><span data-stu-id="d063b-128">Paste the URL into the box where you add a message.</span></span>

   ![Liitä Business Central-URL-osoite Teamsiin](media/teams-paste-url.png)
6. <span data-ttu-id="d063b-130">Kun liität linkin keskusteluun ensimmäistä kertaa, sinua pyydetään kirjautumaan sisään [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmaan ja antamaan suostumus siihen, että sovellus hakee tiedot.</span><span class="sxs-lookup"><span data-stu-id="d063b-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="d063b-131">Seuraa vain näytön ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d063b-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d063b-132">Tämä vaihe tarvitsee tehdä vain kerran.</span><span class="sxs-lookup"><span data-stu-id="d063b-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="d063b-133">Odota hetki, kun kortti luodaan sanomaruutuun.</span><span class="sxs-lookup"><span data-stu-id="d063b-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="d063b-134">Kun kortti tulee näkyviin, tarkista kortin sisältö huolellisesti, ennen kuin lähetät viestin.</span><span class="sxs-lookup"><span data-stu-id="d063b-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="d063b-135">Tämä vaihe on tärkeä, koska kun lähetät viestin, kaikki keskusteluun osallistuvat voivat nähdä kortin.</span><span class="sxs-lookup"><span data-stu-id="d063b-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="d063b-136">Jos kortti näyttää hyvältä, lähetä se keskusteluun valitsemalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="d063b-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="d063b-137">Kun kortti tulee näyttöön ja ennen kuin valitset **Lähetä**, voit halutessasi poistaa liitetyn URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="d063b-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="d063b-138">Jos haluat tarkastella lisätietoja tai tehdä tietueeseen muutoksia, valitse **Tiedot**.</span><span class="sxs-lookup"><span data-stu-id="d063b-138">To view more details or make changes to the record, select **Details**.</span></span>

    <span data-ttu-id="d063b-139">Tietosivu muistuttaa sitä, mitä haluat nähdä [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="d063b-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="d063b-140">Mutta sitä on hieman muokattu Teamsia varten.</span><span class="sxs-lookup"><span data-stu-id="d063b-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="d063b-141">Kun olet lopettanut muutosten tarkastelemisen ja tekemisen, sulje ikkuna palataksesi Teams-keskusteluun.</span><span class="sxs-lookup"><span data-stu-id="d063b-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d063b-142">Tekemäsi muutokset eivät näy kortissa, ennen kuin seuraavan kerran liität sen linkin keskusteluun.</span><span class="sxs-lookup"><span data-stu-id="d063b-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="d063b-143">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d063b-143">See Also</span></span>

[<span data-ttu-id="d063b-144">Business Centralin ja Microsoft Teamsin integraation yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d063b-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="d063b-145">[Asenna [!INCLUDE [prodshort](includes/prodshort.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="d063b-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="d063b-146">Teamsin integroinnin kehittäminen</span><span class="sxs-lookup"><span data-stu-id="d063b-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="d063b-147">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="d063b-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
