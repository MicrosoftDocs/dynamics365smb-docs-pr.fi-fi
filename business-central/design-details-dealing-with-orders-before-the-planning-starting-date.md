---
title: Rakennetiedot – tilausten käsittely ennen suunnittelun aloituspäivää | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään sääntöjä, joita suunnittelu käyttää jäädytetyn alueen tilauksiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 32c523eda09620bd74df53f09bc103a44fbb367a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242273"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Rakennetiedot: tilausten käsittely ennen suunnittelun aloituspäivää
Voit estää mahdottomien ja sen vuoksi hyödyttömien ehdotusten näkymisen toimitussuunnitelmassa niin, että suunnittelujärjestelmä pitää suunnittelun alkupäivämäärää aiemman jakson jäädytetyksi alueeksi, joka ei sisällä suunnitelmia. Seuraava sääntö pätee jäädytettyyn alueeseen:  
  
Kaikki kysyntä ja tarjonta ennen suunnittelujakson aloituspäivämäärää katsotaan osaksi varastoa tai toimitetuksi.  
  
Näin ollen suunnittelujärjestelmä ei muutamia poikkeuksia lukuun ottamatta ehdota mitään muutoksia toimitustilauksiksi jäädytetyllä alueella ja tilauksen seurantalinkkejä ei luoda tai ylläpidetä tämän ajanjakson osalta.  
  
Poikkeukset tähän sääntöön ovat seuraavat:  
  
* Jos oletettu saatavilla oleva varasto, mukaan lukien kysynnän ja tarjonnan summa jäädytetyllä alueella, on nollan alapuolella.  
* Jos takautuvissa tilauksissa vaaditaan sarja-/eränumerot.  
* Jos tarjonta-kysyntä-yhdistelmä on linkitetty tilausten välisellä käytännöllä.  
  
Jos ensimmäinen käytettävissä oleva varasto on alle nollan, suunnittelujärjestelmä ehdottaa puuttuvan määrän kattamiseksi hätätoimitustilausta suunnittelujaksoa edeltävänä päivänä. Näin ollen suunnitellun ja käytettävissä olevan varaston on oltava aina vähintään nolla, kun tulevan kauden suunnittelu alkaa. Tämän toimitustilauksen suunnittelurivillä näytetään Hätävaroituskuvake ja lisätietoa annetaan sitä haettaessa.  
  
## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Sarja-/eränumerot ja Tilauksesta tilaukseen -linkit on vapautettu jäädytetyltä alueelta  
Jos sarja-/eränumerot vaaditaan tai tilausten välinen linkki on olemassa, suunnittelujärjestelmä jättää huomioimatta jäädytetyn vyöhykkeen ja sisällyttää nämä takautuvat määrät aloituspäivämäärästä alkaen ja ehdottaa mahdollisesti korjaavia toimenpiteitä, jos kysyntää ja tarjontaa ei synkronoida. Liiketoimintasyy tälle periaatteelle on se, että tällaisten erityisten kysyntä-tarjonta-asetusten täytyy vastata toisiaan, jotta varmistetaan että tämä erityiskysyntä täyttyy.  
  
## <a name="see-also"></a>Katso myös  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)