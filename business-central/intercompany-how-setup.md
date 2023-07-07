---
title: Konsernitapahtuman kirjauksen määrittäminen
description: Lisätietoja konsernikumppanuuden määrittämisestä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 01/31/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621'
---
# <a name="set-up-intercompany-transactions"></a>Konsernitapahtumien määrittäminen

Konsernikumppanuuksien avulla on helpompi käsitellä kirjanpitoprosesseja, kun vähintään kaksi yrityksen tytäryhtiötä usein tekee kauppaa toistensa kanssa. Kumppanit voivat siirtää tapahtumia, kuten myyntiä ja ostoja, ja käsitellä niitä joko manuaalisesti tai automaattisesti. Jos esimerkiksi osapuoli lähettää myyntipäiväkirjarivin toiselle kumppanille, vastaanottavalle kumppanille luodaan ostopäiväkirjan rivi.

Konsernin tilikartta voi olla esimerkiksi synkronointikumppanin tilikartan versio. Kukin osapuoli linkittää tilinsä konsernin tilikarttaan. Kukin kumppani linkittää myös dimensiot ja dimensioarvot konsernin dimensioihin.

> [!NOTE]
> 2023 julkaisuaallossa 1 olemme ottaneet käyttöön parannetun **Konsernin asetus** -sivun. Uusi sivu helpottaa konsernikumppanuuden määrittämistä yhdistämällä kaikki määritetyt tehtävät yhdelle sivulle. Jos [!INCLUDE [prod_short](includes/prod_short.md)] on sinulle uusi, käytät jo uutta käyttökokemusta. Jos olet jo olemassa oleva asiakas, järjestelmänvalvoja voi ottaa käyttöön **Hyväksy konsernin yleisen päiväkirjan tapahtumat automaattisesti** -toiminnon **Ominaisuuksien hallinta** -sivulla.
>
> Tämän artikkelin tehtävät olettavat, että ominaisuus on käytössä. Jos olet jo luonut konsernikumppanuuden, voit jatkaa sen käyttöä.

## <a name="before-you-start"></a>Ennen kuin aloitat

Ennen konsernikumppanuuden määrittämistä on tehtävä muutamia päätöksiä.

