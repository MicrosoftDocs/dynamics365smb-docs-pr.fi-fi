---
title: Microsoft 365 -käyttöoikeuksien käytön vianmääritys
description: 'Tietoja siitä, miten voit korjata Business Centralin käytön ongelmat vain Microsoft 365 -käyttöoikeuden avulla.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Microsoft 365 -käyttöoikeuksien käytön vianmääritys

## Oireet

Kun käytät Teamsin tietueita, näyttöön tulee välilehdessä tai kortissa virhesanoma, joka muistuttaa seuraavia tietoja:

"Tämä sivu käyttää niihin liittyvien taulukoiden tietoja, joihin sinulla ei ole käyttöoikeuksia. Jos haluat käsitellä kaikkia tämän sivun ominaisuuksia, ota yhteyttä järjestelmänvalvojaan. "

## Syy

Sinulta todennäköisesti puuttuu objektien käyttöoikeuksia niiden taulujen osalta, joihin kyseinen sivu tai tietueiden linkit liittyvät.

## Oireet

Käyttö on otettu käyttöön, mutta käyttäjät saavat käyttöoikeusvirheen, kun he käyttävät mitä tahansa tietueita.

## Syy

Jos otat käyttöoikeuden käyttöön Business Central -hallintakeskuksessa, mutta et määritä käyttöoikeuksia käyttöoikeuksien määrityssivulla, kuka tahansa, joka yrittää käyttää Business Central -tietueita Teamsissa, saa käyttäjä tietueensa valmiiksi ilman oikeuksia mihinkään objekteihin. Business Central on suunniteltu suojatuksi: Järjestelmänvalvojien on ensin määritettävä, mitä tietoja voidaan käyttää Teamsissa. 

## Ratkaisu

Käyttöoikeusasetukset-sivun käyttöoikeuksien mukauttaminen vaikuttaa vain uusiin luotuihin käyttäjiin. Sinun täytyy myös liittää puuttuvat käyttöoikeudet käyttäjille, jotka on jo luotu käyttäjäluettelo-sivulla. 

## Oireet

Kun jaan linkin Teamsissa, toiset saavat virheilmoituksen "Kun käytät Business Centralin Microsoft 365 -käyttöoikeutta, voit tarkastella tietoja vain Microsoft Teamsissa ".

## Syy

Kun Business Central -linkki jaetaan Teams-keskusteluun tai -kanaviin, linkin selaaminen siirtyy aina pois Microsoft Teamsista, jolloin tiedot eivät enää ole Microsoft 365 -käyttöoikeuden käyttäjän saatavilla.

## Ratkaisu

Kun jaat sivuja tai tietueita, voit joko sisällyttää linkin esiversion korttina tai jakaa tiedot välilehdessä keskusteluun tai kanavaan.

## Katso myös

[Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md#minimum-requirements)  
[Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla](admin-access-with-m365-license-setup.md)  
[Business Central- ja Microsoft Teams -integrointi](across-teams-overview.md)
[Business Centralin tietueiden ja sivulinkkien jakaminen Microsoft Teamsissa](across-working-with-teams.md)  
[Teams-integroinnin vianmääritys](admin-teams-troubleshooting.md)  