---
title: Pankkitilien hallinta |Microsoft Docs
description: "Pankkitapahtumat on täsmäytettävä säännöllisesti niihin liittyviin pankkitilitapahtumiin Financialsissa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: dd3068cc1af6a16a43f982d3b48cdec42a7d7eca
ms.contentlocale: fi-fi
ms.lasthandoff: 05/17/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="9584a-103">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="9584a-103">Managing Bank Accounts</span></span>
<span data-ttu-id="9584a-104">Täsmäytä [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilitapahtumat säännöllisin väliajoin pankin pankkitilin liittyvien pankkitapahtumien kanssa. Kirjaa sitten saldo pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="9584a-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="9584a-105">Voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -kohdassa pankin tiliotteessa olevien maksujen käsittelyn osana.</span><span class="sxs-lookup"><span data-stu-id="9584a-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="9584a-106">Vaihtoehtoisesti voit suorittaa tehtävän erikseen maksukäsittelystä **Pankkitilin täsmäytys** -ikkunasta, jossa etsit vastaavat (täsmäytät) pankin tiliotteen rivit vasemmassa ruudussa sisäisen pankkitilin kirjanpidon tapahtumien kanssa oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="9584a-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="9584a-107">Molemmissa ikkunoissa voi täyttää pankin tiliotteen tiedot tuomalla tiedoston tai syötteen ja voit käyttää automaattisia vastaavuusehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="9584a-107">In both windows, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="9584a-108">Pohjois-Amerikan versioissa, voit suorittaa pankkitilin täsmäytyksen myös **Pankin täsmäytyksen työkirja** -ikkunassa, joka sopii paremmin sekeille ja talletuksille, mutta ei tarjoa pankin tiliotetiedostojen tuomista.</span><span class="sxs-lookup"><span data-stu-id="9584a-108">In North American versions, you can also perform bank reconciliation in the **Bank Rec. Worksheet** window, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="9584a-109">Voit käyttää tätä ikkunaa **Pankkitilin täsmäytys** -ikkunan sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinnan **Pääkirjanpidon asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="9584a-109">To use this window instead of the **Bank Acc. Reconciliation** window, deselect the **Bank Recon. with Auto. Match** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="9584a-110">Lisätietoja löydät Yhdysvaltain paikalliset toiminnot -ohjeen Pankkitilien täsmäyttäminen -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="9584a-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="9584a-111">[!INCLUDE[d365fin](includes/d365fin_md.md)]issa on joskus siirrettävä summia pankkitilien välillä pankin siirtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="9584a-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="9584a-112">Tämä tehtävä suoritetaan **Yleinen päiväkirja** -ikkunassa varojen valuutan osoittamalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="9584a-112">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="9584a-113">Jokainen pankkitili on määritettävä pankkitilin kortiksi, ennen kuin pankkitilejä voidaan hallita.</span><span class="sxs-lookup"><span data-stu-id="9584a-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="9584a-114">Lisäksi on määritettävä sähköiset palvelut, joita käytetään pankin tiliotteen tuonnissa ja maksutiedoston viennissä.</span><span class="sxs-lookup"><span data-stu-id="9584a-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="9584a-115">Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="9584a-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="9584a-116">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="9584a-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="9584a-117">Toiminta</span><span class="sxs-lookup"><span data-stu-id="9584a-117">To</span></span> | <span data-ttu-id="9584a-118">Katso</span><span class="sxs-lookup"><span data-stu-id="9584a-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="9584a-119">Täsmäytä maksukäsittelyyn liittyvät pankkitilit **Maksujen täsmäytyskirjauskansio** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="9584a-119">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="9584a-120">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="9584a-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="9584a-121">Täsmäytä pankkitilit, kuten sekkitapahtumat, erillisinä tehtävinä **Pankkitilin täsmäytys** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="9584a-121">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="9584a-122">Pankkitilien täsmäyttäminen erikseen</span><span class="sxs-lookup"><span data-stu-id="9584a-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="9584a-123">Kirjaa pankkitilien väliset siirrot samassa valuutassa tai eri valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="9584a-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="9584a-124">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="9584a-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="9584a-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9584a-125">See Also</span></span>
[<span data-ttu-id="9584a-126">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9584a-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="9584a-127">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="9584a-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="9584a-128">[Ostovelkojen hallinta](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="9584a-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="9584a-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9584a-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9584a-130">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="9584a-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

