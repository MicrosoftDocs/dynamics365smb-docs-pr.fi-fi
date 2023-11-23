---
title: Copilot- ja tekoälyominaisuuksien määrittäminen
description: 'Tässä artikkelissa kerrotaan, miten Copilot otetaan käyttöön ympäristössä.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
---

# Copilotin ja tekoälyn ominaisuuksien määrittäminen 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Tässä artikkelissa kerrotaan, miten voit hallita käyttäjien pääsyä Copilotiin ja muihin tekoälyominaisuuksiin Business Centralissa. Tämän tehtävän suorittaa järjestelmänvalvoja. Copilot- ja tekoälyominaisuuksien käytönvalvontatasoja on kolme sen mukaan, mikä ominaisuus on:

- Azure OpenAI [esiversio](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/)- ja [tietosuoja](https://go.microsoft.com/fwlink/?LinkId=521839)-ehtojen hyväksyminen tai hylkääminen.

   Tämä suostumus on pakollinen, jotta Copilotin tai tekoälyn ominaisuudet toimivat käyttäjille. Suostumus on yleinen kaikille käyttäjille, ja se koskee kaikkia Copilotin ja tekoälyn ominaisuuksia. [Lisätietoja](#consent-to-preview-and-privacy-terms)

- Tiedonsiirtojen salliminen maantieteellisillä alueilla

  Tämä tehtävä on pakollinen vain, jos Business Central -ympäristösi on eri maantieteellisellä alueella kuin sen käyttämä Azure OpenAI Service. [Lisätietoja](#allow-data-movement-across-geographies)

- Ota tietty ominaisuus käyttöön, jos **ominaisuuden hallinta** on yhä käytössä.

  Vuoden 2023 julkaisuaalto 2:ssa sekä markkinointitekstiehdotukset että pankkitilin täsmäytysapuominaisuudet sisältyvät kohtaan **Ominaisuuksien hallinta**. Markkinointitekstiehdotukset ovat kuitenkin oletusarvoisesti käytössä. [Lisätietoja](#enable-feature-in-feature-management)

- Aktivoi ominaisuus **Copilotin ja tekoälyn ominaisuudet** -sivulla. [Lisätietoja](#activate-features)

Jos jokin näistä vaatimuksista ei täyty, ominaisuus ei ole käytettävissä.

## Vaatimukset

- Käytät Business Central online -versiota 23.1 tai sitä uudempaa. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Sinulla on Business Centralin järjestelmänvalvojan tai pääkäyttäjän käyttöoikeudet.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## Suostumus esiversioon ja tietosuojaehtoihin

Hyväksy [Esiversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) ehdot ja [Microsoftin tietosuojalauseke](https://go.microsoft.com/fwlink/?LinkId=521839) organisaation puolesta. Toisin kuin muiden toimintojen ja palveluiden tietosuojailmoitukset, vain järjestelmänvalvojat voivat antaa suostumuksensa Azure OpenAI:n käyttöön organisaation puolesta. Käyttäjät eivät voi päättää itse.   

1. Etsi ja avaa Business Centralissa **tietosuojatietojen tila** -sivu.
2. Valitse **integrointinimi**-sarakkeessa **Azure OpenAI**ja lue sitten sinulle esitettävät käyttöehdot.
3. Valitse **Azure OpenAI** -rivillä **hyväksy kaikille** -valintaruutu, jos haluat hyväksyä tai **hylätä kaikille** valintaruudun valinnan.

## Ota ominaisuus käyttöön Ominaisuuksien hallinnassa

**Ominaisuuksien hallinnan** avulla voit ottaa käyttöön tai poistaa käytöstä esiversiossa olevia toimintoja, kuten pankkitilien täsmäytyksen, sekä joitain yleisesti saatavilla olevia ominaisuuksia, kuten nimikemarkkinointiehdotuksia. [Lue lisää Ominaisuuksien hallinnasta](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. Etsi ja avaa **toimintojen hallinta** -sivu Business Centralissa.
2. Voit ottaa ominaisuuden käyttöön määrittämällä **käytössä** -sarakkeen **Kaikille käyttäjille**. Voit poistaa ominaisuuden käytöstä määrittämällä **käytössä**-sarakkeen **Ei kenellekään**. Käytä seuraavaa taulukkoa apuna, kun määrität sen kytkimen, joka koskee Copilotia ja AO-ominaisuutta, jotka haluat ottaa käyttöön:

   - **Ominaisuuden esiversio: Pankkitilin täsmäytys Copilotin avulla** liittyy pankkitilin täsmäytysavustoimintoon.
   - **Ominaisuuden esiversio: Luo tekoälypohjaiset tuotekuvaukset Copilotin avulla** liittyy markkinointitekstien ehdotustoimintoon.

   Saat lisätietoja ominaisuuksien hallinnasta yleisesti siirtymällä [Ominaisuuksien hallintaan](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Salli tietojen siirto eri maantieteellisillä alueilla

Tämä tehtävä on käytössä vain, jos **Salli tiedonsiirto** -kytkin tulee näkyviin **Copilot ja tekoälytoiminnot** -sivun yläosan lähelle. **Salli tiedonsiirto** -kytkimellä ilmaistaan, että Business Central -ympäristösi sijainti eli maantieteellinen sijainti, jossa tietoja käsitellään ja tallennetaan, ei ole sama kuin Copilotin käyttämä Azure OpenAI Servicen maantieteellinen sijainti. Jos haluat ottaa Copilotin käyttöön, tietojen siirto maantieteellisten sijaintien välillä on sallittu. Lisätietoja tietojen siirtämisestä on kohdassa [Copilot-tietojen siirtäminen maantieteellisillä alueilla](ai-copilot-data-movement.md). 

Voit sallia tietojen siirron maantieteellisen alueen ulkopuolelle noudattamalla seuraavia vaiheita:

1. Etsi ja avaa Business Centralissa **Copilot ja tekoälyominaisuudet** -sivu.
1. Ota **Salli tiedonsiirto** -kytkin käyttöön.

   ![![Vaihtoehtoinen teksti](allow-data-movement.png)](allow-data-movement.png)

Voit kieltäytyä kytkemällä **Salli tietojen siirto** -kytkimen pois päältä. Sen jälkeen, kun Azure OpenAI Service tulee saataville Business Central -ympäristössäsi, ympäristösi liitetään siihen automaattisesti, eikä kytkintä enää ole saatavilla. 


<!--
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

**Copilotin ja tekoälyn ominaisuudet** -sivulla voit ottaa kaikki ominaisuudet käyttöön kaikille käyttäjille tai poistaa ne käytöstä.

1. Etsi ja avaa Business Centralissa **Copilot ja tekoälyominaisuudet** -sivu.

1. Sivulla näkyvät kaikki käytettävissä olevat Copilotiin ja tekoälyyn liittyvät toiminnot sekä niiden nykyinen tila, joka voi olla aktiivinen tai passiivinen. Toiminnot on jaettu kahteen osaan, joista yksi osa sisältää esikatselutoiminnot ja toinen yleensä käytettävissä olevat toiminnot. 

   [![Näyttää Business Central -roolikeskuksen ja Copilot-ohjelman tarkistusluettelon](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Voit ottaa ominaisuuden käyttöön valitsemalla sen luettelosta ja valitsemalla valintanauhassa **Aktivoi**.
   - Voit poistaa ominaisuuden käytöstä valitsemalla sen luettelosta ja valitsemalla valintanauhassa **Deaktivoi**. 


## Seuraavat vaiheet

Kun olet ottanut ominaisuudet käyttöön ja antanut niihin suostumuksesi, voit kokeilla niitä. Mene kohtaan:

- [Markkinointitekstin lisääminen nimikkeille](item-marketing-text.md) 
- [Täsmäyttäminen pankkitilien täsmäytysavustajan avulla](bank-reconciliation-with-copilot.md) 

## Katso myös

[Markkinointitekstiehdotusten yleiskatsaus](ai-overview.md)   
[Markkinointitekstiehdotusten UKK](faqs-marketing-text.md)  
