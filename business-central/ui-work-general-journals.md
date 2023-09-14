---
title: Kirjaaminen suoraan pääkirjanpitoon yleisten päiväkirjojen avulla
description: 'Tutustu siihen, miten päiväkirjoja käytetään rahoitustapahtumien kirjaamisessa pääkirjanpitotileille sekä muille tileille, kuten pankki- ja toimittajatileille.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 08/29/2023
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# Yleisten päiväkirjojen käyttäminen

Useimmat rahoitustapahtumat kirjataan pääkirjanpitoon asiakirjojen, kuten ostolaskujen ja myyntitilausten välityksellä. Voit kuitenkin käsitellä myös liiketoimintaa, kuten:

* Osto
* Maksut
* Jaksotusten kirjaaminen toistuvien päiväkirjojen avulla
* Työntekijän kulujen palautus kirjaamalla päiväkirjarivit päiväkirjoissa  

Useimmat päiväkirjat perustuvat yleiseen päiväkirjaan ja voit käsitellä kaikki tapahtumat **Yleinen päiväkirja** -sivulla. Lue lisätietoja kohdasta [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).  

Voit kirjata esimerkiksi työntekijöiden kuluja hyvityksiin. Lue lisätietoja kohdasta [Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md).

[!INCLUDE [prod_short](includes/prod_short.md)] kuitenkin tarjoaa tietyille tapahtumille tarkoitettuja päiväkirjoja, kuten **maksupäiväkirjaa** maksujen rekisteröinnissä. Lisätietoja on kohdassa [Maksujen ja hyvitysten tallentaminen maksupäiväkirjaan](payables-how-post-payments-refunds.md).  

Käytät yleisiä päiväkirjoja taloustapahtumien kirjaamiseen pääkirjatileille ja useille muille tileille. Muut tilit sisältävät pankki-, asiakas-, toimittaja- ja työntekijätilit. Yleisen päiväkirjan avulla kirjaaminen luo tapahtumia kirjanpitotileille, vaikka esimerkiksi kirjaat päiväkirjan rivin asiakastilille. Tapahtuma kirjataan pääkirjanpidon myyntisaamiset-tilille kirjausryhmän kautta.

Päiväkirjaan lisäämäsi tiedot ovat väliaikaisia, ja niitä voidaan muuttaa niiden ollessa päiväkirjassa. Kun kirjaat päiväkirjan, tiedot siirretään yksittäisten tilien tapahtumiin, missä niitä ei voi muuttaa. Voit kuitenkin peruuttaa kirjattujen tapahtumien kohdistuksen tai kirjata peruuttavia tai korjaavia tapahtumia. Lue lisätietoja kohdasta [Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## Lisää konteksti yleisen päiväkirjan transaktioihin

Kun luot päiväkirjan, voit lisätä linkkejä, jotka antavat kontekstia sen transaktioille. Kun kirjaat päiväkirjan, [!INCLUDE [prod_short](includes/prod_short.md)] kopioi linkit kirjattuun päiväkirjaan ja kirjanpitotapahtumiin, jotka päiväkirja luo. Linkkien tarjoaminen voi esimerkiksi helpottaa tilintarkastajan elämää. Jos säilytät kuvia kulukuiteistasi yrityksesi Sharepoint-sivustossa, voit lisätä linkkejä tiedostoihin. Kun kirjaat päiväkirjan kulujen lähettämiseksi, tilintarkastajasi voi nopeasti päästä kuittitiedostoihin.

## Päiväkirjan mallien ja erien käyttäminen

Yleisen päiväkirjan malleja on useita. Kullakin päiväkirjamallilla on määritetty sivu, jossa on erityistoimintoja sekä näitä toimintoja varten tarvittavat kentät. Näitä sivuja ovat esimerkiksi **Maksujen täsmäytyskirjauskansio**, jossa käsitellään pankkimaksuja, ja **Maksupäiväkirja**, jossa maksetaan toimittajille tai maksetaan hyvitykset työntekijöille. Lisätietoja on kohdissa [Maksujen suorittaminen](payables-make-payments.md) ja [Asiakkaan maksujen täsmäyttäminen kassapäiväkirjan avulla tai asiakastapahtumista](receivables-how-apply-sales-transactions-manually.md).

Voit määrittää kullekin päiväkirjan mallille oman henkilökohtaisen päiväkirjan päiväkirjan eränä. Voit esimerkiksi määrittää maksupäiväkirjalle oman päiväkirjan erän, jolle on määritetty henkilökohtainen asettelu ja asetukset. Seuraava vihje on esimerkki päiväkirjan mukauttamisesta.

> [!TIP]  
> Jos valitset **Yleisen päiväkirjan erät** -sivun erän rivillä olevan **Ehdota vastasummaa** -valintaruudun, esimerkiksi saman asiakirjanumeron yleisen päiväkirjan rivien **Summa**-kenttään esitäytetään automaattisesti arvo, joka vaaditaan asiakirjan täsmäyttämiseksi. Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)]in arvoehdotusten salliminen](ui-let-system-suggest-values.md).

