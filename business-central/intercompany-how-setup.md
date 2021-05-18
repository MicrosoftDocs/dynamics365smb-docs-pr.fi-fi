---
title: Konsernitapahtuman kirjauksen määrittäminen
description: Luo konsernitoimittajat ja -asiakkaat konsernikumppaneina ja määritä konsernin tilikartta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 79c204a6c8a173985a5d3558d5ce1af5a2d8fc39
ms.sourcegitcommit: 6add995f289c56e5497409308825c73eeaa4f62f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941515"
---
# <a name="set-up-intercompany-transaction-posting"></a>Konsernitapahtuman kirjauksen määrittäminen

Jos haluat lähettää yhdestä yrityksestä tapahtuman (kuten myyntipäiväkirjan rivin), jolle luodaan automaattisesti vastaava tapahtuma (kuten ostopäiväkirjan rivi) kumppaniyrityksessä, yrityksillä on oltava yhteinen tilikartta ja dimensiojoukko konsernin tapahtumia varten. Konsernin tilikartta voi olla esimerkiksi pääyrityksen tilikartan yksinkertaistettu versio. Jokainen yritys määrittää oman tilikarttansa vastaavuuden konsernin jaetun tilikartan kanssa ja myös omien dimensioidensa vastaavuuden konsernin dimensioiden kanssa.  

Jokaiselle kumppaniyritykselle on myös määritettävä konsernikumppanin koodi, jonka kaikki yritykset hyväksyvät, ja määrittää se sitten asiakas- ja toimittajakortteihin täyttämällä **Konsernikumppanin koodi** -kenttä.  

Jos luot tai vastaanotat konsernin rivejä, joissa on nimikkeitä, voit joko käyttää omia nimikenumeroja tai määrittää kumppanin nimikenumerot kullekin soveltuvalle nimikkeelle. Nimikenumeron voi määrittää joko nimikkeen kortin **Toimittajan nimikenro**- tai **Yleinen nimikenro** -kenttään. Voit käyttää myös **Nimikeviittaus**-toimintoa yhdistämään nimikenumerot nimikkeiden konsernikumppanien kuvauksiin avaamalla kunkin nimikkeen kortin, valitsemalla **Viittaukset**-toiminnon ja määrittämällä sitten nimikkeen ja konsernikumppanin kuvausten väliset viittaukset. Lisätietoja on kohdassa [Nimikkeen viittausten käyttäminen](inventory-how-use-item-cross-refs.md). 

