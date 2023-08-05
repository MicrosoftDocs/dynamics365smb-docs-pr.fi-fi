---
title: Selaimen määrittäminen
description: 'Tässä artikkelissa kuvataan, miten selaimet määritetään toimimaan Business Centralin ja siihen integroitavien tuotteiden kanssa.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 04/01/2021
ms.author: jswymer
---
# Selaimen määrittäminen ja vianetsintä Business Central -verkkoasiakkaan kanssa työskentelyä varten

Tässä artikkelissa kerrotaan, miten selain määritetään niin, että [!INCLUDE[web_client](includes/web_client.md)] ja kaikki sen ominaisuudet toimivat oikein. Lue tämä artikkeli, jos sinulla on ongelmia [!INCLUDE[web_client](includes/web_client.md)]:n avaamisessa, koska selaimen asetukset saattavat aiheuttaa joitakin ongelmia.

Artikkelissa on yksityiskohtaisia tietoja Microsoft Edgen määrityksestä, mutta JavaScriptin, evästeiden ja ponnahdusikkunoiden vaatimukset ovat samat kaikissa tuetuissa selaimissa. Katso lisätietoja muista selaimista valmistajan tarjoamista ohjeista.  

## Käytä tuettua selainta

Varmista, että käytät jotakin tuetuista selaimista. Lisätietoja on kohdassa [Business Centralin käytön vähimmäisvaatimukset](product-requirements.md#browsers).  

## Salli JavaScript Business Centralista

*Ongelma:*

Jos selain ei salli JavaScriptiä, näet osoite rivillä **Notsupported/DisabledJavaScript**-ilmoituksen ja **HTTP-virhe 404.0 – Ei löydy** -sanoman yritettäessä avata [!INCLUDE[prod_short](includes/prod_short.md)]ia ja 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Korjaus:*

1. Siirry Microsoft Edgessä kohtaan**Asetukset** > **Evästeet ja sivuston käyttöoikeudet** > **JavaScript**.
2. Tee jompikumpi seuraavista vaiheista. Valitse organisaatiosi suosittelema vaihe:

    - Siirrä **Sallittu**-valitsin vasemmalle (pois käytöstä). Valitse sitten **Lisää** ja kirjoita [!INCLUDE[prod_short](includes/prod_short.md)]in osoite (URL-osoite) **Sivusto**-ruutuun. Valitse **Lisää**, kun olet valmis.
    - Siirrä **Sallittu**-valitsin oikealle (käytössä).

## Salli evästeet Business Centralista

*Ongelma:*

Jos selain ei salli evästeitä, saat seuraavan virheilmoituksen:

**Sivua ei valitettavasti löytynyt. Tarkista osoite ja yritä uudelleen.** 

*Korjaus:*

1. Siirry Microsoft Edgessä kohtaan **Asetukset** > **Evästeet ja sivuston käyttöoikeudet** > **Evästeet ja sivuston tiedot**.
2. Siirrä **Salli sivustojen tallentaa ja lukea evästetietoja** -valitsin oikealle (päällä).  

## <a name="popup"></a>Salli ponnahdusikkunat Business Centralista

[!INCLUDE[prod_short](includes/prod_short.md)] integroituu useisiin tuotteisiin. Joissakin tapauksissa, kuten Microsoft Teamsin kanssa, [!INCLUDE[prod_short](includes/prod_short.md)] avaa tai "ponnauttaa" ponnahdusikkunan tuotteen sisällä. Tämä ominaisuus edellyttää, että selain sallii ponnahdusikkunat [!INCLUDE[prod_short](includes/prod_short.md)]ista.

*Ongelma:*

Jos [!INCLUDE[prod_short](includes/prod_short.md)]in ponnahdusikkunat estetään, näyttöön tulee seuraavankaltainen sanoma:

**Jokin meni pieleen. Selaimesi saattaa estää Business Centralin tarvitsemat ponnahdusikkunat.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Korjaus:*

1. Siirry Microsoft Edgessä kohtaan **Asetukset** > **Evästeet ja sivuston käyttöoikeudet** > **Ponnahdusikkunat ja uudelleenohjaukset**.
2. Siirrä **Estetty**-valitsin oikealle (käytössä).
3. Valitse **Lisää**. Kirjoita **Sivusto**- ruutuun `https://businesscentral.dynamics.com` ja valitse sitten **Lisää**.

## Katso myös

[Vianetsintä – Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]