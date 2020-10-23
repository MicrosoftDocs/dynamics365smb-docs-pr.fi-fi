---
title: Perusasetusten tarkasteleminen ja muokkaaminen | Microsoft Docs
description: Tietoja siitä, miten joitakin perusasetuksia voi muuttaa. Tällaisia perusasetuksia ovat esimerkiksi roolikeskus, yritys ja käsittelypäivämäärä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f98cd6423b67fd9bbcc6081d06eca4cb21e81c7
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912669"
---
# <a name="change-basic-settings"></a>Perusasetusten muuttaminen

Voit tarkastella **Omat asetukset** -sivulla [!INCLUDE[d365fin](includes/d365fin_md.md)]in perusasetuksia ja muuttaa niitä. Tekemäsi muutokset vaikuttavat vain omaan työtilaasi; ei muiden käyttäjien työtiloihin.  

## <a name="role-center"></a><a name="role-center"></a> Roolikeskus
Roolikeskus edustaa kotisivua eli aloitussivua, joka on suunniteltu organisaation tiettyä roolia varten. Roolisi mukaan roolikeskus antaa yleiskuvan yrityksestäsi, osastostasi tai henkilökohtaisista tehtävistäsi. Se auttaa myös siirtymään päivittäisten tehtävien välillä ja löytämään työt, jotka on määritetty sinulle.

-   Yläreunan siirtymisvalikon avulla voit siirtyä asiakkaiden, toimittajien, nimikkeiden ja muiden tärkeiden tietoluetteloiden välillä. Vastaavasti toimintojen avulla voit aloittaa tehtävät, kuten luoda uuden myyntilaskun suoraan roolikeskuksesta.

-   Keskellä on nykyiset tiedot näyttävä **Toiminnot**-alue, jota napsauttamalla tai napauttamalla voi tarkastella tietoja lähemmin. Suorituskykyilmaisimet (tunnusluvut) voidaan määrittää niin, että ne näyttävät visuaalisesti esimerkiksi kassavirran tai tuottojen ja kulujen valitun kaavion. Voit luoda roolikeskuksessa myös suosikkiasiakkaiden luettelon niitä yrityksen asiakkaita varten, joiden kanssa käyt kauppaa usein tai jotka vaativat erityishuomiota.

### <a name="to-change-the-role"></a>Roolin vaihtaminen
Oletusrooli on **Liiketoimintajohtaja**, mutta voit valita toisen roolin, jotta saat käyttöösi tarpeitasi paremmin vastaavan roolikeskuksen.
1. Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset** -toiminto.
2. Valitse **Omat asetukset** -sivun **Roolikeskus**-kentässä oletusarvoisesti käytettävä rooli. Valitse esimerkiksi **Kirjanpitäjä**.
3. Valitse **OK**-painike.

## <a name="company"></a><a name="company"></a>Oma yritys
Yritystoiminnot [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen säilönä. Tietokannassa voi olla useita yrityksiä. Kerralla on kuitenkin mahdollista valita vain yksi yritys.

Oletusyrityksen nimi on CRONUS, ja se sisältää vain esittelytietoja. Voit luoda mukautetuilla tiedoilla uuden yrityksen. Lisätietoa on kohdassa [Uusien yritysten luominen](about-new-company.md).

## <a name="to-change-the-company-name"></a>Yrityksen nimen muuttaminen
Yrityksen nimi näkyy aina vasemmassa yläkulmassa. Se on myös toiminto, jonka valitsemalla voit palata roolikeskukseen. Tämän nimen voi muuttaa **Yrityksen tiedot** -sivulla.

1. Valitse ![Hammaspyöräkuvake Asetukset-valikon avaamista varten](media/ui-experience/settings_icon_small.png) -kuvake ja valitse sitten **Yritystiedot**-toiminto.
2. Anna uuden yrityksen nimi **Nimi**-kentässä.
3. Poistu sivulta. Järjestelmä käynnistyy uudelleen ja uusi yritys näkyy vasemmassa yläkulmassa.

## <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a>Yrityksen tietojen nopea käyttäminen näyttämällä yrityksen tunnus  
Voit lisätä oikeaan yläkulmaan mukautetun tunnuksen, jonka valitsemalla voit katsoa nopeasti yrityksen nimen ja vuokraajan tiedot ponnahdusruudussa.

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
Jos käsittelypäivämääräksi ei ole määritetty kuluvan päivän päivämäärää, sivuilla näkyy kaksi ilmaisintyyppiä, joita voidaan muokata ja joissa käsittelypäivämäärä on ratkaiseva:

* Sivun yläosassa näkyvä muistutus ilmaisee, mikä päivämäärä on määritetty käsittelypäivämääräksi. Muistutuksessa on suora linkki **Omat asetukset** -sivun käsittelypäivämääräasetukseen, joten voit tarvittaessa muuttaa päivämäärän. Muistutuksessa voi valita myös muistutuksen hylkäämisen, jolloin se ei enää näy istunnon aikana. Muistutus tulee taas näkyviin, kun kirjaudut seuraavan kerran, ellet muuta käsittelypäivämäärää kuluvaksi päiväksi.

* Jos muistutus hylätään, käsittelypäivämäärä näkyy sivun otsikossa.  

Jos nykyistä päivää (kuluva päivää) ei ole määritetty käsittelypäivämääräksi, nykyinen käsittelypäivämäärä näytetään niiden kaikkien sivujen vasemmassa yläkulmassa, joissa tietoja voidaan muokata.

## <a name="region"></a><a name="region"></a> Alue

**Alue**-asetus määrittää, miten päivämäärät, ajat, luvut ja valuutat näkyvät tai miten ne on muotoiltu.

## <a name="language"></a><a name="language"></a> Kieli
Muuttaa näyttökielen. Tämä kenttä näkyy vain, kun useita kieliä voi valita.

Alkuperäinen kieli määräytyy joko järjestelmänvalvojan asettamien tai selaimen asetusten mukaan, kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen. Määrittämääsi kieltä käytetään kaikissa laitteissa, joista kirjaudut, esimerkiksi puhelimessa ja tabletissa.

Sovellukseen [!INCLUDE[prodshort](includes/prodshort.md)] voi asentaa lisäkieliä AppSourcesta. Kaikki tuetut näyttökielet näkyvät luettelossa. Järjestelmänvalvojan on asennettava asiaankuuluva kielisovellus vuokraajaan, ennen kuin käyttäjät voivat vaihtaa uuteen kieleen sovelluksessa [!INCLUDE[prodshort](includes/prodshort.md)].  

## <a name="changing-when-i-receive-notifications"></a>Ilmoitusten vastaanoton ajankohta-asetusten muuttaminen
Valitsemalla tämän linkin voit tarkastella tai muuttaa ilmoituksia, joita saat tietyistä tapahtumista tai tilamuutoksista esimerkiksi silloin, kun olet laskuttamassa asiakasta, jolla on erääntynyttä saldoa, tai kun käytettävissä oleva varasto on pienempi kuin myytävä määrä. Lisätietoja on kohdassa [Ilmoitusten hallinta](ui-smart-notifications.md).

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Uusien yritysten luominen](about-new-company.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
