---
title: Yrityksen konfiguroinnin määrittäminen | Microsoft Docs
description: Toteutusprosessi alkaa Business Central -ratkaisun edellytyksistä. Yhdistä kaikki tämä tieto konfigurointipakettien tietoihin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: be626aaf9184711bb101c50382f4b85ec394b1ca
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186690"
---
# <a name="set-up-company-configuration"></a>Määritä yrityksen konfigurointi
Toteutus alkaa Microsoft-kumppanin kanssa. Kumppani on vastuussa määritystietojen tarkistamisesta ja helposti asiakkaan käytettävissä olevan paketin luomisesta. Ennen kuin luot uuden yhtiön, suunnittele, miten se määritetään. Ota huomioon perusasennuksen tiedot ja tietotyypit, joita [!INCLUDE[d365fin](includes/d365fin_md.md)] -ratkaisusi edellyttää. Yhdistä kaikki tämä tieto määrityspakettien tietoihin.

RapidStart Services sisältää myös työkalut, joiden avulla voi siirtää vanhat tiedot, kuten asiakkaiden ja toimittajien tiedot.  

On suositeltavaa luoda määrityspaketit, joissa on useimmat asetustaulukot jo täytetty, niin, että asiakkaiden tulee vain muuttaa joitakin asetuksia paketin asentamisen jälkeen. Kun esimerkiksi luot uuden yrityksen, **Nrosarja**- ja **Nrosarjan rivi** -taulukkoon täytetään numerosarjojen ja aloitusnumeroiden joukot. Vastaavat **Nrosarja** -kentät asetustaulukoissa täytetään myös automaattisesti. Sinun ei tarvitse syöttää numerosarjoja ja muita perusasennuksen tietoja. Voi muuttaa myös manuaalisesti kaikki oletustiedot, joita käytetään RapidStart Services -kokoonpanotyökirjan avulla.  

Kokoonpanopaketit on valmistettu esimääritellylle yritykselle. Kun olet määrittänyt yhtiön, joka vastaa tarpeitasi, voit luoda määrityspaketin, joka sisältää tarvittavat tiedot kyseisestä yhtiöstä. Voit sitten käyttää sitä, kun luot uuden yhtiön, joka on määritettävä samalla tavalla.  

Päätietojen, kuten asiakkaan ja toimittajan tietojen tuonnin helpottamiseksi voit käyttää kokoonpanomalleja. Määritysmallit sisältävät oletusasetukset, jotka määritetään automaattisesti tietueisiin, jotka tuodaan kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)].

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Suunnittele yrityksen määritystä täyttämällä määritystyökirja.|[Yrityksen määrittämisen hallinta työkirjassa](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Luo määrityspaketti, mukauta pakettia, liitä pakettiin taulukoita, tarkista olemassa olevat asiakastiedot tai muokkaa niitä, luo uusi yritys ja siirrä sitten testitiedot tuotantoympäristöön.|[Määrityspaketin valmisteleminen](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Katso myös  
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)
