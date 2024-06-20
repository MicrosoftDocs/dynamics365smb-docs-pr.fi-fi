---
title: Johdatus Business Centraliin ja Power BIhin
description: 'Power BI:n yleiskatsaus merkityksellisten tietojen ja tunnuslukujen hakemiseen Business Central -tiedoista.'
author: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 04/24/2024
ms.author: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-business-central-and-power-bi"></a>Johdatus Business Centraliin ja Power BIhin

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE[prod_short](includes/prod_short.md)] -tiedoista saa kätevästi merkityksellisiä tietoja Microsoftin tietojen visualisointiin käytetyn [Power BI:n](https://powerbi.microsoft.com). Power BI noutamista [!INCLUDE[prod_short](includes/prod_short.md)] -tiedoista voidaan muodostaa tietoihin perustuvia koontinäyttöjä ja raportteja. Power BI on joustava vaihtoehto [!INCLUDE[prod_short](includes/prod_short.md)]in raporteille, sillä sen avulla voi porautua tietoja ja mukauttaa visualisointia sekä jopa yhdistää tietoja [!INCLUDE[prod_short](includes/prod_short.md)]in eri yrityksistä. Jotkin Power BI -raportit voidaan myös upottaa Business Centraliin, jossa niitä voidaan tarkastella järjestelmästä poistumatta. Monimutkaisia koontinäyttöjä kannattaa kuitenkin tarkastella Power BI -sivustossa.

![Power BI ja Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-business-central"></a>Power BI:n ja Business Centralin käyttötapoja

[!INCLUDE[prod_short](includes/prod_short.md)]in ja Power BI:n käyttöä varten on erilaisia ominaisuuksia. Joitakin toimintoja voi tehdä Power BI:ssa, kun taas joitakin tehdään [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisäksi osa ominaisuuksista on käytössä vain [!INCLUDE[prod_short](includes/prod_short.md)] online -versiossa mutta ei paikallisessa versiossa. Seuraavassa taulukossa on ominaisuuksien yleiskuva.

|Ominaisuus|Kuvaus|Online|Paikallinen|Lisätietoja|
|-------|-----------|--------------|-----------|----------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] -tietojen näyttäminen Power BI:ssa|Voit tarkastella [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja Power BI -raporteissa. [!INCLUDE[prod_short](includes/prod_short.md)] online sisältää muutamia esimääritettyjä Power BI -raportteja. Organisaatiolla voi lisäksi olla joitakin valmiita mukautettuja raportteja.|![Toimii verkossa.](media/check.png)|![Toimii paikallisesti](media/check.png)|[Täällä...](across-working-with-powerbi.md)|
|Power BI -raporttien näyttäminen [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmassa.| [!INCLUDE[prod_short](includes/prod_short.md)] -tietoja näyttävät Power BI -raportit voidaan upottaa suoraan osien [!INCLUDE[prod_short](includes/prod_short.md)] -sivuille. Osan voi vaihtaa näyttämään minkä tahansa käytettävissä olevan raportin. |![toimii verkossa.](media/check.png)|![Toimii paikallisesti](media/check.png)<sup>[*](#onprem)</sup>|[Täällä...](across-working-with-powerbi.md).|
|Voit luoda Power BI:ssa raportteja ja koontinäyttöjä, joissa näytetään [!INCLUDE[prod_short](includes/prod_short.md)] -tietoja.|Voit luoda omia raportteja ja koontinäyttöjä Power BI Desktopissa. Voit julkaista raportit omaan Power BI -palveluun tai jakaa ne muiden kanssa organisaatiossa.|![Toimii verkossa.](media/check.png)|![toimii paikallisesti](media/check.png)|[Täällä...](across-how-use-financials-data-source-powerbi.md)|
|[!INCLUDE[prod_short](includes/prod_short.md)] -sovellukset Power BI:ssa| [!INCLUDE[prod_short](includes/prod_short.md)] julkaisee Microsoft AppSource kolme Power BI -sovellusta. Nämä sovellukset luovat yksityiskohtaisia raportteja ja koontinäyttöjä Power BI -palvelussa [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen tarkastelua varten. Käytettävissä olevat sovellukset: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Toimii verkossa.](media/check.png)||[Täällä...](across-powerbi-business-central-apps.md)|
|[!INCLUDE [prod_short](includes/prod_short.md)]-tietojen käsitteleminen tietovarastoissa ja tietovoissa|Heinäkuusta 2022 lähtien voit käyttää [!INCLUDE [prod_short](includes/prod_short.md)]-yhdistintä Power Query Onlinessä tietovoiden jakamiseen eri raporttien ja koontinäyttöjen välillä.|![toimii verkossa.](media/check.png)||[Täällä...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a> Tätä ominaisuutta varten tarvitaan Microsoft Azuressa rekisteröity Business Centralin sovellus. Lisätietoja on kohdassa [Paikallisen Business Centralin rekisteröinti Microsoft Entra ID:ssä muiden palvelujen integrointia varten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="get-ready-to-use-power-bi"></a>Power BI:n valmistelu käyttöä varten

Muutama tehtävä on suoritettava, ennen kuin Power BI:ta voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa.<!-- Some of the tasks are typically only done by administrators or super users.--> Tehtävät määräytyvät sen mukaan, mikä roolisi organisaatiossa on ja mitä haluat tehdä Power BI:ssä:

- Jos olet *yrityskäyttäjä*, haluat tarkastella Power BI -raportteja joko Power BI -palvelussa tai Business Centralissa.
- Jos olet *järjestelmänvalvoja*, hallitset koko organisaation asetuksia, jotka hallinnoivat sitä, miten Business Central ja Power BI toimivat.
- Jos olet *raporttien tekijä*, haluat luoda mukautettuja Power BI -raportteja, joita voit jakaa muiden käyttäjien kanssa.

|Tehtävä|Yrityskäyttäjä|Järjestelmänvalvoja|Raportin tekijä|Lisätietoja|
|----|-------------|-------------|-----------------------|----------------|
|Power BI -tilin hankkiminen.|![vielä yksi valintamerkki.](media/check.png)|![se on valintamerkki](media/check.png)|![jälleen valintamerkki](media/check.png)|Siirry kohteeseen [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa. <br /><br/>Rekisteröitymiseen tarvitaan käyttöoikeus, mutta useimmissa tapauksissa käytössä on jo maksuton käyttöoikeus. Lisätietoja on kohdassa [Power BI -käyttöoikeudet](admin-powerbi-setup.md#license).|
|Hanki Power BI Desktop|||![jälleen valintamerkki.](media/check.png)|Lataa osoitteesta [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Lisätietoja on kohdassa [Power BI Desktopin hankkiminen](/power-bi/fundamentals/desktop-get-the-desktop).
|Business Central -tietojen julkaiseminen Power BI:hin||![se on valintamerkki.](media/check.png)|![jälleen valintamerkki](media/check.png)|[Tietojen näyttäminen API-sivujen tai OData-verkkopalvelujen kautta](admin-powerbi-setup.md#exposedata)
|Ota Power BI -integrointi käyttöön<br />(vain paikallinen)||![se on valintamerkki.](media/check.png)||[Määritä paikallinen Business Central Power BI -integraatiota varten](across-working-with-business-central-in-powerbi.md#setup)|


## <a name="next-steps"></a>Seuraavat vaiheet

- Jos olet järjestelmänvalvoja, joka täytyy määrittää Power BI [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan, siirry kohtaan [Power BI -integroinnin käyttöönotto](admin-powerbi-setup.md).
- Jos Power BI on jo määritetty ja haluat kokeilla ominaisuuksia, siirry kohtaan [Power BI -raporttien käsitteleminen Business Centralissa](across-working-with-powerbi.md).

## <a name="see-also"></a>Katso myös

[Analytiikan yleiskatsaus](reports-bi-reporting.md)   
[KPI:iden seuraaminen Power BI -mittareiden avulla](track-kpis-with-power-bi-metrics.md)   
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Automatessa](across-how-use-financials-data-source-flow.md)  
[Power BI -dokumentaatio](/power-bi/)  
[Power BIn kuvaus](/power-bi/fundamentals/power-bi-overview)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  
[Johdatus tietovarastoihin](/power-bi/transform-model/datamarts/datamarts-overview)  
[Tietovoiden ja itsepalvelutietojen valmistelun esittely](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
