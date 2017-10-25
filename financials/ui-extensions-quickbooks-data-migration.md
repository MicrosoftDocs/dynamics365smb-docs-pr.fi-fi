---
title: "QuickBooksin siirtolaajennuksen käyttäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten laajennuksella tuodaan asiakkaita, toimittajia, nimikkeitä ja tilejä QuickBooks Desktopista Dynamics 365 for Financialsiin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a>Dynamics 365 for Financialsin QuickBooks-tietojen siirron laajennus
Tämän laajennuksen avulla asiakkaat, toimittajat, nimikkeet ja tilit on helppo siirtää QuickBooks Desktopista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Jos yrityksessä on käytössä QuickBooks, voit viedä tarpeelliset tiedot ja ladata ne sitten [!INCLUDE[d365fin](includes/d365fin_md.md)]iin avaamalla avustetun asennusoppaan.  
Lisätietoja on kohdassa [Tietojen tuominen muista rahoitusjärjestelmistä](upload-data.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Tietojen vieminen QuickBooks Desktopista
Osa tai kaikki asiakkaat, toimittajat, varastonimikkeet ja tilit on oltava vietynä IIF (Intuit Interchange Format) -tiedostoon. QuickBooks-tietojen siirron laajennus sisältää QuickBooks-tietojen oletusmäärityksen. Voit siis käyttää olemassa olevia tietoja, kun testaat uutta [!INCLUDE[d365fin](includes/d365fin_md.md)]-yritystä. Oletusmääritys on riittävä lähes kaikissa tapauksissa. Voit kuitenkin muuttaa määritystä avustetun asennusoppaan avulla.  
QuickBooks-ohjelman Tiedosto-valikko sisältää apuohjelman luetteloiden viemistä varten. Voit viedä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin seuraavat luettelot:

* Asiakasluettelo  
* Toimittajaluettelo  
* Nimikeluettelo  
* Tililuettelo  

Viedyt tiedot tallennetaan IIF-tiedostona, jonka voi sitten ladata [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

## <a name="finding-the-quickbooks-data-migration-extension"></a>QuickBooks-tietojen siirtolaajennuksen etsiminen
QuickBooks-tietojen siirtolaajennus on asennettu ja valmis käytettäväksi tietojen siirtoasetusten ohjatun määrityksen osana. Jos olet valmis aloittamaan käytön nyt ja olet vienyt tiedot QuickBooksista, valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asetusten ohjattu määritys** ja valitse sitten liittyvä linkki. Valitse **Siirrä liiketoimintatiedot** ja noudata oppaan ohjeita.  

## <a name="see-also"></a>Katso myös
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](upload-data.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  

