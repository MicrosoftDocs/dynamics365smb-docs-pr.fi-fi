---
title: Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla
description: Tässä artikkelissa on vastauksia yleisiin Business Centralin keskustelua Copilotin avulla koskeviin kysymyksiin.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 02/27/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Tässä artikkelissa on vastauksia yleisiin [!INCLUDE[prod_short](includes/prod_short.md)]in keskustelua Copilotin avulla koskeviin kysymyksiin. Lisätietoja tekoälyyn ja keskusteluun liittyvistä kysymyksistä on kohdassa [Vastuullisen tekoälyn usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla (esiversio)](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Voivatko järjestelmänvalvojat myöntää keskustelun käyttöoikeuden yksittäisille käyttäjille tai kieltää sen?

Ei, sillä keskusteluun ei tarvita käyttöoikeuksia tai käyttöoikeuksien joukkoa. Jos keskustelu aktivoidaan [Copilotin ja tekoälyn ominaisuuksien määrittäminen](enable-ai.md) -sivulla, kaikki ympäristön käyttäjät saavat käyttää keskustelua.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Onko keskustelu saatavana tabletissa, puhelimessa ja muissa laitetyypeissä?

Ei. Keskusteluruutu on saatavana vain [!INCLUDE[web_client](includes/web_client.md)] -verkkoasiakasohjelmassa.

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Business Centralin käyttökieli ei ole englanti. Mitä vaihtoehtoja on käytettävissä?

Tällä hetkellä keskustelu on saatavana vain englanninkielisenä. Englanti voidaan vaihtaa käyttäjän kieleksi [omissa asetuksissa](ui-change-basic-settings.md#language).

## <a name="which-business-central-version-do-i-need-to-experience-chat"></a>Mikä Business Central -versio tarvitaan keskustelun käyttämiseen?

Keskustelu on saatavana julkisena esiversiona versiosta 24.0 alkaen (vuoden 2024 1. julkaisuaalto).

## <a name="does-chat-work-with-my-customizations"></a>Voiko keskustellussa käyttää mukautuksia?

Se määräytyy Copilotilta kysyttävän kysymyksen tyypin mukaan. Esimerkki:

- Kun kysymysten avulla paikannetaan tietueita, Copilot löytää tietueita mukautetuista taulukoista, jotka on määritetty mukautettujen kenttien avulla.
- Selitystä tai ohjeita pyydettäessä Copilot ei voi käyttää mukautuksia koskevia tietoja tai lisäosien ohjeita.

## <a name="copilot-never-seems-to-open-the-record-or-page-i-asked-for-what-am-i-doing-wrong"></a>Copilot ei näytä koskaan avaavan pyydettyä tietuetta tai sivua. Mikä on vialla?

Kun Copilotia pyydetään etsimään tietueita [!INCLUDE[prod_short](includes/prod_short.md)]issa, se näyttää kaikki löydetyt tietueet valittavina ruutuina tai linkkeinä keskusteluruudussa. Esiversiossa Copilot ei siirry automaattisesti millekään sivulle.

## <a name="the-answers-i-get-from-copilot-vary-even-though-i-ask-the-same-question-is-it-a-bug"></a>Copilotin antavat vastaukset vaihtelevat, vaikka kysymys on sama. Onko tämä virhe?

Copilot voi aina joskus antaa erilaisia vastauksia. Vastaukset eivät välttämättä ole täysin samoja.

## <a name="when-should-i-use-the-copy-function-on-chat-messages"></a>Milloin kopiointitoimintoa kannattaa käyttää keskustelun viesteissä?

Kopiointipainikkeella voi kopioida viestin Copilot-keskustelun aiemmasta vaiheesta, liittää sen syöteruutuun uudelleenyrittämistä varten tai kokeilla Copilotiin lähettyä viestiä vähän eri muodossa.

## <a name="how-do-i-customize-or-extend-chat"></a>Miten keskustelua mukautetaan tai laajennetaan?

Esiversiossa keskusteluruutua ja Copilotin vastauksia ei voi muokata millään tavalla mukautusten, lisäosien tai räätälöinnin avulla.

## <a name="does-copilot-find-data-in-other-companies-or-environments"></a>Etsiikö Copilot tietoja muista yrityksistä tai ympäristöistä?

Vaikka organisaatio käyttäisi useita ympäristöjä tai yrityksiä tietojen erotteluun, Copilot etsii tietueita vain siitä yrityksestä, johon ollaan kirjautuneena.

## <a name="the-copilot-chat-pane-doesnt-show-what-can-i-do"></a>Copilot-keskusteluruutu ei ole näkyvissä. Mitä voin tehdä?

Tarkista, että käyttäjän kielimääritys omissa asetuksissa on englanti ja että ympäristön versio on 24.0 tai uudempi. Varmista Copilotin ja tekoälyn ominaisuuksien määrittäminen -sivulla, että järjestelmänvalvojat ovat hyväksyneet tietojen siirron maantieteellisten alueiden välillä ja aktivoineet keskustelun. Varmista, että ympäristön lokalisointina ei ole Kanada.

Jos Keskustelu Copilotin avulla -ominaisuus ei ole vieläkään näkyvissä, on mahdollista, että Microsoft on vasta ottamassa ominaisuuden käyttöön alueella. Copilot otetaan ensin käyttöön yhdysvaltalaisille asiakkaille huhtikuussa 2024 ja seuraavien viikkojen aikana se otetaan käyttöön muissa maakohtaisissa lokalisoinneissa.

## <a name="next-steps"></a>Seuraavat vaiheet

[Keskustelu Copilotin avulla (esiversio)](chat-with-copilot.md)
