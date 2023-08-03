---
title: C5-tietojen siirtolaajennuksen käyttäminen | Microsoft Docs
description: 'Voit käyttää tätä laajennusta asiakkaiden, toimittajien, nimikkeiden ja pääkirjanpidon tilien siirtämiseen Microsoft Dynamics C5 2012:sta Business Centraliin.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'extension, migrate, data, C5, import'
ms.search.form: '1860, 1861, 1862, 1863, 1864, 1867, 1868, 1869, 1874, 1882, 1883, 1884, 1885, 1886, 1888, 1890, 1891, 1892, 1893, 1894, 1898, 1899, 1900, 1901, 1902, 1903, 1904, 1905, 1906'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Tietojen siirron C5-laajennus

Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, nimikkeitä ja pääkirjanpidon tilejä Microsoft Dynamics C5 2012 -versiosta [!INCLUDE[prod_short](includes/prod_short.md)]iin. Voit siirtää myös pääkirjanpidon tilien vanhat tapahtumat.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yrityksessä ei saa olla tietoja. Kun siirto on käynnistetty, asiakkaiden, toimittajien, nimikkeiden tai tilien luominen ei ole sallittua. Voit luoda niitä siirron valmistuttua.

## Mitkä tiedot siirretään?

Seuraavat kunkin objektit tiedot siirretään:

### Asiakkaat

* Kontaktit  
* Sijainti
* Maa
* Asiakkaan dimensiota (osasto, tuotantosolu, tarkoitus)
* Toimitusehto
* Myyjä
* Maksuehdot
* Maksutapa
* Asiakkaan hintaryhmä
* Asiakkaan laskun alennus

Jos siirrät tilit, myös seuraavat tiedot siirretään:

* Asiakkaan kirjausasetukset
* Yleisen päiväkirjan erä
* Avoimet tapahtumat (asiakastapahtumat)

### Toimittajat

* Kontaktit
* Sijainti
* Maa
* Toimittajan dimensiot (osasto, tuotantosolu, tarkoitus)
* Laskualennus
* Toimitusehto
* Ostaja
* Maksuehdot
* Maksutapa
* Toimittajan laskun alennus

Jos siirrät tilit, myös seuraavat tiedot siirretään:

* Toimittajan kirjausasetukset
* Yleisen päiväkirjan erä
* Avoimet tapahtumat (toimittajatapahtumat)

### Nimikkeet

* Sijainti
* Maa
* Nimikkeen dimensiot (osasto, tuotantosolu, tarkoitus)
* Myynnin rivialennukset
* Asiakkaan alennusryhmät
* Nimikealennusryhmät
* Myyntihinta
* Tavaranimike
* Mittayksiköt
* Nimikkeen seurantakoodi
* Asiakkaan hintaryhmä
* Kokoonpanon tuoterakenteet

Jos siirrät tilit, myös seuraavat tiedot siirretään:

* Varastokirjauksien asetukset
* Yleiset kirjausasetukset
* Nimikepäiväkirjan erä
* Avoimet tapahtumat (nimiketapahtumat)

> [!NOTE]
> Jos avoimissa tapahtumissa käytetään ulkomaanvaluuttoja, myös kyseisten valuuttojen vaihtokurssit siirretään. Muita vaihtokursseja ei siirretä.

### Tilikartta

* Vakiodimensiot: osasto, kustannupaikka, tarkoitus  
* Historialliset KP-tapahtumat  

> [!NOTE]
> Historialliset KP-tapahtumat, joita käsitellään hieman eri tavalla. Kun siirrät tietoja, määrität **Nykyinen jakso** -parametrin. Tämä parametri määrittää, miten KP-tapahtumia käsitellään. Tämän päivämäärän jälkeen tapahtumat siirretään erikseen. Tapahtumat ennen tätä päivämäärää koostetaan tilikohtaisesti ja siirretään yhtenä summana. Esimerkiksi oletetaan, että tapahtumia on vuosina 2015, 2016, 2017 ja 2018, ja määrität 1. tammikuuta 2017 Nykyinen jakso -kenttään. Kunkin tilin tapahtumien 31.12.2016 tai sitä ennen summat kootaan yhteen yleisen päiväkirjan riviin kullekin KP-tilille. Kaikki tapahtumat tämän päivämäärän jälkeen siirretään yksitellen.

## Tiedoston kokovaatimukset

[!INCLUDE[prod_short](includes/prod_short.md)]iin ladattava tiedoston koko saa olla enintään 150 Mt. Jos C5:stä vietävä tiedosto on tätä suurempi, harkitse tietojen siirtämistä useina tiedostoina. Vie C5:stä yhden tai kahden tyyppiset objektit, kuten asiakkaat ja toimittajat, yhteen tiedostoon, nimikkeet toiseen tiedostoon ja niin edelleen. Voit tuoda tiedostot yksitellen [!INCLUDE[prod_short](includes/prod_short.md)]iin.

