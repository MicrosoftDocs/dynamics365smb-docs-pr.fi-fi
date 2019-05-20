---
title: Usean yrityksen tietojen konsolidointi | Microsoft Docs
description: Hae yhteenvetonäkymä kaikkien yritystesi taloudellisesta tilanteesta.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: cdfcd99c484176d709288f2cf27f0a04e43bdf52
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244467"
---
# <a name="consolidating-financial-data-from-multiple-companies"></a>Usean yrityksen kirjanpitotietojen konsolidoiminen
Jos sinulla on useita [!INCLUDE[d365fin](includes/d365fin_md.md)]-yrityksiä, kirjanpitäjän roolikeskuksen Konsolidoitu alust. tulos/tase -raportti antaa yleiskuvan liiketoiminnan taloudellisesta tilanteesta.  

Raportti yhdistää kunkin yrityksen kirjanpitotapahtumat uuteen yritykseen, joka luodaan konsolidoituja tietoja varten. Tätä yritystä kutsutaan yleensä konsolidoiduksi yritykseksi. Konsolidoitu yritys on vain konsolidoitujen tietojen säilö, eikä se sisällä muita liiketoimintatietoja. Konsolidoituun yritykseen sisällytettävät yritykset ovat raportin **liiketoimintayksiköitä**.

Kirjanpitotietojen konsolidoiminen voi olla erityisen tärkeää konsernin sisäisissä prosesseissa. Lisätietoja on ohjeaiheessa [Konsernitapahtumien hallinta](intercompany-manage.md).

Voit konsolidoida  

* yrityksiä, joissa on käytössä erilaiset tilikartat  
* yrityksiä, joissa on käytössä erilaiset tilikaudet ja valuutat  
* yrityksen taloudelliset tiedot kokonaan tai tietyn prosenttiosuuden niistä
* käyttämällä eri valuuttakursseja yksittäisillä KP-tileillä.

Yritysten monimutkaisuus määrittää, kumpaa tapaa käytetään raportin määrittämiseen:

* Jos et tarvitse lisäasetuksia, kuten vain osittain omistamasi yrityksen sisällyttämistä, voit määrittää konsolidoinnin nopeasti käyttämällä ohjattua **Yrityksen konsolidointi** -määritystä. Opas auttaa suorittamaan perusvaiheet.
* Jos tarvitset lisäasetuksia, voit määrittää konsolidoidun yrityksen ja liiketoimintayksiköt itse.

## <a name="to-do-a-simple-consolidation-setup"></a>Yksinkertaisen konsolidoinnin asetukset
Jos kyse on suoraviivaisesta konsolidoinnista, koska esimerkiksi omistat kokonaan konsolidoitavat liiketoimintayksiköt, ohjattu **Yrityksen konsolidointi** -määritys auttaa seuraavissa vaiheissa:

* Valitse, luodaanko uusi konsolidoitu yritys vai konsolidoidaanko tiedot yritykseen, joka on jo luotu konsolidointia varten. Yrityksessä ei saa olla tapahtumia.
* Esikatsele tulokset. [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että päätiedot ja tapahtumat voidaan siirtää konsolidoituun yritykseen.

Käytä asetusten ohjattua määritystä seuraavasti:

1. Valitse **kirjanpitäjän** roolikeskuksessa **Asetusten ohjattu määritys** -toiminto.
2. Valitse **Määritä konsolidoinnin raportointi** ja tee vaiheet asetusten ohjatun määrityksen mukaisesti.

## <a name="to-do-an-advanced-consolidation-setup"></a>Konsolidoinnin lisäasetukset
Jos konsolidoinnissa on käytettävä lisäasetuksia, voit määrittää konsolidoinnin manuaalisesti. Sinulla voi esimerkiksi olla yrityksiä, jotka omistat vain osittain, tai et ehkä halua sisällyttää tiettyjä yrityksiä konsolidointiin. Konsolidoitu yritys määritetään samalla tavalla kuin muutkin yritykset. Lisätietoja on ohjeaiheessa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).  

Voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]issa konsolidoitavien yritysten luettelon, tarkistaa laskentatiedot ennen konsolidointia, tuoda tiedostoja ja luoda konsolidointiraportteja.  

