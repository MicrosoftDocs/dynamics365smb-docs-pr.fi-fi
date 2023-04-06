---
title: Business Central -tietueiden jakaminen Microsoft Teamsissa
description: Microsoft Teamsin Business Central -sovelluksen käyttäminen.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 09/22/2022
ms.author: jswymer
---

# Business Central -tietueiden ja sivulinkkien jakaminen Microsoft Teamsissa

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa pari tapaa jakaa tietoja Business Centralista suoraan Microsoft Teams -keskusteluun:

<!-- 
## Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Kun [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus on asennettu Teamsiin, voit sisällyttää Teams-keskusteluun Business Central -tietueen vuorovaikutteisen kortin.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Kun [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus on asennettu tai sitä ei ole asennettu, voit jakaa linkin Business Centralin sivuilta Teams-keskusteluun.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

Seuraavissa osissa käsitellään eri tapoja tarkemmin.

## Sisällytä ja näytä Business Central -kortti Teams-keskustelussa

Teamsin Business Central -sovelluksen avulla voit kopioida linkin mistä tahansa Business Central -tietueesta, kuten asiakkaasta tai myyntitilauksesta, ja liittää linkin Teams-keskusteluun. Sovellus muodostaa yhteyden Microsoft Teamsista yritystietoihin [!INCLUDE [prod_short](includes/prod_short.md)]\.issa Linkki laajentuu sen kompaktiksi ja vuorovaikutteiseksi kortiksi, joka näyttää tietoja tietueesta. Keskustelun aikana sinä ja työtoverisi voitte tarkastella lisätietoja tietueesta, muokata tietoja ja toimia&mdash;poistumatta Teamsista.

