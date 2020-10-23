---
title: Tilin tietojen oikeellisuuden varmistamiseen käytettävien sulkemista edeltävien raporttien yleiskatsaus | Microsoft Docs
description: Ohjeaiheessa on yleiskatsaus raporteista, joilla voidaan varmistaa tilien tietojen oikeellisuus ennen kirjojen sulkemista vuoden tai kauden lopussa.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: b270a7b1f9ffda71d68fa981885aacbe31f55eab
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923118"
---
# <a name="using-pre-closing-reports"></a><span data-ttu-id="80a1a-103">Sulkemista edeltävien raporttien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="80a1a-103">Using Pre-Closing Reports</span></span>
<span data-ttu-id="80a1a-104">Ennen kirjojen sulkemista vuoden tai kauden lopussa voit varmistaa tilien tietojen oikeellisuuden käyttämällä useita eri vakioraportteja.</span><span class="sxs-lookup"><span data-stu-id="80a1a-104">There are many standard reports that you can use to verify the accuracy of the accounts before closing the books at the end of a year or period.</span></span> <span data-ttu-id="80a1a-105">Voit esimerkiksi tarkistaa **Asiakas - Alust. saldo** -raportin avulla, että asiakkaan kirjausryhmän saldo vastaa vastaavan kirjanpitotilin saldoa tiettynä päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="80a1a-105">For example, you can use the **Customer - Trial Balance** report to verify that the balance for a customer posting group is equal to the balance on the corresponding general ledger account on a certain date.</span></span>

<span data-ttu-id="80a1a-106">Seuraavassa taulukossa on luettelo raporteista, joista voi olla hyötyä tässä prosessissa.</span><span class="sxs-lookup"><span data-stu-id="80a1a-106">The following table describes a number of reports that may be useful in this process.</span></span>

| <span data-ttu-id="80a1a-107">Toiminta</span><span class="sxs-lookup"><span data-stu-id="80a1a-107">To</span></span> | <span data-ttu-id="80a1a-108">Tarkastele tätä raporttia</span><span class="sxs-lookup"><span data-stu-id="80a1a-108">See this report</span></span> |
| --- | --- |
| <span data-ttu-id="80a1a-109">Pankkitilien eritellyn alustavan saldoraportin tulostaminen siten, että raportissa on lisätietoja yksittäisistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="80a1a-109">Print a detailed trial balance report for one or more bank accounts with additional information about individual entries.</span></span> |<span data-ttu-id="80a1a-110">Pankkitili - Er. alust. saldo</span><span class="sxs-lookup"><span data-stu-id="80a1a-110">Bank Acc. - Detail Trial Bal.</span></span> |
| <span data-ttu-id="80a1a-111">Valittujen asiakkaiden eritellyn alustavan saldoraportin tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="80a1a-111">Print a detail trial balance for selected customers.</span></span> |<span data-ttu-id="80a1a-112">Asiakas - Alustava saldo</span><span class="sxs-lookup"><span data-stu-id="80a1a-112">Customer - Trial Balance</span></span> |
| <span data-ttu-id="80a1a-113">Valittujen asiakkaiden eritellyn alustavan saldoraportin tulostaminen valitulta ajalta siten, että raportissa on yksityiskohtaisia tietoja yksittäisistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="80a1a-113">Print a detail trial balance with detailed information about individual entries, for selected customers during a selected period.</span></span> |<span data-ttu-id="80a1a-114">Asiakas - Erit. alustava saldo</span><span class="sxs-lookup"><span data-stu-id="80a1a-114">Customer - Detail Trial Bal.</span></span> |
| <span data-ttu-id="80a1a-115">Valittujen toimittajien eritellyn alustavan saldoraportin tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="80a1a-115">Print a detail trial balance for selected vendors.</span></span> |<span data-ttu-id="80a1a-116">Toimittaja - Alustava saldo</span><span class="sxs-lookup"><span data-stu-id="80a1a-116">Vendor - Trial Balance</span></span> |
| <span data-ttu-id="80a1a-117">Valittujen toimittajien eritellyn alustavan saldoraportin tulostaminen valitulta ajalta siten, että raportissa on yksityiskohtaisia tietoja yksittäisistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="80a1a-117">Print a detail trial balance with detailed information about individual entries, for selected vendors during a selected period.</span></span> |<span data-ttu-id="80a1a-118">Toimittaja - Er. alust. saldo</span><span class="sxs-lookup"><span data-stu-id="80a1a-118">Vendor - Detail Trial Balance</span></span> |
| <span data-ttu-id="80a1a-119">Alustavan saldon tulostaminen kuluvan vuoden ja edellisen vuoden luvuilla.</span><span class="sxs-lookup"><span data-stu-id="80a1a-119">Print a trial balance with the current year's and the previous year's figures.</span></span> |<span data-ttu-id="80a1a-120">Alustava TP-tulos ja -tase</span><span class="sxs-lookup"><span data-stu-id="80a1a-120">Closing Trial Balance</span></span> |
| <span data-ttu-id="80a1a-121">Eritellyn alustavan saldoraportin tulostaminen kirjanpitotilien saldoista.</span><span class="sxs-lookup"><span data-stu-id="80a1a-121">Print a detailed trial balance report for general ledger account balances.</span></span> |<span data-ttu-id="80a1a-122">Eritelty alustava saldo</span><span class="sxs-lookup"><span data-stu-id="80a1a-122">Detail Trial Balance</span></span> |
| <span data-ttu-id="80a1a-123">Kirjanpitotilien saldot ja nettomuutokset sisältävän alustavan saldoraportin tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="80a1a-123">Print a trial balance report with balances and net changes for general ledger accounts.</span></span> |<span data-ttu-id="80a1a-124">Alustava tulos/tase</span><span class="sxs-lookup"><span data-stu-id="80a1a-124">Trial Balance</span></span> |
| <span data-ttu-id="80a1a-125">Konsolidoidun yrityksen alustavan saldon tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="80a1a-125">Print a trial balance for a consolidated company.</span></span> |<span data-ttu-id="80a1a-126">Konsolidoitu alust. tulos/tase</span><span class="sxs-lookup"><span data-stu-id="80a1a-126">Consolidated Trial Balance</span></span> |

<span data-ttu-id="80a1a-127">Jos haluat nähdä kaikki raportin, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeen, kirjoita taulukossa oleva nimi ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="80a1a-127">To see a report, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, type the name as it appears in the table, and then choose the related link.</span></span>

## <a name="see-also"></a><span data-ttu-id="80a1a-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="80a1a-128">See Also</span></span>
[<span data-ttu-id="80a1a-129">Vuosien ja jaksojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="80a1a-129">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="80a1a-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80a1a-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

