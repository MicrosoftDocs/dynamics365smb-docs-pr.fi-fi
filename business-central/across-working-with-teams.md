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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989416"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Business Centralin tietojen käyttäminen Microsoft Teamsissa

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] tarjoaa sovelluksen, joka yhdistää Microsoft Teamsin yrityksen tietoihin [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa, joten voit jakaa tiedot nopeasti tiimin jäsenten kesken ja reagoida nopeammin kyselyihin. Tässä artikkelissa kerrotaan, miten sovellusta käytetään [!INCLUDE [prodshort](includes/prodshort.md)] -tietojen jakamiseen työtovereiden kanssa Teams-keskusteluissa.

## <a name="overview"></a>Yleiskuvaus

[!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen avulla voit:

- Kopioida linkin mihin tahansa Business Central -tietueeseen ja liittää sen Tems-keskusteluun, jonka haluat jakaa työtovereidesi kanssa. Linkki laajentaa sen kompaktiksi ja vuorovaikutteiseksi kortiksi, joka näyttää tietoja tietueesta.
- Keskustelun aikana sinä ja työtoverisi voitte tarkastella lisätietoja tietueesta, muokata tietoja ja toimia - poistumatta Teamsista.

[![Teamsin ja Business Centralin integrointi](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Vaatimukset

- Sinulla on Microsoft Teamsin käyttöoikeus.
- Olet asentanut [!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen Teamsiin. Lisätietoja, katso [[!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen asentaminen Microsoft Teamsiin](across-install-app-for-teams.md)

> [!NOTE]
> Kaikki Teams-keskustelun osallistujat voivat tarkastella keskusteluun lähetettäviä Business Central -tietueiden kortteja. Mutta halutessaan tarkastella lisätietoja tietueista käyttämällä **Tiedot**- tai **Ponnahdusikkuna**-painikkeita, he tarvitsevat käyttöoikeuden [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmaan. Lisätietoja on kohdassa [Microsoft Teams -integraation hallinta](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Sisällytä Business Central -kortti Teams-keskusteluun

1. Kirjaudu [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmaan käyttämällä selainta.
2. Avaa tietue, jonka haluat jakaa.

    Sovellus on suunniteltu näyttämään korttityyppisivut [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmasta. Avaa siis sivu, jossa näkyy yksittäinen tietue, esimerkiksi nimike, asiakas tai myyntitilaus. Sitä ei voi käyttää roolikeskuksissa tai sivuissa, jotka näyttävät useita tietueita luettelossa.

3. Kopioi koko URL-osoite selaimen osoiteriviltä.

   ![Business Centralin URL-osoitteen kopioiminen selaimesta](media/teams-url.png)
4. Siirry Teamsiin ja aloita keskustelu, joka voi olla keskustelu henkilön, henkilöryhmän tai tiimikanavan kanssa.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Liitä URL-osoite ruutuun, johon lisäät viestin.

   ![Liitä Business Central-URL-osoite Teamsiin](media/teams-paste-url.png)
6. Kun liität linkin keskusteluun ensimmäistä kertaa, sinua pyydetään kirjautumaan sisään [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmaan ja antamaan suostumus siihen, että sovellus hakee tiedot. Seuraa vain näytön ohjeita.

    > [!NOTE]
    > Tämä vaihe tarvitsee tehdä vain kerran.

7. Odota hetki, kun kortti luodaan sanomaruutuun.

8. Kun kortti tulee näkyviin, tarkista kortin sisältö huolellisesti, ennen kuin lähetät viestin. Tämä vaihe on tärkeä, koska kun lähetät viestin, kaikki keskusteluun osallistuvat voivat nähdä kortin.

9. Jos kortti näyttää hyvältä, lähetä se keskusteluun valitsemalla **Lähetä**.

    > [!TIP]
    > Kun kortti tulee näyttöön ja ennen kuin valitset **Lähetä**, voit halutessasi poistaa liitetyn URL-osoitteen.

10. Jos haluat tarkastella lisätietoja tai tehdä tietueeseen muutoksia, valitse **Tiedot**.

    Tietosivu muistuttaa sitä, mitä haluat nähdä [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa. Mutta sitä on hieman muokattu Teamsia varten. Kun olet lopettanut muutosten tarkastelemisen ja tekemisen, sulje ikkuna palataksesi Teams-keskusteluun.

    > [!NOTE]
    > Tekemäsi muutokset eivät näy kortissa, ennen kuin seuraavan kerran liität sen linkin keskusteluun.

## <a name="see-also"></a>Katso myös

[Business Centralin ja Microsoft Teamsin integraation yleiskatsaus](across-teams-overview.md)  
[Asenna [!INCLUDE [prodshort](includes/prodshort.md)] -sovellus Microsoft Teamsiin](across-install-app-for-teams.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Käytön aloittaminen](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
