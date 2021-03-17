---
title: Perusasetusten tarkasteleminen ja muokkaaminen | Microsoft Docs
description: Tietoja siitä, miten joitakin perusasetuksia voi muuttaa. Tällaisia perusasetuksia ovat esimerkiksi roolikeskus, yritys ja käsittelypäivämäärä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 61d0ddfd19dede42497607dd0f1897598ac61b80
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573324"
---
# <a name="change-basic-settings"></a>Perusasetusten muuttaminen

Voit tarkastella **Omat asetukset** -sivulla [!INCLUDE[prod_short](includes/prod_short.md)]in perusasetuksia ja muuttaa niitä. Tekemäsi muutokset vaikuttavat vain omaan työtilaasi; ei muiden käyttäjien työtiloihin.  

## <a name="role-center"></a><a name="role-center"></a> Roolikeskus

Roolikeskus edustaa kotisivua tai aloitusnäyttöä. Se on suunniteltu organisaation tietyn roolin tarpeita varten. Roolisi mukaan roolikeskus antaa yleiskuvan yrityksestäsi, osastostasi tai henkilökohtaisista tehtävistäsi. Roolikeskus auttaa myös siirtymään päivittäisten tehtävien välillä ja löytämään työt, jotka on määritetty sinulle.

- Yläreunan siirtymisvalikon avulla voit siirtyä asiakkaiden, toimittajien, nimikkeiden ja muiden tärkeiden tietoluetteloiden välillä. Vastaavasti toimintojen avulla voit aloittaa tehtävät, kuten luoda uuden myyntilaskun suoraan roolikeskuksesta.

- Keskeltä löydät **Aktiviteetit**-alueen, jossa näkyvät tämänhetkiset tiedot. Voit tarkastella yksityiskohtaisempia tietoja valitsemalla tai napauttamalla tietoja. Suorituskykyilmaisimet (tunnusluvut) voidaan määrittää niin, että ne näyttävät visuaalisesti esimerkiksi kassavirran tai tuottojen ja kulujen valitun kaavion. Voit luoda roolikeskuksessa myös suosikkiasiakkaiden luettelon niitä yrityksen asiakkaita varten, joiden kanssa käyt kauppaa usein tai jotka vaativat erityishuomiota.

### <a name="to-change-the-role"></a>Roolin vaihtaminen

Oletusrooli on **Liiketoimintajohtaja**, mutta voit valita toisen roolin, jotta saat käyttöösi tarpeitasi paremmin vastaavan roolikeskuksen.
1. Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset** -toiminto.
2. Valitse **Omat asetukset** -sivun **Roolikeskus**-kentässä oletusarvoisesti käytettävä rooli. Valitse esimerkiksi **Kirjanpitäjä**.
3. Valitse **OK**-painike.

## <a name="company"></a><a name="company"></a>Oma yritys

Yritystoiminnot [!INCLUDE[prod_short](includes/prod_short.md)]in tietojen säilönä. Tietokannassa voi olla useita yrityksiä. Kerralla on kuitenkin mahdollista valita vain yksi yritys.

Oletusyrityksen nimi on CRONUS, ja se sisältää vain esittelytietoja. Voit luoda mukautetuilla tiedoilla uuden yrityksen. Lisätietoa on kohdassa [Uusien yritysten luominen](about-new-company.md).

## <a name="to-change-the-company-name"></a>Yrityksen nimen muuttaminen

Yrityksen nimi näkyy aina vasemmassa yläkulmassa. Se toimii toimintona, jonka avulla voit palata roolikeskukseen. Tämän nimen voi muuttaa **Yrityksen tiedot** -sivulla.

1. Valitse ![Hammaspyöräkuvake Asetukset-valikon avaamista varten](media/ui-experience/settings_icon_small.png) -kuvake ja valitse sitten **Yritystiedot**-toiminto.
2. Anna uuden yrityksen nimi **Nimi**-kentässä.
3. Poistu sivulta. Järjestelmä käynnistyy uudelleen ja uusi yritys näkyy vasemmassa yläkulmassa.

## <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>Yrityksen tietojen nopea käyttäminen näyttämällä yrityksen tunnus

