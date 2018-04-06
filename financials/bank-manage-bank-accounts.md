---
title: Pankkitilien hallinta |Microsoft Docs
description: "Pankkitapahtumat on täsmäytettävä säännöllisesti niihin liittyviin pankkitilitapahtumiin Financialsissa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 20ff1bad076bff8ce07716cfffc2fa5e05605bb2
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="2b841-103">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="2b841-103">Managing Bank Accounts</span></span>
<span data-ttu-id="2b841-104">Täsmäytä [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilitapahtumat säännöllisin väliajoin pankin pankkitilin liittyvien pankkitapahtumien kanssa. Kirjaa sitten saldo pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="2b841-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="2b841-105">Voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -kohdassa pankin tiliotteessa olevien maksujen käsittelyn osana.</span><span class="sxs-lookup"><span data-stu-id="2b841-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="2b841-106">Vaihtoehtoisesti voit suorittaa tehtävän maksujen käsittelyn ulkopuolella **Pankkitilin täsmäytys** -ikkunassa. Tämä tukee sekkitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="2b841-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window, which supports check ledger entries.</span></span> <span data-ttu-id="2b841-107">Molemmissa tapauksissa ikkunat täytetään tuomalla tiliote [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="2b841-107">In both cases, you fill in the windows by importing the bank statement into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="2b841-108">[!INCLUDE[d365fin](includes/d365fin_md.md)]issa on joskus siirrettävä summia pankkitilien välillä pankin siirtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="2b841-108">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="2b841-109">Tämä tehtävä suoritetaan **Yleinen päiväkirja** -ikkunassa varojen valuutan osoittamalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="2b841-109">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="2b841-110">Jokainen pankkitili on määritettävä pankkitilin kortiksi, ennen kuin pankkitilejä voidaan hallita.</span><span class="sxs-lookup"><span data-stu-id="2b841-110">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="2b841-111">Lisäksi on määritettävä sähköiset palvelut, joita käytetään pankin tiliotteen tuonnissa ja maksutiedoston viennissä.</span><span class="sxs-lookup"><span data-stu-id="2b841-111">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="2b841-112">Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="2b841-112">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="2b841-113">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="2b841-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="2b841-114">Toiminta</span><span class="sxs-lookup"><span data-stu-id="2b841-114">To</span></span> | <span data-ttu-id="2b841-115">Katso</span><span class="sxs-lookup"><span data-stu-id="2b841-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="2b841-116">Täsmäytä maksukäsittelyyn liittyvät pankkitilit **Maksujen täsmäytyskirjauskansio** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="2b841-116">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="2b841-117">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="2b841-117">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="2b841-118">Täsmäytä pankkitilit, kuten sekkitapahtumat, erillisinä tehtävinä **Pankkitilin täsmäytys** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="2b841-118">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="2b841-119">Pankkitilien täsmäyttäminen erikseen</span><span class="sxs-lookup"><span data-stu-id="2b841-119">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="2b841-120">Kirjaa pankkitilien väliset siirrot samassa valuutassa tai eri valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="2b841-120">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="2b841-121">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="2b841-121">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="2b841-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2b841-122">See Also</span></span>
[<span data-ttu-id="2b841-123">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2b841-123">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="2b841-124">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="2b841-124">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="2b841-125">[Ostovelkojen hallinta](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="2b841-125">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="2b841-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2b841-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2b841-127">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="2b841-127">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

