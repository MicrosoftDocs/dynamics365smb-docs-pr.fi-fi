---
title: Kirjaaminen suoraan pääkirjanpitoon yleisten päiväkirjojen avulla
description: Tutustu siihen, miten päiväkirjoja käytetään rahoitustapahtumien kirjaamisessa pääkirjanpitotileille sekä muille tileille, kuten pankki- ja toimittajatileille. Käytä toistuvia päiväkirjoja jaksotusten kirjaamiseen ja saldojen kohdistamiseen dimension arvojen mukaan.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: journals, recurring, accrual
ms.date: 02/15/2021
ms.author: edupont
ms.openlocfilehash: c6a2c6ed0c3fe163f64a3eb7d55f8e128f53a50d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393597"
---
# <a name="working-with-general-journals"></a>Yleisten päiväkirjojen käyttäminen

Useimmat rahoitustapahtumat kirjataan pääkirjanpitoon erityisten yritysasiakirjojen, kuten ostolaskujen ja myyntitilausten välityksellä. Voit myös prosessoida liiketoiminta-aktiviteetteja, kuten ostoja, maksamista, toistuvien päiväkirjojen käyttämistä kertymien kirjaamiseen tai työntekijöiden kulujen hyvitystä kirjaamalla päiväkirjarivejä [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen eri päiväkirjoihin.  

Useimmat päiväkirjat perustuvat *yleiseen päiväkirjaan* ja voit käsitellä kaikki tapahtumat **Yleinen päiväkirja** -sivulla. Lisätietoja on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).  

Voit esimerkiksi kirjata työntekijöiden itse maksamat liiketoimintaan liittyvät kulut myöhemmin hyvitettäväksi. Lisätietoja on kohdassa [Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md).

Useimmissa tapauksissa kuitenkin käyttää tietyille tapahtumille tarkoitettuja päiväkirjoja, kuten **maksupäiväkirjaa** maksujen rekisteröinnissä. Lisätietoja on kohdassa [Maksujen ja hyvitysten tallentaminen maksupäiväkirjaan](payables-how-post-payments-refunds.md).  

Yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamisessa suoraan pääkirjanpitotileille sekä muille tileille, kuten pankki-, asiakas-, toimittaja- ja työntekijätileille. Yleisen päiväkirjan avulla kirjaaminen luo aina tapahtumia kirjanpitotileille. Näin tapahtuu silloinkin, kun kirjataan esimerkiksi päiväkirjan rivi asiakkaan tilille, koska tapahtuma kirjataan pääkirjanpidon myyntisaamisten tilille kirjausryhmän kautta.

