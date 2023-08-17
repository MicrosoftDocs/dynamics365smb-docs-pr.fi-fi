---
title: Yhteyshenkilöiden hakeminen Microsoft Teamsista
description: 'Tietoja Business Centralin asiakkaiden, toimittajien ja muiden yhteyshenkilöiden hakeminen Microsoft Teamsista.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions'
ms.date: 04/12/2021
ms.author: jswymer
---

# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a>Asiakkaiden, toimittajien ja muiden yhteyshenkilöiden hakeminen Microsoft Teamsista

[!INCLUDE [online_only](includes/online_only.md)]. Otettiin käyttöön vuoden 2021 1. julkaisuaallossa.

[!INCLUDE [prod_short](includes/prod_short.md)]issa on kattava liiketoiminnan yhteyshenkilöiden hallintajärjestelmä, joka on välttämätön myynnin, toimintojen tai muiden osastoroolien käyttäjille. Jos käyttäjällä on jokin näistä rooleista, hänen on usein haettava tai tavattava toimittajia, asiakkaita ja muita yhteyshenkilöitä tai aloitettava keskustelu heidän kanssaan. Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksessa nämä tehtävät voidaan tehdä suoraan Teamsissa ilman, että olisi siirryttävä [!INCLUDE [prod_short](includes/prod_short.md)]iin. Teamsissa voi toimia seuraavasti:

- [!INCLUDE [prod_short](includes/prod_short.md)] -yhteyshenkilöiden hakeminen Teams-komentoruudussa tai viestiruudussa. Yhteyshenkilöt voivat sisältää prospekteja, toimittajia, asiakkaita tai muita liikesuhteita.
- Yhteyshenkilön jakaminen korttina Teams-keskustelussa.
- Näytä yhteyshenkilötiedot, vuorovaikutushistoria ja muut merkitykselliset tiedot, kuten avoimet maksut tai asiakirjat.

## <a name="prerequisites"></a>Vaatimukset

