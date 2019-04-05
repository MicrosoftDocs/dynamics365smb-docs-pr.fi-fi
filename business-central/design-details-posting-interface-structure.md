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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 236cbcc45ccca23905dcb79a491236c80b2bdebf
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795618"
---
# <a name="design-details-posting-interface-structure"></a>Rakenteen tiedot: Kirjausliittymän rakenne
[!INCLUDE[d365fin](includes/d365fin_md.md)] -kirjausliittymän rakenteessa on useita globaaleja proseduureja, jotka käyttävät samaa rakennetta:  
  
* RunWithCheck- ja RunWithoutCheck-kutsuproseduurin Code – yleinen vakiopäiväkirjarivin kirjausliittymä.  
* CustPostApplyCustLedgEntry – asiakkaan kirjaussovellus, kutsuja on koodiyksikkö 226 CustEntry-käytä kirjattuja tapahtumia.  
* VendPostApplyVendLedgEntry – toimittajasovelluksen kirjaus, kutsuja on koodiyksikkö 227 VendEntry-käytä kirjattuja tapahtumia.  
* UnapplyCustLedgEntry – peruuta asiakassovelluksen kirjaus, kutsuja on koodiyksikkö 226 CustEntry-käytä kirjattuja tapahtumia.  
* UnapplyVendLedgEntry – peruuta toimittajasovelluksen kirjaus, kutsuja on koodiyksikkö 227 VendEntry-käytä kirjattuja tapahtumia.  
  
## <a name="see-also"></a>Katso myös  
[Rakenteen tiedot: Kirjausohjelman rakenne](design-details-posting-engine-structure.md)