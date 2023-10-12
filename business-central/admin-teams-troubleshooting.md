---
title: Microsoft Teams -integroinnin vianmääritys
description: 'Tietoja siitä, mitä järjestelmänvalvojana voit tehdä Microsoft Teams -integroinnin hallitsemiseksi.'
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors'
ms.date: 09/19/2023
ms.author: jswymer
---

# <a name="troubleshoot-microsoft-teams-integration-with-"></a>[!INCLUDE [prod_short](includes/prod_short.md)] ja Microsoft Teamsin integroinnin vianmääritys

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Tässä artikkelissa on tietoja tavallisten käyttäjien tai järjestelmänvalvojien kohtaamien ongelmien tunnistamisesta ja korjaamisesta, kun käytetään Microsoft Teamsia [!INCLUDE [prod_short](includes/prod_short.md)]in kanssa.

## <a name="the-sign-in-link-doesnt-work"></a>Sisäänkirjautumislinkki ei toimi

Jos yritit kirjautua Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellukseen heti sovelluksen asentamisen jälkeen eikä kirjautumislinkki toiminut, sovelluksen asennus ei ehkä ole vielä täysin valmis. Yritä korjata ongelma kirjautumalla ulos Teams-asiakasohjelmasta ja kirjautumalla sitten uudelleen sisään.

## <a name="the-settings-page-is-empty"></a>Asetukset-sivu on tyhjä

Asetuksiin pääsee vasta kirjautumisen jälkeen. Kirjaudu sovellukseen joko liittämällä linkki [!INCLUDE [prod_short.md](includes/prod_short.md)] -tietueeseen ja yrittämällä hakea yhteyshenkilöitä. Kumpikin toiminto vie kirjautumiskokemukseen, jonka jälkeen **Asetukset**-sivu on käytettävissä.

## <a name="i-changed-company-but-it-didnt-seem-to-work"></a>Yrityksen vaihtaminen ei näytä onnistuneen

Kun yritys on vaihdettu **Asetukset**-sivulla, komentoruudun avattava luettelo voi ilmaista, että haku tapahtuu edelleen edellisessä yrityksessä. Tämä ongelma esiintyy, kun **Asetukset**-sivu avataan suoraan komentoruudussa. Tässä tapauksessa yrityksen vaihtaminen onnistui ja haku tehdään vaihdetussa yrityksessä. Ongelmana on vain se, että komentoruudun avattavaa luetteloa ei ole vielä päivitetty. Jotta avattava luettelo ilmaisisi haun kohteena olevan yrityksen oikein, [!INCLUDE [prod_short.md](includes/prod_short.md)] on suljettava komentoruudussa tai sen kiinnitys poistettava, jonka jälkeen sovellus on avattava uudelleen. 


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## <a name="something-went-wrong-error-when-searching-for-contacts"></a>Tapahtui virhe -ilmoitus yhteyshenkilöitä haettaessa

Tämä virhe voi esiintyä, kun haku koskee yritystä, jota ei ole käynnistetty tai joka ei vastaa. Hakua ei voi esimerkiksi tehdä uudessa kokeiluversion yrityksessä, joka ei vielä hyväksynyt käyttöehtoja. Ongelman voi ratkaista kokeilemalla kirjautumista [!INCLUDE [prod_short.md](includes/prod_short.md)] -verkkoasiakasohjelmaan sekä toimimalla avautuvien valintaikkunoiden ohjeiden mukaisesti tai hylkäämällä ne.

## <a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a>Yhteyshenkilön tai yhteyshenkilön yhteenvedon ohjelmointirajapintaa ei löydy -virhe, kun yhteyshenkilöitä haetaan

Mukauttamiset tai toimialasovellukset voivat aiheuttaa tämän virheen vaikuttaessaan tuotteeseen [!INCLUDE [prod_short.md](includes/prod_short.md)] tai muokatessaan sitä, tai ne eivät sisällä yhteyshenkilön tai yhteyshenkilön yhteenvedon ohjelmointirajapintaa. Jos ongelma toistuu, ota yhteys järjestelmänvalvojaan tai tukeen.

## <a name="none-of-my-links-expand-into-a-card"></a>Yksikään linkkini ei laajennu kortiksi

Jos kohtaat tämän ongelman, kokeile seuraavia asioita:

