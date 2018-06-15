---
title: "Business Central -sovelluksen hallintatehtävät | Microsoft Docs"
description: "Joitakin Business Central -sovelluksen tehtäviä on hallittava ja määritettävä keskitetysti. Katso lisätietoja näistä tehtävistä ja niiden määrittämisestä."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 05/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 93eced90155b9172595561bfc5b80c3c49ca11bc
ms.contentlocale: fi-fi
ms.lasthandoff: 05/15/2018

---
# <a name="administration"></a>Hallinta
Yleensä yksi rooli hoitaa yrityksen keskitetyt hallintatehtävät. Tehtävien laajuus voi määräytyä yrityksen koon ja järjestelmänvalvojan vastuualueiden mukaan. Tehtäviin voi sisältyä esimerkiksi työ- ja sähköpostijonojen tietokantasynkronoinnin hallintaa, käyttäjien määritystä, käyttöliittymän mukautusta ja salausavainten hallintaa.  

Uuden liiketoimintaohjelmiston toimivuuden vuoksi on tärkeää, että syötettävät asetusarvot ovat oikeita alusta alkaen. [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on useita asetusoppaita, jotka helpottavat perustietojen määrittämistä. Lisätietoja on kohdassa [Business Central -sovelluksen määrittäminen](setup.md).

Riippumatta siitä, otatko asetusarvot käyttöön RapidStart Services -palvelussa vai annatko ne manuaalisesti uudessa yrityksessä, voit tukea määrityspäätöksiäsi tietyillä yleisillä suosituksilla sellaisissa määrityskentissä, joiden tiedetään voivan heikentää ratkaisun toimintaa, jos ne määritetään virheellisesti.  

Pääkäyttäjä tai järjestelmänvalvoja voi määrittää tietojen vaihtamiskehyksen, jonka avulla käyttäjät voivat viedä ja tuoda pankki- ja palkanlaskentatiedostojen tietoja esimerkiksi erilaisia kassanhallintaprosesseja varten.

> [!NOTE]
> Voit määrittää uuden yrityksen [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa RapidStart Services -palvelun kanssa. RapidStart Services -palvelun on työkalu, joka on suunniteltu lyhentämään käyttöönottoa, parantamaan toteutuksen laatua, esittelemään toistettavia lähestymistapoja toteutuksiin, ja lisäämään tuottavuutta automatisoimalla ja yksinkertaistamalla toistuvia tehtäviä. Lisätietoja on kohdassa ## [Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Lisää käyttäjiä, hallitse tietojen käyttöoikeuksia ja määritä rooleja.|[Tietoja profiileista ja roolikeskuksista](admin-users-profiles-roles.md)|  
|Määritä käyttöoikeuksia käyttäjille, muokata käyttöoikeusjoukkoja ja ryhmitä käyttäjiä käyttöoikeuksien perusteella.|[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)|
|Luokittele kenttien luottamukselliset tiedot niin, että voit vastata tietojen kohteiden henkilökohtaisia tietoja koskeviin pyyntöihin.|[Tietojen luottamuksellisuuden luokitteleminen](admin-classifying-data-sensitivity.md)|
|Vastaa tietojen kohteiden henkilökohtaisia tietoja koskeviin pyyntöihin.|[Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen](admin-responding-to-requests-about-personal-data.md)|
|Uuden liiketoimintayksikön määrittäminen mallien avulla|[Uusien yritysten luominen](about-new-company.md)|
|Vaihda käyttöliittymässä näytettävät kentät ja toiminnot vastaamaan yrityksen liiketoimintaprosesseja. |[[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen mukauttaminen](ui-customizing-overview.md) |
|Seuraa kaikkia suoria muutoksia, joita käyttäjät tekevät tietokannan tietoihin. Muutoksia seuraamalla voidaan tunnistaa virheiden alkuperä ja tietojen muutokset.|[Muutosten kirjaaminen lokiin](across-log-changes.md)|  
|Määritä yksittäisiä tai toistuvia pyyntöjä raporttien tai koodiyksiköiden suorittamista varten.|[Työjonojen käyttäminen tehtävien aikatauluttamiseen](admin-job-queues-schedule-tasks.md)|  
|Asiakirjojen hallinta, poistaminen ja pakkaaminen|[Asiakirjojen poistaminen](admin-manage-documents.md)|  
|Näytä sivuja, koodiyksiköitä ja kyselyitä verkkopalveluina.|[Verkkopalvelun julkaiseminen](across-how-publish-web-service.md)|
|Kun luot Connect-sovellusta [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ja kolmannen osapuolen ratkaisun välille REST API:a käyttäen, määritä mallit, joita käytetään täyttämään entiteetin tyhjät ominaisuudet luodessasi POST-toiminnon API:n kautta.|[API-mallien määritys](admin-configuring-api-template.md)|

## <a name="see-also"></a>Katso myös
[Liiketoiminnan toiminnallisuus](across-business-functionality.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Käytön aloittaminen](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

