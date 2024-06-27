---
title: Usein kysyttyjä kysymyksiä analyysiavustajasta (esiversio)
description: 'Näissä usein kysytyissä kysymyksissä on tietoja tietojen analysoinnista Business Centralin sivuilla käytettävästä tekoälyteknologiasta. Niissä käsitellään tärkeitä huomioitavia ja niissä on tietoja siitä, miten tekoälyä käytetään sekä miten sitä on testattu ja arvioitu. Lisäksi käsitellään mahdollisia rajoituksia.'
ms.date: 06/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# Usein kysyttyjä kysymyksiä analyysiavustajasta (esiversio)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Näissä usein kysytyissä kysymyksissä käsitellään tekoälyn vaikutusta [!INCLUDE[prod_short](includes/prod_short.md)]in analyysiavustajaominaisuudessa.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Mikä on analyysiavustaja?

Analyysiavustaja on Copilot, joka auttaa käyttämään Business Centralin [tietoanalyysitilaa](analysis-mode.md). Tietoanalyysitila mahdollistaa sivujen ja kyselyjen järjestämisen ja koostamisen sekä yhteenvetojen laatimisen niistä, mikä helpottaa niiden analysointia ja merkityksellisten tietojen saamista. Analyysiavustajan avulla analysoitavista tiedoista voidaan muodostaa automaattisesti näkymä. Tämä tehdään ilmaisemalla tarpeet yksinkertaisella, luonnollisella kielellä pyytämällä esimerkiksi näyttämään toimittajakohtaiset sijainnit ostojen määrän mukaan lajiteltuna. Analyysiavustaja helpottaa tietojen käsittelyä ilman monipuolisia teknisiä taitoja.

## Mitä ominaisuuksia analyysiavustajassa on?

Analyysiavustaja pohjautuu Business Centralin Copilotin kehittäjätyökaluihin. Se käyttää Azure OpenAI Serviceä muuntamaan jäsentämättömät ohjeet jäsennetyksi rakenteeksi, jotta tiedot voidaan näyttää analyysitilassa. Tämä on mahdollista ilman, että asiakkaan liiketoimintatietoja olisi luotava, muokattava tai päivitettävä.

## Mikä on analyysiavustajan käyttötarkoitus?

Analyysiavustaja auttaa luomaan tietoanalyysitilassa analyysivälilehtiä, joissa tiedot esitetään johtopäätösten tekemistä edistävällä tavalla. On kuitenkin tärkeää muistaa, että analyysiavustaja ei anna suoraan merkityksellisiä tietoja tai tee tiedoista johtopäätöksiä. Se on työkalu, joka auttaa käyttäjiä järjestelemään ja tarkastelemaan tietojaan. On käyttäjän vastuulla poimia toimintaa ohjaavia tietoja, havaita trendejä ja tietopohjaisia, liiketoiminnan arvoa edistäviä päätöksiä.

## Miten analyysiavustaja arvioitiin? Mitä mittareita suorituskyvyn mittaamiseen käytetään?

- Ominaisuus testattiin kattavasti [!INCLUDE[prod_short](includes/prod_short.md)]in esittelytietoja muiden kuvitteellisten tuotekatalogien perusteella. Copilotille annettiin lukuisia kehotteita tuetuilla englannin kielialueilla. Kehotteet kattoivaa laaja-alaisesti tietoanalyysiohjeita ja tarkoituksen ilmaisutyylejä. Tulokset arvioitiin tarkkuuden, osuvuuden ja turvallisuuden perusteella.