1. Kirjaudu konsolidoituun yritykseen.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten liittyvä linkki.  
3. Valitse **Uusi** ja täytä sitten tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!IMPORTANT]
> Kun täytät **Aloituspvm**- ja **Lopetuspvm** -kentät, varmista, että noudata kenttiä, varmista, että noudatat liiketoimintayksikön eikä emoyrityksen tilikausien GAAP-sääntöjä.

Jos liiketoimintayksikkösi käyttää ulkomaan valuuttaa, sinun on määritettävä konsolidoinnissa käytettävä valuuttakurssi. Sinun täytyy myös syöttää konsolidointitiedot liiketoimintayksikön KP-tileistä. Nämä prosessit käsitellään seuraavissa osissa.

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a>Kirjanpitotilien valmisteleminen konsolidointia varten
Jos liiketoimintayksikön tilikartta poikkeaa konsolidoidun yrityksen tilikartasta, kirjanpitotilit on valmisteltava konsolidointia varten. Voit määrittää tilit, joihin debet- ja kreditsummat kirjataan, ja menetelmän, jolla valuutat muunnetaan konsolidoidussa yrityksessä. Tästä on hyötyä esimerkiksi silloin, jos raportti suoritetaan usein.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Avaa tilin kortti ja täytä **Konsolidointi**-pikavälilehden kentät.

### <a name="to-specify-exchange-rates-for-consolidations"></a>Valuutan vaihtokurssien määrittäminen konsolidoiduissa yrityksissä
Jos liiketoimintayksikön käyttämä valuutta ei ole sama kuin konsolidoidun yrityksen käyttämä valuutta, kullekin tilille on määritettävä vaihtokurssimenetelmä ennen konsolidointia. Kunkin tilin **Konsolid. muuntomenetelmä** -kentän sisältö määrittää vaihtokurssin. Määritä kunkin liiketoimintayksikön **Valuutan vaihtok.taulu** -kentässä, käytetäänkö konsolidoinnissa liiketoimintayksikön vai konsolidoidun yrityksen vaihtokursseja. Jos käytät konsolidoidun yrityksen vaihtokursseja, voit muuttaa liiketoimintayksikön vaihtokursseja. Jos liiketoimintayksikön kortin **Valuutan vaihtok.taulu** -kentässä on arvo **Paikallinen**, voit muuttaa vaihtokurssia liiketoimintayksikön kortista. Vaihtokurssit kopioidaan **Valuutan vaihtokurssi** -taulukosta, mutta voit muuttaa niitä ennen konsolidointia.

Seuraavassa taulukossa käsitellään tileillä käytettäviä vaihtokurssimenetelmiä.

|Vaihtokurssi | Tyypillinen käyttö |
|---|---|
|Keskikurssi (manuaalinen) | Konsolidoitavan jakson keskikurssi lasketaan manuaalisesti. Laske keskikurssi joko aritmeettisena keskiarvona tai parhaana arvioina ja määritä kunkin liiketoimintayksikön tulos. Käytetään tuloslaskelmatileillä.|
|Loppukurssi | Käytetään tasetileillä.|
|Viimeinen loppukurssi | Valuuttamarkkinoiden kurssi päivämääränä, jona tasetta tai tuloslaskelmaa valmistellaan. Käyttäjä antaa tämän kurssin kullekin liiketoimintayksikölle. Käytetään tasetileillä.|
|Historiallinen kurssi | Vaihtokurssi tapahtuman suoritusajankohtana.|
|Yhdistelmäkurssi | Kuluvan jakson summat muunnetaan keskikurssin mukaan ja lisätään aiemmin kirjattuun saldoon konsolidoidussa yrityksessä. Tätä tapaa käytetään tavallisesti edellisten tilikausien voittojen tileissä, koska ne sisältävät eri jaksojen summia ja ovat siksi eri vaihtokurssien mukaan muunnettujen summien yhdistelmiä.|
|Pääomakurssi | Tämä kurssi muistuttaa **yhdistelmäkurssia**. Erot kirjataan erillisille kirjanpitotileille.|   

