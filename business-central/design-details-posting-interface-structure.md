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
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="e570e-103">Rakenteen tiedot: Kirjausliittymän rakenne</span><span class="sxs-lookup"><span data-stu-id="e570e-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="e570e-104">[!INCLUDE[prod_short](includes/prod_short.md)] -kirjausliittymän rakenteessa on useita globaaleja proseduureja, jotka käyttävät samaa rakennetta:</span><span class="sxs-lookup"><span data-stu-id="e570e-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="e570e-105">RunWithCheck- ja RunWithoutCheck-kutsuproseduurin Code – yleinen kirjausliittymä</span><span class="sxs-lookup"><span data-stu-id="e570e-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="e570e-106">päiväkirjan riville.</span><span class="sxs-lookup"><span data-stu-id="e570e-106">Jnl Line.</span></span>  
* <span data-ttu-id="e570e-107">CustPostApplyCustLedgEntry – asiakkaan kirjaussovellus, kutsuja on codeunit 226 CustEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e570e-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="e570e-108">VendPostApplyVendLedgEntry – toimittajasovelluksen kirjaus, kutsuja on codeunit 227 VendEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e570e-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="e570e-109">UnapplyCustLedgEntry – peruuta asiakassovelluksen kirjaus, kutsuja on codeunit 226 CustEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e570e-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="e570e-110">UnapplyVendLedgEntry – peruuta toimittajasovelluksen kirjaus, kutsuja on codeunit 227 VendEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e570e-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e570e-111">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e570e-111">See Also</span></span>  
[<span data-ttu-id="e570e-112">Rakenteen tiedot: Kirjausohjelman rakenne</span><span class="sxs-lookup"><span data-stu-id="e570e-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]