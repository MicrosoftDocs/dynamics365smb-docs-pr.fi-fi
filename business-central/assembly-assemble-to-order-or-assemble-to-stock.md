---
title: Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista | Microsoft Docs
description: Kokoonpanonimikkeet voidaan toimittaa joko kokoamalla ne tilauksen yhteydessä tai kokoamalla ne varastoon odottamaan myyntitilausta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: a8b5ab66b680b6c49226e308e6f2e17a0c2604f9
ms.sourcegitcommit: 6200a08e91d507bab01d1d5b805fe8ea3f44a58a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2020
ms.locfileid: "3496798"
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista
Kokoonpanon osat voidaan toimittaa seuraavaan kahteen prosessiin:  

-   Kokoonpano tilausta varten.  
-   Kokoonpano varastoon.  

## <a name="assemble-to-order"></a>Kokoonpano tilausta varten  
Käytät yleensä *Kokoonpano tilausta varten* nimikkeille, joita et halua varastoida, koska oletat mukauttavasti ne asiakkaan pyyntöjä astaaviksi tai koska haluat pienentää varastokustannuksia toimittamalla juuri ajoissa. Tukitoimintoja ovat seuraavat:  

-   Kyky mukauttaa kokoonpanon nimikkeet myyntitilauksen ottamisen yhteydessä.  
-   Yleiskuvaus kokoonpanonimikkeen ja sen komponenttien saatavuudesta.  
-   Kyky varata kokoonpanon osat heti, jotta tilauksen toteutuminen voidaan taata.  
-   Funktio, jota käytetään mukautetun tilauksen kannattavuuden määrityksessä hinnan ja kustannuksen vyörytyksen avulla.  
-   Integrointi fyysiseen varastoon kokoonpanon ja toimituksen helpottamiseksi.  
-   Kyky koota tilaus myyntitarjouksen tai puitetilauksen yhteydessä.  
-   Kyky yhdistää varastomäärät kokoonpano tilausta varten -määrien kanssa.  

Kokoonpano tilausta varten -käsittelyssä nimike kootaan vastauksena myyntitilaukseen ja kahdenvälisenä kokoonpanotilauksen ja myyntitilauksen välisenä linkkinä.  