Voit lisätä oikeaan yläkulmaan mukautetun tunnuksen, jonka valitsemalla voit katsoa nopeasti yrityksen nimen ja vuokraajan tiedot ponnahdusruudussa. Yrityksen merkki on hyödyllinen myös silloin , kun [!INCLUDE[prod_short](includes/prod_short.md)] on upotettu toiseen sovellukseen, kuten Microsoft Teamsiin tai johonkin muuhun verkkosovellukseen. Näissä tapauksissa, koska [!INCLUDE[web_client](includes/web_client.md)] näyttää vähemmän ympäröiviä kontekstuaalisia tietoja, yrityksen merkki toimii ainoana tapana määrittää, mihin yritykseen tai ympäristöön tietue kuuluu.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yrityksen tiedot** ja valitse sitten liittyvä linkki.
2. Täytä **Yrityksen tunnus**-pikavälilehden kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Jos yrityksen tunnus on määritetty, et voi muuttaa yrityksen nimeä kohdassa [Yrityksen nimen muuttaminen](ui-change-basic-settings.md#to-change-the-company-name) kuvatulla tavalla.

## <a name="work-date"></a><a name="work-date"></a>Käsittelypvm

Eniten käytetty käsittelypäivämäärä on kuluvan päivän päivämäärä. Saatat joutua muuttamaan käsittelypäivämäärän väliaikaisesti, jotta voit suorittaa tehtäviä, kuten sellaisten tapahtumien täydentäminen, joiden päivämäärä ei ole kuluvan päivän päivämäärä.

> [!TIP]  
> Voit antaa kuluvan päivän päivämäärän nopeasti kaikissa päivämäärääkentissä kirjoittamalla kenttään **t**. Voit antaa käsittelypäivämäärän nopeasti kirjoittamalla **k**, joka on **Omat asetukset** -sivun **Käsittelypvm**-kentän arvo.

> [!IMPORTANT]  
>  Jos olet muuttanut käsittelypäivämäärän ja kirjaudut ulos tai vaihdat toiseen yritykseen, käsittelypäivämäärä palautuu oletuskäsittelypäivämääräksi. Kun sitten kirjaudut seuraavan kerran sisään ja vaihdat takaisin alkuperäiseen yritykseen, käsittelypäivämäärä on ehkä määritettävä uudelleen.

### <a name="work-date-indication"></a>Käsittelypäivämäärän ilmaiseminen

Käsittelypäivämäärä on tärkeä sivuilla, joita voi muokata. Aina kun käsittelypäivämäärää ei ole määritetty muokattavalla sivulla kuluvan päivän päivämäärään, sivulla näkyy kahdenlaisia ilmaisimia:

- Sivun yläosassa näkyvä muistutus ilmaisee, mikä päivämäärä on määritetty käsittelypäivämääräksi. Muistutuksessa on suora linkki **Omat asetukset** -sivun käsittelypäivämääräasetukseen, joten voit tarvittaessa muuttaa päivämäärän. Muistutuksessa voi valita myös muistutuksen hylkäämisen, jolloin se ei enää näy istunnon aikana. Muistutus tulee taas näkyviin, kun kirjaudut seuraavan kerran, ellet muuta käsittelypäivämäärää kuluvaksi päiväksi.

- Jos muistutus hylätään, käsittelypäivämäärä näkyy sivun otsikossa.  

Jos nykyistä päivää (kuluva päivää) ei ole määritetty käsittelypäivämääräksi, nykyinen käsittelypäivämäärä näkyy niiden kaikkien sivujen vasemmassa yläkulmassa, joissa tietoja voidaan muokata.

## <a name="region"></a><a name="region"></a> Alue

**Alue**-asetus määrittää, miten päivämäärät, ajat, luvut ja valuutat näkyvät tai miten ne on muotoiltu.

## <a name="language"></a><a name="language"></a> Kieli

Muuttaa näyttökielen. Tämä kenttä näkyy vain, kun useita kieliä voi valita.

Alkuperäinen kieli määräytyy joko järjestelmänvalvojan asettamien tai selaimen asetusten mukaan, kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen. Määrittämääsi kieltä käytetään kaikissa laitteissa, joista kirjaudut, esimerkiksi puhelimessa ja tabletissa.

Sovellukseen [!INCLUDE[prod_short](includes/prod_short.md)] voi asentaa lisäkieliä AppSourcesta. Kaikki tuetut näyttökielet näkyvät luettelossa. Järjestelmänvalvojan on asennettava asiaankuuluva kielisovellus, ennen kuin käyttäjät voivat vaihtaa uuteen kieleen sovelluksessa [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="changing-when-i-receive-notifications"></a>Ilmoitusten vastaanoton ajankohta-asetusten muuttaminen

Valitsemalla tämän linkin voit tarkastella tai muuttaa ilmoituksia, joita saat tietyistä tapahtumista tai tilan muutoksista. Voit esimerkiksi saada ilmoituksen, kun olet laskuttamassa asiakasta, jolla on erääntynyttä saldoa, tai kun käytettävissä oleva varasto on pienempi kuin myytävä määrä. Lisätietoja on kohdassa [Ilmoitusten hallinta](ui-smart-notifications.md).

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Uusien yritysten luominen](about-new-company.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]