---
title: "Rakenteen tiedot – Kirjausliittymän rakenne | Microsoft Docs"
description: "Tässä aiheessa on yleiskatsaus kirjausliittymän rakenteen yleisistä toimintaohjeista."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 97b1bc02f848d583240a1701e41be4b639422a6c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="a71b8-103">Rakenteen tiedot: Kirjausliittymän rakenne</span><span class="sxs-lookup"><span data-stu-id="a71b8-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="a71b8-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] -kirjausliittymän rakenteessa on useita globaaleja proseduureja, jotka käyttävät samaa rakennetta:</span><span class="sxs-lookup"><span data-stu-id="a71b8-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="a71b8-105">RunWithCheck- ja RunWithoutCheck-kutsuproseduurin Code – yleinen vakiopäiväkirjarivin kirjausliittymä.</span><span class="sxs-lookup"><span data-stu-id="a71b8-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="a71b8-106">CustPostApplyCustLedgEntry – asiakkaan kirjaussovellus, kutsuja on koodiyksikkö 226 CustEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a71b8-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="a71b8-107">VendPostApplyVendLedgEntry – toimittajasovelluksen kirjaus, kutsuja on koodiyksikkö 227 VendEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a71b8-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="a71b8-108">UnapplyCustLedgEntry – peruuta asiakassovelluksen kirjaus, kutsuja on koodiyksikkö 226 CustEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a71b8-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="a71b8-109">UnapplyVendLedgEntry – peruuta toimittajasovelluksen kirjaus, kutsuja on koodiyksikkö 227 VendEntry-käytä kirjattuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a71b8-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a71b8-110">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a71b8-110">See Also</span></span>  
[<span data-ttu-id="a71b8-111">Rakenteen tiedot: Kirjausohjelman rakenne</span><span class="sxs-lookup"><span data-stu-id="a71b8-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)
