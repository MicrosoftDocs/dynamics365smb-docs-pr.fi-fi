---
title: Copilot- ja tekoälyominaisuuksien määrittäminen
description: 'Tässä artikkelissa kerrotaan, miten Copilot otetaan käyttöön ympäristössä.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/28/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: '7771,7772_Primary,7775_Primary'
---

# <a name="configure-copilot-and-ai-capabilities"></a>Copilot- ja tekoälyominaisuuksien määrittäminen

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Tässä artikkelissa kerrotaan, miten hallita Microsoft Copilotia ja muita tekoälyominaisuuksia Dynamics 365 Business Centralissa. Järjestelmänvalvojan on suoritettava nämä tehtävät.

Copilot on järjestelmäominaisuus ja olennainen osa Business Centralia. Kuten useimmissa järjestelmäominaisuuksissa, et myönnä pääsyä yksittäisille käyttäjille etkä voi kytkeä Copilotia päälle tai pois päältä. Copilot tarjoaa kuitenkin tietojen hallintaa ja mahdollisuuden poistaa yksittäiset Copilot- ja tekoälyominaisuudet käytöstä jokaisessa ympäristössä. Tekoälyominaisuuksille on eri tasoisia pääsynhallintaominaisuuksia ominaisuudesta riippuen:

- Tietojen siirtojen salliminen maantieteellisten alueiden välillä.

    Tämä tehtävä on pakollinen vain, jos Business Central -ympäristösi on eri maantieteellisellä alueella kuin sen käyttämä Azure OpenAI Service. [Lisätietoja tästä tehtävästä](#allow-data-movement-across-geographies).

- Aktivoi ominaisuus **Copilotin ja tekoälyn ominaisuudet** -sivulla. [Lisätietoja tästä tehtävästä](#activate-features).

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Jos jokin näistä vaatimuksista ei täyty, ominaisuus ei ole käytettävissä.

## <a name="prerequisites"></a>Vaatimukset

- Käytössä on Business Central Online.
- Olet Business Centralin [järjestelmänvalvoja](#requirements-for-being-an-administrator).

## <a name="allow-data-movement-across-geographies"></a>Salli tietojen siirto eri maantieteellisillä alueilla

Tämä tehtävä on käytössä vain, jos **Salli tiedonsiirto** -valinta tulee näkyviin **Copilot ja tekoälytoiminnot** -sivun yläosan lähelle. Jos **Miten ohjaan avustajatietojani?** -linkki näytetään **Salli tietojen liikkuminen** -valinnan sijaan, ohita tämä tehtävä.

![Näyttökuva, joka näyttää Copilot ja tekoälyominaisuudet -sivun Salli tietojen liikkuminen -vaihtoehdon.](media/allow-data-movement-v2.png)

**Salli tietojen siirto** -vaihtoehdon olemassaolo osoittaa, että Business Central -ympäristösi sijainti (eli maantieteellinen sijainti, jossa tietoja käsitellään ja tallennetaan) eroaa Copilotin käyttämästä Azure OpenAI -palvelun maantieteellisestä sijainnista. Ottaaksesi Copilotin käyttöön, sinun on sallittava tietojen siirto maantieteellisten sijaintien välillä. [Lisätietoja tietojen siirrosta](ai-copilot-data-movement.md).

Voit sallia tietojen siirron maantieteellisen alueen ulkopuolelle seuraamalla näitä vaiheita:

1. Etsi ja avaa Business Centralissa **Copilot ja tekoälyominaisuudet** -sivu.
1. Ota **Salli tiedonsiirto** -vaihtoehto käyttöön.

    > [!NOTE]
    > Länsi-Euroopan ja Pohjois-Euroopan Azure-alueiden ympäristöissä **Salli tiedonsiirto** -vaihtoehto on oletusarvoisesti käytössä.

Voit kieltäytyä tiedonsiirrosta kytkemällä **Salli tietojen siirto** -vaihtoehdon pois päältä.

Sen jälkeen, kun Azure OpenAI Service tulee saataville Business Central -ympäristössäsi, ympäristösi liitetään siihen automaattisesti. Siinä vaiheessa **Salli tietojen siirto** -vaihtoehto ei enää näy **Copilot ja tekoälyominaisuudet** -sivulla.

<!-- Don't review
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->

## <a name="activate-features"></a>Aktivoi ominaisuuksia

Kaikki Copilot- ja tekoälyominaisuudet ovat oletusarvoisesti aktiivisia, kun ne ovat saatavilla esiversiona tai ne tulevat yleisesti saataville. **Copilotin ja tekoälyn ominaisuudet** -sivulla voit poistaa kaikki ominaisuudet käytöstä kaikilta käyttäjiltä tai ottaa ne taas käyttöön.

1. Etsi ja avaa Business Centralissa **Copilot ja tekoälyominaisuudet** -sivu.
1. Sivulla näkyvät kaikki käytettävissä olevat Copilotiin ja tekoälyyn liittyvät toiminnot sekä niiden nykyinen tila. (Tila voi olla joko *Aktiivinen* tai *Passiivinen*.) Toiminnot on jaettu kahteen osaan, joista yksi osa sisältää esikatselutoiminnot ja toinen yleensä käytettävissä olevat toiminnot.

    - Voit ottaa ominaisuuden käyttöön valitsemalla sen luettelosta ja valitsemalla **Aktivoi**.
    - Voit poistaa ominaisuuden käytöstä valitsemalla sen luettelosta ja valitsemalla **Deaktivoi**.

    [![Näyttökuva, jossa näkyvät Copilotin ja tekoälyn ominaisuudet -sivulla olevien ominaisuusluetteloiden Aktivoi- ja Deaktivoi-painikkeet.](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## <a name="enable-feature-in-feature-management"></a>Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## <a name="granting-user-access"></a>Käyttäjien käyttöoikeuksien myöntäminen

Copilot- ja tekoälyominaisuudet voivat tarjota toimintoja, jotka on tarkoitettu kaikille organisaation käyttäjille tai tietyille käyttäjärooleille. Useimmat Copilot- ja tekoälyominaisuudet tarjoavat pääsynhallinnan Business Centralin käyttöoikeuksien hallintajärjestelmän lupien ja käyttöoikeusjoukkojen avulla. [Lue lisää käyttöoikeuksista ja käyttöoikeusjoukoista](ui-define-granular-permissions.md).

Seuraavassa taulukossa on luettelo käyttöoikeuksista, joita tarvitaan Business Centralin Copilotin ominaisuuksien käyttämiseen.

| Copilot-ominaisuus | Vaaditut käyttöoikeudet |
|---|---|
| Analyysiavustaja | **DATA ANALYSIS - EEC** -käyttöoikeusjoukko tai järjestelmäobjektin 9640 **Salli tietojen analysointitila** käyttöoikeuden suorittaminen. Näitä samoja käyttöoikeuksia vaaditaan analyysitilan käyttämiseen. |
| Pankkitilin täsmäytyksen avustaja | Käyttöoikeus sivulla 7250 **Pankkitilin täsmäytyksen tekoälyyn perustuva ehdotus** ja sivu 7252 **Siirto KP-tilin tekoälyehdotukseen**. |
| Keskustelu | Mikään käyttöoikeus tai käyttöoikeusjoukko ei hallita keskustelun käyttöoikeutta käyttäjäkohtaisesti. Jos keskustelu on aktivoitu, se on kaikkien käyttäjien käytettävissä. |
| Liitä sähköisiä asiakirjoja | Käyttöoikeus sivulla 6166 **Sähköisen asiak. PO:n Copilotin omin.** |
| Markkinointitekstiehdotukset | Käyttöoikeus sivulla 5836 **Copilotin markkinointiteksti** |
| Myyntirivin ehdotukset | Käyttöoikeus sivulle 7275 **Myyntirivin tekoälyehdotukset** ja sivu 7276 **Myyntirivin tekoälyehdotusten alirivi** |

Tietyn muun kuin Microsoftin avustajan ja tekoälyominaisuuksien käyttöoikeuden myöntämisestä tai kieltämisestä on lisätietoja ohjeissa tai kyseisen ominaisuuden julkaisijalla. Tällä tavoin saadaan selville, mitä käyttöoikeuksia tarvitaan.

## <a name="requirements-for-being-an-administrator"></a>Järjestelmänvalvojan vaatimukset

Sinulla on oltava joko SUPER-käyttöoikeudet omassa Business Central -käyttäjätilissä tai jokin seuraavista Business Central -käyttöoikeuksista:

- Delegoitu järjestelmänvalvoja - Kumppani
- Delegoitu helpdesk-agentti - Kumppani
- Sisäinen järjestelmänvalvoja
- Sisäinen BC-järjestelmänvalvoja
- Dynamics 365 -järjestelmänvalvoja

Business Central ei vielä tarjoa rakeisia objektitason käyttöoikeuksia, joten vain tietyt järjestelmänvalvojat voivat määrittää Copilotin.

## <a name="next-steps"></a>Seuraavat vaiheet

Kun olet ottanut ominaisuudet käyttöön ja antanut niihin suostumuksesi, voit kokeilla niitä. Siirry seuraaviin artikkeleihin:

- [Lisää markkinointiteksti nimikkeille Copilotin avulla](item-marketing-text.md)
- [Luetteloiden tietojen analysointi Copilotin avulla](analysis-assist.md)
- [Keskustelu Copilotin avulla](chat-with-copilot.md)
- [Sähköisten asiakirjojen yhdistäminen ostotilausriveille Copilotin avulla](map-edocuments-with-copilot.md)
- [Pankkitilien täsmäyttäminen Copilotin avulla](bank-reconciliation-with-copilot.md)
- [Rivien ehdottaminen myyntitilaukseen Copilotin avulla](sales-suggest-sales-lines-with-copilot.md)

## <a name="see-also"></a>Katso myös

[Copilot- ja tekoälyominaisuuksien vianmääritys](ai-copilot-troubleshooting.md)  
[Analyysiavustajan usein kysytyt kysymykset](faqs-analysis-assist.md)  
[Pankkitilin täsmäytyksen avustajan usein kysytyt kysymykset](faqs-bank-reconciliation.md)  
[Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla](faqs-chat-with-copilot.md)  
[Usein kysyttyjä kysymyksiä sähköisten asiakirjojen yhdistämisestä ostotilauksiin](faqs-map-edocuments.md)  
[Markkinointitekstiehdotusten usein kysytyt kysymykset](faqs-marketing-text.md)  
[Myyntirivin ehdotusten UKK](faq-sales-suggest-sales-lines-with-copilot.md)  
[Markkinointitekstiehdotusten yleiskatsaus](ai-overview.md)