|Päätös  |Kuvaus  |
|---------|---------|
|Minkä tilikartan pitäisi olla konsernin tilikartan perustana?     | Kaikkien kumppanuuden yritysten on käytettävä samaa konsernin tilikarttaa. Voit perustaa konsernin tilikartan jonkin kumppanuuden yrityksen tilikarttaan tai luoda uuden konsernin tilikartan. Voit yhdistää tilit, joita käytetään kumppanuudessa molempiin suuntiin, jotta jokainen kumppani sekä lähettää että vastaanottaa tapahtumia oikeilta tililtä. Lisätietoja konsernin tilikartan määrittämisestä on kohdassa [Konsernin tilikartan määrittäminen](#set-up-the-intercompany-charts-of-accounts).         |
|Mitkä dimensiot ovat konsernin dimensioiden perustana?     | Jos käytät konsernin dimensioita, niiden täytyy olla samat kaikille kumppanuuden yrityksille. Kun olet määrittänyt konsernin dimensiot, yhdistä niiden dimensioarvot. Lisätietoja dimensioarvojen yhdistämisestä on kohdassa [Konsernin dimensioiden määrittäminen](#set-up-intercompany-dimensions).        |
|Mitkä kumppanit ovat asiakkaita tai toimittajia tai molempia?     |  Lisätietoja asiakkaiden ja toimittajayritysten määrittämisestä konsernikumppanuudessa on kohdassa [Konsernikumppanien määrittäminen asiakkaiksi ja toimittajiksi](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Haluatko määrittää kumppanuudessa käytettävät pankkitilit?| Maksutapahtumien rekisteröintiprosessia voi nopeuttaa määrittämällä kunkin kumppanuusyrityksen pankkitili. Lisä tietoja on ohjeaiheessa [Konsernikumppanien käyttöön tarkoitettujen pankkitilien määrittäminen](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Miten haluat määrittää kumppanuuden yritykset?     | Kaikkien osapuolten on sovittava yksilöllinen konsernikumppanien tunnuskoodi kullekin yritykselle. Liitä koodi asiakas- ja toimittajakortteihin, jotta voit yksilöidä liittyvät tapahtumat. Lisätietoja tunnisteista on kohdassa [Numerosarjojen luominen](ui-create-number-series.md).        |
|Miten haluat käsitellä nimikenumeroita?     | Jos konsernin riveissä on nimikkeitä, voit joko käyttää omia nimikenumeroja tai määrittää kumppanin nimikenumerot kullekin soveltuvalle nimikkeelle. Nimikenumeron voi määrittää joko nimikkeen kortin **Toimittajan nimikenro**- tai **Yleinen nimikenro** -kenttään. Voit myös käyttää **Nimikeviittaus**-toimintoa, kun haluat yhdistää nimikkeiden numerot konsernikumppanien kuvauksiin. Saat lisätietoja nimikeviitteistä siirtymällä kohtaan [Käytä nimikeviittauksia](inventory-how-use-item-cross-refs.md).        |
|Ovatko resurssit mukana?     | Jos suorittamiisi konsernin myyntitapahtumiin sisältyy resursseja, täytä kunkin resurssin kortin **Kons.kump. oston KP-tilinro** -kenttä. Kentässä on konsernin kirjanpitotilin numero, jolle tämän resurssin summa kirjataan kumppaniyrityksessä. Saat lisätietoja resursseista valitsemalla [Resurssien määrittäminen](projects-how-setup-resources.md).<br><br>**HUOMAUTUS**<br>Konsernin sisäisiä ostotapahtumia, jotka sisältävät resursseja, käyttöomaisuutta ja nimikekuluja, ei täysin tueta. Kumppaniyrityksessä **Rivityyppi**-kenttä on tyhjä ostoasiakirjariveillä, jotka sisältävät kyseiset entiteetit. Kenttä tulee päivittää manuaalisesti.        |

## <a name="overview-of-the-steps-to-get-started"></a>Yleistä aloitusvaiheista

**Konsernin asetukset** -sivun avulla voit määrittää seuraavat konsernin tapahtumien komponentit:

* Yrityksen konsernin asetukset.
* Yritys, joka on synkronointikumppanisi.
* Konsernin tilikartta, jota kaikki kumppanit käyttävät tapahtumien vaihtoon.
* Tilikartan tilit ja konsernin tilikartta kunkin kumppanin saapuvien ja lähtevien tapahtumien osalta.
* Konsernin dimensiot ja käytettävät dimensioarvot sekä se, miten ne on yhdistetty kunkin kumppanin dimensioihin.
* Yritykset, jotka ovat konsernikumppaneita.
* Yritykset, jotka ovat toimittajia tai asiakkaita tai molempia.

## <a name="set-up-a-synchronization-partner"></a>Synkronointikumppanien määrittäminen

Kaikkien kumppaneiden on käytettävä samaa konsernin tilikarttaa ja tarpeen mukaan samoja konsernin dimensioita. Voit säästää aikaa, kun määrität kumppanuuden, käyttämällä jonkin kumppanin tilikarttaa ja dimensioita konsernin tilikartan ja dimensioiden pohjana. Pohjana käyttämäsi yritys on nimeltään *synkronointikumppani*. Yleensä synkronointikumppani on pääkonttorin yritys, mutta sen ei tarvitse olla.

**Konsernin asetukset** -sivulla kukin osapuoli määrittää synkronointikumppanin **Synkronointikumppani** -kentässä. Tämän jälkeen konsernin tilikartta ja konsernin dimensiot määritetään automaattisesti synkronointikumppanin asetusten perusteella. Kumppanit käyttävät **Konsernin tilikartan yhdistämismääritys-** ja **Konsernin dimension yhdistämismääritys** -sivuja, jotta ne voivat linkittää tilikartan ja dimensiot konsernin tilikarttaan ja dimensioihin ja päinvastoin. 

Kun olet valmis synkronoimaan tiedot synkronointikumppanin kanssa, valitse **Synkronoinnin määritys** -toiminto.

> [!NOTE]
> On tärkeää yhdistää tilit ja dimensiot molempiin suuntiin. Tämä koskee sekä konsernin tilikarttaa että dimensioita ja niistä omiin tileihin ja dimensioihisi.

## <a name="set-up-the-intercompany-charts-of-accounts"></a>Konsernin tilikartan määrittäminen

Kaikkien kumppaneiden on käytettävä samaa konsernin tilikarttaa ja määritettävä siihen tilit omissa tilikartoissaan. Jos yrityksesi tilikartta määrittää konsernin tilikartan kumppaniyrityksille, noudata tämän osion ohjeita.

Jos käytät konsernin tilikartan sisältävää XML-tiedostoa, noudata ohjeita kohdassa [Konsernin tilikartan tuonti tai vienti](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Konsernin tilikartta** -toiminto.
3. Voit lisätä tilit tekemällä jonkin seuraavista **Konsernin tilikartta** -sivulla:
    * Valitse **Uusi** ja syötä sitten jokainen tili sivulla olevalle riville.  
    * Jos konsernin tilikartta on täsmälleen sama tai samankaltainen kuin varsinainen tilikartta, voit täyttää sivun automaattisesti valitsemalla **Kopioi tilakartasta** -toiminnon. Voit muokata uusia rivejä tarvittaessa.
    * Jos olet määrittänyt konsernin tilikartan synkronointikumppania varten, kopioi kyseiset tilit **Synkronoinnin määritykset** -toiminnon avulla.

    > [!TIP]
    > Jos kopioit konsernin tilikartan synkronointikumppanilta, voit päivittää konsernin tilit käyttämällä **Synkronoinnin määritykset** -toimintoa kumppanin tekemillä muutoksilla.

Seuraavana vaiheena voit linkittää tilikartan yrityksen tilikarttaan. Lisätietoja on kohdassa [Konsernin tilikartan linkittäminen yrityksen tilikarttaan](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### <a name="import-or-export-an-intercompany-chart-of-accounts"></a>Konsernin tilikartan tuominen tai vieminen

Synkronointiyritys voi jakaa tilikartan kumppaneille viemällä sen tiedostoon. Kumppanit voivat tuoda tiedoston saadakseen tilikartan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Konsernin tilikartta** -toiminto.
3. Valitse **Konsernin tilikartta** -sivulla **Tuonti/vienti** -toiminto ja valitse sitten joko **Tuo** tai **Vie**.
4. Valitse tuotava tai vietävä tiedosto.  

**Konsernin tilikartta** -sivulle on täytetty uudet tai muokatut KP-tilin rivit tiedostossa olevan konsernin tilikartan mukaisesti. Sivulla olevat aiemmin luodut liittymättömät rivit eivät muutu.

## <a name="map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Konsernin tilikartan linkittäminen yrityksen tilikarttaan

Kun olet määrittänyt tai tuonut konsernin tilikartan, yhdistä jokainen konsernin tili johonkin tiliin. Määritä **Konsernin tilikartta** -sivulla, kuinka saapuvien tapahtumien konsernin KP-tilit linkitetään yrityksen tilikartan tileihin.

Jos konsernin tileillä ja omilla tileillä on samat numerot, voit yhdistää tilit automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Konsernin tilikartta** -toiminto.

    > [!TIP]
    > Jotta voisit käyttää sivun toimintoja, sinun on ehkä laajennettava sivu leveää asettelua varten.

3. Valitse **Konsernin tilikartta** -sivulla **Tilikartan yhdistämismääritys** -toiminto.
4. Voit linkittää tilit manuaalisesti tai automaattisesti.

    * Voit luoda yhdistämismäärityksen manuaalisesti valitsemalla **Konsernin tilikartta**- ja **KP-tilikartta** -ruuduista tili ja valitsemalla sitten tili **KP-nro**- ja **Konserninro**-kohdista -kentät.
    * Jos haluat, että tilit, joilla on samat numerot, liitetään automaattisesti, valitse liitettävät rivit, valitse **Liitä tiliin, jolla on sama nro** -toiminto ja valitse sitten päivitettävä tilikartta.

    > [!TIP]
    > Jos haluat yhdistää monta tiliä tai ehkä kaikki tilit, valitse rivi, valitse :::image type="icon" source="media/show-more-options-icon.png" border="false"::: ja valitse sitten **Valitse lisää**.

## <a name="set-up-intercompany-dimensions"></a>Konsernin dimensioiden määrittäminen

Jos kumppanit vaihtavat tapahtumia, joihin on linkitetty dimensioita, sopikaa dimensioista, joita kaikki käyttävät. Esimerkiksi synkronointiyritys voi luoda dimensioista yksinkertaistetun version, viedä ne XML-tiedostoon ja jaella tiedoston sitten jokaiselle kumppanille. Kukin kumppani voi tuoda XML-tiedoston **Konsernin dimensiot** -sivulla ja yhdistää konsernin dimensiot omiin dimensioihin. Lisätietoja on kohdassa [Konsernin dimensioiden linkittäminen oman yrityksen dimensioihin](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Kunkin yrityksen on määritettävä dimensiot konsernin dimensioiksi lähtevien asiakirjojen ja saapuvien asiakirjojen osalta. Tilien yhdistäminen molempiin suuntiin on tärkeää, ja se auttaa ylläpitämään yhtenäisyyttä yritysten välillä.

Jos kumppanit käyttävät synkronointikumppanin konsernin dimensioita, noudata tämän osan ohjeita. Jos haluat jakaa konsernin dimensiot sisältävän XML-tiedoston avulla, noudata [Konsernin dimensioiden tuonti tai vienti](#import-or-export-intercompany-dimensions) -kohdan ohjeita.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Konsernin dimensiot** -toiminto.
3. Voit lisätä dimensioita tekemällä jonkin seuraavista **Konsernin dimensiot** -sivulla:
    * Valitse **Uusi** ja syötä jokainen dimensio riville.  
    * Jos konsernin dimensiot ovat täsmälleen samat tai samankaltaiset kuin varsinaiset dimensiot, voit täyttää sivun automaattisesti valitsemalla **Kopioi dimensioista** -toiminnon. Jälkeenpäin voit muokata uusia rivejä tarvittaessa.
    * Jos olet määrittänyt konsernin dimensiot synkronointikumppania varten, kopioi kyseiset dimensiot **Synkronoinnin määritykset** -toiminnon avulla.

    > [!TIP]
    > Jos kopioit konsernin dimensiot synkronointikumppanilta, voit päivittää konsernin dimensiot käyttämällä **Synkronoinnin määritykset** -toimintoa kumppanin tekemillä muutoksilla.  

### <a name="import-or-export-intercompany-dimensions"></a>Konsernin dimensioiden tuonti tai vienti

Synkronointiyritys voi jakaa dimensiot kumppaneille viemällä ne tiedostoon. Kumppanit voivat tuoda tiedoston, jotta dimensiot saadaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Konsernin dimensiot** -toiminto.  
3. Valitse **Konsernin dimensiot** -sivulla **Tuonti/vienti** -toiminto ja valitse sitten joko **Tuo** tai **Vie**.
4. Valitse tuotava tai vietävä tiedosto.

Seuraava askel on yhdistää dimensiot konsernin dimensioihin. Lisätietoja on kohdassa [Konsernin dimensioiden linkittäminen oman yrityksen dimensioihin](#map-intercompany-dimensions-to-your-companys-dimensions).

### <a name="map-intercompany-dimensions-to-your-companys-dimensions"></a>Konsernin dimensioiden linkittäminen oman yrityksen dimensioihin

Kun olet määrittänyt käytettävät dimensiot, yhdistä jokainen konsernin dimensio oman yrityksen dimensioon ja päinvastoin. Voit määrittää yhdistämismäärityksen **Konsernin dimensioiden linkittäminen** -sivulla. Toista tämän jälkeen dimensioarvojen prosessi uudelleen.

* Voit määrittää, miten saapuvien tapahtumien konsernin dimensiot linkitetään yrityksen dimensioiden luetteloon.
* *Lähtevissä tapahtumissa* voi määrittää, kuinka yrityksen dimensiot muunnetaan konsernin dimensioiksi lähtevissä tapahtumissa.

Jos konsernin dimensioilla on samoja koodeja kuin yrityksen vastaavilla dimensioilla, voit linkittää dimensiot automaattisesti.  

Seuraavissa vaiheissa määritetään ensin konsernin dimensiot saapuvien asiakirjojen dimensioiksi **Konsernin dimensio** -ruudussa. Tämän jälkeen dimensiot määritetään lähtevien asiakirjojen dimensioille **Nykyiset yrityksen dimensiot** -ruudussa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Konsernin dimensiot** -toiminto.
3. Valitse **Konsernin dimensiot** -sivulla **Dimensioiden yhdistämismääritys** -toiminto.
4. Voit linkittää dimensiot manuaalisesti tai automaattisesti.

    * Voit luoda yhdistämismäärityksen manuaalisesti valitsemalla **Konsernin dimensio**- ja **Nykyiset yrityksen dimensiot** -ruuduissa dimension ja valitsemalla sitten dimension **Dim.koodi**- ja **Konsernin dim.koodi** -kentistä.
    * Jos haluat, että dimensiot, joilla on sama koodi, liitetään automaattisesti, valitse liitettävät rivit, valitse **Yhdistä dimensiot, joilla on sama koodi** -toiminto ja valitse sitten päivitettävät dimensiot. 

    > [!TIP]
    > Jos haluat yhdistää monta dimensiota tai ehkä kaikki dimensiot, valitse rivi, valitse :::image type="icon" source="media/show-more-options-icon.png" border="false"::: ja valitse sitten **Valitse lisää**.

5. Valitse **Dimensioarvojen yhdistämismääritys** -toiminto.
6. **Konsernin dimensioarvojen yhdistämismääritys** -sivulla yhdistämismäärityksen luomisvaiheet ovat samanlaiset kuin dimensioissa.

## <a name="set-up-intercompany-general-journal-templates-and-batches"></a>Konsernin yleisen päiväkirjan mallien ja erien määrittäminen

Sinun täytyy määrittää yleisen päiväkirjan malli ja yleisen päiväkirjan erä käytettäväksi oletusarvoisesti konsernin tapahtumissa. Malli ja erä ovat erityisen tärkeitä, jos hyväksyt konsernin tapahtumat automaattisesti kumppaneilta. Saat lisätietoja tapahtumien automaattisesta hyväksymisestä valitsemalla [Hyväksy tapahtumia automaattisesti konsernikumppaneilta](#auto-accept-transactions-from-intercompany-partners).   

* Yleisiä päiväkirjoja käytetään kirjaamisessa kirjanpitotileille sekä muille tileille, kuten pankki-, asiakas- ja toimittajatileille. Yleisen päiväkirjan avulla kirjaaminen luo aina tapahtumia kirjanpitotileille.  **Konsernin yleinen päiväkirja** -sivun avulla voit määrittää yleisen päiväkirjan erän käytettäväksi. Konsernin tapahtumia koskevat asetukset ovat **Konsernin tilityyppi**- ja **Konsernin tilinro** -kentissä määritetyt tilit.
* Päiväkirjan mallit mahdollistavat työskentelemisen erityistarkoitusta varten tehdyssä päiväkirjasivussa. Tämä tarkoittaa sitä, että päiväkirjan malleissa olevat kentät ovat juuri niitä, jotka tarvitaan tiettyä ohjelman osaa varten. Käytä **Yleisen päiväkirjan mallit** -sivua konsernin tapahtumissa käytettävän mallin määrittämiseen.

Saat lisätietoja yleisen päiväkirjan malleista ja eristä valitsemalla [Päiväkirjan mallien ja erien käyttäminen](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="set-up-a-company-for-intercompany-transactions"></a>Konsernitapahtumien yrityksen määrittäminen

Seuraavissa vaiheissa oletetaan, että synkronointikumppanille on määritetty tilikartta ja dimensiot, joihin konsernin tilikartta ja dimensiot perustuvat. Voit määrittää ne itse, mutta se on yleensä nopeampaa päästä alkuun, ja ylläpito on helpompaa, jos käytät synkronointikumppania. Lisä tietoja synkronointikumppanista on kohdassa [Synkronointikumppanien määrittäminen](#set-up-a-synchronization-partner).

> [!TIP]
> On hyvä ajatus täyttää **Yleinen**-pikavälilehdellä **Konsernin asetukset** -sivulla olevat kentät kunkin kumppanin osalta ennen kumppanien lisäämistä. Kun lisäät samalle vuokraajalle kuuluvat kumppanit, [!INCLUDE [prod_short](includes/prod_short.md)] hakee niiden konsernikoodin ja yrityksen nimen yleisestä pikavälilehden asetuksista. **Yrityksen nimi** -kentässä varmistetaan, että niiden IC-koodi on yksilöivä.

> [!NOTE]
> Jos käytät synkronointikumppania, jätä **Synkronointikumppani** -kenttä tyhjäksi, kun määrität yrityksen kumppaniksi kumppanuutta varten.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.  
2. Täytä **Konsernin asetukset** -sivun **Yleinen**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Et voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa tiedostosijainteja tapahtumien siirtämiseen kumppaneille, koska[!INCLUDE[prod_short](includes/prod_short.md)]illa ei ole paikallisen verkon käyttöoikeutta. Niinpä jos valitset **Tiedoston sijainti** **Siirron tyyppi** -kentässä **Kansiopolku**-kenttä ei ole käytettävissä. Tiedosto ladataan sen sijaan tietokoneen **Ladatut tiedostot** -kansioon. Voit sitten lähettää tiedoston sähköpostitse esimerkiksi jollekin kumppaniyrityksessä. Kätevämpää on kuitenkin valita suoraan **Lähetä sähköpostitse**.

Seuraavassa vaiheessa määritetään kumppaniyritykset.

## <a name="set-up-intercompany-partners"></a>Määritä konsernikumppanit

Kunkin kumppanin on lisättävä kaikki muut yritykset kumppanuudessa kumppaniksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Konsernikumppanit** -pikavälilehdessä **Lisää**.
3. Täytä kentät **Konsernikumppani**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Toista työvaiheet 2 ja 3 kaikkien kumppanuuden yritysten osalta.

> [!NOTE]
> Jos konsernin kirjauksessa **Hyväksy tapahtumia automaattisesti** -vaihtopainike **Konsernikumppani**-sivulla on otettu käyttöön, [!INCLUDE[prod_short](includes/prod_short.md)] piilottaa sanomat, joissa varoitetaan ostolaskujen kaksoiskappaleista alkuperäisessä ostotilauksessa. On tärkeää, että yrityksellä on liiketoimintaprosessi kaksoiskappaleiden hallintaa varten. Se voidaan tehdä esimerkiksi poistamalla tällaiset ostotilaukset, kun ostolasku vastaanotetaan konsernikumppanilta.

### <a name="set-up-intercompany-partners-as-customers-and-vendors"></a>Konsernikumppanien määrittäminen asiakkaiksi ja toimittajiksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin asetukset** ja valitse sitten vastaava linkki.
2. Avaa **Konsernikumppanit**-pikavälilehdessä kumppanin korttisivu.
3. Valitse asiakas tai kumppani sen mukaan, mitä haluat tehdä, **Asiakasnro**- tai **Toimittajan nro** -kentissä.

    > [!NOTE]
    > Jos asiakasta tai toimittajaa ei ole luotu, voit määrittää ne valitsemalla avattavasta valikosta **+Uusi**. Saat lisätietoja asiakkaiden ja toimittajien luomisesta valitsemalla [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md) ja [Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > Voit myös määrittää asiakkaan tai toimittajan konsernikumppaniksi täyttämällä **Konsernikumppanin koodi** -kentän **Asiakaskortti**-ja **Toimittajan kortti** -sivuilla.

### <a name="set-up-default-intercompany-partner-general-ledger-accounts"></a>Oletuskonsernikumppanin kirjanpitotilien määrittäminen

Kun luot konsernin myynti- tai ostorivin tapahtumana lähetettäväksi, annat konsernin tilikartasta tilin, johon summa oletusarvoisesti kirjataan kumppaniyrityksessä. Voit määrittää **KP-tilin kortti** -sivulla oletuskonsernikumppanin KP-tilin sellaisia tilejä varten, joita käytät säännöllisesti lähtevissä konsernin myynti- tai ostoriveissä. Voit määrittää esimerkiksi myyntisaamistilejä varten konsernin tilikartasta vastaavat ostovelkatilit. Myyntisaamisten ja ostovelkojen tilejä käytetään konsernikumppanien vastakirjauksen tilinä, kun kirjaat konsernin yleisten päiväkirjojen tapahtumia.  

Kun lisäät kirjanpitotilin **Vastatilin nro** -kenttään sille konsernin riville, jonka **Tilityyppi**-kentässä lukee **Konsernikumppani**, **Konsernikumppanin KP-tili** -kenttä täytetään automaattisesti.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Avaa KP-tili, jota käytetään konsernin tapahtumissa, ja anna konsernitapahtumissa käytettävän KP-tilin rivin **Konsernikumppanin KP-oletustili** -kentässä konsernin kirjanpitotili, jonka kumppani kirjaa kun kirjaat KP-tilin riville.
3. Toista vaihe 2 kaikkien sellaisten tilien osalta, joita lisäät usein konsernin päiväkirjan tai asiakirjan riville **Vastatilin nro** -kenttään.

### <a name="auto-accept-transactions-from-intercompany-partners"></a>Hyväksy tapahtumia automaattisesti konsernikumppaneilta

Jotta konsernin tapahtumat voidaan käsitellä nopeammin, voit määrittää, että haluat luoda automaattisesti päiväkirjarivejä, jotka perustuvat konsernikumppanien kirjauksiin **Konsernin yleinen päiväkirja** -sivulla. Saapuvien ja lähtevien tapahtumien automaattinen luominen edellyttää, että otat käyttöön seuraavat vaihtoehdot jokaiselle kumppanille:

* Ota synkronointikumppania varten käyttöön **Konsernin asetukset** -sivulla **Tapahtumien automaattinen lähetys** -vaihto. Määritä sitten, mihin konsernin päiväkirjan vastaanotetut tapahtumat luodaan, täyttämällä **Konsernin yleisen pvk:n oletusmalli**- ja **Konsernin yleisen pvk:n oletuserä** -kentät.

    > [!TIP]
    > Jos **Konsernin yleisen pvk:n oletusmalli** -kenttä on tyhjä, sinun on määritettävä yleisen päiväkirjan malli, jota käytetään konsernin yleisissä päiväkirjoissa. Saat lisätietoja malleista ja eristä valitsemalla [Konsernin yleisen päiväkirjan mallien ja erien määrittäminen](#set-up-intercompany-general-journal-templates-and-batches)    

* Ota käyttöön **Konsernikumppani**-sivulla **Tapahtumien automaattinen hyväksyntä** -vaihto.

Päiväkirjan rivit luodaan, mutta niitä ei kirjata.

> [!NOTE]
> Jos organisaatiossasi käytettiin konsernin sisäisiä [!INCLUDE [prod_short](includes/prod_short.md)]-toimintoja ennen vuoden 2022 1. julkaisuaaltoa, järjestelmänvalvojan täytyy ottaa käyttöön **Hyväksy konsernin yleisen päiväkirjan tapahtumat automaattisesti** -ominaisuus käyttöön **toiminnon hallinta** -sivulla.

### <a name="specify-the-bank-accounts-to-use-for-intercompany-partners"></a>Konsernikumppanien käyttöön tarkoitettujen pankkitilien määrittäminen

Voit helpottaa maksujen suorittamista määrittämällä yhden tai useamman pankkitilin, joita käytetään konsernikumppanien kanssa. Kun kumppani suorittaa maksun konsernin yleisessä päiväkirjassa, hän voi määrittää pankkitilin riville. Pankkitiliä käytetään vastaanottavan yrityksen vastatilinä, mikä minimoi tapahtumien manuaalisen kirjaamisen tarpeen.

* Määritä käytettävä pankkitili valitsemalla **Konsernikumppanit** -sivulta **Pankkitilit**-toiminto. Syötä tilitiedot kohtaan **Konsernin pankkitili -kortti**.

## <a name="troubleshoot-your-intercompany-setup"></a>Konsernin määritysten vianmääritys

**Konsernin asetukset** -sivulla **Konsernimäärityksen diagnostiikka** -ruudussa on ruutuja, jotka ilmaisevat, onko konsernin tapahtumien vaihtoon tarvittavat komponentit määritetty. Ruudut ovat käytettävissä myös Liiketoimintajohtajan roolikeskuksessa. Valitse ruudut selvittääksesi, mitä puuttuu. Saat yleiskuvauksen tarvittavista komponenteista kohdasta [Yleistä aloitusvaiheista](#overview-of-the-steps-to-get-started).

## <a name="see-also"></a>Katso myös

[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
