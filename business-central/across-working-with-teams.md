---
title: Business Central -tietojen käyttäminen Microsoft Teamsissa | Microsoft Docs
description: Microsoft Teamsin Business Central -sovelluksen käyttäminen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: e20208d50eb65f1a92e6661396bf53007ab88eb8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786880"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Business Centralin tietojen käyttäminen Microsoft Teamsissa

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa sovelluksen, joka yhdistää Microsoft Teamsin yrityksen tietoihin [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa, joten voit jakaa tiedot nopeasti tiimin jäsenten kesken ja reagoida nopeammin kyselyihin. Tässä artikkelissa kerrotaan, miten sovellusta käytetään [!INCLUDE [prod_short](includes/prod_short.md)] -tietojen jakamiseen työtovereiden kanssa Teams-keskusteluissa.

## <a name="overview"></a>Yleiskuvaus

[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen avulla voit:

- Kopioida linkin mihin tahansa Business Central -tietueeseen ja liittää sen Teams-keskusteluun, jonka haluat jakaa työtovereidesi kanssa. Sovellus laajentaa linkin kompaktiksi ja vuorovaikutteiseksi kortiksi, joka näyttää tietoja tietueesta.
- Keskustelun aikana sinä ja työtoverisi voitte tarkastella lisätietoja tietueesta, muokata tietoja ja toimia – poistumatta Teamsista.

[![Teamsin ja Business Centralin integrointi](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Vaatimukset

- Sinulla on Microsoft Teamsin käyttöoikeus.
- Olet asentanut [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen Teamsiin. Lisätietoja, katso [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsiin](across-install-app-for-teams.md)

> [!NOTE]
> Kaikki Teams-keskustelun osallistujat voivat tarkastella keskusteluun lähetettäviä Business Central -tietueiden kortteja. Mutta halutessaan tarkastella lisätietoja tietueista käyttämällä **Tiedot**- tai **Ponnahdusikkuna**-painikkeita, he tarvitsevat käyttöoikeuden [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan. Lisätietoja on kohdassa [Microsoft Teams -integraation hallinta](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Sisällytä Business Central -kortti Teams-keskusteluun

1. Kirjaudu [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan käyttämällä selainta.
2. Avaa tietue, jonka haluat jakaa.

    Sovellus on suunniteltu näyttämään korttityyppisivut [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmasta. Avaa siis sivu, jossa näkyy yksittäinen tietue, esimerkiksi nimike, asiakas tai myyntitilaus. Sitä ei voi käyttää roolikeskuksissa tai sivuissa, jotka näyttävät useita tietueita luettelossa.

3. Kopioi koko URL-osoite selaimen osoiteriviltä.

   ![Business Centralin URL-osoitteen kopioiminen selaimesta](media/teams-url-v2.png)
4. Siirry Teamsiin ja aloita keskustelu, joka voi olla keskustelu henkilön, henkilöryhmän tai tiimikanavan kanssa.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Liitä URL-osoite viestiruutuun, johon kirjoitat viestin.

   ![Liitä Business Central-URL-osoite Teamsiin](media/teams-paste-url-v2.png)
6. Kun liität linkin keskusteluun ensimmäistä kertaa, sinua pyydetään kirjautumaan sisään [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan ja antamaan suostumus siihen, että sovellus hakee tiedot. Seuraa vain näytön ohjeita.

    > [!NOTE]
    > Tämä vaihe tarvitsee tehdä vain kerran.

7. Odota hetki, kun kortti luodaan sanomaruutuun.

8. Kun kortti tulee näkyviin, tarkista kortin sisältö huolellisesti, ennen kuin lähetät viestin. Tämä vaihe on tärkeä, koska kun lähetät viestin, kaikki keskusteluun osallistuvat voivat nähdä kortin.

9. Jos kortti näyttää hyvältä, lähetä se keskusteluun valitsemalla **Lähetä**.

    > [!TIP]
    > Kun kortti tulee näyttöön ja ennen kuin valitset **Lähetä**, voit halutessasi poistaa liitetyn URL-osoitteen.

10. Jos haluat tarkastella lisätietoja tai tehdä kortissa näytettyyn tietueeseen muutoksia, valitse **Tiedot**. Lisätietoja on seuraavassa osassa.

## <a name="view-card-details"></a>Näytä kortin tiedot

Kun kortti on lähetetty keskusteluun, kaikki osallistujat, joilla on [asianmukaiset käyttöoikeudet](admin-teams-integration.md#permissions), voivat valita **Tiedot** ja avata ikkunan, jossa näkyy lisätietoja tietueesta – ja mahdollisesti tehdä muutoksia tietueeseen. Ei ole merkitystä, oletko kortin lähettäjä vai vastaanottaja. **Tiedot**-ominaisuudesta on hyötyä erityisesti vastaanottajille, koska se antaa heille nopeasti ytimekkäitä ja kohdennettuja tietoja tietueesta tarvitsematta tutkia koko tietuetta.

Tietoikkuna on samankaltainen kuin [!INCLUDE [prod_short](includes/prod_short.md)] -tietueen näkymä. Mutta sitä on hieman muokattu Teamsia varten. Kun olet lopettanut muutosten tarkastelemisen ja tekemisen, sulje ikkuna palataksesi Teams-keskusteluun.

Seuraavassa on muutamia asioita, jotka pitää muistaa, kun käsittelet kortin tietoja:

- Avatakseen kortin tiedot käyttäjillä on oltava sivun ja sen tietojen lukuoikeus [!INCLUDE [prod_short](includes/prod_short.md)]issa.
- Teams-keskustelujen kortteja ei päivitetä automaattisesti muutoksien mukaan. Tiedot-ikkunan tietueeseen tallentamasi muutokset tallennetaan [!INCLUDE [prod_short](includes/prod_short.md)]iin. Mutta Teamsissa kortti ei näytä muutoksia keskustelussa, ennen kuin liität linkin uudelleen.

Lisätietoja korttien ja korttiietojen käyttämisestä on kohdassa [Teams – usein kysytyt kysymykset](teams-faq.md).

## <a name="see-also"></a>Katso myös

[Business Centralin ja Microsoft Teamsin integraation yleiskatsaus](across-teams-overview.md)  
[Asenna [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)  
[Teams – usein kysytyt kysymykset](teams-faq.md)  
[Vianetsintä – Teams](admin-teams-troubleshooting.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]