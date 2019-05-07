---
title: Suodattimien määrittäminen dynaamisille kohdistusperusteille | Microsoft Docs
description: Dynaaminen kohdistusmenetelmä on perustuu muutettaviin arvoihin. Esimerkiksi kustannuspaikan työntekijöiden tai kustannuskohteen myytyjen nimikkeiden määrä tietyn ajanjakson aikana. Ohjelmassa on yhdeksän ennalta määritettyä kohdistamisen perustetta ja kaksitoista dynaamista päivämääräväliä. Voit määrittää eri suodattimia kohdistuksen perusteella.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 35f9a542d57bfe27c9a9ee48f4a41af7071cdd47
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "935494"
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
[Kustannusten määrittäminen ja kohdistaminen](finance-define-and-allocate-costs.md)