[![Teamsin ja Business Centralin integrointi.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### Vaatimukset

- Sinulla on Microsoft Teamsin käyttöoikeus.
- Olet asentanut [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen Teamsiin. Lisätietoja, katso [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsiin](across-install-app-for-teams.md)

> [!NOTE]
> Kaikki Teams-keskustelun osallistujat voivat tarkastella keskusteluun lähetettäviä Business Central -tietueiden kortteja. Mutta halutessaan tarkastella lisätietoja tietueista käyttämällä **Tiedot**- tai **Ponnahdusikkuna**-painikkeita, he tarvitsevat käyttöoikeuden [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan. Lisätietoja on kohdassa [Microsoft Teams -integraation hallinta](admin-teams-integration.md#minimum-requirements-1).

### Sisällytä Business Central -kortti Teams-keskusteluun

1. Kirjaudu [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan käyttämällä selainta.
2. Avaa tietue, jonka haluat jakaa.

    Sovellus on suunniteltu näyttämään kortti lähes mitä tahansa [!INCLUDE [prod_short](includes/prod_short.md)] -sivun tyyppiä varten. Se tarjoaa kuitenkin parhaan käyttökokemuksen silloin, kun käytetään sivuja, joilla näkyy yksittäinen tietue, esimerkiksi nimike, asiakas tai myyntitilaus.
3. Kopioi linkki sivulle.

    Linkin voi kopioida kahdella tavalla. Helpoin ja suosituin tapa on valita **Jaa** ![Jaa-kuvake Business Centralissa](media/share-icon.png) > **Kopioi linkki**. Toinen tapa on kopioida koko URL-osoite suoraan selaimen osoiteriviltä.

    [![Business Centralin URL-osoitteen kopioiminen selaimesta.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Siirry Teamsiin ja aloita keskustelu, joka voi olla keskustelu henkilön, henkilöryhmän tai tiimikanavan kanssa.
5. Liitä linkki (URL-osoite) viestiruutuun, johon kirjoitat viestin.

    ![Liitä Business Centralin URL-osoite Teamsiin.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Jos saat viestin, kuten: *Business Central haluaa näyttää esikatselun tästä linkistä.* se tarkoittaa, että et ole asentanut Teamsin Business Central -sovellusta. Voit asentaa sovelluksen valitsemalla **Näytä esikatselu** ja noudattamalla ohjeita.
6. Kun liität linkin keskusteluun ensimmäistä kertaa, sinua pyydetään kirjautumaan sisään [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan ja antamaan suostumus siihen, että sovellus hakee tiedot. Seuraa vain näytön ohjeita.

    > [!NOTE]
    > Tämä vaihe tarvitsee tehdä vain kerran.
7. Odota hetki, kun kortti luodaan sanomaruutuun.
8. Kun kortti tulee näkyviin, tarkista kortin sisältö huolellisesti, ennen kuin lähetät viestin. Tämä vaihe on tärkeä, koska kun lähetät viestin, kaikki keskusteluun osallistuvat voivat nähdä kortin.
9. Jos kortti näyttää hyvältä, lähetä se keskusteluun valitsemalla **Lähetä**.

    > [!TIP]
    > Kun kortti tulee näyttöön ja ennen kuin valitset **Lähetä**, voit halutessasi poistaa liitetyn URL-osoitteen.
10. Jos haluat tarkastella lisätietoja tai tehdä kortissa näytettyyn tietueeseen muutoksia, valitse **Tiedot**. Lisätietoja on seuraavassa osassa.

### Näytä kortin tiedot

Kun kortti on lähetetty keskusteluun, kaikki osallistujat, joilla on [asianmukaiset käyttöoikeudet](admin-teams-integration.md#permissions), voivat valita **Tiedot** ja avata ikkunan, jossa näkyy lisätietoja tietueesta&mdash;ja mahdollisesti tehdä muutoksia tietueeseen. Ei ole merkitystä, oletko kortin lähettäjä vai vastaanottaja. **Tiedot**-ominaisuudesta on hyötyä erityisesti vastaanottajille, koska se antaa heille nopeasti ytimekkäitä ja kohdennettuja tietoja.

Tiedot-ikkuna muistuttaa siitä, mitä näet [!INCLUDE [prod_short](includes/prod_short.md)]issa, mutta se on keskittynyt sivuun tai tietueeseen, josta kortti sisältää tietoja. Kun olet lopettanut muutosten tarkastelemisen ja tekemisen, sulje ikkuna palataksesi Teams-keskusteluun.

Seuraavassa on muutamia asioita, jotka pitää muistaa, kun käsittelet kortin tietoja:

- Avatakseen kortin tiedot käyttäjillä on oltava sivun ja sen tietojen lukuoikeus [!INCLUDE [prod_short](includes/prod_short.md)]\.issa
- Teams-keskustelujen kortteja ei päivitetä automaattisesti muutoksien mukaan. Tiedot-ikkunan tietueeseen tallentamasi muutokset tallennetaan [!INCLUDE [prod_short](includes/prod_short.md)]\.iin Mutta Teamsissa kortti ei näytä muutoksia keskustelussa, ennen kuin liität linkin uudelleen.

Lisätietoja korttien ja korttiietojen käyttämisestä on kohdassa [Teams – usein kysytyt kysymykset](teams-faq.md).

## <a name="share-link"></a>Jaa sivun linkki Business Centralista Teamsiin

Suoraan useimmista kokoelmasivuista, kuten **Kohteet**-sivusta, ja Tiedot-sivuista, kuten **Kohteet**-kortista, voit lähettää linkin sivulle Teams-keskusteluiden tietyille vastaanottajille. Voit esimerkiksi jakaa linkin tietueiden suodatettuun näkymään. Vastaanottajat voivat sitten napsauttamalla linkkiä avata sivun [!INCLUDE [prod_short](includes/prod_short.md)]\.issa

[![Kortilla näkyvä Jaa-valikko.](media/teams-share-link-v2.png "Kortilla näkyvä Jaa-valikko.")](media/teams-share-link-v2.png#lightbox)

### Vaatimukset

- Sinulla on Microsoft Teamsin käyttöoikeus.
- (Valinnainen) Olet asentanut [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen Teamsiin. 

  Kun sovellus on asennettu, linkin mukana lähettämäsi viestit sisältävät myös pienikokoisen kortin sivua varten. Lisätietoja sovelluksen asentamisesta on kohdassa [[!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen Microsoft Teamsille](across-install-app-for-teams.md).

### Linkin jakaminen

1. Avaa [!INCLUDE [prod_short](includes/prod_short.md)]\,issa jaettava sivu.
2. Valitse sivun yläosasta ![!Jaa muihin sovelluksiin -toiminto sivuilla.](media/share-icon.png) -kuvake ja **Jaa Teamsiin**.
3. Jos sinulta kysytään, kirjaudu Teamsiin käyttäen käyttäjänimeäsi ja salasanaasi.
4. Kirjoita **Jaa Teamsiin** -sivulla henkilön, ryhmän tai kanavan nimi, jolle haluat lähettää viestin.
5. Sanomaruutu sisältää linkin sivulle. Jos Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus on asennettu, linkitetylle tietueelle tai sivulle tuleva kortti tulee näkyviin myös sanomaruutuun.

   Lisää halutessasi lisätietoja ja valitse sitten **Jaa**.
6. Linkki on nyt jaettu. Jos haluat siirtyä keskusteluun, valitse **Siirry Teamsiin**.

## Katso myös

[Business Centralin ja Microsoft Teamsin integraation yleiskatsaus](across-teams-overview.md)  
[Microsoft Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen](across-install-app-for-teams.md)  
[Teams – usein kysytyt kysymykset](teams-faq.md)  
[Asiakkaiden, toimittajien ja muiden yhteyshenkilöiden hakeminen Microsoft Teamsista](across-search-contacts-teams.md)  
[Yrityksen ja muiden asetusten muuttaminen Teamsissa](across-teams-settings.md)  
[Vianetsintä – Teams](admin-teams-troubleshooting.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
