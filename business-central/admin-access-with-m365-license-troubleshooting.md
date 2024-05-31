---
title: Microsoft 365 -käyttöoikeuksien käytön vianmääritys
description: 'Tietoja siitä, miten voit korjata Business Centralin käytön ongelmat vain Microsoft 365 -käyttöoikeuden avulla.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.service: dynamics-365-business-central
---

# Microsoft 365 -käyttöoikeuksien käytön vianmääritys

## "Tämä sivu käyttää niihin liittyvien taulukoiden tietoja, joihin sinulla ei ole käyttöoikeuksia" -virheilmoitus

### Oireet

Kun käytät Teamsin tietueita, näyttöön tulee välilehdessä tai kortissa virhesanoma, joka muistuttaa seuraavia tietoja:

"Tämä sivu käyttää niihin liittyvien taulukoiden tietoja, joihin sinulla ei ole käyttöoikeuksia. Jos haluat käsitellä kaikkia tämän sivun ominaisuuksia, ota yhteyttä järjestelmänvalvojaan. "

### Syy

Sinulta todennäköisesti puuttuu objektien käyttöoikeuksia niiden taulujen osalta, joihin kyseinen sivu tai tietueiden linkit liittyvät.

## Microsoft 365 on otettu käyttöön, mutta käyttäjät saavat käyttöoikeusvirheen

### Oireet

Microsoft 365 on otettu käyttöön Business Central -hallintakeskuksessa, mutta käyttäjät saavat käyttöoikeusvirheen, kun he käyttävät mitä tahansa tietueita.

### Syy

Jos otat käyttöoikeuden käyttöön Business Central -hallintakeskuksessa, mutta et määritä käyttöoikeuksia **käyttöoikeuksien määritys** -sivulla, kuka tahansa, joka yrittää käyttää Business Central -tietueita Teamsissa, saa käyttäjä tietueensa valmiiksi ilman oikeuksia mihinkään objekteihin. Business Central on suunniteltu suojatuksi: Järjestelmänvalvojien on ensin määritettävä, mitä tietoja voidaan käyttää Teamsissa. 

### Ratkaisu

Käyttöoikeusasetukset-sivun käyttöoikeuksien mukauttaminen vaikuttaa vain uusiin luotuihin käyttäjiin. Sinun täytyy myös liittää puuttuvat käyttöoikeudet käyttäjille, jotka on jo luotu käyttäjäluettelo-sivulla. 

## Jaoit linkin Teamsiin, mutta käyttäjät saavat viestin, että he voivat vain tarkastella tietoja

### Oireet

Kun jaat linkin Teamsissa Business Central -käyttäjänä, toiset saavat virheilmoituksen "Kun käytät Business Centralin Microsoft 365 -käyttöoikeutta, voit tarkastella tietoja vain Microsoft Teamsissa ".

### Syy

Kun Business Central -linkki jaetaan Teams-keskusteluun tai -kanaviin, linkin selaaminen siirtyy aina pois Microsoft Teamsista, jolloin tiedot eivät enää ole Microsoft 365 -käyttöoikeuden käyttäjän saatavilla.

### Ratkaisu

Kun jaat sivuja tai tietueita, voit joko sisällyttää linkin esiversion korttina tai jakaa tiedot välilehdessä keskusteluun tai kanavaan.

## Kortti jaetusta linkistä on minimaalinen eikä sisällä Tiedot-painiketta

### Oireet 

Kun Microsoft 365:n käyttöoikeuden haltija ilman Business Central -käyttöoikeutta jakaa Business Central -linkin Teamsiin, se laajenee automaattisesti kortille, jolla ei ole hyödyllistä tietoa, ja siinä näkyy vain Business Central ilman **Tiedot**-painiketta.

### Syy

Käyttäjät, joilla on Microsoft 365 -käyttöoikeus mutta ei Business Central -käyttöoikeutta, eivät saa jakaa linkkejä kortteina. Jos käyttäjällä on asennettuna Business Central -sovellus Teamsille ja se liittää linkin luontialueeseen, näyttöön tulee vain vähimmäiskortti. 

## Katso myös

[Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md#minimum-requirements)  
[Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla](admin-access-with-m365-license-setup.md)  
[Business Central- ja Microsoft Teams -integrointi](across-teams-overview.md)
[Business Centralin tietueiden ja sivulinkkien jakaminen Microsoft Teamsissa](across-working-with-teams.md)  
[Teams-integroinnin vianmääritys](admin-teams-troubleshooting.md)  