- Sinulla on Microsoft Teamsin käyttöoikeus.
- Olet asentanut [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen Teamsiin. Lisätietoja, katso [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsiin](across-install-app-for-teams.md)
- Käytössä on [!INCLUDE [prod_short](includes/prod_short.md)] -tili, jolla voi käyttää ainakin yhden yrityksen yhteyshenkilöitä.

> [!NOTE]
> Riippumatta siitä, tehdäänkö haku komento- vai viestiruudussa, sinua voidaan pyytää ensimmäisellä kerralla kirjautumaan sisään tai määrittämään sovellus. Tämä vaihe on välttämätön, jotta yhteyshenkilöitä voidaan hakea oikeasta Business Central -yrityksestä. Lisätietoja sovelluksen määrittämisestä valitsemaan yritys on kohdassa [Yrityksen ja muiden asetusten muuttaminen Teamsissa](across-teams-settings.md).

## <a name="look-up-contacts-from-the-command-box"></a>Yhteyshenkilöiden haku komentoruudussa

Komentoruutu on jokaisen Teamsin näytön yläosassa. Sen avulla voi hakea, tehdä pikatoimintoja tai käynnistää sovelluksia, kuten [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen. Komentoruutuhaku sopii hyvin yhteyshenkilöiden ja niihin liittyvien tietojen hakemiseen nopeasti omaan käyttöön. Oletetaan esimerkiksi, että haluat hakea toimittajan sähköpostiosoitteen kalenteritapaamisen määrittämistä varten. Tai ehkä haluat hakea vuorovaikutushistorian asiakastapaamisen aikana.

1. Kirjoita komentoruutuun **@Business Central** ja valitse sitten tuloksissa Business Central -sovellus.

    ![Avaa Business Central -sovellus ja hae yhteyshenkilöitä komentoruudussa.](media/teams-contacts-command-1.png)

2. Aloita tekstin, kuten nimen, osoitteen tai puhelinnumeron, kirjoittaminen **Business Central** -ruutuun.

    Hakua vastaavia tuloksia näytetään hakusanaa kirjoitettaessa.

    ![Business Central -yhteyshenkilöiden haku Teamsin komentoruudussa.](media/teams-contacts-command-2.png)
3. Valitse yhteyshenkilö tuloksista.

    Yhteyshenkilökortti avautuu komentoruudun alapuolella.

4. Jos haluat lisätä yhteyshenkilökortin keskusteluun, siirry valitse kortin oikeassa yläkulmassa **... (Lisää vaihtoehtoja)** > **Kopioi**. Liitä sitten kopio keskustelun viestiruutuun.  

Lisätietoja Teamsin komentoruudusta on kohdassa [Teams – komentoruudun käyttö](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).

## <a name="look-up-contacts-from-the-message-compose-box"></a>Yhteyshenkilöiden haku viestiruudussa

Viestiruudun käytön etuna on se, että yhteyshenkilökortti voidaan lisätä suoraan keskusteluun muiden nähtäväksi.

1. Käynnistä sovellus valitsemalla viestiruudun alapuolella **Business Central** -kuvake.

    Jos **Business Central** -kuvake ei ole näkyvissä, valitse **... (Viestilaajennukset)**.

    ![Yhteyshenkilöiden hakeminen viestiruudussa avaamalla Business Central -sovellus.](media/teams-contacts-message-box.png)

2. Aloita tekstin, kuten nimen, osoitteen tai puhelinnumeron, kirjoittaminen **Business Central** -ruutuun.

    Hakua vastaavia tuloksia näytetään hakusanaa kirjoitettaessa.

    ![Business Central -yhteyshenkilöiden hakeminen viestiruudussa.](media/teams-contacts-5.png)
3. Valitse yhteyshenkilö tuloksista.

    Yhteishenkilökortti avautuu viestiruudussa.

    > [!NOTE]
    > Yhteyshenkilöruutua ei lähetetä heti keskusteluun muiden nähtäväksi. Voit tarkastella kortin sisältöä sekä lisätä tekstiä ennen tarkastelua tai sen jälkeen tarvittaessa. Kun olet valmis, voit lähettää viestin keskusteluun.

### <a name="heres-another-way"></a>Vaihtoehtoinen tapa

1. **Business Central** -kuvakkeen käytön sijaan voit kirjoittaa **@Business Central** suoraan viestiruutuun.
2. Kirjoita hakusanat ruutuun.
3. Valitse yhteyshenkilö näppäimistön ylä- ja alanuolella ja valitse se sitten <kbd>Enter</kbd>-näppäimellä.

## <a name="viewing-contact-card-details"></a>Yhteyshenkilökortin tietojen näyttäminen

Teamsin yhteyshenkilökortista saa nopeasti yleiskuvan asiakkaasta, toimittajasta tai yhteyshenkilöstä. Kortti on vuorovaikutteinen, joten saat tarkasteltavaksi lisää tietoja tai voit muokata yhteyshenkilöä **Tiedot**- tai **Ponnahdusruutu**-painikkeilla.

**Tiedot**-painike avaa Teamsissa ikkunassa, jossa on lisätietoja yhteyshenkilöstä, joskin [!INCLUDE [prod_short](includes/prod_short.md)]issa on näitä tietoja enemmän. Jos haluat nähdä kaikki [!INCLUDE [prod_short](includes/prod_short.md)] -yhteyshenkilön tiedot, valitse **Ponnahdusikkuna**.

Yhteyshenkilökortti toimii samoin kuin tietueiden, kuten nimikkeiden, asiakkaiden tai myyntitilausten, kortit. Lisätietoja korteista on kohdassa [Kortin tietojen näyttäminen](across-working-with-teams.md#view-card-details).

> [!NOTE]
> Kaikki Teams-keskustelun osallistujat voivat tarkastella keskusteluun lähetettäviä Business Central -yhteyshenkilöiden kortteja. Mutta halutessaan tarkastella lisätietoja tietueista käyttämällä **Tiedot**- tai **Ponnahdusikkuna**-painikkeita, he tarvitsevat käyttöoikeuden [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan. Lisätietoja on kohdassa [Microsoft Teams -integraation hallinta](admin-teams-integration.md#minimum-requirements-1).

## <a name="see-also"></a>Katso myös

[Business Centralin ja Microsoft Teamsin integraation yleiskatsaus](across-teams-overview.md)  
[Microsoft Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen](across-install-app-for-teams.md)  
[Teams – usein kysytyt kysymykset](teams-faq.md)  
[Yrityksen ja muiden asetusten muuttaminen Teamsissa](across-teams-settings.md)  
[Tietueiden jakaminen Microsoft Teams -keskusteluissa](across-working-with-teams.md)  
[Vianetsintä – Teams](admin-teams-troubleshooting.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
