---
title: "Suodattimien määrittäminen dynaamisille kohdistusperusteille | Microsoft Docs"
description: "Dynaaminen kohdistusmenetelmä on perustuu muutettaviin arvoihin. Esimerkiksi kustannuspaikan työntekijöiden tai kustannuskohteen myytyjen nimikkeiden määrä tietyn ajanjakson aikana. Ohjelmassa on yhdeksän ennalta määritettyä kohdistamisen perustetta ja kaksitoista dynaamista päivämääräväliä. Voit määrittää eri suodattimia kohdistuksen perusteella."
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
ms.openlocfilehash: 317e924f3297946f3d933cecf21593f0791ebec0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.
Dynaaminen kohdistusmenetelmä on perustuu muutettaviin arvoihin. Esimerkiksi kustannuspaikan työntekijöiden tai kustannuskohteen myytyjen nimikkeiden määrä tietyn ajanjakson aikana. Ohjelmassa on yhdeksän ennalta määritettyä kohdistamisen perustetta ja kaksitoista dynaamista päivämääräväliä. Voit määrittää eri suodattimia kohdistuksen perusteella.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.  
 Seuraavassa taulukossa on esitetty mitä suodattimia on mahdollista käyttää eri kohdistusperusteille ja mitkä arvot ovat mahdollisia **Nrosuodatus**- ja **Ryhmäsuodatus**-kentissä. Paina F1-näppäintä **Päivämäärän suodatuskoodi** -kentässä, jos haluat lukea yksityiskohtaiset kuvaukset.  

|**Peruste**|**Nro suodatus**|**Päivämäärän suodatuskoodi**|**Kustannuspaikkasuodatus**|**Kustannuskohdesuodatus**|**Ryhmäsuodatus**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|KP-tapahtumat|KP-tili|Kyllä|Kyllä|Kyllä|Ei saatavilla|  
|KP-budjetin tapahtumat|KP-tili|Kyllä|Kyllä|Kyllä|KP-budjetin nimi|  
|Kustannustyyppitapahtumat|Kustannustyyppi|Kyllä|Kyllä|Kyllä|Ei saatavilla|  
|Kustannusbudjettitapahtumat|Kustannustyyppi|Kyllä|Kyllä|Kyllä|Budjetin nimi|  
|Työntekijöiden määrä|Ei saatavilla|Kyllä|Kyllä|Kyllä|Ei saatavilla|  
|Nimikkeitä myyty (Määrä)|Nimikkeen nro|Kyllä|Kyllä|Kyllä|Varaston kirjausryhmä|  
|Nimikkeitä ostettu (Määrä)|Nimikkeen nro|Kyllä|Kyllä|Kyllä|Varaston kirjausryhmä|  
|Nimikkeitä myyty (Summa)|Nimikkeen nro|Kyllä|Kyllä|Kyllä|Varaston kirjausryhmä|  
|Nimikkeitä ostettu (Summa)|Nimikenro|Kyllä|Kyllä|Kyllä|Varaston kirjausryhmä|  

## <a name="see-also"></a>Katso myös  
 [Esimerkkiskenaario: Myytyihin nimikkeisiin perustuvien dynaamisten kohdistusten määrittäminen](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Toimintaohje: Kohdistuksen lähteen ja tavoitteiden määrittäminen](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Kustannusten määrittäminen ja kohdistaminen](finance-define-and-allocate-costs.md)

