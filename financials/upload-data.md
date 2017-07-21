---
title: Vanhojen liiketoimintatietojen tuominen Financialsiin | Microsoft Docs
description: "Voit siirtää asiakkaiden, toimittajien ja varaston tietoja esimerkiksi Excelistä, QuickBooksista tai Dynamics GP:stä Financialsiin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migrate, initialize, implement
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: dd6eb5a6b19bf4c8fd92674a48e8cd29ce912eee
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="importing-business-data-from-other-finance-systems"></a>Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä
Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, voit luoda tyhjän yrityksen, ladata siihen omat tietosi ja testata uuden [!INCLUDE[d365fin](includes/d365fin_md.md)]-yrityksesi. Yrityksen tällä hetkellä käytössä olevan rahoitusratkaisun mukaan voit siirtää tietoja asiakkaista, toimittajista, varastosta ja pankkitileistä.  

Kotisivulla olevan avustetun asennusoppaan avulla voit siirtää liiketoimintatiedot Excel-tiedostosta tai muista muodoista. Ladattavissa olevien tiedostojen tyyppi riippuu käytettävissä olevista laajennuksista. Voit esimerkiksi siirtää tietoja QuickBooks-ohjelmasta, koska [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää laajennuksen, joka käsittelee QuickBooks-tietojen muunnoksen. Jos haluat siirtää tietoja muista rahoitusratkaisuista, tarkista, onko kyseiselle ratkaisulle saatavana laajennus, tai tuo tiedot Excelistä.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää malleja tileille, asiakkaille, toimittajille ja varastonimikkeille, joita voit kohdistaa tietojen tuomisen yhteydessä.  

## <a name="importing-data-from-quickbooks-or-dynamics-gp"></a>Tietojen tuominen QuickBooksista tai Dynamics GP:stä
Jos yrityksessä käytetään tällä hetkellä QuickBooksia tai Dynamics GP:tä, voit viedä tarvittavat tiedot tiedostoon. Tämän jälkeen voit avata avustetun asennusoppaan ja siirtää tiedot.
Jos tiedosto sisältää esimerkiksi asiakkaita ja toimittajia, voit siirtää vain asiakkaiden tiedot. Loput tiedot voit siirtää myöhemmin.  

Avustetun asennuksen avulla voit muuttaa siirron oletusmäärityksiä. Näitä lisäasetuksia kannattaa muuttaa vain, jos tietokantataulukot ovat sinulle ennestään tuttuja. QuickBooksista tai Dynamics GP:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin tehtävän siirron oletusmääritykset siirtävät suurimmassa osassa yrityksiä juuri halutut tiedot.  

Lisätietoja on kohdassa [QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md) tai [Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md).

## <a name="importing-data-from-configuration-packages"></a>Tietojen tuominen määrityspaketeista
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää määrityspaketin, jonka voit viedä Exceliin tietojen määrittämiseksi siellä. Tämän jälkeen voit tuoda tiedot uudelleen Excelistä. Paketissa on 27 taulukkoa, mukaan lukien päätiedot, kuten asiakkaat, toimittajat, nimikkeet ja tilit, muita perusasetustaulukkoja, kuten toimitustavat, ja tapahtumataulukot, kuten myyntiotsikko ja rivit.  

> [!NOTE]  
>   Määrityspakettien käyttäminen on lisätoiminto ja onkin suositeltavaa keskustella sen käytöstä järjestelmänvalvojan kanssa. Lisätietoja on kohdassa [Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md)  
[QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)   
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

