---
title: "Projektin budjetin määrittäminen ja hallinta| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten resursseja suunnitellaan ja ennakoidaan sekä miten projektin kustannukset määritetään kullekin projektille."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e88eaebf65d950dcbb6c0296be24e68628a9494e
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="manage-job-budgets"></a>Projektibudjettien hallinta
Jokaiselle projektille voi määrittää budjetin. Budjettia käytetään projektille kohdistettavien resurssien suunnittelussa. Budjetti voi olla joko yleisluonteinen budjetti, joka sisältää vain vähän tapahtumia, tai se voi sisältää monia tapahtumia, jotka on jaettu toimintotasoille. Voit verrata budjetoituja summia projektipäiväkirjaan kirjattuun todelliseen käyttöön. Kun valvot todellisen ja budjetoidun käytön välisiä eroja, voit hallita suoritettavaa projektia ja parantaa tulevien projektien laatua pienentämällä kustannusten aliarvioinnin riskiä.

Seuraavissa ohjeissa kerrotaan, miten budjetoituja kustannuksia arvioidaan suunnittelun aikana. Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Projektin budjetoitujen kustannusten arvioiminen
Kun asiakas haluaa tietää sellaisen projektin hinnan, joka laskutetaan käytön perusteella, on määritettävä projektin budjetoidut kustannukset. Tähän käytetään **Projektitehtävärivit**-ikkunaa.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa liittyvä projekti.
3. Valitse tehtävärivin tyypiksi Kirjaus ja valitse sitten **Projektin suunnittelurivit** -toiminto.
4. Täytä tarvittaessa uuden rivin kentät. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Viittaa **Rivityyppi**-kentässä seuraaviin tietoihin.  

| Rivityyppi | Kuvaus |
| --- | --- |
| **Sekä budjetti että laskutettava** |Suunnitteluriville annetut kustannus- ja hintasummat ovat tämän suunnittelurivin budjetoidut kustannukset sekä laskutettava hinta. Hinnaston summa laskutetaan. |
| **Budjetti** |Asiakasta ei veloiteta käytöstä. Sitä ei voida koskaan siirtää laskuun, mutta käytetään edelleen KET-laskennassa. |
| **Laskutettava** |Asiakasta veloitetaan käytöstä. Laskutettava määrä on määritetty kunkin ostorivin Laskuun siirrettävä määrä -kentässä. |

> [!NOTE]  
>   Suunnittelurivin **Suunnittelupäivämäärä**-kenttä sisältää päivämäärän, jona suunnitteluriviin liittyvän käytön odotetaan olevan valmis. Se on myös päivämäärä, jona suunnittelurivi voidaan siirtää myyntilaskuun ja kirjata.  

> [!NOTE]  
>   Kun täytät **Määrä**-kentän, ohjelma laskee kaikki kokonaishinnan ja -kustannusten tiedot kyseistä suunnitteluriviä varten. Voit muokata niitä milloin tahansa.

**Projektikortti**-ikkunassa on nyt yhteenveto kunkin tehtävän budjetoiduista kokonaiskustannuksista, budjetoidusta hinnasta, laskutettavista kustannuksista ja laskutettavasta hinnasta.

Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

