---
title: "Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen | Microsoft Docs"
description: "Lisätietoja kustannustyypin ja kirjanpitotilin välisen suhteen määrittämisestä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen
Kustannustyypin ja KP-tilin välinen suhde luodaan kustannustyypissä ja KP-tilillä.  

* **Kustannustyyppi**-taulukon **KP-tilien väli** -kenttä osoittaa, mitkä KP-tilit kuuluvat millekin kustannustyypille.  
* **Saldokustannustyypin numero** -kenttä tilikartassa osoittaa, mitkä KP-tilit kuuluvat millekin kustannustyypille.  

Nämä kaksi kenttää täytetään automaattisesti, kun käytät **Hae kustannustyypit tilikartasta** -toimintoa.  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Pääkirjanpitotilien ja kustannustyyppien välinen suhde.  
Pääkirjanpitotilien ja kustannustyyppien välissä on olemassa n:1-suhde. Useita pääkirjanpitotilejä voi kuulua yhdelle kustannustyypille, mutta jokainen pääkirjanpitotili kuuluu vain yhdelle kustannustyypille. Seuraava taulukko kuvaa suhteen yksityiskohtia.  

|Suhde|**KP-tilien väli**|**Kustannustyypin numero**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Yksi pääkirjanpidon tilin kullekin kustannustyypille|kirjanpitotili.|Yksi kustannuslaji|  
|Useita kirjanpitotilejä yhdelle kustannustyypille|Kirjanpitotiliväli, kuten 7110–7193 jokaisen kirjanpitotilin kohdalla|Alueen kaikille pääkirjanpidon tileillä on vain yksi kustannustyyppi|  
|Kustannustyypit ilman vastaavia pääkirjanpitotilejä|<Empty>||  
|Kirjanpitotilit, joiden tapahtumia ei siirretä||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kustannustyypit ilman suhdetta pääkirjanpitoon  
Kustannuksen tyypillä ei ehkä ole yhteyttä pääkirjanpidon tileille, jos jokin seuraavista ehdoista toteutuu:  

* Operatiivisen kirjanpidon tilit, kuten kortin laskenta ja poistot, ottavat kustannukset vain operatiivisesta kirjanpidosta.  
* Auttavia kustannustyyppejä, kuten [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa olevia tyyppejä 9901, 9902 ja 9903, käytetään kredit- ja debet-tileinä kohdistuksissa.  
* Auttava tili, 9920 [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa, sisältää todellisia kertymiä, jotka näyttävät kustannusten ja KP-kulujen eron.  

## <a name="see-also"></a>Katso myös  
[Kustannuslaskenta](finance-manage-cost-accounting.md)  
[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)   
[Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

