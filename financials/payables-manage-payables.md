---
title: "Ostovelkojen hallintatehtävien yleiskatsaus| Microsoft Docs"
description: "Tässä ohjeaiheessa käsitellään ostovelkojen hallintaan liittyviä tehtäviä, kuten maksamista velkojille tai laskujen tai hyvityslaskujen sulkemista kohdistamalla lähtevät maksut tapahtumiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a><span data-ttu-id="70f45-103">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="70f45-103">Managing Payables</span></span>
<span data-ttu-id="70f45-104">Keskeinen osa ostoreskontraa on toimittajien maksaminen.</span><span class="sxs-lookup"><span data-stu-id="70f45-104">A big part of managing accounts payable is paying your vendors.</span></span> <span data-ttu-id="70f45-105">Voit lisätä toiminnoilla erääntyviin ostolaskuihin maksurivejä **Maksupäiväkirja**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="70f45-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="70f45-106">Voit lähettää tapahtumia pankkiin viemällä useita maksupäiväkirjan rivejä tiedostoon ja ladata sitten tiedoston pankkiin.</span><span class="sxs-lookup"><span data-stu-id="70f45-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="70f45-107">Voit myös maksaa sekeillä ja siirtää sekkejä sähköisinä maksuina.</span><span class="sxs-lookup"><span data-stu-id="70f45-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="70f45-108">Toinen tavallinen tehtävä on lähtevien maksujen kohdistaminen liittyviin toimittajatapahtumiin, jotta liittyvät ostolaskut tai ostohyvityslaskut voidaan sulkea maksettuina.</span><span class="sxs-lookup"><span data-stu-id="70f45-108">Another typical task is to apply outgoing payments to their related vendor ledger entries in order to close purchase invoices or purchase credit memos as paid.</span></span> <span data-ttu-id="70f45-109">Voit tehdä tämän **Maksujen täsmäytyskirjauskansio** -ikkunassa tuomalla pankin tiliotteen ja rekisteröimällä maksut.</span><span class="sxs-lookup"><span data-stu-id="70f45-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="70f45-110">Maksut kohdistetaan avoimiin toimittaja- tai asiakastapahtumiin täsmäyttämällä maksuteksti ja tapahtumatiedot.</span><span class="sxs-lookup"><span data-stu-id="70f45-110">The payments are applied to open vendor or customer ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="70f45-111">Täsmäytykset voi tarkistaa tai niitä voi muuttaa eri tavoilla ennen päiväkirjan kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="70f45-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="70f45-112">Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="70f45-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="70f45-113">Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.</span><span class="sxs-lookup"><span data-stu-id="70f45-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="70f45-114">Vaihtoehtoisesti voit kohdistaa lähtevät maksut manuaalisesti **Maksupäiväkirja**-ikkunassa tai liittyvistä toimittajatapahtumista.</span><span class="sxs-lookup"><span data-stu-id="70f45-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor ledger entries.</span></span>

<span data-ttu-id="70f45-115">Seuraavassa taulukossa on ostoreskontran tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="70f45-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="70f45-116">Toiminta</span><span class="sxs-lookup"><span data-stu-id="70f45-116">To</span></span> | <span data-ttu-id="70f45-117">Katso</span><span class="sxs-lookup"><span data-stu-id="70f45-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="70f45-118">Luo erääntyvät toimittajan maksut, jotka on priorisoitu maksualennusten ja erääntymismaksujen mukaan.</span><span class="sxs-lookup"><span data-stu-id="70f45-118">Generate due vendor payments prioritized according to payment discounts and overdue penalties.</span></span> <span data-ttu-id="70f45-119">Vaihtoehtoisesti voit viedä maksut pankkitiedostoon kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="70f45-119">Optionally, export the payments to a bank file when posting.</span></span> |[<span data-ttu-id="70f45-120">Maksujen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="70f45-120">Make Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="70f45-121">Kohdista toimittajan maksut automaattisesti maksamattomiin ostolaskuihin tuomalla pankin tiliotetiedosto.</span><span class="sxs-lookup"><span data-stu-id="70f45-121">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="70f45-122">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="70f45-122">Apply Payments Automatically and Reconcile Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="70f45-123">Kohdista toimittajan maksut maksamattomiin ostolaskuihin manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="70f45-123">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="70f45-124">Toimintaohje: Toimittajamaksujen täsmäyttäminen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="70f45-124">How to: Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="70f45-125">Varmista varaston oikea arvostus määrittämällä lisätyt nimikekulut, kuten nimikkeiden ostamisessa syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut.</span><span class="sxs-lookup"><span data-stu-id="70f45-125">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="70f45-126">Toimintaohje: Kaupan lisäkustannusten huomiointi nimikekulujen avulla</span><span class="sxs-lookup"><span data-stu-id="70f45-126">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="70f45-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="70f45-127">See Also</span></span>
[<span data-ttu-id="70f45-128">Osto</span><span class="sxs-lookup"><span data-stu-id="70f45-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="70f45-129">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="70f45-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="70f45-130">Toimintaohje: Kaupan lisäkustannusten huomiointi nimikekulujen avulla</span><span class="sxs-lookup"><span data-stu-id="70f45-130">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="70f45-131">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="70f45-131">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="70f45-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="70f45-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

