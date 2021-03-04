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
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 2d86e96b1778df47f0ead9845e2585905087adae
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046478"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Microsoft Teamsin ja [!INCLUDE [prod_short](includes/prod_short.md)]in integroinnin hallinta

[!INCLUDE [online_only](includes/online_only.md)]

Tässä artikkelissa on yleiskuvaus siitä, mitä voit tehdä järjestelmänvalvojana, kun haluat hallita Microsoft Teamsin ja [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman integrointia.

## <a name="in-microsoft-teams"></a>Microsoft Teamsissa

### <a name="minimum-requirements"></a>Vähimmäisvaatimukset

Tässä osassa kuvataan vähimmäisvaatimukset, jotka koskevat [!INCLUDE [prod_short](includes/prod_short.md)] -sovellusominaisuuksia Teams-työskentelyssä.

- Pakolliset lisenssit

    Tämä taulukko sisältää yleiskuvauksen käyttöoikeuksista, joita tarvitaan [!INCLUDE [prod_short](includes/prod_short.md)] -sovellusominaisuuksien Teams-työskentelyssä.

    |Mikä|Teams-lisenssi|[!INCLUDE [prod_short](includes/prod_short.md)] -käyttöoikeus|
    |----|---|---|
    |Liitä linkki [!INCLUDE [prod_short](includes/prod_short.md)] -tietueeseen keskusteluun ja lähetä se korttina.|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")|
    |Näytä [!INCLUDE [prod_short](includes/prod_short.md)] -tietueen kortti keskustelussa.|![valintamerkki](media/check.png "tarkistus")||
    |Näytä lisätietoja [!INCLUDE [prod_short](includes/prod_short.md)] -tietueen kortista keskustelussa.|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")|

- Salli URL-esikatselut

    **Salli URL-esikatselut** -käytäntöasetuksen on oltava käytössä. Muussa tapauksessa Teams-keskusteluun liitetyissä [!INCLUDE [prod_short](includes/prod_short.md)] -linkeissä ei voi luoda korttia. Lisätietoja tästä asetuksen käyttämisestä on kohdassa [Teamsin viestintäkäytäntöjen hallinta](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen hallinta (valinnainen)

Teamsin järjestelmänvalvojana voit hallita kaikkia organisaatiosi sovelluksia, myös [!INCLUDE [prod_short](includes/prod_short.md)] -sovellusta. Voit hyväksyä tai asentaa [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen organisaatiota varten, estää käyttäjän asentamasta sovellusta ja paljon muuta.

Lisätietoja on seuraavissa Microsoft Teams -asiakirjojen artikkeleissa:

- [Hallitse sovelluksiasi Microsoft Teams -hallintakeskuksessa](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Sovelluksen asetuskäytäntöjen hallinta Microsoft Teamsissa](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>[!INCLUDE [prod_short](includes/prod_short.md)]issa

### <a name="minimum-requirements"></a>Vähimmäisvaatimukset

- [!INCLUDE [prod_short](includes/prod_short.md)] -versio:

    [!INCLUDE [prod_short](includes/prod_short.md)] 2020 2. julkaisuaalto (päivitys 17.3 tai uudempi). Teamsin integrointia tuetaan vain [!INCLUDE [prod_short](includes/prod_short.md)] online-tilassa, ei paikallisesti.

- Codeunit **2718 Sivun yhteenvedon toimittaja** on julkaistu verkkopalveluna:

    Tämä codeunit julkaistaan oletusarvoisesti verkkopalveluna. Codeunit on osa [!INCLUDE [prod_short](includes/prod_short.md)] -järjestelmäsovellusta. Sen avulla saadaan kenttätiedot [!INCLUDE [prod_short](includes/prod_short.md)] -sivulle, joka on lisätty Teams- keskusteluun. Tietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

- <a name="permissions"></a>Käyttöoikeudet:

    Suurin osa niistä sivuista ja tiedoista, joita käyttäjät voivat tarkastella ja muokata Teams-keskusteluissa, määräytyy niiden käyttöoikeuksien mukaan [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa.
    
    - Jos haluat liittää [!INCLUDE [prod_short](includes/prod_short.md)] -linkin Teams-keskusteluun ja lisätä sen korttiin, käyttäjillä on oltava vähintään lukuoikeus sivulle ja sen tietoihin.
    - Kun kortti on lähetetty keskusteluun, kuka tahansa kyseisessä keskustelussa oleva käyttäjä voi tarkastella korttia ilman [!INCLUDE [prod_short](includes/prod_short.md)]in käyttöoikeutta.
    - Jotta voisit katsoa lisätietoja kortista tai avata sen [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa, käyttäjillä on oltava sivun ja sen tietojen lukuoikeus.
    - Jos haluat muuttaa tietoja, käyttäjän täytyy muokata käyttöoikeuksia.
    
    Tietoja käyttöoikeuksista on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).

## <a name="managing-privacy-and-compliance"></a>Tietosuojan ja vaatimustenmukaisuuden hallinta 

Microsoft Teams sisältää laajoja hallintatoimintoja, jotka koskevat arkaluontoisten tai henkilökohtaisten tunnistetietojen säännöstenmukaisuutta ja hallintaa – koskien myös [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen chatteihin ja kanaviin lisättyjä tietoja.

### <a name="understanding-where-prod_short-cards-are-stored"></a>[!INCLUDE [prod_short](includes/prod_short.md)] -korttien tallennussijainnin ymmärtäminen 

Kun kortti on lähetetty chattiin, kortti ja kortissa näkyvät kentät kopioidaan Teamsiin. Nämä tiedot ovat organisaation Teams-käytäntöjen, esimerkiksi tietojensäilytyskäytäntöjen, alaisia. Kun näytetään kortin tiedot, mitään Tiedot-ikkunan tietoja ei tallenneta Teamsiin. Tiedot säilyvät tallennettuna [!INCLUDE [prod_short](includes/prod_short.md)]iin ja Teams vain noutaa ne, kun käyttäjä päättää tarkastella tietoja. 

- Lisätietoja siitä, mihin Teams tallentaa tiedot, on kohdassa [Tietojen sijainti Microsoft Teamsissa](/microsoftteams/location-of-data-in-teams).
- Lisätietoja Teamsin säilytyskäytännöistä on kohdassa [Microsoft Teamsin säilytyskäytännöt](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Korttien jakamisen rajoittaminen 

Voit estää tiettyjä käyttäjiä tai ryhmiä lähettämästä kortteja chatteihin tai kanaviin, kun määrität viestikäytäntöjä, jotka ottavat **URL-esikatselut** -asetuksen pois käytöstä. Lisätietoja tästä asetuksen käyttämisestä on kohdassa [Teamsin viestintäkäytäntöjen hallinta](/microsoftteams/messaging-policies-in-teams). 

Tietoesteiden avulla voit myös estää yksittäisiä henkilöitä tai ryhmiä viestimästä keskenään. Lisätietoja on kohdassa [Tietoesteet Microsoft Teamsissa](/microsoftteams/information-barriers-in-teams).

Microsoft 365 Security & Compliance Centerin tietojen menetyksen estämisen ominaisuuksia ei voi kohdistaa erityisesti kortteihin. Mutta niitä voidaan käyttää chat-viesteihin, jotka sisältävät kortteja. Jos haluat seurata tulevia lisätoimintoja, jotka sisältävät DLP-käytäntöjä kortteille, katso [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).

### <a name="responding-to-data-requests"></a>Tietopyyntöihin vastaaminen

Annat tiimin jäsenille ja tiimin omistajille mahdollisuuden poistaa viestejä, jotka sisältävät arkaluonteisia kortteja, määrittämällä viestikäytännöt, kuten: **Omistajat voivat poistaa lähetettyjä viestejä** ja **Käyttäjät voivat poistaa lähetettyjä viestejä**. Lisätietoja: [Teamsin viestintäkäytäntöjen hallinta](/microsoftteams/messaging-policies-in-teams).

Microsoft 365 Security & Compliance Centerin sisältöhaun ja eDiscoveryn vaatimustenmukaisuuden ominaisuuksia ei voi kohdistaa erityisesti kortteihin. Mutta niitä voidaan käyttää chat-viesteihin, jotka sisältävät kortteja. Jos haluat seurata korttien tulevia yhteensopivuusominaisuuksia, katso [https://www.microsoft.com/microsoft-365/roadmap?featureid=68875](https://www.microsoft.com/microsoft-365/roadmap?featureid=68875).

Koska Teamsin korttien tiedot ovat kopio [!INCLUDE [prod_short](includes/prod_short.md)]in tiedoista, voit myös käyttää [!INCLUDE [prod_short](includes/prod_short.md)] -ominaisuuksia asiakkaan tietojen viemiseen pyydettäessä. Lisä tietoja tietosuojasta on [!INCLUDE [prod_short](includes/prod_short.md)][Business Central-asiakkaiden tietosuojan usein kysytyissä kysymyksissä](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Katso myös
[[!INCLUDE [prod_short](includes/prod_short.md)]in ja Microsoft Teamsin integroinnin yleiskatsaus](across-teams-overview.md)  
[Asenna [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)  
[Teams – usein kysytyt kysymykset](teams-faq.md)  
[Vianetsintä – Teams](admin-teams-troubleshooting.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]