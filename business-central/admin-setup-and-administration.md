---
title: Business Central -sovelluksen hallintatehtävät | Microsoft Docs
description: Joitakin Business Central -sovelluksen tehtäviä on hallittava ja määritettävä keskitetysti. Katso lisätietoja näistä tehtävistä ja niiden määrittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 3388e30168e6f0da0dfee2b6dcd7e70cb7a62eac
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953561"
---
# <a name="administration"></a>Hallinta
Yleensä yksi rooli hoitaa yrityksen keskitetyt hallintatehtävät. Tehtävien laajuus voi määräytyä yrityksen koon ja järjestelmänvalvojan vastuualueiden mukaan. Tehtäviin voi sisältyä esimerkiksi työ- ja sähköpostijonojen tietokantasynkronoinnin hallintaa, käyttäjien määritystä ja käyttöliittymän mukautusta.  

Uuden liiketoimintaohjelmiston toimivuuden vuoksi on tärkeää, että annettavat asetusarvot ovat oikein heti alusta alkaen. [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on useita asetusoppaita, jotka helpottavat perustietojen määrittämistä. Lisätietoja on kohdassa [Business Central -sovelluksen määrittäminen](setup.md).

Riippumatta siitä, käytätkö RapidStart Servicesia ottamaan käyttöön arvoja vai annatko ne manuaalisesti uudelle yritykselle, voit tukea määrityspäätöksiäsi tietyissä sellaisissa määrityskentissä joillain yleisillä suosituksilla, joiden tiedetään aiheuttavan mahdollisesti heikentävän ratkaisun suorituskykyä, jos kenttä määritetään väärin.  

Pääkäyttäjä tai järjestelmänvalvoja voi määrittää tietojen vaihtamiskehyksen, jonka avulla käyttäjät voivat viedä ja tuoda pankki- ja palkanlaskentatiedostojen tietoja esimerkiksi erilaisia kassanhallintaprosesseja varten.

> [!NOTE]
> Voit määrittää uuden yrityksen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa RapidStart Servicesin avulla. RapidStart Services on työkalu, joka on suunniteltu lyhentämään käyttöönottoa, parantamaan toteutuksen laatua, esittelemään toistettavia lähestymistapoja toteutuksiin sekä lisäämään tuottavuutta automatisoimalla ja yksinkertaistamalla toistuvia tehtäviä. Lisätietoja on kohdassa [Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Määritä, ketkä voivat kirjautua sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]een luomalla käyttäjiä Microsoft 365 -hallintakeskuksessa tuotteen käyttöoikeuksien mukaan.|[Luo käyttäjät käyttöoikeuksien mukaan](ui-how-users-permissions.md)|
|Määritä käyttöoikeuksia käyttäjille, muokata käyttöoikeusjoukkoja ja ryhmitä käyttäjiä käyttöoikeuksien helppoa hallintaa varten.|[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-how-users-permissions.md)|
|Lisää käyttäjiä, hallitse tietojen käyttöoikeuksia ja määritä rooleja.|[Profiilien hallinta](admin-users-profiles-roles.md)|
|Luokittele kenttien luottamukselliset tiedot niin, että voit vastata tietojen kohteiden henkilökohtaisia tietoja koskeviin pyyntöihin.|[Tietojen luottamuksellisuuden luokitteleminen](admin-classifying-data-sensitivity.md)|
|Vastaa tietojen kohteiden henkilökohtaisia tietoja koskeviin pyyntöihin.|[Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen](admin-responding-to-requests-about-personal-data.md)|
|Uuden liiketoimintayksikön määrittäminen mallien avulla|[Uusien yritysten luominen](about-new-company.md)|
|Seuraa kaikkia suoria muutoksia, joita käyttäjät tekevät tietokannan tietoihin. Muutoksia seuraamalla voidaan tunnistaa virheiden alkuperä ja tietojen muutokset.|[Muutosten kirjaaminen lokiin](across-log-changes.md)|  
|Määritä yksittäisiä tai toistuvia pyyntöjä raporttien tai koodiyksiköiden suorittamista varten.|[Työjonojen käyttäminen tehtävien aikatauluttamiseen](admin-job-queues-schedule-tasks.md)|  
|Asiakirjojen hallinta, poistaminen ja pakkaaminen|[Asiakirjojen poistaminen](admin-manage-documents.md)|  
|Näytä sivuja, koodiyksiköitä ja kyselyitä verkkopalveluina.|[Verkkopalvelun julkaiseminen](across-how-publish-web-service.md)|
|Kun luot Connect appsia [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ja kolmannen osapuolen ratkaisun välille REST API:a käyttäen, määritä mallit, joita käytetään täyttämään entiteetin tyhjät ominaisuudet luodessasi POST-toiminnon API:n kautta.|[API-mallien määritys](admin-configuring-api-template.md)|
|Salaa [!INCLUDE[d365fin](includes/d365fin_md.md)] Serverin tietoja luomalla uusia tai tuomalla olemassa olevia salausavaimia, jotka voi ottaa käyttöön palvelimessa.|[Tietojen salauksen hallinta](admin-manage-data-encryption.md)|
|Dynamics 365 Salesin yhdistäminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, mikä mahdollistaa asiakassuhteiden ja tilausten käsittelyn saumattoman integroinnin liidistä tuottoon -prosessissa.|[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Vaihda käyttöliittymässä näytettävät kentät ja toiminnot vastaamaan yrityksen liiketoimintaprosesseja ja laajenna ratkaisua sovelluksilla.|[[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen mukauttaminen](ui-customizing-overview.md)|

## <a name="see-related-training-at-microsoft-learnlearnpathsdeploy-configure-dynamics-365-business-central"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Liiketoiminnan toiminnallisuus](across-business-functionality.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Käytön aloittaminen](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
