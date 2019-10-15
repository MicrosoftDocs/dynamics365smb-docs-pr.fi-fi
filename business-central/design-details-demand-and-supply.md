---
title: Rakennetiedot – kysyntä ja tarjonta | Microsoft Docs
description: Kysyntä on yleinen termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta. Lisäksi sovellus sallii tekniset kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 8ef7211aa812b1faf784ecf36f1873a6e2dcc6fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303626"
---
# <a name="design-details-demand-and-supply"></a>Rakennetiedot: kysyntä ja tarjonta
Kysyntä on yleinen termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta. Lisäksi sovellus sallii tekniset kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset.  

 Tarjonta on yleinen termi, jota käytetään mille tahansa positiiviselle tai tulevalle määrälle, kuten varasto, ostot, kokoonpano, tuotanto tai tulevat siirrot. Lisäksi myyntipalautus voi myös kuvata tarjontaa.  

 Voit lajitella useita kysynnän ja tarjonnan lähteitä, kun suunnittelujärjestelmä järjestää ne kahdelle aikajanalle, joita kutsutaan varastoprofiileiksi. Yksi profiili sisältää kysyntätapahtumat ja toinen sisältää vastaavat tarjontatapahtumat. Kukin tapahtuma edustaa yhtä tilausverkon kokonaisuutta, kuten myyntitilausriviä, nimiketapahtumaa tai tuotantotilausriviä.  

 Kun varaston profiilit ladataan, erilaiset kysyntä- ja tarjontajoukot täsmäytetään listatut tavoitteet täyttävän tarjontasuunnitelman tuotoksen saamiseksi.  

 Suunnitteluparametrit ja varastotasot ovat muita kysynnän ja tarjonnan tyyppejä, jotka käyvät läpi integroidun täsmäytyksen varastonimikkeiden täydentämiseksi. Lisätietoja on kohdassa [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md).  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
 [Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
 [Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