Liiketoimintayksiköiden vaihtokurssit määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten liittyvä linkki.  
2. Valitse ensin **Liiketoimintayksiköiden luettelo** -sivulla liiketoimintayksikkö ja sitten **Keskikurssi (manuaalinen)** -toiminto.   
3. **Muuta vaihtokurssi** -sivun **Suhteellinen vaihtokurssi** -kentän sisältö on kopioitu **Valuutan vaihtokurssi** -taulukosta. Sisältöön voi kuitenkin tehdä muutoksia. Sulje sivu.  
4. Valitse **Loppukurssi**-toiminto.  
5. Anna vaihtokurssi **Suhteellinen vaihtokurssisumma** -kentässä

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a>Yrityksen jättäminen konsolidoinnin ulkopuolelle
Jos et halua sisällyttää liiketoimintayksikköä konsolidointiin, voit jättää sen pois. Se onnistuu siirtymällä liiketoimintayksikön korttiin ja poistamalla **Konsolidoi**-valintaruudun valinta.

### <a name="to-include-a-partially-owned-company-in-consolidation"></a>Osittain omistetun yrityksen sisällyttäminen konsolidointiin
Jos omistat osan yrityksestä, voit sisällyttää kustakin tapahtumasta sen prosenttiosuuden, joka vastaa omistamaasi osuutta yrityksestä. Jos esimerkiksi omistat yrityksestä 70 prosenttia, konsolidointiin sisältyy lasku 70 dollaria 100 dollarin laskusta. Voit määrittää omistusosuuden yrityksestä siirtymällä liiketoimintayksikön korttiin ja antamalla prosenttiosuuden **Konsolidointi-%** -kentässä.  

### <a name="to-test-the-data-before-you-consolidate"></a>Tietojen testaus ennen konsolidointia
Voit testata tiedot, ennen kuin siirrät ne konsolidoituun yritykseen. [!INCLUDE[d365fin](includes/d365fin_md.md)] etsii eroavaisuuksia liiketoimintayksiköiden tietojen ja konsolidoidun yrityksen tietojen välillä. Tarkistettavia kohteita ovat esimerkiksi erot tilinumeroiden tai dimensiokoodien välillä. Virheet on korjattava ennen raportin suorittamista. Voit testata tietokannan. Jos tuot tietoja XML-tiedostosta, voit testata myös tiedoston.   

1. Avaa konsolidoitu yritys.  
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten liittyvä linkki.  
3. Tee jompikumpi seuraavista toimista:  

    * Testaa tiedosto valitsemalla **Testaa tiedosto** -toiminto, antamalla testattavan tiedoston nimen ja valitsemalla **Tulosta**.  
    * Voit testata tietokannan valitsemalla **Testaa tietokanta**.  

## <a name="to-run-the-consolidation"></a>Konsolidoinnin suorittaminen
Kun olet testannut tiedot, voit siirtää ne konsolidoituun yritykseen.  

1. Kirjaudu konsolidoituun yritykseen.  
2. Valitse **kirjanpitäjän roolikeskuksessa** **Suorita konsolidointi** -toiminto.  
3. Täytä vaaditut kentät.  
4. Valitse **Jossa**-kentässä ensin **Yrityksen nimi** ja sitten konsolidoitu yritys **on**-kentässä.

## <a name="to-eliminate-repeated-transactions"></a>Toistuvien tapahtumien estäminen
Kaikkien yritysten konsolidoinnin jälkeen on etsittävä tapahtumat, jotka on tallennettu useaan yritykseen. Ne on sen jälkeen poistettava kirjaamalla eliminointitapahtumat.

Sisäisten liiketapahtumien eliminointien käsittely on manuaalinen prosessi. Toimi seuraavasti:
1. Etsi tapahtumat, joita on mahdollisesti muutettava, ja anna ne eliminoivat yleisen päiväkirjan rivit.
2. **Sis. liiketapaht. eliminoinnit** -raportin suorittaminen auttaa arvioimaan yleisen päiväkirjan rivien vaikutuksen ennen kirjaamista.
3. Kirjaa muutostapahtumat.

**Sis. liiketapaht. eliminoinnit** raportissa näkyy alustava saldon, jolla voit simuloida tapahtumien poistamisen seuraukset vertaamalla konsolidoidun yrityksen tapahtumia yleiseen päiväkirjaan lisättyihin eliminointeihin.

Ennen kuin liiketoimintayksikkö voidaan sisällyttää eräajoon, se on luotava **Liiketoimintayksiköt** -sivulla ja **Konsolidoi**-kenttä on valittava.

