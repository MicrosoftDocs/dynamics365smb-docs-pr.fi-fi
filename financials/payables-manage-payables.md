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
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: d59c00f7a00854639250ae587805dece50fd1d78
ms.contentlocale: fi-fi
ms.lasthandoff: 02/02/2018

---
# <a name="managing-payables"></a><span data-ttu-id="6b1df-103">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="6b1df-103">Managing Payables</span></span>
<span data-ttu-id="6b1df-104">Keskeinen osa ostoreskontran hoitoa on toimittajille maksamista tai kulujen hyvittämistä työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="6b1df-104">A big part of managing accounts payable is paying your vendors, or reimbursing your employees for expenses.</span></span> <span data-ttu-id="6b1df-105">Voit lisätä toiminnoilla erääntyviin ostolaskuihin maksurivejä **Maksupäiväkirja**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="6b1df-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="6b1df-106">Voit lähettää tapahtumia pankkiin viemällä useita maksupäiväkirjan rivejä tiedostoon ja ladata sitten tiedoston pankkiin.</span><span class="sxs-lookup"><span data-stu-id="6b1df-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="6b1df-107">Voit myös maksaa sekeillä ja siirtää sekkejä sähköisinä maksuina.</span><span class="sxs-lookup"><span data-stu-id="6b1df-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="6b1df-108">Toinen tavallinen tehtävä on lähtevien maksujen kohdistaminen liittyviin toimittaja- tai työntekijätapahtumiin, jotta ostolaskut, ostohyvityslaskut tai työntekijätilit voidaan sulkea maksettuina.</span><span class="sxs-lookup"><span data-stu-id="6b1df-108">Another typical task is to apply outgoing payments to their related vendor or employee ledger entries in order to close purchase invoices, purchase credit memos, or employee accounts as paid.</span></span> <span data-ttu-id="6b1df-109">Voit tehdä tämän **Maksujen täsmäytyskirjauskansio** -ikkunassa tuomalla pankin tiliotteen ja rekisteröimällä maksut.</span><span class="sxs-lookup"><span data-stu-id="6b1df-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="6b1df-110">Maksut kohdistetaan avoimiin toimittaja-, asiakas- tai työntekijätapahtumiin täsmäyttämällä maksuteksti ja tapahtumatiedot.</span><span class="sxs-lookup"><span data-stu-id="6b1df-110">The payments are applied to open vendor, customer, or employee ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="6b1df-111">Täsmäytykset voi tarkistaa tai niitä voi muuttaa eri tavoilla ennen päiväkirjan kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="6b1df-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="6b1df-112">Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6b1df-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="6b1df-113">Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.</span><span class="sxs-lookup"><span data-stu-id="6b1df-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="6b1df-114">Vaihtoehtoisesti voit kohdistaa lähtevät maksut manuaalisesti **Maksupäiväkirja**-ikkunassa tai liittyvistä toimittaja- tai työntekijätapahtumista.</span><span class="sxs-lookup"><span data-stu-id="6b1df-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor or employee ledger entries.</span></span>

<span data-ttu-id="6b1df-115">Seuraavassa taulukossa on ostoreskontran tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="6b1df-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="6b1df-116">Toiminta</span><span class="sxs-lookup"><span data-stu-id="6b1df-116">To</span></span> | <span data-ttu-id="6b1df-117">Katso</span><span class="sxs-lookup"><span data-stu-id="6b1df-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="6b1df-118">Luo toimittajien maksuja tai työntekijöiden hyvityksiä, valmistele suoritettavat sekkimaksut ja vie maksut pankkitiedostoon kirjauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6b1df-118">Generate due vendor payments or employee reimbursements, prepare check payments, and export payments to a bank file when posting.</span></span> |[<span data-ttu-id="6b1df-119">Maksujen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="6b1df-119">Making Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="6b1df-120">Kohdista toimittajan maksut automaattisesti maksamattomiin ostolaskuihin tuomalla pankin tiliotetiedosto.</span><span class="sxs-lookup"><span data-stu-id="6b1df-120">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="6b1df-121">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="6b1df-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="6b1df-122">Kohdista toimittajan maksut maksamattomiin ostolaskuihin manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="6b1df-122">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="6b1df-123">Toimittajamaksujen täsmäyttäminen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="6b1df-123">Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="6b1df-124">Varmista varaston oikea arvostus määrittämällä lisätyt nimikekulut, kuten nimikkeiden ostamisessa syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut.</span><span class="sxs-lookup"><span data-stu-id="6b1df-124">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="6b1df-125">Kaupan lisäkustannusten huomiointi nimikekulujen avulla</span><span class="sxs-lookup"><span data-stu-id="6b1df-125">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="6b1df-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6b1df-126">See Also</span></span>
[<span data-ttu-id="6b1df-127">Osto</span><span class="sxs-lookup"><span data-stu-id="6b1df-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="6b1df-128">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="6b1df-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="6b1df-129">Kaupan lisäkustannusten huomiointi nimikekulujen avulla</span><span class="sxs-lookup"><span data-stu-id="6b1df-129">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="6b1df-130">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="6b1df-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="6b1df-131">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6b1df-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

