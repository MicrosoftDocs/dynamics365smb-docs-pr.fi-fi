---
title: Nykyisen käyttäjän perusasetusten muuttaminen
description: Opi muuttamaan joitakin Business Centralin perusasetuksia, kuten rooliasi ja roolikeskusta, yritystä, työpäivämäärää sekä aikavyöhykkeitä.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date, decimal separator
ms.search.form: 9022, 9019, 9027, 9020, 9026, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: f466a12898422fb7c936972f0874d38ab2a6ab4b
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515951"
---
# <a name="change-basic-settings"></a>Perusasetusten muuttaminen

Voit tarkastella **Omat asetukset** -sivulla [!INCLUDE[prod_short](includes/prod_short.md)]in perusasetuksia ja muuttaa niitä. Tekemäsi muutokset vaikuttavat vain omaan työtilaasi; ei muiden käyttäjien työtiloihin.  

## <a name="role"></a><a name="role-center"></a>Rooli

Rooli määrittää aloitussivun, joka on suunniteltu organisaation tiettyä roolia varten. Roolin mukaan aloitussivu tai roolikeskus antaa yleiskuvan yrityksestä, osastosta tai henkilökohtaisista tehtävistä. Se auttaa myös siirtymään päivittäisten tehtävien välillä ja löytämään työt, jotka on määritetty sinulle.

* Yläreunan siirtymisvalikon avulla voit siirtyä asiakkaiden, toimittajien, nimikkeiden ja muiden tärkeiden tietoluetteloiden välillä. Vastaavasti toimintojen avulla voi aloittaa tehtävät, kuten luoda uuden myyntilaskun suoraan aloitussivulla.

* Keskellä on nykyiset tiedot näyttävä **Toiminnot**-alue, jota napsauttamalla tai napauttamalla voi tarkastella tietoja lähemmin. Suorituskykyilmaisimet (tunnusluvut) voidaan määrittää niin, että ne näyttävät visuaalisesti esimerkiksi kassavirran tai tuottojen ja kulujen valitun kaavion. Voit luoda aloitussivulla myös suosikkiasiakkaiden luettelon niitä yritysasiakkaita varten, joiden kanssa käyt kauppaa usein tai jotka vaativat erityishuomiota.

### <a name="to-change-the-role"></a>Roolin vaihtaminen

Oletusrooli on **Liiketoimintajohtaja**, mutta voit valita toisen roolin, jotta saat käyttöösi tarpeitasi paremmin vastaavan roolikeskuksen.  

1. Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset** -toiminto.
2. Valitse **Omat asetukset** -sivun **Roolikeskus**-kentässä oletusarvoisesti käytettävä rooli. Valitse esimerkiksi **Kirjanpitäjä**.
3. Valitse **OK**-painike.

## <a name="company"></a><a name="company"></a>Oma yritys

Yritystoiminnot [!INCLUDE[prod_short](includes/prod_short.md)]in tietojen säilönä. Tietokannassa voi olla useita yrityksiä. Kerralla on kuitenkin mahdollista valita vain yksi yritys.

Oletusyrityksen nimi on CRONUS, ja se sisältää vain esittelytietoja. Voit luoda mukautetuilla tiedoilla uuden yrityksen. Lisätietoa on kohdassa [Uusien yritysten luominen](about-new-company.md).

### <a name="to-change-the-company-name"></a>Yrityksen nimen muuttaminen

Yrityksen nimi näkyy aina vasemmassa yläkulmassa. Se on myös toiminto, jonka valitsemalla voit palata roolikeskukseen. Tämän nimen voi muuttaa **Yrityksen tiedot** -sivulla.

1. Valitse ![Hammaspyörä-kuvake, joka avaa Asetukset-valikon.](media/ui-experience/settings_icon_small.png) -kuvake ja valitse sitten **Yrityksen tiedot** -toiminto.
2. Anna uuden yrityksen nimi **Nimi**-kentässä.
3. Poistu sivulta. Järjestelmä käynnistyy uudelleen ja uusi yritys näkyy vasemmassa yläkulmassa.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>Yrityksen tietojen nopea käyttäminen näyttämällä yrityksen tunnus

