---
title: Rakenteen tiedot – Kirjausliittymän rakenne | Microsoft Docs
description: Tässä aiheessa on yleiskatsaus kirjausliittymän rakenteen yleisistä toimintaohjeista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 529a0e42d814f0754e62fcc4b93b793d44b8daa7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215826"
---
# <a name="design-details-posting-interface-structure"></a>Rakenteen tiedot: Kirjausliittymän rakenne
[!INCLUDE[prod_short](includes/prod_short.md)] -kirjausliittymän rakenteessa on useita globaaleja proseduureja, jotka käyttävät samaa rakennetta:  
  
* RunWithCheck- ja RunWithoutCheck-kutsuproseduurin Code – yleinen kirjausliittymä päiväkirjan riville.  
* CustPostApplyCustLedgEntry – asiakkaan kirjaussovellus, kutsuja on codeunit 226 CustEntry-käytä kirjattuja tapahtumia.  
* VendPostApplyVendLedgEntry – toimittajasovelluksen kirjaus, kutsuja on codeunit 227 VendEntry-käytä kirjattuja tapahtumia.  
* UnapplyCustLedgEntry – peruuta asiakassovelluksen kirjaus, kutsuja on codeunit 226 CustEntry-käytä kirjattuja tapahtumia.  
* UnapplyVendLedgEntry – peruuta toimittajasovelluksen kirjaus, kutsuja on codeunit 227 VendEntry-käytä kirjattuja tapahtumia.  
  
## <a name="see-also"></a>Katso myös  
[Rakenteen tiedot: Kirjausohjelman rakenne](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]