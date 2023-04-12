---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: 'Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot Power Appsin avulla yrityssovelluksen.'
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 04/01/2023
ms.author: jswymer
---
# Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten Power Appsin avulla

Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -tietoja Power Appsin tietolähteenä.  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[prod_short](includes/prod_short.md)]- ja Power Apps -tili.  

## [!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power Appsin tietolähteeksi

1. Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/) ja kirjaudu sisään.
2. Valitse aloitussivun **Aloita tiedoista** -osassa **Muut tietolähteet** -ruutu.  

    Power Apps Studio avautuu. Ensimmäisellä kertaa kirjauduttaessa on määritettävä maa tai alue.  
3. Tarjolla olevien yhteyksien joukosta, valitse **Business Central**, ja valitse sitten **Luo** nappula.

    Power Apps muodostaa [!INCLUDE[prod_short](includes/prod_short.md)] -yhteyden niillä käyttäjätiedoilla, joilla olet kirjautunut sisään. Jos et ole järjestelmänvalvoja [!INCLUDE[prod_short](includes/prod_short.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.  

4. Power Apps näyttää luettelon *ympäristöistä ja yrityksistä*, jotka ovat käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)]issa. Valitse ne tiedot sisältävä ympäristö ja yritys, joihin haluat muodostaa yhteyden, kuten *TUOTANTO – oma yritys*.  

5. Seuraavaksi näkyviin tulee taulukkoluettelo, jotka näkyvät ympäristön ohjelmointirajapinnan osana. Valitse taulukko, johon haluat muodostaa yhteyden ja valitse sitten **Yhdistä**.

Power Appsin [!INCLUDE[prod_short](includes/prod_short.md)] -yhdistin näyttää nämä niin kutsutut taulukot päätepisteinä.  

> [!NOTE]
> Jos haluat sisällyttää muiden taulukoiden dataa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta sovelluksessasi, sinun tulee työskennellä kehittäjän kanssa, jotta voitte määrittää mukautetun API:n [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa.  

Tässä kohtaa olet yhdistänyt [!INCLUDE[prod_short](includes/prod_short.md)] dataasi ja olet valmis aloittamaan PowerAppisi rakentamisen. Voit luoda lisää ruutuja ja yhdistää lisädataan [!INCLUDE[prod_short](includes/prod_short.md)]. Lisätietoja on kohdassa [Kaaviosovelluksen luominen Power Appsin mallista](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa. Lisätietoja on kohdassa [Kaaviosovelluksen tallentaminen julkaiseminen Power Appsissa](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Jos haluat yhdistää [!INCLUDE[prod_short](includes/prod_short.md)]iin paikallisesti, sinun täytyy valita  **Business Central (paikallinen)** yhdistin vaiheessa 3.  

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/power-apps-power-automate-business-central/)

## Katso myös

[Kaaviosovelluksen luominen Power Appsin mallista](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
