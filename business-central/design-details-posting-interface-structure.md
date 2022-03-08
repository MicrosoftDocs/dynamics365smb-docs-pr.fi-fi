---
title: Rakenteen tiedot – Kirjausliittymän rakenne | Microsoft Docs
description: Tässä aiheessa on yleiskatsaus kirjausliittymän rakenteen yleisistä toimintaohjeista.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f484c6474c840b4c2d802494407f8d819256596c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306938"
---
# <a name="design-details-posting-interface-structure"></a>Rakenteen tiedot: Kirjausliittymän rakenne
[!INCLUDE[d365fin](includes/d365fin_md.md)] -kirjausliittymän rakenteessa on useita globaaleja proseduureja, jotka käyttävät samaa rakennetta:  
  
* RunWithCheck- ja RunWithoutCheck-kutsuproseduurin Code – yleinen kirjausliittymä päiväkirjan riville.  
* CustPostApplyCustLedgEntry – asiakkaan kirjaussovellus, kutsuja on koodiyksikkö 226 CustEntry-käytä kirjattuja tapahtumia.  
* VendPostApplyVendLedgEntry – toimittajasovelluksen kirjaus, kutsuja on koodiyksikkö 227 VendEntry-käytä kirjattuja tapahtumia.  
* UnapplyCustLedgEntry – peruuta asiakassovelluksen kirjaus, kutsuja on koodiyksikkö 226 CustEntry-käytä kirjattuja tapahtumia.  
* UnapplyVendLedgEntry – peruuta toimittajasovelluksen kirjaus, kutsuja on koodiyksikkö 227 VendEntry-käytä kirjattuja tapahtumia.  
  
## <a name="see-also"></a>Katso myös  
[Rakenteen tiedot: Kirjausohjelman rakenne](design-details-posting-engine-structure.md)