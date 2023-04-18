---
title: Määritä yhteyshenkilön synkronointi paikalliselle Outlook for Business Centralille
description: Tietoja paikallisen Business Central -ympäristön määrittämisestä synkronoimaan yhteyshenkilöitä Business Centralissa ja Outlookissa.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/04/2023
ms.custom: bap-template
---

# Määritä yhteyshenkilön synkronointi paikalliselle Outlook for Business Centralille

Tässä artikkelissa on tietoja siitä, miten voit määrittää paikalliset [!INCLUDE[prod_short](includes/prod_short.md)]-tiedot synkronoimaan yhteyshenkilöitä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa Outlook-kontaktien avulla. Lisätietoja ominaisuudesta on kohdassa [Synkronoi yhteystiedot Business Centralissa Microsoft Outlookin kontaktien avulla](admin-synchronize-outlook-contacts.md).

## Esittely

Kontaktin synkronointi edellyttää OAuth 2.0-protokollan käyttämistä Exchange Online -todennukseen. Aiemmin perustodennusta tuettiin myös, mutta se on vanhentunut eikä sitä enää tueta Exchange Onlinessa. Voit lukea lisää poistoista kohdassa [Perustodennuksen vanhentuminen Exchange Onlinessa](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Tämä muutos tarkoittaa sitä, että Business Centralin yhteystietojen synkronointi on saattanut lakata toimimasta paikallisessa ympäristössä. Tämä artikkeli kertoo, miten saada se taas toimimaan.

## Vaatimukset

- Exchange Online, joko itsenäinen versio tai Microsoft 365 -suunnitelman kautta  
- Käytä Azure Active Directory ( Azure AD) -vuokralaista, jota Exchange Online käyttää
- [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjillä on Microsoft 365- tai Exchange Online -sähköpostitili, joka on liitetty [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman tileihin. Voit tarkistaa tämän asetuksen **Käyttäjät**-luettelossa käyttäjäprofiilin **Microsoft 365 -todennus** -osassa. 

## Kontaktin synkronoinnin määritys

Määritä kontaktin synkronointi suorittamalla seuraavat vaiheet. Jos käytössäsi on [!INCLUDE[prod_short](includes/prod_short.md)] kevät 2019 (v.14), sinun on tehtävä ylimääräinen vaihe, joka joko muuttaa sovelluskoodia tai määrittää yhteyden Power BI:hin.

1. <a name="registerapp"></a>Sovelluksen rekisteröinti Exchange Online -ohjelmointirajapintaan Azure AD -vuokraajassa.

   Tässä vaiheessa lisäät rekisteröidyn sovelluksen Microsoft 365- tai Exchange Online- suunnitelman Azure AD -vuokraajassa. Muiden Business Centralissa käytettävien Azure-palvelujen tavoin Exchange Online edellyttää rekisteröityä sovellusta Azure ADssa. Rekisteröity sovellus tuottaa Business Centralin ja Exchange Onlinein välisiä todennus- ja valtuutuspalveluita.

   Seuraa yksityiskohtaisia ohjeita kehittäjä- ja IT-ammattilaisen tuessa kohdassa [Sovelluksen rekisteröinti Azure Active Directoryssa](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) . Kun käyt läpi ohjeita, muista seuraavat asiat:

   - Jos olet jo rekisteröinyt sovelluksen osana jonkin muun Microsoft-tuotteen (kuten Power BI) integrointia, voit käyttää kyseistä rekisteröityä sovellusta uudelleen. Tässä tapauksessa sinun on vain määritettävä sovellus Office 365 Exchange Online -käyttöoikeuksilla, jotka on kuvattu seuraavassa luettelossa.

   - Määritä rekisteröidylle sovellukselle seuraavat delegoidut käyttöoikeudet Office 365 Exchange Online API -liittymään:

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. Tee [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa 14 jokin seuraavista tehtävistä:

   - Muokkaa sivua 6700 muuttamalla `FALSE` `TRUE`:ksi seuraavan rivin koodilla `OnPageOpen`-käynnistimessä:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Luo uusi sivu, jossa on seuraava koodi OnPageOpen-käynnistimelle:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Määritä Power BI seuraamalla ohjeita kohdassa [Määritä paikallisen Business Centralin Power BI -integraatio](admin-powerbi-setup.md#setup).

   Kun valitsemasi ratkaisu on valmis, pyydä käyttäjiä joko suorittamaan uusi/modifioitu sivu tai [muodostamaan yhteys Power BI:hin](across-working-with-powerbi.md#connect). Tämä vaihe tarvitsee tehdä vain kerran.

## Seuraavat vaiheet

[Business Centralin kontaktien synkronisointi Microsoft Outlookin yhteystietojen kanssa](admin-synchronize-outlook-contacts.md)  
