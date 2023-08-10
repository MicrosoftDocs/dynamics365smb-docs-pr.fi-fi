---
title: Tekoälypohjainen tuotteen markkinointiteksti (esiversio) Copilotilla - UKK
description: 'Vastauksia yleisiin kysymyksiin, jotka koskevat tekoälypohjaisia tekstiominaisuuksia Copilot-ohjelman avulla.'
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# <a name="ai-powered-item-marketing-text-preview-with-copilot-faq"></a>Tekoälypohjainen tuotteen markkinointiteksti (esiversio) Copilotilla - UKK

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Tässä artikkelissa on kysymyksiä ja vastauksia, jotka selittävät Copilot-ohjelman takana olevan tekoälyteknologian ja sen luoman tekstin tärkeät näkökohdat.

## [Yleiset](#tab/general)

### <a name="what-is-copilot"></a>Copilotin kuvaus

Copilot tarjoaa tekoälypohjaisia tekstiehdotuksia Business Centralin nimikkeille. Se on tarkoitettu käyttäjille, jotka kirjoittavat markkinointitekstiä nimikkeille, jotka auttavat heitä tuottamaan kiinnostavaa ja innostavaa sisältöä. Tärkeimpiin etuihin kuuluu:

- Vähentää tekstin kirjoittamiseen käytettyä aikaa, mikä voi nopeuttaa verkkokaupoissa myytävien tuotteiden markkinoille tuloa.
- Avaa luovuuden ja tarjoaa kiinnostavamman tuotekuvauksen.
- Parantaa tuoteryhmien markkinointimateriaalin yhdenmukaisuutta.

Käyttäjien tulisi ottaa tekoälyn luoma teksti huomioon ehdotuksena, jota täytyy tarkastella ja muokata tarkkuuden varmistamiseksi, ennen kuin se on julkisesti saatavilla.

### <a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central"></a>Miksei Copilot ole saatavilla markkinointitekstille Business Centralin nimikkeissä?

Jotta Copilot olisi saatavilla, seuraavien vaatimusten on täytyttävä:

- Business Centralin käytössä olevan kielen on oltava englanti. Mikä tahansa saatavilla olevista englannin kieliversioista toimii, kuten englanti (Yhdysvallat), englanti (Yhdistynyt kuningaskunta) tai englanti (Etelä-Afrikka).

  Valitse oikeasta yläkulmasta **Asetukset**-kuvake ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") > **Omat asetukset** > **Kieli**. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md#language).
