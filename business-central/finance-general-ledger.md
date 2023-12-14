---
title: Tietoa pääkirjanpidosta ja tilikartasta
description: 'Tämä artikkeli sisältää tietoja pääkirjanpidosta, tilikartasta ja tililuokista. Määritä Pääkirjanpidon asetukset -sivulla, miten yrityksen kirjanpitoasiat käsitellään.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/24/2022
ms.author: bholtorf
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts"></a>Tietoja pääkirjanpidosta ja tilikartasta

Pääkirjanpito(KP) sisältää taloustiedot ja tilikartta näyttää tilit, joihin kaikki pääkirjanpidon tapahtumat kirjataan. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Pääkirjanpidon asetukset ja yleiset kirjausasetukset

Pääkirjanpidon asetukset ovat keskeisiä rahoitusprosesseja, sillä niillä määritetään tietojen kirjaaminen. Erityisesti kaksi sivua on tärkeässä osassa rahoitusprosessien määrittämisessä:  

* **Pääkirjanpidon asetukset** -sivu

  **Pääkirjanpidon asetukset** -sivulla määritetään, miten esimerkiksi seuraavat yrityksen kirjanpitoasiat:  

  * Laskun pyöristystiliedot  
  * Osoitteen muodot  
  * Talousraportointi

  > [!TIP]
  > **Pääkirjanpidon asetukset** -sivulla on yleisiä kenttiä ja kenttiä, jotka ovat maa- tai aluekohtaisia. Jos et ole varma kentän merkityksestä, suosittelemme työskentelemään kirjanpitäjän kanssa ja miettimään, onko kentällä merkitystä organisaatiolle. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

  Avaa sivu [täällä](https://businesscentral.dynamics.com/?page=118).
  
* **Yleiset kirjausasetukset** -sivu

  Samaan tapaan määritetään **Yleiset kirjausasetukset** -sivulla, miten liiketoiminnan ja tuotteen yleisten kirjausryhmien yhdistelmät määritetään. Kirjausryhmät yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjoja pääkirjanpidon tileille. Jokaiselle liiketoiminnan kirjausryhmän ja tuotteen kirjausryhmän yhdistelmälle täytetään rivi. Voit myös avata jokaisen rivin omassa kirjauksien asetusten kortissaan. Lisätietoja kohdassa [Kirjausryhmien määritykset](finance-posting-groups.md).  

  > [!TIP]
  > Jos etsimäsi **Yleiset kirjausasetukset** -sivun kentät eivät ole näkyvissä, siirry sivulla oikealle sivun alaosassa olevan vaakavierityspalkin avulla.  

  Avaa sivu [täällä](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Tilikartta

Kaikki pääkirjanpidon tilit näkyvät tilikartassa. Tilikartassa voi tehdä esimerkiksi seuraavia toimintoja:  

* Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
* Voit sulkea tuloslaskelman.  
* Voita avata pääkirjanpitotilikortin (KP) asetusten lisäämistä tai muuttamista varten.  
* Voit tarkastella luetteloa kyseisen tilin kirjausryhmistä.
* Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen.

Voit lisätä, muuttaa tai poistaa pääkirjanpidon tilejä. Ristiriitojen estämiseksi et voi kuitenkaan poistaa pääkirjanpidon tiliä, jos sen tietoja käytetään tilikartassa. Alkaen vuoden 2022 2. julkaisuaallosta voit myös estää tilien vahingossa poistamisen arkaluonteisina kausina. Lisätietoja on [Tilien poistaminen](finance-setup-chart-accounts.md#delete-accounts) -osassa.  

## <a name="account-categories"></a>Tililuokat

Voit räätälöidä rahoituslaskelmien rakennetta yhdistämällä pääkirjanpidon tilit tililuokkiin.  

**KP-tilin luokat** -sivulla on aiemmin luodut pää- ja alaluokat sekä niihin liitetyt pääkirjanpitotilit. Voit luoda uusia alaluokkia ja liittää luokat aiemmin luotuihin tileihin.  

Voit luoda luokkaryhmän sisentämällä **KP-tilin luokat** -sivun rivin alla olevia muita alaluokkia. Yleiskuvauksen saaminen luokkaryhmien avulla on helppoa, koska kunkin ryhmittelyn yhteydessä näytetään kokonaissaldo. Voit luoda esimerkiksi alaluokkia eri käyttöomaisuustyypeille ja luoda sitten luokkaryhmiä esimerkiksi käyttöomaisuudelle ja nykyisille vastaaville.  

Voit määrittää, pitääkö tietyntyyppisten raporttien sisältää kunkin alaluokan tilit. Tililuokat auttavat rahoituslaskelmien asettelun määrittämisessä.  

### <a name="example"></a>Esimerkki

Esimerkiksi oletussaldon tiliotteessa on *Käteisvarat*-alaluokka *Vastaavaa*-kohdassa. Jos haluat, että tiliote ottaa käteiskassan ja sekit huomioon, sinun tulee suorittaa seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-tililuokat** ja valitse sitten vastaava linkki.
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
> Jos luot KP-tilin määrittelemättä tililuokkaa, kun liität tilin kirjausryhmään [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelma liittää tililuokan KP-tilistä automaattisesti tilikarttaan. Jos haluat sisällyttää uuden tilin talousraportteihin, sinun täytyy kuitenkin valita **Luo rahoitusraportit** -toiminto **pääkirjanpidon tililuokat** -sivulta. Vaihtoehtoisesti voit avata KP-tilin korttisivun, määrittää tililuokan ja luoda talousraportin uudelleen.

## <a name="get-a-quick-overview"></a>Nopean yleiskuvauksen saaminen

**Tilikartat**-sivulla näkyvät hierarkkisessa luettelossa olevat tilit, jotka tarjoavat nopean pääsyn kunkin tilin avaintietoihin. Luettelo on kuitenkin staattinen, ja jos sinulla on paljon tilejä, sinun on ehkä vieritettävä nähdäksesi eri tilejä. Jos haluat vain nopean yleiskatsauksen perusasioista, kuten nettomuutoksista ja saldoista, **Tilikartan yleiskuvaus** -sivu on hyödyllinen vaihtoehto. Sivun sarakeasettelu on nyt sama kuin jonka löydät **tilikartta**-sivulta (vaikkakin vähemmillä sarakkeilla), joten sinun ei tarvitse suuntautua uudelleen. Voit tiivistää näkymää laajentamalla tai kutistamalla hierarkiatasoja. Jotta sivuja olisi helppo vaihtaa, **Tilikartan yleiskuvaus** -sivu on käytettävissä **Tilikartta**-sivulta.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Luo ja muokkaa tilejä ja tililuokkia

Pienessä organisaatiossa, kuten CRONUS-esittely-yrityksessä, useimmat käyttäjät voivat muokata tilikarttaa lukuun ottamatta niitä käyttäjiä, joilla on TEAM MEMBER -käyttöoikeus. Suuremmissa organisaatioissa käytetään tyypillisesti rooleja ja käyttöoikeuksia rajoittamaan tilikartan muokkausoikeutta. Jos olet järjestelmänvalvoja tai sinulla on *Liiketoimintajohtaja*- tai *Kirjanpitäjä*-rooli, voit hallita käyttöoikeuksia antaaksesi oikeille käyttäjille oikeuden käyttää asianomaisia taulukoita. Lue lisätietoja [Käyttäjän käyttöoikeuksien yleiskatsauksen hankkiminen](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions) -osassa.  

## <a name="see-also"></a>Katso myös

[Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md)  
[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
