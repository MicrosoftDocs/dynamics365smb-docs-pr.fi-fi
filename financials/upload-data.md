---
title: Vanhojen liiketoimintatietojen tuominen Financialsiin | Microsoft Docs
description: "Tässä artikkelissa kerrotaan, miten omat tiedot tuodaan Dynamics 365 for Financialsiin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migrate, initialize, implement
ms.date: 04/27/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 001dccf7935f38dd2f409e4fea31598a279472d4
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="importing-business-data-from-other-finance-systems"></a>Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä
Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, voit luoda tyhjän yrityksen, ladata siihen omat tietosi ja testata uuden [!INCLUDE[d365fin](includes/d365fin_md.md)]-yrityksesi. Yrityksen tällä hetkellä käytössä olevan rahoitusratkaisun mukaan voit siirtää tietoja asiakkaista, toimittajista, varastosta ja pankkitileistä.  

Kotisivulla olevan avustetun asennusoppaan avulla voit siirtää liiketoimintatiedot Excel-tiedostosta tai muista muodoista. Ladattavissa olevien tiedostojen tyyppi riippuu käytettävissä olevista laajennuksista. Voit esimerkiksi siirtää tietoja QuickBooks-ohjelmasta, koska [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää laajennuksen, joka käsittelee QuickBooks-tietojen muunnoksen. Jos haluat siirtää tietoja muista rahoitusratkaisuista, tarkista, onko kyseiselle ratkaisulle saatavana laajennus, tai tuo tiedot Excelistä.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää malleja tileille, asiakkaille, toimittajille ja varastonimikkeille, joita voit kohdistaa tietojen tuomisen yhteydessä.  

## <a name="importing-data-from-quickbooks-or-dynamics-gp"></a>Tietojen tuominen QuickBooksista tai Dynamics GP:stä
Jos yrityksessä käytetään tällä hetkellä QuickBooksia tai Dynamics GP:tä, voit viedä tarvittavat tiedot tiedostoon. Tämän jälkeen voit avata avustetun asennusoppaan ja siirtää tiedot.
Jos tiedosto sisältää esimerkiksi asiakkaita ja toimittajia, voit siirtää vain asiakkaiden tiedot. Loput tiedot voit siirtää myöhemmin.  

Avustetun asennuksen avulla voit muuttaa siirron oletusmäärityksiä. Näitä lisäasetuksia kannattaa muuttaa vain, jos tietokantataulukot ovat sinulle ennestään tuttuja. QuickBooksista tai Dynamics GP:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin tehtävän siirron oletusmääritykset siirtävät suurimmassa osassa yrityksiä juuri halutut tiedot.  

## <a name="importing-data-from-configuration-packages"></a>Tietojen tuominen määrityspaketeista
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää määrityspaketin, jonka voit viedä Exceliin tietojen määrittämiseksi siellä. Tämän jälkeen voit tuoda tiedot uudelleen Excelistä. Paketissa on 27 taulukkoa, mukaan lukien päätiedot, kuten asiakkaat, toimittajat, nimikkeet ja tilit, muita perusasetustaulukkoja, kuten toimitustavat, ja tapahtumataulukot, kuten myyntiotsikko ja rivit.  

> [!NOTE]  
>  Määrityspakettien käyttäminen on lisätoiminto ja onkin suositeltavaa keskustella sen käytöstä järjestelmänvalvojan kanssa. Lisätietoja on kohdassa [Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennuksilla](ui-extensions.md)   
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
