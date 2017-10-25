---
title: Tuotannon suorittaminen | Microsoft Docs
description: "Kun kysyntä on suunniteltu ja materiaalit on otettu tuotannon tuoterakenteen mukaisesti, tuotantotoiminnot voivat alkaa, ja ne suoritetaan tuotantotilauksen reitityksen määrittämässä järjestyksessä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: e27ceb91b25669a31d95256385cb7e5acd9160bd
ms.contentlocale: fi-fi
ms.lasthandoff: 09/27/2017

---
# <a name="manufacturing"></a>Tuotanto
Kun kysyntä on suunniteltu ja materiaalit on otettu tuotannon tuoterakenteen mukaisesti, tuotantotoiminnot voivat alkaa, ja ne suoritetaan tuotantotilauksen reitityksen määrittämässä järjestyksessä.  

Järjestelmän näkökulmasta tärkeä tuotannon toteutuksen osa on kirjata tuotantomäärä tietokantaan edistymisen raportoimiseksi ja varastomäärän päivittämiseksi valmiilla tuotteilla. Tuotoskirjaus voidaan tehdä manuaalisesti täyttämällä päiväkirjarivit ja kirjaamalla ne tuotantotoimintojen jälkeen. Se voidaan tehdä myös automaattisesti taaksepäinsiirron avulla. Tällöin materiaalin kulutus kirjataan automaattisesti tuotoksen kanssa, kun tuotantotilauksen tilaksi tulee Valmis.  

Vaihtoehto useiden tuotantotilausten tuotoksen kirjaamiselle eräpäiväkirjaan on yhden tuotantotilausrivin kulutuksen ja/tai tuotoksen kirjaaminen **Tuotantopäiväkirja**-ikkunassa.

Ennen nimikkeiden tuotannon aloittamista on tehtävä useita asetuksia, esimerkiksi tuotantosoluissa, reitityksissä ja tuotannon tuoterakenteissa. Lisätietoja on kohdassa [Tuotannon määrittäminen](production-configure-production-processes.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Tietoja tuotantotilausten käytöstä.|[Tietoja tuotantotilauksista](production-about-production-orders.md)|
|Luo tuotantotilaukset manuaalisesti.|[Toimintaohje: Tuotantotilausten luominen:](production-how-to-create-production-orders.md)|
|Ulkoista tuotantotilauksen kaikki toiminnot tai valitut toiminnot alihankkijalle.|[Toimintaohje: Tuotanto alihankintana](production-how-to-subcontract-manufacturing.md)|
|Tallenna ja kirjaa yksittäisen vapautetun tuotantotilausrivin tuotos sekä materiaalien ja ajan kulutus.|[Toimintaohje: Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen kirjaaminen.](production-how-to-register-consumption-and-output.md)|  
|Tee eräkirjauksena toiminnon käyttämien komponenttien määrä päiväkirjaan, joka voi käsitellä useita suunniteltuja tuotantotilauksia.|[Toimintaohje: Kulutuksen eräkirjaus](production-how-to-post-consumption.md)|
|Kirjaa toimintakohtainen valmistuneiden nimikkeiden määrä ja käytetty aika päiväkirjaan, joka voi käsitellä useita vapautettuja tuotantotilauksia.|[Toimintaohje: Tuotos- ja suoritusaikojen eräkirjaus](production-how-to-post-output-quantity.md)|  
|Kirjaa valmiiksi saatujen toimintojen osalta sellaisten tuotettujen nimikkeiden määrä, joita ei ole luokiteltu valmiiksi tuotokseksi vaan hukkatavaraksi.|[Toimintaohje: Hukkatavaran kirjaaminen](production-how-to-post-scrap.md)|
|Tarkastele tuotannon kuormitusta suunniteltujen ja vapautettujen tuotantotilausten tuloksena.|[Toimintaohje: Tuotantosolujen ja kuormitusryhmien kuormituksen tarkasteleminen](production-how-to-view-the-load-on-work-centers.md)|      
|Käytä **Kapasiteettipäiväkirja**-ikkunaa, jonka avulla voit kirjata sellaisia kulutettuja kapasiteetteja, joita ei ole kohdistettu tuotantotilaukseen (esimerkiksi kunnossapitotyö).|[Kapasiteettien kirjaaminen](production-how-to-post-capacities.md)|  
|Laske ja muuta valmiiden tuotantonimikkeiden kustannuksia ja kulutettuja komponentteja kirjanpidon täsmäytystä varten.|[Tietoja valmiin tuotantotilauksen kustannuksista](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Katso myös  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

