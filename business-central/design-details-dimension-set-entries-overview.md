---
title: Dimensioyhdistelmän tapahtumien yleiskatsaus | Microsoft Docs
description: Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan Dynamics 365:ssä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8ed544486af6949932814bf97d99293f1ef17ee2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303578"
---
# <a name="dimension-set-entries-overview"></a>Dimensioyhdistelmätapahtumien yleiskuva
Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="dimension-sets"></a>Dimensioyhdistelmät  
Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä. Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan. Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa. Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.  

Seuraavassa esimerkissä näytetään dimensioyhdistelmä, jolla on kolme dimensioyhdistelmätapahtumaa. Dimensioyhdistelmä tunnistetaan dimensioyhdistelmän tunnuksella, joka on 108.  

|Dimensioyhdistelmän tunnus|Dimensiokoodi|Dimension arvokoodi|Dimensioarvon nimi|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|ALUE|70|Pohjois-Amerikka|  
|108|YRITYSRYHMÄ|HOME|Kotitalous|  
|108|OSASTO|MYYNTI|Myynti|  

## <a name="dimension-set-entries"></a>Dimensioyhdistelmän tapahtumat  
Dimensioyhdistelmät tallennetaan **Dimensioyhdistelmän tapahtuma** -taulukkoon dimensioyhdistelmätapahtumina, joilla on sama dimensioyhdistelmän tunnus.  

![Dimensiojoukon tapahtumavirta](media/dimensionentrynav7.png "Dimensiojoukon tapahtumavirta")  

Kun luot uuden päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän. Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.  

Kun muokkaat **Muokkaa dimensioyhdistelmän tapahtumia** -sivua ja suljet sen, tarkastus on suoritettu nähdäksesi onko dimensioarvojen yhdistelmä olemassa dimensionyhdistelmänä taulukossa. Jos yhdistelmä tehdään taulukossa, vastaavan dimensioyhdistelmän tunnus liitetään päiväkirjariviin, asiakirjan otsikkoon tai asiakirjariville. Muussa tapauksessa taulukkoon lisätään uusi dimensioyhdistelmä ja uuden dimensioyhdistelmä tunnus määritetään päiväkirjariville, asiakirjaotsikkoon tai asiakirjariville.

## <a name="codeunit-408-dimension-management"></a>Codeunit 408 -dimension hallinta
Codeunit 408, dimension hallinta, on toimintokirjasto, joka käsittelee yleiset dimensioihin liittyvät tehtävät, kuten kopioinnin taulukosta toiseen tai yhdestä asiakirjasta toiseen.

## <a name="performance-improvement"></a>Suorituskyvyn parantaminen  
Määrittämällä dimensioyhdistelmän kerran tietokannassa tietokannan tilaa säästyy ja yleinen suorituskyky on entistä parempi.  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md)   
[Rakennetiedot: taulukkorakenne](design-details-table-structure.md)   
[Rakennetiedot: Dimensioyhdistelmä-tapahtumat](design-details-dimension-set-entries.md)   
