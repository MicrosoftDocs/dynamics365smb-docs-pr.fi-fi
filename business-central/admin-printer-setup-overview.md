---
title: Tulostimen asetusten ja hallinnan yleiskuvaus
description: Tietoja Business Centralin erilaisista tulostinmahdollisuuksia
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: overview
ms.date: 09/28/2023
ms.custom: bap-template
---

# Tulostimen asetusten ja hallinnan yleiskuvaus

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Asiakirjojen ja raporttien tulostaminen [!INCLUDE[prod_short](includes/prod_short.md)]ista on tärkeä tehtävä yrityskäyttäjille. Käyttäjä haluaa yleensä lähettää tulostustyöt suoraan johonkin organisaation tulostimiin riippumatta siitä, mikä [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelma tai -sovellus on käytössä. Koska [!INCLUDE[prod_short](includes/prod_short.md)] online on pilvipalvelu, se ei voi olla suoraan yhteydessä käyttäjien laitteisiin yhdistettyihin tulostimiin. Se voidaan kuitenkin yhdistää pilvipohjaisiin tulostimiin.

## Business Centralin tulostinmahdollisuudet

[!INCLUDE[prod_short](includes/prod_short.md)]issa on seuraavat tulostamista tukevat ominaisuudet:

|Ominaisuus|Kuvaus|Verkkoasiakasohjelma| Mobiilisovellus|Teamsin käyttöön sopiva sovellus|
|-------|-----------|----------|-----------|--------------|
|Yleistulostus|Yleistulostus on Microsoftin pilvipalveluna saatava tulostimen hallintaratkaisu. Tällä ominaisuudessa tulostimet voidaan määrittää yleistulostuksessa, jonka jälkeen rekisteröidään käyttöä varten [!INCLUDE[prod_short](includes/prod_short.md)]issa. Ominaisuuden käyttöä varten tarvitaan yleistulostustilaus ja **Yleistulostuksen integrointi** -laajennus.|![toimii verkossa.](media/check.png)|![toimii verkossa.](media/check.png)|![toimii verkossa](media/check.png)|
|Sähköpostitulostus|Tällä ominaisuudella voidaan määrittää sähköpostitulostukseen sopivia tulostimia. [!INCLUDE[prod_short](includes/prod_short.md)] lähettää sitten tulostustyöt tulostimeen käyttämällä tulostimen sähköpostiosoitetta. Ominaisuuden käyttöä varten tarvitaan tulostin, jossa sähköpostitulostus on otettu käyttöön, ja **Lähetä sähköpostitulostimeen** -laajennus.|![toimii verkossa.](media/check.png)|![toimii verkossa](media/check.png)|![toimii verkossa](media/check.png)|
|Selaimesta tulostaminen|Käyttäjän selaimen tulostustoiminto käsittelee tulostustyöt. Jos pilvitulostinta ei ole asennettu ja määritetty tai jos asennettu tulostin ei toimi kunnolla, tulostuksessa käytetään selaimen tulostusasetusten oletustulostinta. Raportin pyyntösivun **Tulostin**-kentässä on teksti *(Käsitellään selaimessa)*.|![toimii verkossa](media/check.png)|||

Tulostimet määritetään pääasiassa [!INCLUDE[prod_short](includes/prod_short.md)]in **Tulostimien hallinta** -sivulla. Yleistulostuksen tulostimien yhteydessä on kuitenkin ehkä käytettävä myös Microsoft 365 -hallintakeskusta ja Azure-portaalia.

> [!IMPORTANT]
> Paikallisessa Business Centralissa yleistulostus ja sähköpostitulostus edellyttävät Microsoft Entra ID- -tai NavUserPassword-todennuksen käyttöä.

## Mukautetut tulostinlaajennukset

[!INCLUDE[prod_short](includes/prod_short.md)] tukee muita mukautettuja tulostinlaajennuksia, joilla saadaan käyttöön vielä lisää tulostusominaisuuksia. Jos asennettuna on mukautettuja tulostinlaajennuksia, sovelluksessa voi olla sellaisia tulostusominaisuuksia, joita ei käsitellä tässä artikkelissa.

AL-kehittäjille tarkoitettuja lisätietoja tulostinlaajennusten luomisesta on kohdassa [Tulostinlaajennusten kehittäminen Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## Seuraavat vaiheet

- [Yleistulostuksen tulostimien määrittäminen](admin-printer-setup-universal-print.md)  
- [Sähköpostitulostuksen määrittäminen](admin-printer-setup-email.md)  
- [Oletustulostimien määrittäminen](ui-specify-printer-selection-reports.md)