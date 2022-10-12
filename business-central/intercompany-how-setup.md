---
title: Konsernitapahtuman kirjauksen määrittäminen
description: Luo konsernitoimittajat ja -asiakkaat konsernikumppaneina ja määritä konsernin tilikartta.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.search.form: 605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621
ms.date: 03/09/2022
ms.author: edupont
ms.openlocfilehash: 32a0005f2ebbc6bfc87c21fed8469c86535e15de
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607281"
---
# <a name="set-up-intercompany-transaction-posting"></a>Konsernitapahtuman kirjauksen määrittäminen

Konsernin kirjaukset tekevät kahden tai useamman yrityksen kirjanpidollisesta tehtävästä helpompaa konsernin konsernikumppanien ja yritysten keskitetyn talousosaston ja kirjanpitäjien kesken. Jos haluat lähettää yhdestä yrityksestä tapahtuman (kuten myyntipäiväkirjan rivin), jolle luodaan automaattisesti vastaava tapahtuma (kuten ostopäiväkirjan rivi) kumppaniyrityksessä, yrityksillä on oltava yhteinen tilikartta ja dimensiojoukko konsernin tapahtumia varten. Konsernin tilikartta voi olla esimerkiksi pääyrityksen tilikartan yksinkertaistettu versio. Jokainen yritys määrittää oman tilikarttansa vastaavuuden konsernin jaetun tilikartan kanssa ja myös omien dimensioidensa vastaavuuden konsernin dimensioiden kanssa.  

Jokaiselle [!INCLUDE [prod_short](includes/prod_short.md)]-yritykselle on myös määritettävä konsernikumppanin koodi, jonka kaikki yritykset hyväksyvät, ja määrittää se sitten asiakas- ja toimittajakortteihin.  

Jos luot tai vastaanotat konsernin rivejä, joissa on nimikkeitä, voit joko käyttää omia nimikenumeroja tai määrittää kumppanin nimikenumerot kullekin soveltuvalle nimikkeelle. Nimikenumeron voi määrittää joko nimikkeen kortin **Toimittajan nimikenro**- tai **Yleinen nimikenro** -kenttään. Voit käyttää myös **Nimikeviittaus**-toimintoa yhdistämään nimikenumerot nimikkeiden konsernikumppanien kuvauksiin avaamalla kunkin nimikkeen kortin, valitsemalla **Nimikeviittaukset**-toiminnon ja määrittämällä sitten nimikkeen ja konsernikumppanin kuvausten väliset viittaukset. Lisätietoja on kohdassa [Nimikkeen viittausten käyttäminen](inventory-how-use-item-cross-refs.md).

Jos suorittamiisi konsernin myyntitapahtumiin sisältyy resursseja, täytä kunkin asiaankuuluvan resurssin kortin **Kons.kump. oston KP-tilinro** -kenttä. Tämä on konsernin kirjanpitotilin numero, jolle tämän resurssin summa kirjataan kumppaniyrityksessä. Lisätietoja on kohdassa [Resurssien määrittäminen](projects-how-setup-resources.md).

> [!NOTE]
> Konsernin sisäisiä ostotapahtumia, jotka sisältävät resursseja, käyttöomaisuutta ja nimikekuluja, ei täysin tueta. Konsernikumppanin yrityksessä **Rivityyppi**-kenttä on tyhjä ostoasiakirjariveillä, jotka sisältävät kyseiset entiteetit. Kenttä tulee päivittää manuaalisesti.

## <a name="auto-accept-transactions-from-intercompany-partners"></a>Hyväksy tapahtumia automaattisesti konsernikumppaneilta

Vuoden 2022 julkaisuaalto 1 esitteli uuden **Konsernikumppaniasetukset**-sivun, jonka avulla konsernikumppanit voivat käsitellä tapahtumia nopeammin. Sivun avulla voit määrittää, luoko yritys automaattisesti kirjauskansiorivejä **Konsernin yleinen päiväkirja** -sivulta. Päiväkirjan rivit luodaan, mutta niitä ei kirjata. Uuden Konsernin asetukset -sivun seuraavien kenttien avulla voit määrittää, missä vastaanotetut konsernin päiväkirjan tapahtumat luodaan:

* **Konsernin yleisen pvk:n oletusmalli**
* **Konsernin yleisen pvk:n oletuserä**

> [!NOTE]
> Jos organisaatiossasi käytettiin konsernin sisäisiä [!INCLUDE [prod_short](includes/prod_short.md)]-toimintoja ennen vuoden 2022 1. julkaisuaaltoa, järjestelmänvalvojan täytyy ottaa käyttöön **Hyväksy konsernin yleisen päiväkirjan tapahtumat automaattisesti** -ominaisuus käyttöön **toiminnon hallinta** -sivulla.

