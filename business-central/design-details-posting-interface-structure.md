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
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="620c4-103">Rakenteen tiedot: Kirjausliittymän rakenne</span><span class="sxs-lookup"><span data-stu-id="620c4-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="620c4-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] -kirjausliittymän rakenteessa on useita globaaleja proseduureja, jotka käyttävät samaa rakennetta:</span><span class="sxs-lookup"><span data-stu-id="620c4-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="620c4-105">RunWithCheck- ja RunWithoutCheck-kutsuproseduurin Code – yleinen vakiopäiväkirjarivin kirjausliittymä.</span><span class="sxs-lookup"><span data-stu-id="620c4-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="620c4-106">CustPostApplyCustLedgEntry – asiakkaan kirjaussovellus, kutsuja on koodiyksikkö 226 CustEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="620c4-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="620c4-107">VendPostApplyVendLedgEntry – toimittajasovelluksen kirjaus, kutsuja on koodiyksikkö 227 VendEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="620c4-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="620c4-108">UnapplyCustLedgEntry – peruuta asiakassovelluksen kirjaus, kutsuja on koodiyksikkö 226 CustEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="620c4-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="620c4-109">UnapplyVendLedgEntry – peruuta toimittajasovelluksen kirjaus, kutsuja on koodiyksikkö 227 VendEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="620c4-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="620c4-110">Katso myös</span><span class="sxs-lookup"><span data-stu-id="620c4-110">See Also</span></span>  
[<span data-ttu-id="620c4-111">Rakenteen tiedot: Kirjausohjelman rakenne</span><span class="sxs-lookup"><span data-stu-id="620c4-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)