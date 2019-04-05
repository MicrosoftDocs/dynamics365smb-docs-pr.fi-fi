---
title: Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin | Microsoft Docs
description: On tärkeää ymmärtää ehdot, joiden mukaan pääkirjanpidon tapahtumat siirretään kustannustapahtumiin. Siirron aikana **Siirrä KP-tapahtumat kustannuslaskentaan** -eräajo käyttää seuraavia kriteerejä määrittääkseen, jos ja miten pääkirjanpidon tapahtumat siirretään.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6e5fcfedbb899633f61c05b0b8b5ec8125112d65
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795335"
---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin
On tärkeää ymmärtää ehdot, joiden mukaan pääkirjanpidon tapahtumat siirretään kustannustapahtumiin. Siirron aikana **Siirrä KP-tapahtumat kustannuslaskentaan** -eräajo käyttää seuraavia kriteerejä määrittääkseen, jos ja miten pääkirjanpidon tapahtumat siirretään.  

Kirjanpitotapahtumat siirretään, jos:  

-   Tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa tai kustannuskohdetta.  
-   Tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta. Kustannuspaikka ratkaisee asian näiden tapahtumien kohdalla. Näin vältetään tilanne, jossa kustannustyyppi näkyy sekä kustannuskohteessa että kustannuspaikassa ja näin ollen ne lasketaan tilastoihin kahdesti.  
-   Asiakirjan numeroa ei ole tapahtumissa, joten kustannustapahtumissa näytetään asiakirjanumeron kohdalla 0000.  
-   Tapahtumat siirretään kustannustyypille, jolla yhdistettyjä tapahtumia voidaan käsitellä, ja tapahtumat siirretään yhdistettynä joko kuukausittain tai päivittäin.  

Kirjanpitotapahtumia ei siirretä, jos:  

-   Tapahtumilla on dimensioarvot, jotka eivät vastaa kustannuspaikkaa tai kustannuskohdetta.  
-   Tapahtumien summa on nolla.  
-   Tapahtumissa on poistettu KP-tili.  
-   Tapahtumissa on KP-tili, joka ei ole **Tuloslaskelma**-tyyppiä  
-   Tapahtumissa on KP-tili, jolle ei ole määritetty kustannustyyppiä.  
-   Tapahtumien kirjauspäivämäärä on ennen **KP-siirron alkamispäivämäärää**.  
-   Tapahtumille on kirjattu sulkemispäivämäärä. Tässä on tyypillisiä tapahtumia, jotka palauttavat tuloslaskelman saldon vuoden lopussa.  

## <a name="see-also"></a>Katso myös  
[Kustannuslaskenta](finance-manage-cost-accounting.md)  
 [Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md)   
 [Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
