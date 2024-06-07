---
title: Copilot- ja tekoälyominaisuuksien vianmääritys
description: 'Opi korjaamaan yleisiä ongelmia, joita saatat kohdata käyttäessäsi Copilot- ja tekoälyominaisuuksia Business Centralissa.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 02/01/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
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

## Microsoftin avustajaominaisuudet, joita ei ole lueteltu Copilot- ja tekoälyominaisuudet -sivulla

Jos mikään Microsoftin tekoälyominaisuuksista ei näy **Copilotin ja tekoälyn ominaisuudet** -sivulla, se johtuu todennäköisesti siitä, että ympäristöösi on asennettu yksi tai useampi upotettu sovellus. Upotetut sovellukset voivat tarjota omia Copilot-ominaisuuksia, mutta Microsoftin julkaisemat ominaisuudet eivät ole yhteensopivia sellaisten ympäristöjen kanssa, joihin on upotettu sovelluksia.

## Katso myös

[Copilot- ja tekoälyominaisuuksien määrittäminen](enable-ai.md)  
[Copilotin avulla luodut markkinointitekstiehdotukset](ai-overview.md)  
[Täsmäytä pankkitilit Copilotin avulla](bank-reconciliation-with-copilot.md)  