1. Varmista ensin, että Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus on asennettu.

    Voit tarkistaa sen kirjautumalla Teams-työpöytäsovellukseen tai Teamsin selainversioon. Valitse sitten vasemmalta puolelta **sovellukset**ja etsi **[!INCLUDE [prod_short](includes/prod_short.md)]**. Kun löydät **[!INCLUDE [prod_short](includes/prod_short.md)]** -sovelluksen, avaa Sovelluksen tiedot -sivu valitsemalla se. Jos **Lisää**-painike näkyy, [!INCLUDE [prod_short](includes/prod_short.md)] -sovellusta ei ole asennettu. Lisätietoja sovelluksen asentamisesta on kohdassa [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsille](across-install-app-for-teams.md).

    > [!NOTE]
    > Vieraskäyttäjät eivät voi heti asentaa sovelluksia. Lisä tietoja vieraskäyttäjistä on [usein kysytyissä kysymyksissä koskien yhteistyötä asiakkaiden kanssa](teams-faq.md?tabs=collaborating#language). 

2. Tarkista seuraavaksi, että olet kirjautunut sisään oikeilla tunnistetiedoilla.

    Siirry Teamsissa mihin tahansa keskusteluun, valitse viestiruudussa [!INCLUDE [prod_short](includes/prod_short.md)] -kuvake hiiren kakkospainikkeella ja valitse sitten **Asetukset**. Näyttöön avautuu ikkuna, jossa kerrotaan käyttäjätili, johon olet kirjautunut. Varmista, että käyttäjätili on oikea.

3. Varmista, että codeunit 2718 **Sivun yhteenvedon toimittaja** on julkaistu verkkopalveluna.

    Teams muodostaa yhteyden [!INCLUDE [prod_short](includes/prod_short.md)]iin tämän codeunitin päätepisteeseen [!INCLUDE [prod_short](includes/prod_short.md)]issa. Tietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

4. Organisaatiosi voi myös rajoittaa, että et voi liittää linkkejä, jotka laajenevat korteiksi. Ota yhteyttä järjestelmänvalvojaan, jotta ymmärrät Teamsin organisaatiokäytännöt, jotka voivat koskea sinua.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Linkki ei aina laajennu kortiksi

Linkki ei laajennu kortiksi seuraavissa tilanteissa:

- Linkki kohdistuu sivuun, jota (teknisellä tasolla) ei ole liitetty [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman lähdetaulukkoon. Voit tarkistaa, onko sivulla lähdetaulukko, verkkoasiakkaan sivun tarkastusruudun avulla [!INCLUDE [prod_short](includes/prod_short.md)]issa. Lisätietoja sivun tarkastuksesta on kohdassa [Sivujen tarkastaminen](across-inspect-page.md).
- Teams ei tue linkkien esikatseluita joissakin ominaisuuksissa. Avaa esimerkiksi keskustelun ponnahdusikkunassa tai olet vieras toisessa organisaatiossa.
- Teams hiljaa hylkää kortin näyttämisen yrittämisen 15 sekunnin kuluttua esimerkiksi verkko-ongelmien vuoksi.
- Teams ei välttämättä laajenna linkkiä, jos olet jo liittänyt linkin samaan viestiruutuun ja poistanut kortin.

Linkin tulee sisältää myös kaikki tarvittavat tiedot, jotta tietue voidaan paikantaa ja sitä vastaava kortti näyttää. Näitä tietoja ovat:

- Ympäristön nimi sisällyttämällä se URL-polkuun. Jos et määrittele ympäristön nimeä, Teams olettaa, että yrität päästä ympäristöön nimeltä "Tuotanto".
- Yrityksen nimi, käyttämällä parametria *company=*
- Sivun tunnus käyttämällä parametria *page=*
- Kirjanmerkki tietueeseen käyttämällä parametria*bookmark=*

Esimerkiksi:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Teknisiä tietoja [!INCLUDE [prod_short](includes/prod_short.md)]in URL-osoitteista on [!INCLUDE [prod_short](includes/prod_short.md)]in kehittäjän ja IT-ammattilaisen ohjeessa kohdassa [Verkkoasiakkaan URL-osoite](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

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

- Lisätietoja [!INCLUDE [prod_short](includes/prod_short.md)]in kielen vaihtamisesta on ohjeaiheessa [Perusasetusten muuttaminen –kieli](ui-change-basic-settings.md#language).

Lisätietoja siitä, miten kielet toimivat Teamsin ja [!INCLUDE [prod_short](includes/prod_short.md)]in välillä, on kohdassa [Teams – usein kysytyt kysymykset](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Muokkasin tietoikkunan kenttä, mutta muutosta ei tallennettu

Tiedot-ikkunoissa kenttään tekemäsi muutokset tallentuvat automaattisesti, kun poistut kentästä. Ennen kuin suljet ikkunan sen jälkeen, kun olet muuttanut kenttää, valitse <kbd>Sarkain</kbd>-näppäin tai napsauta/napauta kentän ulkopuolella.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>Uusi ruutu ilmestyi sovelluksen käynnistimeen. Miten poistan sen?

Kun tarkastelet sovelluksia Office 365 -kotisivulla (https://home.office.com) tai sovelluksen käynnistimessä, uusi "Business Central teams Integration Service Connector" -niminen ruutu tulee näkyviin, kun Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus on asennettu. Tämä ruutu ei tarjoa arvoa itsessään, ja se voidaan piilottaa turvallisesti.

Järjestelmänvalvoja, jolla on Microsoft Entra -järjestelmänvalvojan käyttöoikeudet, voit piilottaa ruudun toimimalla seuraavasti:

1. Kirjaudu [Microsoft Entra -hallintakeskukseen](https://entra.microsoft.com/).
2. Valitse **Yrityssovellukset** ja valitse sitten **Business Central Teams Integration Service Connector**.
3. Valitse **Ominaisuudet**, määritä sitten **Näkyy käyttäjille** -valitsin asentoon **Ei**.
4. Valitse **Tallenna**.

> [!NOTE]
> Tämä muutos tulee voimaan jonkin ajan kuluttua.

## <a name="duplicate-text-in-the-share-to-teams-window"></a>Monista teksti Jaa Teamsiin -ikkunassa

Kun liität tekstiä **Jaa Teamsiin** -ikkunan sanomaruutuun, teksti monistetaan. Tämä ongelma on Microsoftin tiedossa, ja sitä käsitellään myöhemmässä päivityksessä. 

## <a name="unable-to-sign-in-to-the-share-to-teams-window"></a>Jaa Teamsiin -ikkunaan ei voi kirjautua

Tämä ongelma voi johtua useista eri syistä. Esimerkiksi käyttäjätunnuksella, jota käytät sisäänkirjautuessa, on oltava käyttöoikeus Microsoft Teamsiin esimerkiksi Microsoft 365 -tilauksen kautta.

## <a name="my-cards-no-longer-have-a-popout-button"></a>Kortteissani ei ole enää ponnahduspainiketta

Huhtikuusta 2022 alkaen linkit, jotka näkyvät kompaktina korttina Teamsissa, eivät enää sisällä **Ponnahdusikkuna**-painiketta. Jos haluat avata kortin omassa ikkunassaan, valitse **Tiedot**-painike ja sitten **Avaa selaimessa** ikkunan oikeassa yläkulmassa olevasta ellipsivalikosta (**...**).

## <a name="cant-pin-a-card-to-tab"></a>Kortin kiinnittäminen välilehteen ei onnistu

Tälle ongelmalle on pari syytä.

- Jos kortti oli jaettu Search ME:stä, sitä ei voi kiinnittää välilehteen. 

- Kiinnittäminen ei onnistu, ennen kuin lisäät ensimmäisen Business Central -välilehden. Tämä ongelma on tiedossa Teamsissa. 

## <a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a>Joku lisäsi välilehden, mutta välilehti ei näy minulle

Tämä ongelma johtuu siitä, että sinulla ei ole asennettuna BC-sovellusta Teamsille. Vain he, joilla on sovellus asennettuna, näkevät Business Central -välilehdet.

## <a name="others-see-a-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a>Toiset näkevät eri lajittelu- tai sarakeasettelun kuin välilehden tekijä näkee

Tämä ongelma johtuu todennäköisesti siitä, että olet jakanut oman näkymän luettelonäkymänä. Tässä tapauksessa voit työskennellä yhdessä järjestelmänvalvojan kanssa ja luoda joko roolikohtaisia luettelonäkymiä, jotka peittävät kanavan/keskustelun eri roolit, tai luoda tämän näkymän koko organisaatiolle, jotta kaikki voivat saada yhdenmukaisen näkymän.


## <a name="see-also"></a>Katso myös

[[!INCLUDE [prod_short](includes/prod_short.md)]in ja Microsoft Teamsin integroinnin yleiskatsaus](across-teams-overview.md)  
[Microsoft Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen](across-install-app-for-teams.md)  
[Asiakkaiden, toimittajien ja muiden yhteyshenkilöiden hakeminen Microsoft Teamsista](across-search-contacts-teams.md)  
[Tietueiden jakaminen Microsoft Teams -keskusteluissa](across-working-with-teams.md)  
[Teams – usein kysytyt kysymykset](teams-faq.md)  
[Yrityksen ja muiden asetusten muuttaminen Teamsissa](across-teams-settings.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
