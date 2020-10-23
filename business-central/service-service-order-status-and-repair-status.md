---
title: Huoltotilauksen tila ja korjauksen tila | Microsoft Docs
description: Huoltotilaus-sivun Tila-kentällä (huoltotilauksen tilalla) ja Huoltotilaus-sivun Korjauksen tilakoodi -kentällä on tietty yhteys huoltohallinnon kohdistusalueella. Huoltotilauksen tila kuvastaa kaikkien huoltotilauksessa olevien huoltonimikkeiden korjauksen tilaa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 638b1f560dc28374e0e8d5afbc94f6ef8d416c83
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913144"
---
# <a name="service-order-status-and-repair-status"></a>Huoltotilauksen tila ja korjauksen tila
**Huoltotilaus**-sivun **Tila**-kentällä (huoltotilauksen tilalla) ja **Huoltotilaus**-sivun **Korjauksen tilakoodi** -kentällä on tietty yhteys huoltohallinnon kohdistusalueella. Huoltotilauksen tila kuvastaa kaikkien huoltotilauksessa olevien huoltonimikkeiden korjauksen tilaa.  

> [!NOTE]  
>  Nämä kaksi tilakenttää eivät liity huoltotilausotsikon **Vapautustila**-kenttään, joka määrittää sen, miten fyysinen varasto käsittelee huoltonimikkeitä.  

 Kun huoltotilauksessa olevan huoltonimikkeen korjauksen tilaa muutetaan, ohjelma päivittää huoltotilauksen tilan. Jotta ohjelma voisi näyttää tilan, joka kuvastaa yksittäisten huoltonimikkeiden korjauksen kokonaistilaa, seuraavat tulee määritellä:  

* Huoltotilauksen tila, johon kukin korjauksen tila on linkitetty. Lisätietoja on ohjeaiheessa Huoltotilauksen tila.  
* Kunkin huoltotilauksen tilavaihtoehdon prioriteettitaso. Lisätietoja on kohdassa Prioriteetti.  

 Kun huoltotarjous muunnetaan huoltotilaukseksi, ohjelma muuttaa jokaisen tilauksessa olevan huoltonimikkeen korjauksen tilaksi **Alku** ja huoltotilauksen tilaksi **Odottava**.  

## <a name="specifying-service-order-status-for-repair-status"></a>Huoltotilauksen tilan määrittäminen korjauksen tilaa varten  
Jokainen korjauksen tila on linkitetty tiettyyn huoltotilauksen tilaan. Huoltotilauksen tilan vaihtoehdot ovat **Odottava**, **Työn alla**, **Estossa** ja **Valmis**. Korjauksen tilan vaihtoehtoja ovat seuraavat: **Alku**, **Työn alla**, **Lykätty**, **Osittain huollettu**, **Tarjous valmis**, **Odotetaan asiakasta**, **Varaosa tilattu**, **Varaosa vastaanotettu** ja **Valmis**.  

### <a name="pending"></a>Odottava  
Huoltotilauksen tila **Odottava** tarkoittaa sitä, että huolto voi alkaa tai jatkua milloin tahansa. Tämän vuoksi korjauksen tilan vaihtoehdot **Alku**, **Lykätty**, **Osittain huollettu** ja **Varaosa vastaanotettu** voidaan kaikki linkittää kyseiseen huoltotilauksen tilaan.  

### <a name="in-process"></a>Työn alla  
Huoltotilauksen tila **Työn alla** tarkoittaa sitä, että huolto on käynnissä. Tämän vuoksi korjauksen tilan vaihtoehdot **Työn alla** ja **Varaosa tilattu** voidaan molemmat linkittää kyseiseen huoltotilauksen tilaan. Jos **Varaosa tilattu** -tila linkitetään huoltotilauksen **Työn alla** -tilaan, myös **Varaosa vastaanotettu** -tila tulee linkittää tähän huoltotilauksen tilaan.  

### <a name="on-hold"></a>Estossa  
Huoltotilauksen tila **Estossa** tarkoittaa sitä, että huolto on tällä hetkellä estossa, koska ennen huollon aloittamista täytyy odottaa asiakkaan vastausta tai varaosia. Tämän vuoksi korjauksen tilan vaihtoehdot **Tarjous valmis**, **Varaosa tilattu** ja **Odotetaan asiakasta** voidaan kaikki linkittää kyseiseen huoltotilauksen tilaan.  

### <a name="finished"></a>Valmis  
Huoltotilauksen tila **Valmis** tarkoittaa sitä, että huolto on suoritettu loppuun. Tämän vuoksi korjauksen tila **Valmis** on linkitetty kyseiseen tilaan.  

## <a name="assigning-priority-to-service-order-status"></a>Prioriteetin määritteleminen huoltotilauksen tilalle  
Kun muutat (tai ohjelma muuttaa) huoltonimikkeen korjauksen tilaa, ohjelma etsii huoltotilauksen tilan vaihtoehdot, jotka on linkitetty kaikkien tilauksessa olevien huoltonimikkeiden eri korjauksen tilan vaihtoehtoihin. Jos huoltonimikkeet on linkitetty kahteen tai useampaan huoltotilauksen tilan vaihtoehtoon, ohjelma valitsee huoltotilauksen tilan, jolla on korkein prioriteetti.  

Sinun täytyy päättää, mikä huoltotilauksen tila sisältää tärkeimmät tiedot huoltotilauksen tilasta, ja määritellä kyseiselle tilalle korkein prioriteetti ja niin edelleen.  

### <a name="example"></a>Esimerkki  
Tavallinen prioriteettitason määrittely voisi olla seuraavanlainen:  

* Työn alla - Korkea  
* Odottava - Melko korkea  
* Estossa - Melko matala  
* Valmis - Matala  

Esimerkiksi jos yhdellä huoltonimikkeellä on korjauksen tilana **Alku** (joka on linkitetty huoltotilauksen tilaan **Odottava**), toisella tilana on **Työn alla** (joka on linkitetty huoltotilauksen tilaan **Työn alla**) ja kolmannella **Varaosa tilattu** (joka on linkitetty huoltotilauksen tilaan **Estossa**), seurauksena syntyvä huoltotilauksen tila on **Työn alla**, koska sillä on korkein prioriteetti.  

## <a name="see-also"></a>Katso myös  
[Huoltotilausten ja -korjausten tilan määrittäminen](service-order-repair-status.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
