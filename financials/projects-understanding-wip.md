---
title: "Tietoja KET-menetelmistä| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan KET-menetelmistä, joilla kirjataan ja seurataan keskeneräisen projektien rahoitustietoja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d6f82b3eb086b53be8a091e7a805c745a74ac10f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="understanding-wip-methods"></a>Tietoja KET-menetelmistä
[!INCLUDE[d365fin](includes/d365fin_md.md)] tukee seuraavia keskeneräisen työn arvon laskennan ja kirjaamisen menetelmiä.

| KET-menetelmä | Laskentakaava | Laskennan kuvaus |
| --- | --- | --- |
| Kustannusarvo |Tuloutettu tuotto = laskutettava laskutettu hinta<br /><br /> Arvioidut kokonaiskustannukset = laskutettava kokonaishinta * budjetin kustannusten suhde<br /><br /> KET-kustannukset = \(valmistumisen %-osuus - laskutettu %\) x arvioidut kokonaiskustannukset<br /><br /> Valmistumisen %-osuus = käytön kokonaiskustannukset / budjetoidut kokonaiskustannukset<br /> Laskutettu % = laskutettava laskutettu hinta<br /><br /> Laskutettu tuloutettujen kokonaiskustannusten hinta = käytön kokonaiskustannukset - KET |Kustannusarvon laskelmat aloitetaan laskemalla tuotettujen arvo. Se tehdään ottamalla osa valmistumisen prosenttiosuuteen perustuvista arvioiduista kustannuksista. Laskutetut kustannukset vähennetään ottamalla osa laskutettuun prosenttiin perustuvista arvioiduista kokonaiskustannuksista.<br /><br /> Tämä laskenta vaatii, että koko projektin laskutettava kokonaishinta, budjetoitu kokonaishinta ja budjetoidut kokonaiskustannukset on syötettävä oikein. |
| Myynnin kulut |Tuloutettu tuotto = laskutettava laskutettu hinta<br /><br /> Tuloutetut kustannukset = budjetoidut kokonaiskustannukset x laskutettu prosenttiosuus<br /><br /> Laskutettu % = laskutettava laskutettu hinta / laskutettava kokonaishinta<br /><br /> \(Laskutettu % on projektitehtävärivin sarake\)<br /><br /> KET-kustannukset = käytön kokonaiskustannukset - tuloutetut kustannukset |Myynnin kulujen laskeminen alkaa tuloutettujen kustannusten laskemisella. Kustannukset tuloutetaan suhteessa budjetin kokonaiskustannuksiin.<br /><br /> Tämä laskenta vaatii, että koko projektin laskutettava kokonaishinta ja budjetin kokonaiskustannukset on syötettävä oikein. |
| Myyntiarvo |Tuloutetut kustannukset = käytön kokonaiskustannukset<br /><br /> Tuloutettu tuotto = käytön kokonaishinta * odotettu laskutuksen suhde<br /><br /> Kustannusten korvaus-% = laskutettava kokonaishinta / budjetin kokonaishinta<br /><br /> KET-myynti = tuloutettu myynti - laskutettava laskutettu hinta |Myyntiarvon laskelmat tulouttavat tuoton suhteessa käytön kokonaiskustannuksiin ja odotettuihin kustannuksiin korvaussuhteen perusteella.<br /><br /> Tämä laskenta vaatii, että koko projektin laskutettava kokonaishinta ja budjetin kokonaishinta on syötettävä oikein. |
| Valmistumisen prosenttiosuus |Tuloutetut kustannukset = käytön kokonaiskustannukset<br /><br /> Tuloutettu tuotto = laskutettava kokonaishinta x valmistumisen %-osuus<br /><br /> Valmistumisen %-osuus = käytön kokonaiskustannukset / budjetoidut kokonaiskustannukset<br /> \(Projektitehtäväriveillä tätä kutsutaan kustannuksen valmistumisprosentiksi\)<br /><br /> KET-myynti = tuloutettu myynti - laskutettava laskutettu hinta |Valmistumisen %-osuuden laskennat tulouttavat tuoton suhteessa valmistumisen prosenttiosuuteen (eli käytön kokonaiskustannuksiin ja budjetin kustannuksiin).<br /><br /> Tämä laskenta vaatii, että koko projektin laskutettava kokonaishinta ja budjetin kokonaiskustannukset on syötettävä oikein. |
| Valmis sopimus |KET-summa = KET-kustannusten summa = käyttö \(kokonaiskustannukset\)<br /><br /> KET-myynnin summa = laskutettava \(laskutettu hinta\) |Valmis sopimus ei tulouta tuottoa ja kustannuksia ennen projektin valmistumista. Tästä voi olla hyötyä, kun projektin kustannusten ja tuoton arviointi on hyvin epävarmaa.<br /><br /> Kaikki käyttö kirjataan KET-kustannusten tilille \(saatavat\) ja kaikki laskutettu myynti kirjataan laskutetun KET-myynnin tilille\(velat\), kunnes projekti on valmis. |

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