- Ominaisuus pohjautuu Microsoftin vastuulliseen tekoälystandardiin. [Lisätietoja Microsoftin vastuullisesta tekoälystä.](https://aka.ms/RAI)

## Miten Microsoft seuraa luodun sisällön laatua?

Microsoftilla on erilaisia järjestelmiä, joilla varmistetaan, että Copilotin luoma sisältö on korkealaatuista, havaitsee väärinkäytön sekä varmistaa asiakkaiden ja heidän tietojensa turvallisuuden.

Käyttäjillä on mahdollisuus antaa palautetta jokaisesta Copilotin vastauksesta ja ilmoittaa epätarkasta tai epäsopivasta sisällöstä, mikä auttaa Microsoftia parantamaan ominaisuutta.

- Jos kohtaat sopimatonta sisältöä, ilmoita siitä Microsoftille käyttämällä tätä palautelomaketta: [Ilmoita väärinkäytöstä](https://go.microsoft.com/fwlink/?linkid=2249810)

- Käyttäjän ominaisuudessa antama palaute analysoidaan ja sitä käytetään parantamaan vastauksia.

  Palautetta annetaan [!INCLUDE[prod_short](includes/prod_short.md)]in **Copilot**-sivun tykkää (peukalo ylös)- ja ei tykkää (peukalo alas) -kuvakkeella.

- Microsoft voi poistaa Copilotiin liittyvät toiminnot käytöstä valittujen asiakkaiden osalta, jos toimintojen väärinkäyttö havaitaan.

## Mitä rajoituksia analyysiavustajassa on? Miten käyttäjät voivat minimoida analyysiavustajan rajoitukset, kun he käyttävät järjestelmää?

- Tekoälyn yleiset rajoitukset:

  Tekoälyjärjestelmät ovat arvokkaita työkaluja ne eivät ole deterministisiä. Niiden luoma sisältö ei ole ehkä virheetöntä. Tämän vuoksi on tärkeää arvioida ja varmistaa vastauksen ennen sidosryhmiä, kuten asiakkaita ja kumppaneita, koskevien päätösten tekemistä.

- Käytettävissä olevat kielet

   [!INCLUDE[analysis-assist-language-support](includes/analysis-assist-language-support.md)]

   Vastausten laatu voi olla myös huonompi, jos Business Centralin käyttäjän kieliasetus poikkeaa [!INCLUDE[prod_short](includes/prod_short.md)] -tietokannassa olevien yritystietojen ensisijaisesta kielestä.
  
- Maantieteellinen rajoitus:
  
   Ominaisuus on käytettävissä kaikilla tuetuilla [Business Centralin maissa/alueilla](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)<!-- except for Canada-->. Ominaisuus kuitenkin käyttää Microsoft Azure OpenAI Servicea, joka on tällä hetkellä saatavana Business Centralissa joillakin maantieteellisillä alueilla. Jos ympäristö sijaitsee maassa tai alueella, jossa Azure OpenAI Service ei ole saatavana, järjestelmänvalvojien on sallittava tietojen siirtojen maantieteellisten alueiden välillä. [Lue lisätietoja Copilot-tietojen siirtämisestä maantieteellisten alueiden välillä](/dynamics365/business-central/ai-copilot-data-movement).

- Toimialue-, tuote- ja aihekohtaisia rajoituksia:

  Tietyillä liiketoiminta-alueilla, jotka koskevat lääketiedettä, huumeita, lainsäädäntöä ja aseita, palvelun laatu saattaa heikentyä.

## Mitä tietoja analyysi kerää ja miten niitä käytetään?

Analyysiavustajaominaisuus kerää vain ne tiedot, joita Business Central tarvitsee palvelun tarjoamiseen. Microsoft ei käytä yrityksen tietoja, mukaan lukien Copilotiin lähettyä tekstiä, muiden käyttöön tarkoitettujen perusmallien kouluttamiseen. Lisätietoja on kohdassa [Dynamics 365:n käyttöehdot Azure OpenAI -pohjaisille ominaisuuksille](https://go.microsoft.com/fwlink/?linkid=2236010).

Se kerää tietoja myös palautteesta, jota käyttäjät voiva antaa käyttämällä analyysiavustajan **Copilot**-sivun yläosassa olevia tykkää (peukalo ylös)- tai en tykkää (peukalo alas) -kuvakkeita. Tiedot ovat anonyymeja ja sisältävät vaihtoehtoina tykkäämiseen ja ei-tykkäämisen, ei-tykkäämisen syyn, jos se on annettu, ja Copilot-ominaisuuden, jota palaute koskee.

## Katso myös

[Tietojen analysointi Copilotin avulla (esiversio)](analysis-assist.md)
