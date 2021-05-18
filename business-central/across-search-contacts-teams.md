---
title: Yhteyshenkilöiden hakeminen Microsoft Teamsista
description: Tietoja Business Centralin asiakkaiden, toimittajien ja muiden yhteyshenkilöiden hakeminen Microsoft Teamsista.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 6d094e365ad0c7da73467e5a3160d926902c45d9
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935159"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="a799c-103">Asiakkaiden, toimittajien ja muiden yhteyshenkilöiden hakeminen Microsoft Teamsista</span><span class="sxs-lookup"><span data-stu-id="a799c-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="a799c-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="a799c-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="a799c-105">Otettiin käyttöön vuoden 2021 1. julkaisuaallossa.</span><span class="sxs-lookup"><span data-stu-id="a799c-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="a799c-106">[!INCLUDE [prod_short](includes/prod_short.md)]issa on kattava liiketoiminnan yhteyshenkilöiden hallintajärjestelmä, joka on välttämätön myynnin, toimintojen tai muiden osastoroolien käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="a799c-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="a799c-107">Jos käyttäjällä on jokin näistä rooleista, hänen on usein haettava tai tavattava toimittajia, asiakkaita ja muita yhteyshenkilöitä tai aloitettava keskustelu heidän kanssaan.</span><span class="sxs-lookup"><span data-stu-id="a799c-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="a799c-108">Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksessa nämä tehtävät voidaan tehdä suoraan Teamsissa ilman, että olisi siirryttävä [!INCLUDE [prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="a799c-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a799c-109">Teamsissa voi toimia seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="a799c-109">From within Teams, you can:</span></span>

- <span data-ttu-id="a799c-110">[!INCLUDE [prod_short](includes/prod_short.md)] -yhteyshenkilöiden hakeminen Teams-komentoruudussa tai viestiruudussa.</span><span class="sxs-lookup"><span data-stu-id="a799c-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="a799c-111">Yhteyshenkilöt voivat sisältää prospekteja, toimittajia, asiakkaita tai muita liikesuhteita.</span><span class="sxs-lookup"><span data-stu-id="a799c-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="a799c-112">Yhteyshenkilön jakaminen korttina Teams-keskustelussa.</span><span class="sxs-lookup"><span data-stu-id="a799c-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="a799c-113">Näytä yhteyshenkilötiedot, vuorovaikutushistoria ja muut merkitykselliset tiedot, kuten avoimet maksut tai asiakirjat.</span><span class="sxs-lookup"><span data-stu-id="a799c-113">View details about the contact, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a799c-114">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="a799c-114">Prerequisites</span></span>

