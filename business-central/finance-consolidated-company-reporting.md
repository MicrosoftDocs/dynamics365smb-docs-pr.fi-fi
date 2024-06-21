---
title: Usean yrityksen tietojen konsolidointi
description: 'Tämä artikkeli selittää, miten voit konsolidoida yritysten (tytäryritysten) pääkirjanpidon tapahtumat konsolidoituun yritykseen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# Usean yrityksen kirjanpitotietojen konsolidoiminen

Jotkin organisaatiot käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa useassa liiketoimintayksikössä tai yrityksessä. Muut käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa tytäryhtiöissä, joiden tulee raportoida emo-organisaatioihin. [!INCLUDE [prod_short](includes/prod_short.md)] antaa kirjanpitäjille työkalut, jotka auttavat heitä siirtämään pääkirjanpidon tapahtumia kahdesta tai useammasta yrityksestä (tytäryrityksistä) konsolidoituun yritykseen.  

Kutakin konsolidointiin liittyvää yritystä kutsutaan liiketoimintayksiköksi. Yritystä, jossa tiedot yhdistetään, kutsutaan konsolidoiduksi yritykseksi.  

Voit siirtää taloudellisia tietoja tytäryrityksistä konsolidoituun yritykseen, vaikka tytäryritykset käyttäisivät kohdetta [!INCLUDE [prod_short](includes/prod_short.md)] erilaisissa ympäristöissä. Lisätietoja yhteyden muodostamisesta muihin ympäristöihin on [Määritä yrityksen konsolidointi](finance-consolidated-company-reporting-setup.md#busunit) -kohdassa.

Jos liiketoimintayksikön tilinpäätösten valuutta ei ole sama kuin konsolidoidun yrityksen, konsolidointia varten on määritettävä vaihtokurssit. Lisätietoja konsolidointien vaihtokursseista on [Määritä yrityksen konsolidointi](finance-consolidated-company-reporting-setup.md#exchrates) -kohdassa.  

Voit konsolidoida  

* yrityksiä, joissa on käytössä erilaiset tilikartat  
* yrityksiä, joissa on käytössä erilaiset tilikaudet ja valuutat  
* yrityksen taloudelliset tiedot kokonaan tai tietyn prosenttiosuuden niistä.
* käyttämällä eri valuuttakursseja yksittäisillä KP-tileillä.
* Yritykset muissa kirjanpidon ja liiketoiminnan hallintaohjelmissa.
* Yritykset eri [!INCLUDE [prod_short](includes/prod_short.md)] -ympäristöissä.

Konsolidoitu yritys määritetään samalla tavalla kuin muutkin yritykset. Tilikartta on riippumaton liiketoimintayksiköiden tilikartasta. Liiketoimintayksiköiden tilikartat voivat vaihdella keskenään. Lisätietoja konsolidoinnin määrittämisestä on [Määritä yrityksen konsolidointi](finance-consolidated-company-reporting-setup.md) -kohdassa.  

> [!TIP]
> Kirjanpitotietojen konsolidoiminen voi olla erityisen tärkeää konsernin sisäisissä prosesseissa. Lisätietoja konsernin ominaisuuksista on [Konsernitapahtumien hallinta](intercompany-manage.md) -kohdassa.

## Tietojen konsolidointi

Ennen konsolidoinnin aloittamista on hyvä testata tiedot ennen niiden siirtämistä konsolidoituun yritykseen. [!INCLUDE[prod_short](includes/prod_short.md)] etsii eroavaisuuksia liiketoimintayksiköiden tietojen ja konsolidoidun yrityksen tietojen välillä. Tarkistettavia kohteita ovat esimerkiksi erot tilinumeroiden tai dimensiokoodien välillä. Virheet on korjattava ennen raportin suorittamista. Voit testata tietokannan. Jos tuot tietoja XML-tiedostosta, voit testata myös tiedoston.

### Tietojen testaus ennen konsolidointia

1. Avaa konsolidoitu yritys.  
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten vastaava linkki.  
3. Testaa tiedosto ja tietokanta seuraavasti:  

    * Testaa tiedosto valitsemalla **Testaa tiedosto** -toiminto, antamalla testattavan tiedoston nimen ja valitsemalla **Tulosta**.  
    * Voit testata tietokannan valitsemalla **Testaa tietokanta**.  

### Suorita konsolidointi

Kun olet testannut tiedot, voit siirtää ne konsolidoituun yritykseen. Asetusten ohjatun määrityksen avulla voit käsitellä prosessia.

> [!NOTE]
> Kun suoritat konsolidoinnin, voit valita sisällytettävät yritykset. Jos konsolidoidulla yrityksellä ei ole pääsyä yhteen tai useampaan tytäryritykseen, oppaassa voit antaa heille käyttöoikeuden.

1. Kirjaudu konsolidoituun yritykseen.  
2. Valitse **Liiketoimintayksiköt**-sivulta **Konsolidoi**-toiminto.  
3. Täytä vaaditut kentät.  

## Käytä Konsolidoitu alustava saldo -raporttia

**Konsolidoitu alustava saldo** -raportti antaa yleiskuvan liiketoiminnan yleisestä taloudellisesta tilanteesta. Raportti yhdistää kunkin yrityksen kirjanpitotapahtumat uuteen yritykseen, joka luodaan konsolidoituja tietoja varten. Konsolidoitu yritys on vain konsolidoitujen tietojen säilö, eikä se sisällä muita liiketoimintatietoja. Konsolidoituun yritykseen sisällytettävät yritykset ovat raportin **liiketoimintayksiköitä**. Jos liiketoimintayksiköitä on neljä tai vähemmän, voit käyttää myös **Konsol. alust. tulos/tase (4)** -raporttia.  

Raportissa näkyy rivi kullekin tilille ja se noudattaa tilikartan rakennetta. Tiliä ei ole näkyvissä, jos rivin kaikki summat ovat 0. Raportissa näkyy seuraavat tiedot kullekin tilille:

* Tilinumero ja tilin nimi.
* Konsolidoidun yrityksen ja kunkin liiketoimintayksikön kokonaissummat. Kokonaissummat voidaan näyttää joko nettomuutoksena tai päivän saldona.
* Konsolidoidussa yrityksessä tehdyt poistot. Poistot näkyvät aina ajanjaksolta, joka vastaa konsolidoidun yrityksen tilikautta.
* Konsolidoidun yrityksen kokonaissumma poistojen jälkeen, ilmoitettuna joko nettomuutoksena tai päivän saldona.

## Estä toistuvat tapahtumat

Yritysten konsolidoinnin jälkeen on etsittävä ja poistettava tapahtumat, jotka on tallennettu useaan yritykseen. Sisäisten liiketapahtumien eliminointien käsittely on manuaalinen prosessi.  

Toistuvien tapahtumien estäminen:

1. Etsi tapahtumat, joita on mahdollisesti muutettava, ja anna ne eliminoivat yleisen päiväkirjan rivit.
2. **Sis. liiketapaht. eliminoinnit** -raportin suorittaminen auttaa arvioimaan yleisen päiväkirjan rivien vaikutuksen ennen kirjaamista.
3. Kirjaa muutostapahtumat.

**KP-konsolidoinnin eliminoinnit** -raportissa näkyy alustava saldo, jossa voit simuloida tapahtumien poistamisen seurauksia. Raportissa verrataan konsolidoidun yrityksen kirjauksia yleiseen päiväkirjaan kirjattuihin eliminointeihin.

Ennen kuin liiketoimintayksikkö voidaan sisällyttää raporttiin, yksikkö on luotava **Liiketoimintayksiköt**-sivulla. Ota **Konsolidoi**-vaihto käyttöön.

Jokaiselle tilille luodaan oma rivi noudattaen tilikartan rakennetta. Tiliä ei ole näkyvissä, jos rivin kaikki summat ovat 0. Raportissa näkyy seuraavat tiedot kullekin tilille:

* Tilinumero.
* Tilin nimi.
* Jos olet valinnut vähintään yhden liiketoimintayksikön koodin pyyntösivun **Liiketoimintayksikön koodi** -kentässä, niin konsolidoidun yrityksen kokonaissumma näkyy siten, että siitä on vähennetty valitut liiketoimintayksiköt ja poistot. Jos et täyttänyt **Liiketoimintayksikön koodi** -kenttää, konsolidoidun yrityksen kokonaissumma ei sisällä poistoja.
* Jos olet valinnut liiketoimintayksikön koodin pyyntösivun **Liiketoimintayksikön koodi** -kentässä, kokonaissumma näyttää liiketoimintayksiköstä tuotujen tapahtumien kokonaissumman. Jos et täyttänyt **Liiketoimintayksikön koodi** -kenttää, kokonaissumma näyttää konsolidoidun yrityksen kirjattujen poistojen kokonaissumman.
* Konsolidoidun yrityksen kokonaissumma, mukaan lukien kaikki liiketoimintayksiköt ja kaikki kirjatut eliminoinnit.
* Konsolidoidussa yrityksessä tehtävät poistot. Toisin sanoen pyyntösivulla valittuna olevan yleisen päiväkirjan tapahtumat.
* Yleisestä päiväkirjasta kopioitu kirjausteksti.
* Konsolidoidun yrityksen kokonaissumma poistojen jälkeen (jos ne on kirjattu).

## Vie ja tuo konsolidoituja tietoja tietokantojen välillä

Jos liiketoimintayksikön tiedot ovat toisessa tietokannassa, voit tehdä manuaalisen tiedostopohjaisen siirron tai automatisoida prosessin ohjelmointirajapinnan avulla. Lisätietoja ohjelmointirajapinnasta on kohdassa [Käytä ohjelmointirajapintaa, kun haluat jakaa tietoja automaattisesti ympäristöissä](#use-our-api-to-automatically-share-data-across-environments).

Tässä osassa kuvataan manuaalinen tiedostopohjainen prosessi.

Tiedot viedään tiedostoon ennen niiden sisällyttämistä konsolidointiin. Vie jokainen yritys erikseen **Konsolidoinnin vienti** -eräajon avulla.  

> [!TIP]
> Käytä samaa prosessia, kun haluat viedä konsolidoitua tietoa, joka on lähetettävä Dynamics 365 Finance -ohjelmaan. Jos liiketoimintayksikkö on esimerkiksi tytäryritys ja emoyritys käyttää Dynamics 365 Finance -ohjelmaa.

Kun eräajo on suoritettu, KP-tilien kaikki tapahtumat käsitellään. Jokaisen globaalin dimension ja päivämäärän yhdistelmän osalta tapahtumien **summa**-kentät lasketaan yhteen, ja nämä summat viedään konsolidoituun yritykseen. Valittujen dimensioiden ja päivämäärän seuraava yhdistelmä samalla tilinumerolla käsitellään. Sitten käsitellään seuraavan tilinumeron yhdistelmät ja niin edelleen.  

Viedyt tapahtumat sisältävät seuraavat kentät: **Tilinro**, **Kirjauspvm** ja **Summa**. Jos myös dimensiotiedot vietiin, tapahtumiin sisältyvät myös dimensiokoodit ja dimension arvot.  

1. Jos tuodun rivin **Summa**-kenttien kokonaissumma on debet, liiketoimintayksikön **Konsolidoinnin debet**-tili -kentässä määritetty tilinumero tuodaan riville. Jos kokonaissumma on kredit, riville tuodaan **Konsolidoinnin kredit-tili** -kentän vastaava numero.  
2. Kullakin tuodulla rivillä käytettävä päivämäärä on joko kauden lopetuspäivämäärä tai, mikäli siirto tapahtuu päivän mukaan, laskennan tarkka päivämäärä.  
3. Tapahtumaan tuotava dimension arvo on kyseisen dimension arvon **Konsolidointikoodi**-kentässä määritetty konsolidoidun yrityksen dimension arvo. Jos kyseisen dimension arvon **Konsolidointikoodi**-kenttään ei ole määritetty konsolidoidun yrityksen dimension arvoa, riville tuodaan itse dimension arvo.  
4. XML-tiedostot sisältävät lisäksi konsolidointikauden valuutanvaihtokurssit. Nämä kurssit ovat erillisessä osassa tiedoston alussa.  

## Ohjelmointirajapinnan käyttäminen tietojen automaattiseen jakamiseen ympäristöissä

[!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa ohjelmointirajapinnan, jonka avulla voit automatisoida taloustietojen jakamisen liiketoimintayksiköistä konsolidoituun yritykseen. Ohjelmointirajapinta on helppokäyttöinen ja helppo määrittää. Voit myös jakaa tietoja [!INCLUDE [prod_short](includes/prod_short.md)] -ympäristöissä. Sinun on esimerkiksi ehkä jaettava ympäristöissä silloin, kun liiketoimintayksiköt eivät ole samoilla Azuren maantieteellisillä alueilla. Lisätietoja ohjelmointirajapinnan käyttämisestä konsolidointiprosessin automatisoimiseen on [Määritä yrityksen konsolidointi](finance-consolidated-company-reporting-setup.md#busunit) -kohdassa.

## Katso myös

[Yrityksen konsolidoinnin määrittäminen](finance-consolidated-company-reporting-setup.md)  
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Liiketoimintatietojen vienti Exceliin](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]