> [!TIP]
> Kenttiä voidaan lisätä päiväkirjoihin tai niitä voidaan poistaa mukauttamisen avulla. Lue lisää kohdasta [Työtilan mukauttaminen](ui-personalization-user.md).

### Yleisen päiväkirjan erien arvioiminen

Voit ottaa taustatarkistuksen käyttöön, mikä auttaa estämään viiveet kirjauksessa. Merkki ilmoittaa sinulle, kun käsittelemäsi talouspäiväkirjassa oleva virhe estää sinua kirjaamasta päiväkirjaa. **Yleisen päiväkirjan erä** -sivulla voit valita **taustan virheen tarkistuksen**, jos haluat, että [!INCLUDE[prod_short](includes/prod_short.md)] vahvistaa rahoituspäiväkirjat, kuten yleiset tai maksupäiväkirjat, kun käsittelet niitä.

Kun oikeellisuustarkistus otetaan käyttöön, **päiväkirjan tarkistuksen** -tietoruudussa näkyvät tämän rivin ja koko erän seurantakohteet. Vahvistus tehdään silloin, kun lataat rahoituspäiväkirjan erän ja kun valitset toisen päiväkirjarivin. Tietoruudun **Virheet yhteensä** -ruudussa näkyy [!INCLUDE[prod_short](includes/prod_short.md)]in löytämien virheiden kokonaismäärä, ja valitsemalla se voidaan avata virheiden yleiskatsaus.

Voit käyttää **Näytä rivit, joilla on seurantakohteita**- ja **Näytä kaikki rivit** -toimintoja, joilla voi siirtyä päiväkirjan riveillä, joilla on tai ei ole ongelmia. **Päiväkirjan rivitiedot** -ruudun avulla saat nopeasti yleiskuvan ja voit käyttää päiväkirjarivien, kuten KP-tilin, asiakkaan tai toimittajan, tietoja sekä tiettyjen tilien kirjausasetuksia.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## Tietoja päätileistä ja vastatileistä

Jos olet määrittänyt päiväkirjan erille oletusvastatilit **Yleiset päiväkirjat** -sivulla, vastatili täytetään automaattisesti, kun täytät **Tilinro**-kentän. Muussa tapauksessa täytä sekä **Tilinro**- että **Vastatilin nro** -kenttä manuaalisesti. Positiivinen summa **Summa**-kentässä veloitetaan päätililtä ja hyvitetään vastatilille. Negatiivinen summa hyvitetään päätilille ja veloitetaan vastatililtä.

> [!NOTE]  
> ALV lasketaan erikseen päätiliä varten ja vastatiliä varten, joten niillä voi olla eri ALV-prosentit.

## Toistuvien tapahtumien päiväkirjojen käyttäminen