Jos suorittamiisi konsernin myyntitapahtumiin sisältyy resursseja, täytä kunkin asiaankuuluvan resurssin kortin **Kons.kump. oston KP-tilinro** -kenttä. Tämä on konsernin kirjanpitotilin numero, jolle tämän resurssin summa kirjataan kumppaniyrityksessä. Lisätietoja on kohdassa [Resurssien määrittäminen](projects-how-setup-resources.md).

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Konsernitapahtumien yritysten määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yrityksen tiedot** ja valitse sitten liittyvä linkki.  
2. Täytä **Yrityksen tiedot** -sivulla **Konsernikumppanin koodi**, **Konsernin Saapuneet-kansion tyyppi**. ja **Konsernin Saapuneet-kansion tiedot** -kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Konsernikumppanien määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Konsernikumppani** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Konsernikumppanit**-sivulla.[!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Et voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa tiedostosijainteja tapahtumien siirtämiseen kumppaneille, koska[!INCLUDE[prod_short](includes/prod_short.md)]illa ei ole paikallisen verkon käyttöoikeutta. Niinpä jos valitset **Tiedoston sijainti** **Siirron tyyppi** -kentässä **Kansiopolku**-kenttä ei ole käytettävissä. Tiedosto ladataan sen sijaan tietokoneen Ladatut tiedostot -kansioon. Voit sitten lähettää tiedoston sähköpostitse esimerkiksi jollekin kumppaniyrityksessä. Kätevämpää on kuitenkin valita suoraan **Lähetä sähköpostitse**.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Konsernin toimittajien ja asiakkaiden määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten liittyvä linkki.
2. Voit käyttää toimittajaa myös **Konsernikumppani**-sivun **Toimittajan nro** -kentästä.
3. Avaa sellaisen toimittajan kortti, joka on konsernikumppani. Lisätietoja on kohdassa [Uusien toimittajien rekisteröinti](purchasing-how-register-new-vendors.md).
4. Valitse **Konsernikumppanin koodi** -kentässä sopiva konsernikumppanin koodi.
5. Toista vaiheet 1–4 asiakkaiden kohdalla.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Konsernin tilikartan määrittäminen
Konsernikumppanien väliset tapahtumat ovat mahdollisia vasta, kun konsernikumppanit ovat sopineet yhteisestä tilikartasta. Käyttäjän täytyy sopia konsernikumppanien kanssa tilinumeroista, joita kaikki osapuolet käyttävät konsernin tapahtumia luotaessa. Konsernin emoyritys voi esimerkiksi luoda yksinkertaistetun version omasta tilikartastaan, viedä kyseisen tilikartan tietokannasta XML-tiedostoon ja jakaa sen muille konsernin yrityksille.  

Jos oma yritys on emoyhtiö ja sen tarkoitus oin määrittää konsernin viitekehyksenä käyttämä konsernin tilikartta, noudata kohdan [Konsernin tilikartan määrittäminen](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts) ohjeita.  

Jos oma yritys on tytäryhtiö, ja olet vastaanottanut konsernin yleisen tilikartan XML-tiedostona, noudata kohdan [Konsernin tilikartan tuominen](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts) ohjeita.  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Määrittävän konsernin tilikartan määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin tilikartta** ja valitse sitten liittyvä linkki.
2. Anna **Konsernin tilikartta** -sivulla kukin tili sivun riville.  
3. Jos konsernin tilikartta on täsmälleen sama tai samankaltainen kuin varsinainen tilikartta, voit täyttää sivun automaattisesti valitsemalla **Kopioi tilakartasta** -toiminnon. Voit muokata uusia rivejä tarvittaessa.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Konsernin tilikartan vieminen
Jotta konsernikumppanit voisivat tuoda määrittävän tilikartan, se on vietävä tiedostoon.      
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin tilikartta** ja valitse sitten liittyvä linkki.
2. Valitse **Konsernin Tilikartta** -sivulla **Vie**-toiminto ja valitse sitten **Tallenna**-painike.
3. Määritä tiedostonimi sekä sijainti, johon haluat tallentaa XML-tiedoston, ja valitse sitten **Tallenna**-painike.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Voit tuoda konsernin tilikartan seuraavasti  
Kun määrittävällä konsernin tilikartalla on tiedosto, konsernikumppani voi tuoda sen ja varmistaa näin, että käytettävät tilit ovat samoja.  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin tilikartta** ja valitse sitten liittyvä linkki.  
2. Valitse **Konsernin tilikartta** -sivulla **Tuo**-toiminto.  
3. Valitse XML-tiedoston nimi sekä sijainti ja valitse sitten **Avaa**.  

**Konsernin tilikartta** -sivulle on täytetty uudet tai muokatut KP-tilin rivit tiedostossa olevan konsernin tilikartan mukaisesti. Sivulla olevat aiemmin luodut liittymättömät rivit eivät muutu.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Voit linkittää konsernin tilikartan yrityksen tilikarttaan seuraavasti  
Kun olet määrittänyt tai tuonut konsernin tilikartan, jonka käytöstä on sovittu konsernikumppanien kesken, kukin konsernin KP-tili on liitettävä oman yrityksen KP-tiliin. Määritä **Konsernin tilikartta** -sivulla, kuinka saapuvien tapahtumien konsernin KP-tilit muunnetaan yrityksen tilikartan tileiksi.

Jos konsernin tilikartan tileillä on samoja tilinumeroita kuin tilikartan vastaavilla tileillä, tilit voi linkittää automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin tilikartta** ja valitse sitten liittyvä linkki.  
2. Valitse ensin automaattisesti linkitettävät rivit ja sitten **Liitä tiliin, jolla on sama nro** -toiminto.  
3. Täytä kunkin sellaisen konsernin kirjanpitotilin **Liitä konsernin KP-tilinumeroon** -kenttä, jota ei linkitetty automaattisesti.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Oletuskonsernikumppanin kirjanpitotilien määrittäminen  
Kun luot konsernin myynti- tai ostorivin tapahtumana lähetettäväksi, annat konsernin tilikartasta tilin, johon summa oletusarvoisesti kirjataan kumppaniyrityksessä. Voit määrittää **Tilikartta**-sivulla oletuskonsernikumppanin KP-tilin sellaisia tilejä varten, joita käytät usein lähtevissä konsernin myynti- tai ostoriveissä. Voit määrittää esimerkiksi myyntisaamistilejä varten konsernin tilikartasta vastaavat ostovelkatilit.  

Kun lisäät kirjanpitotilin **Vastatilin nro** -kenttään sille konsernin riville, jonka **Tilityyppi**-kentässä lukee **Konsernikumppani**, **Konsernikumppanin KP-tili** -kenttä täytetään automaattisesti.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Anna konsernitapahtumissa käytettävän KP-tilin rivin **Konsernikumppanin KP-oletustili** -kentässä konsernin kirjanpitotili, jonka kumppani kirjaa kun kirjaat KP-tilin riville.  
3. Toista vaihe 2 kaikkien sellaisten tilien osalta, joita lisäät usein konsernin päiväkirjan tai asiakirjan riville **Vastatilin nro** -kenttään.

## <a name="to-set-up-intercompany-dimensions"></a>Konsernin dimensioiden määrittäminen

Jos oman yrityksen ja konsernikumppanien välillä halutaan siirtää tapahtumia, joihin on linkitetty dimensioita, kaikkien on hyväksyttävä käytettävät dimensiot. Konsernin emoyritys voi esimerkiksi luoda yksinkertaistetun version omasta dimensiojoukostaan, viedä kyseiset konsernin dimensiot XML-tiedostoon ja jakaa tiedoston muille konsernin yrityksille. Jokainen tytäryhtiö tuo tämän jälkeen XML-tiedoston **Konsernin dimensiot** -sivulle ja linkittää konsernin dimensiot oman **Dimensiot**-sivunsa dimensioihin.  

> [!NOTE]
> Kunkin [!INCLUDE [prod_short](includes/prod_short.md)]in yrityksen täytyy yhdistää dimensiot konsernin dimensioihin lähtevien asiakirjojen osalta ja linkittää konsernin dimensiot omiin dimensioihin saapuville asiakirjoille. Tämä yhdstäminen auttaa varmistamaan yhdenmukaisuuden yritysten välillä. Lisäietoja on [Voit linkittää konsernin dimensiot oman yrityksen dimensioihin seuraavasti](#to-map-intercompany-dimensions-to-your-companys-dimensions) -osiossa.

Jos oma yritys on emoyhtiö ja sen on tarkoitus määrittää konsernin viitekehyksenä käyttämä konsernin dimensiojoukko, noudata kohdan [Konsernin dimensioiden määrittäminen](intercompany-how-setup.md#to-define-the-intercompany-dimensions) ohjeita.

Jos oma yritys on tytäryhtiö, ja olet vastaanottanut konsernin viitekehyksenä käytettävät konsernin dimensiot, noudata kohdan [Konsernin dimensioiden tuominen](intercompany-how-setup.md#to-import-the-intercompany-dimensions) ohjeita.

### <a name="to-define-the-intercompany-dimensions"></a>Konsernin dimensioiden määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Konsernin dimensiot** ja valitse sitten liittyvä linkki.  
2. Lisää **Konsernin dimensiot** -sivulla kukin dimensio sivun riville.

    Jos konsernin dimensiot muistuttavat läheisesti yrityksen omia dimensioita, voit täyttää sivun automaattisesti valitsemalla **Kopioi dimensioista** -toiminnon. Rivejä voi tämän jälkeen muokata.  
3. Kun valitset **Vie**-toiminnon, voit viedä konsernin dimensiot XML-tiedostoon kumppaniyrityksille jaettavaksi.  
4. Määritä tiedostonimi sekä sijainti, johon haluat tallentaa XML-tiedoston, ja valitse sitten **Tallenna**-painike.  

### <a name="to-import-the-intercompany-dimensions"></a>Konsernin dimensioiden tuominen  
Kun määrittävällä konsernin dimensioilla on tiedosto, konsernikumppanit voivat tuoda sen ja varmistaa näin, että käytettävät dimensiot ovat samoja.  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Konsernin dimensiot** ja valitse sitten liittyvä linkki.  
2. Valitse **Konsernin dimensiot** -sivulla **Tuo**-toiminto.  
3. Määritä XML-tiedoston nimi sekä sijainti ja valitse sitten **Avaa**.  

**Konsernin dimensiot**- ja **Konsernin dimensioarvot** -sivujen rivit tuodaan.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Voit linkittää konsernin dimensiot oman yrityksen dimensioihin seuraavasti
Kun olet määrittänyt tai tuonut dimensiot, joiden käytöstä olette sopineet konsernikumppanien kesken, kukin konsernin dimensio on yhdistettävä oman yrityksen dimensioon ja päin vastoin. Määritä **Konsernin dimensiot** -sivulla, miten *saapuvien tapahtumien* konsernin dimensiot muunnetaan yrityksen dimensioluettelon dimensioiksi. **Dimensiot**-sivulla voi määrittää, kuinka yrityksen dimensiot muunnetaan konsernin dimensioiksi *lähtevissä tapahtumissa*.

Jos konsernin dimensioilla on samoja koodeja kuin yrityksen dimensioluettelon vastaavilla dimensioilla, voit määrittää sovelluksen linkittämään dimensiot automaattisesti ja linkittää tilit sitten automaattisesti.  

Seuraavissa vaiheissa määritetään ensin konsernin dimensiot saapuvien asiakirjojen dimensioiksi **Konsernin dimensio** -sivulla. Tämän jälkeen dimensiot määritetään lähtevien asiakirjojen dimensioille **Dimensiot**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Konsernin dimensiot** ja valitse sitten liittyvä linkki.
2. Valitse **Konsernin dimensiot** -sivulla rivit, jotka haluat linkittää automaattisesti, ja valitse sitten **Liitä dimensioon, jolla on sama koodi** -toiminto.
3. Jos konsernin dimensiota ei linkitetä automaattisesti, täytä **Liitä dimensiokoodiin** -kenttä.

    Kenttä on ehkä lisättävä näkymään. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).
4. Valitse **Konsernin dimension arvot** -toiminto.
5. Täytä **Konsernin dimension arvot** -sivun **Liitä kons. dim. arvokoodiin** -kenttä.

    Jatka dimensioiden linkittämistä konsernin dimensioihin vastaavasti.
6. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Dimensiot** ja valitse sitten liittyvä linkki.
7. Valitse **Dimensiot**-sivulla rivit, jotka haluat linkittää automaattisesti, ja valitse sitten **Liitä konsernin dimensioon, jolla on sama koodi** -toiminto.
8. Jos konsernin dimensiota ei linkitetä automaattisesti, täytä **Liitä konsernin dimensioarvon koodiin** -kenttä.
9. Valitse **Konsernin dimension arvot** -toiminto.
10. Täytä **Dimension arvot** -sivun **Liitä kons. dim. arvokoodiin** -kenttä.

## <a name="see-also"></a>Katso myös

[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]