- Sinun on käytettävä Business Central Online -versiota 22 tai uudempaa (jos olet olemassa oleva asiakas) tai kokeiluversiota.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Voit tarkistaa version valitsemalla oikeassa yläkulmassa olevan kysymysmerkin ja valitsemalla sitten **Ohjeet & tuki**. Etsi **vianetsintä**-kohdassa sovelluksen versiota. Saat lisätietoja oikean esiversion hankkimisesta siirtymällä [Business Central -esiversion käytön aloittaminen](ai-preview-getstarted.md).
- **Luo tekoälypohjaisia tuotekuvauksia Copilotin avulla** -ominaisuuden tulee olla käytössä.

   Lisätietoja on kohdassa [Luo tekoälypohjaiset tuotekuvaukset Copilot-ominaisuuden avulla tai poista se käytöstä](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- Ylläpitäjä on hyväksynyt käyttöehdot.

   Lisä tietoja on kohdassa [Kaikkien käyttäjien esiversio- ja tietosuojaehtojen hyväksyminen tai hylkääminen](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### <a name="is-copilot-available-for-preview-in-business-central-on-premises"></a>Onko Copilot saatavilla esiversiona paikalliselle Business Central -versiolle?

Ei, sitä ei tällä hetkellä tueta paikallisessa Business Centralissa.

### <a name="how-does-copilot-work-where-does-the-suggested-text-come-from"></a>Miten Copilot toimii, mistä ehdotettu teksti on peräisin?

Copilot käyttää [Microsoftin Azure OpenAI-palvelua](/azure/cognitive-services/openai/overview) käyttääkseen tehokkaita kielimalleja, jotka analysoivat ja luovat luonnollista kieltä. Nämä mallit on koulutettu laajoilla tekstikokonaisuuksilla. Tämän seurauksena Copilot voi luoda ehdotettuja, henkilökohtaisia vastauksia englanniksi. Ne perustuvat vähimmäismäärään syötettyä tietoa, kuten kohteen määritteitä, luokkaa tai kuvausta. 

### <a name="whats-the-quality-of-the-text-suggested-by-copilot"></a>Minkä laatuista Copilotin ehdottama teksti on?

Koska Copilotin taustalla oleva teknologia käyttää tekoälyä, joka on koulutettu monenlaisilla lähteillä, tuotettu sisältö ei aina ole tosiasiallista tai sopivaa. Joihinkin ehdotuksiin voi sisältyä jopa kyseenalaista tai sopimatonta sisältöä. On sinun vastuullasi tarkistaa ja muokata luotuja ehdotuksia varmistaaksesi, että se on oikea ja sopiva.

Lisätietoja sopimattomista ehdotuksista on kohdassa [Mitä loukkaaville ja haitallisille tekstiehdotuksille on tehty?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions)

### <a name="how-can-i-improve-the-suggestions-i-get-from-copilot"></a>Kuinka voin parantaa Copilotin ehdotuksia?

On olemassa muutamia asioita, joita voit tehdä, jotta saat kaiken irti Copilot-ehdotuksista:

- Lisää määritteitä nimikkeeseen, jos haluat mainostaa tiettyjä toimintoja ja ominaisuuksia, joita olet kiinnostunut.
- Muuta vaihtoehtoja äänensävyn ja painopisteen laadun osalta vastaamaan henkilökohtaisia mieltymyksiä.
- Paranna nimikkeen kuvausta.
- Varmista, että nimikkeelle on määritetty sopivin luokka.

Lisätietoja on ohjeaiheessa [Tekstiehdotusten parantaminen ja mukauttaminen](item-marketing-text.md#improve-and-tailor-text-suggestions).

### <a name="what-if-im-not-satisfied-with-the-generated-text"></a>Entä jos en ole tyytyväinen luotuun tekstiin?

Jos haluat auttaa meitä parantamaan tekstiä, valitse **Onko tämä hyvä ehdotus?** **Luo Copilotin avulla** -sivu, johon voit vastata peukalolla ylös (Tykkään) tai peukalolla alas (tarvitsee parannusta).

![Näyttää nimikkeen kortin, jossa on markkinointitekstiruutu](media/create-with-copilot-window-feedback.png)

### <a name="can-admins-disable-copilot-if-so-how"></a>Voiko ylläpitäjät poistaa Copilotin? Jos voivat, miten?

Business Central tarjoaa ylläpitäjille kaksi tapaa poistaa Copilotin esiversiossa:

- Älä hyväksy Azure OpenAI -tietosuojailmoitusta kaikille käyttäjille.

  tai

- Poista käytöstä **Luo tekoälypohjaiset tuotekuvaukset CoPilotilla** -ominaisuus **Ominaisuudenhallinta**-sivulla.

Lue lisää kohdasta [Nimikkeen tekoälypohjaisen markkinointitekstin määrittäminen (esiversio) Copilotin avulla järjestelmänvalvojana](enable-ai.md).

## [Oikeudenmukaisuus](#tab/fairness)

### <a name="does-copilot-work-with-languages-other-than-english"></a>Toimiiko Copilot muilla kielillä kuin englanniksi?

Tällä hetkellä Copilot tukee vain englantia. Epätarkkoja vastauksia saatetaan palauttaa, kun käyttäjät keskustelevat järjestelmän kanssa muilla kielillä kuin englannilla.

## [Ihmisen tarkistus](#tab/oversight)

### <a name="whats-done-about-abusive-and-harmful-text-suggestions"></a>Mitä loukkaaville ja haitallisille tekstiehdotuksille tehdään?

Azure OpenAI -palvelu tallentaa kehotteet ja täydennykset palvelusta valvomaan väärinkäyttöä sekä kehittämään ja parantamaan Azure OpenAI:n sisällön hallintajärjestelmien laatua. [Lisätietoja sisällönhallinnasta ja suodattamisesta.](/azure/cognitive-services/openai/concepts/content-filter)

Valtuutetut Microsoft-työntekijät voivat käyttää kehote- ja valmistumistietojasi, jotka ovat käynnistäneet automatisoidut järjestelmämme mahdollisten väärinkäytösten tutkintaa ja todentamista varten. Asiakkaille, jotka ovat ottaneet käyttöön Azure OpenAI -palvelun Euroopan unionissa, valtuutetut Microsoft-työntekijät sijaitsevat Euroopan unionissa. Näitä tietoja voidaan käyttää sisällönhallintajärjestelmien parantamiseen. Jos kyseessä on vahvistettu käytäntörikkomus, saatamme pyytää sinua ryhtymään välittömiin toimiin ongelman kunnostamisen ja väärinkäytösten estämiseksi. Ongelman laiminlyönti voi johtaa Azure OpenAI-resurssin käyttöoikeuden keskeyttämiseen tai lopettamiseen.

Lisätietoja on kohdassa [Azure OpenAI -palvelun tiedot, tietosuoja ja tietoturva](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### <a name="can-i-opt-out-of-the-logging-and-human-review-process"></a>Voinko kieltäytyä kirjaamisesta ja ihmisen suorittamasta tarkistusprosessista?

Osana Azure Open AI esiversio-ohjelman tarjoamista Microsoft käsittelee ja varastoi palveluun lähetettyjä asiakastietoja sekä tulostussisältöä tarkkaillakseen ja estääkseen palvelun väärinkäyttöä tai haitallisia käyttötarkoituksia tai tuotoksia; ja kehittääkseen, testatakseen ja parantaakseen valmiuksia, joiden avulla estetään palvelun väärinkäyttö ja/tai haitalliset tuotokset. 

Valtuutettu Microsoft-henkilöstö voi tarkastella tietoja, jotka ovat käynnistäneet automatisoidut järjestelmämme mahdollisten väärinkäytösten tutkimiseksi ja tarkistamiseksi, ja se voi käyttää rajoitettua satunnaisotantaa käsitteistä, joita automaattiset järjestelmämme eivät ole merkittyjä varmistaakseen, että järjestelmät toimivat oikein. Valtuutettu Microsoft-henkilöstö voi myös käyttää näitä tietoja parantaakseen järjestelmiämme, jotka valvovat palvelun väärinkäyttöä tai haitallisia käyttötarkoituksia tai tuotoksia. Lue lisää kohdasta [esiversion ehdot](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

## [Tietosuoja](#tab/privacy)

### <a name="what-data-does-the-capability-collect-how-is-the-data-used"></a>Mitä tietoja ominaisuus kerää? Miten tietoja käytetään?

Ominaisuus kerää vastauksesi **Onko tämä hyvä ehdotus?** -kysymykseen **Luo Copilotin avulla** -sivulla, johon voit vastata peukalolla ylös (Tykkään) tai peukalolla alas (tarvitsee parannusta).

Käytämme näitä tietoja ominaisuuden laadun arviointiin ja parantamiseen. Lisätietoja siitä, mitä tietoja kerätään on saatavilla [esiversioehdoissa](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Näyttää nimikkeen kortin, jossa on markkinointitekstiruutu](media/create-with-copilot-window-feedback.png)

---

## <a name="see-also"></a>Katso myös

[Tekoälypohjainen tuotteen markkinointiteksti Copilotin avulla -yleiskatsaus](ai-overview.md)  
[Nimikkeen tekoälypohjaisen markkinointitekstin määrittäminen Copilotin avulla järjestelmänvalvojana](enable-ai.md)  
[Luo markkinointiteksti nimikkeille käyttämällä Copilotia](item-marketing-text.md)  

