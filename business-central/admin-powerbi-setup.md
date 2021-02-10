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
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: dd0974c20f8c038fcc0cac27c9ef165b2aadcd36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752498"
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

1. OData-verkkopalvelut ja ODataV4-päätepiste on otettu käyttöön.

    OData-verkkopalvelu on otettava käyttöön [!INCLUDE[server](includes/server.md)]issä ja OData-portti avattava palomuurissa. Lisätietoja on kohdassa [Business Central Serverin määrittäminen – OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    Internet-yhteys on voitava muodostaa paikalliseen palvelimeen.

2. [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjätileillä on verkkopalvelun käyttöoikeusavain.

    Verkkopalvelun käyttöoikeusavain tarvitaan [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen tarkastelemiseen Power BI:ssa. Verkkopalvelun käyttöoikeusavain voidaan määrittää kullekin käyttäjätilille. Vaihtoehtoisesti voidaan luoda tietty tili, jonka verkkopalvelun käyttöoikeusavainta kaikki käyttäjät voivat käyttää. Lisätietoja on kohdassa [Verkkopalvelujen todennus](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. NavUserPassword tai Azure Active Directory -todennus on määritetty.

4. [!INCLUDE[prod_short](includes/prod_short.md)] -sivuille upotettujen Power BI -raporttien näyttämistä varten sovellus on rekisteröitävä [!INCLUDE[prod_short](includes/prod_short.md)]ia varten Microsoft Azuressa.

    Rekisteröity sovellus tarvitsee Power BI -palvelujen käyttöoikeuden. Lisätietoja on kohdassa [Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version rekisteröinti Azure AD:ssä muiden palvelujen integrointia varten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Jos käyttöönotto käyttää NavUserPassword-todennusta, [!INCLUDE[prod_short](includes/prod_short.md)] muodostaa yhteyden samaan Power BI -palveluun kaikilla käyttäjillä. Tämä palvelu määritetään sovelluksen rekisteröinnin yhteydessä. Azure AD -todennuksessa [!INCLUDE[prod_short](includes/prod_short.md)] muodostaa yhteyden yksittäisiin käyttäjätileihin liitettyyn Power BI -palveluun.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

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
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Automate'ssa](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
