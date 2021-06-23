---
title: Sijaintikortin ja siirtoreittien määrittäminen
description: Jokaisille varastoitavalle varastonimikkeelle luodaan sijaintikortti, kuten varasto tai jakelukeskus. Lisäksi sijaintien välille määritetään siirtoreitit.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184322"
---
# <a name="set-up-locations"></a>Sijaintien määrittäminen

Jos ostat, varastoit tai myyt nimikkeitä useamman varaston avulla, sijaintikortti ja siirtoreitit on määritettävä jokaiselle sijainnille. [!INCLUDE [prod_short](includes/prod_short.md)] käyttää sijainteja varaston seurannassa sekä yksinkertaisemmissa tapauksissa että monimutkaisemmissa varastoprosesseissa.

Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen. Lisätietoja on myös kohdassa [Varaston hallinta](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Sijaintikortit

Sijaintikortissa määritetään tietoja sijainnista, esimerkiksi fyysisestä varastosta tai jakelukeskuksesta. Kullekin sijainnille annetaan sijaintia kuvaava nimi ja koodi. Tämän jälkeen sijaintikoodin voi syöttää muualle ohjelmaan silloin, kun haluat tallentaa transaktioita tietylle sijainnille.  

Voit syöttää tietoja varastopaikasta ja fyysisen varaston periaatteista jokaiselle sijainnille. Valitsemiesi fyysisen varaston periaatteiden perusteella voit määrittää **Varastopaikat**-pikavälilehden vaihtoehtojen avulla varastopaikat, joita käytetään oletusvarastopaikkoina toteutettaessa tapahtumia. Jos käytät ohjattua hyllytystä ja poimintaa, voit määrittää **Var.paikkojen periaatteet** -pikavälilehden vaihtoehtojen avulla, miten haluat käyttää fyysisen varaston eri lisäominaisuuksia.  

Jotkut vaihtoehtokentät ovat harmaana ja poissa käytöstä muiden asetusten vuoksi **Sijaintikortti**-sivulla. Tällä rajoitetaan asetusyhdistelmiä, joita ei tueta.  

Valitse toiminto **Alueet** tai **Varastopaikat** nähdäksesi tiedot alueista ja varastopaikoista, jotka voidaan määrittää sijaintiin.

### <a name="to-create-a-location-card"></a>Sijaintikortin luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sijainnit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Sijaintikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.

> [!NOTE]  
> Monet sijaintikortin kentät viittaavat saapuvien ja lähtevien varastoprosessien nimikkeiden käsittelyyn. Kentät eivät ole olennaisia yrityksille, jotka eivät tarvitse monimutkaisempaa varastotoimintoa. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Voit muuttaa sijainnin määritystä myöhemmin, mutta et voi muokata asetuksia niille sijainneille, joilla on kirjanpitotapahtumia.  

Jos sinulla on useampia sijainteja, seuraavaksi voit määrittää sijaintien välisiä siirtoreittejä.  

### <a name="to-create-a-transfer-route"></a>Siirtoreittien luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Siirtoreitit** ja valitse sitten liittyvä linkki.
2. Voit myös valita **Siirtoreitit**-toiminnon miltä tahansa **Sijaintikortti**-sivulta.
3. Valitse **Uusi**-toiminto.
4. Täytä **Sijaintikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voit nyt siirtää varastonimikkeitä sijaintien välillä. Lisätietoja on kohdassa [Varastonimikkeiden siirtäminen sijantien välillä](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Varastopaikat

Varastopaikkat edustavat varastoinnin perusrakennetta ja niitä käytetään ehdotusten tekemiseksi nimikkeiden sijoittelusta. Kun olet luonut varastopaikat, voit määrittää tarkasti sisällön, jonka haluat ohjelman sijoittavan kuhunkin varastopaikkaan, tai varastopaikka voi toimia määrittelemättömänä varastopaikkana, jolla ei ole määritettyä sisältöä. Varastopaikkoja käytetään pääasiassa varaston perus- ja lisäoperaatioissa. Jos hallitset varastoa yksinkertaisemmassa asetelmassa, et todennäköisesti tarvitse varastopaikkoja.

Jos haluat käyttää varastopaikkatoimintoa sijainnissa, aktivoi toiminto ensin **Sijainti**-kortissa valitsemalla **Varastopaikat pakollisia** -kenttä **Fyysinen varastointi**-pikavälilehdessä. Sitten voi suunnitella nimikevirran sijainnissa määrittämällä varastopaikkakoodit määrityskentistä, jotka edustavat eri virtoja.

> [!NOTE]
> Ennen kuin voit määrittää varastopaikkakoodeja sijaintikortissa, on luotava varastopaikkakoodit.

Lisätietoja on kohdissa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md) ja [Varastopaikkatyyppien määrittäminen](warehouse-how-to-set-up-bin-types.md).  

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