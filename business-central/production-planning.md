---
title: Toimitusten suunnittelu | Microsoft Docs
description: Valmistele myynti- ja tuotantotarvetta varten seikkaperäinen ja toteuttamiskelpoinen suunnitelma sekä viimeistelykokoonpanon tuotantoaikataulu.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 41fb80f39edc87aabce18c5ef39e799148eb0058
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "852192"
---
# <a name="planning"></a>Suunnittelu
Tuotanto-operaatiot, joita tarvitaan panoksen muuttamiseen lopputuotteiksi, on suunniteltava päivittäin tai viikoittain volyymin ja tuotteiden luonteen mukaan. [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää toimintoja, joiden avulla voidaan vastata myynnin, kokoonpanon ja tuotannon ennakoituun ja todelliseen kysyntään. Lisäksi siinä on toimintoja, joita käytetään jakelun suunnitteluun varastointiyksiköiden ja sijaintisiirtojen avulla.

> [!NOTE]
> Tässä ohjeaiheessa käsitellään lähinnä tuotantoon tai kokoonpanon hallintaan liittyviä yrityksiä, joissa toimitustilaukset voivat olla tuotanto-, kokoonpano-, siirto- tai ostotilauksia. Tämä suunnittelutyö tehdään pääasiassa **Suunnittelutyökirja**-sivulla.

> [!INCLUDE[d365fin](includes/d365fin_md.md)] tukee myös niitä tukkukaupan yritysten toimitussuunnittelua, joissa syntyvät toimitustilaukset voivat olla vain siirto- tai ostotilauksia. Tämä suunnittelutyö tehdään pääasiassa **Hankintalista**-sivulla, jota käsitellään epäsuorasti tässä ohjeaiheessa, sillä useimmat suunnittelutoiminnot koskevat molempia sivuja.

Ennen tuotantotilausten suunnittelua ja toteuttamista on määritettävä tuotantokapasiteetit, kuten luotavat tuotantokalenterit, reititykset, tuotannon tuoterakenteet ja kuormitusryhmät. Lisätietoja on kohdassa [Tuotannon määrittäminen](production-configure-production-processes.md).

Suunnittelua voidaan pitää kysynnän täyttämiseen tarvittavana toimitustilausten valmisteluna kokoonpano- ja tuotanto-osastoilla. Lisätietoja on kohdissa [Kokoonpanon hallinta](assembly-assemble-items.md) ja [Tuotanto](production-manage-manufacturing.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Tutustu lyhyeen esittelyyn suunnittelujärjestelmän käytöstä kysynnän tunnistamisessa ja priorisoinnissa sekä tasapainotetun toimitussuunnitelman ehdottamisessa.|[Tietoja toimintojen suunnittelusta](production-about-planning-functionality.md)|
|Tiedosto miten, suunnittelujärjestelmän eri osa-alueet toimivat ja miten algoritmeja voidaan muuttaa eri ympäristöjen suunnitteluvaatimuksia vastaaviksi.|[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)|
|Tutustu, miten suunnittelulogiikka tekee eron sijaintien kysynnän välillä varastointiyksikön asetusten mukaan ja silloin, kun kysynnällä ei ole sijaintikoodeja.|[Suunnittelu sijainteja käyttämällä tai ilman niitä](production-planning-with-without-locations.md)|
|Ennustettu kysyntä odotetun myynnin ja tuotannon komponenttien perusteella.|[Kysyntäennusteen luominen](production-how-to-create-a-forecast.md)|  
|Luo myyntitilauksesta riippuvaisia tuotantotilauksia, jotka kattavat täsmällisesti myyntitilausrivin kysynnän.|[Tuotantotilausten luominen myyntitilauksista:](production-how-to-create-production-orders-from-sales-orders.md)|
|Luo tuotantoprojektia edustava projektituotantotilaus suoraan monirivistä myyntitilauksesta.|[Projektitilausten suunnitteleminen](production-how-to-plan-project-orders.md)|
|Käytä **Tilauksen suunnittelu** -sivua, jonka avulla voit suunnitella myynnin tai tuotantokysynnän manuaalisesti yksi tuotannon tuoterakenne kerrallaan.|[Uuden kysynnän tilauskohtainen suunnittelu](production-how-to-plan-for-new-demand.md)|
|Voit suorittaa **Suunnittelutyökirja**-sivulla sekä tuotanto-ohjelman että tarvelaskennan ja luoda niiden avulla joko ylätason tai yksityiskohtaisen toimitussuunnitelman kaikilla nimiketasoilla.|[Kokonaisvaltaisen suunnittelun, tuotanto-ohjelman tai tarvelaskennan suorittaminen](production-how-to-run-mps-and-mrp.md)|
|Suorita hankintalista, jonka avulla voit luoda automaattisesti yksityiskohtaisen toimitussuunnitelman, joka kattaa sellaisten nimikkeiden kysynnän, joita täydennetään vain ostojen tai siirtojen avulla.|**Hankintalista**-sivu|  
|Aloita tai päivitä tuotantotilaus raakasuunniteltuna operaationa päätuotantoaikataulussa.|[Tuotantotilausten suora uudelleensuunnittelu tai päivittäminen](production-how-to-replan-refresh-production-orders.md)|
|Laske tuotantosolun tai kuormitusryhmän kalenterit uudelleen suunnittelun muutosten vuoksi.|[Tuotantosolun kalenterin laskeminen](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|Seuraa tilauskysyntää (seurattu määrä), ennustetta, myyntipuitetilausta tai suunnitteluparametria (ei-seurattu määrä), joka on kiinnittänyt huomion kyseiseen suunnitteluriviin.|[Kysynnän ja tarjonnan välisten suhteiden seuraaminen](production-how-track-demand-supply.md)|
|Tarkastele nimikkeen suunniteltua saatavilla olevaa varastoa erilaisissa näkymissä ja katso, mitkä bruttotarpeet, suunnitellut tilausten vastaanotot ja muut tekijät vaikuttavat varastoon tietyn ajan kuluessa.|[Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)|  
|Suorita valitut suunnitellut tehtävät, kuten suunnittelutyökirjan rivien muuttaminen tai lisääminen, toimitussuunnitelma graafisessa näkymässä.|[Suunnitteluehdotusten muokkaaminen graafisessa näkymässä](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Katso myös
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
