---
title: Siirron tulokset | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään mitä tapahtuu, kun pääkirjanpidon tapahtumat siirretään kustannustapahtumiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 590c1501f9da2c7c343b5c2f3617df873fcd3b7a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242489"
---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Tulokset siirrettäessä pääkirjanpidon tapahtumat kustannustapahtumiin
Kun pääkirjanpidon tapahtumia siirretään kustannustapahtumiin, [!INCLUDE[d365fin](includes/d365fin_md.md)] luo yhteyksiä tapahtumiin **KP-tapahtuma**-, **Kustannustapahtuma**- ja **Kustannusrekisteri**-taulukossa. Tämä mahdollistaa pääkirjanpidon tapahtumien ja kustannustapahtumien välisten yhteyksien jäljittämisen.  

## <a name="general-ledger-entries"></a>Pääkirjanpidon tapahtumat  
[!INCLUDE[d365fin](includes/d365fin_md.md)] täyttää kaikkien kustannuslaskentaan siirrettävien pääkirjanpidon tapahtumien kustannusten **Tapahtumanro**-kentän.  

## <a name="cost-entries"></a>Kustannustapahtumat  
[!INCLUDE[d365fin](includes/d365fin_md.md)] tallentaa vastaavan pääkirjanpidon tapahtuman jokaisen kustannustapahtuman numeron **Kustannustapahtuma**-ikkunan **KP-tapahtuman nro** -kenttään.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] tallentaa yhdistettyjen kustannustapahtumien pääkirjanpidon viimeisen tapahtuman tapahtumanumeron (tapahtuma, jonka numero on kaikkein suurin).  

**Kustannustapahtuma**-taulukon **KP-tili**-kentässä on KP-tilin numero, jolta kustannustapahtuma on peräisin.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] siirtää yksittäisten kustannustapahtumien kirjaustekstin pääkirjanpidon tapahtumasta **Kuvaus**-tekstikenttään. Tekstikenttä osoittaa, että yhdistetyt tapahtumat siirretään yhdistettyinä tapahtumina. Esimerkiksi vuoden 2013 lokakuun yhdistetyn tapahtuman teksti voi olla **Yhdistetyt tapahtumat, lokakuu 2013**.  

## <a name="cost-register"></a>Kustannusrekisteri  
**Kustannusrekisteri**-taulukkoon [!INCLUDE[d365fin](includes/d365fin_md.md)] luo merkinnän lähteen siirtämisestä pääkirjanpidosta. Tapahtuma kirjaa siirrettyjen pääkirjanpidon tapahtumien ensimmäisen ja viimeisen tapahtumanumeron sekä luotujen kustannustapahtumien ensimmäisen ja viimeisen tapahtumanumeron.  

## <a name="see-also"></a>Katso myös  
[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md)   
