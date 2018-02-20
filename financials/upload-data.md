---
title: Vanhojen liiketoimintatietojen tuominen Finance and Operations, Business editioniin | Microsoft Docs
description: "Voit siirtää asiakkaiden, toimittajien ja varaston tietoja esimerkiksi Excelistä, QuickBooksista tai Dynamics GP:stä Finance and Operations, Business editioniin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QuickBooks, transfer, import, migrate, initialize, implement
ms.date: 09/25/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f1339468507efc474c709f35fa04d61ca7e5b9a2
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a>Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä
Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, voit luoda tyhjän yrityksen, ladata siihen omat tietosi ja testata uuden [!INCLUDE[d365fin](includes/d365fin_md.md)]-yrityksesi. Yrityksen tällä hetkellä käytössä olevan rahoitusratkaisun mukaan voit siirtää tietoja asiakkaista, toimittajista, varastosta ja pankkitileistä.  

Kotisivulla olevan avustetun asennusoppaan avulla voit siirtää liiketoimintatiedot Excel-tiedostosta tai muista muodoista. Ladattavissa olevien tiedostojen tyyppi riippuu käytettävissä olevista laajennuksista. Voit esimerkiksi siirtää tietoja QuickBooks-ohjelmasta, koska [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää laajennuksen, joka käsittelee QuickBooks-tietojen muunnoksen. Jos haluat siirtää tietoja muista rahoitusratkaisuista, tarkista, onko kyseiselle ratkaisulle saatavana laajennus, tai tuo tiedot Excelistä.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]  sisältää malleja tileille, asiakkaille, toimittajille ja varastonimikkeille, joita voit kohdistaa tietojen tuomisen yhteydessä.  

## <a name="importing-data-from-quickbooks-desktop-quickbooks-online-or-dynamics-gp"></a>Tietojen tuominen QuickBooks Desktopista, QuickBooks Onlinesta tai Dynamics GP:stä
Jos yrityksessä käytetään tällä hetkellä QuickBooksia tai Dynamics GP:tä, voit viedä tarvittavat tiedot tiedostoon. Tämän jälkeen voit avata avustetun asennusoppaan ja siirtää tiedot.
Jos tiedosto sisältää esimerkiksi asiakkaita ja toimittajia, voit siirtää vain asiakkaiden tiedot. Loput tiedot voit siirtää myöhemmin.  

Avustetun asennuksen avulla voit muuttaa siirron oletusmäärityksiä. Näitä lisäasetuksia kannattaa muuttaa vain, jos tietokantataulukot ovat sinulle ennestään tuttuja. QuickBooksista tai Dynamics GP:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin tehtävän siirron oletusmääritykset siirtävät suurimmassa osassa yrityksiä juuri halutut tiedot.  

Lisätietoja on kohdassa [QuickBooks Desktopin tietojen siirto](ui-extensions-quickbooks-data-migration.md), [QuickBooks Onlinen tietojen siirto](ui-extensions-quickbooks-online-data-migration.md), tai [Dynamics GP:n tietojen siirto](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="importing-data-from-configuration-packages"></a>Tietojen tuominen määrityspaketeista
[!INCLUDE[d365fin](includes/d365fin_md.md)]  sisältää määrityspaketin, jonka voit viedä Exceliin tietojen määrittämiseksi siellä. Tämän jälkeen voit tuoda tiedot uudelleen Excelistä. Paketissa on 27 taulukkoa, mukaan lukien päätiedot, kuten asiakkaat, toimittajat, nimikkeet ja tilit, muita perusasetustaulukkoja, kuten toimitustavat, ja tapahtumataulukot, kuten myyntiotsikko ja rivit.  

> [!NOTE]  
>   Määrityspakettien käyttäminen on lisätoiminto ja onkin suositeltavaa keskustella sen käytöstä järjestelmänvalvojan kanssa. Lisätietoja on kohdassa [Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md)  
[QuickBooks Desktopin tietojen siirto](ui-extensions-quickbooks-data-migration.md)  
[QuickBooks Online -tietojen siirto](ui-extensions-quickbooks-online-data-migration.md)  
[Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)   
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