Kun syötät myyntiriville kokoonpano tilausta varten nimikkeen, kokoonpanotilaus luodaan automaattisesti otsikolla, joka perustuu myyntiriviin ja riveillä, jotka perustuvat nimikkeen kokoonpanon tuoterakenteeseen kerrottuna tilausmäärällä. Voit käyttää **Kokoonpano tilausta varten -rivit** -sivua nähdäksesi linkitetyt kokoonpanotilausrivit tukeaksesi muokkaamaan kokoonpanon nimikettä ja toimituspäivää, joka perustuu osan saatavuustietoihin. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Vaikka se ei ole osa oletusprosessia, voit myydä varastomääriä kokoonpano tilausta varten -määrillä. Lisätietoja on kohdassa [Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

 Ottaaksesi tämän prosessin käyttöön **Kokoonpanokäytäntö** -kentän nimikekortissa on oltava **Kokoonpano tilausta varten**.  

## <a name="assemble-to-stock"></a>Kokoonpano varastoon  
 Käytät yleensä *kokoonpano varastoon* nimikkeille, jotka haluat koota ennen myyntiä, kuten valmistauta kampanjapakettiin ja pitää varastossa, kunnes ne on tilattu. Nämä kohteet ovat yleensä vakiokohteita, kuten pakattuja sarjoja, joita ei tarjota asiakkaalle heidän pyyntöjensä mukauttamiseksi.  

 Kokoonpano varastoon -käsittelyssä nimike kootaan ilman välitöntä myyntikysyntää ja varastoidaan fyysiseen varastoon varastonimikkeenä myöhempää myyntiä varten tai osakokoonpanona kulutettavaksi. Lisätietoja on kohdassa [Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md). Tästä eteenpäin nimike poimitaan ja sitä käsitellään yksittäisenä nimikkeenä. Sitä kohdellaan valmiina tuotantonimikkeenä.  

 Kun syötät myyntiriville kokooknpano varastoon nimikkeen, kuten minkä tahansa muun nimikkeen, joka on myyty varastosta. Esimerkiksi saatavuus tarkistetaan vain kokoonpanon nimikkeen osalta.  

> [!NOTE]  
>  Vaikka se ei ole osa oletusprosessia, voit koota nimikkeen tilattavaksi, vaikka se on määritetty kokoonpantavaksi varastoon. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden ja -varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

 Ottaaksesi tämän prosessin käyttöön **Kokoonpanokäytäntö** -kentän nimikekortissa on oltava **Kokoonpano varastoon**.  

## <a name="combination-scenarios"></a>Skenaarioiden yhdistelmä  
 Kokoonpanon hallinnan yleinen periaate on se, että yhdistettäessä myyntitilauksen riville, kokoonpano tilausta varten on lähetettävä ennen varaston määriä.  

 Jos kokoonpanotilaus on linkitetty myyntitilauksen riville, tilausrivin **Kokoonpantava määrä tilausta varten** -kentän arvo kopioidaan **Kokoonpantava määrä** -kenttään kokoonpanotilauksen otsikon **Määrä** -kentän välityksellä. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

 Lisäksi **Kokoonpantava määrä** -kentän arvo liittyy myyntitilausrivin **Toimitettava määrä** -kenttään. Tämä suhde hallitsee Kokoonpano tilausta varten -määrien toimitusta sekä osittaisen että koko määrän toimituksessa. Tämä pätee sekä silloin, kun koko myyntirivin määrä kootaan tilauksesta, että yhdistelmätilanteissa, jossa osa myyntirivin määrää kootaan tilauksesta ja toinen osa toimitetaan varastosta. Yhdistelmätilanne on kuitenkin joustava, kun toimitus tehdään osissa. Voit muokata **Kokoonpantava määrä** -kenttää ennalta määritettyjen sääntöjen mukaisesti ja määrittää, miten monta yksikköä toimitetaan osittain varastosta ja miten monta yksikköä kokoonpano tilausta varten -menetelmällä.  

 Jos myyntirivin koko määrä on koottava tilausta varten ja toimitettava, **Toimitettava määrä** -kentän arvo kopioidaan linkitetyn kokoonpanotilauksen **Kokoonpantava määrä** -kenttään toimitettavan määrän muuttuessa. Tämä varmistaa, että toimitettu määrä on täysin kokoonpano tilausta varten -määrän mukainen.   

 Yhdistelmätilanteissa **Toimitettava määrä** -kentän koko arvoa ei kuitenkaan kopioida kokoonpanotilauksen otsikon **Kokoonpantava määrä** -kenttään. Sen sijaan oletusarvo lisätään **Kokoonpantava määrä** -kenttään, joka lasketaan **Toimitettava määrä** -kentästä ennalta määritetyn säännön mukaan. Se varmistaa Kokoonpano tilausta varten -määrien toimittamisen ensin.  

 Jos haluat muuttaa oletusarvoa, koska haluat esimerkiksi suurentaa tai pienentää kokoonpanon määrää **Toimitettava määrä** -kentässä, voit muokata **Kokoonpantava määrä** -kenttää alla olevien ennalta määritettyjen sääntöjen mukaisesti.  

 Voit esimerkiksi muokata kokoonpanomäärää, jos haluat kirjata varastomäärän toimituksen osittain, ennen kuin koko kokoonpanomäärä voidaan toimittaa.  

 Seuraavassa taulukossa käsitellään sääntöjä, joilla määritetään pienin ja suurin **Kokoonpantava määrä** -kenttään annettava arvo, kun halutaan poiketa yhdistelmätilanteen oletusarvosta. Taulukossa näkyy yhdistelmätilanne, jossa linkitetyn myyntitilausrivin arvo **Toimitettava määrä** -kentässä muutetaan 7:stä 4:ksi, ja **Kokoonpantava määrä** -oletusarvoksi tulee sen vuoksi 4.  

||Myyntitilausrivi|Kokoonpanotilauksen otsikko|  
|-|----------------------|---------------------------|  
||**Määrä**|**Toimitettava määrä**|**Kokoonpantava määrä tilausta varten**|**Toimitettu määrä**|**Määrä**|**Kokoonpantava määrä**|**Kokoonpantu määrä**|**Jäljellä oleva määrä**|  
|Alku|10|7|7|0|7|7|0|7|  
|Vaihtoraha||4||||4 (lisätään oletusarvon mukaan)|||  

 Edellä mainitun tilanteen perusteella voit muuttaa vain **Kokoonpantava määrä** -kentän seuraavasti:  

-   Pienin määrä, joka voidaan syöttää on 1. Tämä johtuu siitä, että ainakin yksi yksikkö on koottava, jotta voit myydä neljä yksikköä, olettaen, että loput kolme ovat saatavilla varastossa.  
-   Suurin määrä, joka voidaan syöttää on 4. Näin varmistetaan, että tilaukselle ei koota enempää nimikkeitä kuin mitä myyntiin tarvitaan.  

## <a name="see-also"></a>Katso myös  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
