---
title: Business Central -välilehden lisääminen Microsoft Teamsiin
description: 'Opettele lisäämään Teamsiin välilehtiä, jotka näyttävät Business Central -sivut.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# <a name="add-business-central-tab-in-microsoft-teams"></a><a name="add-business-central-tab-in-microsoft-teams"></a>Business Central -välilehden lisääminen Microsoft Teamsiin

[!INCLUDE [online_only](includes/online_only.md)]

Teamsissa välilehdet näkyvät kanavien ja keskustelujen yläosassa, jolloin osallistujat pääsevät nopeasti käsiksi olennaisiin tietoihin. Tässä artikkelissa selitetään erilaisia tapoja lisätä välilehti, joka näyttää [!INCLUDE [prod_short](includes/prod_short.md)] -tiedot.

![Välilehdet Teamsissa](media/teams-tabs-border.png)

## <a name="about-business-central-tabs"></a><a name="about-business-central-tabs"></a>Tietoja Business Centralin välilehdistä

[!INCLUDE [prod_short](includes/prod_short.md)] -välilehdessä on keskitetty näkymä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman luettelo- ja korttisivuista. Välilehdessä ei näy koko [!INCLUDE [prod_short](includes/prod_short.md)] -WWW-asiakasohjelmaa. Ei ole selaimen rajaa, [!INCLUDE [prod_short](includes/prod_short.md)] -ilmoituspalkkia (esim. Kerro minulle, haku, ohje) tai ylänavigointivalikkoa&mdash;vain sivun sisältö ja sen toiminnot. Sisältö on vuorovaikutteinen, joten voit valita toimintoja ja linkkejä, muuttaa tietoja ja paljon muuta. Käyttöoikeutesi rajoittuvat siihen, mitä näet ja mitä voit tehdä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman tiliisi liitetyistä käyttöoikeuksista.

