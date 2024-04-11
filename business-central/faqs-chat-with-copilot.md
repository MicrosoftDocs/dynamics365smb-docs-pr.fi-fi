---
title: Vastuullisen tekoälyn usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla (esiversio)
description: 'Näissä usein kysytyissä kysymyksissä on tietoja Business Centralin keskustelussa Copilotin avulla. Niissä käsitellään tärkeitä huomioitavia ja niissä on tietoja siitä, miten tekoälyä käytetään sekä miten sitä on testattu ja arvioitu. Lisäksi käsitellään mahdollisia rajoituksia.'
ms.date: 03/18/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# Vastuullisen tekoälyn usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla (esiversio)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Näissä usein kysytyissä kysymyksissä käsitellään tekoälyn vaikutusta [!INCLUDE[prod_short](includes/prod_short.md)]in keskusteluun Copilotin avulla. Lisätietoja ominaisuuden käyttöön liittyvistä yleisistä kysymyksistä on kohdassa [Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla](chat-with-copilot-faq.md).

## Keskustelu Copilotin avulla – mikä se on?

Microsoft Copilot on tekoälypohjainen avustaja, joka inspiroi toimimaan luovasti, tehostaa tuottavuutta ja poistaa tarpeen tehdä pitkäveteisiä tehtäviä. Keskustelemalla Copilotin avulla Business Centralissa saadaan vastauksia kysymyksiin ja löydetään liiketoimintatietoja. Keskustelun tavoite ilmaistaan luonnollisella kielellä.

Keskustelun Copilotin kanssa tai lyhyemmin keskustelu on vuorovaikutteinen ominaisuus, joka vastaa kysymyksiin ja etsii [!INCLUDE[prod_short](includes/prod_short.md)]iin liittyviä liiketoimintatietoja ilman, että käyttäjien olisi siirryttävä käyttöliittymässä tai tuoteohjeissa. Copilot-ruutua voi käyttää kaikkialta [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmassa.

Käyttäjät kysyvät kysymyksiä luonnollisella kielellä. Esimerkkejä: Voidaanko tavarat toimittaa asiakkaille suoraan toimittajilta? tai Onko varastossa työtuoleja, joiden hinta on alle 600 $? Copilot vastaa kysymyksiin luonnollisella kielellä. Kysymykset määrittävät, onko vastauksen sisältö vain teksti -muotoinen, linkkejä [!INCLUDE[prod_short](includes/prod_short.md)]in tietueisiin tai sivuille ja linkkejä [!INCLUDE[prod_short](includes/prod_short.md)]in ohjeartikkeleihin Microsoft Learnissa.

## Minkälaisia ominaisuuksia keskustelussa Copilotin kanssa on?

Keskustelua Copilotin avulla voi käyttää vastausten saamiseen seuraavien luokkien kysymyksiin:

### Selittäminen ja opastaminen

Käyttäjät voivat pyytää Copilotia selittämään tiettyjä [!INCLUDE[prod_short](includes/prod_short.md)]iin liittyviä käsitteitä, kuten dimensiot, tai opastamaan tehtävän suorittamisessa, kuten myyntitilauksen kirjaamisessa. Copilot hakee tietoa Microsoftin julkaisemista virallisista [!INCLUDE[prod_short](includes/prod_short.md)]in ohjeista ja vastaa kysymyksiin ohjeiden perusteella.

- Copilot Microsoft Learnissa olevaa tietoa (eikä laajaa verkkohakua), kun se tekee Microsoft Learnissa semanttisia hakuja ainoastaan Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)] -ohjeissa.

- Copilot ei suorita toimintoja, luo uutta tietoa tai muokkaa määrityksiä. Sen sijaan se laatii yhteenvedon Microsoft Learnista löytyneistä keskustelun kysymystä tai kehotetta vastaavista kappaleista.

### Yritystietojen ja niihin liittyvien sivujen etsiminen

Käyttäjät voivat pyytää Copilotia paikantamaan sivuja nimen perusteella tai pyytää tietueita niiden kenttien ja rajoitusten perusteella. Jos Copilot löytää vastineen, sen vastaus sisältää soveltuvan tietueen tai sivun linkin, jonka avaamisen käyttäjä voi valita.

