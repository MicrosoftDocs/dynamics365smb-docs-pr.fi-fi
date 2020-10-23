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
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Microsoft Teamsin ja Business Centralin integroinnin hallinta

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Tässä artikkelissa on yleiskuvaus siitä, mitä voit tehdä järjestelmänvalvojana, kun haluat hallita Microsoft Teamsin ja [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelman integrointia.

## <a name="in-microsoft-teams"></a>Microsoft Teamsissa

### <a name="minimum-requirements"></a>Vähimmäisvaatimukset

Tässä osassa kuvataan vähimmäisvaatimukset, jotka koskevat [!INCLUDE [prodshort](includes/prodshort.md)] -sovellusominaisuuksia Teams-työskentelyssä.

- Pakolliset lisenssit

    Tämä taulukko sisältää yleiskuvauksen käyttöoikeuksista, joita tarvitaan [!INCLUDE [prodshort](includes/prodshort.md)] -sovellusominaisuuksien Teams-työskentelyssä.

    |Mikä|Teams-lisenssi|Business Central -lisenssi|
    |----|---|---|
    |Liitä linkki [!INCLUDE [prodshort](includes/prodshort.md)] -tietueeseen keskusteluun ja lähetä se korttina.|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")|
    |Näytä [!INCLUDE [prodshort](includes/prodshort.md)] -tietueen kortti keskustelussa.|![valintamerkki](media/check.png "tarkistus")||
    |Näytä lisätietoja [!INCLUDE [prodshort](includes/prodshort.md)] -tietueen kortista keskustelussa.|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")|

- Salli URL-esikatselut

    **Salli URL-esikatselut** -käytäntöasetuksen on oltava käytössä. Muussa tapauksessa Teams-keskusteluun liitetyissä Business Central -linkeissä ei voi luoda korttia. Lisätietoja tästä asetuksen käyttämisestä on kohdassa [Teamsin viestintäkäytäntöjen hallinta](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Business Central -sovelluksen hallinta (valinnainen)

Teamsin järjestelmänvalvojana voit hallita kaikkia organisaatiosi sovelluksia, myös [!INCLUDE [prodshort](includes/prodshort.md)] -sovellusta. Voit hyväksyä tai asentaa [!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen organisaatiota varten, estää käyttäjän asentamasta sovellusta ja paljon muuta.

Lisätietoja on seuraavissa Microsoft Teams -asiakirjojen artikkeleissa:

- [Hallitse sovelluksiasi Microsoft Teams -hallintakeskuksessa](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Sovelluksen asetuskäytäntöjen hallinta Microsoft Teamsissa](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>[!INCLUDE [prodshort](includes/prodshort.md)]issa

### <a name="minimum-requirements"></a>Vähimmäisvaatimukset

- [!INCLUDE [prodshort](includes/prodshort.md)] -versio:

    [!INCLUDE [prodshort](includes/prodshort.md)] 2020 julkaisuaalto 2 (versio 17) tai uudempi. Teamsin integrointia tuetaan vain [!INCLUDE [prodshort](includes/prodshort.md)] online-tilassa, ei paikallisesti.

- Koodiyksikkö **2718 Sivun yhteenvedon toimittaja** on julkaistu verkkopalveluna:

    Tämä koodiyksikkö julkaistaan oletusarvoisesti verkkopalveluna. Koodiyksikkö on osa [!INCLUDE [prodshort](includes/prodshort.md)] -järjestelmäsovellusta. Sen avulla saadaan kenttätiedot [!INCLUDE [prodshort](includes/prodshort.md)] -sivulle, joka on lisätty Teams- keskusteluun. 

- Käyttöoikeudet:

    Suurin osa niistä sivuista ja tiedoista, joita käyttäjät voivat tarkastella ja muokata Teams-keskusteluissa, määräytyy niiden käyttöoikeuksien mukaan [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa.
    
    - Jos haluat liittää [!INCLUDE [prodshort](includes/prodshort.md)] -linkin Teams-keskusteluun ja lisätä sen korttiin, käyttäjillä on oltava vähintään lukuoikeus sivulle ja sen tietoihin.
    - Kun kortti on lähetetty keskusteluun, kuka tahansa kyseisessä keskustelussa oleva käyttäjä voi tarkastella korttia ilman Business Centralin käyttöoikeutta.
    - Jotta voisit katsoa lisätietoja kortista tai avata sen [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa, käyttäjillä on oltava sivun ja sen tietojen lukuoikeus.
    - Jos haluat muuttaa tietoja, käyttäjän täytyy muokata käyttöoikeuksia.
    
    Tietoja käyttöoikeuksista on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).

## <a name="see-also"></a>Katso myös
[Business Centralin ja Microsoft Teamsin integraation yleiskatsaus](across-teams-overview.md)  
[Asenna [!INCLUDE [prodshort](includes/prodshort.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Käytön aloittaminen](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
