---
title: Power BIn ja Business Centralin integroinnin käyttöönotto
description: 'Lue, miten voit määrittää yhteyden Power BI:hin. Merkityksellisten tietojen, liiketoimintatietojen ja tunnuslukujen saaminen Business Central -tiedoista Power BI -raporttien avulla.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power BI, setup, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 07/13/2022
ms.author: jswymer
---
# <a name="enabling-power-bi-integration-with-"></a><a name="enabling-power-bi-integration-with-"></a>Power BI:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in integroinnin ottaminen käyttöön

Tässä artikkelissa käsitellään [!INCLUDE[prod_short](includes/prod_short.md)]in valmistelua Power BI -integrointia varten. Vaikka integrointi on jo otettu käyttöön [!INCLUDE[prod_short](includes/prod_short.md)] online -versiossa, kannattaa kuitenkin tutustua joihinkin käyttöoikeuksia koskeviin tietoihin. Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa ympäristön on määritettävä muodostamaan yhteys Power BI:hin, ennen kuin käyttäjät voivat käyttää sitä.

## <a name="power-bi-licensing"></a><a name="power-bi-licensing"></a><a name="license"></a>Power BI:n käyttöoikeudet

Käyttäjät saavat [!INCLUDE[prod_short](includes/prod_short.md)]in mukana maksuttoman Power BI -käyttöoikeuden, jolla voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in ja Power BI:n tavallisia ominaisuuksia. Ostamalla Power BI Pro -käyttöoikeuden saa käyttöön myös lisäominaisuuksia. Seuraavassa taulukossa on kunkin käyttöoikeuden ominaisuuksien yleiskatsaus.