- Copilot muuntaa luonnollisen kielisen syötteen kyselyksi, joka koostuu taulukon haku-, lajittelu- ja suodatusehdoista.

  Ominaisuus etsii [!INCLUDE[prod_short](includes/prod_short.md)]in omien tietohakuominaisuuksien avulla vastaavia tietoja yrityksin tietokannan taulukoista. Haku suoritetaan käyttäjän käyttäjätiedoilla suojauksen ja vaatimustenmukaisuuden vuoksi. Se ei tee hakuja [!INCLUDE[prod_short](includes/prod_short.md)] -tietokannan ulkopuolella.

- Copilot ei suorita toimintoja, luo uutta tietoa tai muokkaa määrityksiä. Se vain laatii yhteenvedon tietueista, jotka saatiin [!INCLUDE[prod_short](includes/prod_short.md)]in oman tietohaun tuloksena. 

## Mihin keskustelua Copilotin avulla on tarkoitus käyttää?

Keskustelu on suunniteltu yrityskäyttöön vastaamaan kysymyksiin, jotka liittyvät [!INCLUDE[prod_short](includes/prod_short.md)]iin ja sen sisältämiin liiketoimintatietoihin. Ominaisuus antaa käyttäjille mahdollisuuden ratkaista yleisiä tehtäviä, kuten tietueiden etsimistä ja opastusta itsensä ilmaisemiseen omin sanoin, mikä helpottaa [!INCLUDE[prod_short](includes/prod_short.md)]in käyttöä.

## Miten keskustelu Copilotin avulla arvioitiin? Mitä mittareita suorituskyvyn mittaamiseen käytetään?

