---
title: "Tilin tietojen oikeellisuuden varmistamiseen käytettävien sulkemista edeltävien raporttien yleiskatsaus | Microsoft Docs"
description: Ohjeaiheessa on yleiskatsaus raporteista, joilla voidaan varmistaa tilien tietojen oikeellisuus ennen kirjojen sulkemista vuoden tai kauden lopussa.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ead7f45583b8edbdc00b6d41ae335d4b8adb14cf
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017


---
# <a name="using-pre-closing-reports"></a><span data-ttu-id="3ff5a-103">Sulkemista edeltävien raporttien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="3ff5a-103">Using Pre-Closing Reports</span></span>
<span data-ttu-id="3ff5a-104">Ennen kirjojen sulkemista vuoden tai kauden lopussa voit varmistaa tilien tietojen oikeellisuuden käyttämällä useita eri vakioraportteja.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-104">There are many standard reports that you can use to verify the accuracy of the accounts before closing the books at the end of a year or period.</span></span> <span data-ttu-id="3ff5a-105">Voit esimerkiksi tarkistaa **Asiakas - Alust. saldo** -raportin avulla, että asiakkaan kirjausryhmän saldo vastaa vastaavan kirjanpitotilin saldoa tiettynä päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-105">For example, you can use the **Customer - Trial Balance** report to verify that the balance for a customer posting group is equal to the balance on the corresponding general ledger account on a certain date.</span></span>

<span data-ttu-id="3ff5a-106">Seuraavassa taulukossa on luettelo raporteista, joista voi olla hyötyä tässä prosessissa.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-106">The following table describes a number of reports that may be useful in this process.</span></span>

| <span data-ttu-id="3ff5a-107">Toiminta</span><span class="sxs-lookup"><span data-stu-id="3ff5a-107">To</span></span> | <span data-ttu-id="3ff5a-108">Tarkastele tätä raporttia</span><span class="sxs-lookup"><span data-stu-id="3ff5a-108">See this report</span></span> |
| --- | --- |
| <span data-ttu-id="3ff5a-109">Pankkitilien eritellyn alustavan saldoraportin tulostaminen siten, että raportissa on lisätietoja yksittäisistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-109">Print a detailed trial balance report for one or more bank accounts with additional information about individual entries.</span></span> |<span data-ttu-id="3ff5a-110">Pankkitili</span><span class="sxs-lookup"><span data-stu-id="3ff5a-110">Bank Acc.</span></span> <span data-ttu-id="3ff5a-111">- Er. alust. saldo</span><span class="sxs-lookup"><span data-stu-id="3ff5a-111">- Detail Trial Bal.</span></span> |
| <span data-ttu-id="3ff5a-112">Valittujen asiakkaiden eritellyn alustavan saldoraportin tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-112">Print a detail trial balance for selected customers.</span></span> |<span data-ttu-id="3ff5a-113">Asiakas - Alustava saldo</span><span class="sxs-lookup"><span data-stu-id="3ff5a-113">Customer - Trial Balance</span></span> |
| <span data-ttu-id="3ff5a-114">Valittujen asiakkaiden eritellyn alustavan saldoraportin tulostaminen valitulta ajalta siten, että raportissa on yksityiskohtaisia tietoja yksittäisistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-114">Print a detail trial balance with detailed information about individual entries, for selected customers during a selected period.</span></span> |<span data-ttu-id="3ff5a-115">Asiakas - Erit. alustava saldo</span><span class="sxs-lookup"><span data-stu-id="3ff5a-115">Customer - Detail Trial Bal.</span></span> |
| <span data-ttu-id="3ff5a-116">Valittujen toimittajien eritellyn alustavan saldoraportin tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-116">Print a detail trial balance for selected vendors.</span></span> |<span data-ttu-id="3ff5a-117">Toimittaja - Alustava saldo</span><span class="sxs-lookup"><span data-stu-id="3ff5a-117">Vendor - Trial Balance</span></span> |
| <span data-ttu-id="3ff5a-118">Valittujen toimittajien eritellyn alustavan saldoraportin tulostaminen valitulta ajalta siten, että raportissa on yksityiskohtaisia tietoja yksittäisistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-118">Print a detail trial balance with detailed information about individual entries, for selected vendors during a selected period.</span></span> |<span data-ttu-id="3ff5a-119">Toimittaja - Er. alust. saldo</span><span class="sxs-lookup"><span data-stu-id="3ff5a-119">Vendor - Detail Trial Balance</span></span> |
| <span data-ttu-id="3ff5a-120">Alustavan saldon tulostaminen kuluvan vuoden ja edellisen vuoden luvuilla.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-120">Print a trial balance with the current year's and the previous year's figures.</span></span> |<span data-ttu-id="3ff5a-121">Alustava TP-tulos ja -tase</span><span class="sxs-lookup"><span data-stu-id="3ff5a-121">Closing Trial Balance</span></span> |
| <span data-ttu-id="3ff5a-122">Eritellyn alustavan saldoraportin tulostaminen kirjanpitotilien saldoista.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-122">Print a detailed trial balance report for general ledger account balances.</span></span> |<span data-ttu-id="3ff5a-123">Eritelty alustava saldo</span><span class="sxs-lookup"><span data-stu-id="3ff5a-123">Detail Trial Balance</span></span> |
| <span data-ttu-id="3ff5a-124">Kirjanpitotilien saldot ja nettomuutokset sisältävän alustavan saldoraportin tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-124">Print a trial balance report with balances and net changes for general ledger accounts.</span></span> |<span data-ttu-id="3ff5a-125">Alustava tulos/tase</span><span class="sxs-lookup"><span data-stu-id="3ff5a-125">Trial Balance</span></span> |
| <span data-ttu-id="3ff5a-126">Konsolidoidun yrityksen alustavan saldon tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-126">Print a trial balance for a consolidated company.</span></span> |<span data-ttu-id="3ff5a-127">Konsolidoitu alust. tulos/tase</span><span class="sxs-lookup"><span data-stu-id="3ff5a-127">Consolidated Trial Balance</span></span> |

<span data-ttu-id="3ff5a-128">Voit avata raportin valitsemalla ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, kirjoita nimi sellaisena kuin se näkyy taulukossa ja valitse aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3ff5a-128">To see a report, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, type the name as it appears in the table, and then choose the related link.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ff5a-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3ff5a-129">See Also</span></span>
[<span data-ttu-id="3ff5a-130">Vuosien ja jaksojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="3ff5a-130">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="3ff5a-131">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3ff5a-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


