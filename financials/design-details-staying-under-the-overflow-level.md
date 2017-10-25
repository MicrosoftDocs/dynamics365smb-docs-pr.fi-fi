---
title: "Rakennetiedot – Sallitun ylityksen alapuolella pysytteleminen | Microsoft Docs"
description: "Kun käytössä on Enimmäismäärä ja Kiinteä uusintatil. määrä suunnittelujärjestelmä keskittyy oletettuun varastoon vain annetulla aikavälillä. Tämä tarkoittaa sitä, että suunnittelujärjestelmä voi ehdottaa tarpeetonta tarjontaa, kun annetun aikavälin ulkopuolella tapahtuu negatiivisia tai positiivisia tarjonnan muutoksia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bbfafc41f22a5582b90683bdacf8135e78e46843
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-staying-under-the-overflow-level"></a>Rakennetiedot: sallitun ylityksen alapuolella pysytteleminen
Kun Enimmäismäärä- ja Kiinteä uusintatil. määrä -käytäntöjä käytetään, suunnittelujärjestelmä keskittyy oletettuun varastoon vain annetulla aikavälillä. Tämä tarkoittaa sitä, että suunnittelujärjestelmä voi ehdottaa tarpeetonta tarjontaa, kun annetun aikavälin ulkopuolella tapahtuu negatiivisia tai positiivisia tarjonnan muutoksia. Jos tästä syystä ehdotetaan tarpeetonta tarjontaa, suunnittelujärjestelmä laskee mihin määrään tarjonta tulee vähentää (tai poistaa) tarpeettoman tarjonnan välttämiseksi. Tätä määrää kutsutaan ylivuototasoksi. Ylitys ilmoitetaan suunnittelurivinä, jossa on **Muuta määrä (vähennys)**- tai **Peruuta**-toiminto, ja seuraava varoitusviesti:  

*Huomio: arvioitu varastomäärä [xx] on korkeampi kuin sallittu ylitys [xx] [xx] eräpäivänä [xx].*  

![Varaston ylivuototaso](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")  

##  <a name="calculating-the-overflow-level"></a>Lasketaan sallittua ylitystä  
Ylitystaso lasketaan eri tavoin riippuen suunnitteluasetuksista.  

### <a name="maximum-qty-reordering-policy"></a>Enimmäismäärä-uusintatilaustapa  
Sallittu ylitys = enimmäisvarasto  

> [!NOTE]  
>  Jos vähimmäistilausmäärä on olemassa, se lisätään seuraavasti: sallittu ylitys = enimmäisvarasto + vähimmäistilausmäärä.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Kiinteän uusintatilausmäärän uusintatilaustapa  
Sallittu ylitys = uusintatilausmäärä + uusintatilauspiste  

> [!NOTE]  
>  Jos vähimmäistilausmäärä on korkeampi kuin uusintatilauspiste, se korvaa seuraavasti: sallittu ylitys = uusintatilausmäärä + vähimmäistilausmäärä  

### <a name="order-multiple"></a>Tilauskerrannainen  
Jos tilauskerrannainen on olemassa, se säätää sekä enimmäismäärän että kiinteän uusintatilaustavan sallittua ylitystä.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>Suunnittelurivin luominen ylitys-varoituksella  
Suunnittelurivi luodaan, kun oletettu varasto on aikavälin lopussa suurempi kuin sallittu ylitys olemassa olevan tarjonnan vuoksi. Kun mahdollisesta tarpeettomasta tarjonnasta varoitetaan, suunnittelurivillä on varoitusviesti, **Hyväksy toimenpideviesti** -kenttää ei ole valittu ja toimenpideviesti on Peruuta tai Muuta määrä.  

### <a name="calculating-the-planning-line-quantity"></a>Lasketaan suunnittelurivin määrää  
Suunnittelurivin määrä = nykyisen tarjonnan määrä (oletettu varasto – sallittu ylitys)  

> [!NOTE]  
>  Kuten kaikkien varoitusrivien kohdalla, kaikki tilauksen enimmäis-/vähimmäismäärät ohitetaan.  

### <a name="defining-the-action-message-type"></a>Toimintoviestin tyypin määrittäminen  

-   Jos suunnittelurivin määrä on suurempi kuin 0, toimenpideviesti on Muuta määrä  
-   Jos suunnittelurivin määrä on yhtä suuri tai pienempi kuin 0, toimenpideviesti on Peruuta  

### <a name="composing-the-warning-message"></a>Varoitusviestin luonti  
Ylivuodon tapauksessa **Ei-seuratut suunnitteluelementit** -ikkunassa on varoitusviesti, jossa on seuraavat tiedot:  

-   Käsitelty varastotaso, joka laukaisi varoituksen  
-   Laskettu ylitystaso  
-   Tarjontatapahtuman eräpäivä.  

Esimerkki: Suunniteltu varasto 120 on suurempi kuin sallittu ylitys 60 kohteessa 28-01-11.  

## <a name="scenario"></a>Esimerkkitilanne  
Tässä tilanteessa asiakas muuttaa myyntitilauksen arvosta 70 kappaletta arvoksi 40 kappaletta suunnitteluajojen välillä. Ylitystoiminto alkaa vähentämään tilausta, jota ehdotettiin alkuperäiselle myyntimäärälle.  

### <a name="item-setup"></a>Nimikkeen asetus  

|Uusintatilaustapa|Enimmäismäärä|  
|-----------------------|------------------|  
|Enimmäistilausmäärä|100|  
|Uusintatilauspiste|50|  
|Varasto|80|  

### <a name="situation-before-sales-decrease"></a>Tilanne ennen myynnin vähenemistä  

|Tapahtuma|Muuta määrä|Suunniteltu varasto|  
|-----------|-----------------|-------------------------|  
|Yksi päivä|Ei mitään|80|  
|Myynti|-70|10|  
|Aikavälin loppu|Ei mitään|10|  
|Ehdota uutta ostopalautustilausta|+90|100|  

### <a name="situation-after-sales-decrease"></a>Tilanne myynnin vähenemisen jälkeen  

|Vaihtoraha|Muuta määrä|Suunniteltu varasto|  
|------------|-----------------|-------------------------|  
|Yksi päivä|Ei mitään|80|  
|Myynti|-40|40|  
|Osto|+90|130|  
|Aikavälin loppu|Ei mitään|130|  
|Ehdotus tilauksen pienentämiseksi<br /><br /> tilaus arvosta 90 arvoon 60|-30|100|  

### <a name="resulting-planning-lines"></a>Tuloksena suunnittelurivit  
 Järjestelmä luo yhden suunnittelurivin (varoitus) oston vähentämiseksi 30 yksiköllä 90 yksiköstä 60 yksikköön, jotta arvioitu varasto on 100 sallitun ylityksen mukaan.  

![Suunnittelu ylivuototason mukaisesti](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")  

> [!NOTE]  
>  Ilman ylivuototoimintoa varoitusta ei luoda, jos oletetun varaston taso ylittää enimmäisvaraston. Tämä voi aiheuttaa tarpeettoman tarjonnan, joka on 30.  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: Uusintatilauskäytännöt](design-details-reordering-policies.md)   
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)

