---
title: Tuoterakenteen käyttäminen
description: 'Kokoonpanon tai tuotannon tuoterakenteella voi määrittää komponentit tai resurssit, joita tarvitaan kyseisen tuoterakenteen nimikkeen kokoamiseen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 09/26/2022
ms.author: a-reishima
---
# <a name="work-with-bills-of-material"></a>Tuoterakenteen käyttäminen

Tuoterakenteilla voi jäsentää päänimikkeet, jotka resurssien tai kuormituskeskusten on koottava muista nimikkeistä tai tuotettava komponenteista.

## <a name="assembly-boms-or-production-boms"></a>Kokoonpanon tuoterakenteet tai tuotannon tuoterakenteet

[!INCLUDE[prod_short](includes/prod_short.md)] tukee kahta seuraavaa erityyppistä tuoterakennetta:

| Tuoterakenteen tyyppi | Yleinen luokka | Esimerkki |
| -------- | ---------------- | ------- |
| [Kokoonpanon tuoterakenteet](assembly-how-work-assembly-boms.md) | Fyysinen varasto / kokoonpano | Nimikkeet, jotka koostuvat muista nimikkeistä, ja jotka on koottu perusresurssien avulla tai ilman resursseja. |
| [Tuotannon tuoterakenteet](production-how-to-create-production-boms.md) | Valmistus/tuotanto | Nimikkeet, jotka koostuvat eri komponenteista ja osakokoonpanoista, jotka on tuotettu tuotantosolussa tai kuormitusryhmässä. |

Voit käyttää kokoonpanotilauksia, kun teet komponenteista loppunimikkeitä yksinkertaisella prosessilla. Tämä prosessi voidaan toteutetaan vähintään yhdellä perusresurssilla, joka ei ole kuormituskeskus eikä tuotantosolu, tai ilman resursseja. Kokoonpanoprosessi voi olla esimerkiksi kahden viinipullon ja yhden kahvipaketin valinta ja niiden pakkaaminen lahjaksi.  

Kokoonpanon tuoterakenne muodostaa perustiedot, jotka määrittävät, mitkä osanimikkeet käytetään kokoonpanon lopputuotteeseen ja mitkä resurssit käytetään kokoonpanon nimikkeen kokoamiseen. Kun syötät kokoonpanon nimikkeen ja määrän uuden kokoonpanotilauksen otsikkoon, kokoonpanotilausrivit täytetään automaattisesti kokoonpanon tuoterakenteen mukaan yhdellä kokoonpanotilausrivillä osaa tai resurssia kohden. Lisätietoja on kohdassa [Kokoonpanon hallinta](assembly-assemble-items.md).

Käytä tuotantotilauksia tehdäksesi loopullisia nimikkeitä osista monimutkaisessa prosessissa, joka edellyttää tuotannon reititystä ja tuotantosoluja tai kuormitusryhmiä, jotka edustavat tuotantokapasiteettia. Tuotantoprosessi voi koostua esimerkiksi toiminnoista, jotka ovat teräslevyjen leikkaaminen, niiden hitsaaminen ja loppunimikkeen maalaaminen viimeisenä toimintona. Lisätietoja kohdassa [Valmistus](production-manage-manufacturing.md).

Tuotannon tuoterakenne määrittää tuotannon kohteen ja sen komponentit. Tuotannon tuoterakenteen on oltava sertifioitu ja määritetty tuotantokohteelle ennen kuin sitä voidaan käyttää tuotantotilauksessa. Kun syötät tuotantonimikkeen tuotantotilausriville joko manuaalisesti tai päivittämällä järjestystä, tuotannon rruoterakenteen sisällöstä tulee tuotantotilauksen komponentit. Lisätietoja on kohdassa [Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md).

Tuotannossa olevien resurssien konsepti on paljon kehittyneempi kuin kokoonpanon hallinnassa. Tuotantosolut ja kuormitusryhmät toimivat resursseina ja tuotannon vaiheet on esitetty toimina, jotka on määritetty resursseille tuotannon reitityksissä. Lisätietoja on [Reititysten luominen](production-how-to-create-routings.md) -artikkelissa.

Sekä kokoonpanotilaukset että tuotantotilaukset voidaan linkittää suoraan myyntitilauksiin. Voit käyttää kokoonpanotilauksia kuitenkin vain loppunimikkeen mukauttamiseen suoraan asiakkaan pyynnöstä myyntitilauksessa

## <a name="see-also"></a>Katso myös

[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Tuotevarianttien hallinta](inventory-item-variants.md)  
[Varasto](inventory-manage-inventory.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
