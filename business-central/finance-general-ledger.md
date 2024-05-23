---
title: Tietoja pääkirjanpidosta ja tilikartasta
description: 'Tämä artikkeli sisältää tietoja pääkirjanpidosta, tilikartasta ja tililuokista. Määritä Pääkirjanpidon asetukset -sivulla, miten yrityksen kirjanpitoasiat käsitellään.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts"></a>Tietoja pääkirjanpidosta ja tilikartasta

Pääkirjanpito(KP) sisältää taloustiedot ja tilikartta näyttää tilit, joihin kirjaat kaikki pääkirjanpidon tapahtumat. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Pääkirjanpidon asetukset ja yleiset kirjausasetukset

Pääkirjanpidon asetukset ovat keskeisiä rahoitusprosesseja, sillä niillä määritetään tietojen kirjaaminen. Erityisesti kaksi sivua on tärkeässä osassa rahoitusprosessien määrittämisessä:  

* **Pääkirjanpidon asetukset**
* **Yleiset kirjausasetukset**

### <a name="the-general-ledger-setup-page"></a>**Pääkirjanpidon asetukset** -sivu

Käytä **Pääkirjanpidon asetukset** -sivua määrittääksesi, miten käsitellä esimerkiksi seuraavia yrityksen kirjanpitoasioita:  

* Laskun pyöristystiliedot  
* Osoitteen muodot  
* Talousraportointi

