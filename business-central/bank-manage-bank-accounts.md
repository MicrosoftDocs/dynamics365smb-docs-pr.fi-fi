---
title: Pankkitilien hallinta |Microsoft Docs
description: "Pankkitapahtumat on täsmäytettävä säännöllisesti niihin liittyviin pankkitilitapahtumiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 62b2bf8987146a69d17bd343f88d31d60a205ffb
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="7e76c-103">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="7e76c-103">Managing Bank Accounts</span></span>
<span data-ttu-id="7e76c-104">Täsmäytä [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilitapahtumat säännöllisin väliajoin pankin pankkitilin liittyvien pankkitapahtumien kanssa. Kirjaa sitten saldo pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="7e76c-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="7e76c-105">Voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -kohdassa pankin tiliotteessa olevien maksujen käsittelyn osana.</span><span class="sxs-lookup"><span data-stu-id="7e76c-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="7e76c-106">Vaihtoehtoisesti voit suorittaa tehtävän erikseen maksukäsittelystä **Pankkitilin täsmäytys** -sivulla, jossa etsit vastaavat (täsmäytät) pankin tiliotteen rivit vasemmassa ruudussa sisäisen pankkitilin kirjanpidon tapahtumien kanssa oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="7e76c-106">Alternatively, you can perform the task separately from payment processing, on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="7e76c-107">Molemmilla sivuilla voi täyttää pankin tiliotteen tiedot tuomalla tiedoston tai syötteen ja voit käyttää automaattisia vastaavuusehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="7e76c-107">In both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="7e76c-108">Pohjois-Amerikan versioissa, voit suorittaa pankkitilin täsmäytyksen myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille, mutta ei tarjoa pankin tiliotetiedostojen tuomista.</span><span class="sxs-lookup"><span data-stu-id="7e76c-108">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="7e76c-109">Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7e76c-109">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="7e76c-110">Lisätietoja löydät Yhdysvaltain paikalliset toiminnot -ohjeen Pankkitilien täsmäyttäminen -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="7e76c-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="7e76c-111">[!INCLUDE[d365fin](includes/d365fin_md.md)]issa on joskus siirrettävä summia pankkitilien välillä pankin siirtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7e76c-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="7e76c-112">Tämä tehtävä suoritetaan **Yleinen päiväkirja** -sivulla varojen valuutan osoittamalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="7e76c-112">You perform this task on the **General Journal** page, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="7e76c-113">Jokainen pankkitili on määritettävä pankkitilin kortiksi, ennen kuin pankkitilejä voidaan hallita.</span><span class="sxs-lookup"><span data-stu-id="7e76c-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="7e76c-114">Lisäksi on määritettävä sähköiset palvelut, joita käytetään pankin tiliotteen tuonnissa ja maksutiedoston viennissä.</span><span class="sxs-lookup"><span data-stu-id="7e76c-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="7e76c-115">Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="7e76c-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="7e76c-116">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="7e76c-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="7e76c-117">Toiminta</span><span class="sxs-lookup"><span data-stu-id="7e76c-117">To</span></span> | <span data-ttu-id="7e76c-118">Katso</span><span class="sxs-lookup"><span data-stu-id="7e76c-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="7e76c-119">Täsmäytä maksukäsittelyyn liittyvät pankkitilit **Maksujen täsmäytyskirjauskansio** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7e76c-119">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="7e76c-120">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="7e76c-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="7e76c-121">Täsmäytä pankkitilit, kuten sekkitapahtumat, erillisinä tehtävinä **Pankkitilin täsmäytys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7e76c-121">Reconcile bank accounts, including check ledger entries, as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="7e76c-122">Pankkitilien täsmäyttäminen erikseen</span><span class="sxs-lookup"><span data-stu-id="7e76c-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="7e76c-123">Kirjaa pankkitilien väliset siirrot samassa valuutassa tai eri valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="7e76c-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="7e76c-124">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="7e76c-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="7e76c-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7e76c-125">See Also</span></span>
[<span data-ttu-id="7e76c-126">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7e76c-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="7e76c-127">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="7e76c-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="7e76c-128">[Ostovelkojen hallinta](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="7e76c-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="7e76c-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e76c-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="7e76c-130">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="7e76c-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

