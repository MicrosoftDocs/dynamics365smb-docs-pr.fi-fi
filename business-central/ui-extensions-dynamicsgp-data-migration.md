---
title: "Tietojen siirtäminen Dynamics GP:stä tietojen siirron laajennuksella | Microsoft Docs"
description: "Voit siirtää asiakkaita, toimittajia, varastonimikkeitä ja tilejä Dynamics GP:stä Business Central -sovellukseen Dynamics GP:n tietojen siirron laajennuksella."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 3761bdb0d6b9a51ed309ac4189ff263de76f4679
ms.contentlocale: fi-fi
ms.lasthandoff: 05/17/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a>Dynamics GP -tietojen siirron laajennus Business Central -sovellusta varten 
Tämän laajennuksen avulla asiakkaat, toimittajat, varastonimikkeet ja tilit on helppo siirtää Dynamics GP:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Jos yrityksessä on käytössä Dynamics GP, voit viedä soveltuvat päätietueet ja lisätä tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]iin avaamalla avustetun asennusoppaan. Lisätietoja on kohdassa [Tietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Tietojen vieminen Dynamics GP:stä
Sinun on vietävä tiedostoon osa tai kaikki aiemmin luodut asiakkaat, toimittajat, varastonimikkeet ja tilit Dynamics GP:n tietojen vientitoiminnolla. Voit viedä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin seuraavan tyyppisiä tietoja:

* Tili  
* Asiakas  
* Vaihtoehto  
* Toimittaja  

Dynamics GP:n tietojen siirtolaajennus yhdistää viedyt tiedot automaattisesti, joten tiedot ovat nopeasti käytettävissä uudessa [!INCLUDE[d365fin](includes/d365fin_md.md)]-yritykseen. Prosessin aikana luodaan tukevia määritystietoja, kuten kirjausryhmiä. Varastonimikkeet tuodaan järjestelmään käyttämällä FIFO-menetelmää kustannusten arvostukseen. Tilit määritetään Dynamics GP:n dimensioita sisältävänä päätilisegmenttinä, koska [!INCLUDE[d365fin](includes/d365fin_long_md.md)]issa ei ole tilisegmenttejä.

## <a name="see-also"></a>Katso myös
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  

