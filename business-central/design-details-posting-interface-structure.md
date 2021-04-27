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
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b852d6e5d7f96cfba64de219ca414de60cea3a31
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777598"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="3729d-103">Rakenteen tiedot: Kirjausliittymän rakenne</span><span class="sxs-lookup"><span data-stu-id="3729d-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="3729d-104">[!INCLUDE[prod_short](includes/prod_short.md)] -kirjausliittymän rakenteessa on useita globaaleja proseduureja, jotka käyttävät samaa rakennetta:</span><span class="sxs-lookup"><span data-stu-id="3729d-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="3729d-105">RunWithCheck- ja RunWithoutCheck-kutsuproseduurin Code – yleinen kirjausliittymä</span><span class="sxs-lookup"><span data-stu-id="3729d-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="3729d-106">päiväkirjan riville.</span><span class="sxs-lookup"><span data-stu-id="3729d-106">Jnl Line.</span></span>  
* <span data-ttu-id="3729d-107">CustPostApplyCustLedgEntry – asiakkaan kirjaussovellus, kutsuja on codeunit 226 CustEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="3729d-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="3729d-108">VendPostApplyVendLedgEntry – toimittajasovelluksen kirjaus, kutsuja on codeunit 227 VendEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="3729d-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="3729d-109">UnapplyCustLedgEntry – peruuta asiakassovelluksen kirjaus, kutsuja on codeunit 226 CustEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="3729d-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="3729d-110">UnapplyVendLedgEntry – peruuta toimittajasovelluksen kirjaus, kutsuja on codeunit 227 VendEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="3729d-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3729d-111">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3729d-111">See Also</span></span>  
[<span data-ttu-id="3729d-112">Rakenteen tiedot: Kirjausohjelman rakenne</span><span class="sxs-lookup"><span data-stu-id="3729d-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]