---
title: Projektin budjetin määrittäminen ja hallinta| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten resursseja suunnitellaan ja ennakoidaan sekä miten projektin kustannukset määritetään kullekin projektille.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ceb57fb6425b988920957c3066aa19659d08ae89
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443455"
---
# <a name="manage-job-budgets"></a>Projektibudjettien hallinta
Jokaiselle projektille voi määrittää budjetin. Budjettia käytetään projektille kohdistettavien resurssien suunnittelussa. Budjetti voi olla joko yleisluonteinen budjetti, joka sisältää vain vähän tapahtumia, tai se voi sisältää monia tapahtumia, jotka on jaettu toimintotasoille. Voit verrata budjetoituja summia projektipäiväkirjaan kirjattuun todelliseen käyttöön. Kun valvot todellisen ja budjetoidun käytön välisiä eroja, voit hallita suoritettavaa projektia ja parantaa tulevien projektien laatua pienentämällä kustannusten aliarvioinnin riskiä.

Seuraavissa ohjeissa kerrotaan, miten budjetoituja kustannuksia arvioidaan suunnittelun aikana. Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="JobBudgetCosts"></a> Projektin budjetoitujen kustannusten arvioiminen
Kun asiakas haluaa tietää sellaisen projektin hinnan, joka laskutetaan käytön perusteella, on määritettävä projektin budjetoidut kustannukset. Tähän käytetään **Projektitehtävärivit**-sivua.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Avaa liittyvä projekti.
3. Valitse tehtävärivin tyypiksi Kirjaus ja valitse sitten **Projektin suunnittelurivit** -toiminto.
4. Täytä tarvittaessa uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Viittaa **Rivityyppi**-kentässä seuraaviin tietoihin.  

| Rivityyppi | Kuvaus |
| --- | --- |
| **Sekä budjetti että laskutettava** |Suunnitteluriville annetut kustannus- ja hintasummat ovat tämän suunnittelurivin budjetoidut kustannukset sekä laskutettava hinta. Hinnaston summa laskutetaan. |
| **Budjetti** |Asiakasta ei veloiteta käytöstä. Sitä ei voida koskaan siirtää laskuun, mutta käytetään edelleen KET-laskennassa. |
| **Laskutettava** |Asiakasta veloitetaan käytöstä. Laskutettava määrä on määritetty kunkin ostorivin Laskuun siirrettävä määrä -kentässä. |

> [!NOTE]  
> Suunnittelurivin **Suunniteltu toimituspvm** -kenttä sisältää päivämäärän, jona suunnitteluriviin liittyvän käytön odotetaan olevan valmis. Se on myös päivämäärä, jona suunnittelurivi voidaan siirtää myyntilaskuun ja kirjata. <br /><br /> **Projektikortti**-sivun taustalla olevan projektitehtävän **Aloituspäivämäärä**- ja **Päättymispäivämäärä**-kentät sisältävät **Suunniteltu toimituspvm** -kentän arvon ensimmäisillä ja viimeisellä projektin suunnittelurivillä liittyvällä **Projektin suunnittelurivit** -sivulla.

> [!NOTE]  
>   Kun täytät **Määrä**-kentän, ohjelma laskee kaikki kokonaishinnan ja -kustannusten tiedot kyseistä suunnitteluriviä varten. Voit muokata niitä milloin tahansa.

**Projektikortti**-sivulla on nyt yhteenveto kunkin tehtävän budjetoiduista kokonaiskustannuksista, budjetoidusta hinnasta, laskutettavista kustannuksista ja laskutettavasta hinnasta.

Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]