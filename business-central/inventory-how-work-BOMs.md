---
title: Tuoterakenteen käyttäminen
description: 'Kokoonpanon tai tuotannon tuoterakenteella voi määrittää komponentit tai resurssit, joita tarvitaan kyseisen tuoterakenteen nimikkeen kokoamiseen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# <a name="work-with-bills-of-material"></a>Tuoterakenteen käyttäminen

Tuoterakenteilla voi jäsentää päänimikkeet, jotka resurssien tai kuormituskeskusten on koottava muista nimikkeistä tai tuotettava komponenteista.

## <a name="assembly-boms-or-production-boms"></a>Kokoonpanon tuoterakenteet tai tuotannon tuoterakenteet

[!INCLUDE[prod_short](includes/prod_short.md)] tukee kahta seuraavaa erityyppistä tuoterakennetta:

| Tuoterakenteen tyyppi | Yleinen luokka | Esimerkki |
| -------- | ---------------- | ------- |
| [Kokoonpanon tuoterakenteet](assembly-how-work-assembly-boms.md) | Fyysinen varasto / kokoonpano | Nimikkeet, jotka koostuvat muista nimikkeistä, ja jotka on koottu perusresurssien avulla tai ilman resursseja. |
| [Tuotannon tuoterakenteet](production-how-to-create-production-boms.md) | Valmistus/tuotanto | Nimikkeet, jotka koostuvat eri komponenteista ja osakokoonpanoista, jotka on tuotettu tuotantosolussa tai kuormitusryhmässä. |

Kokoonpanotilauksia käytetään loppunimikkeiden tekemiseen komponenteista yksinkertaisessa prosessissa, jonka voi suorittaa yksi tai useampi perusresurssi, joka ei ole kuormitusryhmä tai tuotantosolu tai jossa ei ole resursseja. Kokoonpanoprosessi voi olla esimerkiksi kahden viinipullon ja yhden kahvipaketin valinta ja niiden pakkaaminen lahjaksi.  

Kokoonpanon tuoterakenne muodostaa perustiedot, jotka määrittävät, mitkä osanimikkeet käytetään kokoonpanon lopputuotteeseen ja mitkä resurssit käytetään kokoonpanon nimikkeen kokoamiseen. Kun syötät kokoonpanon nimikkeen ja määrän uuden kokoonpanotilauksen otsikkoon, kokoonpanotilausrivit täytetään automaattisesti kokoonpanon tuoterakenteen mukaan yhdellä kokoonpanotilausrivillä osaa tai resurssia kohden. Lisätietoja on kohdassa [Kokoonpanon hallinta](assembly-assemble-items.md).

Käytä tuotantotilauksia tehdäksesi loopullisia nimikkeitä osista monimutkaisessa prosessissa, joka edellyttää tuotannon reititystä ja tuotantosoluja tai kuormitusryhmiä, jotka edustavat tuotantokapasiteettia. Tuotantoprosessi voi koostua esimerkiksi toiminnoista, jotka ovat teräslevyjen leikkaaminen, niiden hitsaaminen ja loppunimikkeen maalaaminen viimeisenä toimintona. Lisätietoja kohdassa [Valmistus](production-manage-manufacturing.md).

Tuotannon tuoterakenne määrittää tuotannon kohteen ja sen komponentit. Tuotannon tuoterakenteen on oltava sertifioitu ja määritetty tuotantokohteelle ennen kuin sitä voidaan käyttää tuotantotilauksessa. Kun syötät tuotantonimikkeen tuotantotilausriville joko manuaalisesti tai päivittämällä järjestystä, tuotannon rruoterakenteen sisällöstä tulee tuotantotilauksen komponentit. Lisätietoja on kohdassa [Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md).

Tuotannossa olevien resurssien konsepti on paljon kehittyneempi kuin kokoonpanon hallinnassa. Työkeskukset ja kuormitusryhmien alennukset toimivat resursseina. Tuotannon reititysten resursseihin kohdistetut toiminnot edustavat tuotantovaiheita. Lisätietoja on [Reititysten luominen](production-how-to-create-routings.md) -artikkelissa.

Sekä kokoonpanotilaukset että tuotantotilaukset voidaan linkittää suoraan myyntitilauksiin. Voit käyttää kokoonpanotilauksia kuitenkin vain loppunimikkeen mukauttamiseen suoraan asiakkaan pyynnöstä myyntitilauksessa

## <a name="see-also"></a>Katso myös

[Kokoonpanon tuoterakenteiden käsitteleminen](assembly-how-work-assembly-boms.md)    
[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)    
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)    
[Tuotevarianttien hallinta](inventory-item-variants.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)    
[Tuotanto](production-manage-manufacturing.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
