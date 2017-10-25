---
title: "Kustannusten määrittäminen ja kohdistaminen | Microsoft Docs"
description: "Kustannusten kohdistukset siirtävät kustannukset ja tuotot eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä. Voit määrittää niin monta kodhistusta kuin on tarpeen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 050b0bd997629ca189cfbe035e361de7a252d079
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="defining-and-allocating-costs"></a>Kustannusten määrittäminen ja kohdistaminen
Kustannusten kohdistukset siirtävät kustannuksia ja tuottoja eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä. Voit määrittää niin monta kodhistusta kuin on tarpeen. Jokainen kohdistus koostuu:  

-   Kohdistamisen lähde.  
-   Vähintään yksi kohdistuskohde.  

Kohdistuksen lähde määrittää, mitkä kustannukset täytyy kohdistaa sekä kohdistustavoitteet määrittävät, missä kustannukset on kohdistettava. Esimerkiksi kohdistuksen lähde voi olla Sähkö ja lämmitys -kustannuslajin kustannukset. Kohdista kaikki sähkö ja lämmityskustannukset kolmeen kustannuspaikkaan: korjaamo, tuotanto ja myynti. Näihin kustannuspaikkoihin kohdistetaan kohteita.  

Määritä jokaiselle kohdistuksen lähteelle kohdistustaso, voimassaoloaika ja variantti ryhmittelyn tunnukseksi. Erätyön avulla voit määrittää suodattimia valitaksesi kohdistusmääritelmiä ja suorittaaksesi sitten kustannusten kohdistukset automaattisesti.  

Määritä jokaiselle kohdistuksen kohteelle kohdistusperuste. Kohdistusperuste voi olla joko staattinen tai dynaaminen.  

-   Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.  
-   Dynaaminen kohdistus perustuu muutettaviin arvoihin, kuten työntekijöiden määrään kustannuspaikassa, kustannuskohteen myyntituottoihin tiettynä aikajaksona.  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

|Vastaanottaja|Katso|  
|--------|---------|  
|Kohdistuksen lähteen ja sen tavoitteiden määrittäminen.|[Kohdistuksen lähteen ja tavoitteiden määrittäminen](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Määrittää useita suodattimia dynaamisen kohdistuksen perusteille.|[Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Esimerkki siitä, miten voit määrittää staattista kohdistamista.|[Esimerkkiskenaario: Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Esimerkki siitä, miten voit määrittää dynaamista kohdistamista.|[Esimerkkiskenaario: Määrittämällä myytyihin nimikkeisiin perustuvat dynaamiset kohdistamiset](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Katso myös  
 [Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)   
 [Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md)   
 [Kustannuslaskenta](finance-manage-cost-accounting.md)   
 [Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)   
 [Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)

