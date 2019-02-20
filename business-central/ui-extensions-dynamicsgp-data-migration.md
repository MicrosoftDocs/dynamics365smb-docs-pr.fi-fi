---
title: "Tietojen siirtäminen Dynamics GP:stä tietojen siirron laajennuksella | Microsoft Docs"
description: "Voit siirtää asiakkaita, toimittajia, varastonimikkeitä, pääkirjanpidon tilejä sekä avoimia ostoreskontran ja myyntireskontran tapahtumia Dynamics GP:stä Business Centraliin Dynamics GP:n tietojen siirron laajennuksella."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 34a6789780fb3d55c0a97b29408dca659992f781
ms.openlocfilehash: 1441e15785b159f7a8c13ee59c8ebea4c32512dc
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2019

---
# <a name="the-dynamics-gp-data-migration-extension"></a>Dynamics GP:n tietojen siirron laajennus 
Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, varastonimikkeitä, pääkirjanpidon tilejä sekä avoimia ostoreskontran ja myyntireskontran tapahtumia Dynamics GP:stä [!INCLUDE[prodshort](includes/prodshort.md)] -sovellukseen. Jos yrityksessä on käytössä Dynamics GP, voit viedä soveltuvat tietueet ja lisätä tiedot [!INCLUDE[prodshort](includes/prodshort.md)] -sovellukseen avaamalla avustetun asennusoppaan. Siirtolaajennusta voi käyttää kaikkien tuettujen Microsoft Dynamics GP -versioiden kanssa. Lisätietoja on kohdassa [Tietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Tietojen vieminen Dynamics GP:stä
Sinun on vietävä tiedostoon osa tai kaikki aiemmin luodut asiakkaat, toimittajat, varastonimikkeet ja pääkirjanpidon tilit Dynamics GP:n tietojen vientitoiminnolla. Vietävien tietojen valitsemisen yhteydessä voidaan valita seuraavia tyyppejä:

* Tili  
* Asiakas  
* Vaihtoehto  
* Toimittaja  

Kun vientitiedosto luodaan, tuloksena on zip-tiedosto, joka sisältää useita txt-tiedostoja. Ne määritetään tietojen vientiprosessin aikana valittujen tietojen perusteella.  Samalla luodaan txt-tiedostoja, jotka sisältävät tukitietoja uuden [!INCLUDE[prodshort](includes/prodshort.md)] -yrityksen määrittämistä varten.

Dynamics GP:n tietojen siirtolaajennus yhdistää viedyt tiedot automaattisesti, joten tiedot ovat nopeasti käytettävissä uudessa [!INCLUDE[prodshort](includes/prodshort.md)]-yritykseen.

## <a name="whats-new-in-the-october-2018-release"></a>Lokakuun 2018 version uudet ominaisuudet

Tässä versiossa Dynamics GP:stä [!INCLUDE[prodshort](includes/prodshort.md)] -sovellukseen tuotavien tietojen määrää on kasvatettu.

Voit nyt valita ohjatussa siirtotoiminnossa Dynamics GP -tilikartan siirtotavan. Voit siirtää olemassa olevan tilikartan tai luoda uuden tilikartan olemassa olevien tilikarttojen perusteella.  

Jos haluat käyttää olemassa olevaa tilikarttaa, tilit määritetään päätilin segmentteinä Dynamics GP:stä ja lisäsegmentit määritetään [!INCLUDE[prodshort](includes/prodshort.md)] -sovelluksen dimensioina.  

Jos luot uuden tilikartan, ohjattu toiminto näyttää tilin lisätietojen sivun. Sen avulla voit ladata työkirjan, tehdä tarpeelliset muutokset ja tuoda työkirjan uudelleen, jotta tilit muutetaan.  

Sinun on ladattava Excel-työkirja ja yhdistettävä uusi tilinumero jokaiseen Excel-laskentataulukon tilinumeroon. Jos jokaisella tilillä ei ole omaa numeroa, siirto päättyy virheeseen. Kun yhdistäminen on tehty, voit jatkaa ohjattua siirtotoimintoa tuomalla juuri lataamasi Excel-työkirjan. Ohjattu toiminto varmistaa, että jokaisella rivillä on yksilöllinen tilinumero ja että riveillä ei ole tyhjiä uusia tilinumeroita.  

Tilikartan yhdistämisasetusten muutoksen vuoksi yleiseen päiväkirjaan tulevien tietojen tyyppi muuttuu tilinumeroiden osalta.  

- Jos haluat käyttää olemassa olevia tilinumeroita, saatavilla on pääsegmentin (uusi tilinumero) aloitussaldo. Se on siirron aikaisen päätilin numeron yhteenveto.  
- Jos haluat luoda uusia tilinumeroita, saatavilla on kahta tilivuotta vastaavien yhteenvetojen tiedot Dynamics GP:ssä määritettyjen tilikausien perusteella.

[!INCLUDE[prodshort](includes/prodshort.md)] -sovelluksen aiemmissa versioissa ohjattu toiminto siirsi Dynamics GP:n asiakkaan/toimittajan saldon yhteenvetotapahtuman. Nyt asiakkaiden ja toimittajien eritellyt avoimet tapahtumat tuodaan siirron yhteydessä. Mitä tämä tarkoittaa? Jos asiakkaalla on kolme avointa tapahtumaa, jotka on rekisteröity Myyntireskontra-moduuliin, ohjattu toiminto tuo nämä tapahtumat [!INCLUDE[prodshort](includes/prodshort.md)] -sovellukseen niin, että avoin summa on asiakirjan summa. Samoin tapahtuu toimittajien Ostoreskontra-moduulissa.  

Varastonimikkeet tuodaan sen kustannusten arvostusmenetelmän avulla, joka valittiin yrityksen ohjatun määritystoiminnon suorituksen yhteydessä. Huoltonimikkeille määritetään automaattisesti FIFO-arvostusmenetelmä. Tällä hetkellä nimikkeille tuodaan varastosaldo siirron yhteydessä.  Tämä määrä tuodaan tyhjään kohtaan.  

Dynamics GP:n ohjatun tietojen siirtotoiminnon viimeinen näytössä oleva asetus on mahdollisuus määrittää oma kirjausvaihtoehto. Tämä asetus määrittää, haluatko kirjata kaikki tapahtumat automaattisesti yleisiin päiväkirjoihin heti, kun ne siirretään siirtotoiminnolla [!INCLUDE[prodshort](includes/prodshort.md)] -sovellukseen, vai haluatko kirjata ne manuaalisesti. Tällöin tapahtumat odottavat yleisen päiväkirjan sivulla erinä, ja voit tarkistaa niiden tiedot ennen kirjaamista. Tämä vaihtoehto on näkyvissä tilikartan asetusten sivulla.


## <a name="see-also"></a>Katso myös
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prodshort](includes/prodshort.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  

