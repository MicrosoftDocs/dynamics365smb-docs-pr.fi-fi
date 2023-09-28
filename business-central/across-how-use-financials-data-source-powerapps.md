---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: 'Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot Power Appsin avulla yrityssovelluksen.'
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten Power Appsin avulla

Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -tietoja Power Appsin tietolähteenä.  

> [!TIP]  
> Business Central tarjoaa nyt kehitys- ja toimintatukea Power Platformin Al-Go-ja näyte-ohjelmissa, joiden avulla pääset alkuun omien sovellusten luomisessa Power Appsissa. Nämä ominaisuudet ovat tällä hetkellä esiversiotoimintoja. Saat lisätietoja siirtymällä [Business Centraliin ja Power Appsiin](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) kehittäjien ja IT-ammattilaisten ohjeissa.

## Vaatimukset

Sinulla on oltava kelvollinen [!INCLUDE[prod_short](includes/prod_short.md)]- ja Power Apps -tili.  

## [!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power Appsin tietolähteeksi

Näiden vaiheiden avulla Business Centralin taulukko, kuten asiakkaat tai nimikkeet, lisätään Power Apps -sovelluksen tietolähteeksi.

1. Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/) ja kirjaudu sisään.
2. Valitse siirtymisruudussa vasemmalla puolella **+ Luo** ja valitse sitten **Lisää tietolähteitä** **Luo sovellus** -sivulta.
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. **Yhteydet**-luettelossa näkyvät kaikki olemassa olevat tietoyhteydet, jotka sinulla on.

   - Jos **Business Central** -yhteys on jo olemassa, valitse se ja valitse sitten **Luo**.

   - Jos et näe Business Central-yhteyttä, valitse **+ Uusi yhteys**, etsi ja valitse **Business Central** ja valitse sitten **Luo**.

   > [!NOTE]
   > Jos haluat yhdistää [!INCLUDE[prod_short](includes/prod_short.md)]iin paikallisesti, sinun täytyy valita **Business Central (paikallinen)** -yhdistin.  
  
4. Power Apps muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Kirjaudu Business Central -tilin käyttäjänimen ja salasanan avulla. Jos et ole järjestelmänvalvoja [!INCLUDE[prod_short](includes/prod_short.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.  
5. Kirjauduttuasi Power Apps näyttää luettelon *ympäristöistä ja yrityksistä*, jotka ovat käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)]issa. Valitse ne tiedot sisältävä ympäristö ja yritys, joihin haluat muodostaa yhteyden, kuten *TUOTANTO – oma yritys*.  
6. Seuraavaksi näkyviin tulee taulukkoluettelo, jotka näkyvät ympäristön ohjelmointirajapinnan osana. Valitse taulukko, johon haluat muodostaa yhteyden ja valitse sitten **Yhdistä**.

Power Appsin [!INCLUDE[prod_short](includes/prod_short.md)] -yhdistin näyttää nämä niin kutsutut taulukot päätepisteinä.  

> [!NOTE]
> Jos haluat sisällyttää muiden taulukoiden dataa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta sovelluksessasi, sinun tulee työskennellä kehittäjän kanssa, jotta voitte määrittää mukautetun API:n [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa.  

Tässä kohtaa olet yhdistänyt [!INCLUDE[prod_short](includes/prod_short.md)] dataasi ja olet valmis aloittamaan Power App -sovelluksesi rakentamisen. Voit aina luoda lisää ruutuja ja yhdistää lisädataan. Lue lisää kohdasta [Kaaviosovelluksen luominen Power Appsin mallista](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa. Lisätietoja on kohdassa [Kaaviosovelluksen tallentaminen julkaiseminen Power Appsissa](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## Katso myös

[Kaaviosovelluksen luominen Power Appsin mallista](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
