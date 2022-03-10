---
title: 'Toimintaohje: varastonimikkeiden myyminen kokoonpano tilausta varten -virroissa'
description: Jos nimikkeessä on kokoonpano tilausta varten -määritys, nimike on koottava myyntitilauksia varten, ja linkitetty kokoonpanotilaus luodaan automaattisesti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 2d68bb10c6ff7d153417dbdc491dd8abd75b7adc
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146954"
---
# <a name="selling-inventory-items-in-assemble-to-order-flows"></a>Varastonimikkeiden myyminen kokoonpano tilausta varten -virroissa
Jos kokoonpanon nimikkeen kortin **Kokoonpanokäytäntö**-kenttä sisältää **Kokoonpano tilausta varten** -kohdan, myyntitilauksen oletusprosessi olettaa, että nimikettä ei ole varastossa, vaan se on koottava tätä tiettyä myyntitilausta varten. Tämän vuoksi linkitetyn kokoonpanon tilaus luodaan automaattisesti, kun kohde lisätään myyntitilauksen riville. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md). Jos osa myyntitilauksen määrästä on jo saatavana varastossa, voit pienentää kokoonpanotilauksen määrää muuttamalla myyntitilausrivin **Kokoonpantava määrä tilausta varten** -kentän arvoa.  

Tämä esimerkki on harvinainen, koska kokoonpano tilausta varten -nimikkeiden oletetaan aina olevan mukautettuja, ja se mahdollisuus, että ne ovat fyysisessä varastossa toisen asiakkaan pyytämässä kokoonpanossa, on pieni. Jos yrityksellä kuitenkin on varastossa kokoonpano tilausta varten -määriä palautusten tai tilausten peruutusten vuoksi, nämä määrät on kerättävä ja myytävä ennen uusien kokoonpanoa.  

> [!NOTE]  
>  Toimintoa ei ole myyntitilauksissa, jotka ilmoittavat automaattisesti tai auttavat vähentämään jo saatavissa olevia kokoonpanotilauksen määriä. Sen sijaan sinun on valvottava saatavuustietoja, kuten **Myyntirivin tiedot** -tietoruutua.  

Vastaava toiminto on käytettävissä, kun myyt kokoonpanon nimikkeitä varastosta ja jotkut tai kaikki niistä eivät ole käytettävissä, ja ne voidaan toimittaa kokoonpanotilauksella. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden ja -varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
>  Tietyt säännöt koskevat **Toimitettava määrä** -kenttää myyntitilauksen riveillä, jotka sisältävät Kokoonpano tilausta varten -määrien ja varaston määrien yhdistelmiä. Lisätietoja on ohjeaiheen [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md) kohdassa Skenaarioiden yhdistelmä.  

Tässä toimenpiteessä korvaat tilausta varten kokoonpantavat määrät myyntitilauksen rivin varastomäärillä. Vaiheita ovat saatavuuden havaitseminen, määrän päätteleminen linkitetystä kokoonpanotilauksesta ja sen jälkeen varastomäärän varaaminen sen varmistamiseksi, että se poimitaan ja toimitetaan tilaukseen.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Myy varastonimikkeidtä kokoonpano tilausta varten -virroissa  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2.  Luo myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  
3.  Anna kokoonpano tilausta varten -nimikkeen myyntitilausrivn **Määrä**-kenttään kysyntämäärä.  
4.  Määritä **Myyntirivin tiedot** -tietoruudussa, onko koko kysyntämäärä tai osa kysyntämäärästä saatavilla.  
5.  Vähennä **Kokoonpantava määrä tilausta varten** -kentässä saatavilla olevaa määrää niin, että ei saatavilla oleva määrä kootaan tilaukseen. **Varattu määrä** -kenttä väheni vastaamaan sitä, että tilauksesta-tilaukseen -linkki tai varaus koskee vain koottavaa määrää.  
6.  Valitse **Rivit**-pikavälilehdessä ensin **Toiminnot** ja sitten **Varaa**-toiminto.  
7.  Valitse **Varaus**-sivulla nimiketapahtumarivit, joilla saatavilla olevat määrät ovat. Valitse sitten **Varaa nykyiseltä riviltä** -toiminto ja lopuksi **OK**.  

    **Myyntitilaus**-sivun **Varausmäärä**-kentässä näkyy nyt, että tilausrivin koko määrä on varattu. **Kokoonpantava määrä tilausta varten** -kentässä näkyy edelleen, on koottava alatuotteen määrä.  

8.  Vapauta myyntitilaus varastonimikkeiden poimintaan ja ei käytettävissä olevien kohteiden kokoonpanoon. Lisätietoja on kohdassa [Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Myyntitilauksen **Varastopaikkakoodi**-kenttä voidaan tarvittaessa esitäyttää sijaintikortin **Kokoonpanot. toim. var.p.koodi**- tai **Kokoonpanosta-varastop.koodi** -kentästä. Tässä tapauksessa myyntitilauksen rivin **Varastopaikkakoodi**-kentän arvo saattaa olla virheellinen tässä Kokoonpano tilausta varten -määrän ja Kokoonpano varastoon -määrän yhdistelmässä. On hyvä tarkistaaa **Varastopaikkakoodi**-kenttä ja varmistaa, että paikka sopii kaikille määrille. Voit myös kirjoittaa kaksi eri määrää myyntitilauksen eri riveille.  

## <a name="see-also"></a>Katso myös  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Nimikkeiden varaaminen](inventory-how-to-reserve-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]