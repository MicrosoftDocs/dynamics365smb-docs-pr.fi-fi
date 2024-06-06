---
title: Usein kysyttyjä kysymyksiä Copilotin myyntiriviehdotuksista
description: Näissä usein kysytyissä kysymyksissä on tietoja Business Centralissa käytettävästä tekoälyteknologiasta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# Usein kysyttyjä kysymyksiä Copilotin myyntiriviehdotuksista (esiversio)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Näissä usein kysytyissä kysymyksissä käsitellään tekoälyn vaikutusta [!INCLUDE [prod_short](includes/prod_short.md)]in myyntiriviehdotuksiin.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Mitä Copilotin myyntiriviehdotukset ovat?

Copilotin myyntiriviehdotus voi auttaa luomaan rivejä myyntiasiakirjoihin, kuten myyntitarjouksiin, tilauksiin ja laskuihin, jäsennetyn syötön tai luonnollisen kielen perusteella. Ominaisuus ei ole yleinen keskustelu vaan erittäin kohdistettu ja integroitu kokemus, jota voi käyttää myyntiasiakirjoissa. Ominaisuudessa on kaksi erillistä taitoa, jotka auttavat etsimään yksittäisiä tuotteita tai koko asiakirjoja koskevia tietoja.

## Copilotin myyntiriviehdotusten ominaisuudet

* Tuotteiden etsiminen

  Useisiin paikkoihin [!INCLUDE [prod_short](includes/prod_short.md)]issa tallennettuja tuotteita kuvailevat tiedot. Esimerkiksi nimikenumerot ja -kuvaukset tallennetaan **Nimike**-taulukkoon, useita viivakoodeja tallennetaan **Nimikeviittaus**-taulukkoon ja tuoteominaisuudet tallennetaan **Nimikemääritteet**-taulukkoon. Vaikka kehote voi olla *punainen polkupyörä*, varsinainen tuote onkin *tulipunainen matkapyörä*, jossa *polkupyörä* on tuoteluokka ja *punainen* määrite.

* Asiakirjan etsiminen viitteen perusteella

  Ihmiset toistavat usein edellisen tilauksen tai ainakin käyttävät sitä aloituskohtana. Oikean tilauksen löytäminen tilauspinosta voi olla kuitenkin hankalaa. Muistissa on ehkä tilaustunnuksen osa, joka voi olla yritykselle määritetty numero tai asiakkaalta saatu viitanumero. Kehotteet, kuten *tarvitsen huhtikuun viimeisen laskun*, todennäköisesti nopeuttavat tilauksen löytämistä.

## Mikä on Copilotin myyntiriviehdotusten käyttötarkoitus?

* Tuotteiden etsiminen

  Tarkoitettu vastaamaan käyttäjän kehotteisiin, joilla etsitään tuotteita epämääräisten, epätäydellisten tai epätarkkojen kuvausten perusteella.

  Koska [!INCLUDE [prod_short](includes/prod_short.md)] -asiakkailla on keskimäärin 10 000 nimikettä (tuotteita tai palveluja), oikean nimikkeen etsiminen voi olla hankalaa ilman aiempaa kokemusta tai tietämystä. Tapa, jolla tiedot tallennetaan [!INCLUDE [prod_short](includes/prod_short.md)]iin, ei helpota etsintää, sillä tuotetiedot sisältävillä eri sivuilla on tehtävä useita hakuja tai suodatuksia.

  Copilot noutaa pyydetyt tuotteet ja määrät sekä tunnistaa päähakusanan ja määritteet, mikä nopeuttaa kehotteen syöttämistä. Copilot tekee sitten tarkennetun haun useissa liittyvissä taulukossa käyttämällä synonyymeja, korjaamalla kirjoitusvirheet ja arvioimalla hakutuloksen laadun.

* Asiakirjan etsiminen viitteen perusteella

  Tarkoitettu vastaamaan käyttäjän kyselyihin, joissa etsitään tietyn asiakkaan aiemmin luotuja myyntiasiakirjoja osittaisten tai lähellä olevien tietojen perusteella.

  Yritystenvälisissä ympäristöissä joudutaan usein käsittelemään toistuvia pyyntöjä ja tilausten käsittelijät voivat saada kyselyjä, joka toisintaa aiemman asiakirjan – tai sitä voidaan ainakin käyttää aloituskohtana. Oikean asiakirjan löytäminen voi kuitenkin olla hankalaa monestakin syystä:

  - Myyntiasiakirja voi kehittyä elinkaaren aikana tarjouksesta tilaukseksi ja sitten kirjatuksi laskuksi tai toimitukseksi. Asiakirjoja voi myös arkistoida.
  - Tarkka tunniste voi olla saatavana muttei tietoa siitä, mitä se tarkoittaa. Se voi olla esimerkiksi tilausnumero, laskun numero tai ulkoinen viite.
  - Joskus käytettävissä on päivämäärä tai kausi muttei asiakirjan tunnusta.

  Lähdeasiakirjan manuaalinen etsiminen edellyttäisi useiden sivujen avaamista sekä useiden hakujen ja suodatusten käyttämistä. Copilot voi kuitenkin yksinkertaistaa kaiken tämän yhdeksi luonnollisella kielellä tehdyksi kyselyksi, jossa haettava kohde voidaan ilmaista omin sanoin. 

  * *Hae tilauksen103031 tuotteet*
  * *Tarvitsen elokuun viimeisen laskun tuotteet*

