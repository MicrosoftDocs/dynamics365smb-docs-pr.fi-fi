---
title: Copilot- ja tekoälyominaisuuksien määrittäminen
description: 'Tässä artikkelissa kerrotaan, miten Copilot otetaan käyttöön ympäristössä.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 02/27/2024
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# Copilot- ja tekoälyominaisuuksien määrittäminen 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Tässä artikkelissa kerrotaan, miten hallita Copilotia ja muita tekoälyominaisuuksia Business Centralissa. Tämän tehtävän suorittaa järjestelmänvalvoja. Copilot on järjestelmäominaisuus ja olennainen osa Business Centralia. Kuten useimmissa järjestelmäominaisuuksissa, et myönnä pääsyä yksittäisille käyttäjille etkä voi kytkeä Copilotia päälle tai pois päältä. Copilot tarjoaa kuitenkin tietojen hallintaa ja mahdollisuuden poistaa yksittäiset Copilot- ja tekoälyominaisuudet käytöstä jokaisessa ympäristössä. Tekoälyominaisuuksille on eri tasoisia pääsynhallintaominaisuuksia ominaisuudesta riippuen:

- Tietojen siirtojen salliminen maantieteellisten alueiden välillä.

  Tämä tehtävä on pakollinen vain, jos Business Central -ympäristösi on eri maantieteellisellä alueella kuin sen käyttämä Azure OpenAI Service. [Lisätietoja](#allow-data-movement-across-geographies)

- Aktivoi ominaisuus **Copilotin ja tekoälyn ominaisuudet** -sivulla. [Lisätietoja](#activate-features)

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Jos jokin näistä vaatimuksista ei täyty, ominaisuus ei ole käytettävissä.-->

## Vaatimukset

- Käytössä on Business Central Online <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Sinulla on Business Centralin järjestelmänvalvojan tai pääkäyttäjän käyttöoikeudet.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## Salli tietojen siirto eri maantieteellisillä alueilla

Tämä tehtävä on käytössä vain, jos **Salli tiedonsiirto** -kytkin tulee näkyviin **Copilot ja tekoälytoiminnot** -sivun yläosan lähelle. Jos linkki **Miten ohjaan avustajatietojani?** näytetään  **Salli tietojen liikkuminen** -kytkimen sijaan, ohita tämä vaihe.

![Näyttää kuvakaappauksen Copilot ja tekoälyominaisuudet -sivun Salli tietojen liikkuminen -kytkimestä.](media/allow-data-movement-v2.png)

**Salli tiedonsiirto** -kytkimellä ilmaistaan, että Business Central -ympäristösi sijainti eli &mdash;maantieteellinen sijainti, jossa tietoja käsitellään ja tallennetaan&mdash;, ei ole sama kuin Copilotin käyttämä Azure OpenAI Servicen maantieteellinen sijainti. Jos haluat ottaa Copilotin käyttöön, tietojen siirto maantieteellisten sijaintien välillä on sallittu. Lisätietoja tietojen siirtämisestä on kohdassa [Copilot-tietojen siirtäminen maantieteellisillä alueilla](ai-copilot-data-movement.md). 

Voit sallia tietojen siirron maantieteellisen alueen ulkopuolelle noudattamalla seuraavia vaiheita:

1. Etsi ja avaa Business Centralissa **Copilot ja tekoälyominaisuudet** -sivu.
1. Ota **Salli tiedonsiirto** -kytkin käyttöön.

   **Salli tiedonsiirto** -kytkin on oletusarvoisesti käytössä Länsi-Euroopan ja Pohjois-Euroopan Azure-ympäristöissä.

Voit kieltäytyä tiedonsiirrosta kytkemällä **Salli tietojen siirto** -kytkimen pois päältä. Sen jälkeen, kun Azure OpenAI Service tulee saataville Business Central -ympäristössäsi, ympäristösi liitetään siihen automaattisesti, eikä kytkintä enää ole saatavilla.

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

## Aktivoi ominaisuuksia

Kaikki Copilot- ja tekoälyominaisuudet ovat oletusarvoisesti aktiivisia, kun ne ovat saatavana esiversiona tai ne tulevat yleisesti saataville. **Copilotin ja tekoälyn ominaisuudet** -sivulla voit poistaa kaikki ominaisuudet käytöstä kaikilta käyttäjiltä tai ottaa ne taas käyttöön.

1. Etsi ja avaa Business Centralissa **Copilot ja tekoälyominaisuudet** -sivu.

1. Sivulla näkyvät kaikki käytettävissä olevat Copilotiin ja tekoälyyn liittyvät toiminnot sekä niiden nykyinen tila, joka voi olla aktiivinen tai passiivinen. Toiminnot on jaettu kahteen osaan, joista yksi osa sisältää esikatselutoiminnot ja toinen yleensä käytettävissä olevat toiminnot. 

   [![Näyttää Business Central -roolikeskuksen ja Copilot-ohjelman tarkistusluettelon](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Voit ottaa ominaisuuden käyttöön valitsemalla sen luettelosta ja valitsemalla **Aktivoi**-toiminnon.
   - Voit poistaa ominaisuuden käytöstä valitsemalla sen luettelosta ja valitsemalla **Deaktivoi**-toiminnon. 

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## Käyttäjien käyttöoikeuksien myöntäminen

Copilot- ja tekoälyominaisuudet voivat tarjota toimintoja, jotka on tarkoitettu kaikille organisaation käyttäjille tai tietyille käyttäjärooleille. Useimmat Copilot- ja tekoälyominaisuudet tarjoavat pääsynhallinnan Business Centralin käyttöoikeuksien hallintajärjestelmän lupien ja käyttöoikeusjoukkojen avulla. [Lue lisää käyttöoikeuksista ja käyttöoikeusjoukoista](ui-define-granular-permissions.md).

Seuraavassa taulukossa on luettelo käyttöoikeuksista, joita tarvitaan Business Centralin Copilotin ominaisuuksien käyttämiseen.

|Copilot-ominaisuudet|Vaaditut käyttöoikeudet|
|-|-|
|Analyysiavustaja|**DATA ANALYSIS - EEC** -käyttöoikeusjoukko tai järjestelmäobjektin 9640 **Salli tietojen analysointitila** käyttöoikeuden suorittaminen. Näitä samoja käyttöoikeuksia tarvitaan analyysitilan käyttämiseen.|
|Pankkitilin täsmäytyksen avustaja|Käyttöoikeus sivulla 7250 **Pankkitilin täsmäytyksen tekoälyyn perustuva ehdotus** ja sivu 7252 **Siirto KP-tilin tekoälyehdotukseen**.|
|Keskustelu |Mikään käyttöoikeus tai käyttöoikeusjoukko ei hallita keskustelun käyttöoikeutta käyttäjäkohtaisesti. Jos keskustelu on aktivoitu, se on kaikkien käyttäjien käytettävissä.|
|Markkinointitekstiehdotukset |Käyttöoikeus sivulla 5836 **Copilotin markkinointiteksti**|

Tietyn muun kuin Microsoftin avustajan ja tekoälyominaisuuksien käyttöoikeuden myöntämisestä tai kieltämisestä on lisätietoja ohjeissa tai kyseisen ominaisuuden julkaisijalla. Tällä tavoin saadaan selville, mitä käyttöoikeuksia tarvitaan.

## Seuraavat vaiheet

Kun olet ottanut ominaisuudet käyttöön ja antanut niihin suostumuksesi, voit kokeilla niitä. Mene kohtaan:

- [Markkinointitekstin lisääminen nimikkeille](item-marketing-text.md)
- [Tietojen analysoiminen analyysitilassa Copilotin avulla](analysis-assist.md)  
- [Keskustelu Copilotin avulla](chat-with-copilot.md)
- [Täsmäyttäminen pankkitilien täsmäytysavustajan avulla](bank-reconciliation-with-copilot.md)

## Katso myös

[Copilot- ja tekoälyominaisuuksien vianmääritys](ai-copilot-troubleshooting.md)  
[Analyysiavustajan usein kysytyt kysymykset](faqs-analysis-assist.md)  
[Pankkitilin täsmäytyksen avustajan usein kysytyt kysymykset](faqs-bank-reconciliation.md)  
[Usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla](faqs-chat-with-copilot.md)  
[Markkinointitekstiehdotusten usein kysytyt kysymykset](faqs-marketing-text.md)  
[Markkinointitekstiehdotusten yleiskatsaus](ai-overview.md)  