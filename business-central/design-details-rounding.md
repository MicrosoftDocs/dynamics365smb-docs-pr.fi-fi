---
title: "Rakennetiedot – Pyöristys | Microsoft Docs"
description: "Pyöristyksestä voi jäädä jäännöksiä, kun arvioit varaston vähennyksen kustannuksia, jotka on mitattu eri määristä, kuin vastaava varaston kasvu. Pyöristyksen jäännökset lasketaan kaikille kustannuslaskentamenetelmille, kun suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 231481ed9b8de81fb565e86e9b89c96434545cbf
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-rounding"></a>Rakennetiedot: pyöristys
Pyöristyksestä voi jäädä jäännöksiä, kun arvioit varaston vähennyksen kustannuksia, jotka on mitattu eri määristä kuin vastaava varaston kasvu. Pyöristyksen jäännökset lasketaan kaikille kustannuslaskentamenetelmille, kun suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon.  

 Kun käytössä on keskimääräinen arvostusmenetelmä, pyöristysjäännös lasketaan ja tallennetaan kumulatiivisesti ja syöttö syötöltä.  

 Kun käytät jotain muuta kuin keskimääräistä arvostusmenetelmää, pyöristysjäännös lasketaan, kun varaston arvon nousu on kohdistettu kokonaan eli varaston arvon nousun jäljellä oleva määrä on nolla. Pyöristyksen jäljelle jäävälle osalle luodaan tämän jälkeen erillinen tapahtuma ja tämän pyöristystapahtuman kirjauspäivämäärä on viimeisen laskutetun varaston lisäyksen arvotapahtuma.  

## <a name="example"></a>Esimerkki  
 Seuraava esimerkki kuvaa sitä, kuinka eri pyöristysjäämiä käsitellään keskimääräisen kustannuslaskelman menetelmässä sekä ei-keskimääräisen kustannuslaskelman menetelmässä tässä järjestyksessä. Kummassakin tapauksessa **Muuta kustannuksia - Nimiketapahtumat** -erätyö on suoritettu.  

 Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset, joihin esimerkki perustuu.  

|Kirjauspvm|määrä.|Tapahtumanro|  
|------------------|--------------|---------------|  
|01-01-20|3|1|  
|02-01-20|-1|2|  
|03-01-20|-1|3|  
|04-01-20|-1|4|  

 Niiden nimikkeiden osalta, jotka käyttävät keskimääräinen-arvostusmenetelmää, pyöristysjäännös (1/300) lasketaan ensimmäisellä vähennyksellä (tapahtumanumero 2) ja se siirretään eteenpäin tapahtumaan numero 3. Tämän vuoksi numero 3 on arvostettu arvossa –3,34.  

 Seuraavassa taulukossa on tuloksena saatavat arvotapahtumat.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3.33|2|2|  
|03-01-20|-1|-3.34|3|3|  
|04-01-20|-1|-3.33|4|4|  

 Niiden nimikkeiden osalta, jotka käyttävät muuta arvostusmenetelmää kuin keskiarvo, pyöristysjäännös (0,01) lasketaan, kun varastoarvon nousun jäljellä oleva määrä on nolla. Pyöristysylijäämällä on erillinen kirjaus (numero 5).  

 Seuraavassa taulukossa on tuloksena saatavat arvotapahtumat.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3.33|2|2|  
|03-01-20|-1|-3.33|3|3|  
|04-01-20|-1|-3.33|4|4|  
|01-01-20|0|-0.01|1|5|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: Kustannuksen muutos](design-details-cost-adjustment.md)   
 [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md) [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

