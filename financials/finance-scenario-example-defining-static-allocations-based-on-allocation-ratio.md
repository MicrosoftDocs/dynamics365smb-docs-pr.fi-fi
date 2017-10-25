---
title: "Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen | Microsoft Docs"
description: "Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4."
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
ms.openlocfilehash: b48d7f73b640b98d0cdab6e2e7e7486a3bdb39db
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Esimerkkiskenaario: Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen
Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.  

Tässä aiheessa kuvataan, miten määrittää kolmen uuden kohdistuskohteen kustannuskohteet TUOT kustannuspaikoille käyttäen vahvistettu-varaus -suhdetta 5:2:4. Kolme kohdekustannuskohdetta ovat LISÄLAITT, MAALIT ja KALUSTO.  

> [!NOTE]  
>  Esimerkissä käytetään demodataa [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta.  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Määritä varauksen lähde TUOT kustannuspaikka yleisessä pikavälilehdessä  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannusten kohdistaminen** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Kustannusten kohdistaminen** -ikkunassa **Uusi**-toiminto.  
3.  Paina **Tunnus**-kentässä Enter tai kirjoita tunnus.  
4.  Syötä **Taso**-kenttään **1**.  
5.  Syötä arvot **Voimassaolo alkaa**- ja **Voimassaolo päättyy** -kenttiin.  
6.  Syötä **Kustanuspaikkakoodi**-kenttään **TUOT**.  
7.  Syötä **Luotto kustannustyyppiin** -kenttään kustannustyyppi **9903**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Määritä kodhistuskohteen kustannus-objektit Rivit-pikavälilehdellä  

1.  Syötä laskun ensimmäiselle riville **Kohdekustannustyyppi**-kenttään **9903**.  
2.  Syötä ensimmäiselle riville **Kohdekustannuskohde**-kenttään **LISÄLAITT**.  
3.  Valitse ensimmäisen rivin **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.  
4.  Valitse ensimmäisen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.  
5.  Anna ensimmäisen rivin **Jaa**-kentässä varaussuhde **5**.  
6.  Syötä toiselle riville **Kohdekustannustyyppi**-kenttään **9903**.  
7.  Syötä toiselle riville **Kohdekustannuskohde**-kenttään **MAALI**.  
8.  Valitse toiselle riville **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.  
9. Valitse toisen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.  
10. Anna toisen rivin **Jaa**-kentässä varaussuhde **2**.  
11. Syötä kolmannelle riville **Kohdekustannustyyppi**-kenttään **9903**.  
12. Syötä kolmannelle riville **Kohdekustannuskohde**-kenttään **KALUSTO**.  
13. Valitse kolmannen rivin **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.  
14. Valitse kolmannen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.  
15. Anna kolmannen rivin **Jaa**-kentässä varaussuhde **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee automaattisesti **Prosentti**-kenttään prosenttiarvon, joka määräytyy kaikkien niiden kolmen kohdistussuhteen mukaan, jotka syötetty **Osuus**-kenttään kaikilla kolmella rivillä.  

## <a name="see-also"></a>Katso myös  
[Kohdistuksen lähteen ja tavoitteiden määrittäminen](finance-how-to-set-up-allocation-source-and-targets.md)   
[Kustannusten määrittäminen ja kohdistaminen](finance-define-and-allocate-costs.md)   
[Esimerkkiskenaario: Myytyihin nimikkeisiin perustuvien dynaamisten kohdistusten määrittäminen](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
[Kustannusten määrittäminen ja kohdistaminen](finance-define-and-allocate-costs.md)

