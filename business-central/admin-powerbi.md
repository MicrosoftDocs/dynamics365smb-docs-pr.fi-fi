---
title: Tietoja Business Centralista ja Power BI:sta | Microsoft Docs
description: Power BI:n yleiskatsaus merkityksellisten tietojen, liiketoimintatietojen ja tunnuslukujen hakemiseen Business Central -tiedoista.
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
ms.openlocfilehash: 9768fca2bea274a8124c34e151d399baa23f9f03
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493115"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] ja Power BI

[!INCLUDE[prod_short](includes/prod_short.md)] -tiedoista saa kätevästi merkityksellisiä tietoja Microsoftin tietojen visualisointiin käytetyn [Power BI:n](https://powerbi.microsoft.com). Power BI noutamista [!INCLUDE[prod_short](includes/prod_short.md)] -tiedoista voidaan muodostaa tietoihin perustuvia koontinäyttöjä ja raportteja. Power BI on joustava vaihtoehto [!INCLUDE[prod_short](includes/prod_short.md)]in raporteille, sillä sen avulla voi porautua tietoja ja mukauttaa visualisointia sekä jopa yhdistää tietoja [!INCLUDE[prod_short](includes/prod_short.md)]in eri yrityksistä. Jotkin Power BI -raportit voidaan myös upottaa Business Centraliin, jossa niitä voidaan tarkastella järjestelmästä poistumatta. Monimutkaisia koontinäyttöjä kannattaa kuitenkin tarkastella Power BI -sivustossa.

![Power BI ja Business Central](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Power BI:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in käyttötapoja

[!INCLUDE[prod_short](includes/prod_short.md)]in ja Power BI:n käyttöä varten on erilaisia ominaisuuksia. Joitakin toimintoja voi tehdä Power BI:ssa, kun taas joitakin tehdään [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisäksi osa ominaisuuksista on käytössä vain [!INCLUDE[prod_short](includes/prod_short.md)] online -versiossa mutta ei paikallisessa versiossa. Seuraavassa taulukossa on ominaisuuksien yleiskuva.

|Ominaisuus|Kuvaus|Online|Paikallinen|Lisätietoja|
|-------|-----------|--------------|-----------|----------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] -tietojen näyttäminen Power BI:ssa|Voit tarkastella [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja Power BI -raporteissa. [!INCLUDE[prod_short](includes/prod_short.md)] online sisältää muutamia esimääritettyjä Power BI -raportteja. Organisaatiolla voi lisäksi olla joitakin valmiita mukautettuja raportteja.|![Toimii verkossa](media/check.png)|![Toimii paikallisesti](media/check.png)|[Katso...](across-working-with-business-central-in-powerbi.md)|
|Power BI -raporttien näyttäminen [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmassa.| [!INCLUDE[prod_short](includes/prod_short.md)] -tietoja näyttävät Power BI -raportit voidaan upottaa suoraan osien [!INCLUDE[prod_short](includes/prod_short.md)] -sivuille. Osan voi vaihtaa näyttämään minkä tahansa käytettävissä olevan raportin. |![toimii verkossa](media/check.png)|![Toimii paikallisesti](media/check.png)<sup>[*](#onprem)</sup>|[Katso...](across-working-with-powerbi.md).|
|Voit luoda Power BI:ssa raportteja ja koontinäyttöjä, joissa näytetään [!INCLUDE[prod_short](includes/prod_short.md)] -tietoja.|Voit luoda omia raportteja ja koontinäyttöjä Power BI Desktopissa. Voit julkaista raportit omaan Power BI -palveluun tai jakaa ne muiden kanssa organisaatiossa.|![Toimii verkossa](media/check.png)|![toimii paikallisesti](media/check.png)|[Katso...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)] -sovellukset Power BI:ssa| [!INCLUDE[prod_short](includes/prod_short.md)] julkaisee Microsoft AppSource kolme Power BI -sovellusta. Nämä sovellukset luovat yksityiskohtaisia raportteja ja koontinäyttöjä Power BI -palvelussa [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen tarkastelua varten. Käytettävissä olevat sovellukset: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Toimii verkossa](media/check.png)||[Katso...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Tätä ominaisuutta varten tarvitaan Microsoft Azuressa rekisteröity Business Centralin sovellus. Lisätietoja on kohdassa [Paikallisen Business Centralin rekisteröinti Azure AD:ssä muiden palvelujen integrointia varten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Power BI:n valmistelu käyttöä varten

Muutama tehtävä on suoritettava, ennen kuin Power BI:ta voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa. Osan tehtävistä tekee yleensä vain järjestelmänvalvoja tai super-käyttäjä.

1. Jos käytössä on paikallinen [!INCLUDE[prod_short](includes/prod_short.md)], varmista, että käyttöönotto vastaa vaatimuksia, jotka on käsitelty kohdassa [Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version määrittäminen Power BI -integraatiota varten](admin-powerbi-setup.md#setup). Tämä on yleensä järjestelmänvalvojan tehtävä.

2. Tietojen julkaisu verkkopalveluina.

    Codeunitit, sivut ja kyselyt, joita halutaan käyttää Power BI -raporttien tietolähteenä, on julkaistava verkkopalveluina. Useita verkkopalveluja julkaistaan oletusarvoisesti. Verkkopalveluja voi etsiä kätevästi hakemalla *verkkopalveluja* [!INCLUDE[prod_short](includes/prod_short.md)]issa.

    Lisätietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

3. Power BI -tilin hankkiminen.

    Power BI:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in yhteiskäyttöön tarvitaan Power BI -palvelutili riippumatta siitä, onko kyse järjestelmänvalvojasta vai kuluttajasta. Tilin voi hankkia siirtymällä sivustoon [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa. Rekisteröitymiseen tarvitaan käyttöoikeus, mutta useimmissa tapauksissa käytössä on jo maksuton käyttöoikeus. Lisätietoja on kohdassa [Power BI:n käyttöoikeudet](admin-powerbi-setup.md#license).

4. Jos haluat luoda omia Power BI -raportteja, hanki Power BI Desktop.

    Voit ladata [Power BI Desktopin](https://powerbi.microsoft.com/desktop/). Lisätietoja on kohdassa [Power BI Desktopin hankkiminen](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

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


[!INCLUDE[footer-include](includes/footer-banner.md)]