## Miten Copilotin myyntiriviehdotukset arvioitiin? Mitä mittareita suorituskyvyn mittaamiseen käytetään?

Ominaisuutta testattiin laajasti käyttämällä runsaasti Yhdysvaltain englanninkielisiä kehotteita, jotka ilmaisivat sekä tyypillistä käyttöä että haitallisten toimijoiden käyttöä. Testaus perustui [!INCLUDE [prod_short](includes/prod_short.md)]in esittelytietoihin ja suureen avoimena lähdekoodina saatavana olevaan otsikoituun tuoteluetteloon.

Tämä ominaisuus on rakennettu Microsoftin Vastuullinen tekoäly -standardin mukaisesti. [Lisätietoja Microsoftin vastuullisesta tekoälystä](https://aka.ms/RAI).

## Mitä rajoituksia Copilotin myyntiriviehdotuksissa on? Miten käyttäjät voivat minimoida Copilotin myyntiriviehdotuksia koskevat rajoitukset, kun he käyttävät järjestelmää?

* Tuotteiden etsiminen
  
  Tuotteiden etsiminen toimii parhaiten englannin kielellä. Vaikka tätä ominaisuutta voi käyttää millä tahansa [!INCLUDE [prod_short](includes/prod_short.md)]in tukemalla kielellä, muilla kielillä tehtävät nimikehaut eivät ole yhtä tarkkoja.

Jos toimiala tai toimialue kattaa aiheet, joita Microsoft pitää arkaluonteisena (kuten huumeet, väkivalta ja aikuisviihde), Copilot voi siirtyä neutraaleihin, kuratoituihin vastauksiin tai antaa virheellisiä vastauksia.

Myyntiriviehdotukset täyttävät **Tyyppi**-kenttiin vain arvon **Nimike**, **Nro** ja **Määrä**. Muut kentät, mukaan lukien **Mittayksikkö**, **Yksikköhinta** ja **Sijainti** käyttävät valittua logiikkaa, ja ne täytetään joko nimikkeen asetusten tai asiakirjan otsikosta perittyjen arvojen perusteella.

**Varianttikoodi**-kenttää ei tueta tällä hetkellä. Jos tuote voidaan esimerkiksi toimittaa kahtena eri värinä, Copilot etsii tarvittavan tuotteen mutta jättää **Varianttikoodi**-kentän tyhjäksi. Kenttä on täytettävä manuaalisesti.

Tuotteiden nimeämistapa voi vaikuttaa tulokseen. Esimerkiksi epäselvien lyhenteiden käyttäminen selkeän nimen sijaan voi heikentää tuloksen laatua.

Seuraavassa taulukossa on luettelo taulukoista ja kentistä, joista Copilot hakee tuotteita.

|Sivupöytä  |Kentät  |
|---------|---------|
|**Nimikkeet**     |  * Nro<br>* Kuvaus<br>* Kuvaus 2<br>* Haun kuvaus<br>* GTIN<br>* Toimittajan nimikenumero       |
|**Nimikevariantti**     | * Koodi<br>* Kuvaus<br>* Kuvaus 2          |
|**Nimikeviittaus**     | * Viittauksen nro<br>* Kuvaus<br>* Kuvaus 2        |
|**Nimikemääritteet**     | * Nimi<br>* Arvo        |
|**Nimikeluokka**     |  * Koodi<br>* Kuvaus<br>* Pääluokka – taso 1           |
|**Nimikekäännös**     | * Kieli<br>* Kuvaus<br>* Kuvaus 2          |
|**Nimiketunnistin**     |  * Koodi       |
|**Lisätekstirivi**     |  * Teksti      |

* Asiakirjojen etsiminen viitteen perusteella

  Tällä hetkellä myyntiehdotus voidaan käynnistää myyntitilauksista, laskuista ja tarjouksista. Haku voidaan tehdä seuraavissa asiakirjoissa:

  * Myyntitilaukset
  * Myyntitarjoukset
  * Myyntilaskut
  * Kirjatut myyntilaskut
  * Kirjatut myyntitoimitukset

  Copilot tekee hakuja seuraavissa kentissä

  * Asiakirjanro
  * Ulkoinen asiakirjanro
  * Viitteesi
  * Tarjouksen nro
  * Asiakirjan päivämäärä
  * Tilausasiakkaan asiakasnro

  Copilot ei palauta Nimike-tyypin kaikkia rivejä. Vain nimikenumerot, varianttikoodit ja määrät siirretään. Lähdeasiakirjan määrät muunnetaan **myynnin mittayksiköksi**.

## Millä maantieteellisillä alueilla ja kielillä myyntiriviehdotukset ovat saatavana?

Kanadaa lukuun ottamatta tämä ominaisuus on saatavana kaikissa ympäristöissä, maa- tai aluelokalisoinnissa ja kaikilla tuetuilla kielillä. Rajoitetun kielituen vuoksi ominaisuus ei ole aluksi kanadalaisten asiakkaiden käytettävissä, koska ominaisuus ei ole kielen osalta säädösten mukainen. Tämän ominaisuuden saatavuus niiden maiden ja alueiden asiakasympäristöissä, joissa Azure OpenAI Servicea ei ole otettu käyttöön, edellyttää, että järjestelmänvalvojien on ensin annettava suostumus tietojen siirtämiseen rajojen, jotta [!INCLUDE [prod_short](includes/prod_short.md)] voi muodostaa yhteyden Azure OpenAI Serviceen.  

## Mitkä operatiiviset tekijät ja asetukset mahdollistavat ominaisuuden tehokkaan ja vastuullisen käytön?

Tekoälypohjaiset ehdotukset voivat joskus olla virheellisiä tai epätäydellisiä. Copilotin ehdotusten oikeellisuus on aina tarkistettava ennen päätöstä ehdotusten säilyttämisestä. Copilotin ehdotuksia ei tallenneta [!INCLUDE [prod_short](includes/prod_short.md)] -tietokantaan ennen **Säilytä se** -painikkeen valintaa ja Copilot-ikkunan sulkemista. Ehdotuksia voi muokata ja korjata joko ennen kuin ne päätetty säilyttää tai sen jälkeen kun ne on lisätty myyntiasiakirjaan.

### Mitä järjestelmänvalvojilta ja loppukäyttäjiltä odotetaan myyntiriviehdotuksia käytettäessä?

Kukin yksittäinen käyttäjä tekee oman valinnan **myyntiriviehdotusten** käyttämisestä. Vaikka järjestelmänvalvoja on ottanut ominaisuuden käyttöön ja se on käytettävissä, käyttäjä voi valita, käytetäänkö sitä aina, joskus vai ei koskaan.  

Järjestelmänvalvojat päättävät viime kädessä, käytetäänkö Copilotin ominaisuuksia [!INCLUDE [prod_short](includes/prod_short.md)]issa. Jos järjestelmänvalvojat ottavat Copilotin käyttöön, heidän on varmistettava, että he myöntävät sen käyttöoikeuden soveltuville käyttäjille.   

> [HUOMAUTUS!]
> - Ominaisuutta ei tueta [!INCLUDE [prod_short](includes/prod_short.md)]in paikallisissa versioissa tai yksityisessä pilvessä.
> - Kumppanit eivät voi laajentaa tätä ominaisuutta. Niinpä kumppanikehittäjät eivät voi muokata, korvata eivätkä laajentaa sitä.

## Onko Copilot ainoa tapa luoda myyntirivejä?  

Ei. Copilotin käyttö on valinnaista. [!INCLUDE [prod_short](includes/prod_short.md)]issa on muita kuin tekoälypohjaisia tapoja lisätä myyntirivejä ja kopioida asiakirjoja. Organisaatiot voivat käyttää molempia vaihtoehtoja samanaikaisesti.  

## Miten annetaan palautetta tekoälyn luomasta sisällöstä?  

Aina kun Copilot tekee ehdotuksia, voit antaa palautetta Microsoftille suoraan Copilot-ikkunasta Tykkää- ja Ei tykkää -painikkeilla. Palaute pysyy anonyymina, ja näitä tietoja käytetään palvelun laadun parantamiseen.  

## Katso myös

[Rivien ehdottaminen myyntitilaukseen Copilotin avulla](sales-suggest-sales-lines-with-copilot.md)  
[Copilotin ja tekoälyn ominaisuuksien määrittäminen](enable-ai.md)  
[Dynamics 365 Business Centralin vastuullisen tekoälyn usein kysytyt kysymykset](responsible-ai-overview.md)  
