---
title: Business Centralin hallintatehtävät
description: Joitakin Business Central -sovelluksen tehtäviä on hallittava ja määritettävä keskitetysti. Katso lisätietoja näistä tehtävistä ja niiden määrittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: 959a56e4bb7fcaac57b05d30dca4939ed2f8576d
ms.sourcegitcommit: e904da8dc45e41cdd1434111c15e2a9d9edd3fa2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2021
ms.locfileid: "6660129"
---
# <a name="administration"></a>Hallinta

Yleensä yksi rooli hoitaa yrityksen keskitetyt hallintatehtävät. Tehtävien laajuus voi määräytyä yrityksen koon ja järjestelmänvalvojan vastuualueiden mukaan. Tehtäviin voi sisältyä esimerkiksi työ- ja sähköpostijonojen tietokantasynkronoinnin hallintaa, käyttäjien määritystä ja käyttöliittymän mukautusta.  

Uuden liiketoimintaohjelmiston toimivuuden vuoksi on tärkeää, että annettavat asetusarvot ovat oikein heti alusta alkaen. [!INCLUDE[prod_short](includes/prod_short.md)]issa on useita asetusoppaita, jotka helpottavat perustietojen määrittämistä. Lisätietoja on kohdassa [Business Central -sovelluksen määrittäminen](setup.md).

> [!NOTE]
> Voit määrittää uuden yrityksen [!INCLUDE[prod_short](includes/prod_short.md)]issa RapidStart Servicesin avulla. RapidStart Services on työkalu, joka on suunniteltu lyhentämään käyttöönottoa, parantamaan toteutuksen laatua, esittelemään toistettavia lähestymistapoja toteutuksiin sekä lisäämään tuottavuutta automatisoimalla ja yksinkertaistamalla toistuvia tehtäviä. Lisätietoja on kohdassa [Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md).

Riippumatta siitä, käytätkö RapidStart Servicesia ottamaan käyttöön arvoja vai annatko ne manuaalisesti uudelle yritykselle, voit tukea määrityspäätöksiäsi tietyissä sellaisissa määrityskentissä joillain yleisillä suosituksilla, joiden tiedetään aiheuttavan mahdollisesti heikentävän ratkaisun suorituskykyä, jos kenttä määritetään väärin.  

Pääkäyttäjä tai järjestelmänvalvoja voi määrittää tietojen vaihtamiskehyksen, jonka avulla käyttäjät voivat viedä ja tuoda pankki- ja palkanlaskentatiedostojen tietoja esimerkiksi erilaisia kassanhallintaprosesseja varten. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|
|Määritä, ketkä voivat kirjautua sisään [!INCLUDE[prod_short](includes/prod_short.md)]een luomalla käyttäjiä Microsoft 365 -hallintakeskuksessa tuotteen käyttöoikeuksien mukaan.|[Luo käyttäjät käyttöoikeuksien mukaan](ui-how-users-permissions.md)|
|Määritä käyttöoikeuksia käyttäjille, muokata käyttöoikeusjoukkoja ja ryhmitä käyttäjiä käyttöoikeuksien helppoa hallintaa varten.|[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-how-users-permissions.md)|
|Lisää käyttäjiä, hallitse tietojen käyttöoikeuksia ja määritä rooleja.|[Profiilien hallinta](admin-users-profiles-roles.md)|
|Käyttäjäasetusten, kuten yrityksen, roolin, kielen, alueen tai aikavyöhykkeen, hallinta.|[Käyttäjän asetukset](admin-manage-user-settings-preferences.md)|
|Määritä tulostimet ja tulostettavat raportit.|[Tulostimien määrittäminen](ui-specify-printer-selection-reports.md)|
|Luokittele kenttien luottamukselliset tiedot niin, että voit vastata tietojen kohteiden henkilökohtaisia tietoja koskeviin pyyntöihin.|[Tietojen luottamuksellisuuden luokitteleminen](admin-classifying-data-sensitivity.md)|
|Vastaa tietojen kohteiden henkilökohtaisia tietoja koskeviin pyyntöihin.|[Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen](admin-responding-to-requests-about-personal-data.md)|
|Uuden liiketoimintayksikön määrittäminen mallien avulla|[Uusien yritysten luominen](about-new-company.md)|
|Seuraa kaikkia suoria muutoksia, joita käyttäjät tekevät tietokannan tietoihin. Muutoksia seuraamalla voidaan tunnistaa virheiden alkuperä ja tietojen muutokset.|[Muutosten kirjaaminen lokiin](across-log-changes.md)|  
|Määritä yksittäisiä tai toistuvia pyyntöjä raporttien tai codeunitien suorittamista varten.|[Työjonojen käyttäminen tehtävien aikatauluttamiseen](admin-job-queues-schedule-tasks.md)|  
|Asiakirjojen hallinta, poistaminen ja pakkaaminen|[Asiakirjojen poistaminen](admin-manage-documents.md)|  
|Näytä sivuja, codeuniteja ja kyselyitä verkkopalveluina.|[Verkkopalvelun julkaiseminen](across-how-publish-web-service.md)|
|Kun luot Connect appsia [!INCLUDE[prod_short](includes/prod_short.md)]:n ja kolmannen osapuolen ratkaisun välille REST API:a käyttäen, määritä mallit, joita käytetään täyttämään entiteetin tyhjät ominaisuudet luodessasi POST-toiminnon API:n kautta.|[API-mallien määritys](admin-configuring-api-template.md)|
|Salaa [!INCLUDE[prod_short](includes/prod_short.md)] Serverin tietoja luomalla uusia tai tuomalla olemassa olevia salausavaimia, jotka voi ottaa käyttöön palvelimessa.|[Tietojen salauksen hallinta](admin-manage-data-encryption.md)|
|Dynamics 365 Salesin yhdistäminen [!INCLUDE[prod_short](includes/prod_short.md)]iin, mikä mahdollistaa asiakassuhteiden ja tilausten käsittelyn saumattoman integroinnin liidistä tuottoon -prosessissa.|[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Vaihda käyttöliittymässä näytettävät kentät ja toiminnot vastaamaan yrityksen liiketoimintaprosesseja ja laajenna ratkaisua sovelluksilla.|[[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen mukauttaminen](ui-customizing-overview.md)|

## <a name="administration-in-the-admin-center"></a>Hallinta hallintakeskuksessa

Sisäiset ja delegoidut järjestelmänvalvojat voivat käyttää [!INCLUDE [prod_short](includes/prod_short.md)] -hallintakeskusta, jossa he voivat määrittää ja valvoa [!INCLUDE [prod_short](includes/prod_short.md)] -ympäristöjä ja tehdä vianmääritystä. Seuraavassa taulukossa on kuvataan tärkeimpiä tehtäviä ja siinä on linkit tehtäviä kuvaaviin artikkeleihin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|
|Lue lisää käytettävissä olevista työkaluista, jotka auttavat vianmäärityksessä.|[Tekninen tuki](/dynamics365/business-central/dev-itpro/technical-support)|
|Seuraa käyttöä ja tee istuntojen vianmäärityksiä|[Ympäristön telemetria Business Centralin hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Käyttäjäistuntojen hallinta, mukaan lukien istunnon peruuttaminen, jos käyttäjä on estetty.|[Istuntojen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|
|Määritä vuokraaja lähettämään telemetriatiedot Azureen Application Insightsin analyysin ja vianmäärityksen parantamiseksi.|[Ota käyttöön telemetrian lähettäminen Application Insightsiin](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Liiketoiminnan toiminnallisuus](across-business-functionality.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]