---
title: Usean yrityksen tietojen konsolidointi | Microsoft Docs
description: Hae yhteenvetonäkymä kaikkien liiketoimintayksikköjesi taloudellisesta tilanteesta.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7274be55600bf2c67ec81aa592940a15bc31162d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381011"
---
# <a name="consolidating-financial-data-from-multiple-companies"></a>Usean yrityksen kirjanpitotietojen konsolidoiminen

Jotkin organisaatiot käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa useassa liiketoimintayksikössä tai yrityksessä. Muut käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa tytäryhtiöissä, joiden tulee raportoida emo-organisaatioihin. Molemmissa tapauksissa kirjanpitäjät käyttävät sisäisiä työkaluja, jotka auttavat vahvistamaan taloudellisia tietoja.  

Voit konsolidoida yritysten (tytäryritysten) pääkirjanpidon tapahtumat konsolidoituun yritykseen. Kutakin konsolidointiin liittyvää yksittäistä yritystä kutsutaan liiketoimintayksiköksi. Yhdistettyä yritystä kutsutaan konsolidoiduksi yritykseksi.  

Voit tuoda tietoja konsolidoituun yritykseen muista saman tietokannan yrityksistä samasta [!INCLUDE [prod_short](includes/prod_short.md)] -vuokraajasta, vuokraajista tai tiedostoista.  

Jos liiketoimintayksikön tilinpäätösten valuutta ei ole sama kuin konsolidoidun yrityksen, konsolidointia varten on määritettävä vaihtokurssit.  

Voit konsolidoida  

* yrityksiä, joissa on käytössä erilaiset tilikartat  
* yrityksiä, joissa on käytössä erilaiset tilikaudet ja valuutat  
* yrityksen taloudelliset tiedot kokonaan tai tietyn prosenttiosuuden niistä
* käyttämällä eri valuuttakursseja yksittäisillä KP-tileillä.
* Yritykset muissa kirjanpidon ja liiketoiminnan hallintaohjelmissa

