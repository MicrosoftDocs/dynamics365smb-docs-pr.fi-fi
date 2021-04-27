---
title: Lakisääteisten ilmoitusten lähettäminen | Microsoft Docs
description: Jos olet tietoinen uudesta lainsäädännöstä, jota mielestäsi on tuettava Business Centralissa, voit lähettää lakisääteisen ilmoituksen tuotetiimille tämän oppaan ohjeiden avulla.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: soalex
ms.openlocfilehash: f75e75cbc220e673fe0e841f8a1f1f04b247bb88
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784838"
---
# <a name="submit-alerts-about-countryregion-specific-regulatory-features"></a>Maa- tai aluekohtaisten lakisääteisiä ominaisuuksia koskevien ilmoitusten lähettäminen

Voit lähettää lakisääteisiä ilmoituksia Microsoft Dynamics Lifecycle Servicesin (LCS) kautta Dynamicsin lakisääteisten ilmoitusten lähetyspalveluun.  

## <a name="to-submit-a-regulatory-alert-in-lcs"></a>Lakisääteisen ilmoituksen lähettäminen LCS:ssä

1. Siirry sivustoon https://lcs.dynamics.com ja kirjaudu sisään  

    Projektit, joiden käyttöoikeus sinulla on, tulevat näkyviin.

2. Valitse **Lakisääteiset ilmoitukset – maailmanlaajuinen** -projekti.

    Projekti avautuu ja näkyviin tulee erilaisia tähän projektiin liittyviä seikkoja.

3. Valitse **Lisää työkaluja** -kohdan oikealla puolella **Ilmoituspalvelu**.

    Näkyvissä on ilmoitusluettelo, jonka otsikkona on **Dynamicsin lakisääteisen ilmoituksen lähettäminen**.

4. Voit lisätä uuden ilmoituksen napsauttamalla plusmerkkiä **(+)** luettelon yläreunassa.

    Näkyviin tulee opas, jossa ilmoitus luodaan neljässä vaiheessa. Oppaassa on seuraavat vaiheet:
    - Aiemmin luotujen nimikkeiden etsiminen

        Etsi tietoja, joiden arvelet liittyvät luotavaan ilmoitukseen. Jos et saa mitään soveltuvia hakutuloksia, voit valita sivun alareunassa **Lähetä lakisääteinen ilmoitus** -painikkeen ja jatkaa ilmoituksen lähettämistä.
    - Liiketoimintaprosessien liittäminen

        Tämä osa ei liity Dynamics 365 Business Centraliin. Jatka seuraavaan vaiheeseen valitsemalla **Ohita**.
    - Ilmoituksen kuvaus

        Anna soveltuviin kenttiin ilmoitusta koskevat tiedot. Pakolliset kentät on merkitty oppaassa punaisella tähdellä (\*).

        |Kenttä        |Description                               |
        |-------------|------------------------------------------|
        |Otsikko  | Määritä vaikutusalue antamalla kuvaava nimi. Kirjoita esimerkiksi *Muutokset laskuasiakirjaan 1.7.2019 alkaen*. |
        |Description  | Kirjoita lyhyt lainsäädännön kuvaus. Kuvauksen pitäisi keskittyä tuotannonohjaus- eli ERP-toimiin liittyviin ongelmiin, jotta käyttäjät ymmärtävät ylätason vaatimukset lainsäädäntöön tutustumatta.|
        |Maa  | Määritä maa tai alue, jota lainsäädäntö koskee.|
        |Toimiala| Määritä toimiala, jos vaatimus koskee vain tiettyjä toimialoja. Valitse esimerkiksi **julkinen sektori**, **vähittäismyynti** tai **tuotanto**.|
        |Ominaisuusviite  | Tämä ei koske Dynamics 365 Business Centralia, mutta jos sinulla on ominaisuusviite, voit antaa sen. Maakohtainen ominaisuusluettelo on CustomerSource-sivuston [lokalisointiportaalissa](/dynamics/s-e/). |
        |Lainsäädännön voimaantulopäivä  | Määritä päivämäärä, jolloin asiakkaiden on aloitettava lainsäädännön noudattaminen.|
        |Julkishallinnon ilmoituspäivä  | Määritä päivämäärä, jolloin viranomainen ilmoitti muutoksesta.|
        |Viimeisin ilmoituspäivä  | Valitse määräaika, jolloin uusi tai muuttunut raportti on lähetettävä ensimmäisen kerran.|
        |Linkki lainsäädäntöön  | Anna vähintään yksi linkki julkaistuun lainsäädäntöön, tulkintaohjeisiin, käyttöönotto-ohjeisiin tai muihin hyödyllisiin tietoihin, jotka auttavat käyttäjiä ymmärtämään tai toteuttamaan vaatimuksen.|
        |Yrityksen nimi  | Anna ilmoituksen lähettävän henkilön yrityksen nimi.|
        |Kontaktin nimi  | Anna ilmoituksen lähettävän henkilön nimi. |
        |Kontaktin sähköposti  | Anna ilmoituksen lähettävän henkilön sähköpostiosoite.|
        |Liiketoimintaprosessi  | Ohjatussa **ilmoituksen lähetystoiminnossa** valitut liiketoimintaprosessit.|
        |Kommentit  | Anna mahdolliset lisätiedot, jotka auttavat käyttäjiä ymmärtämään tai toteuttamaan vaatimuksen. Tallenna kommentti valitsemalla **Lähetä**. Kommentteja voi lisätä useita, ja ne on lähetettävä erikseen. Kommentit tallennetaan lisäysjärjestyksessä. |
        |Haluan nähdä...  | Valitse **Lataa**-painike ja selaa liitteenä lisättävään tiedostoon. Kun olet valinnut tiedoston, se ladataan ja tulee näkyviin linkitettynä tiedostona. Voit lisätä enintään kolme tiedostoa, joista kunkin koko voi olla 5 Mt. Voit poistaa liitettyjä tiedostoja valitsemalla tiedoston otsikon kohdalla **Poista**. Liitteiden on oltava julkisesti saatavilla olevaa aineistoa. Ne eivät voi olla yksinoikeudellisia eivätkö asiakas- tai kumppanikohtaisia.|

        Lähetä ilmoitus valitsemalla **Lähetä**.

        Jos sinulla ei ole kaikkia tarvittavia tietoja tai et ole vielä valmis lähettämään ilmoitusta, voit tallentaa osittain täytetyn ilmoituksen.

    - Lähetyksen vahvistus

      Kun olet lähettänyt ilmoituksen, saat vahvistuksen, että ilmoituksen lähetys Microsoftille onnistui.

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_long](includes/prod_long.md)]in paikalliset toiminnot](about-localization.md)  
[Kielen ja kielialueen muuttaminen](about-locale-language.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Tervetuloa Business Centraliin](index.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]