- <span data-ttu-id="a799c-115">Sinulla on Microsoft Teamsin käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="a799c-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="a799c-116">Olet asentanut [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="a799c-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="a799c-117">Lisätietoja, katso [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsiin](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="a799c-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="a799c-118">Käytössä on [!INCLUDE [prod_short](includes/prod_short.md)] -tili, jolla voi käyttää ainakin yhden yrityksen yhteyshenkilöitä.</span><span class="sxs-lookup"><span data-stu-id="a799c-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="a799c-119">Riippumatta siitä, tehdäänkö haku komento- vai viestiruudussa, sinua voidaan pyytää ensimmäisellä kerralla kirjautumaan sisään tai määrittämään sovellus.</span><span class="sxs-lookup"><span data-stu-id="a799c-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="a799c-120">Tämä vaihe on välttämätön, jotta yhteyshenkilöitä voidaan hakea oikeasta Business Central -yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="a799c-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="a799c-121">Lisätietoja sovelluksen määrittämisestä valitsemaan yritys on kohdassa [Yrityksen ja muiden asetusten muuttaminen Teamsissa](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a799c-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="a799c-122">Yhteyshenkilöiden haku komentoruudussa</span><span class="sxs-lookup"><span data-stu-id="a799c-122">Look up contacts from the command box</span></span>

<span data-ttu-id="a799c-123">Komentoruutu on jokaisen Teamsin näytön yläosassa.</span><span class="sxs-lookup"><span data-stu-id="a799c-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="a799c-124">Sen avulla voi hakea, tehdä pikatoimintoja tai käynnistää sovelluksia, kuten [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="a799c-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="a799c-125">Komentoruutuhaku sopii hyvin yhteyshenkilöiden ja niihin liittyvien tietojen hakemiseen nopeasti omaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a799c-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="a799c-126">Oletetaan esimerkiksi, että haluat hakea toimittajan sähköpostiosoitteen kalenteritapaamisen määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="a799c-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="a799c-127">Tai ehkä haluat hakea vuorovaikutushistorian asiakastapaamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="a799c-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="a799c-128">Kirjoita komentoruutuun **@Business Central** ja valitse sitten tuloksissa Business Central -sovellus.</span><span class="sxs-lookup"><span data-stu-id="a799c-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Yhteyshenkilöiden hakeminen komentoruudussa avaamalla Business Central -sovellus](media/teams-contacts-command-1.png)

2. <span data-ttu-id="a799c-130">Aloita tekstin, kuten nimen, osoitteen tai puhelinnumeron, kirjoittaminen **Business Central** -ruutuun.</span><span class="sxs-lookup"><span data-stu-id="a799c-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="a799c-131">Hakua vastaavia tuloksia näytetään hakusanaa kirjoitettaessa.</span><span class="sxs-lookup"><span data-stu-id="a799c-131">As you type, matching results will appear.</span></span>

    ![Business Central -yhteyshenkilöiden haku Teamsin komentoruudussa](media/teams-contacts-command-2.png)
3. <span data-ttu-id="a799c-133">Valitse yhteyshenkilö tuloksista.</span><span class="sxs-lookup"><span data-stu-id="a799c-133">Select a contact from the results.</span></span>

    <span data-ttu-id="a799c-134">Yhteyshenkilökortti avautuu komentoruudun alapuolella.</span><span class="sxs-lookup"><span data-stu-id="a799c-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="a799c-135">Jos haluat lisätä yhteyshenkilökortin keskusteluun, siirry valitse kortin oikeassa yläkulmassa **... (Lisää vaihtoehtoja)** > **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="a799c-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="a799c-136">Liitä sitten kopio keskustelun viestiruutuun.</span><span class="sxs-lookup"><span data-stu-id="a799c-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="a799c-137">Lisätietoja Teamsin komentoruudusta on kohdassa [Teams – komentoruudun käyttö](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="a799c-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="a799c-138">Yhteyshenkilöiden haku viestiruudussa</span><span class="sxs-lookup"><span data-stu-id="a799c-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="a799c-139">Viestiruudun käytön etuna on se, että yhteyshenkilökortti voidaan lisätä suoraan keskusteluun muiden nähtäväksi.</span><span class="sxs-lookup"><span data-stu-id="a799c-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="a799c-140">Käynnistä sovellus valitsemalla viestiruudun alapuolella **Business Central** -kuvake.</span><span class="sxs-lookup"><span data-stu-id="a799c-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="a799c-141">Jos **Business Central** -kuvake ei ole näkyvissä, valitse **... (Viestilaajennukset)**.</span><span class="sxs-lookup"><span data-stu-id="a799c-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Yhteyshenkilöiden hakeminen viestiruudussa avaamalla Business Central -sovellus](media/teams-contacts-message-box.png)

2. <span data-ttu-id="a799c-143">Aloita tekstin, kuten nimen, osoitteen tai puhelinnumeron, kirjoittaminen **Business Central** -ruutuun.</span><span class="sxs-lookup"><span data-stu-id="a799c-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="a799c-144">Hakua vastaavia tuloksia näytetään hakusanaa kirjoitettaessa.</span><span class="sxs-lookup"><span data-stu-id="a799c-144">As you type, matching results will appear.</span></span>

    ![Business Central -yhteyshenkilöiden hakeminen viestiruudussa](media/teams-contacts-5.png)
3. <span data-ttu-id="a799c-146">Valitse yhteyshenkilö tuloksista.</span><span class="sxs-lookup"><span data-stu-id="a799c-146">Select a contact from the results.</span></span>

    <span data-ttu-id="a799c-147">Yhteishenkilökortti avautuu viestiruudussa.</span><span class="sxs-lookup"><span data-stu-id="a799c-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a799c-148">Yhteyshenkilöruutua ei lähetetä heti keskusteluun muiden nähtäväksi.</span><span class="sxs-lookup"><span data-stu-id="a799c-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="a799c-149">Voit tarkastella kortin sisältöä sekä lisätä tekstiä ennen tarkastelua tai sen jälkeen tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="a799c-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="a799c-150">Kun olet valmis, voit lähettää viestin keskusteluun.</span><span class="sxs-lookup"><span data-stu-id="a799c-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="a799c-151">Vaihtoehtoinen tapa</span><span class="sxs-lookup"><span data-stu-id="a799c-151">Here's another way</span></span>

1. <span data-ttu-id="a799c-152">**Business Central** -kuvakkeen käytön sijaan voit kirjoittaa **@Business Central** suoraan viestiruutuun.</span><span class="sxs-lookup"><span data-stu-id="a799c-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="a799c-153">Kirjoita hakusanat ruutuun.</span><span class="sxs-lookup"><span data-stu-id="a799c-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="a799c-154">Valitse yhteyshenkilö näppäimistön ylä- ja alanuolella ja valitse se sitten Enter-näppäimellä.</span><span class="sxs-lookup"><span data-stu-id="a799c-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="a799c-155">Yhteyshenkilökortin tietojen näyttäminen</span><span class="sxs-lookup"><span data-stu-id="a799c-155">Viewing contact card details</span></span>

<span data-ttu-id="a799c-156">Teamsin yhteyshenkilökortista saa nopeasti yleiskuvan asiakkaasta, toimittajasta tai yhteyshenkilöstä.</span><span class="sxs-lookup"><span data-stu-id="a799c-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="a799c-157">Kortti on vuorovaikutteinen, joten saat tarkasteltavaksi lisää tietoja tai voit muokata yhteyshenkilöä **Tiedot**- tai **Ponnahdusruutu**-painikkeilla.</span><span class="sxs-lookup"><span data-stu-id="a799c-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="a799c-158">**Tiedot**-painike avaa Teamsissa ikkunassa, jossa on lisätietoja yhteyshenkilöstä, joskin [!INCLUDE [prod_short](includes/prod_short.md)]issa on näitä tietoja enemmän.</span><span class="sxs-lookup"><span data-stu-id="a799c-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a799c-159">Jos haluat nähdä kaikki [!INCLUDE [prod_short](includes/prod_short.md)] -yhteyshenkilön tiedot, valitse **Ponnahdusikkuna**.</span><span class="sxs-lookup"><span data-stu-id="a799c-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="a799c-160">Yhteyshenkilökortti toimii samoin kuin tietueiden, kuten nimikkeiden, asiakkaiden tai myyntitilausten, kortit.</span><span class="sxs-lookup"><span data-stu-id="a799c-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="a799c-161">Lisätietoja korteista on kohdassa [Kortin tietojen näyttäminen](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="a799c-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="a799c-162">Kaikki Teams-keskustelun osallistujat voivat tarkastella keskusteluun lähetettäviä Business Central -yhteyshenkilöiden kortteja.</span><span class="sxs-lookup"><span data-stu-id="a799c-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="a799c-163">Mutta halutessaan tarkastella lisätietoja tietueista käyttämällä **Tiedot**- tai **Ponnahdusikkuna**-painikkeita, he tarvitsevat käyttöoikeuden [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="a799c-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a799c-164">Lisätietoja on kohdassa [Microsoft Teams -integraation hallinta](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="a799c-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="a799c-165">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a799c-165">See Also</span></span>

[<span data-ttu-id="a799c-166">Business Centralin ja Microsoft Teamsin integraation yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a799c-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="a799c-167">[Asenna [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="a799c-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="a799c-168">Teams – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="a799c-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="a799c-169">Vianetsintä – Teams</span><span class="sxs-lookup"><span data-stu-id="a799c-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="a799c-170">Teamsin integroinnin kehittäminen</span><span class="sxs-lookup"><span data-stu-id="a799c-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]