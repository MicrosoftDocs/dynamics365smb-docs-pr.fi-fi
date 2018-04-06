---
title: "Rakennetiedot – Kustannuskomponentit | Microsoft Docs"
description: "Kustannuskomponentit ovat erityyppisiä kustannuksia, jotka muodostavat varaston arvon kasvun tai vähennyksen."
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
ms.openlocfilehash: e1410e2511b2f1dd27e80ea23d6e08b2b5063158
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-cost-components"></a>Rakennetiedot: kustannuskomponentit
Kustannuskomponentit ovat erityyppisiä kustannuksia, jotka muodostavat varaston arvon nousun tai laskun.  

 Seuraavassa taulukossa kuvataan eri kustannusosat ja mitkä tahansa toissijaiset kustannusosat, joista ne koostuvat.  

|Kustannuskomponentti|Alisteinen kustannuskomponentti|Description|  
|--------------------|--------------------------------|---------------------------------------|  
|Välitön kustannus|Yksikkökustannus (välitön ostohinta)|Kustannus, joka voidaan jäljittää kustannuskohteeseen.|  
|Välitön kustannus|Rahtikulu (nimikekulu)|Kustannus, joka voidaan jäljittää kustannuskohteeseen.|  
|Välitön kustannus|Vakuutuskustannus (nimikekulu)|Kustannus, joka voidaan jäljittää kustannuskohteeseen.|  
|Epäsuora kustannus||Kustannus, jota ei voida jäljittää kustannuskohteeseen.|  
|Vaihtelu|Ostovaihtelu|Todellisten ja vakiokustannusten välinen ero, joka kirjataan vain niiden nimikkeiden osalta, joille käytetään **Vakio**-arvostusmenetelmää.|  
|Vaihtelu|Materiaalin vaihtelu|Todellisten ja vakiokustannusten välinen ero, joka kirjataan vain niiden nimikkeiden osalta, joille käytetään **Vakio**-arvostusmenetelmää.|  
|Vaihtelu|Kapasit. vaihtelu|Todellisten ja vakiokustannusten välinen ero, joka kirjataan vain niiden nimikkeiden osalta, joille käytetään **Vakio**-arvostusmenetelmää.|  
|Vaihtelu|Alihankkijavaihtelu|Todellisten ja vakiokustannusten välinen ero, joka kirjataan vain niiden nimikkeiden osalta, joille käytetään **Vakio**-arvostusmenetelmää.|  
|Vaihtelu|Kapasit. yleiskust. vaihtelu|Todellisten ja vakiokustannusten välinen ero, joka kirjataan vain niiden nimikkeiden osalta, joille käytetään **Vakio**-arvostusmenetelmää.|  
|Vaihtelu|Tuotannon yleiskustannusten vaihtelu|Todellisten ja vakiokustannusten välinen ero, joka kirjataan vain niiden nimikkeiden osalta, joille käytetään **Vakio**-arvostusmenetelmää.|  
|Uudelleenarvostus||Nykyisen varaston arvon arvonalennus tai arvonkorotus.|  
|Pyöristys||Ylijäämät, jotka on aiheutettu menetelmällä, jossa varaston arvostuksen vähennykset on laskettu.|  

> [!NOTE]  
>  Rahti-ja vakuutuskustannukset ovat nimikekustannuksia, jotka voidaan lisätä milloin tahansa nimikkeen kustannukseen. Kun **Muuta kustannuksia - Nimiketapahtumat** -eräajo suoritetaan, minkä tahansa liittyvän varaston arvon laskut päivitetään sen mukaan.  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: Vaihtelu](design-details-variance.md) [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

