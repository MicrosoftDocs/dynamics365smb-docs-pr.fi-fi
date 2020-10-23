---
title: Microsoft Teamsin Business Centralin integroinnin hallinta | Microsoft Docs
description: Microsoft Teamsin ja Business Centralin integroinnin hallinta.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989356"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a><span data-ttu-id="ca5ce-103">Microsoft Teamsin ja Business Centralin integroinnin hallinta</span><span class="sxs-lookup"><span data-stu-id="ca5ce-103">Managing Microsoft Teams Integration with Business Central</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="ca5ce-104">Tässä artikkelissa on yleiskuvaus siitä, mitä voit tehdä järjestelmänvalvojana, kun haluat hallita Microsoft Teamsin ja [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelman integrointia.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-104">This article provides an overview of what you can do as an administrator to control Microsoft Teams integration with [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

## <a name="in-microsoft-teams"></a><span data-ttu-id="ca5ce-105">Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="ca5ce-105">In Microsoft Teams</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="ca5ce-106">Vähimmäisvaatimukset</span><span class="sxs-lookup"><span data-stu-id="ca5ce-106">Minimum requirements</span></span>

<span data-ttu-id="ca5ce-107">Tässä osassa kuvataan vähimmäisvaatimukset, jotka koskevat [!INCLUDE [prodshort](includes/prodshort.md)] -sovellusominaisuuksia Teams-työskentelyssä.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-107">This section describes the minimum requirements for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

- <span data-ttu-id="ca5ce-108">Pakolliset lisenssit</span><span class="sxs-lookup"><span data-stu-id="ca5ce-108">Required licenses</span></span>

    <span data-ttu-id="ca5ce-109">Tämä taulukko sisältää yleiskuvauksen käyttöoikeuksista, joita tarvitaan [!INCLUDE [prodshort](includes/prodshort.md)] -sovellusominaisuuksien Teams-työskentelyssä.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-109">This table gives you an overview of the licenses needed for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

    |<span data-ttu-id="ca5ce-110">Mikä</span><span class="sxs-lookup"><span data-stu-id="ca5ce-110">What</span></span>|<span data-ttu-id="ca5ce-111">Teams-lisenssi</span><span class="sxs-lookup"><span data-stu-id="ca5ce-111">Teams license</span></span>|<span data-ttu-id="ca5ce-112">Business Central -lisenssi</span><span class="sxs-lookup"><span data-stu-id="ca5ce-112">Business Central license</span></span>|
    |----|---|---|
    |<span data-ttu-id="ca5ce-113">Liitä linkki [!INCLUDE [prodshort](includes/prodshort.md)] -tietueeseen keskusteluun ja lähetä se korttina.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-113">Paste a link to a [!INCLUDE [prodshort](includes/prodshort.md)] record into a conversation, and send it as a card.</span></span>|<span data-ttu-id="ca5ce-114">![valintamerkki](media/check.png "tarkistus")</span><span class="sxs-lookup"><span data-stu-id="ca5ce-114">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="ca5ce-115">![valintamerkki](media/check.png "tarkistus")</span><span class="sxs-lookup"><span data-stu-id="ca5ce-115">![check mark](media/check.png "check")</span></span>|
    |<span data-ttu-id="ca5ce-116">Näytä [!INCLUDE [prodshort](includes/prodshort.md)] -tietueen kortti keskustelussa.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-116">View a card of a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="ca5ce-117">![valintamerkki](media/check.png "tarkistus")</span><span class="sxs-lookup"><span data-stu-id="ca5ce-117">![check mark](media/check.png "check")</span></span>||
    |<span data-ttu-id="ca5ce-118">Näytä lisätietoja [!INCLUDE [prodshort](includes/prodshort.md)] -tietueen kortista keskustelussa.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-118">View more details of card for a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="ca5ce-119">![valintamerkki](media/check.png "tarkistus")</span><span class="sxs-lookup"><span data-stu-id="ca5ce-119">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="ca5ce-120">![valintamerkki](media/check.png "tarkistus")</span><span class="sxs-lookup"><span data-stu-id="ca5ce-120">![check mark](media/check.png "check")</span></span>|

- <span data-ttu-id="ca5ce-121">Salli URL-esikatselut</span><span class="sxs-lookup"><span data-stu-id="ca5ce-121">Allow URL previews</span></span>

    <span data-ttu-id="ca5ce-122">**Salli URL-esikatselut** -käytäntöasetuksen on oltava käytössä.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-122">**Allow URL previews** policy setting must be turned on.</span></span> <span data-ttu-id="ca5ce-123">Muussa tapauksessa Teams-keskusteluun liitetyissä Business Central -linkeissä ei voi luoda korttia.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-123">Otherwise, a card can't be generated for Business Central links pasted into a Teams conversation.</span></span> <span data-ttu-id="ca5ce-124">Lisätietoja tästä asetuksen käyttämisestä on kohdassa [Teamsin viestintäkäytäntöjen hallinta](/microsoftteams/messaging-policies-in-teams).</span><span class="sxs-lookup"><span data-stu-id="ca5ce-124">For more information about this setting, see [Manage messaging policies in Teams](/microsoftteams/messaging-policies-in-teams).</span></span>

### <a name="managing-the-business-central-app-optional"></a><span data-ttu-id="ca5ce-125">Business Central -sovelluksen hallinta (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="ca5ce-125">Managing the Business Central app (optional)</span></span>

<span data-ttu-id="ca5ce-126">Teamsin järjestelmänvalvojana voit hallita kaikkia organisaatiosi sovelluksia, myös [!INCLUDE [prodshort](includes/prodshort.md)] -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-126">As a Teams administrator, you can manage all apps for your organization, including the [!INCLUDE [prodshort](includes/prodshort.md)] app.</span></span> <span data-ttu-id="ca5ce-127">Voit hyväksyä tai asentaa [!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen organisaatiota varten, estää käyttäjän asentamasta sovellusta ja paljon muuta.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-127">You can approve or install the [!INCLUDE [prodshort](includes/prodshort.md)] app for your organization, block user's from installing the app, and more.</span></span>

<span data-ttu-id="ca5ce-128">Lisätietoja on seuraavissa Microsoft Teams -asiakirjojen artikkeleissa:</span><span class="sxs-lookup"><span data-stu-id="ca5ce-128">For more information, see the following articles in the Microsoft Teams documentation:</span></span>

- [<span data-ttu-id="ca5ce-129">Hallitse sovelluksiasi Microsoft Teams -hallintakeskuksessa</span><span class="sxs-lookup"><span data-stu-id="ca5ce-129">Manage your apps in the Microsoft Teams admin center</span></span>](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [<span data-ttu-id="ca5ce-130">Sovelluksen asetuskäytäntöjen hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="ca5ce-130">Manage app setup policies in Microsoft Teams</span></span>](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a><span data-ttu-id="ca5ce-131">[!INCLUDE [prodshort](includes/prodshort.md)]issa</span><span class="sxs-lookup"><span data-stu-id="ca5ce-131">In [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="ca5ce-132">Vähimmäisvaatimukset</span><span class="sxs-lookup"><span data-stu-id="ca5ce-132">Minimum requirements</span></span>

- <span data-ttu-id="ca5ce-133">[!INCLUDE [prodshort](includes/prodshort.md)] -versio:</span><span class="sxs-lookup"><span data-stu-id="ca5ce-133">[!INCLUDE [prodshort](includes/prodshort.md)] version:</span></span>

    <span data-ttu-id="ca5ce-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 julkaisuaalto 2 (versio 17) tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 release wave 2 (version 17) or later.</span></span> <span data-ttu-id="ca5ce-135">Teamsin integrointia tuetaan vain [!INCLUDE [prodshort](includes/prodshort.md)] online-tilassa, ei paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-135">Teams integration is only supported for [!INCLUDE [prodshort](includes/prodshort.md)] online; not on-premises.</span></span>

- <span data-ttu-id="ca5ce-136">Koodiyksikkö **2718 Sivun yhteenvedon toimittaja** on julkaistu verkkopalveluna:</span><span class="sxs-lookup"><span data-stu-id="ca5ce-136">Codeunit **2718 Page Summary Provider** is published as a web service:</span></span>

    <span data-ttu-id="ca5ce-137">Tämä koodiyksikkö julkaistaan oletusarvoisesti verkkopalveluna.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-137">This codeunit is published as a web service by default.</span></span> <span data-ttu-id="ca5ce-138">Koodiyksikkö on osa [!INCLUDE [prodshort](includes/prodshort.md)] -järjestelmäsovellusta.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-138">The codeunit is part of the [!INCLUDE [prodshort](includes/prodshort.md)] system application.</span></span> <span data-ttu-id="ca5ce-139">Sen avulla saadaan kenttätiedot [!INCLUDE [prodshort](includes/prodshort.md)] -sivulle, joka on lisätty Teams- keskusteluun.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-139">It's used to get the field data for a [!INCLUDE [prodshort](includes/prodshort.md)] page added to a Teams conversation.</span></span> 

- <span data-ttu-id="ca5ce-140">Käyttöoikeudet:</span><span class="sxs-lookup"><span data-stu-id="ca5ce-140">User permissions:</span></span>

    <span data-ttu-id="ca5ce-141">Suurin osa niistä sivuista ja tiedoista, joita käyttäjät voivat tarkastella ja muokata Teams-keskusteluissa, määräytyy niiden käyttöoikeuksien mukaan [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-141">For the most part, the pages and data that users can view and edit in a Teams conversation is controlled by their permissions in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
    
    - <span data-ttu-id="ca5ce-142">Jos haluat liittää [!INCLUDE [prodshort](includes/prodshort.md)] -linkin Teams-keskusteluun ja lisätä sen korttiin, käyttäjillä on oltava vähintään lukuoikeus sivulle ja sen tietoihin.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-142">To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, users must have at least read permission on the page and its data.</span></span>
    - <span data-ttu-id="ca5ce-143">Kun kortti on lähetetty keskusteluun, kuka tahansa kyseisessä keskustelussa oleva käyttäjä voi tarkastella korttia ilman Business Centralin käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-143">Once a card is submitted into a conversation, any user in that conversation can view that card without permission to Business Central.</span></span>
    - <span data-ttu-id="ca5ce-144">Jotta voisit katsoa lisätietoja kortista tai avata sen [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa, käyttäjillä on oltava sivun ja sen tietojen lukuoikeus.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-144">To view more details for a card or open the record in [!INCLUDE [prodshort](includes/prodshort.md)], users must have read permission on the page and its data.</span></span>
    - <span data-ttu-id="ca5ce-145">Jos haluat muuttaa tietoja, käyttäjän täytyy muokata käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="ca5ce-145">To change data, user's need modify permissions.</span></span>
    
    <span data-ttu-id="ca5ce-146">Tietoja käyttöoikeuksista on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ca5ce-146">For information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ca5ce-147">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ca5ce-147">See Also</span></span>
[<span data-ttu-id="ca5ce-148">Business Centralin ja Microsoft Teamsin integraation yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ca5ce-148">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="ca5ce-149">[Asenna [!INCLUDE [prodshort](includes/prodshort.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="ca5ce-149">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="ca5ce-150">Teamsin integroinnin kehittäminen</span><span class="sxs-lookup"><span data-stu-id="ca5ce-150">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="ca5ce-151">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="ca5ce-151">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