## Tietojen siirtäminen

Tietojen siirtäminen C5:stä ja tuominen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta edellyttää vain seuraavien vaiheiden suorittamista:  

1. Voit viedä tiedot C5:stä käyttämällä **Vie tietokanta** -toimintoa. Pakkaa sitten viennin kansio.  
2. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]issa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tietojen siirto** ja valitse sitten **Tietojen siirto**.  
3. Suorita asetusten ohjatun määrityksen oppaan vaiheet. Varmista, että valitset tietolähteeksi **Tuo Microsoft Dynamics C5 2012** -versiosta -kohdan.  

## Siirron tilan tarkasteleminen

Voit valvoa siirron onnistumista **Tietojen siirron yleiskuvaus** -sivulla. Sivulla on tietoja esimerkiksi siirrettävien objektien määrästä, siirron tilasta, siirrettyjen nimikkeiden määrästä ja siirron onnistumisesta. Sivulla on tietoja myös virheiden määrästä. Voit tarkastella sivulla virheitä ja mahdollisesti siirtyä sivulta korjaamaan objektin ongelmat. Lisätietoja on tämän aiheen seuraavassa osassa.  

> [!NOTE]
> Päivitä sivu, jotta siirron tulokset näkyvät sivulla.

## Miten voit välttää kaksinkertaisen kirjauksen

Voit välttää kaksinkertaisen kirjaamisen pääkirjanpitoon, käyttämällä seuraavia vastatilejä avoimille tapahtumille:  

* Toimittajia varten käytetään ostoreskontratiliä toimittajan kirjausryhmästä.  
* Asiakkaita varten käytetään myyntireskontratiliä asiakkaan kirjausryhmästä.  
* Nimikkeille luodaan yleinen kirjausasetus, missä oikaisutili on tili, joka on määritetty varastotiliksi varaston kirjausasetuksissa.  

## Virheiden korjaaminen

Jos siirrossa tapahtuu virheitä, **Tila**-kentän arvoksi tulee **Valmis (löytyi virheitä)**. **Virheiden määrä** -kenttä osoittaa virheiden määrän. Voit tarkastella virheluetteloa, kun avaat **Tietojen siirron virheet** -sivun valitsemalla seuraavat kohdat:  

* Objektin **Virheiden määrä** -kentässä oleva luku.  
* Objekti ja sen jälkeen **Näytä virheet** -toiminto.  

Voit korjata virheen **Tietojen siirron virheet** -sivulla valitsemalla virhesanoman ja valitsemalla sitten **Muokkaa tietuetta**. Näyttöön avautuu objektin siirretyt tiedot. Jos korjattavia virheitä on paljon, voit muokata luettelossa olevia objekteja **Korjaa virheet joukkotoimintona** -kohdan avulla. Jos virheen aiheuttaja on liittyvä merkintä, yksittäiset tietueet on avattava tästä huolimatta. Esimerkiksi toimittajaa ei siirretä, jos toimittajan jonkin yhteyshenkilön sähköpostiosoite on virheellisessä muodossa.

Kun olet korjannut yhden tai useita virheitä, voit siirtää korjaamasi objektit valitsemalla **Siirrä**. Koko siirtoprosessia ei siis tarvitse käynnistää uudelleen.  

> [!TIP]
> Jos olet korjannut useita virheitä, voit valita useita siirrettäviä rivejä valitsemalla **Valitse lisää** -toiminnon. Jos virheitä ei tarvitse korjata, voit valita ne ja valita sitten **Ohita valinnat**.

> [!NOTE]
> Jos osa nimikkeistä sisältyy tuoterakenteeseen, siirto on ehkä tehtävä useaan kertaan, jos alkuperäistä nimikettä ei luoda ennen siihen viittaavien varianttien luomista. Jos nimikevariantti luodaan ensin, alkuperäisen nimikkeen viite voi aiheuttaa virhesanoman.  

## Tietojen tarkistaminen siirron jälkeen

Yksi tapa tarkistaa, että tiedot on siirretty oikein, on katsoa seuraavia C5:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in sivuja.

|Microsoft Dynamics C5 2012 | Dynamics 365 Business Central| Käytettävä eräajo |
|---------------------------|------------------------------|------------------|
|Asiakastapahtumat| Yleiset päiväkirjat| CUSTMIGR |
|Toimittajatapahtumat| Yleiset päiväkirjat| VENDMIGR|
|Nimiketapahtumat| Nimikepäiväkirjat| ITEMMIGR |
|KP-tapahtumat| Yleiset päiväkirjat| GLACMIGR |

## Tietojen siirron pysäyttäminen

Voit pysäyttää tietojen siirron valitsemalla **Pysäytä kaikki siirrot**. Jos teet näin, kaikki odottavat siirrot pysäytetään.

## Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