> [!TIP]
> **Pääkirjanpidon asetukset** -sivulla on yleisiä kenttiä ja kenttiä, jotka ovat maa- tai aluekohtaisia. Jos et ole varma kentän merkityksestä, suosittelemme työskentelemään kirjanpitäjän kanssa ja miettimään, onko kentällä merkitystä organisaatiolle. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Kun haluat avata sivun nyt, käytä seuraavaa [Pääkirjanpidon asetukset](https://businesscentral.dynamics.com/?page=118) -linkkiä.

### <a name="the-general-posting-setup-page"></a>**Yleiset kirjausasetukset** -sivu

Käytä **Yleiset kirjausasetukset** -sivulla voi määrittää yleisen liiketoimintaryhmän ja yleisen tuoteryhmän yhdistelmiä. Kirjausryhmät yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjoja pääkirjanpidon tileille. Jokaiselle liiketoiminnan kirjausryhmän ja tuotteen kirjausryhmän yhdistelmälle täytetään rivi. Voit myös avata jokaisen rivin omassa kirjauksien asetusten kortissaan. Lisätietoja kohdassa [Kirjausryhmien määritykset](finance-posting-groups.md).  

> [!TIP]
> Jos etsimäsi **Yleiset kirjausasetukset** -sivun kentät eivät ole näkyvissä, siirry sivulla oikealle sivun alaosassa olevan vaakavierityspalkin avulla.  

Kun haluat avata sivun nyt, käytä seuraavaa [Yleiset kirjausasetukset](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Tilikartta

**Pääkirjanpidon tilit** -sivulla näkyvät kaikki pääkirjanpidon tilit. Tilikartassa voi tehdä esimerkiksi seuraavia toimintoja:  

* Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
* Voit sulkea tuloslaskelman.  
* Voita avata pääkirjanpitotilikortin (KP) asetusten lisäämistä tai muuttamista varten.  
* Voit tarkastella luetteloa kyseisen tilin kirjausryhmistä.
* Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen.

Lisätietoja on kohdassa [Tilikartan ymmärtäminen](finance-chart-of-accounts.md).

## <a name="account-categories"></a>Tililuokat

Voit räätälöidä rahoituslaskelmien rakennetta yhdistämällä pääkirjanpidon tilit tililuokkiin.  

**KP-tilin luokat** -sivulla on aiemmin luodut pää- ja alaluokat sekä niihin liitetyt pääkirjanpitotilit. Voit luoda uusia alaluokkia ja liittää luokat aiemmin luotuihin tileihin.  

Voit luoda luokkaryhmän sisentämällä **KP-tilin luokat** -sivun rivin alla olevia muita alaluokkia. Yleiskuvauksen saaminen luokkaryhmien avulla on helppoa, koska kunkin ryhmittelyn yhteydessä näytetään kokonaissaldo. Voit luoda esimerkiksi alaluokkia eri käyttöomaisuustyypeille ja luoda sitten luokkaryhmiä esimerkiksi käyttöomaisuudelle ja nykyisille vastaaville.  

Voit määrittää, pitääkö tietyntyyppisten raporttien sisältää kunkin alaluokan tilit. Tililuokat auttavat rahoituslaskelmien asettelun määrittämisessä.  

### <a name="example"></a>Esimerkki

Esimerkiksi oletussaldon tiliotteessa on *Käteisvarat*-alaluokka *Vastaavaa*-kohdassa. Jos haluat, että tiliote ottaa käteiskassan ja sekit huomioon, voit suorittaa seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-tililuokat** ja valitse sitten vastaava linkki.
   1. Vaihtoehtoisesti [Avaa tämä sivu](https://businesscentral.dynamics.com/?page=790).
2. Valitse **Muokkaa luetteloa** -toiminto.
3. Lisää kaksi alaluokkaa: Niistä toinen on tarkoitettu käteiskassalle ja toinen sekkitilille:
   1. Valitse **Nykyinen omaisuus** -luokka.
   2. Valitse **Uusi**-toiminto.
   3. Kirjoita nimikkeen nimi **Kuvaus**-kenttään.
   4. Valitse **KP-tilit luokassa** -kentässä asianmukainen KP-tili.
   5. Valitse **Lisäraporttimääritys**-kentässä **Kassa tilit** -vaihtoehdon.
4. Sisennä ne **Käteisvarat**-alaluokassa.
   1. Valitse vaiheessa 3 luotu alaluokka.
   2. Valitse **Sisennä**-toiminto.
   3. Valitse **Siirrä alas** -toiminto.
   4. Valitse **käteinen**-alaluokan alla oleva **Sisennä**-toiminto.

Kun valitset **Luo talousraportit** -toiminnon tai seuraavan kerran, kun raportti luodaan, saldo laskelmassa näkyvät seuraavat rivit:

* Käteisen kokonaissaldo.
* Rivit, joissa on saldot käteiskassalle ja sekkitilille.  

> [!NOTE]
> Jos luot KP-tilin määrittelemättä tililuokkaa, kun liität tilin kirjausryhmään [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelma liittää tililuokan KP-tilistä automaattisesti tilikarttaan. Jos haluat sisällyttää uuden tilin talousraportteihin, sinun täytyy kuitenkin valita **Luo rahoitusraportit** -toiminto **pääkirjanpidon tililuokat** -sivulta. Vaihtoehtoisesti avaa KP-tilin korttisivu, määritä tililuokka ja luo talousraportti uudelleen.

## <a name="access-to-create-and-edit-gl-accounts-and-account-categories"></a>Luo ja muokkaa KP-tilejä ja tililuokkia

Pienessä organisaatiossa, kuten CRONUS-esittely-yrityksessä, useimmat käyttäjät voivat muokata talouskokonaisuuksia, kuten KP-tilejä, tililuokkia ja tilikarttoja, paitsi ne käyttäjät, joilla on RYHMÄN JÄSEN -käyttöoikeus. Suuremmissa organisaatioissa käytetään tyypillisesti rooleja ja käyttöoikeuksia rajoittamaan näiden entiteettien muokkausoikeutta. Jos olet järjestelmänvalvoja tai sinulla on *Liiketoimintajohtaja*- tai *Kirjanpitäjä*-rooli, voit hallita käyttöoikeuksia antaaksesi oikeille käyttäjille oikeuden käyttää asianomaisia taulukoita. Lue lisätietoja kohdasta [Käyttäjän käyttöoikeuksien yleiskatsauksen hankkiminen](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Dimensioiden käyttäminen tilikartan yksinkertaistamiseksi

Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten myyntitilauksissa. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin. Sen sijaan, että määrittäisit kullekin osastolle ja projektille erilliset kirjanpitotilit, voit käyttää dimensioita analyysin perustana ja välttää monimutkaisen tilikartan luomisen.

Lue lisätietoja dimensioista kohdasta [Asiakkaiden, toimittajien ja muiden tilien oletusdimensioiden määrittäminen](finance-dimensions.md#to-set-up-default-dimensions-for-customers-vendors-and-other-accounts).

## <a name="see-also"></a>Katso myös

[Tietoja tilikartasta](finance-chart-of-accounts.md)  
[Dimensioiden käsitteleminen](finance-dimensions.md)  
[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