Lisätietoja siitä, ketkä voivat tarkastella [!INCLUDE [prod_short](includes/prod_short.md)] -välilehden sisältöä, on kohdassa [Kuka voi nähdä välilehden sisällön?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Oletko kehittäjä? Voit myös lisätä välilehtiä ohjelmallisesti Microsoft Graph API -liittymän avulla. Lisätietoja on kohdassa [Business Central -välilehtien lisääminen Teamsiin](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites"></a><a name="prerequisites"></a>Vaatimukset

Jotta voit lisätä [!INCLUDE [prod_short](includes/prod_short.md)]-välilehden, seuraavien vaatimusten on täytyttävä:

- Sinulla on Microsoft Teamsin käyttöoikeus.
- Käytössä on [!INCLUDE [prod_short](includes/prod_short.md)] -käyttöoikeus.
- Olet asentanut [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen Teamsiin. Lisätietoja, katso [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsiin](across-install-app-for-teams.md).

Jos haluat tarkastella [!INCLUDE [prod_short](includes/prod_short.md)] -välilehteä, jonka toinen osallistuja on lisännyt kanavaan tai keskusteluun, seuraavien vaatimusten on täytyttävä:

- Sinulla on Microsoft Teamsin käyttöoikeus.
- Sinulla on [!INCLUDE [prod_short](includes/prod_short.md)] -käyttöoikeus tai rajoitettu pääsy Business Centraliin Microsoft 365:n käyttöoikeuden avulla. Lisätietoja on kohdassa [Business Centralin käyttö Microsoft 365:n käyttöoikeuksien avulla](admin-access-with-m365-license.md).
- Olet asentanut [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen Teamsiin.

## <a name="add-tab-using-recommended-content"></a><a name="add-tab-using-recommended-content"></a>Lisää välilehti käyttäen suositeltua sisältöä

Näiden vaiheiden avulla voit lisätä välilehden valitsemalla, mitä näyttöön tulee käytettävissä olevasta suositellusta sisällöstä, joka perustuu roolikeskukseesi&mdash;ilman Teamsista poistumista. Lisätietoja sisällöstä, josta voit valita, on ohje aiheessa [Mistä suositeltu sisältö on peräisin](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Valitse kanavan tai Teams-keskustelun yläosassa **+ Lisää välilehti**.
2. Kirjoita **haku**-ruutuun *Business Central* ja valitse sitten **[!INCLUDE [prod_short](includes/prod_short.md)]** -kuvake ja odota, kunnes [!INCLUDE [prod_short](includes/prod_short.md)] -välilehden asetukset-ikkuna tulee näkyviin.

   ![Näyttää Business Central -välilehden määritysikkunan Teamsissa](media/teams-bc-tab-config-window.png)

3. **Valitse suositellusta sisällöstä** -valinta näyttää yrityksen, jossa työskentelet [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa. Jos haluat näyttää toisen yrityksen sisältöä, valitse tämänhetkinen yritys ja määritä sitten yritys, jota haluat käsitellä, käyttämällä **ympäristö**- ja **yritys**-asetuksia.
4. Valitse **Välilehden sisältö** -vaihtoehdon alanuoli ja valitse sisältö, jonka haluat näyttää.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Jotkin sivut voivat sisältää erilaisia näkymiä, jotka ovat suodatetun sivun muunnelmia, jotka näyttävät tietyt tiedot. Jos haluat muuttaa sisällön näkymää, valitse **haluamasi näkymä** -vaihtoehdon alanuoli ja valitse näkymä luettelosta.

   Lisätietoja näkymistä on kohdassa [Näkymien tallentaminen ja mukauttaminen](ui-views.md).
6. Valitse **Julkaise kanavalle tästä välilehdestä**, jos haluat lähettää tiedotteen automaattisesti Teams-kanavassa tai -keskustelussa ja antaa osallistujien tietää, että olet lisännyt tämän välilehden.
7. Valitse **Tallenna**.

## <a name="add-tab-using-a-page-link"></a><a name="add-tab-using-a-page-link"></a>Lisää välilehti käyttämällä sivun linkkiä

Toinen tapa lisätä välilehti käyttämällä näytettävän sivun linkkiä (URL). Tästä on hyötyä silloin, kun haluat näyttää tietyn [!INCLUDE [prod_short](includes/prod_short.md)] -tietueen tai -luettelosivun, jota ei ole merkitty roolikeskuksessa.

1. Valitse kanavan tai Teams-keskustelun yläosassa **+ Lisää välilehti**.
2. Kirjoita **haku**-ruutuun *Business Central* ja valitse sitten**[!INCLUDE [prod_short](includes/prod_short.md)]** -kuvake.
3. Odota, että [!INCLUDE [prod_short](includes/prod_short.md)] -välilehden määritys ikkuna tulee näkyviin, valitse sitten **Liitä [!INCLUDE [prod_short](includes/prod_short.md)] -linkki sen sijaan** -asetus.

   ![Näyttää Business Central -välilehden konfigurointi-ikkunan Teamsissa ja korostaa linkkiasetuksen](media/teams-bc-tab-config-window-page-link.png)
4. Siirry [!INCLUDE [prod_short](includes/prod_short.md)] -kohtaan ja avaa sivu, jonka haluat näkyvän välilehdessä.
5. Kopioi linkki sivulle.

   Linkin voi kopioida kahdella tavalla. Helpoin ja suosituin tapa on valita **Jaa** ![Jaa-kuvake Business Centralissa](media/share-icon.png) > **Kopioi linkki**. Toinen tapa on kopioida koko URL-osoite suoraan selaimen osoiteriviltä. Lisätietoja tästä vaiheesta on kohdassa [Business Central -tietueiden ja sivulinkkien jakaminen](across-working-with-teams.md).

6. Mene takaisin Teamsiin ja liitä linkki **URL**-ruutuun.
7. Kirjoita **välilehden nimi** -ruutuun nimi, joka näkyy välilehdessä.
8. Valitse **Julkaise kanavalle tästä välilehdestä**, jos haluat lähettää tiedotteen automaattisesti Teams-kanavassa tai -keskustelussa ja antaa osallistujien tietää, että olet lisännyt tämän välilehden.
9. Valitse **Tallenna**.

## <a name="add-tab-by-pinning-card-details"></a><a name="add-tab-by-pinning-card-details"></a>Lisää välilehti kiinnittämällä kortin tiedot

Näiden vaiheiden avulla voit lisätä välilehden, joka on jaettu tai kopioitu Teams-kanavaan tai -keskusteluun. Tietoja tietueiden ja sivulinkkien jakamisesta Teamsissa on kohdassa [Tietueiden ja sivulinkkien jakaminen Teamsissa](across-working-with-teams.md).

1. Valitse Teams-kohdassa **tiedot**-painike kortilta.
2. Valitse korttitietojen oikeasta yläkulmasta **Kiinnitä keskustelun yläpuolelle** ![Kiinnitä kuvake lisäämällä Teams-välilehti Business Centraliin](media/pin-teams.png) -kuvakkeeseen.

## <a name="change-a-tab-and-its-content"></a><a name="change-a-tab-and-its-content"></a>Välilehden ja sen sisällön muuttaminen

Kun välilehti on lisätty, voit tehdä välilehteen tiettyjä muutoksia. Voit esimerkiksi nimetä välilehden uudelleen, siirtää sen ja poistaa sen. Löydät nämä toiminnot käytettävissä olevista välilehden vaihtoehdoista valitsemalla välilehdestä alanuolen.

![Näyttää Business Central -välilehden konfigurointi-ikkunan Teamsissa ja välilehden asetusvalikon](media/teams-bc-tab-config-window-options.png)

Välilehden sisällön osalta voit muokata tietoja, jos sinulla on tarvittavat käyttöoikeudet. Jos muutat tietoja, muutokset eivät näy, ennen kuin käyttäjät poistuvat välilehdestä ja palaavat takaisin. Sama pätee, jos joku muu tekee muutoksia tietoihin. Et voi muuttaa sivua, joka näkyy välilehdessä, joten poista välilehti ja lisää toinen, joka sopii.

Voit myös muuttaa sivun ja sen tietojen näkymää, esimerkiksi lajitella ja vaihtaa asettelua luettelo- ja ruutunäkymien välillä. Kun teet tällaisia muutoksia, ne eivät vaikuta siihen, mitä muut näkevät. He näkevät, mitä alun perin julkaisit, kunnes he tekevät samanlaisia muutoksia itse.

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Business Centralin ja Microsoft Teamsin integraation yleiskatsaus](across-teams-overview.md)  
[Microsoft Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen](across-install-app-for-teams.md)  
[Business Central -tietueiden ja sivulinkkien jakaminen Microsoft Teamsissa](across-working-with-teams.md).
[Teams – usein kysytyt kysymykset](teams-faq.md)  
[Asiakkaiden, toimittajien ja muiden yhteyshenkilöiden hakeminen Microsoft Teamsista](across-search-contacts-teams.md)  
[Yrityksen ja muiden asetusten muuttaminen Teamsissa](across-teams-settings.md)  
[Vianetsintä – Teams](admin-teams-troubleshooting.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
