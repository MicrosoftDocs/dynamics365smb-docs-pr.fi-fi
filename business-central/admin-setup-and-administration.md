---
title: Business Centralin hallintatehtävät
description: Joitakin Business Central -sovelluksen tehtäviä on hallittava ja määritettävä keskitetysti. Katso lisätietoja näistä tehtävistä ja niiden määrittämisestä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/11/2023
ms.custom: bap-template
---
# <a name="administration-tasks"></a>Hallintatehtävät

Yleensä yksi rooli hoitaa yrityksen keskitetyt hallintatehtävät. Tehtävien laajuus voi määräytyä yrityksen koon ja järjestelmänvalvojan vastuualueiden mukaan. Tehtäviin voi sisältyä esimerkiksi työ- ja sähköpostijonojen tietokantasynkronoinnin hallintaa, käyttäjien määritystä ja käyttöliittymän mukautusta.  

Uuden liiketoimintaohjelmiston toimivuuden vuoksi on tärkeää, että annettavat asetusarvot ovat oikein heti alusta alkaen. [!INCLUDE[prod_short](includes/prod_short.md)]issa on useita asetusoppaita, jotka helpottavat perustietojen määrittämistä. Lisätietoja on kohdassa [Business Central -sovelluksen määrittäminen](setup.md).

> [!NOTE]
> Tiedonsiirtotyökalujen avulla voit siirtää aiemmin luodut tiedot [!INCLUDE [prod_short](includes/prod_short.md)] -online-käyttöön. Vaihtoehtoisesti voit määrittää uuden yrityksen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa määrityspakettien avulla lyhentääksesi käyttöönottoa, parantaaksesi toteutuksen laatua, esittelläksesi toistettavia lähestymistapoja toteutuksiin sekä lisätäksesi tuottavuutta automatisoimalla ja yksinkertaistamalla toistuvia tehtäviä. Lisätietoja hallintasisällössä: [Paikallisten tietojen siirtäminen Business Central Onlineen](/dynamics365/business-central/dev-itpro/administration/migrate-data).

Voit tukea määritysten suhteen tekemiäsi päätöksiä joillakin valittujen määrityskenttien suosituksilla, joiden tiedetään mahdollisesti aiheuttavan sen, että ratkaisu on tehoton, jos se määritetään virheellisesti.  

Pääkäyttäjä tai järjestelmänvalvoja voi määrittää tietojen vaihtamiskehyksen, jonka avulla käyttäjät voivat viedä ja tuoda pankki- ja palkanlaskentatiedostojen tietoja esimerkiksi erilaisia kassanhallintaprosesseja varten. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|
|Määritä, ketkä voivat kirjautua sisään [!INCLUDE[prod_short](includes/prod_short.md)]:een luomalla käyttäjiä Microsoft 365 -hallintakeskuksessa tuotteen käyttöoikeuksien mukaan.|[Luo käyttäjät käyttöoikeuksien mukaan](ui-how-users-permissions.md)|
|Määritä käyttöoikeuksia käyttäjille, muokata käyttöoikeusjoukkoja ja ryhmitä käyttäjiä käyttöoikeuksien helppoa hallintaa varten.|[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-how-users-permissions.md)|
|Lisää käyttäjiä, hallitse tietojen käyttöoikeuksia ja määritä rooleja.|[Profiilien hallinta](admin-users-profiles-roles.md)|
|Käyttäjäasetusten, kuten yrityksen, roolin, kielen, alueen tai aikavyöhykkeen, hallinta.|[Käyttäjän asetukset](admin-manage-user-settings-preferences.md)|
|Määritä tulostimet ja tulostettavat raportit.|[Tulostimien määrittäminen](ui-specify-printer-selection-reports.md)|
|Luokittele kenttien luottamukselliset tiedot niin, että voit vastata tietojen kohteiden henkilökohtaisia tietoja koskeviin pyyntöihin.|[Tietojen luottamuksellisuuden luokitteleminen](admin-classifying-data-sensitivity.md)|
|Vastaa tietojen kohteiden henkilökohtaisia tietoja koskeviin pyyntöihin.|[Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen](admin-responding-to-requests-about-personal-data.md)|
|Uuden liiketoimintayksikön määrittäminen mallien avulla|[Luo uusia yrityksiä](about-new-company.md)|
|Seuraa kaikkia suoria muutoksia, joita käyttäjät tekevät tietokannan tietoihin. Muutoksia seuraamalla voidaan tunnistaa virheiden alkuperä ja tietojen muutokset.|[Muutosten kirjaaminen lokiin](across-log-changes.md)|  
|Määritä yksittäisiä tai toistuvia pyyntöjä raporttien tai codeunitien suorittamista varten.|[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)|  
|Asiakirjojen hallinta, poistaminen ja pakkaaminen|[Asiakirjojen poistaminen](admin-manage-documents.md)|  
|Näytä sivuja, codeuniteja ja kyselyitä verkkopalveluina.|[Verkkopalvelun julkaiseminen](across-how-publish-web-service.md)|
|Kun luot Connect appsia [!INCLUDE[prod_short](includes/prod_short.md)]:n ja kolmannen osapuolen ratkaisun välille REST API:a käyttäen, määritä mallit, joita käytetään täyttämään entiteetin tyhjät ominaisuudet luodessasi POST-toiminnon API:n kautta.|[API-mallien määritys](admin-configuring-api-template.md)|
|Salaa [!INCLUDE[prod_short](includes/prod_short.md)] Serverin tietoja luomalla uusia tai tuomalla olemassa olevia salausavaimia, jotka voi ottaa käyttöön palvelimessa.|[Tietojen salauksen hallinta](admin-manage-data-encryption.md)|
|Dynamics 365 Salesin yhdistäminen [!INCLUDE[prod_short](includes/prod_short.md)]iin, mikä mahdollistaa asiakassuhteiden ja tilausten käsittelyn saumattoman integroinnin liidistä tuottoon -prosessissa.|[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Vaihda käyttöliittymässä näytettävät kentät ja toiminnot vastaamaan yrityksen liiketoimintaprosesseja ja laajenna ratkaisua sovelluksilla.|[Mukauta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|

## <a name="administration-in-the-admin-center"></a>Hallinta hallintakeskuksessa

Sisäiset ja delegoidut järjestelmänvalvojat voivat käyttää [!INCLUDE [prod_short](includes/prod_short.md)] -hallintakeskusta, jossa he voivat määrittää ja valvoa [!INCLUDE [prod_short](includes/prod_short.md)] -ympäristöjä ja tehdä vianmääritystä. Seuraavassa taulukossa on kuvataan tärkeimpiä tehtäviä ja siinä on linkit tehtäviä kuvaaviin artikkeleihin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|
|Lue lisää käytettävissä olevista työkaluista, jotka auttavat vianmäärityksessä.|[Tekninen tuki](/dynamics365/business-central/dev-itpro/technical-support)|
|Seuraa käyttöä ja tee istuntojen vianmäärityksiä|[Ympäristön telemetria Business Centralin hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Käyttäjäistuntojen hallinta, mukaan lukien istunnon peruuttaminen, jos käyttäjä on estetty.|[Istuntojen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions)|
|Määritä vuokraaja lähettämään telemetriatiedot Azureen Application Insightsin analyysin ja vianmäärityksen parantamiseksi.|[Ota käyttöön telemetrian lähettäminen Application Insightsiin](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-also"></a>Katso myös

[Yrityksen toiminnot](across-business-functionality.md)  
[Yrityksen yleiset toiminnot](ui-across-business-areas.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