- Ominaisuuden laajan testauksen aikana Copilotiin syötettiin runsaasti englanninkielisiä tekstejä, jotka käsittelevät monenlaisia aiheita ja tarkoituksia ilmaisevia tyylejä. Tulokset arvioitiin tarkkuuden, osuvuuden ja turvallisuuden perusteella.
- Ominaisuus pohjautuu Microsoftin vastuulliseen tekoälystandardiin. [Lisätietoja Microsoftin vastuullisesta tekoälystä](https://aka.ms/RAI).

## Miten Microsoft seuraa luodun sisällön laatua?

Microsoftilla on erilaisia järjestelmiä, joilla varmistetaan, että Copilotin luoma sisältö on korkealaatuista, havaitsee väärinkäytön sekä varmistaa asiakkaiden ja heidän tietojensa turvallisuuden.

Käyttäjillä on mahdollisuus antaa palautetta jokaisesta Copilotin vastauksesta ja ilmoittaa epätarkasta tai epäsopivasta sisällöstä, mikä auttaa Microsoftia parantamaan ominaisuutta. 

- Palautetta annetaan [!INCLUDE[prod_short](includes/prod_short.md)]in **Copilot**-sivun tykkää (peukalo ylös)- ja ei tykkää (peukalo alas) -kuvakkeella.
- Käyttäjän ominaisuudessa antama palaute analysoidaan ja sitä käytetään parantamaan vastauksia.
- Jos kohtaat sopimatonta sisältöä, ilmoita siitä Microsoftille käyttämällä tätä palautelomaketta: [Ilmoita väärinkäytöstä](https://go.microsoft.com/fwlink/?linkid=2249810).
- Microsoft voi poistaa Copilotiin liittyvät toiminnot käytöstä valittujen asiakkaiden osalta, jos toimintojen väärinkäyttö havaitaan.

## Mitä rajoituksia keskustelussa Copilotin avulla on? Miten käyttäjät voivat minimoida keskustelua Copilotin avulla koskevat rajoitukset, kun he käyttävät järjestelmää?

- Tekoälyn yleiset rajoitukset

  Tekoälyjärjestelmät ovat arvokkaita työkaluja ne eivät ole deterministisiä. Niiden luoma sisältö ei ole ehkä täysin oikeellista. Tämän vuoksi on tärkeää arvioida ja varmistaa Copilotin vastauksen ennen sidosryhmiä, kuten asiakkaita ja kumppaneita, koskevien päätösten tekemistä. Useimmat Copilotin vastaukset sisältävät myös lainauksia tai viitelinkkejä, joiden avulla voidaan tarkistaa nopeasti, onko Copilotin antama vastaus oikein. Esimerkiksi pyydettäessä ohjeita jonkin tehtävän suorittamiseen Copilot sisällyttää linkit lähdeartikkeliin. Jos Copilotia pyydetään etsimään tietue tiettyjen ehtojen perusteella, se sisällyttää linkit, jotka kuvailevat keskustelun aiheeksi määritetyn luettelosivun, sekä mahdolliset suodattimet tai lajittelu, joita käyttämällä vastaukseen päädyttiin.

- Kielirajoitukset

  - Vain englanninkielistä keskustelu tuetaan seuraavilla kielialueilla: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Jos [!INCLUDE[prod_short](includes/prod_short.md)]in näyttökieli ei ole jokin edellä mainituista kielialueista, keskustelu ei ole käytettävissä.

  - Seuraavat seikat voivat heikentää vastausten laatua:
    - Kielialue on jokin muu kuin en-US.
    - [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjän kieliasetus ei ole sama kuin [!INCLUDE[prod_short](includes/prod_short.md)] -tietokannassa olevien tietojen ensisijainen kieli.

- Toimiala-, tuote- ja aihekohtaiset rajoitukset

   Keskustelu sisältää suojamekanismeja, jotka estävät ei-toivotun, haitallisen sisällön luonnin, kuten seksuaalissävytteisen tai väkivaltaan yllättävän sisällön. Joskus asiakkaat toimivat sellaisilla toimialoilla, myyvät sellaisia tuotteita ja palveluja tai käyttävät sellaisia prosesseja, joita voitaisiin muissa yhteyksissä pitää epäsopivina, taikka käsittelevät tietoja, jotka voisivat käynnistää nämä turvatoimet. Keskustelu ei ehkä toimi hyvin näissä tapauksissa.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## Mitä tietoja keskustelussa Copilotin avulla kerätään ja miten niitä käytetään?

Microsoft ei käytä yrityksen tietoja, mukaan lukien Copilotiin lähettyä tekstiä, muiden käyttöön tarkoitettujen perustekoälymallien kouluttamiseen. Yrityksen järjestelmänvalvojat hallitsevat täysin näitä Azure-tilaukseen kuuluvia tietoja. Koska järjestelmänvalvojilla tai muilla yrityksen työntekijöillä voi olla näiden tietojen käyttöoikeus työnantajan määrittämällä tavalla, on suositeltavaa, ettei arkaluonteisia tietoja, kuten salasanoja tai muita salaisia tietoja, syötetä.

## Miten keskustelu Copilotin avulla on suojattu?

Keskustelu on suunniteltu turvalliseksi, ja sitä käytetään käyttäjän käyttäjätietojen perusteella, joten se perii kaikki käyttöoikeudet ja muut rajoitukset. Se ei myöskään koskaan toimi [!INCLUDE[prod_short](includes/prod_short.md)]in ympäristösuojauksen ulkopuolella. Niinpä Copilot voi käyttää vain tietoja, joiden käyttöoikeus käyttäjällä on.

Jos käyttäjällä on SUPER-käyttöoikeus, keskustelun on helppo paikantaa suojaamattomat tiedot, joiden käyttäminen on yleensä hankalaa muille käyttäjille. Jos organisaatiot eivät käytä [!INCLUDE[prod_short](includes/prod_short.md)]in suojausmallia rajoittamaan käyttäjän tai käyttäjäroolin käytössä olevia taulukoita tai objekteja, keskustelun käyttö voi aiheuttaa niille enemmän riskejä. Tämän vuoksi suositellaan, että organisaatio joko toteuttaa [!INCLUDE[prod_short](includes/prod_short.md)]in suojausmallin tai poistaa keskustelun aktivoinnin.

## Katso myös

[Keskustelu Copilotin avulla (esiversio)](chat-with-copilot.md)

