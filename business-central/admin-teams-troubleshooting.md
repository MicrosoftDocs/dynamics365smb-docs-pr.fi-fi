---
title: Microsoft Teams -integroinnin vianmääritys
description: Tietoja siitä, mitä järjestelmänvalvojana voit tehdä Microsoft Teams -integroinnin hallitsemiseksi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 10612a3e5e257969b2daf0839ea0826316a956ee
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046530"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>[!INCLUDE [prod_short](includes/prod_short.md)] ja Microsoft Teamsin integroinnin vianmääritys

[!INCLUDE [online_only](includes/online_only.md)]

Tässä artikkelissa on tietoja tavallisten käyttäjien tai järjestelmänvalvojien kohtaamien ongelmien tunnistamisesta ja korjaamisesta, kun käytetään Microsoft Teamsia [!INCLUDE [prod_short](includes/prod_short.md)]in kanssa.

## <a name="none-of-my-links-expand-into-a-card"></a>Yksikään linkkini ei laajennu kortiksi 

Jos kohtaat tämän ongelman, kokeile seuraavia asioita:

1. Varmista ensin, että Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus on asennettu.

    Voit tarkistaa sen kirjautumalla Teams-työpöytäsovellukseen tai Teamsin selainversioon. Valitse sitten vasemmalta puolelta **sovellukset** ja etsi **[!INCLUDE [prod_short](includes/prod_short.md)]**. Kun löydät **[!INCLUDE [prod_short](includes/prod_short.md)]** -sovelluksen, avaa Sovelluksen tiedot -sivu valitsemalla se. Jos **Lisää minulle** -painike näkyy, [!INCLUDE [prod_short](includes/prod_short.md)] -sovellusta ei ole asennettu. Lisätietoja sovelluksen asentamisesta on kohdassa [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsille](across-install-app-for-teams.md).

    > [!NOTE]
    > Vieraskäyttäjät eivät voi heti asentaa sovelluksia. Lisä tietoja vieraskäyttäjistä on usein kysytyissä kysymyksissä koskien yhteistyötä asiakkaiden kanssa. 

2. Tarkista seuraavaksi, että olet kirjautunut sisään oikeilla tunnistetiedoilla.

    Siirry Teamsissa mihin tahansa keskusteluun ja valitse viestiruudusta [!INCLUDE [prod_short](includes/prod_short.md)] -kuvake. Kun näyttöön tulee ikkuna, tarkista, että yhdistetty käyttäjä vastaa sitä, mitä käytät yhteyden muodostamiseen [!INCLUDE [prod_short](includes/prod_short.md)]iin.

3. Varmista, että codeunit 2718 **Sivun yhteenvedon toimittaja** on julkaistu verkkopalveluna.

    Teams muodostaa yhteyden [!INCLUDE [prod_short](includes/prod_short.md)]iin tämän codeunitin päätepisteeseen [!INCLUDE [prod_short](includes/prod_short.md)]issa. Tietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

4. Organisaatiosi voi myös rajoittaa, että et voi liittää linkkejä, jotka laajenevat korteiksi. Ota yhteyttä järjestelmänvalvojaan, jotta ymmärrät Teamsin organisaatiokäytännöt, jotka voivat koskea sinua.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Linkki ei aina laajennu kortiksi 

Linkki ei laajennu kortiksi seuraavissa tilanteissa:

