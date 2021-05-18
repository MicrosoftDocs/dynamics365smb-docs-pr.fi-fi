---
title: Power BIn ja Business Centralin integroinnin käyttöönotto
description: Katso, miten voit määrittää yhteyden Power BI:hin, jotta voit saada kävijätietoja, liiketoimintatietoja ja suorituskykyilmaisimia Business Centralin tiedoista Business Centralin Power BI -sovelluksiin.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 4b8fbdb89f47a05d4265751fddc10ab208901831
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935109"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Power BI:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in integroinnin ottaminen käyttöön

Tässä artikkelissa käsitellään [!INCLUDE[prod_short](includes/prod_short.md)]in valmistelua Power BI -integrointia varten. Vaikka integrointi on jo otettu käyttöön [!INCLUDE[prod_short](includes/prod_short.md)] online -versiossa, kannattaa kuitenkin tutustua joihinkin käyttöoikeuksia koskeviin tietoihin. Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa ympäristön on määritettävä muodostamaan yhteys Power BI:hin, ennen kuin käyttäjät voivat käyttää sitä.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI:n käyttöoikeudet

Käyttäjät saavat [!INCLUDE[prod_short](includes/prod_short.md)]in mukana maksuttoman Power BI -käyttöoikeuden, jolla voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in ja Power BI:n tavallisia ominaisuuksia. Ostamalla Power BI Pro -käyttöoikeuden saa käyttöön myös lisäominaisuuksia. Seuraavassa taulukossa on kunkin käyttöoikeuden ominaisuuksien yleiskatsaus.

|Power-käyttöoikeus|Raporttien näyttäminen|Raporttien luominen|Raporttien jakaminen|Raporttien päivittäminen| [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukset|
|-------------|--------||
|Power BI, maksuton|![valintamerkki](media/check.png)|![toinen valintamerkki](media/check.png)|(rajoitettu)|(rajoitettu)||
|Power BI Pro|![vielä yksi valintamerkki](media/check.png)|![se on valintamerkki](media/check.png)|![jälleen valintamerkki](media/check.png)|(laaja)|![viimeinen valintamerkki](media/check.png)|

Lisätietoja on kohdassa [Power BI -palvelun käyttöoikeuden organisaation käyttäjille](/power-bi/admin/service-admin-licensing-organization) tai [Rekisteröityminen Power BI -palveluun henkilönä](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version Power BI -integroinnin valmistelu

Tässä osassa käsitellään paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -käyttöönoton edellytyksiä Power BI -integrointia varten.

1. Määritä joko NavUserPassword tai Azure Active Directory -todennus käyttöönottoa varten.

    Power BI -integrointi ei tue Windows-todennusta.  

2. Ota OData-verkkopalvelut ja ODataV4-päätepiste käyttöön.

    OData-verkkopalvelu on otettava käyttöön [!INCLUDE[server](includes/server.md)]issä ja OData-portti avattava palomuurissa. Lisätietoja on kohdassa [Business Central Serverin määrittäminen – OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Internet-yhteys on voitava muodostaa paikalliseen palvelimeen.

3. Anna [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjätileille verkkopalvelun käyttöoikeusavain.

    Verkkopalvelun käyttöoikeusavain tarvitaan vain [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen tarkastelemiseen Power BI:ssa. Verkkopalvelun käyttöoikeusavain voidaan määrittää kullekin käyttäjätilille. Vaihtoehtoisesti voidaan luoda tietty tili, jonka verkkopalvelun käyttöoikeusavainta kaikki käyttäjät voivat käyttää. Lisätietoja on kohdassa [Verkkopalvelujen todennus](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](../upgrade/deprecated-features-w1.md#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Using OAuth to Authorize Business Central Web Services](../webservices/authenticate-web-services-using-oauth.md).-->

4. Luo sovelluksen rekisteröinti [!INCLUDE[prod_short](includes/prod_short.md)]ille Microsoft Azuressa.

    Jos haluat tarkastella [!INCLUDE[prod_short](includes/prod_short.md)] -sivuihin upotettuja Power BI -raportteja, sovelluksen täytyy olla rekisteröity [!INCLUDE[prod_short](includes/prod_short.md)]ille Microsoft Azuressa. Rekisteröity sovellus tarvitsee oikeuden Power BI -palveluihin. Lisätietoja on kohdassa [Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version rekisteröinti Azure AD:ssä muiden palvelujen integrointia varten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Jos käyttöönotto käyttää NavUserPassword-todennusta, [!INCLUDE[prod_short](includes/prod_short.md)] muodostaa yhteyden samaan Power BI -palveluun kaikilla käyttäjillä. Tämä palvelu määritetään sovelluksen rekisteröinnin yhteydessä. Azure AD -todennuksessa [!INCLUDE[prod_short](includes/prod_short.md)] muodostaa yhteyden yksittäisiin käyttäjätileihin liitettyyn Power BI -palveluun.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Luo ensimmäinen yhteys Business Centralista Power BI -palveluun.

    Ennen kuin loppukäyttäjät voivat käyttää Power BI:tä [!INCLUDE[prod_short](includes/prod_short.md)]issa, Azure-sovelluksen järjestelmänvalvojan täytyy antaa suostumuksensa Power BI-palvelulle.

    Voit muodostaa ensimmäisen yhteyden avaamalla [!INCLUDE[prod_short](includes/prod_short.md)]in ja suorittamalla roolikeskuksessa **Aloita Power BI:n käyttö** -toiminnon. Tämä toiminto opastaa hyväksyntäprosessin läpi ja tarkistaa Power BI -käyttöoikeutesi. Ohjelma pyytää kirjautumaan sisään käyttämällä Azuren järjestelmänvalvojatiliä. Lisätietoja on kohdassa [Power BI -yhteyden muodostaminen – kerran](across-working-with-powerbi.md#connect).

## <a name="publish-data-as-web-services"></a>Tietojen julkaisu verkkopalveluina

Codeunitit, sivut ja kyselyt, joita halutaan käyttää Power BI -raporttien tietolähteenä, on julkaistava verkkopalveluina. Useita verkkopalveluja julkaistaan oletusarvoisesti. Verkkopalveluja voi etsiä kätevästi hakemalla *verkkopalveluja* [!INCLUDE[prod_short](includes/prod_short.md)]issa. Varmista **Verkkopalvelut**-sivulla, että **Julkaisu**-kenttä on valittuna edellä mainituissa verkkopalveluissa. Tämä on yleensä järjestelmänvalvojan tehtävä.

Lisätietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

> [!TIP]
> Lisätietoja tavoista, joilla voidaan verkkopalvelujen paras mahdollinen suorituskyky sekä Business Central Serverin (päätepiste) että kuluttajan (asiakasohjelma) kannalta, on kohdassa [Tehokkaiden verkkopalvelujen kirjoittaminen](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Business Central ja Power BI](admin-powerbi.md)  
[Power BI:n -integrointiosa ja [!INCLUDE[prod_short](includes/prod_short.md)] -arkkitehtuurin yleiskatsaus](admin-powerbi-overview.md)  
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