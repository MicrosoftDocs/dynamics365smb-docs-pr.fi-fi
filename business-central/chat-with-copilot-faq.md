---
title: Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla
description: 'Tutustu siihen, miten voit keskustella Copilotin, Business Centralin käyttöä helpottavan virtuaaliavustajan kanssa. Etsi vastauksia keskustelutoimintoja, asetuksia ja rajoituksia koskeviin yleisiin kysymyksiin.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Tässä artikkelissa on vastauksia yleisiin [!INCLUDE[prod_short](includes/prod_short.md)]in keskustelua Copilotin avulla koskeviin kysymyksiin. Lisätietoja tekoälyyn ja keskusteluun liittyvistä kysymyksistä on kohdassa [Vastuullisen tekoälyn usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla (esiversio)](faqs-chat-with-copilot.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Voivatko järjestelmänvalvojat myöntää keskustelun käyttöoikeuden yksittäisille käyttäjille tai kieltää sen?

Ei, sillä keskusteluun ei tarvita käyttöoikeuksia tai käyttöoikeuksien joukkoa. Jos keskustelu aktivoidaan [Copilotin ja tekoälyn ominaisuuksien määrittäminen](enable-ai.md) -sivulla, kaikki ympäristön käyttäjät saavat käyttää keskustelua.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Onko keskustelu saatavana tabletissa, puhelimessa ja muissa laitetyypeissä?

Ei. Keskusteluruutu on saatavana vain [!INCLUDE[web_client](includes/web_client.md)] -verkkoasiakasohjelmassa.

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Business Centralin käyttökieli ei ole englanti. Mitä vaihtoehtoja on käytettävissä?

Tällä hetkellä keskustelu on saatavana vain englanninkielisenä. Englanti voidaan vaihtaa käyttäjän kieleksi [omissa asetuksissa](ui-change-basic-settings.md#language).

## <a name="what-version-of-business-central-do-i-need-for-chat"></a>Mikä Business Central -versio tarvitaan keskustelun käyttämiseen?

Keskustelu on saatavana julkisena esiversiona versiosta 24.0 alkaen (vuoden 2024 1. julkaisuaalto).

## <a name="does-chat-work-with-my-customizations"></a>Voiko keskustellussa käyttää mukautuksia?

Se määräytyy Copilotilta kysyttävän kysymyksen tyypin mukaan. Esimerkki:

- Jos kysyt tietueiden etsimiseen liittyviä kysymyksiä, se voi löytää tietueita mukautetuista taulukoistasi, jotka käyttävät mukautettuja kenttiä.
- Jos kysyt Copilotilta selitystä tai ohjeita, se ei voi käyttää mukautuksia koskevia tietoja tai lisäosien ohjeita.

## <a name="how-do-i-open-a-record-or-page-with-chat"></a>Miten avaan tietueen tai sivun, jossa on keskustelu?

Kun Copilotia pyydetään etsimään tietueita [!INCLUDE[prod_short](includes/prod_short.md)]issa, se näyttää kaikki löydetyt tietueet valittavina ruutuina tai linkkeinä keskusteluruudussa. Esiversiossa Copilot ei siirry automaattisesti millekään sivulle.

## <a name="why-do-i-get-different-answers-from-copilot-for-the-same-question"></a>Miksi saan Copilotilta eri vastauksia samaan kysymykseen?

Copilot voi aina joskus antaa erilaisia vastauksia. Vastaukset eivät aina ole täysin samoja.

## <a name="how-do-i-use-the-copy-function-on-chat-messages"></a>Miten Copilot-toimintoa kannattaa käyttää keskustelun viesteissä?

Kopiointipainikkeella voi kopioida viestin Copilot-keskustelun aiemmasta vaiheesta, liittää sen syöteruutuun uudelleenyrittämistä varten tai kokeilla Copilotiin lähettyä viestiä vähän eri muodossa.

## <a name="can-i-customize-or-extend-chat"></a>Voinko mukauttaa tai laajentaa keskustelua?

Esiversiossa keskusteluruutua ja Copilotin vastauksia ei voi muokata millään tavalla mukautusten, lisäosien tai räätälöinnin avulla.

## <a name="does-copilot-search-for-data-in-other-companies-or-environments"></a>Etsiikö Copilot tietoja muista yrityksistä tai ympäristöistä?

Copilot etsii tietueita vain siitä yrityksestä, jossa olet tällä hetkellä kirjautuneena. Se ei hae tietoja useista ympäristöistä tai yrityksistä.

## <a name="what-can-i-do-if-the-chat-pane-doesnt-show"></a>Mitä voin tehdä, jos keskusteluruutu ei näy?

Tarkista, että käyttäjän kielimääritys **Omat asetukset** -kohdassa on englanti ja että ympäristön versio on 24.0 tai uudempi. Varmista Copilotin ja tekoälyn ominaisuuksien määrittäminen -sivulla, että järjestelmänvalvoja on hyväksynyt tietojen siirron maantieteellisten alueiden välillä ja aktivoinut keskustelun. Varmista myös, että ympäristön lokalisointina ei ole Kanada.

Jos Keskustelu Copilotin avulla -ominaisuus ei ole vieläkään näkyvissä, on mahdollista, että Microsoft on vasta ottamassa ominaisuuden käyttöön alueella. Copilot otetaan ensin käyttöön yhdysvaltalaisille asiakkaille huhtikuussa 2024 ja seuraavien viikkojen aikana se otetaan käyttöön muissa maa- tai aluekohtaisissa lokalisoinneissa.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>Miksi Copilot näyttää keskusteluruudussa vain kolme tietuetta?

Kun pyydät Copilotia etsimään tietueita, tapa, jolla muotoilet kysymyksen, määrittää sen, miten Copilot tunnistaa ja käyttää sivuilla suodattimia löytääkseen etsimäsi. Jotta vastaukset pysyvät ytimekkäinä, keskusteluruudussa on enintään kolme tietueruutua, vaikka Copilot löytäisi asianmukaisempia tietueita.

## <a name="why-does-copilot-give-incorrect-answers-to-calculations"></a>Miksi Copilot antaa virheellisiä vastauksia laskelmiin?

Esiversion aikana Copilot-keskustelu voi auttaa tietueiden etsimisessä, käsitteiden selittämisessä ja Business Centralin tehtävien suorittamisessa. Muita käyttötapauksia ei tueta, kuten kentän laskeminen tietueiden kesken tai keskimääräisen kuukausisumman laskeminen. Toivomme voivamme lisätä Copilotiin tulevaisuudessa matematiikan peruskykyjä.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>Voinko käyttää puhetta kehotusten kirjoittamisen sijasta?

Voit keskustella Copilotin kanssa käyttämällä puhekirjoitusta sen sijaan, että kirjoittaisit sanojasi keskusteluruutuun. Puhekirjoituksessa käytetään online-puheentunnistusta, ja se on käytettävissä Windowsissa. Kun haluat käyttää ääntä, aktivoi keskusteluviestiruutu, käytä <kbd>Windows</kbd>+<kbd>H</kbd> -pikanäppäintä ja aloita puhuminen. Lisätietoja on kohdassa [puhekirjoituksen käyttäminen tietokoneella kirjoittamisen sijaan](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Seuraavat vaiheet

- [Keskustelu Copilotin avulla (esiversio)](chat-with-copilot.md)