- Linkki kohdistuu sellaiseen sivutyyppiin, joka ei edusta tietuetta. Se voi olla esimerkiksi linkki [!INCLUDE [prod_short](includes/prod_short.md)] -roolikeskukseen. Voit tarkistaa sivutyypin verkkoasiakkaan sivun tarkastusruudun avulla [!INCLUDE [prod_short](includes/prod_short.md)]issa. Lisätietoja sivun tarkastuksesta on kohdassa [Sivujen tarkastaminen](across-inspect-page.md).
- Linkki kohdistuu sivuun, jota (teknisellä tasolla) ei ole liitetty [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman lähdetaulukkoon. Voit tarkistaa, onko sivulla lähdetaulukko, verkkoasiakkaan sivun tarkastusruudun avulla [!INCLUDE [prod_short](includes/prod_short.md)]issa. Lisätietoja sivun tarkastuksesta on kohdassa [Sivujen tarkastaminen](across-inspect-page.md). 
- Teams ei tue linkkien esikatseluita joissakin ominaisuuksissa. Kun esimerkiksi avaat chatin ponnahdusikkunassa, olet kokouksessa tai vieras toisessa organisaatiossa.
- Teams hiljaa hylkää kortin näyttämisen yrittämisen 15 sekunnin kuluttua esimerkiksi verkko-ongelmien vuoksi.
- Teams ei välttämättä laajenna linkkiä, jos olet jo liittänyt linkin samaan viestiruutuun ja poistanut kortin.

Linkin tulee sisältää myös kaikki tarvittavat tiedot, jotta tietue voidaan paikantaa ja sitä vastaava kortti näyttää. Näitä tietoja ovat:

- Ympäristön nimi sisällyttämällä se URL-polkuun. Jos et määrittele ympäristön nimeä, Teams olettaa, että yrität päästä ympäristöön nimeltä "Tuotanto".
- Yrityksen nimi, käyttämällä parametria *company=*
- Sivun tunnus käyttämällä parametria *page=*
- Kirjanmerkki tietueeseen käyttämällä parametria *bookmark=*

Esimerkiksi:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Teknisiä tietoja [!INCLUDE [prod_short](includes/prod_short.md)]in URL-osoitteista on [!INCLUDE [prod_short](includes/prod_short.md)]in kehittäjän ja IT-ammattilaisen ohjeessa kohdassa [Verkkoasiakkaan URL-osoite](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>Kortti näkyy viestiruudussa, mutta Tiedot-painikkeen valitseminen ei tee mitään 

Kun linkki laajenee kortiksi viestiruudussa, sinun on lähetettävä viesti keskusteluun, ennen kuin voit käyttää **Tiedot**-painiketta.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Tiedot-ikkuna aukeaa, mutta näyttöön tulee virhe, ennen kuin tiedot näkyvät

Tämä ongelma voi johtua muutamasta asiasta: käyttöoikeuksien puutteesta [!INCLUDE [prod_short](includes/prod_short.md)]issa tai selaimen asetuksista (käytettäessä Teamsia selaimessa).

1. Tarkista käyttöoikeutesi [!INCLUDE [prod_short](includes/prod_short.md)]issa.

    Jos haluat tarkastella kortin tietoja, [!INCLUDE [prod_short](includes/prod_short.md)] tarkistaa lisenssisi ja käyttöoikeutesi, kun haluat tarkastella tiettyä tietuetta ja sivua tietyssä yrityksessä ja ympäristössä. Jos et ole oikeutettu näihin asioihin, käyttöoikeuksiin liittyvät [!INCLUDE [prod_short](includes/prod_short.md)] -vakiovirhesanomat tulevat näkyviin Tiedot-ikkunaan. 

    Lisätietoja käyttöoikeuksista on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)

2. Tarkista selaimen asetukset, jos käytät Teamsia selaimessa.

    - Selaimen ponnahdusikkunoiden eston täytyy olla joko poissa käytöstä tai asetettu sallimaan toimialueet *businesscentral.dynamics.com* tai *bc.dynamics.com*. Lisätietoja ponnahdusikkunoiden sallimisesta [!INCLUDE [prod_short](includes/prod_short.md)]ille on kohdassa [Selaimen määrittäminen](across-browser-settings.md#popup).
    - Selaimen on voitava käyttää paikallista selaimen tallennustilaa evästeitä ja asetuksia varten, kun työskentelet.
    - Älä käytä vierasselailua tai yksityistä selaamista, ellei se ole tarpeen, koska ne hylkäävät tai estävät tietyt sisällöt joissakin selaimissa.

    Lisätietoja selaimen vähimmäisvaatimuksista on kohdassa [[!INCLUDE [prod_short](includes/prod_short.md)]in käytön vähimmäisvaatimukset](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Minulla on ongelmia kameran tai sijainnin kanssa Teamsissa 

Kun käytät [!INCLUDE [prod_short](includes/prod_short.md)]issa tietoikkunassa ominaisuuksia, jotka vaativat sijainnin tai laitteen kameran käyttöä, sinun on ensin annettava Teamsille suostumuksesi näiden laiteominaisuuksien käyttämiseen.  

- Teams-selainversiossa varmista, että selaimen asetukset sallivat kameroiden ja sijaintien käyttämisen osoitteelle https://teams.microsoft.com. 

- Teamsin iOS- ja Android-versiossa varmista, että laitteen asetukset sallivat kameroiden ja sijaintien käyttämisen Teams-mobiilisovellukselle. 

Lisätietoja näiden asetusten muuttamisesta on Microsoft-tuen ohjeaiheessa [Kamera ei toimi Teamsissa](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us).

[!INCLUDE [prod_short](includes/prod_short.md)] -sovellus ei tue sijaintia Teams-työpöytäsovelluksessa. Lisätietoja sijainnista on [Teamsin usein kysytyissä kysymyksissä](teams-faq.md#location).

Joissakin selaimissa, kuten uudessa Microsoft Edgessä, voit valita, mitä laitekameraa käytetään, kun laitteesi tukee useaa kameraa. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams näyttää useita kieliä korteissani ja korttien tiedoissa 

Jotta korttien ja korttien tiedot näkyvät johdonmukaisesti samalla kielellä Teamsissa, Teams-asiakkaan kielen ja [!INCLUDE [prod_short](includes/prod_short.md)] -verkkoasiakkaassa käytettävän kielen on vastattava toisiaan.

- Lisätietoja Teamsin kielen vaihtamisesta on Microsoft-tuen kohdassa [Teamsi asetusten muuttaminen ](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7). 

- Lisä tietoja [!INCLUDE [prod_short](includes/prod_short.md)]in kielen vaihtamisesta on ohjeaiheessa [Perusasetusten muuttaminen –kieli](ui-change-basic-settings.md#language).

Lisätietoja siitä, miten kielet toimivat Teamsin ja [!INCLUDE [prod_short](includes/prod_short.md)]in välillä, on kohdassa [Teams – usein kysytyt kysymykset](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Muokkasin tietoikkunan kenttä, mutta muutosta ei tallennettu

Tiedot-ikkunoissa kenttään tekemäsi muutokset tallentuvat automaattisesti, kun poistut kentästä. Ennen kuin suljet ikkunan sen jälkeen, kun olet muuttanut kenttää, pidä sarkainta painettuna tai napsauta/napauta kentän ulkopuolella.

## <a name="see-also"></a>Katso myös

[[!INCLUDE [prod_short](includes/prod_short.md)]in ja Microsoft Teamsin integroinnin yleiskatsaus](across-teams-overview.md)  
[Asenna [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)  
[Teams – usein kysytyt kysymykset](teams-faq.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
