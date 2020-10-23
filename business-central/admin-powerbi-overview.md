---
title: Business Centralin Power BI -integrointiosa ja arkkitehtuurin yleiskatsaus | Microsoft Docs
description: Analyysitietojen, liiketoimintatietojen ja tunnuslukujen hakeminen Business Centralin tiedoista on helppoa Power BI:n Business Central -sovelluksia.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: d02740b0f4c73b96be9268cfdf5e4c3de157d5d5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924526"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a>[!INCLUDE[prodshort](includes/prodshort.md)]in Power BI -integrointiosa ja arkkitehtuurin yleiskatsaus

Tässä artikkelissa käsitellään Power BI:n ja [!INCLUDE[prodshort](includes/prodshort.md)]in integrointia eri tavoin, mikä auttaa ymmärtämään sen toteutusta ja käyttöä.

## <a name="components"></a>Komponentit

Seuraavassa taulukossa käsitellään Power BI -integraation keskeisiä komponentteja.

|Komponentti|Kuvaus|
|---------|-----------|
|Power BI|Pilvipohjaisen raportoinnin isännöinti- ja hallintapalvelu.|
|Power BI Desktop|Raporttien ja koontinäyttöjen luontityökalu, jolla voi suorittaa raportteja. Sen voi ladata maksutta Microsoft Storesta ja se asennetaan paikallisesti.|
|[!INCLUDE[prodshort](includes/prodshort.md)]|Online- tai paikallinen ratkaisu yhdistimineen on näkyvissä Power BI:ssa ja mahdollistaa Power BI -osan upotuksen.|

## <a name="whats-available-from-the-start"></a>Käytettävissä heti

Seuraavassa taulukossa käsitellään käytettävissä olevat ominaisuudet.

|Ominaisuus|[!INCLUDE[prodshort](includes/prodshort.md)] online- tai paikallisen version tuki|
|-------|---------------------|
|Power BI -yhdistimet|Molemmat. Online- ja paikallisessa versioilla eri liittimet. Samaa yhdistintä käytetään Power BI Desktopissa ja Power BI -palvelussa |
|Tietyn raportin upotettu tarkastelukokemus [!INCLUDE[prodshort](includes/prodshort.md)]in tietoruudussa|Molemmat. Edellyttää paikallisen version raporttien näyttämisen määrittämistä.|
|Power BI -raportin hallinta [!INCLUDE[prodshort](includes/prodshort.md)]issa|Online|
|Power BI:ssa näkyvät roolikeskusten Power BI -oletusraportit|Online|
|Power BI -sovellukset Microsoft AppSourcessa|Online.|

## <a name="architecture"></a>Arkkitehtuuri

[!INCLUDE[prodshort](includes/prodshort.md)] integroidaan Power BI:n kanssa ODataa käyttävällä yhdistimellä. Power BI -raporttien tietolähde näkyy OData-verkkopalveluina.

![Power BI:n ja Business Centralin integrointiarkkitehtuuri](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Yleinen työnkulku

Seuraava kaavio näyttää käyttäjien perustyönkulun yhdistettäessä [!INCLUDE[prodshort](includes/prodshort.md)] Power BI:hin.

![Power BI:n ja Business Centralin integroinnin työnkulku](./media/power-bi-flow.png)

1. Käyttää rekisteröityy Power BI -tilille.
2. Käyttää muodostaa yhteyden [!INCLUDE[prodshort](includes/prodshort.md)]sta Power BI:hin.
3. [!INCLUDE[prodshort](includes/prodshort.md)] tarkistaa käyttöoikeuden.
4. [!INCLUDE[prodshort](includes/prodshort.md)] ottaa oletusraportit käyttöön Power BI -palvelussa. Tämä vaihe tehdään vain [!INCLUDE[prodshort](includes/prodshort.md)] online -versiossa.
5. [!INCLUDE[prodshort](includes/prodshort.md)] tuo Power BI -raportit valittaviksi [!INCLUDE[prodshort](includes/prodshort.md)]issa. Oletusraportit näytetään automaattisesti Power BI -osissa.
6. Käyttäjä luo raportin Power BI Desktopissa.
7. Käyttäjä julkaisee raportin Power BI -palveluun. Raportit ovat sitten valittavissa [!INCLUDE[prodshort](includes/prodshort.md)]issa.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Business Central ja Power BI](admin-powerbi.md)  
[Power BI kuluttajille](/power-bi/consumer/end-user-consumer)  
[Power BI -palvelun uusi ulkoasu](/power-bi/service-new-look)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI -dokumentaatio](/power-bi/)  
[Business Intelligence](bi.md)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power Automate'ssa](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
