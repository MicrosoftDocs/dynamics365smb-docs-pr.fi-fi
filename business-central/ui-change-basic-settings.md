---
title: Nykyisen käyttäjän perusasetusten muuttaminen
description: 'Opi muuttamaan joitakin Business Centralin perusasetuksia, kuten rooliasi ja roolikeskusta, yritystä, työpäivämäärää sekä aikavyöhykkeitä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/31/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="change-basic-settings"></a>Perusasetusten muuttaminen

Voit tarkastella **Omat asetukset** -sivulla [!INCLUDE[prod_short](includes/prod_short.md)]in perusasetuksia ja muuttaa niitä. Tekemäsi muutokset vaikuttavat vain omaan työtilaasi; ei muiden käyttäjien työtiloihin.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role"></a><a name="role-center"></a>Rooli

Rooli määrittää aloitussivun, joka on suunniteltu organisaation tiettyä roolia varten. Roolin mukaan aloitussivu tai roolikeskus antaa yleiskuvan yrityksestä, osastosta tai henkilökohtaisista tehtävistä. Se auttaa myös siirtymään päivittäisten tehtävien välillä ja löytämään työt, jotka on määritetty sinulle.

* Yläreunan siirtymisvalikon avulla voit siirtyä asiakkaiden, toimittajien, nimikkeiden ja muiden tärkeiden tietoluetteloiden välillä. Vastaavasti toimintojen avulla voi aloittaa tehtävät, kuten luoda uuden myyntilaskun suoraan aloitussivulla.

* Keskellä on nykyiset tiedot näyttävä **Toiminnot**-alue, jossa näkyvät nykyiset tiedot. Ne voidaan valita tarkempaa tarkastelua varten. Suorituskykyilmaisimet (tunnusluvut) voidaan määrittää niin, että ne näyttävät visuaalisesti esimerkiksi kassavirran tai tuottojen ja kulujen valitun kaavion. Voit luoda aloitussivulla myös suosikkiasiakkaiden luettelon niitä yritysasiakkaita varten, joiden kanssa käyt kauppaa usein tai jotka vaativat erityishuomiota.

### <a name="change-the-role"></a>Roolin vaihtaminen

Oletusrooli on **Liiketoimintajohtaja**, mutta voit valita toisen roolin, jotta saat käyttöösi tarpeitasi paremmin vastaavan roolikeskuksen.  

1. Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset** -toiminto.
2. Valitse **Omat asetukset** -sivun **Roolikeskus**-kentässä oletusarvoisesti käytettävä rooli. Valitse esimerkiksi **Kirjanpitäjä**.
3. Valitse **OK**.

## <a name="company"></a><a name="company"></a>Oma yritys

Yritystoiminnot [!INCLUDE[prod_short](includes/prod_short.md)]in tietojen säilönä. Tietokannassa voi olla useita yrityksiä. Kerralla on kuitenkin mahdollista valita vain yksi yritys. Oletusyrityksen nimi on CRONUS, ja se sisältää vain esittelytietoja.

**Yritys**-kentässä on yritys, jonka tietoja käsittelet parhaillaan. Voit käyttää sitä vaihtaessasi toiseen yritykseen. Yrityksen nimi näkyy aina vasemmassa yläkulmassa. Se on myös toiminto, jonka valitsemalla voit palata roolikeskukseen.

> [!TIP]
> Voit myös vaihtaa yrityksen käyttämällä yrityksen vaihtajaa (Crtl+O). Lisätietoja tästä ominaisuudesta ja muista tavoista vaihtaa yritystä tai ympäristöä on kohdassa [Siirtyminen toiseen yritykseen tai ympäristöön](ui-organization-switch.md).

Oletusyrityksen nimi on CRONUS, ja se sisältää vain esittelytietoja. Voit luoda mukautetuilla tiedoilla uuden yrityksen. Lisätietoa on kohdassa [Uusien yritysten luominen](about-new-company.md).

<!--
### <a name="to-change-the-company-name"></a>To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

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

## <a name="region"></a><a name="region"></a>Alue

**Alue**-asetus määrittää, miten päivämäärät, ajat, luvut ja valuutat näkyvät tai miten ne on muotoiltu. Se määrittää myös, mitä merkkiä käytetään desimaalierottimena, kun käytetään numeronäppäimistöä tietojen syöttämiseen. Lisätietoja on kohdassa [Tietojen syöttäminen](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a>Kieli

Muuttaa näyttökielen. Tämä kenttä näkyy vain, kun useita kieliä voi valita.

Alkuperäinen kieli määräytyy joko järjestelmänvalvojan asettamien tai selaimen asetusten mukaan, kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen. Määrittämääsi kieltä käytetään kaikissa laitteissa, joista kirjaudut, esimerkiksi puhelimessa ja tabletissa.

Sovellukseen [!INCLUDE[prod_short](includes/prod_short.md)] voi asentaa lisäkieliä AppSourcesta. Kaikki tuetut näyttökielet näkyvät luettelossa. Järjestelmänvalvojan on asennettava sopiva kielisovellus vuokraajaan, ennen kuin käyttäjät voivat vaihtaa uuteen kieleen [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

## <a name="time-zone"></a>Aikavyöhyke

Määrittää aikavyöhykkeen, jossa olet. Kun kirjaudut ensimmäisen kerran [!INCLUDE [prod_short](includes/prod_short.md)]iin, aikavyöhyke määritetään yrityksen osoitteen perusteella. Vaihda se, jos se ei vastaa sijaintiasi.  

## <a name="notifications"></a>Ilmoitukset

Valitsemalla *Muuta asetusta, milloin saan ilmoituksia* -linkin voit tarkastella tai muuttaa ilmoituksia, joita saat tietyistä tapahtumista tai tilamuutoksista esimerkiksi silloin, kun olet laskuttamassa asiakasta, jolla on erääntynyttä saldoa, tai kun käytettävissä oleva varasto on pienempi kuin myytävä määrä. Lisätietoja on kohdassa [Ilmoitusten hallinta](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Opetusvinkkejä

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-also"></a>Katso myös

[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Uusien yritysten luominen](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