|Power-käyttöoikeus|Raporttien näyttäminen|Raporttien luominen|Raporttien jakaminen|Raporttien päivittäminen| [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukset|
|-------------|--------||
|Power BI, maksuton|![valintamerkki.](media/check.png)|![toinen valintamerkki](media/check.png)|(rajoitettu)|(rajoitettu)||
|Power BI Pro|![vielä yksi valintamerkki.](media/check.png)|![se on valintamerkki](media/check.png)|![jälleen valintamerkki](media/check.png)|(laaja)|![viimeinen valintamerkki](media/check.png)|

Lisätietoja on kohdassa [Power BI -palvelun käyttöoikeuden organisaation käyttäjille](/power-bi/admin/service-admin-licensing-organization) tai [Rekisteröityminen Power BI -palveluun henkilönä](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-or-odata-web-services"></a><a name="expose-data-through-api-or-odata-web-services"></a><a name="exposedata"></a>Tietojen näyttäminen ohjelmointirajapinnan tai OData-verkkopalvelujen kautta

Business Central tarjoaa kaksi tapaa näyttää tiedot, joita Power BI -raportit voivat käyttää: API-sivut tai -kyselyt ja OData (Open Data Protocol) -verkkopalvelut.

### <a name="api-pages-and-queries"></a><a name="api-pages-and-queries"></a>API-sivut ja -kyselyt

> **KOHDE:** vain Business Central online

Kehittäjät voivat määrittää sivuobjekteja ja kyselyobjekteja, joiden tyyppi on *API*. Tällä tavalla he voivat näyttää tietoja tietokantataulukoista webhook-tuetun, OData v4 -yhteensopivan REST-palvelun avulla. Tämäntyyppisiä tietoja ei voi näyttää käyttöliittymässä, vaan ne on tarkoitettu luotettavien integrointipalveluiden rakentamiseen.

Business Central online sisältää useita sisäänrakennettuja ohjelmointirajapintoja, joiden avulla voit saada tietoja yleisimmistä liiketoimintaentiteeteistä, kuten asiakkaista, nimikkeistä ja myyntitilauksista. Näiden ohjelmointirajapintojen käyttö raporttien tietolähteenä ei edellytä lisätyötä tai Power BI -asetuksia. Lisätietoja näistä ohjelmointirajapinnoista on kohdassa [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online tukee myös mukautettuja ohjelmointirajapintoja. Business Central -ratkaisujen sovelluskehittäjät voivat luoda omia API-sivujaan ja -kyselyjään ja pakata ne sovelluksiksi. Sitten sovellukset asennetaan vuokraajaan. Kun asennus on valmis, voit käyttää API-sivuja Power BI -raporteissasi, kuten tekisit sisäänrakennettujen ohjelmointirajapintojenkin (v2.0) kanssa. Lisätietoja API:n luomisesta näyttämällä sivuja tai kyselyjä on kohdassa [Mukautetun ohjelmointirajapinnan kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Helmikuusta 2022 alkaen [!INCLUDE[prod_short](includes/prod_short.md)] Onlinen Power BI -raporttien lähteenä käytetään suorituskykysyistä toissijaista vain luku -tilassa olevaa tietokantareplikaa. Tämän seurauksena AL-kehittäjien pitäisi välttää sellaisten ohjelmointirajapintasivujen kehittämistä, jotka muokkaavat tietokantoja, kun sivut avautuvat tai lataavat tietueita. Erityistä huomiota kannattaa kiinnittää AL-käynnistinten OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord ja OnAfterGetCurrRecord koodiin. Nämä tietokantamuutokset voivat joissakin tapaukissa aiheuttaa suorituskykyongelmia ja estää raporttia päivittämästä tietoja. Lisätietoja on Business Centralin kehityssisällön kohdassa [Kehittäjien suorituskykyartikkelit](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services).
>
> Joissakin harvoissa tapauksissa tämä toiminta aiheuttaa virheen, kun käyttäjä yrittää noutaa tietoja ohjelmointirajapinnasta Power BI Desktop -raporttia varten. Jos tietokantamuutokset kuitenkin ovat tarpeen muokatulla ohjelmointirajapinnalla, Power BI Desktopin käyttäjät voivat pakottaa tämän toimintatavan. Lisätietoja: [Power BI -raporttien kokoaminen näyttämään Business Central -tietoja](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a><a name="odata-web-services"></a>OData-verkkopalvelut

Voit julkaista Business Central -sovellusobjekteja kuten koodiyksikköjä, sivuja ja kyselyitä [OData-verkkopalveluina](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Business Central onlinessa on oletusarvoisesti julkaistu monia verkkopalveluita. Verkkopalveluja voi etsiä kätevästi hakemalla *verkkopalveluja* [!INCLUDE[prod_short](includes/prod_short.md)]issa. Varmista **Verkkopalvelut**-sivulla, että **Julkaisu**-kenttä on valittuna edellä mainituissa verkkopalveluissa. Lisätietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

Lisätietoja tavoista, joilla voidaan verkkopalvelujen paras mahdollinen suorituskyky sekä Business Central Serverin (päätepiste) että kuluttajan (asiakasohjelma) kannalta, on kohdassa [Tehokkaiden verkkopalvelujen kirjoittaminen](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a><a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>API-sivujen tai OData-verkkopalvelujen valitseminen

Aina kun mahdollista, suositellaan käyttämään API-sivuja OData-verkkopalvelun sijaan. Yleensä API-sivut lataavat tiedot nopeammin Power BI -raportteihin kuin OData-verkkopalvelut. Lisäksi ne ovat joustavampia, koska niiden avulla voit saada tietoja taulukon kentistä, joita ei ole määritetty sivuobjektissa.

## <a name="set-up--on-premises-for-power-bi-integration"></a><a name="set-up--on-premises-for-power-bi-integration"></a><a name="setup"></a>Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version Power BI -integroinnin valmistelu

Tässä osassa käsitellään paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -käyttöönoton edellytyksiä Power BI -integrointia varten.

1. Määritä joko NavUserPassword tai Azure Active Directory -todennus käyttöönottoa varten.  
    
    > [!NOTE]
    > Power BI -integrointi ei tue Windows-todennusta eikä sitä tueta Windows-asiakasohjelmassa.

2. Ota OData-verkkopalvelut ja ODataV4-päätepiste käyttöön.

    OData-verkkopalvelu on otettava käyttöön [!INCLUDE[server](includes/server.md)]issä ja OData-portti avattava palomuurissa. Lisätietoja on kohdassa [Business Central Serverin määrittäminen – OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Internet-yhteys on voitava muodostaa paikalliseen palvelimeen.

3. Anna [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjätileille verkkopalvelun käyttöoikeusavain.

    Verkkopalvelun käyttöoikeusavain tarvitaan vain [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen tarkastelemiseen Power BI:ssa. Verkkopalvelun käyttöoikeusavain voidaan määrittää kullekin käyttäjätilille. Vaihtoehtoisesti voidaan luoda tietty tili, jonka verkkopalvelun käyttöoikeusavainta kaikki käyttäjät voivat käyttää. Lisätietoja on kohdassa [Verkkopalvelujen todennus](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

4. Luo sovelluksen rekisteröinti [!INCLUDE[prod_short](includes/prod_short.md)]ille Microsoft Azuressa.

    [!INCLUDE[prod_short](includes/prod_short.md)] -sivuille upotettujen Power BI -raporttien näyttämistä varten sovellus on rekisteröitävä [!INCLUDE[prod_short](includes/prod_short.md)]ia varten Microsoft Azuressa. Rekisteröity sovellus tarvitsee Power BI -palvelujen käyttöoikeuden. Sovellus vaatii vähintään **User.ReadWrite.All**-käyttöoikeuden. Jotta käyttäjät voivat tarkastella raportteja jaetuissa Power BI -työtiloissa, sovellus tarvitsee **Workspace.Read.All**-käyttöoikeuden. Lisätietoja on kohdassa [Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version rekisteröinti Azure AD:ssä muiden palvelujen integrointia varten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Jos käyttöönotto käyttää NavUserPassword-todennusta, [!INCLUDE[prod_short](includes/prod_short.md)] muodostaa yhteyden samaan Power BI -palveluun kaikilla käyttäjillä. Tämä palvelu määritetään sovelluksen rekisteröinnin yhteydessä. Azure AD -todennuksessa [!INCLUDE[prod_short](includes/prod_short.md)] muodostaa yhteyden yksittäisiin käyttäjätileihin liitettyyn Power BI -palveluun.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Luo ensimmäinen yhteys Business Centralista Power BI -palveluun.

    Ennen kuin loppukäyttäjät voivat käyttää Power BI:tä [!INCLUDE[prod_short](includes/prod_short.md)]issa, Azure-sovelluksen järjestelmänvalvojan täytyy antaa suostumuksensa Power BI-palvelulle.

    Voit muodostaa ensimmäisen yhteyden avaamalla [!INCLUDE[prod_short](includes/prod_short.md)]in ja suorittamalla aloitussivulla **Aloita Power BI:n käyttö** -toiminnon. Tämä toiminto opastaa hyväksyntäprosessin läpi ja tarkistaa Power BI -käyttöoikeutesi. Ohjelma pyytää kirjautumaan sisään käyttämällä Azuren järjestelmänvalvojatiliä. Lisätietoja on kohdassa [Power BI -yhteyden muodostaminen – kerran](across-working-with-powerbi.md#connect).


## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a>Katso myös

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