Päiväkirjaan lisäämäsi tiedot ovat väliaikaisia, ja niitä voi muuttaa niiden ollessa päiväkirjassa. Kun kirjaat päiväkirjan, tiedot siirretään yksittäisten tilien tapahtumiin, missä niitä ei voi muuttaa. Voit kuitenkin peruuttaa kirjattujen tapahtumien kohdistuksen tai kirjata peruuttavia tai korjaavia tapahtumia. Lisätietoja on kohdassa [Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Päiväkirjan mallit ja erien käyttäminen

Yleisen päiväkirjan malleja on useita. Kullakin päiväkirjamallilla on määritetty sivu, jossa on erityistoimintoja sekä näitä toimintoja varten tarvittavat kentät. Näitä sivuja ovat esimerkiksi **Maksujen täsmäytyskirjauskansio**, jossa käsitellään pankkimaksuja, ja **Maksupäiväkirja**, jossa maksetaan toimittajille tai maksetaan hyvitykset työntekijöille. Lisätietoja on kohdissa [Maksujen suorittaminen](payables-make-payments.md) ja [Asiakkaan maksujen täsmäyttäminen kassapäiväkirjan avulla tai asiakastapahtumista](receivables-how-apply-sales-transactions-manually.md).

Voit määrittää kullekin päiväkirjan mallille oman henkilökohtaisen päiväkirjan päiväkirjan eränä. Voit esimerkiksi määrittää maksupäiväkirjalle oman päiväkirjan erän, jolle on määritetty henkilökohtainen asettelu ja asetukset. Seuraava vihje on esimerkki päiväkirjan mukauttamisesta.

> [!TIP]  
> Jos valitset **Yleisen päiväkirjan erät** -sivun erän rivillä olevan **Ehdota vastasummaa** -valintaruudun, esimerkiksi saman asiakirjanumeron yleisen päiväkirjan rivien **Summa**-kenttään esitäytetään automaattisesti arvo, joka vaaditaan asiakirjan täsmäyttämiseksi. Lisätietoja on ohjeaiheessa [[!INCLUDE[prod_short](includes/prod_short.md)] saa ehdottaa arvoja](ui-let-system-suggest-values.md).

> [!TIP]
> Kenttiä voi lisätä päiväkirjoihin tai poistaa niitä **Mukauttaminen**-palkin avulla. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Yleisen päiväkirjan erien arvioiminen
Voit estää kirjauksen viivästymistä ottamalla käyttöön taustatarkistuksen, joka ilmoittaa, kun työstettävässä päiväkirjassa on virhe, joka estää päiväkirjan kirjaamisen. **Yleisen päiväkirjan erä** -sivulla voit valita **taustan virheen tarkistuksen**, jos haluat, että [!INCLUDE[prod_short](includes/prod_short.md)] vahvistaa rahoituspäiväkirjat, kuten yleiset tai maksupäiväkirjat, kun käsittelet niitä. 

Kun oikeellisuustarkistus otetaan käyttöön, **päiväkirjan tarkistuksen** -tietoruutu näkyy päiväkirjarivien vieressä, ja siinä näkyvät tämän rivin ja koko erän seurantakohteet. Vahvistus tehdään silloin, kun lataat rahoituspäiväkirjan erän ja kun valitset toisen päiväkirjarivin. Tietoruudun **kokonaisongelmat**-ruudussa näkyy [!INCLUDE[prod_short](includes/prod_short.md)]:n löytämien ongelmien kokonaismäärän, ja voit valita sen, kun haluat avata yleiskuvauksen ongelmista. 

Voit käyttää **Näytä rivit, joilla on seurantakohteita**- ja **Näytä kaikki rivit** -toimintoja, joilla voi siirtyä päiväkirjan riveillä, joilla on tai ei ole ongelmia. Uuden **päiväkirjan rivitiedot** -ruudun avulla saat nopeasti yleiskuvan ja voit käyttää päiväkirjarivien, kuten KP-tilin, asiakkaan tai toimittajan, tietoja sekä tiettyjen tilien kirjausasetuksia.     

### <a name="reversing-journals-to-correct-mistakes"></a>Päiväkirjojen peruuttaminen virheiden korjaamiseksi
Kun käsittelet päiväkirjoja, joissa on monta riviä ja jokin menee pieleen, on tärkeää, että virheet on helppo korjata. **Kirjattu yleisen päiväkirjan** sivu sisältää muutamia toimintoja, jotka voivat auttaa.

* **Kopioi valitut rivit päiväkirjaan** - Kopioi vain valitsemasi rivit.
* **Kopioi KP-rekisteri päiväkirjaan** - Kopioi kaikki rivit, jotka kuuluvat samaan KP-rekisteriin.

Näiden toimintojen avulla voit luoda kopion yleisen päiväkirjan rivistä tai erästä ja määrittää seuraavat tiedot:

* Päiväkirja, johon rivit kopioidaan
* Onko vastakkaisilla merkeillä (peruutuspvk)
* Eri kirjauspäivämäärä tai asiakirjan numero

Jos haluat sallia päiväkirjojen kirjausten kopioimisen yleisiin päiväkirjoihin **Yleiset päiväkirjamallit** -sivulle, valitse **Kopioi kirjatuille pvk-riveille** -valintaruutu. Sen jälkeen kun olet sallinut ihmisten kopioida kirjatut yleiset päiväkirjat, voit halutessasi poistaa kopioinnin käytöstä tiettyjen erien osalta.

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Päätilit ja vastatilit
Jos olet määrittänyt päiväkirjan erille oletusvastatilit **Yleiset päiväkirjat** -sivulla, vastatili täytetään automaattisesti, kun täytät **Tilinro**-kentän. Muussa tapauksessa täytä sekä **Tilinro**-kenttä että **Vastatilin nro** -kenttä manuaalisesti. Positiivinen summa **Summa**-kentässä veloitetaan päätililtä ja hyvitetään vastatilille. Negatiivinen summa hyvitetään päätilille ja veloitetaan vastatililtä.

> [!NOTE]  
>   ALV lasketaan erikseen päätiliä varten ja vastatiliä varten, joten niillä voi olla eri ALV-prosentit.

## <a name="working-with-recurring-journals"></a>Toistuvien tapahtumien päiväkirjojen käyttäminen
Toistuvien tapahtumien päiväkirja on yleinen päiväkirja, jossa on erityiskenttiä sellaisten tapahtumien hallintaa varten, jotka kirjataan usein vähäisin muutoksin tai ilman muutoksia. Näitä ovat esimerkiksi vuokra, lehtitilaukset, sähkö ja lämmitys. Käyttämällä näitä kenttiä toistuviin tapahtumiin, voit kirjata sekä vakiosummia että muuttuvia summia. Voit myös määrittää automaattiset peruutustapahtumat kirjauspäivämäärän jälkeisenä päivänä. Voit myös käyttää kohdistusavaimia ja jakaa toistuvat tapahtumat eri tileille. Lisätietoja on kohdassa [Toistuvien tapahtumien päiväkirjan summien kohdistaminen useisiin tileihin](#allocating-recurring-journal-amounts-to-several-accounts).

Toistuvassa päiväkirjassa säännöllisesti kirjattavat tapahtumat tarvitsee syöttää vain kerran. Siten tilit, dimensiot , dimension arvot ym. tiedot jotka syötät, säilyvät päiväkirjassa kirjauksen jälkeen. Jos sinun tarvitsee tehdä muutoksia, voit tehdä niitä jokaisen kirjauksen yhteydessä.

### <a name="recurring-method-field"></a>Toistotapa-kenttä

Tämä kenttä määrittää, miten päiväkirjan rivin summaa käsitellään kirjauksen jälkeen. Jos esimerkiksi haluat käyttää samaa summaa aina kun kirjaat rivin, voit valita, että summa säilyy rivillä. Jos käytät rivillä samoja tilejä ja tekstiä, mutta summa vaihtelee kirjattaessa, voit valita sen vaihtoehdon, että summa poistuu riviltä kirjauksen jälkeen.

| Tehtävä | Katso |
| --- | --- |
|K Kiinteä|Summa säilyy päiväkirjan rivillä kirjauksen jälkeen.|
|M Muuttuva|Ohjelma poistaa summan päiväkirjan riviltä kirjauksen jälkeen.|
|S Saldo|Rivin tilille kirjattu summa jaetaan niiden tilien kesken, jotka on määritelty riville Yleisen päiväkirjan kohdistus -taulukossa. Tilin saldoksi tulee siten nolla. Muista täyttää **Kohdistus-%**-kenttä **Kohdistukset**-sivulla. Lisätietoja on kohdassa [Toistuvien tapahtumien päiväkirjan summien kohdistaminen useisiin tileihin](#allocating-recurring-journal-amounts-to-several-accounts).|
|KV Kiinteä vastakirjaus|Päiväkirjan rivillä oleva summa säilyy kirjauksen jälkeen, ja vastakirjaus kirjataan seuraavana päivänä.|
|MV Muuttuva vastakirjaus|Päiväkirjan rivillä oleva summa poistuu kirjauksen jälkeen, ja vastakirjaus kirjataan seuraavana päivänä.|
|VS Vastasaldo|Rivin tilille kirjattu summa jaetaan niiden tilien kesken, jotka on määritelty riville **Kohdistukset**-sivulla. Tilin saldoksi määritetään nolla ja vastatapahtuma kirjataan seuraavana päivänä.|
|SD Saldo dimensioittain|Päiväkirjan rivi kohdistaa kustannukset, jotka perustuvat KP-tilin saldoon dimensioittain. Sinua pyydetään asettamaan dimensiosuodattimia, joiden avulla lasketaan lähteen KP-tilin saldo dimensioittain, josta haluat kohdistaa kustannukset. Vaihtoehtoisesti voit valita **Aseta dimensiosuodattimet** -toiminnon myöhemmin.|
|VSD Vastasaldo dimensioittain|Päiväkirjan rivi kohdistaa kustannukset, jotka perustuvat KP-tilin vastasaldoon dimensioittain. Sinua pyydetään asettamaan dimensiosuodattimia, joiden avulla lasketaan lähteen KP-tilin saldo dimensioittain, josta haluat kohdistaa kustannukset. Vaihtoehtoisesti voit valita **Aseta dimensiosuodattimet** -toiminnon myöhemmin.|

> [!NOTE]  
> ALV-kentät voidaan täyttää joko toistuvan päiväkirjan rivillä tai kohdistuspäiväkirjan rivillä, mutta ei molemmilla. Siten ne voidaan täyttää **Kohdistukset**-sivulla vain, jos vastaavia kenttiä ei ole täytetty toistuvassa päiväkirjassa.

### <a name="recurring-frequency-field"></a>Toistotiheys-kenttä
Tämä kenttä määrittää, kuinka usein päiväkirjarivillä oleva tapahtuma kirjataan. Se on Päivämäärän kaava -kenttä, joka on täytettävä toistuvien tapahtumien päiväkirjan riveille. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Esimerkkejä
Jos päiväkirjan rivi tulee kirjata joka kuukausi, syötä 1K. Jokaisen kirjauksen jälkeen **Kirjauspvm.**-kentässä oleva päivämäärä päivitetään seuraavan kuukauden samaan päivään.

Jos haluat kirjata tapahtuman jokaisen kuukauden viimeisenä päivänä, voit toimia yhdellä seuraavista tavoista:

- Kirjaa ensimmäinen tapahtuma kuukauden viimeisenä päivänä syöttämällä 1P+1K-1P (1 päivä + 1 kuukausi - 1 päivä). Tämän laskukaavan avulla ohjelma laskee kirjauspäivämäärän oikein riippumatta siitä, kuinka monta päivää kussakin kuukaudessa on.

- Kirjaa ensimmäinen tapahtuma minä tahansa kuukauden päivänä syöttämällä 1K+NK. Tämän kaavan avulla kirjauspäivämäärä on yhden kokonaisen kuukauden + nykyisen kuukauden jäljellä olevien päivien verran myöhemmin.

### <a name="expiration-date-field"></a>Vanhentumispäivämäärä -kenttä
Tämä kenttä määrittää päivämäärän, jolloin rivi kirjataan viimeisen kerran. Riviä ei kirjata tämän päivämäärän jälkeen.

Kentän käyttämisessä on se etu, että rivi ei poistu päiväkirjasta heti, ja voit aina korvata nykyisen vanhentumispäivämäärän myöhäisemmällä, niin että riviä voi käyttää jatkossakin.

Jos kenttä on tyhjä, rivi kirjataan joka kerta, kun kirjaat siihen asti, kun se poistetaan päiväkirjasta.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Toistuvien tapahtumien päiväkirjan summien kohdistaminen useisiin tileihin

Valitse **Toistuva yleinen päiväkirja** -sivulla **Kohdistukset**-toiminto, kun haluat nähdä, miten toistuvien tapahtumien päiväkirjan rivin summat on kohdistettu useille tileille ja useisiin dimensioihin. Toiminnon avulla voit myös hallita näitä summia. Huomaa, että kohdistus toimii toistuvien tapahtumien päiväkirjan rivin vastatilin rivinä.

Kuten toistuvien tapahtumien päiväkirjassa, sinun tarvitsee syöttää kohdistus vain kerran. Kohdistus säilyy kohdistuspäiväkirjassa kirjauksen jälkeen, joten sinun ei tarvitse syöttää summia ja kohdistuksia aina kun kirjaat toistuvan päiväkirjan rivin.

Jos *Toistotapa*-kenttään toistuvien tapahtumien päiväkirjassa on asetettu **Saldo** tai **Vastasaldo**, ohjelma ei huomioi mitään dimension arvokoodeja toistuvassa päiväkirjassa, kun tili on nollattu. Jos siis kohdistat toistuvan rivin useampaan dimension arvoon **Kohdistukset**-sivulla, syntyy vain yksi vastakirjaus. Jos kohdistat toistuvan rivin, jolla on dimension arvon koodi, et voi syöttää samaa koodia **Kohdistukset**-sivulle. Jos teet niin, dimension arvot ovat virheellisiä.  

Jos haluat kohdistaa toistuvan päiväkirjan arvot dimensioiden perusteella, määritä **Toistotapa**-kenttään sen sijaan **Saldo dimensioittain** tai **Vastasaldo dimensioittain**. Jos Toistotapa-kenttään toistuvien tapahtumien päiväkirjassa on asetettu **Saldo dimensioittain** tai **Vastasaldo dimensioittain**, ohjelma huomioi dimension arvokoodit toistuvassa päiväkirjassa, kun tili on nollattu. Jos kohdistat toistuvan rivin useisiin dimension arvoihin **Kohdistukset**-sivulla, ohjelma luo useita peruuttavia tapahtumia, jotka vastaavat niiden dimensioarvoyhdistelmien määrää, joista saldo koostuu. Jos kohdistat tilin saldon toistuvan päiväkirjan kautta, joka sisältää dimensioarvokoodin, käytä **Saldo dimensioittain**- tai **Vastasaldo dimensioittain** -kohteita, jotta voit varmistaa, että dimensioarvot tasapainotetaan tai palautetaan oikein lähdetililtä.  

Yritykselläsi on esimerkiksi pari liiketoiminta yksikköä ja kourallinen osastoja, jotka valvojat ovat asettaneet dimensioiksi. Ostolaskutapahtumaprosessin nopeuttamiseksi päätät vaatia, että ostoreskontran kirjaajat voivat syöttää vain liiketoimintayksikön dimensiot. Koska jokaisella liiketoimintayksiköllä on erityiset kohdistusavaimet Osasto-dimensiolle, esimerkiksi työntekijöiden lukumäärän perusteella, voit käyttää **SD Saldo dimensioittain** tai **VSD Vastasaldo dimensioittain** -toistumismenetelmiä ja kohdistaa kustannukset uudelleen kunkin liiketoimintayksikön osalta oikeisiin osastoihin kohdistusavainten perusteella.  

> [!NOTE]
> Kohdistusriveillä määritettyjä dimensioita ei lasketa automaattisesti, ja sinun täytyy määrittää, mitkä dimension arvot on määritettävä kohdistustileille. Jos haluat säilyttää linkin lähdetili- ja kohdistustilidimension välillä, on suositeltavaa käyttää sen sijaan [kustannuslaskennan](finance-about-cost-accounting.md) ominaisuuksia.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Esimerkki: Vuokramaksujen kohdistaminen eri osastoihin
Jos maksat vuokraa joka kuukausi, olet syöttänyt vuokrasumman kassatilille toistuvien tapahtumien päiväkirjan rivillä. **Kohdistukset**-sivulla voit jakaa kulun useamman osaston (Osasto-dimension) kesken osastojen pinta-alaneliöiden mukaan. Laskenta perustuu kunkin rivin kohdistusprosenttiin. Voit syöttää erilaisia tilejä jokaiselle eri kohdistusriville (jos myös vuokra jaetaan useammalle tilille) tai voit syöttää saman tilin erilaisilla dimension arvokoodeilla Osasto-dimension jokaisella rivillä.

### <a name="reversal-date-calculation"></a>Päinvastainen päivämäärän laskenta
Kun jaksotusten kirjaamisessa käytetään toistuvia yleisiä päiväkirjoja jakson lopussa, on tärkeää, että peruutusten tapahtumat ovat täysin hallinnassa. **Toistuvat yleiset päiväkirjat** -sivulla **Peruutuspäivämäärän laskenta** -kentässä voit määrittää päivämäärän, jolloin peruutustapahtumat kirjataan peruutusten toistuvia menetelmiä käytettäessä.

#### <a name="example"></a>Esimerkki
Jaksotukset kirjataan yleensä päiväkirjan rivillä kiinteiden, muuttuvien tai tasapainoisten toistuvien menetelmien avulla. Päiväkirjarivin tilin kirjatun summan kirjauspäivämäärä lasketaan toistotiheyden mukaan. Vastatapahtuman kirjauspäivämäärä lasketaan **Peruutusten päivämäärän laskenta** -kentän avulla seuraavasti:

* Jos kenttä on tyhjä, vastatapahtuma kirjataan seuraavana päivänä.
* Jos kentässä on päivämääräkaava (esimerkiksi **5D** viideksi päiväksi), vastatapahtuma kirjataan siten, että kirjauspäivämäärä lasketaan peruutuspäivämäärän laskennan avulla.

> [!NOTE]
> Oletusarvon mukaan **peruutuspäivämäärän laskenta** -kenttä ei ole käytettävissä **Toistuvien yleisten päiväkirjojen** sivulla. Jos haluat käyttää kenttää, sinun täytyy lisätä se mukauttamalla sivua. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## <a name="working-with-standard-journals"></a>Vakiopäiväkirjojen käyttäminen
Kun olet luonut päiväkirjan rivejä, joita todennäköisesti käytät myös vastaisuudessa, voit tallentaa rivit vakiopäiväkirjana, ennen kuin kirjaat rivit päiväkirjaan. Tämä toiminto koskee nimikepäiväkirjoja sekä yleisiä päiväkirjoja.

> [!NOTE]  
>   Vaikka seuraavassa puhutaan nimikepäiväkirjasta, samat tiedot koskevat myös yleistä päiväkirjaa.

### <a name="to-save-a-standard-journal"></a>Tallentaminen vakiopäiväkirjana
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikepäiväkirjat** ja valitse sitten liittyvä linkki.
2. Lisää koodi yhdelle tai usealle päiväkirjariville.
3. Valitse ne päiväkirjan rivit, joita haluat käyttää uudelleen.
4. Valitse **Tallenna vakiopäiväkirjana** -toiminto.
5. Määritä **Tallenna vakionimikepäiväkirjana** -pyyntösivulla uusi tai aiemmin luotu vakionimikepäiväkirja, johon rivit on tarkoitus tallentaa.

    Jos olet aiemmin luonut vähintään yhden vakionimikepäiväkirjan ja haluat korvata jonkin niistä uusilla päiväkirjan riveillä, valitse haluamasi vakionimikepäiväkirjan koodi napsauttamalla Koodi-kenttää.
6. Kun valitset **OK**, ohjelma pyytää varmistamaan aiemmin luodun vakionimikepäiväkirjan ja kaiken sen sisällön korvaamisen.
7. Valitse **Tallenna yksikkösumma** -kenttä, jos haluat tallentaa arvot vakionimikepäiväkirjan **Yksikkösumma** -kenttään.
8. Valitse **Tallenna määrä** -kenttä, jos sovelluksen on tarkoitus tallentaa arvot **Määrä**-kenttään.
9. Valitse **OK**-painike tallentaaksesi vakionimikepäiväkirjan.

Kun olet tallentanut vakionimikepäiväkirjan, ohjelma siirtyy takaisin Nimikepäiväkirja-sivulle, jossa voit kirjata rivit. Tämän jälkeen voit kirjata samat tai vastaavat rivit vaivattomasti aina, kun tilanne sitä edellyttää.

### <a name="to-reuse-a-standard-journal"></a>Vakiopäiväkirjan käyttäminen uudelleen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikepäiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse **Hae vakiopäiväkirjat** -toiminto.

    Näkyviin tulee Vakionimikepäiväkirjat-sivu, jossa on kaikkien luotujen vakionimikepäiväkirjojen koodit ja kuvaukset.
3. Voit tarkastella vakionimikepäiväkirjaa, ennen kuin valitset sen uudelleenkäytettäväksi, valitsemalla **Näytä päiväkirja** -toiminto.

    Vakionimikepäiväkirjaan tekemäsi muutokset toteutetaan heti. Ne ovat siellä, kun kyseinen vakionimikepäiväkirja seuraavan kerran avataan tai sitä käytetään uudelleen. Tämän vuoksi sinun täytyy olla varma, että muutos on tarpeeksi tärkeä sovellettavaksi yleisesti. Muutoin tee tarvittava muutos nimikepäiväkirja, kun nimikepäiväkirjan vakiorivit on lisätty. Lisätietoja on alla vaiheessa 4.
4. Valitse ensin **Vakionimikepäiväkirjat**-sivulla uudelleenkäytettävä vakiopäiväkirja ja sitten **OK**-painike.

    Vakiopäiväkirja täytetään riveillä, jotka olet tallentanut vakionimikepäiväkirjana. Jos nimikepäiväkirjassa on entuudestaan päiväkirjarivejä, lisättävät rivit sijoitetaan aiemmin luotujen päiväkirjarivien alle.

    Jos **Tallenna yksikkösumma** -kenttään ei lisätä valintamerkkiä **Tallenna vakionimikepäiväkirjana** -toiminnon suorittamisen yhteydessä, päiväkirjasta lisättyjen rivien **Yksikkösumma**-kenttä täytetään automaattisesti nimikkeen nykyisellä arvolla (joka kopioidaan nimikkeen kortin **Yksikkökustannus**-kentästä).

    > [!NOTE]  
    >   Jos lisäät **Tallenna yksikkösumma**- ja/tai **Tallenna määrä** -kenttään valintamerkin, varmista, että lisätyt arvot ovat oikein tämän varastonmuutoksen osalta ennen niiden kirjaamista nimikepäiväkirjaan.

    Jos lisätyillä nimikepäiväkirjan riveillä on tallennettuja yksikkösummia, joita ei ole tarkoitus kirjata, voit muuttaa summan nopeasti nimikkeen nykyisen arvon mukaiseksi seuraavasti:

6. Valitse ensin muutettavat päiväkirjanrivit ja sitten **Laske yksikkösummat uudelleen** -toimintoa. Tällöin nimikkeen nykyinen yksikkökustannus tallennetaan Yksikkösumma-kenttään.
7. Valitse **Kirjaa**-toiminto.

## <a name="to-renumber-document-numbers-in-journals"></a>Asiakirjanumeroiden uudelleennumerointi päiväkirjoissa
Jos haluat varmistaa, että et saa kirjausvirheitä asiakirjan numerojärjestyksestä, voit käyttää **Numeroi asiakirjanumerot uudelleen**-toimintoa ennen päiväkirjan kirjaamista.

Kaikissa yleiseen päiväkirjaan perustuvissa päiväkirjoissa **Asiakirjanumero**-kenttä on muokattava, joten voit määrittää erilaisia asiakirjanumeroita päiväkirjan eri riveille tai saman asiakirjanumeron liittyville päiväkirjan riveille.

Jos **Nrosarja**-kenttä on kuitenkin täytetty päiväkirjaerässä, toiminnon kirjaaminen yleisessä päiväkirjassa vaatii, että asiakirjan numero yksittäisissä tai ryhmitetyissä päiväkirjarivissä on peräkkäisessä järjestyksessä. Jos haluat varmistaa, että et saa kirjausvirheitä asiakirjan numerojärjestyksestä, voit käyttää **Numeroi asiakirjanumerot uudelleen**-toimintoa ennen kuin kirjasit päiväkirjan. Jos liittyvät päiväkirjarivit ryhmitellään asiakirjanumeron mukaan ennen kuin käytit toimintoa, ne pysyvät ryhmiteltyinä, mutt saatetaan kohdistaa eri asiakirjanumeroon.

Tämä toiminto toimii myös suodatetuissa näkymissä.

Kaikissa asiakirjan numeroinneissa täytyy ottaa huomioon niihin liittyvät kohdistukset, kuten maksun kohdistus, joka on tehty asiakirjasta päiväkirjan rivillä toimittajan tiliin. Niinpä kyseisten tapahtumien **Kohdistetaan tunnisteeseen**- ja **Kohdistetaan asiakirjaan nro** -kentät voidaan päivittää.

Seuraavat toimenpiteet perustuvat **Yleinen päiväkirja** -sivuun, mutta niitä sovelletaan kaikkiin muihin päiväkirjoihin, jotka perustuvat yleiseen päiväkirjaan, kuten **Maksupäiväkirja**-sivu.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.
2. Kun olet valmis kirjaamaan päiväkirjan, valitse **Numeroi asiakirjanumerot uudelleen** -toiminto.

**Asiakirjanumero**-kentän arvoja muutetaan tarvittaessa siten, että yksittäisten tai ryhmitettyjen päiväkirjojen rivien asiakirjanumerot ovat peräkkäisessä järjestyksessä. Voit kirjata päiväkirjan, kun asiakirjat on numeroitu uudelleen.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md)  
[Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md)  
[Kustannusten ja tulojen kohdistaminen](year-allocate-costs-income.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Varaston uudelleenarvostus uudelleenarvostuspäiväkirjassa](inventory-how-revalue-inventory.md)  
[Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja](inventory-how-count-adjust-reclassify.md)  
[Asiakkaan maksujen täsmäyttäminen kassapäiväkirjan avulla tai asiakastapahtumista](receivables-how-apply-sales-transactions-manually.md)  
[Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista](payables-how-apply-purchase-transactions-manually.md)  
[Konserniasiakirjojen ja -päiväkirjojen käyttäminen](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]