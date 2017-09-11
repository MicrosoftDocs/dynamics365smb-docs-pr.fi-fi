---
title: "Päiväkirjakirjauksen peruuttaminen kirjaamalla palautustapahtuma| Microsoft Docs"
description: "Jos olet tehnyt virheellisen kirjauksen yleiseen päiväkirjaan, Peruuta tapahtuma -toiminnolla kumottu kirjaus luo oikean kirjausketjun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="ecbe7-103">Päiväkirjakirjauksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="ecbe7-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="ecbe7-104">Voit kumota virheellisen kirjauksen päiväkirjaan valitsemalla tapahtuman luomalla peruutustapahtuman (alkuperäistä tapahtumaa vastaava tapahtuma, jossa summakentässä on vastakkainen etumerkki), jossa on sama asiakirjanumero ja kirjauspäivämäärä kuin alkuperäisessä tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="ecbe7-105">Kun olet peruuttanut tapahtuman, lisää tapahtuma korjattuna.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="ecbe7-106">Vain yleisen päiväkirjan riviltä kirjatut tapahtumat voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="ecbe7-107">Tapahtuman voi peruuttaa vain kerran.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="ecbe7-108">Lisätietoja yleisestä päiväkirjasta tehtävistä kirjauksista on ohjeaiheessa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="ecbe7-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="ecbe7-109">Tapahtumia voi peruuttaa kaikista **Tapahtumakirjaukset**-ikkunoista.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="ecbe7-110">Seuraava menettely perustuu **Pääkirjanpidon tapahtumat** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="ecbe7-111">Pääkirjanpidon tapahtuman päiväkirjakirjauksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="ecbe7-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="ecbe7-112">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Pääkirjanpidon tapahtumat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="ecbe7-113">Valitse ensin peruutettava tapahtuma ja sitten **Peruuta tapahtuma** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="ecbe7-114">Huomaa, että sen on oltava peräisin päiväkirjan kirjauksesta.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="ecbe7-115">Valitse **Peruuta tapahtumat** -ikkunassa käsiteltävä tapahtuma ja valitse sitten **Peruuta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="ecbe7-116">Valitse vahvistusviestissä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ecbe7-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="ecbe7-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ecbe7-117">See Also</span></span>
[<span data-ttu-id="ecbe7-118">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="ecbe7-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="ecbe7-119">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="ecbe7-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="ecbe7-120">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="ecbe7-120">Finance</span></span>](finance.md)  
<span data-ttu-id="ecbe7-121">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ecbe7-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

