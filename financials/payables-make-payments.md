---
title: "Toimittajille suoritettavien maksujen hallintatehtävien yleiskatsaus| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan toimittajille tai luotonantajille suoritettavien maksujen hallintatehtävistä, kuten maksurivien kirjaamisesta ja erääntyvän saldon yleiskatsauksen hakemisesta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="28ed3-103">Maksujen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="28ed3-103">Make Payments</span></span>
<span data-ttu-id="28ed3-104">Kun suoritat maksut toimittajille, kirjaat liittyvät maksurivit **Maksupäiväkirja**-ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="28ed3-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="28ed3-105">**Ehdota toimittajamaksuja** -eräajon avulla voit etsiä erääntyvät maksut.</span><span class="sxs-lookup"><span data-stu-id="28ed3-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="28ed3-106">Voit myös hakea erääntyvien maksujen yhteenvedon käyttämällä **Toimittaja - Eräänt.yht.veto** -raporttia.</span><span class="sxs-lookup"><span data-stu-id="28ed3-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="28ed3-107">Maksupäiväkirjassa voit tulostaa tietokonesekkejä tai kirjata käsin kirjoitettuja sekkejä.</span><span class="sxs-lookup"><span data-stu-id="28ed3-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="28ed3-108">Jos valitset **Tietokonesekki**-vaihtoehdon **Pankkimaksun tyyppi** -kenttään, sekkejä edustavat rivit on tulostettava, ennen kuin maksupäiväkirja voidaan kirjata.</span><span class="sxs-lookup"><span data-stu-id="28ed3-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="28ed3-109">Kun maksut kirjataan, voit viedä ne pankkitiedostoon, jolloin ne voidaan ladata verkkopankkiisi käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="28ed3-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="28ed3-110">Kun maksut on tehty pankkiin, kohdista ne liittyviin avoimiin toimittajatapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="28ed3-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="28ed3-111">Voit tehdä sen manuaalisesti tai tuomalla pankin tiliotetiedoston ja kohdistamalla maksut automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="28ed3-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="28ed3-112">Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="28ed3-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="28ed3-113">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="28ed3-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="28ed3-114">Toiminta</span><span class="sxs-lookup"><span data-stu-id="28ed3-114">To</span></span> | <span data-ttu-id="28ed3-115">Katso</span><span class="sxs-lookup"><span data-stu-id="28ed3-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="28ed3-116">Käytä toimintoa ehdottaaksesi toimittajan maksuja valittujen ehtojen, kuten eräpäivän, alennuskelpoisuuden ja maksuvalmiutesi, mukaan.</span><span class="sxs-lookup"><span data-stu-id="28ed3-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="28ed3-117">Toimintaohje: Toimittajamaksujen ehdottaminen</span><span class="sxs-lookup"><span data-stu-id="28ed3-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="28ed3-118">Myönnä sekkejä maksuille joko tulosteina tai tietokonesekkeinä.</span><span class="sxs-lookup"><span data-stu-id="28ed3-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="28ed3-119">Mitätöi sekit ennen kirjaamista tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="28ed3-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="28ed3-120">Toimintaohje: Sekkien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="28ed3-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="28ed3-121">Varmista lähettämällä toimittaja-, sekki- ja maksutiedot sisältävä tiedosto, että pankki vahvistaa vain tarkistetut sekit ja summat.</span><span class="sxs-lookup"><span data-stu-id="28ed3-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="28ed3-122">Toimintaohje: Positive Pay -tiedoston vieminen</span><span class="sxs-lookup"><span data-stu-id="28ed3-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="28ed3-123">Vie maksut **Maksupäiväkirja**-ikkunasta pankkitiedostoon, joka ladataan pankkiin käsiteltäväksi. Tämä tiedosto voi olla Pohjois-Amerikassa myös sähköinen rahansiirtotiedosto (EFT).</span><span class="sxs-lookup"><span data-stu-id="28ed3-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="28ed3-124">Toimintaohje: Maksujen vieminen pankkitiedostoon</span><span class="sxs-lookup"><span data-stu-id="28ed3-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="28ed3-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="28ed3-125">See Also</span></span>
[<span data-ttu-id="28ed3-126">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="28ed3-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="28ed3-127">Osto</span><span class="sxs-lookup"><span data-stu-id="28ed3-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="28ed3-128">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="28ed3-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="28ed3-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="28ed3-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

