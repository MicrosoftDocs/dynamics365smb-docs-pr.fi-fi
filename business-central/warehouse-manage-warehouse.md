---
title: Fyysisen varaston aktiviteetit
description: Tavaroiden vastaanoton jälkeen ja ennen tavaroiden toimitusta suoritetaan joukko sisäisiä varastotoimintoja, joiden avulla varmistetaan nimikkeiden tehokas kulku varastossa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5774, 5776, 5777, 5785, 5793, 5797, 7318, 7364, 7401, 8909, 9000, 9008, 9009, 9050, 9053, 9056
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: d8cc547aa5187c270228a1e2dcd562eeb7f1cbb3
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511968"
---
# <a name="warehouse-management"></a>Varastoinninhallinta

Tavaroiden vastaanoton jälkeen ja ennen tavaroiden toimitusta suoritetaan joukko sisäisiä varastotoimintoja, joiden avulla varmistetaan nimikkeiden tehokas kulku varastossa sekä järjestellään ja ylläpidetään yrityksen varastoja.

Tyypillisiin varastotoimintoihin kuuluvat nimikkeiden hyllytys, nimikkeiden siirtäminen varaston sisällä tai varastoiden välillä sekä nimikkeiden poiminta kokoonpanoa, tuotantoa tai toimitusta varten. Myös nimikkeiden kokoamista myyntiin tai varastoon voidaan pitää varastotoimintoja, mutta niitä käsitellään toisaalla. Lisätietoja on kohdassa [Kokoonpanon hallinta](assembly-assemble-items.md).  

Suurissa fyysisissä varastoissa eri käsittelytehtävät voi erotella osastojen mukaan ja niiden integrointia voi hallita ohjatun työnkulun avulla. Yksinkertaisissa asennuksissa toiminta on epämuodollisempaa ja varastotoiminnot suoritetaan niin kutsuttuina varaston hyllytyksinä ja poimintoina. Lisätietoja fyysisen varastoinnin perusmäärityksistä ja laajennetuista varastomäärityksistä on kohdassa [Rakennetiedot: Fyysisen varaston yleiskuvaus](design-details-warehouse-overview.md).

Ennen varastotoimintojen suorittamista järjestelmään on määritettävä soveltuva fyysisen varastoinnin monimutkaisuustaso. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Varastoon liittyvät tehtävät (nimikkeiden inventointi, muuttaminen ja uudelleenluokittelu) voivat koskea varastointitehtäviä, jotka on suoritettava varastotapahtumissa, ennen kuin ne voidaan synkronoida liittyviin nimiketapahtumiin. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus](inventory-how-count-adjust-reclassify.md).

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Kirjaa nimikkeiden vastaanotto fyysisissä varastosijainneissa (myös vastaanoton ylittävä määrä) joko pelkällä ostotilauksella (yksinkertaiset sijaintimääritykset) tai fyysisen varastoinnin vastaanottona, jos sijainnissa käytetään osittain tai kokonaan automatisoitua varastokäsittelyä.|[Nimikkeiden vastaanottaminen](warehouse-how-receive-items.md)|
|Nopeuta nimikkeen siirtymistä vastaanotosta tai tuotannosta suoraan toimitukseen ohittamalla hyllytys- ja poimintakäsittelyt.|[Nimikkeiden laiturointi](warehouse-how-to-cross-dock-items.md)|
|Hyllytä ostoista, myyntipalautuksista, siirroista tai tuotannon tuotoksesta vastaanotettuja nimikkeitä määritetyn varastokäsittelyn mukaisesti.|[Nimikkeiden hyllyttäminen](warehouse-put-away-items.md)|
|Siirrä nimikkeitä fyysisen varaston varastopaikkojen välillä.|[Nimikkeiden siirtäminen](warehouse-move-items.md)|
|Poimi toimitettavia, siirrettäviä tai kokoonpanossa tai tuotannossa kulutettavia nimikkeitä määritetyn varastokäsittelyn mukaisesti.|[Nimikkeiden poiminta](warehouse-pick-items.md)|
|Kirjaa nimikkeiden toimitus fyysisistä varastosijainneista joko pelkällä myyntitilauksella (yksinkertaiset sijaintimääritykset) tai fyysisen varastoinnin toimituksena, jos sijainnissa käytetään osittain tai kokonaan automatisoitua varastokäsittelyä.|[Nimikkeiden lähettäminen](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Katso myös

[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Warehouse Managementin määrittäminen](warehouse-setup-warehouse.md) 
[Kokoonpanon hallinta](assembly-assemble-items.md)
[Rakennetiedot: Warehouse Management](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]