## <a name="to-set-up-a-company-for-intercompany-transactions"></a>Konsernitapahtumien yrityksen määrittäminen

Nämä täytettävät kentät vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.  
2. Täytä kentät **Konsernin asetukset** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-intercompany-partners"></a>Konsernikumppaneiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernikumppanit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Konsernikumppanit**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Toista vaiheet 2 ja 3 kaikille muille yrityksille, jotka ovat osa konsernin asetuksia.

> [!NOTE]
> Et voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa tiedostosijainteja tapahtumien siirtämiseen kumppaneille, koska[!INCLUDE[prod_short](includes/prod_short.md)]illa ei ole paikallisen verkon käyttöoikeutta. Niinpä jos valitset **Tiedoston sijainti** **Siirron tyyppi** -kentässä **Kansiopolku**-kenttä ei ole käytettävissä. Tiedosto ladataan sen sijaan tietokoneen Ladatut tiedostot -kansioon. Voit sitten lähettää tiedoston sähköpostitse esimerkiksi jollekin kumppaniyrityksessä. Kätevämpää on kuitenkin valita suoraan **Lähetä sähköpostitse**.

> [!NOTE]
> Jos konsernin kirjauksessa **Hyväksy tapahtumia automaattisesti** -vaihtopainike **Konsernikumppanin kortti** -sivulla on otettu käyttöön, [!INCLUDE[prod_short](includes/prod_short.md)] piilottaa sanomat, joissa varoitetaan ostolaskujen kaksoiskappaleista alkuperäisessä ostotilauksessa. Tämän vuoksi on tärkeää, että yrityksellä on liiketoimintaprosessi kaksoiskappaleiden hallintaa varten. Se voidaan tehdä esimerkiksi poistamalla tällaiset ostotilaukset, kun ostolasku vastaanotetaan konsernikumppanilta.


## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Konsernin toimittajien ja asiakkaiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.
2. Voit käyttää toimittajaa myös **Konsernikumppani**-sivun **Toimittajan nro** -kentästä.
3. Avaa sellaisen toimittajan kortti, joka on konsernikumppani. Lisätietoja on kohdassa [Uusien toimittajien rekisteröinti](purchasing-how-register-new-vendors.md).
4. Valitse **Konsernikumppanin koodi** -kentässä sopiva konsernikumppanin koodi.
5. Toista vaiheet 1–4 asiakkaiden kohdalla.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Konsernin tilikartan määrittäminen

Konsernikumppanien väliset tapahtumat ovat mahdollisia vasta, kun konsernikumppanit ovat sopineet yhteisestä tilikartasta. Käyttäjän täytyy sopia konsernikumppanien kanssa tilinumeroista, joita kaikki osapuolet käyttävät konsernin tapahtumia luotaessa. Konsernin emoyritys voi esimerkiksi luoda yksinkertaistetun version omasta tilikartastaan, viedä sen XML-tiedostoon ja jakaa tiedoston muille konsernin yrityksille.  

