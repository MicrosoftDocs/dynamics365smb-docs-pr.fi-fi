---
title: Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla
description: Tässä artikkelissa on vastauksia yleisiin Business Centralin keskustelua Copilotin avulla koskeviin kysymyksiin.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Tässä artikkelissa on vastauksia yleisiin [!INCLUDE[prod_short](includes/prod_short.md)]in keskustelua Copilotin avulla koskeviin kysymyksiin. Lisätietoja tekoälyyn ja keskusteluun liittyvistä kysymyksistä on kohdassa [Vastuullisen tekoälyn usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla (esiversio)](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Voivatko järjestelmänvalvojat myöntää keskustelun käyttöoikeuden yksittäisille käyttäjille tai kieltää sen?

Ei, sillä keskusteluun ei tarvita käyttöoikeuksia tai käyttöoikeuksien joukkoa. Jos keskustelu aktivoidaan [Copilotin ja tekoälyn ominaisuuksien määrittäminen](enable-ai.md) -sivulla, kaikki ympäristön käyttäjät saavat käyttää keskustelua.
 
## Onko keskustelu saatavana tabletissa, puhelimessa ja muissa laitetyypeissä?

Ei. Keskusteluruutu on saatavana vain [!INCLUDE[web_client](includes/web_client.md)] -verkkoasiakasohjelmassa.

## Business Centralin käyttökieli ei ole englanti. Mitä vaihtoehtoja on käytettävissä?

Tällä hetkellä keskustelu on saatavana vain englanninkielisenä. Englanti voidaan vaihtaa käyttäjän kieleksi [omissa asetuksissa](ui-change-basic-settings.md#language).

## Mikä Business Central -versio tarvitaan keskustelun käyttämiseen?

Keskustelu on saatavana julkisena esiversiona versiosta 24.0 alkaen (vuoden 2024 1. julkaisuaalto).

## Voiko keskustellussa käyttää mukautuksia?

Se määräytyy Copilotilta kysyttävän kysymyksen tyypin mukaan. Esimerkki:

- Kun kysymysten avulla paikannetaan tietueita, Copilot löytää tietueita mukautetuista taulukoista, jotka on määritetty mukautettujen kenttien avulla.
- Selitystä tai ohjeita pyydettäessä Copilot ei voi käyttää mukautuksia koskevia tietoja tai lisäosien ohjeita.

## Copilot ei näytä koskaan avaavan pyydettyä tietuetta tai sivua. Mikä on vialla?

Kun Copilotia pyydetään etsimään tietueita [!INCLUDE[prod_short](includes/prod_short.md)]issa, se näyttää kaikki löydetyt tietueet valittavina ruutuina tai linkkeinä keskusteluruudussa. Esiversiossa Copilot ei siirry automaattisesti millekään sivulle.

## Copilotin antavat vastaukset vaihtelevat, vaikka kysymys on sama. Onko tämä virhe?

Copilot voi aina joskus antaa erilaisia vastauksia. Vastaukset eivät välttämättä ole täysin samoja.

## Milloin kopiointitoimintoa kannattaa käyttää keskustelun viesteissä?

Kopiointipainikkeella voi kopioida viestin Copilot-keskustelun aiemmasta vaiheesta, liittää sen syöteruutuun uudelleenyrittämistä varten tai kokeilla Copilotiin lähettyä viestiä vähän eri muodossa.

## Miten keskustelua mukautetaan tai laajennetaan?

Esiversiossa keskusteluruutua ja Copilotin vastauksia ei voi muokata millään tavalla mukautusten, lisäosien tai räätälöinnin avulla.

## Etsiikö Copilot tietoja muista yrityksistä tai ympäristöistä?

Vaikka organisaatio käyttäisi useita ympäristöjä tai yrityksiä tietojen erotteluun, Copilot etsii tietueita vain siitä yrityksestä, johon ollaan kirjautuneena.

## Copilot-keskusteluruutu ei ole näkyvissä. Mitä voin tehdä?

Tarkista, että käyttäjän kielimääritys omissa asetuksissa on englanti ja että ympäristön versio on 24.0 tai uudempi. Varmista Copilotin ja tekoälyn ominaisuuksien määrittäminen -sivulla, että järjestelmänvalvojat ovat hyväksyneet tietojen siirron maantieteellisten alueiden välillä ja aktivoineet keskustelun. Varmista, että ympäristösi lokalisointi ei ole Kanada.

Jos Keskustelu Copilotin avulla -ominaisuus ei ole vieläkään näkyvissä, on mahdollista, että Microsoft on vasta ottamassa ominaisuuden käyttöön alueella. Copilot otetaan ensin käyttöön yhdysvaltalaisille asiakkaille huhtikuussa 2024 ja seuraavien viikkojen aikana se otetaan käyttöön muissa maakohtaisissa lokalisoinneissa.

## Miksi Copilot näyttää vain kolme tietuetta keskusteluruudussa?

Kun pyydät Copilotia hakemaan tietueita, tapa, jolla muotoilet kysymyksen, määrittää sen, miten Copilot tunnistaa ja käyttää sivuilla suodattimia löytääkseen etsimäsi. Jotta vastaukset pysyvät kompakteina ja ytimekkäinä, keskusteluruudussa on enintään kolme tietueruutua, vaikka Copilot löytäisi suuremman määrän asianmukaisia tietueita.

## Copilot palauttaa virheellisiä vastauksia kokonaissummia ja muita laskentoja varten

Esikatselun aikana Keksustelu Copilotin avulla -ominaisuus voi etsiä tietueita, selittää käsitteitä ja opastaa Business Centralin tehtävien suorittamisessa. Muita käyttötapauksia ei tueta, kuten kentän laskeminen tietueissa tai keskimääräisen kuukausisumman laskeminen. Toivomme voivamme lisätä tulevaisuudessa matematiikan peruskykyjä Copilotiin.

## Voinko käyttää puhetta sen sijaan, että kirjoitan kehotteitani?

Voit keskustella Copilotin kanssa kirjoittamalla äänikirjoituksen puheille, sen sijaan että kirjoittaisit sanasi Keskusteluruutuun. Äänikirjoituksessa käytetään online-puheentunnistusta, ja se on käytettävissä Windowsissa. Kun haluat käyttää ääntä, aktivoi chat-viestiruutu, käytä <kbd>Windows</kbd>+<kbd>H</kbd> -pikanäppäintä ja aloita puhuminen. Lisätietoja on kohdassa [Äänikirjoittaminen tietokoneella puhumista varten kirjoittamisen sijaan](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## Seuraavat vaiheet

[Keskustelu Copilotin avulla (esiversio)](chat-with-copilot.md)