Jokainen tili on omalla rivillään (noudattaen tilikartan rakennetta). Tiliä ei ole näkyvissä, jos rivin kaikki summat ovat 0. Jokaisesta tilistä näkyy seuraavat tiedot:

* Tilinumero
* Tilin nimi.
* Jos olet valinnut vähintään yhden liiketoimintayksikön koodin pyyntösivun **Liiketoimintayksikön koodi** -kentässä, niin konsolidoidun yrityksen kokonaissumma näkyy siten, että siitä on vähennetty valitut liiketoimintayksiköt ja poistot. Jos et ole täyttänyt **Liiketoimintayksikön koodi** -kenttää, konsolidoidun yrityksen kokonaissumma näkyy siten että siitä on vähennetty poistot.
* Jos olet valinnut liiketoimintayksikön koodin pyyntösivun **Liiketoimintayksikön koodi** -kentässä, kokonaissumma on liiketoimintayksiköstä tuotujen tapahtumien kokonaissumma. Jos et ole täyttänyt **Liiketoimintayksikön koodi** -kenttää, kokonaissumma on konsolidoidun yrityksen kirjattujen poistojen kokonaissumma.
* Konsolidoidun yrityksen kokonaissumma, mukaan lukien kaikki liiketoimintayksiköt ja kaikki kirjatut eliminoinnit.
* Konsolidoidussa yrityksessä tehtävät poistot, siis tapahtumat siinä yleisessä päiväkirjassa, joka on valittu pyyntösivulla.
* Yleisestä päiväkirjasta kopioitu kirjausteksti.
* Konsolidoidun yrityksen kokonaissumma poistojen jälkeen (jos ne on kirjattu).


## <a name="to-export-and-import-consolidated-data-between-databases"></a>Konsolidoitujen tietojen vieminen ja tuominen tietokantojen välillä
Jos liiketoimintayksikön tiedot ovat toisessa tietokannassa, tiedot on vietävä tiedostoon, ennen kuin ne voidaan sisällyttää konsolidointiin. Jokainen yritys täytyy viedä erikseen. Tähän tarkoitukseen ohjelma käyttää **Konsolidoinnin vienti** -eräajoa.  

Kun eräajo on suoritettu, KP-tilien kaikki tapahtumat käsitellään. Jokaisen globaalin dimension ja päivämäärän yhdistelmän osalta tapahtumien **summa**-kentät lasketaan yhteen, ja nämä summat viedään konsolidoituun yritykseen. Sen jälkeen seuraava globaalin dimension ja päivämäärän yhdistelmä, jossa on sama tilinumero, käsitellään – ja sen jälkeen seuraavan tilinumeron yhdistelmät, ja niin edelleen.  

Viedyt tapahtumat sisältävät seuraavat kentät: **Tilinro**, **Kirjauspvm** ja **Summa**. Jos myös dimensiotiedot vietiin, tapahtumiin sisältyvät myös dimensiokoodit ja dimension arvot.  

1. Jos tuodun rivin **Summa**-kenttien kokonaissumma on debet, liiketoimintayksikön **Konsolidoinnin debet**-tili -kentässä määritetty tilinumero tuodaan riville. Jos kokonaissumma on kredit, riville tuodaan **Konsolidoinnin kredit-tili** -kentän vastaava numero.  
2. Kullakin tuodulla rivillä käytettävä päivämäärä on joko kauden lopetuspäivämäärä tai, mikäli siirto tapahtuu päivän mukaan, laskennan tarkka päivämäärä.  
3. Tapahtumaan tuotava dimension arvo on kyseisen dimension arvon **Konsolidointikoodi**-kentässä määritetty konsolidoidun yrityksen dimension arvo. Jos kyseisen dimension arvon **Konsolidointikoodi**-kenttään ei ole määritetty konsolidoidun yrityksen dimension arvoa, riville tuodaan itse dimension arvo.   
4. XML-tiedostot sisältävät lisäksi konsolidointikauden valuutanvaihtokurssit. Nämä kurssit ovat erillisessä osassa tiedoston alussa.

## <a name="see-also"></a>Katso myös
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Liiketoimintatietojen vienti Exceliin](about-export-data.md)