Voit lisätä oikeaan yläkulmaan mukautetun tunnuksen, jonka valitsemalla voit katsoa nopeasti yrityksen nimen ja vuokraajan tiedot ponnahdusruudussa. Yrityksen merkki on hyödyllinen myös silloin , kun [!INCLUDE[prod_short](includes/prod_short.md)] on upotettu toiseen sovellukseen, kuten Microsoft Teamsiin tai johonkin muuhun verkkosovellukseen. Näissä tapauksissa, koska [!INCLUDE[web_client](includes/web_client.md)] näyttää vähemmän ympäröiviä kontekstuaalisia tietoja, yrityksen merkki toimii ainoana tapana määrittää, mihin yritykseen tai ympäristöön tietue kuuluu.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yrityksen tiedot** ja valitse sitten vastaava linkki.
2. Täytä **Yrityksen tunnus**-pikavälilehden kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Jos yrityksen tunnus on määritetty, et voi muuttaa yrityksen nimeä kohdassa [Yrityksen nimen muuttaminen](ui-change-basic-settings.md#to-change-the-company-name) kuvatulla tavalla.

## <a name="work-date"></a><a name="work-date"></a>Käsittelypäivämäärä
Eniten käytetty käsittelypäivämäärä on kuluvan päivän päivämäärä. Saatat joutua muuttamaan käsittelypäivämäärän väliaikaisesti, jotta voit suorittaa tehtäviä, kuten sellaisten tapahtumien täydentäminen, joiden päivämäärä ei ole kuluvan päivän päivämäärä.

> [!TIP]  
> Voit antaa kuluvan päivän päivämäärän nopeasti kaikissa päivämäärääkentissä kirjoittamalla kenttään **t**. Voit antaa käsittelypäivämäärän nopeasti kirjoittamalla **k**, joka on **Omat asetukset** -sivun **Käsittelypvm**-kentän arvo.

> [!IMPORTANT]  
> Jos olet muuttanut käsittelypäivämäärän ja kirjaudut ulos tai vaihdat toiseen yritykseen, käsittelypäivämäärä palautuu oletuskäsittelypäivämääräksi. Kun sitten kirjaudut seuraavan kerran sisään ja vaihdat takaisin alkuperäiseen yritykseen, käsittelypäivämäärä on ehkä määritettävä uudelleen.

### <a name="work-date-indication"></a>Käsittelypäivämäärän ilmaiseminen

Käsittelypäivämäärä on tärkeä sivuilla, joita voi muokata. Aina kun käsittelypäivämäärää ei ole määritetty muokattavalla sivulla kuluvan päivän päivämäärään, sivulla näkyy kahdenlaisia ilmaisimia:

* Sivun yläosassa näkyvä muistutus ilmaisee, mikä päivämäärä on määritetty käsittelypäivämääräksi. Muistutuksessa on suora linkki **Omat asetukset** -sivun käsittelypäivämääräasetukseen, joten voit tarvittaessa muuttaa päivämäärän. Muistutuksessa voi valita myös muistutuksen hylkäämisen, jolloin se ei enää näy istunnon aikana. Muistutus tulee taas näkyviin, kun kirjaudut seuraavan kerran, ellet muuta käsittelypäivämäärää kuluvaksi päiväksi.

* Jos muistutus hylätään, käsittelypäivämäärä näkyy sivun otsikossa.  

Jos nykyistä päivää (kuluva päivää) ei ole määritetty käsittelypäivämääräksi, nykyinen käsittelypäivämäärä näkyy niiden kaikkien sivujen vasemmassa yläkulmassa, joissa tietoja voidaan muokata.

## <a name="region"></a><a name="region"></a> Alue

**Alue**-asetus määrittää, miten päivämäärät, ajat, luvut ja valuutat näkyvät tai miten ne on muotoiltu. Se määrittää myös, mitä merkkiä käytetään desimaalierottimena, kun käytetään numeronäppäimistöä tietojen syöttämiseen. Lisätietoja on kohdassa [Tietojen syöttäminen](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a> Kieli

Muuttaa näyttökielen. Tämä kenttä näkyy vain, kun useita kieliä voi valita.

Alkuperäinen kieli määräytyy joko järjestelmänvalvojan asettamien tai selaimen asetusten mukaan, kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen. Määrittämääsi kieltä käytetään kaikissa laitteissa, joista kirjaudut, esimerkiksi puhelimessa ja tabletissa.

Sovellukseen [!INCLUDE[prod_short](includes/prod_short.md)] voi asentaa lisäkieliä AppSourcesta. Kaikki tuetut näyttökielet näkyvät luettelossa. Järjestelmänvalvojan on asennettava sopiva kielisovellus vuokraajaan, ennen kuin käyttäjät voivat vaihtaa uuteen kieleen [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

## <a name="time-zone"></a>Aikavyöhyke

Määrittää aikavyöhykkeen, jossa olet. Kun kirjaudut ensimmäisen kerran [!INCLUDE [prod_short](includes/prod_short.md)]iin, aikavyöhyke määritetään yrityksen osoitteen perusteella. Vaihda se, jos se ei vastaa sijaintiasi.  

## <a name="notifications"></a>Ilmoitukset

Valitsemalla *Muuta asetusta, milloin saan ilmoituksia* -linkin voit tarkastella tai muuttaa ilmoituksia, joita saat tietyistä tapahtumista tai tilamuutoksista esimerkiksi silloin, kun olet laskuttamassa asiakasta, jolla on erääntynyttä saldoa, tai kun käytettävissä oleva varasto on pienempi kuin myytävä määrä. Lisätietoja on kohdassa [Ilmoitusten hallinta](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Opetusvinkkejä

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Uusien yritysten luominen](about-new-company.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
