---
title: Tietoja Business Centralista ja Power BI:sta | Microsoft Docs
description: Analyysitietojen, liiketoimintatietojen ja tunnuslukujen hakeminen Business Centralin tiedoista on helppoa Power BI:n Business Central -sovelluksia.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: a1e2e8ceee41c2c6ed517d000fc7c3a4a6aa274c
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697670"
---
# <a name="prodshort-and-power-bi"></a>[!INCLUDE[prodshort](includes/prodshort.md)] ja Power BI

[!INCLUDE[prodshort](includes/prodshort.md)] -tiedoista saa kätevästi merkityksellisiä tietoja Microsoftin tietojen visualisointiin käytetyn [Power BI:n](https://powerbi.microsoft.com). Power BI noutamista [!INCLUDE[prodshort](includes/prodshort.md)] -tiedoista voidaan muodostaa tietoihin perustuvia koontinäyttöjä ja raportteja. Power BI on joustava vaihtoehto [!INCLUDE[prodshort](includes/prodshort.md)]in raporteille, sillä sen avulla voi porautua tietoja ja mukauttaa visualisointia sekä jopa yhdistää tietoja [!INCLUDE[prodshort](includes/prodshort.md)]in eri yrityksistä. Jotkin Power BI -raportit voidaan myös upottaa Business Centraliin, jossa niitä voidaan tarkastella järjestelmästä poistumatta. Monimutkaisia koontinäyttöjä kannattaa kuitenkin tarkastella Power BI -sivustossa.

![Power BI ja Business Central](media/power-bi-intro.png)


## <a name="what-you-can-do-with-power-bi-and-prodshort"></a>Power BI:n ja [!INCLUDE[prodshort](includes/prodshort.md)]in käyttötapoja

[!INCLUDE[prodshort](includes/prodshort.md)]in ja Power BI:n käyttöä varten on erilaisia ominaisuuksia. Joitakin toimintoja voi tehdä Power BI:ssa, kun taas joitakin tehdään [!INCLUDE[prodshort](includes/prodshort.md)]issa. Lisäksi osa ominaisuuksista on käytössä vain [!INCLUDE[prodshort](includes/prodshort.md)] online -versiossa mutta ei paikallisessa versiossa. Seuraavassa taulukossa on ominaisuuksien yleiskuva.

|Ominaisuus|Kuvaus|Online|Paikallinen|Lisätietoja|
|-------|-----------|--------------|-----------|----------------|
|[!INCLUDE[prodshort](includes/prodshort.md)] -tietojen näyttäminen Power BI:ssa|Voit tarkastella [!INCLUDE[prodshort](includes/prodshort.md)]in tietoja Power BI -raporteissa. [!INCLUDE[prodshort](includes/prodshort.md)] online sisältää muutamia esimääritettyjä Power BI -raportteja. Organisaatiolla voi lisäksi olla joitakin valmiita mukautettuja raportteja.|![tarkistus](media/check.png)|![tarkistus](media/check.png)|[Katso...](across-working-with-powerbi.md)|
|Power BI -raporttien näyttäminen [!INCLUDE[prodshort](includes/prodshort.md)] -asiakasohjelmassa.| [!INCLUDE[prodshort](includes/prodshort.md)] -tietoja näyttävät Power BI -raportit voidaan upottaa suoraan osien [!INCLUDE[prodshort](includes/prodshort.md)] -sivuille. Osan voi vaihtaa näyttämään minkä tahansa käytettävissä olevan raportin. |![tarkistus](media/check.png)|![tarkistus](media/check.png)<sup>[*](#onprem)</sup>|[Katso...](across-working-with-business-central-in-powerbi.md).|
|Voit luoda Power BI:ssa raportteja ja koontinäyttöjä, joissa näytetään [!INCLUDE[prodshort](includes/prodshort.md)] -tietoja.|Voit luoda omia raportteja ja koontinäyttöjä Power BI Desktopissa. Voit julkaista raportit omaan Power BI -palveluun tai jakaa ne muiden kanssa organisaatiossa. .|![tarkistus](media/check.png)|![tarkistus](media/check.png)|[Katso...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prodshort](includes/prodshort.md)] -sovellukset Power BI:ssa| [!INCLUDE[prodshort](includes/prodshort.md)] julkaisee Microsoft AppSource kolme Power BI -sovellusta. Nämä sovellukset luovat yksityiskohtaisia raportteja ja koontinäyttöjä Power BI -palvelussa [!INCLUDE[prodshort](includes/prodshort.md)] -tietojen tarkastelua varten. Käytettävissä olevat sovellukset: <ul><li>[!INCLUDE [prodlong](includes/prodlong.md)] – CRM </li><li>[!INCLUDE [prodlong](includes/prodlong.md)] – Finance </li><li>[!INCLUDE [prodlong](includes/prodlong.md)] – Sales </li></ul>  |![tarkistus](media/check.png)||[Katso...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Tätä ominaisuutta varten tarvitaan Microsoft Azuressa rekisteröity Business Centralin sovellus. Lisätietoja on kohdassa [Paikallisen Business Centralin rekisteröinti Azure AD:ssä muiden palvelujen integrointia varten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Power BI:n valmistelu käyttöä varten

Muutama tehtävä on suoritettava, ennen kuin Power BI:ta voi käyttää [!INCLUDE[prodshort](includes/prodshort.md)]in kanssa. Osan tehtävistä tekee yleensä vain järjestelmänvalvoja tai super-käyttäjä.

1. Jos käytössä on paikallinen [!INCLUDE[prodshort](includes/prodshort.md)], varmista, että käyttöönotto vastaa vaatimuksia, jotka on käsitelty kohdassa [Paikallisen [!INCLUDE[prodshort](includes/prodshort.md)] -version määrittäminen Power BI -integraatiota varten](admin-powerbi-setup.md#setup). Tämä on yleensä järjestelmänvalvojan tehtävä.

2. Tietojen julkaisu verkkopalveluina.

    Codeunitit, sivut ja kyselyt, joita halutaan käyttää Power BI -raporttien tietolähteenä, on julkaistava verkkopalveluina. Useita verkkopalveluja julkaistaan oletusarvoisesti. Verkkopalveluja voi etsiä kätevästi hakemalla *verkkopalveluja* [!INCLUDE[prodshort](includes/prodshort.md)]issa.
    
    Lisätietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

3. Power BI -tilin hankkiminen.

    Power BI:n ja [!INCLUDE[prodshort](includes/prodshort.md)]in yhteiskäyttöön tarvitaan Power BI -palvelutili riippumatta siitä, onko kyse järjestelmänvalvojasta vai kuluttajasta. Tilin voi hankkia siirtymällä sivustoon [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa. Rekisteröitymiseen tarvitaan käyttöoikeus, mutta useimmissa tapauksissa käytössä on jo maksuton käyttöoikeus. Lisätietoja on kohdassa [Power BI:n käyttöoikeudet](admin-powerbi-setup.md#license).

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
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power Automate'ssa](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
