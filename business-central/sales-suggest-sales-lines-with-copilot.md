---
title: Copilotin myyntiriviehdotukset
description: Tietoja rivien ehdottamisesta myyntitilauksessa Copilotin avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# Rivien ehdottaminen myyntiasiakirjoissa Copilotin avulla (esiversio)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Tässä artikkelissa käsitellään myyntiasiakirjojen luonnin nopeuttamista antamalla Copilotin ehdottaa asiakkaiden myyntiasiakirjojen riveille lisättäviä nimikkeitä.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Tietoja Copilotin myyntiriviehdotuksista

Copilotin myyntiriviehdotus voi auttaa luomaan rivejä myyntiasiakirjoihin, kuten myyntitarjouksiin, tilauksiin ja laskuihin, jäsennetyn syötön tai luonnollisen kielen perusteella. Ominaisuus ei ole yleinen keskustelu vaan erittäin kohdistettu ja integroitu kokemus, jota voi käyttää myyntiasiakirjoissa. Ominaisuudessa on kaksi erillistä taitoa, jotka auttavat etsimään yksittäisiä tuotteita tai koko asiakirjoja koskevia tietoja.

* Tuotteiden etsiminen

  Useisiin paikkoihin [!INCLUDE [prod_short](includes/prod_short.md)]issa tallennettuja tuotteita kuvailevat tiedot. Esimerkiksi nimikenumerot ja -kuvaukset tallennetaan **Nimike**-taulukkoon, useita viivakoodeja tallennetaan **Nimikeviittaus**-taulukkoon ja tuoteominaisuudet tallennetaan **Nimikemääritteet**-taulukkoon. Vaikka kehote voi olla *punainen polkupyörä*, varsinainen tuote onkin *tulipunainen matkapyörä*, jossa *polkupyörä* on tuoteluokka ja *punainen* määrite.

* Asiakirjojen etsiminen viitteen perusteella

  Ihmiset toistavat usein edellisen tilauksen tai ainakin käyttävät sitä aloituskohtana. Oikean tilauksen löytäminen tilauspinosta voi olla kuitenkin hankalaa. Muistissa on ehkä tilaustunnuksen osa, joka voi olla yritykselle määritetty numero tai asiakkaalta saatu viitanumero. Kehotteet, kuten *tarvitsen huhtikuun viimeisen laskun*, todennäköisesti nopeuttavat tilauksen löytämistä.

## Käytettävissä olevat kielet

[!INCLUDE[sales-lines-suggestions-language-support](includes/sales-lines-suggestions-language-support.md)]

## Vaatimukset

* Järjestelmänvalvoja ottaa Copilotin myyntiriviehdotuksen käyttöön ja aktivoi sen. Lisätietoja tekoälyominaisuuksien käyttöönottamisesta on kohdassa [Copilot- ja tekoälyominaisuuksien määrittäminen](enable-ai.md).
* Myyntitilausten luominen on tuttua.

## Esimerkkejä kehotteista

Copilotin myyntiriviehdotuksissa voidaan käsitellä monenlaisia kehotesyötteitä. Tässä osassa on esimerkkejä erilaisissa skenaarioissa testattuja kehotteita.

### Esimerkkikysely aiemman asiakirjan toistamisesta

Kehote: *Tarvitse kaikki tuotteet laskusta 103031*

### Käyttäjä kirjoittaa puhelun aikana nopeasti luettelon tarvittavista tuotteista ja määristä, mutta nämä tiedot eivät ole aina riittävän tarkkoja tai niissä käytetään sisäisiä tuotenimiä

Kehote: *2 punasta lasten pyörää*

Kannattaa huomata, että kehote toimii kirjoitusvirheitä huolimatta.

### Käyttäjä kopioi kyselyn saapuvasta viestinnästä ja liittää sen Myyntirivien ehdotukset -sivulle

Kehote: *Hei, olen kiinnostunut ostamaan oheislaitteita kannettavaan XXXX-tietokoneeseen, kuten langattoman hiiren, näppäimistön suojuksen ja tietokonelaukun. Haluaisin näitä nimikkeitä koskevia suosituksia tai ehdotuksia. Onko kanta-asiakkaille erityistarjouksia tai alennuksia? Terveisin, M*

Kannattaa huomata, että kannettava XXXX-tietokone ei sisälly hakuun.

## Rivien ehdottaminen myyntiasiakirjassa

Tässä prosessissa käsitellään rivien ehdottamista myyntitilauksessa. Vaiheet ovat samat myyntitarjouksissa ja -laskuissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaus** ja valitse sitten vastaava linkki.
1. Avaa myyntitilaus.
1. Valitse **Rivit**-pikavälilehdessä **Hae riviehdotukset**.
1. Syötä kehote **Copilotin riviehdotukset** -ikkunassa tai valitse kehoteohje.

## Ehdotusten tarkistaminen, tallentaminen, hylkääminen tai luominen uudelleen

Tarkista Copilotin ehdottamat riveillä lisättävät nimikkeet ja päätä, vastaavatko ne tarkoitusta:

* Hylkää yksittäinen ehdotettu rivi, valitsemalla se luettelossa ja valitsemalla sitten **Poista rivi** -toiminto.
* Hylkää kaikki ehdotetut rivit ja sulje Copilot-ikkuna valitsemalla hylkäyspainike (roskakori) **Säilytä se** -painikkeen vieressä.
* Siirrä kaikki Copilot-ikkunassa näkyvät rivit valitsemalla **Säilytä se**. 

**Luotettavuus**-kentässä on näkyvissä pistemäärä, **Korkea (80+)**, **Keskitaso (60–80)** ja **Matala(60-)**. Tämä pistemäärä ilmaisee toimia edellyttävät rivit.

Tämä vaihe varmistaa, että rivit halutaan siirtää myyntiasiakirjaan. Siirrettyjä rivejä voi poistaa tai muokata myös myyntiasiakirjassa, tai koko asiakirja voidaan poistaa.

## Katso myös

[Usein kysyttyjä kysymyksiä Copilotin myyntiriviehdotuksista](faq-sales-suggest-sales-lines-with-copilot.md)
[Copilotin ja tekoälyn ominaisuuksien määrittäminen](enable-ai.md)
