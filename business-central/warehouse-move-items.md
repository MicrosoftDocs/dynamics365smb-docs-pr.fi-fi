---
title: Nimikkeiden siirtäminen | Microsoft Docs
description: Varaston nimikkeitä pitää joskus siirtää varastopaikasta toiseen päivittäisten varastotapahtumien ja varaston nimikevirran tukemiseksi. Jotkut liikkeet tapahtuvat suorassa suhteessa sisäisiin toimintoihin, kuten tuotantotilaus, jonka komponentit täytyy toimittaa tai lopulliset nimikkeet hyllyttää. Muut siirrot tapahtuvat vain fyysisen varastoinnin tilan optimointina tai ad-hoc-siirtoina toimintoihin ja toiminnoista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66c2b9d191bc899de6ec2b6e6bbcd99d133448b7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784115"
---
# <a name="moving-items"></a>Nimikkeiden siirtäminen
Nimikkeiden siirtäminen fyysisessä varastossa on varastotoiminto, joka suoritetaan eri tavoilla sen mukaan, miten varastoinninhallintajärjestelmän ominaisuudet on määritetty. Määritysten monimutkaisuus voi vaihdella: ominaisuusluettelossa ei ole varastotoimintoja lainkaan, tilauskohtaisessa fyysisen varastoinnin perusmäärityksissä käsittelytoimintoja on vain muutama toiminto, kun laajennetuissa varastomäärityksissä kaikki varastotoiminnot tehdään ohjatun työnkulun mukaisesti. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Nimikkeitä on ehkä siirrettävä samassa fyysisessä varastosijainnissa varastopaikasta toiseen päivittäisten varastotapahtumien ja varaston nimikevirran tukemiseksi. Jotkut liikkeet tapahtuvat suorassa suhteessa sisäisiin toimintoihin, kuten tuotantotilaus, jonka komponentit täytyy toimittaa tai lopulliset nimikkeet hyllyttää. Muut siirrot tapahtuvat vain fyysisen varastoinnin tilan optimointina tai ad-hoc-siirtoina toimintoihin ja toiminnoista.

Muita siirtotehtäviä ovat poiminnan tai tuotannon varastopaikkojen kausittainen täydennys sekä varastopaikan sisällön muuttaminen.

Nimikkeiden siirtäminen toiseen sijaintiin vaikuttaa nimiketapahtumiin, joten ne on tehtävä siirtotilauksen avulla. Lisätietoja on kohdassa [Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).  

Varastoon liittyvät tehtävät (nimikkeiden inventointi, muuttaminen ja uudelleenluokittelu) voivat koskea varastointitehtäviä, jotka on suoritettava varastotapahtumissa, ennen kuin ne voidaan synkronoida liittyviin nimiketapahtumiin. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus](inventory-how-count-adjust-reclassify.md)  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Siirrä nimikkeitä perusvaraston määrityksten mukaisten varastopaikkojen välillä milloin tahansa ja ilman lähdeasiakirjoja.|[Nimikkeiden siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Fyysisen varastoinnin siirtotyökirjan avulla voit siirtää kohteita laajennetuissa varastointimäärityksissä, sekä lähdeasiakiroihin että ad-hoc -raportteihin.|[Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Tuo komponenttinimikkeet sisäisiin toimintoihin varastoinnin määritysten mukaisesti kyseisten toimintojen lähdeasiakirjojen pyytämänä.|[Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Suunnittele, mitä varastopaikkoja täytetään tai tyhjennetään tehokkaan nimikevirran ylläpitämiseksi (esimerkiksi irtotavaravaraston tyhjentäminen ennen suurta vastaanottoa).|[Fyysisen varaston siirtojen suunnitteleminen työkirjoissa](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Päivitä taajuus, jolla varastopaikat (kuten poiminnan varastopaikat) täydennetään kysynnän vaihtelun seurauksena.|[Laske var.paikan täydennys](warehouse-how-to-calculate-bin-replenishment.md)|
|Järjestä fyysinen varasto uudelleen uusilla varastopaikan koodeilla ja uusilla varastopaikan ominaispiirteillä sekä mahdollisesti vaihtamalla niiden paikkaa.|[Fyysisten varastojen uudelleenjärjestely](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]