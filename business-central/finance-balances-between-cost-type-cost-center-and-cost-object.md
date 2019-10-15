---
title: Kustannustyypin, kustannuspaikan ja kustannusobjektin saldot | Microsoft Docs
description: Kun määrität kustannuslaskennan, sinun on varmistettava, että kaikki tapahtumat on liitetty sekä kustannustyyppiin että kustannuspaikkaan ja kustannuskohteeseen. Tämä tarkoittaa, että jokaisella kustannustapahtumalla täytyy olla määritettynä sekä kustannustyyppi ja joko kustannuspaikkakoodi tai kustannuskohde. Tämä sääntö varmistaa, että kukin kustannustapahtuma näkyy joko kustannuspaikassa tai kustannuskohteessa, mutta ei koskaan molemmissa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 7ae54e8a1a011b8e4f1914ef9f15c179794d2675
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302522"
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
