---
title: Sijaintikortin ja siirtoreittien määrittäminen (sisältää videon)
description: Jos ostat, varastoit tai myyt nimikkeitä useamman varaston avulla, sijaintikortti ja siirtoreitit on määritettävä jokaiselle sijainnille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 2482b25e6b8e29e5cff420db1700943ca4f1df51
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060088"
---
# <a name="set-up-locations"></a>Sijaintien määrittäminen

Sijainnit ovat paikkoja, kuten varasto, jossa nimikkeitä ostetaan, säilytetään tai myydään. [!INCLUDE [prod_short](includes/prod_short.md)] käyttää sijainteja varaston seurannassa sekä yksinkertaisissa että monimutkaisissa varastoprosesseissa.

Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen. Lisätietoja on myös kohdassa [Varaston hallinta](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Sijaintikortit
Tietoja sijainnista, esimerkiksi fyysisestä varastosta tai jakelukeskuksesta määritetään **Sijaintikortti**-sivulla. Kullekin sijainnille annetaan sijaintia kuvaava nimi ja koodi. Tämän jälkeen sijaintikoodin voi syöttää muualle ohjelmaan silloin, kun haluat tallentaa transaktioita tietylle sijainnille.  

Voit syöttää tietoja varastopaikasta ja fyysisen varaston periaatteista jokaiselle sijainnille. Valitsemiesi fyysisen varaston periaatteiden perusteella voit määrittää **Varastopaikat**-pikavälilehden vaihtoehtojen avulla varastopaikat, joita käytetään oletusvarastopaikkoina toteutettaessa tapahtumia. Jos käytät ohjattua hyllytystä ja poimintaa, voit määrittää **Var.paikkojen periaatteet** -pikavälilehden vaihtoehtojen avulla, miten haluat käyttää fyysisen varaston eri lisäominaisuuksia.  

Jotkut vaihtoehtokentät määräytyvät **Sijaintikortti**-sivun asetusten mukaan. Tällä rajoitetaan asetusyhdistelmiä, joita ei tueta.  

Valitse toiminnot **Alueet** tai **Varastopaikat** nähdäksesi tiedot alueista ja varastopaikoista, jotka on määritetty sijainnille.

### <a name="to-set-up-a-location"></a>Sijaintien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Sijaintikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.

> [!NOTE]  
> Monet sijaintikorttisivun kentät viittaavat saapuvien ja lähtevien varastoprosessien nimikkeiden käsittelyyn. Nämä kentät eivät ole olennaisia yrityksille, jotka eivät tarvitse monimutkaista varastotoimintoa. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Voit muuttaa sijainnin määritystä myöhemmin, mutta et voi muokata asetuksia niille sijainneille, joilla on kirjanpitotapahtumia.  

Jos sinulla on useampia sijainteja, voit määrittää sijaintien välisiä siirtoreittejä. Lisätietoja on ohjeaiheessa [Siirtoreittien luonti](inventory-how-setup-locations.md#to-create-a-transfer-route). 

### <a name="to-create-a-transfer-route"></a>Siirtoreittien luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtoreitit** ja valitse sitten vastaava linkki.
2. Voit myös valita **Siirtoreitit**-toiminnon miltä tahansa **Sijaintikortti**-sivulta.
3. Valitse **Uusi**-toiminto.
4. Täytä **Sijaintikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voit nyt siirtää varastonimikkeitä sijaintien välillä. Lisätietoja on kohdassa [Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Varastopaikat

Varastopaikkat edustavat varastoinnin perusrakennetta ja niitä käytetään ehdotusten tekemiseksi nimikkeiden sijoittelusta. Kun olet luonut varastopaikat, voit määrittää niiden sisällön. Varastopaikka voi myös toimia määrittelemättömänä varastopaikkana, jolla ei ole määritettyä sisältöä. Varastopaikkoja käytetään pääasiassa varaston perus- ja lisäoperaatioissa. Jos hallitset varastoa yksinkertaisemmassa asetelmassa, et todennäköisesti tarvitse varastopaikkoja.

Jos haluat käyttää varastopaikkatoimintoa sijainnissa, aktivoi toiminto ensin **Sijaintikortti**-sivulla valitsemalla **Varastopaikat pakollisia** -kenttä **Fyysinen varastointi**-pikavälilehdessä. Sitten voi suunnitella nimikevirran sijainnissa määrittämällä varastopaikkakoodit määrityskentistä, jotka edustavat eri virtoja.

> [!NOTE]
> Ennen kuin voit määrittää varastopaikkakoodeja sijainnissa, on luotava varastopaikkakoodit. Lisätietoja on kohdissa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md) ja [Varastopaikkatyyppien määrittäminen](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Alueet

Jos haluat jäsentää varastopaikat alueiden alla, voit tehdä sen **Alueet**-sivulla.

[!INCLUDE [prod_short](includes/prod_short.md)] kopioi tietylle alueelle asetetut kentät alueessa oleville varastopaikoille. Voit määritellä alueen varastopaikalle tai varastopaikkamallille (varastopaikan luontisuodatus), ja sitten muita kenttiä täytetään automaattisesti.

Voit kuitenkin määrittää vain yhden alueen ja järjestellä fyysisen varaston vain varastopaikkojen mukaisesti. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

## <a name="see-also"></a>Katso myös

[Varaston hallinta](inventory-manage-inventory.md)  
[Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)  
[Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md)  
[Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]