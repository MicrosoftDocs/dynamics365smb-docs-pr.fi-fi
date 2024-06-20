---
title: Power BIn ja Business Centralin integroinnin käyttöönotto
description: 'Lue, miten voit määrittää yhteyden Power BI:hin. Merkityksellisten tietojen, liiketoimintatietojen ja tunnuslukujen saaminen Business Central -tiedoista Power BI -raporttien avulla.'
author: jswymer
ms.topic: get-started
ms.search.keywords: 'Power BI, setup, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/28/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
---
# Power BI:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in integroinnin ottaminen käyttöön

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Tässä artikkelissa käsitellään [!INCLUDE[prod_short](includes/prod_short.md)]in valmistelua Power BI -integrointia varten. Vaikka integrointi on jo otettu käyttöön [!INCLUDE[prod_short](includes/prod_short.md)] online -versiossa, kannattaa kuitenkin tutustua joihinkin käyttöoikeuksia koskeviin tietoihin. Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa ympäristön on määritettävä muodostamaan yhteys Power BI:hin, ennen kuin käyttäjät voivat käyttää sitä.

## <a name="license"></a>Power BI:n käyttöoikeudet

Käyttäjät saavat [!INCLUDE[prod_short](includes/prod_short.md)]in mukana maksuttoman Power BI -käyttöoikeuden, jolla voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in ja Power BI:n tavallisia ominaisuuksia. Ostamalla Power BI Pro -käyttöoikeuden saa käyttöön myös lisäominaisuuksia. Seuraavassa taulukossa on kunkin käyttöoikeuden ominaisuuksien yleiskatsaus.

