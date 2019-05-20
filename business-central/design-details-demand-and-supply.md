---
title: Rakennetiedot – kysyntä ja tarjonta | Microsoft Docs
description: Kysyntä on yleinen termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta. Lisäksi ohjelma sallii teknisemmät kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: c26e74cb2a362339b1e7c95809fb19e13869c61e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242281"
---
# <a name="design-details-demand-and-supply"></a>Rakennetiedot: kysyntä ja tarjonta
Kysyntä on yleinen termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta. Lisäksi ohjelma sallii teknisemmät kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset.  
  
 Tarjonta on yleinen termi, jota käytetään mille tahansa positiiviselle tai tulevalle määrälle, kuten varasto, ostot, kokoonpano, tuotanto tai tulevat siirrot. Lisäksi myyntipalautus voi myös kuvata tarjontaa.  
  
 Voit lajitella useita kysynnän ja tarjonnan lähteitä, kun suunnittelujärjestelmä järjestää ne kahdelle aikajanalle, joita kutsutaan varastoprofiileiksi. Yksi profiili sisältää kysyntätapahtumat ja toinen sisältää vastaavat tarjontatapahtumat. Kukin tapahtuma edustaa yhtä tilausverkon kokonaisuutta, kuten myyntitilausriviä, nimiketapahtumaa tai tuotantotilausriviä.  
  
 Kun varaston profiilit ladataan, erilaiset kysyntä- ja tarjontajoukot täsmäytetään listatut tavoitteet täyttävän tarjontasuunnitelman tuotoksen saamiseksi.  
  
 Suunnitteluparametrit ja varastotasot ovat muita kysynnän ja tarjonnan tyyppejä, jotka käyvät läpi integroidun täsmäytyksen varastonimikkeiden täydentämiseksi. Lisätietoja on kohdassa [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md).  
  
## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
 [Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
 [Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)