Jos oman yrityksen tilikartta määrittää kumppaniyritysten käyttämän konsernin tilikartan, noudata kohdan [Konsernin tilikartan määrittäminen](intercompany-how-setup.md#to-set-up-the-intercompany-chart-of-accounts) ohjeita.  

Jos oma yritys on tytäryhtiö, ja olet vastaanottanut konsernin yleisen tilikartan XML-tiedostona, noudata kohdan [Konsernin tilikartan tuominen](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts) ohjeita.  

### <a name="to-set-up-the-intercompany-chart-of-accounts"></a>Konsernin tilikartan valmistelutoimien tekeminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernikumppanin tilikartta** ja valitse sitten vastaava linkki.
2. Anna **Konsernin tilikartta** -sivulla kukin tili sivun riville.  
3. Jos konsernin tilikartta on täsmälleen sama tai samankaltainen kuin varsinainen tilikartta, voit täyttää sivun automaattisesti valitsemalla **Kopioi tilakartasta** -toiminnon. Voit muokata uusia rivejä tarvittaessa.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Konsernin tilikartan vieminen

Jotta konsernikumppanit voisivat tuoda määrittävän tilikartan, se on vietävä tiedostoon.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernikumppanin tilikartta** ja valitse sitten vastaava linkki.
2. Valitse **Konsernin Tilikartta** -sivulla **Vie**-toiminto ja valitse sitten **Tallenna**-painike.
3. Määritä tiedostonimi sekä sijainti, johon haluat tallentaa XML-tiedoston, ja valitse sitten **Tallenna**-painike.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Voit tuoda konsernin tilikartan seuraavasti  

Kun määrittävällä konsernin tilikartalla on tiedosto, konsernikumppani voi tuoda sen ja varmistaa näin, että käytettävät tilit ovat samoja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernikumppanin tilikartta** ja valitse sitten vastaava linkki.  
2. Valitse **Konsernin tilikartta** -sivulla **Tuo**-toiminto.  
3. Valitse XML-tiedoston nimi sekä sijainti ja valitse sitten **Avaa**.  

**Konsernin tilikartta** -sivulle on täytetty uudet tai muokatut KP-tilin rivit tiedostossa olevan konsernin tilikartan mukaisesti. Sivulla olevat aiemmin luodut liittymättömät rivit eivät muutu.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Voit linkittää konsernin tilikartan yrityksen tilikarttaan seuraavasti  

Kun olet määrittänyt tai tuonut konsernin tilikartan, jonka käytöstä on sovittu konsernikumppanien kesken, kukin konsernin KP-tili on liitettävä oman yrityksen KP-tiliin. Määritä **Konsernin tilikartta** -sivulla, kuinka saapuvien tapahtumien konsernin KP-tilit muunnetaan yrityksen tilikartan tileiksi.

Jos konsernin tilikartan tileillä on samoja tilinumeroita kuin tilikartan vastaavilla tileillä, tilit voi linkittää automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernikumppanin tilikartta** ja valitse sitten vastaava linkki.  
2. Valitse ensin automaattisesti linkitettävät rivit ja sitten **Liitä tiliin, jolla on sama nro** -toiminto.  
3. Täytä kunkin sellaisen konsernin kirjanpitotilin **Liitä konsernin KP-tilinumeroon** -kenttä, jota ei linkitetty automaattisesti.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Oletuskonsernikumppanin kirjanpitotilien määrittäminen  

Kun luot konsernin myynti- tai ostorivin tapahtumana lähetettäväksi, annat konsernin tilikartasta tilin, johon summa oletusarvoisesti kirjataan kumppaniyrityksessä. Voit määrittää **Tilikartta**-sivulla oletuskonsernikumppanin KP-tilin sellaisia tilejä varten, joita käytät säännöllisesti lähtevissä konsernin myynti- tai ostoriveissä. Voit määrittää esimerkiksi myyntisaamistilejä varten konsernin tilikartasta vastaavat ostovelkatilit.  

Kun lisäät kirjanpitotilin **Vastatilin nro** -kenttään sille konsernin riville, jonka **Tilityyppi**-kentässä lukee **Konsernikumppani**, **Konsernikumppanin KP-tili** -kenttä täytetään automaattisesti.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Anna konsernitapahtumissa käytettävän KP-tilin rivin **Konsernikumppanin KP-oletustili** -kentässä konsernin kirjanpitotili, jonka kumppani kirjaa kun kirjaat KP-tilin riville.  
3. Toista vaihe 2 kaikkien sellaisten tilien osalta, joita lisäät usein konsernin päiväkirjan tai asiakirjan riville **Vastatilin nro** -kenttään.

## <a name="to-set-up-intercompany-dimensions"></a>Konsernin dimensioiden määrittäminen

Jos oman yrityksen ja konsernikumppanien välillä halutaan siirtää tapahtumia, joihin on linkitetty dimensioita, kaikkien on hyväksyttävä käytettävät dimensiot. Konsernin emoyritys voi esimerkiksi luoda yksinkertaistetun version omasta dimensioyhdistelmästään, viedä ne XML-tiedostoon ja jakaa tiedoston muille konsernin yrityksille. Jokainen tytäryhtiö tuo tämän jälkeen XML-tiedoston **Konsernin dimensiot** -sivulle ja linkittää konsernin dimensiot oman **Dimensiot**-sivunsa dimensioihin.  

> [!NOTE]
> Kunkin [!INCLUDE [prod_short](includes/prod_short.md)]in yrityksen täytyy yhdistää dimensiot konsernin dimensioihin lähtevien asiakirjojen osalta ja linkittää konsernin dimensiot omiin dimensioihin saapuville asiakirjoille. Tämä yhdstäminen auttaa varmistamaan yhdenmukaisuuden yritysten välillä. Lisäietoja on [Voit linkittää konsernin dimensiot oman yrityksen dimensioihin seuraavasti](#to-map-intercompany-dimensions-to-your-companys-dimensions) -osiossa.

Jos oma yritys on emoyhtiö ja sen on tarkoitus määrittää konsernin viitekehyksenä käyttämä konsernin dimensiojoukko, noudata kohdan [Konsernin dimensioiden määrittäminen](intercompany-how-setup.md#to-define-the-intercompany-dimensions) ohjeita.

Jos oma yritys on tytäryhtiö, ja olet vastaanottanut konsernin viitekehyksenä käytettävät konsernin dimensiot, noudata kohdan [Konsernin dimensioiden tuominen](intercompany-how-setup.md#to-import-the-intercompany-dimensions) ohjeita.

### <a name="to-define-the-intercompany-dimensions"></a>Konsernin dimensioiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin dimensiot** ja valitse sitten vastaava linkki.  
2. Lisää **Konsernin dimensiot** -sivulla kukin dimensio sivun riville.

    Jos konsernin dimensiot muistuttavat läheisesti yrityksen omia dimensioita, voit täyttää sivun automaattisesti valitsemalla **Kopioi dimensioista** -toiminnon. Rivejä voi tämän jälkeen muokata.  
3. Kun valitset **Vie**-toiminnon, voit viedä konsernin dimensiot XML-tiedostoon kumppaniyrityksille jaettavaksi.  
4. Määritä tiedostonimi sekä sijainti, johon haluat tallentaa XML-tiedoston, ja valitse sitten **Tallenna**-painike.  

### <a name="to-import-the-intercompany-dimensions"></a>Konsernin dimensioiden tuominen  

Kun määrittävällä konsernin dimensioilla on tiedosto, konsernikumppanit voivat tuoda sen ja varmistaa näin, että käytettävät dimensiot ovat samoja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin dimensiot** ja valitse sitten vastaava linkki.  
2. Valitse **Konsernin dimensiot** -sivulla **Tuo**-toiminto.  
3. Määritä XML-tiedoston nimi sekä sijainti ja valitse sitten **Avaa**.  

**Konsernin dimensiot**- ja **Konsernin dimensioarvot** -sivujen rivit tuodaan.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Voit linkittää konsernin dimensiot oman yrityksen dimensioihin seuraavasti

Kun olet määrittänyt tai tuonut dimensiot, joiden käytöstä olette sopineet konsernikumppanien kesken, kukin konsernin dimensio on yhdistettävä oman yrityksen dimensioon ja päin vastoin. Määritä **Konsernin dimensiot** -sivulla, miten *saapuvien tapahtumien* konsernin dimensiot muunnetaan yrityksen dimensioluettelon dimensioiksi. **Dimensiot**-sivulla voi määrittää, kuinka yrityksen dimensiot muunnetaan konsernin dimensioiksi *lähtevissä tapahtumissa*.

Jos konsernin dimensioilla on samoja koodeja kuin yrityksen dimensioluettelon vastaavilla dimensioilla, voit määrittää sovelluksen linkittämään dimensiot automaattisesti ja linkittää tilit sitten automaattisesti.  

Seuraavissa vaiheissa määritetään ensin konsernin dimensiot saapuvien asiakirjojen dimensioiksi **Konsernin dimensio** -sivulla. Tämän jälkeen dimensiot määritetään lähtevien asiakirjojen dimensioille **Dimensiot**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin dimensiot** ja valitse sitten vastaava linkki.
2. Valitse **Konsernin dimensiot** -sivulla rivit, jotka haluat linkittää automaattisesti, ja valitse sitten **Liitä dimensioon, jolla on sama koodi** -toiminto.
3. Jos konsernin dimensiota ei linkitetä automaattisesti, täytä **Liitä dimensiokoodiin** -kenttä.

    Kenttä on ehkä lisättävä näkymään. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).
4. Valitse **Konsernin dimension arvot** -toiminto.
5. Täytä **Konsernin dimension arvot** -sivun **Liitä kons. dim. arvokoodiin** -kenttä.

    Jatka dimensioiden linkittämistä konsernin dimensioihin vastaavasti.
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Dimensiot** ja valitse sitten vastaava linkki.
7. Valitse **Dimensiot**-sivulla rivit, jotka haluat linkittää automaattisesti, ja valitse sitten **Liitä konsernin dimensioon, jolla on sama koodi** -toiminto.
8. Jos konsernin dimensiota ei linkitetä automaattisesti, täytä **Liitä konsernin dimensioarvon koodiin** -kenttä.
9. Valitse **Konsernin dimension arvot** -toiminto.
10. Täytä **Dimension arvot** -sivun **Liitä kons. dim. arvokoodiin** -kenttä.

## <a name="see-also"></a>Katso myös

[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]