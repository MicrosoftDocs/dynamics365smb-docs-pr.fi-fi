---
title: Business Central -tietojen käyttäminen Power BI:ssa | Microsoft Docs
description: Merkityksellisten tietojen, liiketoimintatietoja ja tunnuslukujen saaminen Business Central -tiedoista Power BI:n avulla.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 07/10/2020
ms.author: jswymer
ms.openlocfilehash: bdcbcb0fa82d799e29cfcdbb034e231635510656
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697756"
---
# <a name="working-with-prodshort-data-in-power-bi"></a>[!INCLUDE [prodshort](includes/prodshort.md)] -tietojen käyttäminen Power BI:ssa

Tässä artikkelissa on perustietoja niistä Power BI:n raporteista ja koontinäytöistä, jotka käyttävät [!INCLUDE [prodshort](includes/prodshort.md)]ia tietolähteenä. Artikkelissa käsitellään seikkoja, jotka helpottavat [!INCLUDE[prodshort](includes/prodshort.md)] -käytön aloittamista käyttäjänä. Yleistä opastusta ja ohjeita Power BI:n käytöstä on kohdassa [Power BI:n kuluttajille suunnattu dokumentaatio](https://review.docs.microsoft.com/en-us/power-bi/consumer).

## <a name="get-ready"></a>Valmistelut

Rekisteröidy Power BI -palveluun. Jos et ole vielä rekisteröitynyt, siirry osoitteeseen [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa.

## <a name="get-started"></a>Aloitus

Kun olet saanut Power BI -tilin, voit kirjautua osoitteessa [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Power BI -palvelu on kaikkien käytettävissä olevien raporttien isäntä. Saat raportin näkyviin valitsemalla **Oma työtila** > **Raportit**. Valitse sitten raportti, jota haluat tarkastella.

[!INCLUDE[prodshort](includes/prodshort.md)] online -versiossa työtilassa on automaattisesti joukko oletusraportteja. Jos haluat luoda omia raportteja, voit tehdä sen Power BI Desktopissa ja julkaista luodut raportit sitten työtilaan. Lisätietoja on kohdassa [[!INCLUDE [prodlong](includes/prodlong.md)] -tiedot näyttävien raporttien luonnin muodostamisen aloittaminen Power BI Desktopissa](across-how-use-financials-data-source-powerbi.md).

Jos käytössä on paikallinen [!INCLUDE[prodshort](includes/prodshort.md)], raporttien luonti on aloitettava alusta Power BI Desktopissa. Vaihtoehtoiesti Power BI -raportit voidaan jakaa palvelimeen ladattavina tiedostoina.

## <a name="get-the-latest-data"></a>Viimeisten tietojen hakeminen

Kukin Power BI -raportti perustuu tietojoukkoon, joka saa tietoja [!INCLUDE[prodshort](includes/prodshort.md)] -lähteistä. Power BI -raporttien tietojen halutaan olevan aina ajantasaisia [!INCLUDE[prodshort](includes/prodshort.md)] -tietojen kanssa. Tätä kutsutaan *päivittämiseksi*.  Sen perusteella, miten organisaatio on määrittänyt Power BI:n, päivitystä ei välttämättä tehdä automaattisesti. Tiedot voidaan päivittää kahdella tavalla: manuaalisesti tai ajoitetulla päivityksellä. Manuaalinen päivitys tehdään tarvittaessa. Ajoitetussa päivityksessä tiedot päivitetään automaattisesti määritetyn ajan kuluttua.

### <a name="refresh-manually"></a>Manuaalinen päivitys

Valitse siirtymisruudussa **Tietojoukot**-kohdassa tietojoukon vieressä **Lisää vaihtoehtoja (...)** ja valitse sitten **Päivitä nyt**.

### <a name="schedule-a-refresh"></a>Päivityksen ajoittaminen

Valitse siirtymisruudussa Tietojoukot-kohdassa tietojoukon vieressä Lisää vaihtoehtoja (...) ja valitse sitten **Ajoita päivitys**. Täytä **Ajoita päivitys** -osan tiedot ja valitse **Käytä**.

Lisätietoja on kohdassa [Aikataulutetun päivityksen määrittäminen](/power-bi/connect-data/refresh-scheduled-refresh)

## <a name="upload-reports-from-files"></a><a name="upload"></a>Raporttien lataaminen tiedostoista

Power BI -raportteja voi jakaa käyttäjille .pbix-tiedostoina. .pbix-tiedoston voi puolestaan ladata työtilaan. Raportti ladataan seuraavasti:

1. Valitse uudessa työtilassa **Nouda tiedot**.

2. Valitse Tiedostot-ruudussa **Hae**.

3. Valitse **Paikallinen tiedosto**, siirry tiedoston tallennussijaintiin ja valitse **Avaa**.

Lisätietoja on kohdassa [Raportin lataaminen palveluun](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Raportin lataamista varten tarvitaan [Premium-kapasiteetin](/power-bi/service-premium-what-is) työtila. Lisätietoja on kohdassa [Premium-kapasiteetin hallinta](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> Jos käytössä on [!INCLUDE[prodshort](includes/prodshort.md)] online, raportin voi ladata myös [!INCLUDE[prodshort](includes/prodshort.md)]issa. Lisätietoja on kohdassa [Power BI -raporttien käyttäminen [!INCLUDE [prodshort](includes/prodshort.md)]issa – raporttien lataaminen palvelimeen](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Raporttien jakaminen muiden kanssa

Kun raportti on työtilassa, sen voi jakaa organisaatiossa muiden kanssa.

Voit jakaa raportin valitsemalla raporttiluettelossa tai avoimessa raportissa **Jaa**. Anna **Jaa raportti** -ruudussa niiden henkilöiden tai jakeluryhmien täydellinen sähköpostiosoite, joiden kanssa haluat jakaa raportin. Suorita jakaminen loppuun näytön ohjeiden mukaisesti. Lisätietoja on kohdassa [Koontinäytön tai raportin jakaminen](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Sekä sinulla että henkilöillä, joiden kanssa jaat raportin, on oltava [Power BI Pro -käyttöoikeus](/power-bi/service-features-license-type). Sisällön on oltava työtilassa [Premium-kapasiteettina](/power-bi/service-premium-what-is). Lisätietoja on kohdassa [Työn jakaminen Power BI:ssä](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Business Central ja Power BI](admin-powerbi.md)  
[Power BI -raporttien luominen näyttämään [!INCLUDE [prodlong](includes/prodlong.md)] -tietoja](across-how-use-financials-data-source-powerbi.md)  
[Power BI:n -integrointiosa ja [!INCLUDE[prodshort](includes/prodshort.md)] -arkkitehtuurin yleiskatsaus](admin-powerbi-overview.md)  
[Power BI -raporttien käyttäminen [!INCLUDE [prodshort](includes/prodshort.md)]issa](across-working-with-powerbi.md)  
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
