---
title: Pankkitilien hallinta |Microsoft Docs
description: Pankkitapahtumat on täsmäytettävä säännöllisesti niihin liittyviin pankkitilitapahtumiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 7d7ca565218f45a753abd7e468e201538d0e6841
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786519"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="c3150-103">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="c3150-103">Reconciling Bank Accounts</span></span>

<span data-ttu-id="c3150-104">Pankkitilin täsmäytys tulee suorittaa säännöllisin väliajoin kaikille pankkitileille, jotta yrityksen käteistietueet ovat oikein.</span><span class="sxs-lookup"><span data-stu-id="c3150-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="c3150-105">Voit tehdä tämän vertaamalla sisäisten pankkitilien tapahtumia pankkitapahtumiin pankistasi ja kirjaamalla sitten saldot sisäisiin pankkitileihin, jolloin summat ovat talouspäälliköiden käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="c3150-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="c3150-106">Pankkitilin täsmäytys on myös käytännöllinen tapa löytää ja ratkaista puuttuvat maksut ja kirjanpitovirheet.</span><span class="sxs-lookup"><span data-stu-id="c3150-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="c3150-107">Voit suorittaa tehtävän erikseen maksukäsittelystä **Pankkitilin täsmäytys** -sivulla, jossa etsit vastaavat (täsmäytät) vasemmassa ruudussa olevat pankin tiliotteen rivit oikealla puolella olevien sisäisen pankkitilin kirjanpidon tapahtumien kanssa.</span><span class="sxs-lookup"><span data-stu-id="c3150-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="c3150-108">Vaihtoehtoisesti voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -sivulla pankin tiliotteessa olevien maksujen käsittelyn osana.</span><span class="sxs-lookup"><span data-stu-id="c3150-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="c3150-109">Molemmilla sivuilla voi täyttää pankin tiliotteen tiedot tuomalla tiedoston tai syötteen ja voit käyttää automaattisia vastaavuusehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="c3150-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="c3150-110">Pohjois-Amerikan versioissa voi suorittaa pankkitilin täsmäytyksen myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille mutta ei sisällä pankin tiliotetiedostojen tuontia.</span><span class="sxs-lookup"><span data-stu-id="c3150-110">In the North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="c3150-111">Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c3150-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="c3150-112">Lisätietoja on kohdan [Pankkitilien täsmäyttäminen](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) Yhdysvaltain paikallisissa toimintoja käsittelevässä osassa.</span><span class="sxs-lookup"><span data-stu-id="c3150-112">For more information, see [Reconcile Bank Accounts](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under United States Local Functionality.</span></span>

<span data-ttu-id="c3150-113">Jokainen pankkitili on määritettävä pankkitilin kortiksi, ennen kuin pankkitilejä voidaan hallita kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c3150-113">Before you can manage your bank accounts within [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="c3150-114">Lisäksi on määritettävä sähköiset palvelut, joita käytetään pankin tiliotteen tuonnissa ja maksutiedoston viennissä.</span><span class="sxs-lookup"><span data-stu-id="c3150-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="c3150-115">Lisätietoja on kohdassa [Pankkitoiminnan määrittäminen](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="c3150-115">For more information, see [Setting Up Banking](bank-setup-banking.md).</span></span>

<span data-ttu-id="c3150-116">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="c3150-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="c3150-117">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="c3150-117">To</span></span> | <span data-ttu-id="c3150-118">Katso</span><span class="sxs-lookup"><span data-stu-id="c3150-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="c3150-119">Täsmäytä pankkitilit erillisenä tehtävänä **Pankkitilin täsmäytys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c3150-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="c3150-120">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="c3150-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="c3150-121">Täsmäytä maksukäsittelyyn liittyvät pankkitilit **Maksujen täsmäytyskirjauskansio** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c3150-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="c3150-122">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="c3150-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> <span data-ttu-id="c3150-123">Pankkitilin täsmäytyksen avulla voi varmistaa, että kirjat ovat ajan tasalla ja että täsmäytystä ei kirjata, ennen kuin olet tyytyväinen täsmäytykseen.</span><span class="sxs-lookup"><span data-stu-id="c3150-123">Use bank reconciliation to help verify that your books are up-to-date, and do not post the reconciliation until you are satisfied with the reconciliation.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="c3150-124">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="c3150-124">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="c3150-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c3150-125">See Also</span></span>

[<span data-ttu-id="c3150-126">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c3150-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="c3150-127">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="c3150-127">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md)  
[<span data-ttu-id="c3150-128">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="c3150-128">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[<span data-ttu-id="c3150-129">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="c3150-129">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="c3150-130">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="c3150-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="c3150-131">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="c3150-131">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="c3150-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c3150-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c3150-133">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="c3150-133">General Business Functionality</span></span>](ui-across-business-areas.md)