Toistuva päiväkirja on yleinen päiväkirja, jossa on tiettyjä kenttiä sellaisten tapahtumien hallintaa varten, jotka kirjataan usein vähäisin muutoksin tai ilman muutoksia. Tällaisia tapahtumia ovat esimerkiksi vuokrat, tilaukset, sähkö ja lämpö. Toistuvien päiväkirjojen avulla voit kirjata kiinteitä ja muuttuvia summia ja määrittää automaattiset peruutustapahtumat kirjauspäivämäärän jälkeisenä päivänä. Kohdistusavaimet sallivat sinun jakaa toistuvat tapahtumat eri tileille. Lisätietoja on kohdassa [Toistuvien tapahtumien päiväkirjan summien kohdistaminen useisiin tileihin](#allocating-recurring-journal-amounts-to-several-accounts).

Toistuvan päiväkirjan avulla luot merkinnät, jotka kirjataan säännöllisesti vain kerran. Esimerkiksi tilit, dimensiot ja dimensioarvot säilyvät päiväkirjassa kirjaamisen jälkeen. Jos muutoksia tarvitaan, ne voidaan tehdä aina kirjauksen yhteydessä.

### Toistotapa-kenttä

**Toistotapa**-kenttä on tärkeä. Se määrittää, miten päiväkirjan rivin summaa käsitellään kirjauksen jälkeen. Jos esimerkiksi haluat käyttää samaa summaa aina kun kirjaat rivin, voit valita, että summa säilyy rivillä. Jos käytät rivillä samoja tilejä ja tekstiä, mutta summa vaihtelee kirjattaessa, voit valita sen vaihtoehdon, että summa poistuu riviltä kirjauksen jälkeen.

| Tehtävä | Katso |
| --- | --- |
|K Kiinteä|Summa säilyy päiväkirjan rivillä kirjauksen jälkeen.|
|M Muuttuva|Ohjelma poistaa summan päiväkirjan riviltä kirjauksen jälkeen.|
|S Saldo|Rivin tilille kirjattu summa jaetaan niiden tilien kesken, jotka on määritelty riville Yleisen päiväkirjan kohdistus -taulukossa. Tilin saldoksi tulee nolla. Muista täyttää **Kohdistus-%**-kenttä **Kohdistukset**-sivulla. Lisätietoja on kohdassa [Toistuvien tapahtumien päiväkirjan summien kohdistaminen useisiin tileihin](#allocating-recurring-journal-amounts-to-several-accounts).|
|KV Kiinteä vastakirjaus|Päiväkirjan rivillä oleva summa säilyy kirjauksen jälkeen, ja vastakirjaus kirjataan seuraavana päivänä.|
|MV Muuttuva vastakirjaus|Päiväkirjan rivillä oleva summa poistuu kirjauksen jälkeen, ja vastakirjaus kirjataan seuraavana päivänä.|
|VS Vastasaldo|Rivin tilille kirjattu summa jaetaan niiden tilien kesken, jotka on määritelty riville **Kohdistukset**-sivulla. Tilin saldoksi määritetään nolla ja vastatapahtuma kirjataan seuraavana päivänä.|
|SD Saldo dimensioittain|Päiväkirjan rivi kohdistaa kustannukset, jotka perustuvat KP-tilin saldoon dimensioittain. Sinua pyydetään asettamaan dimensiosuodattimia, joiden avulla lasketaan lähteen KP-tilin saldo dimensioittain, josta haluat kohdistaa kustannukset. Vaihtoehtoisesti voit valita **Aseta dimensiosuodattimet** -toiminnon myöhemmin.|
|VSD Vastasaldo dimensioittain|Päiväkirjan rivi kohdistaa kustannukset, jotka perustuvat KP-tilin vastasaldoon dimensioittain. Sinua pyydetään asettamaan dimensiosuodattimia, joiden avulla lasketaan lähteen KP-tilin saldo dimensioittain, josta haluat kohdistaa kustannukset. Voit myös valita **Aseta dimensiosuodattimet** -toiminnon myöhemmin.|

> [!NOTE]  
> ALV-kentät voidaan täyttää joko toistuvan päiväkirjan rivillä tai kohdistuspäiväkirjan rivillä, mutta ei molemmilla. Siten ne voidaan täyttää **Kohdistukset**-sivulla vain, jos vastaavia kenttiä ei ole täytetty toistuvassa päiväkirjassa.

### Toistotiheys-kenttä

Tämä pvm-kaava-kenttä määrittää, kuinka usein tapahtuma kirjataan päiväkirjan riville, ja se tulee täyttää. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#use-date-formulas).

#### Esimerkkejä

Jos päiväkirjan rivi tulee kirjata joka kuukausi, syötä 1K. Jokaisen kirjauksen jälkeen **Kirjauspvm.**-kentässä oleva päivämäärä päivitetään seuraavan kuukauden samaan päivään.

Jos haluat kirjata tapahtuman jokaisen kuukauden viimeisenä päivänä, voit toimia yhdellä seuraavista tavoista:

* Kirjaa ensimmäinen tapahtuma kuukauden viimeisenä päivänä syöttämällä 1P+1K-1P (1 päivä + 1 kuukausi - 1 päivä). Tämän laskukaavan avulla ohjelma laskee kirjauspäivämäärän oikein riippumatta siitä, kuinka monta päivää kussakin kuukaudessa on.

* Kirjaa ensimmäinen tapahtuma minä tahansa kuukauden päivänä syöttämällä 1K+NK. Tämän kaavan avulla kirjauspäivämäärä on yhden kokonaisen kuukauden + nykyisen kuukauden jäljellä olevien päivien verran myöhemmin.

### Vanhentumispäivämäärä -kenttä

Tämä kenttä määrittää päivämäärän, jolloin rivi kirjataan viimeisen kerran. Riviä ei kirjata tämän päivämäärän jälkeen.

Päättymispäivämäärä-kentän käyttämisessä on se etu, että rivi ei poistu päiväkirjasta heti. Voit syöttää myöhemmän päivämäärän, jotta voit käyttää riviä tulevaisuudessa.

Jos kenttä on tyhjä, rivi kirjataan joka kerta, kunnes se poistetaan päiväkirjasta.

### Toistuvien tapahtumien päiväkirjan summien kohdistaminen useisiin tileihin

Valitsemalla **Toistuva yleinen päiväkirja** -sivulla **Kohdistukset**-toiminto voidaan määrittää, miten toistuvien tapahtumien päiväkirjan rivin summat kohdistetaan useille tileille ja useisiin dimensioihin. Kohdistus toimii toistuvien tapahtumien päiväkirjan rivin vastatilin rivinä.

Kuten toistuvassa päiväkirjassa, voit syöttää kohdistuksen kerran ja se pysyy kohdistuspäiväkirjassa lähettämisen jälkeen. Sinun ei tarvitse syöttää summaa ja kohdistuksia aina, kun kirjaat toistuvan päiväkirjan rivin.

Jos Toistotapa-kenttään toistuvien tapahtumien päiväkirjassa on asetettu **Saldo** tai **Vasta-saldo**, ohjelma ei huomioi dimension arvokoodeja toistuvassa päiväkirjassa, kun tili on nollattu. Jos kohdistat toistuvan rivin dimension arvoon **Kohdistukset**-sivulla, syntyy vain yksi vastakirjaus.

> [!NOTE]
> Jos kohdistat toistuvan rivin, jolla on dimension arvon koodi, älä syötä samaa koodia **Kohdistukset**-sivulle. Jos teet niin, dimension arvot ovat virheellisiä.  

Toistuvan päiväkirjan arvot voidaan kohdistaa dimensioiden perusteella määrittämällä **Toistotapa**-kenttään **Saldo dimensioittain** tai **Vastasaldo dimensioittain**. Jos Toistotapa-kenttään toistuvien tapahtumien päiväkirjassa on asetettu **Saldo dimensioittain** tai **Vastasaldo dimensioittain**, ohjelma huomioi dimension arvokoodit toistuvassa päiväkirjassa, kun tili on nollattu. Jos kohdistat toistuvan rivin dimension arvoihin **Kohdistukset**-sivulla, ohjelma luo useita peruuttavia tapahtumia, jotka vastaavat niiden dimensioarvoyhdistelmien määrää, joista saldo koostuu. Jos kohdistat tilin saldon toistuvan päiväkirjan kautta, joka sisältää dimensioarvokoodin, käytä **Saldo dimensioittain**- tai **Vastasaldo dimensioittain** -kohteita, jotta voit varmistaa, että dimensioarvot tasapainotetaan tai palautetaan oikein lähdetililtä.  

Yritykselläsi on esimerkiksi pari liiketoiminta yksikköä ja kourallinen osastoja, jotka valvojat ovat asettaneet dimensioiksi. Ostolaskutapahtumaprosessin nopeuttamiseksi päätät vaatia, että ostoreskontran kirjaajat voivat syöttää vain liiketoimintayksikön dimensiot. Koska jokaisella liiketoimintayksiköllä on erityiset kohdistusavaimet Osasto-dimensiolle, esimerkiksi työntekijöiden lukumäärän perusteella, voit käyttää **SD Saldo dimensioittain**tai **VSD Vastasaldo dimensioittain** -toistumismenetelmiä ja kohdistaa kustannukset uudelleen kunkin liiketoimintayksikön osalta oikeisiin osastoihin kohdistusavainten perusteella.  

> [!NOTE]
> Kohdistusriveillä määritettyjä dimensioita ei lasketa automaattisesti, ja sinun täytyy määrittää, mitkä dimension arvot on määritettävä kohdistustileille. Jos haluat säilyttää linkin lähdetili- ja kohdistustilidimension välillä, on suositeltavaa käyttää sen sijaan [kustannuslaskennan](finance-about-cost-accounting.md) ominaisuuksia.

#### Esimerkki: Vuokramaksujen kohdistaminen eri osastoihin

Jos maksat vuokraa kuukausittain, olet syöttänyt summan kassatilille toistuvien tapahtumien päiväkirjan rivillä. **Kohdistukset**-sivulla voit jakaa Osasto-dimension avulla kulun useamman osaston kesken. Esimerkiksi kunkin osaston kattamien neliömetrien määrän mukaan. Laskenta perustuu kunkin rivin kohdistusprosenttiin. Voit jakaa eri tavoilla:

* Syötä eri tilit eri kohdistusriveille, jotta voit jakaa vuokrakulun useiden tiliesi kesken.
* Syötä sama tili, mutta käytä eri dimension arvokoodeja kunkin rivin osaston dimensiolle.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### Peruutuspäivämäärän laskenta

Kun jaksotusten kirjaamisessa käytetään toistuvia yleisiä päiväkirjoja jakson lopussa, on tärkeää, että peruutusten tapahtumat ovat täysin hallinnassa. **Toistuvat yleiset päiväkirjat** -sivulla **Peruutuspäivämäärän laskenta** -kentässä voit määrittää päivämäärän, jolloin peruutustapahtumat kirjataan peruutusten toistuvia menetelmiä käytettäessä.

#### Esimerkki

Jaksotukset kirjataan tyypillisesti päiväkirjan rivillä **kiinteiden**, **muuttuvien** tai **tasapainoisten** toistuvien menetelmien avulla. Päiväkirjarivin tilin kirjatun summan kirjauspäivämäärä lasketaan toistotiheyden mukaan. Vastatapahtuman kirjauspäivämäärä lasketaan **Peruutusten päivämäärän laskenta** -kentän avulla seuraavasti:

* Jos kenttä on tyhjä, vastatapahtuma kirjataan seuraavana päivänä.
* Jos kentässä on päivämääräkaava (esimerkiksi **5D** viideksi päiväksi), vastatapahtuma kirjataan siten, että kirjauspäivämäärä lasketaan peruutuspäivämäärän laskennan avulla.

> [!NOTE]
> Oletusarvon mukaan **peruutuspäivämäärän laskenta** -kenttä ei ole käytettävissä **Toistuvien yleisten päiväkirjojen** sivulla. Jos haluat käyttää kenttää, sinun täytyy lisätä se mukauttamalla sivua. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## Vakiopäiväkirjojen käyttäminen

Kun olet luonut päiväkirjan rivejä, joita todennäköisesti käytät myös vastaisuudessa, voit tallentaa rivit vakiopäiväkirjana, ennen kuin kirjaat rivit päiväkirjaan. Sama koskee nimikepäiväkirjoja sekä yleisiä päiväkirjoja.

> [!NOTE]
> Vakiopäiväkirjat eivät välttämättä sisällä kaikki kenttiä, jotka halutaan sisällyttää tuloksena oleviin tapahtumiin. Jos esimerkiksi maksujen rekisteröintiin käytetään vakioyleispäiväkirjaa, tapahtumat eivät sisällä Maksutavan koodi -kenttää.

> [!NOTE]  
> Vaikka seuraavissa toimenpiteissä viitataan nimikepäiväkirjaan, samat tiedot koskevat myös yleistä päiväkirjaa.

### Tallentaminen vakiopäiväkirjana

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirjat** ja valitse sitten vastaava linkki.
2. Lisää koodi yhdelle tai usealle päiväkirjariville.
3. Valitse ne päiväkirjan rivit, joita haluat käyttää uudelleen.
4. Valitse **Tallenna vakiopäiväkirjana** -toiminto.
5. Määritä **Tallenna vakionimikepäiväkirjana** -pyyntösivulla uusi tai aiemmin luotu vakionimikepäiväkirja, johon rivit on tarkoitus tallentaa.

    Jos olet aiemmin luonut vähintään yhden vakionimikepäiväkirjan ja haluat korvata jonkin niistä uusilla päiväkirjan riveillä, valitse haluamasi nimikepäiväkirjan koodi napsauttamalla **Koodi**-kenttää.
6. Valitset **OK** vahvistaaksesi, että haluat korvata olemassa olevan vakionimikepäiväkirjan sisällön.
7. Jos haluat tallentaa arvot vakiotuotepäiväkirjan **Yksikkömäärä** -kenttään, valitse **Tallenna yksikkömäärä** -kenttä.
8. Jos haluat tallentaa arvot **määrä**-kenttään, valitse **Tallenna määrä** -kenttä.
9. Valitse **OK** tallentaaksesi vakionimikepäiväkirjan.

Kun tallennat vakionimikepäiväkirjan, nimikepäiväkirjan sivu näkyy niin, että voit kirjata sen.

### Vakiopäiväkirjan käyttäminen uudelleen

> [!NOTE]
> Vakiopäiväkirjoissa ei ole aina samoja kenttiä kuin yleisissä päiväkirjoissa. Käytettäessä Hae vakiopäiväkirjat -toimintoa kenttien kopiointiin yleiseen päiväkirjaan, yleisessä päiväkirjassa voi olla vähemmän tietoja kuin siinä tapauksessa, että se olisi luotu manuaalisesti. 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirjat** ja valitse sitten vastaava linkki.
2. Valitse **Hae vakiopäiväkirjat** -toiminto.
3. Voit tarkastella vakionimikepäiväkirjaa, ennen kuin valitset sen uudelleenkäytettäväksi, valitsemalla **Näytä päiväkirja** -toiminto.

    Vakionimikepäiväkirjaan tehdyt muutokset otetaan käyttöön heti, ja ne tulevat näkyviin, kun vakionimikepäiväkirja avataan tai käytetään uudelleen. Varmista, että muutos on tarpeeksi tärkeä sovellettavaksi yleisesti. Muutoin tee tarvittava muutos nimikepäiväkirja, kun nimikepäiväkirjan vakiorivit on lisätty. Katso vaihe 4.
4. Valitse ensin **Vakionimikepäiväkirjat**-sivulla uudelleenkäytettävä vakiopäiväkirja ja sitten **OK**.

    Nimikepäiväkirja sisältää tallentamasi rivit. Jos nimikepäiväkirjassa on jo rivejä, uudet rivit tulevat näkyviin niiden jälkeen.

    Jos **Tallenna mittayksiköiden summa** -vaihtoehtoa ei ole otettu vaihtopainikkeella käyttöön päiväkirjan tallennuksen yhteydessä, vakiopäiväkirjasta lisättyjen rivien **Yksikkösumma**- kenttä sisältää nimikekortin **Yksikkökustannus**-kentän arvon.

    > [!NOTE]  
    > Jos **Tallenna yksikkösumma** tai **Tallenna määrä** otettiin käyttöön vaihtopainikkeella päiväkirjan tallennus yhteydessä, on varmistettava, että uudet arvot ovat oikein, ennen kuin ne kirjataan nimikepäiväkirjaan.
    >
    > Jos lisätyillä nimikepäiväkirjan riveillä on tallennettuja yksikkösummia, joita ei ole tarkoitus kirjata, se voidaan muuttaa nimikkeen nykyisen arvon mukaiseksi.

5. Valitse ensin muutettavat päiväkirjanrivit ja sitten **Laske yksikkösummat uudelleen** -toimintoa. Tämän toiminnon nimikkeen nykyinen yksikkökustannus tallennetaan Yksikkösumma-kenttään.
6. Valitse **Kirjaa**-toiminto.

## Asiakirjanumeroiden uudelleennumerointi päiväkirjoissa

Jos haluat varmistaa, että et saa kirjausvirheitä asiakirjan numerojärjestyksestä, voit käyttää **Numeroi asiakirjanumerot uudelleen**-toimintoa ennen päiväkirjan kirjaamista.

Kaikissa yleiseen päiväkirjaan perustuvissa päiväkirjoissa **Asiakirjanumero**-kenttä on muokattava, joten voit määrittää erilaisia asiakirjanumeroita päiväkirjan eri riveille tai saman asiakirjanumeron liittyville päiväkirjan riveille.

Jos **Nrosarja**-kenttä on kuitenkin täytetty päiväkirjaerässä, toiminnon kirjaaminen yleisessä päiväkirjassa vaatii, että asiakirjan numero yksittäisissä tai ryhmitetyissä päiväkirjarivissä on peräkkäisessä järjestyksessä. Kun valitset **Numeroi asiakirjat uudelleen** -toiminnon, asiaankuuluvat **Asiakirjanumero**-kentät päivitetään. Jos liittyvät päiväkirjarivit ryhmitellään asiakirjanumeron mukaan ennen kuin käytit toimintoa, ne pysyvät ryhmiteltyinä, mutt saatetaan kohdistaa eri asiakirjanumeroon.  

Tämä toiminto toimii myös suodatetuissa näkymissä.

Kaikissa asiakirjan numeroinneissa täytyy ottaa huomioon niihin liittyvät kohdistukset, kuten maksun kohdistus, joka on tehty asiakirjasta päiväkirjan rivillä toimittajan tiliin. Niinpä kyseisten tapahtumien **Kohdistetaan tunnisteeseen**- ja **Kohdistetaan asiakirjaan nro** -kentät voidaan päivittää.

### Asiakirjanumeroiden uudelleennumerointi päiväkirjoissa

Seuraavat toimenpiteet perustuvat **Yleinen päiväkirja** -sivuun, mutta niitä sovelletaan kaikkiin muihin päiväkirjoihin, jotka perustuvat yleiseen päiväkirjaan, kuten **Maksupäiväkirja**-sivu.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten vastaava linkki.
2. Kun olet valmis kirjaamaan päiväkirjan, valitse **Numeroi asiakirjanumerot uudelleen** -toiminto.

**Asiakirjanumero**-kentän arvoja muutetaan tarvittaessa siten, että yksittäisten tai ryhmitettyjen päiväkirjojen rivien asiakirjanumerot ovat peräkkäisessä järjestyksessä. Voit kirjata päiväkirjan, kun asiakirjat on numeroitu uudelleen.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/use-journals-dynamics-365-business-central/)

## Katso myös

[Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md)  
[Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md)  
[Kustannusten ja tulojen kohdistaminen](year-allocate-costs-income.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Varaston uudelleenarvostus uudelleenarvostuspäiväkirjassa](inventory-how-revalue-inventory.md)  
[Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja](inventory-how-count-adjust-reclassify.md)  
[Asiakkaan maksujen täsmäyttäminen kassapäiväkirjan avulla tai asiakastapahtumista](receivables-how-apply-sales-transactions-manually.md)  
[Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista](payables-how-apply-purchase-transactions-manually.md)  
[Konserniasiakirjojen ja -päiväkirjojen käyttäminen](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