|Power-käyttöoikeus|Raporttien näyttäminen|Raporttien luominen|Raporttien jakaminen|Raporttien päivittäminen| [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukset|
|-------------|--------||
|Power BI, maksuton|![valintamerkki.](media/check.png)|![toinen valintamerkki](media/check.png)|(rajoitettu)|(rajoitettu)||
|Power BI Pro|![vielä yksi valintamerkki.](media/check.png)|![se on valintamerkki](media/check.png)|![jälleen valintamerkki](media/check.png)|(laaja)|![viimeinen valintamerkki](media/check.png)|

Lisätietoja on kohdassa [Power BI -palvelun käyttöoikeuden organisaation käyttäjille](/power-bi/admin/service-admin-licensing-organization) tai [Rekisteröityminen Power BI -palveluun henkilönä](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="exposedata"></a>Tietojen näyttäminen ohjelmointirajapinnan tai OData-verkkopalvelujen kautta

Business Central tarjoaa kaksi tapaa näyttää tiedot, joita Power BI -raportit voivat käyttää: API-sivut tai -kyselyt ja OData (Open Data Protocol) -verkkopalvelut.

### API-sivut ja -kyselyt

> **KOHDE:** vain Business Central online

Kehittäjät voivat määrittää sivuobjekteja ja kyselyobjekteja, joiden tyyppi on *API*. Tällä tavalla he voivat näyttää tietoja tietokantataulukoista webhook-tuetun, OData v4 -yhteensopivan REST-palvelun avulla. Tämäntyyppisiä tietoja ei voi näyttää käyttöliittymässä, vaan ne on tarkoitettu luotettavien integrointipalveluiden rakentamiseen.

Business Central online sisältää useita sisäänrakennettuja ohjelmointirajapintoja, joiden avulla voit saada tietoja yleisimmistä liiketoimintaentiteeteistä, kuten asiakkaista, nimikkeistä ja myyntitilauksista. Näiden ohjelmointirajapintojen käyttö raporttien tietolähteenä ei edellytä lisätyötä tai Power BI -asetuksia. Lisätietoja näistä ohjelmointirajapinnoista on kohdassa [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online tukee myös mukautettuja ohjelmointirajapintoja. Business Central -ratkaisujen sovelluskehittäjät voivat luoda omia API-sivujaan ja -kyselyjään ja pakata ne sovelluksiksi. Sitten sovellukset asennetaan vuokraajaan. Kun asennus on valmis, voit käyttää API-sivuja Power BI -raporteissasi, kuten tekisit sisäänrakennettujen ohjelmointirajapintojenkin (v2.0) kanssa. Lisätietoja API:n luomisesta näyttämällä sivuja tai kyselyjä on kohdassa [Mukautetun ohjelmointirajapinnan kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Helmikuusta 2022 alkaen [!INCLUDE[prod_short](includes/prod_short.md)] Onlinen Power BI -raporttien lähteenä käytetään suorituskykysyistä toissijaista vain luku -tilassa olevaa tietokantareplikaa. Tämän seurauksena AL-kehittäjien pitäisi välttää sellaisten ohjelmointirajapintasivujen kehittämistä, jotka muokkaavat tietokantoja, kun sivut avautuvat tai lataavat tietueita. Erityistä huomiota kannattaa kiinnittää AL-käynnistinten OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord ja OnAfterGetCurrRecord koodiin. Nämä tietokantamuutokset voivat joissakin tapaukissa aiheuttaa suorituskykyongelmia ja estää raporttia päivittämästä tietoja. Lisätietoja on Business Centralin kehityssisällön kohdassa [Kehittäjien suorituskykyartikkelit](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services).
>
> Joissakin harvoissa tapauksissa tämä toiminta aiheuttaa virheen, kun käyttäjä yrittää noutaa tietoja ohjelmointirajapinnasta Power BI Desktop -raporttia varten. Jos tietokantamuutokset kuitenkin ovat tarpeen muokatulla ohjelmointirajapinnalla, Power BI Desktopin käyttäjät voivat pakottaa tämän toimintatavan. Lisätietoja: [Power BI -raporttien kokoaminen näyttämään Business Central -tietoja](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### OData-verkkopalvelut

Voit julkaista Business Central -sovellusobjekteja kuten koodiyksikköjä, sivuja ja kyselyitä [OData-verkkopalveluina](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Business Central onlinessa on oletusarvoisesti julkaistu monia verkkopalveluita. Verkkopalveluja voi etsiä kätevästi hakemalla *verkkopalveluja* [!INCLUDE[prod_short](includes/prod_short.md)]issa. Varmista **Verkkopalvelut**-sivulla, että **Julkaisu**-kenttä on valittuna edellä mainituissa verkkopalveluissa. Lisätietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

Lisätietoja tavoista, joilla voidaan verkkopalvelujen paras mahdollinen suorituskyky sekä Business Central Serverin (päätepiste) että kuluttajan (asiakasohjelma) kannalta, on kohdassa [Tehokkaiden verkkopalvelujen kirjoittaminen](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### API-sivujen tai OData-verkkopalvelujen valitseminen

Aina kun mahdollista, suositellaan käyttämään API-sivuja OData-verkkopalvelun sijaan. API-sivut lataavat tiedot nopeammin Power BI -raportteihin kuin OData-verkkopalvelut. Lisäksi ne ovat joustavampia, koska niiden avulla voit saada tietoja taulukon kentistä, joita ei ole määritetty sivuobjektissa.

<!--## <a name="setup"></a>Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration

This section explains the requirements for a [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment to integrate with Power BI.

1. Configure either [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) or [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) as the authentication method for the deployment.  
    
    > [!NOTE]
    > Power BI integration doesn't support Windows authentication and is not supported on Windows Client.

2. Enable OData web services and the ODataV4 endpoint.

    OData web service must be enabled on the [!INCLUDE[server](includes/server.md)], and OData port opened in firewall. For more information, see [Configuring Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    The local server must be accessible from the Internet.

3. Give [!INCLUDE[prod_short](includes/prod_short.md)] user accounts a web service access key.

    A web service access key is only needed to view [!INCLUDE[prod_short](includes/prod_short.md)] data in Power BI. You can assign a web service access key to each user account. Or instead, create a specific account with a web service access key for use by all users. For more information, see [Web Services Authentication](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

<!--4. Create an application registration for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    To view Power BI reports embedded in [!INCLUDE[prod_short](includes/prod_short.md)] pages, an application must be registered for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. The registered application needs permission to Power BI services. At a minimum, the app requires  **User.ReadWrite.All** permission. For users to view reports from shared Power BI workspaces, the app requires **Workspace.Read.All** permission. For more information, see [Registering [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises in Microsoft Entra ID for Integrating with Other Services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > If your deployment uses NavUserPassword authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the same Power BI service for all users. You'll specify this service account as part of registering the application. With Microsoft Entra authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the Power BI service associated with the individual user accounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
<!--5. Make the initial connection from Business Central to Power BI.

    Before end-users can use Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], an Azure application administrator will have to give consent to the Power BI service.

    To make the initial connection, open [!INCLUDE[prod_short](includes/prod_short.md)], and run **Get Started with Power BI** from the Home page. This action will lead you through the consent process, and check your Power BI license. When prompted sign in using an Microsoft Entra admin account. For more information, see [Connect to Power BI - one time only](across-working-with-powerbi.md#connect).-->

## Tietovoiden määrittäminen

Tietovoiden avulla voit tarkastella, muuntaa ja ladata tietoja Power BI -työtilaan ja käyttää sitten tietoja raporttien perustana. Näissä tietovoissa voi joissakin tapauksissa ilmetä ohimeneviä virheitä ajoitetun päivityksen yhteydessä. Virheviesti näyttää tältä: `DataSource.Error: OData: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.` 

PowerAutomaten avulla voit määrittää uudelleenyritykset tälle paikalle. Lisätietoja on kohdassa [Tietovuon automaattinen uudelleenyritys epäonnistumisen jälkeen](/power-query/dataflows/automatically-retry-dataflow).

## Katso myös

[Business Central ja Power BI](admin-powerbi.md)  
[Power BI -integrointiosa ja [!INCLUDE[prod_short](includes/prod_short.md)] -arkkitehtuurin yleiskatsaus](admin-powerbi-overview.md)  
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
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Automatessa](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
