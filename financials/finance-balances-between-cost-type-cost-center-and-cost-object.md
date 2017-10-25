---
title: Kustannustyypin, kustannuspaikan ja kustannusobjektin saldot | Microsoft Docs
description: "Kun määrität kustannuslaskennan, sinun on varmistettava, että kaikki tapahtumat on liitetty sekä kustannustyyppiin että kustannuspaikkaan ja kustannuskohteeseen. Tämä tarkoittaa, että jokaisella kustannustapahtumalla täytyy olla määritettynä sekä kustannustyyppi ja joko kustannuspaikkakoodi tai kustannuskohde. Tämä sääntö varmistaa, että kukin kustannustapahtuma näkyy joko kustannuspaikassa tai kustannuskohteessa, mutta ei koskaan molemmissa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3c33d5f5cdc4ac131d7c85221d16f60b2f9c6c00
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Kustannustyypin, kustannuspaikan ja kustannusobjektin saldot
Kun määrität kustannuslaskennan, sinun on varmistettava, että kaikki tapahtumat on liitetty sekä kustannustyyppiin että kustannuspaikkaan ja kustannuskohteeseen. Tämä tarkoittaa, että jokaisella kustannustapahtumalla täytyy olla määritettynä sekä kustannustyyppi ja joko kustannuspaikkakoodi tai kustannuskohde. Tämä sääntö varmistaa, että kukin kustannustapahtuma näkyy joko kustannuspaikassa tai kustannuskohteessa, mutta ei koskaan molemmissa.  

 Näin luot seuraavan kirjanpitolaskutoimituksen:  

 Kustannustyypin saldo = Kustannuspaikan saldo + Kustannuskohteen saldo  

 Kun tulostat Kustannustyyppikaavion, kustannuspaikkakaavion ja kustannuskohteiden raporttikaavion, voit analysoida tämän suhteen.  

## <a name="see-also"></a>Katso myös  
[Kustannuslaskenta](finance-manage-cost-accounting.md)  
 [Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)   
 [Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)   
 [Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)  
 [Kustannusbudjettien luominen](finance-create-cost-budgets.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

