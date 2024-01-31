---
title: Copilot- ja tekoälyominaisuuksien vianmääritys
description: 'Opi korjaamaan yleisiä ongelmia, joita saatat kohdata käyttäessäsi Copilot- ja tekoälyominaisuuksia Business Centralissa.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 11/15/2023
ms.custom: bap-template
---
# Copilot- ja tekoälyominaisuuksien vianmääritys

Copilot on tekoälyllä toimiva Business Centralin toiminto, joka auttaa erilaisissa tehtävissä, kuten markkinointitekstien laatimisessa ja pankkitilien täsmäytyksessä. Jos sinulla on ongelmia Copilotin tai muiden tekoälyominaisuuksien kanssa, tämä artikkeli voi auttaa sinua tunnistamaan ja korjaamaan yleisiä ongelmia.

## Copilot ei näy sivuilla

Jos Copilot-toiminto, kuten **Tee luonnos Copilotin avulla** -toiminto markkinointitekstiehdotuksille tai **Sovita Copilotin avulla** -toiminto pankkitilin täsmäytysavulle ei näy sivulla odotetulla tavalla, tarkista seuraavat asiat:

- Jos ominaisuutta ohjataan Ominaisuuksien hallinnassa, varmista, että se on käytössä. [Lue lisää Ominaisuuksien hallinnasta](admin-feature-management.md).

- Varmista, että toimintoa ei ole piilotettu mukautuksen vuoksi. [Lisätietoja mukautuksen käyttämisestä](ui-personalization-user.md).

## Copilot näkyy sivuilla, mutta saat virheilmoituksen, että sitä ei ole aktivoitu

Kun yrität käyttää Copilotia ja saat virheilmoituksen, kuten **Copilotia ei ole aktivoitu \[ominaisuuden\] osalta**, on tarkistettava pari asiaa:

- Varmista ensin, että ominaisuus on aktivoitu **Copilotin ja tekoälyn ominaisuudet** -sivulla. [Lisätietoja Copilotin ja tekoälyn ominaisuuksien aktivoinnista](enable-ai.md#activate-features). 
- Varmista seuraavaksi, että Azuren OpenAI -integraation tietosuojailmoitus ei ole asetettu arvoon **Eri mieltä kaikkien kanssa**. Jos on, muuta se muotoon **Samaa mieltä kaikkien kanssa**. [Lue lisää tietosuojailmoituksista](privacy-notices-status.md).

## Katso myös

[Copilotin ja tekoälyn ominaisuuksien määrittäminen](enable-ai.md)  
[Copilotin avulla luodut markkinointitekstiehdotukset](ai-overview.md)  
[Täsmäytä pankkitilit Copilotin avulla](bank-reconciliation-with-copilot.md)  
