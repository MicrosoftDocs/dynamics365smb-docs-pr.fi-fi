---
title: Rakennetiedot – Kustannuskomponentit | Microsoft Docs
description: Kustannuskomponentit ovat erityyppisiä kustannuksia, jotka muodostavat varaston arvon kasvun tai vähennyksen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: fa49d48d4af1efe40cda6579ff15f703ef5ad426
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8523047"
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
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]