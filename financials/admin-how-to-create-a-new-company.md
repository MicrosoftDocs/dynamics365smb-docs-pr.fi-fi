---
title: Uuden yrityksen luominen | Microsoft Docs
description: "RapidStart Services -palvelun käyttämisessä tarvittavat taulukot ja sivut luodaan, mutta niissä ei ole tietoja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c07b7c4e6b1c82004295a187184a6f3ccb4c7c7
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-new-company"></a>Uuden yrityksen luominen
Kun haluat käyttää RapidStart Services -palvelua [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa, luo ensin uusi yritys, jossa asiakkaan käyttöönotto suoritetaan. Kun luot uuden yhtiön, standardi [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukot ja sivut luodaan, mutta niissä ei ole tietoja.

Voit lisäksi ottaa yrityksessä käyttöön tietyt asetustiedot alustamisen jälkeen. Tiedot esitetään kokoonpanopaketissa, .rapidstart-tiedostossa, joka tarjoaa sisältöä pakatussa muodossa.  

Määrityspakettien esimerkit, mukaan lukien maa-/aluekohtaiset tiedostot, sisältyvät CRONUS-esittely-yritykseen. Käytä seuraavia toimenpiteitä käyttääksesi esimerkki määrityspakettia uuden yrityksen kanssa.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>BASICCONFIG-esimerkkimäärityspaketin käyttäminen  
1. Avaa CRONUS Finland Oy -yritys. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).
2. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Määrityspaketit** ja valitse sitten aiheeseen liittyvä linkki.  
3. Valitse BASICCONFIG-paketti luettelosta ja valitse sitten **Vie paketti** -toiminto.  

Luo seuraavan menettelyn avulla uusi yritys ja käytä BASICCONFIG-pakettia prosessin osana.  

## <a name="to-create-a-new-company"></a>Luo uusi yritys  
1. Luo uusi yritys. Lisätietoa on kohdassa [Uusien yritysten luominen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa](about-new-company.md).
2. RapidStart Services -palvelun käyttöönottajan roolikeskukseen voi nyt tuoda määrityspaketin, joka vietiin CRONUS Finland Oy -yrityksestä.

Kun luot uuden yhtiön, joitakin taulukoita täytetään automaattisesti, vaikka yhtiömallia ei ole käytössä. Voit esimerkiksi tarkastella kirjauksen ja erätapahtumien vakiokoodeja **Lähdekoodi**-ikkunassa. Jos määrität [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman paikallisen version, tarkista tämä taulukko ja ota huomioon mahdolliset ongelmat paikallisen kielen kanssa.

## <a name="about-data-tables"></a>Tietoja tietotaulukoista
[!INCLUDE[d365fin](includes/d365fin_md.md)] -arvotaulukoita on kaksi perustyyppiä: pää- ja asetustaulukot. Kun määrität yrityksen kokoonpanoa, voit käyttää näitä tyyppejä keskittyäksesi kokoonpanostrategiaasi.  

### <a name="master-data-tables"></a>Päätietotaulukot  
Seuraavassa taulukossa on joitakin esimerkkejä päätietotaulukoista. Kun alustat uuden yrityksen, nämä taulut ovat tyhjät.  

|Taulukon nro|Taulukon nimi|  
|-------------------|--------------------|  
|15|KP-tili|  
|18|Asiakas|  
|23|Toimittaja|  
|27|Vaihtoehto|  
|5050|Kontakti|  

### <a name="setup-data-tables"></a>Tietotaulukoiden asetukset  
Seuraavassa taulukossa on joitakin asennustaulukoita, joihin siepataan asetustietoja määrityskyselylomakkeesta. Nämä taulukot sisältävät perustietoja ajalta, jolloin yritys luotiin.  

|Taulukon nro|Taulukon nimi|  
|-------------------|--------------------|  
|98|Pääkirjanpidon asetukset|  
|311|Myyntien ja myyntisaamisten asetukset|  
|312|Ostojen ja ostovelkojen asetukset|  
|313|Varastonhallinnan asetukset|  

[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää asetustietotaulukoiden lisäksi myös asetustyyppisiä tietotaulukoita, jotka määrittävät yrityksen ja sen liiketoimintaprosessien perustiedot. Seuraavassa taulukossa esitellään osa niistä.  

|Taulukon nro|Taulukon nimi|  
|-------------------|--------------------|  
|3|Maksuehdot|  
|4|Valuutta|  
|6|Asiakashintaryhmät|  
|5700|Varastointiyksikkö|

  

## <a name="see-also"></a>Katso myös  
[Kokoonpanojen käyttäminen uusissa yrityksissä](admin-apply-configuration-to-new-companies.md)  
[Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)

