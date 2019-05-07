---
title: C5-tietojen siirtolaajennuksen käyttäminen | Microsoft Docs
description: Voit käyttää tätä laajennusta asiakkaiden, toimittajien, nimikkeiden ja pääkirjanpidon tilien siirtämiseen Microsoft Dynamics C5 2012:sta Business Centraliin.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 23d2f6c950786bbd5eb8af0a79ea1351d4e8a3d0
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "919604"
---
# <a name="the-c5-data-migration-extension"></a>Tietojen siirron C5-laajennus
Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, nimikkeitä ja pääkirjanpidon tilejä Microsoft Dynamcis C5 2012 -versiosta [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan. Voit siirtää myös pääkirjanpidon tilien vanhat tapahtumat.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yrityksessä ei saa olla tietoja. Kun siirto on käynnistetty, asiakkaiden, toimittajien, nimikkeiden tai tilien luominen ei ole sallittua. Voit luoda niitä siirron valmistuttua.

## <a name="what-data-is-migrated"></a>Mitkä tiedot siirretään?
Seuraavat kunkin objektit tiedot siirretään:

**Asiakkaat**
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

**Toimittajat**
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

**Nimikkeet**
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

> [!Note]
> Jos avoimissa tapahtumissa käytetään ulkomaanvaluuttoja, myös kyseisten valuuttojen vaihtokurssit siirretään. Muita vaihtokursseja ei siirretä.

**Tilikartta**  
* Vakiodimensiot: osasto, kustannupaikka, tarkoitus  
* Historialliset KP-tapahtumat  

> [!Note]
> Historialliset KP-tapahtumat, joita käsitellään hieman eri tavalla. Kun siirrät tietoja, määrität **Nykyinen jakso** -parametrin. Tämä parametri määrittää, miten KP-tapahtumia käsitellään. Tämän päivämäärän jälkeen tapahtumat siirretään erikseen. Tapahtumat ennen tätä päivämäärää koostetaan tilikohtaisesti ja siirretään yhtenä summana. Esimerkiksi oletetaan, että tapahtumia on vuosina 2015, 2016, 2017 ja 2018, ja määrität 1. tammikuuta 2017 Nykyinen jakso -kenttään. Kunkin tilin tapahtumien 31.12.2016 tai sitä ennen summat kootaan yhteen yleisen päiväkirjan riviin kullekin KP-tilille. Kaikki tapahtumat tämän päivämäärän jälkeen siirretään yksitellen.

## <a name="file-size-requirements"></a>Tiedoston kokovaatimukset
[!INCLUDE[d365fin](includes/d365fin_md.md)]iin ladattava tiedoston koko saa olla enintään 150 Mt. Jos C5:stä vietävä tiedosto on tätä suurempi, harkitse tietojen siirtämistä useina tiedostoina. Vie C5:stä yhden tai kahden tyyppiset objektit, kuten asiakkaat ja toimittajat, yhteen tiedostoon, nimikkeet toiseen tiedostoon ja niin edelleen. Voit tuoda tiedostot yksitellen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

## <a name="to-migrate-data"></a>Tietojen siirtäminen
Tietojen siirtäminen C5:stä ja tuominen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmasta edellyttää vain seuraavien vaiheiden suorittamista:  

1. Voit viedä tiedot C5:stä käyttämällä **Vie tietokanta** -toimintoa. Pakkaa sitten viennin kansio.  
2. Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tietojen siirto** ja valitse **Tietojen siirto**.  
3. Suorita asetusten ohjatun määrityksen oppaan vaiheet. Varmista, että valitset tietolähteeksi **Tuo Microsoft Dynamcis C5 2012 -versiosta** -kohdan.  

## <a name="viewing-the-status-of-the-migration"></a>Siirron tilan tarkasteleminen
Voit valvoa siirron onnistumista **Tietojen siirron yleiskuvaus** -sivulla. Sivulla on tietoja esimerkiksi siirrettävien objektien määrästä, siirron tilasta, siirrettyjen nimikkeiden määrästä ja siirron onnistumisesta. Sivulla on tietoja myös virheiden määrästä. Voit tarkastella sivulla virheitä ja mahdollisesti siirtyä sivulta korjaamaan objektin ongelmat. Lisätietoja on tämän aiheen seuraavassa osassa.  

> [!Note]
> Päivitä sivu, jotta siirron tulokset näkyvät sivulla.

## <a name="how-to-avoid-double-posting"></a>Miten voit välttää kaksinkertaisen kirjauksen
Voit välttää kaksinkertaisen kirjaamisen pääkirjanpitoon, käyttämällä seuraavia vastatilejä avoimille tapahtumille:  

* Toimittajia varten käytetään ostoreskontratiliä toimittajan kirjausryhmästä.  
* Asiakkaita varten käytetään myyntireskontratiliä asiakkaan kirjausryhmästä.  
* Nimikkeille luodaan yleinen kirjausasetus, missä oikaisutili on tili, joka on määritetty varastotiliksi varaston kirjausasetuksissa.  

## <a name="correcting-errors"></a>Virheiden korjaaminen
Jos siirrossa tapahtuu virheitä, **Tila**-kentän arvoksi tulee **Valmis (löytyi virheitä)**. **Virheiden määrä** -kenttä osoittaa virheiden määrän. Voit tarkastella virheluetteloa, kun avaat **Tietojen siirron virheet** -sivun valitsemalla seuraavat kohdat:  

* Objektin **Virheiden määrä** -kentässä oleva luku.  
* Objekti ja sen jälkeen **Näytä virheet** -toiminto.  

Voit korjata virheen **Tietojen siirron virheet** -sivulla valitsemalla virhesanoman ja valitsemalla sitten **Muokkaa tietuetta**. Näyttöön avautuu objektin siirretyt tiedot. Jos korjattavia virheitä on paljon, voit muokata luettelossa olevia objekteja **Korjaa virheet joukkotoimintona** -kohdan avulla. Jos virheen aiheuttaja on liittyvä merkintä, yksittäiset tietueet on avattava tästä huolimatta. Esimerkiksi toimittajaa ei siirretä, jos toimittajan jonkin yhteyshenkilön sähköpostiosoite on virheellisessä muodossa.

Kun olet korjannut yhden tai useita virheitä, voit siirtää korjaamasi objektit valitsemalla **Siirrä**. Koko siirtoprosessia ei siis tarvitse käynnistää uudelleen.  

> [!Tip]
> Jos olet korjannut useita virheitä, voit valita useita siirrettäviä rivejä valitsemalla **Valitse lisää** -toiminnon. Jos virheitä ei tarvitse korjata, voit valita ne ja valita sitten **Ohita valinnat**.

> [!Note]
> Jos osa nimikkeistä sisältyy tuoterakenteeseen, siirto on ehkä tehtävä useaan kertaan, jos alkuperäistä nimikettä ei luoda ennen siihen viittaavien varianttien luomista. Jos nimikevariantti luodaan ensin, alkuperäisen nimikkeen viite voi aiheuttaa virhesanoman.  

## <a name="verifying-data-after-migrating"></a>Tietojen tarkistaminen siirron jälkeen
Yksi tapa tarkistaa, että tiedot on siirretty oikein, on katsoa seuraavia C5:n ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in sivuja.

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]| Käytettävä eräajo |
|-----|-----|-----|
|Asiakastapahtumat| Yleiset päiväkirjat| CUSTMIGR |
|Toimittajatapahtumat| Yleiset päiväkirjat| VENDMIGR|
|Nimiketapahtumat| Nimikepäiväkirjat| ITEMMIGR |
|KP-tapahtumat| Yleiset päiväkirjat| GLACMIGR |

## <a name="stopping-data-migration"></a>Tietojen siirron pysäyttäminen
Voit pysäyttää tietojen siirron valitsemalla **Pysäytä kaikki siirrot**. Jos teet näin, kaikki odottavat siirrot pysäytetään.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Käytön aloittaminen](product-get-started.md)
