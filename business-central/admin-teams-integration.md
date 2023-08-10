---
title: Microsoft Teamsin Business Centralin integroinnin hallinta | Microsoft Docs
description: Microsoft Teamsin ja Business Centralin integroinnin hallinta.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics365-business-central
---

# <a name="managing-microsoft-teams-integration-with-"></a>Microsoft Teamsin ja [!INCLUDE [prod_short](includes/prod_short.md)]in integroinnin hallinta

[!INCLUDE [online_only](includes/online_only.md)]

Tässä artikkelissa on yleiskuvaus siitä, mitä voit tehdä järjestelmänvalvojana, kun haluat hallita Microsoft Teamsin ja [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman integrointia.

## <a name="in-microsoft-teams"></a>Microsoft Teamsissa

### <a name="minimum-requirements"></a>Vähimmäisvaatimukset

Tässä osassa kuvataan vähimmäisvaatimukset, jotka koskevat [!INCLUDE [prod_short](includes/prod_short.md)] -sovellusominaisuuksia Teams-työskentelyssä.

- Pakolliset lisenssit

    [!INCLUDE[prod_short](includes/prod_short.md)] -sovellus edellyttää Teams-käyttöoikeutta Microsoft 365 Business- tai -Enterprise-tilauksen kautta. Erillisiä Teams-tilauksia (kuten Microsoft Teams (maksuton) tai Microsoft Teams Essentials) ei tueta.

    Useimmat Teamsin [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen ominaisuudet edellyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -käyttöoikeuksia, kuten seuraavasta taulukosta näkyy.

    |Mikä|[!INCLUDE [prod_short](includes/prod_short.md)] -käyttöoikeus|
    |----|---|
    |Hae [!INCLUDE [prod_short](includes/prod_short.md)] yhteyshenkilöitä.|![valintamerkki](media/check.png "tarkistus")|
    |Liitä linkki [!INCLUDE [prod_short](includes/prod_short.md)] -tietueeseen keskusteluun ja lähetä se korttina.|![valintamerkki](media/check.png "tarkistus")|
    |Jaa linkki [!INCLUDE [prod_short](includes/prod_short.md)] -sivulta Teams-keskusteluun.|![valintamerkki](media/check.png "tarkistus")|
    |Näytä [!INCLUDE [prod_short](includes/prod_short.md)] -tietueen kortti keskustelussa.||
    |Näytä lisätietoja [!INCLUDE [prod_short](includes/prod_short.md)] -tietueen kortista keskustelussa.|![valintamerkki](media/check.png "tarkistus")|
    |Avaa sivulinkki [!INCLUDE [prod_short](includes/prod_short.md)]iin keskustelusta.|![valintamerkki](media/check.png "tarkistus")|

- Salli URL-esikatselut

    **Salli URL-esikatselut** -käytäntöasetuksen on oltava käytössä. Muussa tapauksessa Teams-keskusteluun liitetyissä [!INCLUDE [prod_short](includes/prod_short.md)] -linkeissä ei voi luoda korttia. Lisätietoja tästä asetuksen käyttämisestä on kohdassa [Teamsin viestintäkäytäntöjen hallinta](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the--app-optional"></a>[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen hallinta (valinnainen)

Teamsin järjestelmänvalvojana voit hallita kaikkia organisaatiosi sovelluksia, myös [!INCLUDE [prod_short](includes/prod_short.md)] -sovellusta. Voit hyväksyä tai asentaa [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen organisaatiota varten, estää käyttäjän asentamasta sovellusta ja paljon muuta.

Lisätietoja on seuraavissa Microsoft Teams -asiakirjojen artikkeleissa:

- [Sovellusten hallinta Microsoft Teams -hallintakeskuksessa](/MicrosoftTeams/manage-apps)
- [Sovelluksen määrityskäytäntöjen hallinta Microsoft Teamsissa](/microsoftteams/teams-app-setup-policies)

## <a name="in-"></a>[!INCLUDE [prod_short](includes/prod_short.md)]issa

### <a name="minimum-requirements-1"></a>Vähimmäisvaatimukset

- [!INCLUDE [prod_short](includes/prod_short.md)] -versio:

    [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen vuoden 2021 1. julkaisuaalto tai uudempi. Teamsin integrointia tuetaan vain [!INCLUDE [prod_short](includes/prod_short.md)] online-tilassa, ei paikallisesti.

- Codeunit **2718 Sivun yhteenvedon toimittaja** on julkaistu verkkopalveluna:

    Tämä codeunit julkaistaan oletusarvoisesti verkkopalveluna. Codeunit on osa [!INCLUDE [prod_short](includes/prod_short.md)] -järjestelmäsovellusta. Sen avulla saadaan kenttätiedot [!INCLUDE [prod_short](includes/prod_short.md)] -sivulle, joka on lisätty Teams- keskusteluun. Tietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

- <a name="permissions"></a>Käyttöoikeudet:

    Suurin osa niistä yhteyshenkilöhauista, sivuista ja tiedoista, joita käyttäjät voivat tarkastella ja muokata Teams-keskusteluissa, määräytyy niiden käyttöoikeuksien mukaan [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa.

    - Käyttäjät voivat hakea yhteyshenkilöitä, jos heillä on ainakin **Yhteyshenkilöt**-taulukon lukuoikeus. 
    - Jos haluat liittää [!INCLUDE [prod_short](includes/prod_short.md)] -linkin Teams-keskusteluun ja lisätä sen korttiin, käyttäjillä on oltava vähintään lukuoikeus sivulle ja sen tietoihin.
    - Kun kortti on lähetetty keskusteluun, kuka tahansa kyseisessä keskustelussa oleva käyttäjä voi tarkastella korttia ilman [!INCLUDE [prod_short](includes/prod_short.md)]in käyttöoikeutta.
    - Jotta voisit katsoa lisätietoja kortista tai avata sen [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa, käyttäjillä on oltava sivun ja sen tietojen lukuoikeus.
    - Jos haluat muuttaa tietoja, käyttäjän täytyy muokata käyttöoikeuksia.
    
    Tietoja käyttöoikeuksista on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).

## <a name="installing-the-business-central-app-by-using-centralized-deployment"></a>Business Central -sovelluksen asentaminen keskitetyn käyttöönoton avulla

Microsoft Teams -hallintakeskus on paikka, jossa määritetään Teams-sovelluksen asetuskäytännöt organisaatiota varten. Teams-hallintakeskuksessa voit käyttää keskitetyn käyttöönoton ominaisuutta, kun haluat asentaa Business Central -sovelluksen automaattisesti Teamsiin kaikille organisaation käyttäjille, tietyille ryhmille tai yksittäisille käyttäjille.

> [!NOTE]
> Jotta voisit määrittää keskitetyn käyttöönoton, Teams-tililläsi täytyy olla **Teams-palvelun järjestelmänvalvoja** -rooli tai **Yleinen järjestelmänvalvoja** -rooli.

1. Valitse Business Centralissa ![Suurennuslasi, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Teams-sovelluksen keskitetty käyttöönotto** ja valitse sitten liittyvä linkki. Voit myös avata sivun suoraan valitsemalla [tämän](https://businesscentral.dynamics.com/?page=1833).
2. Lue tietoja **Teamsin Business Central-sovelluksen määrittämisestä** ja valitse sitten **Seuraava**, kun olet valmis.
3. Avaa [Teamsin hallintakeskus ](https://go.microsoft.com/fwlink/?linkid=2163970) ja tee seuraavat toimet.
    1. Siirry kohtaan **Teams-sovellukset** > **Asennuskäytännöt**.
    2. Luo uusi käytäntö tai valitse käytäntö, jota haluat käyttää Business Central -sovelluksen asentamiseen, ja valitse sitten **Lisää sovelluksia**.
    3. Etsi ja valitse **Lisää asennetut sovellukset** -sivulla **Business Central**.
    4. Valitse **Lisää**.

       Business Centralin pitäisi nyt näkyä käytännön **Asennetut sovellukset** -kohdassa.
    5. Määritä tarvittavat lisäasetukset ja valitse **Tallenna**.

    Lisä tietoja Teamsin asennuskäytännöistä on Teams-dokumentaation ohjeaiheessa [Sovelluksen asennuskäytäntöjen hallinta Microsoft Teamsissa](/MicrosoftTeams/teams-app-setup-policies).
4. Siirry takaisin **Teams-sovellusten keskitetty käyttöönotto** -kohtaan Business Centralissa ja valitse **Valmis**.

> [!IMPORTANT]
> Sovelluksen asennuskäytännön päivitys ja sovelluksen käyttöönotto käyttäjille voi kestää jopa 24 tuntia.

## <a name="managing-privacy-and-compliance"></a>Tietosuojan ja vaatimustenmukaisuuden hallinta

Microsoft Teams sisältää laajoja hallintatoimintoja, jotka koskevat arkaluontoisten tai henkilökohtaisten tunnistetietojen säännöstenmukaisuutta ja hallintaa – koskien myös [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen chatteihin ja kanaviin lisättyjä tietoja.

### <a name="understanding-where--cards-are-stored"></a>[!INCLUDE [prod_short](includes/prod_short.md)] -korttien tallennussijainnin ymmärtäminen

Kun kortti on lähetetty chattiin, kortti ja kortissa näkyvät kentät kopioidaan Teamsiin. Nämä tiedot ovat organisaation Teams-käytäntöjen, esimerkiksi tietojensäilytyskäytäntöjen, alaisia. Kun näytetään kortin tiedot, mitään Tiedot-ikkunan tietoja ei tallenneta Teamsiin. Tiedot säilyvät tallennettuna [!INCLUDE [prod_short](includes/prod_short.md)]iin ja Teams vain noutaa ne, kun käyttäjä päättää tarkastella tietoja. 

- Lisätietoja siitä, mihin Teams tallentaa tiedot, on kohdassa [Tietojen sijainti Microsoft Teamsissa](/microsoftteams/location-of-data-in-teams).
- Lisätietoja Teamsin säilytyskäytännöistä on kohdassa [Microsoft Teamsin säilytyskäytännöt](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Korttien jakamisen rajoittaminen

Voit estää tiettyjä käyttäjiä tai ryhmiä lähettämästä kortteja chatteihin tai kanaviin, kun määrität viestikäytäntöjä, jotka ottavat **URL-esikatselut** -asetuksen pois käytöstä. Lisätietoja tästä asetuksen käyttämisestä on kohdassa [Teamsin viestintäkäytäntöjen hallinta](/microsoftteams/messaging-policies-in-teams). 

Tietoesteiden avulla voit myös estää yksittäisiä henkilöitä tai ryhmiä viestimästä keskenään. Lisätietoja on kohdassa [Tietoesteet Microsoft Teamsissa](/microsoftteams/information-barriers-in-teams).

Microsoft 365 Security & Compliance Centerin tietojen menetyksen estämisen ominaisuuksia ei voi kohdistaa erityisesti kortteihin. Mutta niitä voidaan käyttää chat-viesteihin, jotka sisältävät kortteja. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests"></a>Tietopyyntöihin vastaaminen

Annat tiimin jäsenille ja tiimin omistajille mahdollisuuden poistaa viestejä, jotka sisältävät arkaluonteisia kortteja, määrittämällä viestikäytännöt, kuten: **Omistajat voivat poistaa lähetettyjä viestejä** ja **Käyttäjät voivat poistaa lähetettyjä viestejä**. Lisätietoja: [Teamsin viestintäkäytäntöjen hallinta](/microsoftteams/messaging-policies-in-teams).

Microsoft 365:n tietoturva- ja yhteensopivuuskeskuksen sisältöhaun ja eDiscoveryn vaatimustenmukaisuuden ominaisuudet voidaan kohdistaa myös kortteihin.

Koska Teamsin korttien tiedot ovat kopio [!INCLUDE [prod_short](includes/prod_short.md)]in tiedoista, voit myös käyttää [!INCLUDE [prod_short](includes/prod_short.md)] -ominaisuuksia asiakkaan tietojen viemiseen pyydettäessä. Lisä tietoja tietosuojasta on [!INCLUDE [prod_short](includes/prod_short.md)][Business Central-asiakkaiden tietosuojan usein kysytyissä kysymyksissä](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="show-or-hide-record-data-on-cards"></a>Näytä tai Piilota korttien tietueiden tiedot

Kun tietue jaetaan muiden kanssa Teams-keskustelussa tai -kanavassa, näytetään kortti, jossa on tietueen tietoja sisältävät kentät. Kaikki vastaanottajat voivat tarkastella näitä tietoja (tai tietueiden yhteenvetoa) oletusarvoisesti riippumatta niiden käyttöoikeuksista tai oikeuksista Business Centralin yhteydessä. Jos olet ylläpitäjä, voit piilottaa tietueiden yhteenvedon **kortin asetukset** asetusten ohjattu määritys -toiminnolla, joka näkyy Teamsin korteissa. Tietueen yhteenvedon piilottaminen poistaa kaikki kentät ja kuvat, mutta näyttää edelleen **Tiedot**-painikkeen ja muut kortilla olevat ei-tietuetiedot.

|Tietueen yhteenveto käytössä|Tietueen yhteenveto ei käytössä|
|-|-|
|![Kuva, jossa näkyy kortti Teamsissa, kun tietueiden yhteenveto on käytössä.](media/card-settings-example-on.png)|![Kuva, jossa näkyy kortti Teamsissa, kun tietueiden yhteenveto ei ole käytössä.](media/card-settings-example-off.png)|

Asetus määritetään ympäristöä kohti. Joten kun otat tietueiden yhteenvedon käyttöön tai poistat sen käytöstä, se vaikuttaa kaikkiin ympäristön yrityksiin.

1. Avaa Business Centralissa ympäristö, jota haluat muuttaa.

   > [!TIP]
   > Vaihda ympäristöä valitsemalla <kbd>Ctrl</kbd>+<kbd>O</kbd>.
2. Valitse ![Suurennuslasi, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kortin asetukset** ja valitse sitten vastaava linkki. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Lue **kortin asetusten** tiedot ja valitse **Seuraava**, kun olet valmis.
4. Ota **Tietojen näkyvyys** -sivulla käyttöön **Näytä tietueiden yhteenveto** -kytkin, joka näyttää korttien tiedot tai piilottaa tiedot.
5. Valitse **Seuraava** ja viimeistele asennusopas noudattamalla ohjeita.

## <a name="see-also"></a>Katso myös

[[!INCLUDE [prod_short](includes/prod_short.md)]in ja Microsoft Teamsin integroinnin yleiskatsaus](across-teams-overview.md)  
[Microsoft Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen](across-install-app-for-teams.md)  
[Teams – usein kysytyt kysymykset](teams-faq.md)  
[Vianetsintä – Teams](admin-teams-troubleshooting.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
