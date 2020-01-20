---
title: Pankkitilien hallinta |Microsoft Docs
description: Pankkitapahtumat on täsmäytettävä säännöllisesti niihin liittyviin pankkitilitapahtumiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 01/10/2020
ms.author: sgroespe
ms.openlocfilehash: 0d1a38468f5d07a1170027bc728ba16996f2b782
ms.sourcegitcommit: 2f741f442226b8be74586e355f283f365e43220f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947235"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="56e1f-103">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="56e1f-103">Reconciling Bank Accounts</span></span>
<span data-ttu-id="56e1f-104">Pankkitilin täsmäytys tulee suorittaa säännöllisin väliajoin kaikille pankkitileille, jotta yrityksen käteistietueet ovat oikein.</span><span class="sxs-lookup"><span data-stu-id="56e1f-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="56e1f-105">Voit tehdä tämän vertaamalla sisäisten pankkitilien tapahtumia pankkitapahtumiin pankistasi ja kirjaamalla sitten saldot sisäisiin pankkitileihin, jolloin summat ovat talouspäälliköiden käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="56e1f-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="56e1f-106">Pankkitilin täsmäytys on myös käytännöllinen tapa löytää ja ratkaista puuttuvat maksut ja kirjanpitovirheet.</span><span class="sxs-lookup"><span data-stu-id="56e1f-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="56e1f-107">Voit suorittaa tehtävän erikseen maksukäsittelystä **Pankkitilin täsmäytys** -sivulla, jossa etsit vastaavat (täsmäytät) vasemmassa ruudussa olevat pankin tiliotteen rivit oikealla puolella olevien sisäisen pankkitilin kirjanpidon tapahtumien kanssa.</span><span class="sxs-lookup"><span data-stu-id="56e1f-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="56e1f-108">Vaihtoehtoisesti voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -sivulla pankin tiliotteessa olevien maksujen käsittelyn osana.</span><span class="sxs-lookup"><span data-stu-id="56e1f-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="56e1f-109">Molemmilla sivuilla voi täyttää pankin tiliotteen tiedot tuomalla tiedoston tai syötteen ja voit käyttää automaattisia vastaavuusehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="56e1f-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="56e1f-110">Pohjois-Amerikan versioissa, voit suorittaa pankkitilin täsmäytyksen myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille, mutta ei tarjoa pankin tiliotetiedostojen tuomista.</span><span class="sxs-lookup"><span data-stu-id="56e1f-110">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="56e1f-111">Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="56e1f-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="56e1f-112">Lisätietoja löydät Yhdysvaltain paikalliset toiminnot -ohjeen Pankkitilien täsmäyttäminen -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="56e1f-112">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="56e1f-113">Jokainen pankkitili on määritettävä pankkitilin kortiksi, ennen kuin pankkitilejä voidaan hallita kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="56e1f-113">Before you can manage your bank accounts within [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="56e1f-114">Lisäksi on määritettävä sähköiset palvelut, joita käytetään pankin tiliotteen tuonnissa ja maksutiedoston viennissä.</span><span class="sxs-lookup"><span data-stu-id="56e1f-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="56e1f-115">Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="56e1f-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="56e1f-116">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="56e1f-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="56e1f-117">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="56e1f-117">To</span></span> | <span data-ttu-id="56e1f-118">Katso</span><span class="sxs-lookup"><span data-stu-id="56e1f-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="56e1f-119">Täsmäytä pankkitilit erillisenä tehtävänä **Pankkitilin täsmäytys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="56e1f-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="56e1f-120">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="56e1f-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="56e1f-121">Täsmäytä maksukäsittelyyn liittyvät pankkitilit **Maksujen täsmäytyskirjauskansio** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="56e1f-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="56e1f-122">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="56e1f-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learnlearnpathsreconcile-bank-accounts-dynamics-365-business-central"></a><span data-ttu-id="56e1f-123">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="56e1f-123">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="56e1f-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="56e1f-124">See Also</span></span>
[<span data-ttu-id="56e1f-125">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="56e1f-125">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="56e1f-126">Siirrä pankkivarat</span><span class="sxs-lookup"><span data-stu-id="56e1f-126">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="56e1f-127">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="56e1f-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="56e1f-128">[Ostovelkojen hallinta](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="56e1f-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="56e1f-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56e1f-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="56e1f-130">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="56e1f-130">General Business Functionality</span></span>](ui-across-business-areas.md)