Konsolidoitu yritys määritetään samalla tavalla kuin muutkin yritykset. Tilikartta on riippumaton muiden liiketoimintayksiköiden tilikartoista, ja yksittäisten liiketoimintayksiköiden tilikartat voivat olla keskenään erilaisia. Määritä konsolidoitavien yritysten luettelo, tarkista laskentatiedot ennen konsolidointia, tuo tiedostoista tai tietokannoista ja luo konsolidointiraportteja. Lisätietoja on kohdassa [Yrityksen konsolidoinnin määrittäminen](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Kirjanpitotietojen konsolidoiminen voi olla erityisen tärkeää konsernin sisäisissä prosesseissa. Lisätietoja on ohjeaiheessa [Konsernitapahtumien hallinta](intercompany-manage.md).

## <a name="trial-balance"></a>Alustava saldo

Jos sinulla on useita [!INCLUDE[prod_short](includes/prod_short.md)] -yrityksiä, kirjanpitäjän roolikeskuksen **Konsolidoitu alustava saldo** -raportti antaa yleiskuvan liiketoiminnan taloudellisesta tilanteesta.  

Raportti yhdistää kunkin yrityksen kirjanpitotapahtumat uuteen yritykseen, joka luodaan konsolidoituja tietoja varten. Tätä yritystä kutsutaan yleensä konsolidoiduksi yritykseksi. Konsolidoitu yritys on vain konsolidoitujen tietojen säilö, eikä se sisällä muita liiketoimintatietoja. Konsolidoituun yritykseen sisällytettävät yritykset ovat raportin **liiketoimintayksiköitä**. Lisätietoja on kohdassa [Yrityksen konsolidoinnin määrittäminen](finance-consolidated-company-reporting-setup.md).  

## <a name="consolidate-data"></a>Tietojen konsolidointi

Varsinainen konsolidointi on prosessi, jossa luvut siirretään liiketoimintayksiköistä *konsolidoituun* yritykseen. Ennen sitä on hyvä tarkistaa, onko perustiedoissa eroa liiketoimintayksiköiden ja konsolidoidun yrityksen välillä. Ohjelmassa on kaksi raporttia, joita voi käyttää tietokannan ja tiedoston testaamiseen.

### <a name="to-test-the-data-before-you-consolidate"></a>Tietojen testaus ennen konsolidointia

Voit testata tiedot, ennen kuin siirrät ne konsolidoituun yritykseen. [!INCLUDE[prod_short](includes/prod_short.md)] etsii eroavaisuuksia liiketoimintayksiköiden tietojen ja konsolidoidun yrityksen tietojen välillä. Tarkistettavia kohteita ovat esimerkiksi erot tilinumeroiden tai dimensiokoodien välillä. Virheet on korjattava ennen raportin suorittamista. Voit testata tietokannan. Jos tuot tietoja XML-tiedostosta, voit testata myös tiedoston.  

1. Avaa konsolidoitu yritys.  
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten liittyvä linkki.  
3. Tee jompikumpi seuraavista toimista:  

    * Testaa tiedosto valitsemalla **Testaa tiedosto** -toiminto, antamalla testattavan tiedoston nimen ja valitsemalla **Tulosta**.  
    * Voit testata tietokannan valitsemalla **Testaa tietokanta**.  

### <a name="run-the-consolidation"></a>Suorita konsolidointi

Kun olet testannut tiedot, voit siirtää ne konsolidoituun yritykseen.  

1. Kirjaudu konsolidoituun yritykseen.  
2. Valitse **kirjanpitäjän roolikeskuksessa** **Suorita konsolidointi** -toiminto.  
3. Täytä vaaditut kentät.  
4. Aseta suodatin-osassa haluamasi liiketoimintayksikön tai yrityksen nimen suodatin.  
5. Vaihtoehtoisesti voit aikatauluttaa raportin suorituksen sopivalle ajalle.  

## <a name="eliminate-repeated-transactions"></a>Estä toistuvat tapahtumat

Kaikkien yritysten konsolidoinnin jälkeen on etsittävä tapahtumat, jotka on tallennettu useaan yritykseen. Ne on sen jälkeen poistettava kirjaamalla eliminointitapahtumat.

Sisäisten liiketapahtumien eliminointien käsittely on manuaalinen prosessi.  

Toistuvien tapahtumien estäminen:

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

## <a name="export-and-import-consolidated-data-between-databases"></a>Vie ja tuo konsolidoituja tietoja tietokantojen välillä

Jos liiketoimintayksikön tiedot ovat toisessa tietokannassa, tiedot on vietävä tiedostoon, ennen kuin ne voidaan sisällyttää konsolidointiin. Jokainen yritys täytyy viedä erikseen. Tähän tarkoitukseen ohjelma käyttää **Konsolidoinnin vienti** -eräajoa.  

> [!TIP]
> Käytä samaa prosessia sellaisten konsolidoitavien tietojen viemiseen, jotka on tarkoitus lähettää Dynamics 365 Financeen, kuten jos tämänhetkinen liiketoimintayksikkösi on tytäryhtiö ja emoyhtiö käyttää Dynamics 365 Financea.

Kun eräajo on suoritettu, KP-tilien kaikki tapahtumat käsitellään. Jokaisen globaalin dimension ja päivämäärän yhdistelmän osalta tapahtumien **summa**-kentät lasketaan yhteen, ja nämä summat viedään konsolidoituun yritykseen. Sen jälkeen seuraava globaalin dimension ja päivämäärän yhdistelmä, jossa on sama tilinumero, käsitellään – ja sen jälkeen seuraavan tilinumeron yhdistelmät, ja niin edelleen.  

Viedyt tapahtumat sisältävät seuraavat kentät: **Tilinro**, **Kirjauspvm** ja **Summa**. Jos myös dimensiotiedot vietiin, tapahtumiin sisältyvät myös dimensiokoodit ja dimension arvot.  

1. Jos tuodun rivin **Summa**-kenttien kokonaissumma on debet, liiketoimintayksikön **Konsolidoinnin debet**-tili -kentässä määritetty tilinumero tuodaan riville. Jos kokonaissumma on kredit, riville tuodaan **Konsolidoinnin kredit-tili** -kentän vastaava numero.  
2. Kullakin tuodulla rivillä käytettävä päivämäärä on joko kauden lopetuspäivämäärä tai, mikäli siirto tapahtuu päivän mukaan, laskennan tarkka päivämäärä.  
3. Tapahtumaan tuotava dimension arvo on kyseisen dimension arvon **Konsolidointikoodi**-kentässä määritetty konsolidoidun yrityksen dimension arvo. Jos kyseisen dimension arvon **Konsolidointikoodi**-kenttään ei ole määritetty konsolidoidun yrityksen dimension arvoa, riville tuodaan itse dimension arvo.  
4. XML-tiedostot sisältävät lisäksi konsolidointikauden valuutanvaihtokurssit. Nämä kurssit ovat erillisessä osassa tiedoston alussa.  

## <a name="see-also"></a>Katso myös

[Määritä yrityksen konsolidointi](finance-consolidated-company-reporting-setup.md)  
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Liiketoimintatietojen vienti Exceliin](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]