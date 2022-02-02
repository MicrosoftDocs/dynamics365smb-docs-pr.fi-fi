---
title: Business Centralin Power BI -integrointiosa ja arkkitehtuurin yleiskatsaus | Microsoft Docs
description: Lisätietoja Power BI:n integroinnista Business Centralin kanssa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 9ce0b5232a0629bb6248eaaaade69b7c7ebceb02
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012339"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a>[!INCLUDE[prod_short](includes/prod_short.md)]in Power BI -integrointiosa ja arkkitehtuurin yleiskatsaus

Tässä artikkelissa käsitellään Power BI:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in integrointia eri tavoin, mikä auttaa ymmärtämään sen toteutusta ja käyttöä.

## <a name="components"></a>Komponentit

Seuraavassa taulukossa käsitellään Power BI -integraation keskeisiä komponentteja.

|Komponentti|Kuvaus|
|---------|-----------|
|Power BI|Pilvipohjaisen raportoinnin isännöinti- ja hallintapalvelu.|
|Power BI Desktop|Raporttien ja koontinäyttöjen luontityökalu, jolla voi suorittaa raportteja. Sen voi ladata maksutta Microsoft Storesta ja se asennetaan paikallisesti.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Online- tai paikallinen ratkaisu yhdistimineen on näkyvissä Power BI:ssa ja mahdollistaa Power BI -osan upotuksen.|

## <a name="whats-available-from-the-start"></a>Käytettävissä heti

Seuraavassa taulukossa käsitellään käytettävissä olevat ominaisuudet.

|Ominaisuus|[!INCLUDE[prod_short](includes/prod_short.md)] online- tai paikallisen version tuki|
|-------|---------------------|
|Power BI -yhdistimet|Molemmat. Online- ja paikallisessa versioilla eri liittimet. Samaa yhdistintä käytetään Power BI Desktopissa ja Power BI -palvelussa |
|Tietyn raportin upotettu tarkastelukokemus [!INCLUDE[prod_short](includes/prod_short.md)]in tietoruudussa|Molemmat. Edellyttää paikallisen version raporttien näyttämisen määrittämistä.|
|Power BI -raportin hallinta [!INCLUDE[prod_short](includes/prod_short.md)]issa|Online|
|Power BI:ssa näkyvät roolikeskusten Power BI -oletusraportit|Online|
|Power BI -sovellukset Microsoft AppSourcessa|Online|

## <a name="architecture"></a>Arkkitehtuuri

[!INCLUDE[prod_short](includes/prod_short.md)] integroidaan Power BI:n kanssa ODataa käyttävällä yhdistimellä. Power BI -raporttien tietolähde näkyy API-sivuina ja OData-verkkopalveluina.

![Power BI:n ja Business Centralin integrointiarkkitehtuuri.](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Yleinen työnkulku

Seuraava kaavio näyttää käyttäjien perustyönkulun yhdistettäessä [!INCLUDE[prod_short](includes/prod_short.md)] Power BI:hin.

![Power BI:n ja Business Centralin integroinnin työnkulku.](./media/power-bi-flow.png)

1. Käyttää rekisteröityy Power BI -tilille.
2. Käyttää muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]sta Power BI:hin.
3. [!INCLUDE[prod_short](includes/prod_short.md)] tarkistaa käyttöoikeuden.
4. [!INCLUDE[prod_short](includes/prod_short.md)] ottaa oletusraportit käyttöön Power BI -palvelussa. Tämä vaihe tehdään vain [!INCLUDE[prod_short](includes/prod_short.md)] online -versiossa.
5. [!INCLUDE[prod_short](includes/prod_short.md)] tuo Power BI -raportit valittaviksi [!INCLUDE[prod_short](includes/prod_short.md)]issa. Oletusraportit näytetään automaattisesti Power BI -osissa.
6. Käyttäjä luo raportin Power BI Desktopissa.
7. Käyttäjä julkaisee raportin Power BI -palveluun. Raportit ovat sitten valittavissa [!INCLUDE[prod_short](includes/prod_short.md)]issa.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Business Central ja Power BI](admin-powerbi.md)  
[Power BI kuluttajille](/power-bi/consumer/end-user-consumer)  
[Power BI -palvelun uusi ulkoasu](/power-bi/service-new-look)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI -dokumentaatio](/power-bi/)  
[Business Intelligence](bi.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Automate'ssa](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]