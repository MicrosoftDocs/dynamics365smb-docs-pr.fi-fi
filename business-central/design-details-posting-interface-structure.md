---
title: Rakenteen tiedot – kirjausliittymän rakenne
description: Tässä aiheessa on yleiskatsaus kirjausliittymän rakenteen yleisistä toimintaohjeista ja rakennetiedoista.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'posting, interface, design'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-posting-interface-structure" />Rakenteen tiedot: Kirjausliittymän rakenne
[!INCLUDE[prod_short](includes/prod_short.md)] -kirjausliittymän rakenteessa on useita globaaleja proseduureja, jotka käyttävät samaa rakennetta:  
  
* RunWithCheck- ja RunWithoutCheck-kutsuproseduurin Code – yleinen kirjausliittymä päiväkirjan riville.  
* CustPostApplyCustLedgEntry – asiakkaan kirjaussovellus, kutsuja on codeunit 226 CustEntry-käytä kirjattuja tapahtumia.  
* VendPostApplyVendLedgEntry – toimittajasovelluksen kirjaus, kutsuja on codeunit 227 VendEntry-käytä kirjattuja tapahtumia.  
* UnapplyCustLedgEntry – peruuta asiakassovelluksen kirjaus, kutsuja on codeunit 226 CustEntry-käytä kirjattuja tapahtumia.  
* UnapplyVendLedgEntry – peruuta toimittajasovelluksen kirjaus, kutsuja on codeunit 227 VendEntry-käytä kirjattuja tapahtumia.  
  
## <a name="see-also" />Katso myös
[Rakenteen tiedot: Kirjausohjelman rakenne](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
