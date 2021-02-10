---
title: Tilikartan määrittäminen
description: Voit muuttaa tilikartan oletustilejä ja lisätä uusia tilejä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b20c4680393fa13b260beca366c7e4ba04abb291
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750378"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="d1c20-103">Tilikartan määrittäminen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="d1c20-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="d1c20-104">Tilikartta näyttää ne kirjanpidon tilit, joihin on tallennettu taloustietoja.</span><span class="sxs-lookup"><span data-stu-id="d1c20-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d1c20-105">sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.</span><span class="sxs-lookup"><span data-stu-id="d1c20-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="d1c20-106">Voit kuitenkin muuttaa oletustilejä ja lisätä uusia tilejä.</span><span class="sxs-lookup"><span data-stu-id="d1c20-106">However, you can change the default accounts, and you can add new accounts.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="d1c20-107">Tilien lisääminen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="d1c20-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="d1c20-108">Voit avata kunkin tilin KP-tilin tilikartasta ja lisätä tai muuttaa asetuksia.</span><span class="sxs-lookup"><span data-stu-id="d1c20-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d1c20-109">Voit poistaa pääkirjanpitotilin.</span><span class="sxs-lookup"><span data-stu-id="d1c20-109">You can delete a general ledger account.</span></span> <span data-ttu-id="d1c20-110">Ennen sen poistamista seuraavien on kuitenkin toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="d1c20-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="d1c20-111">Tilin saldon tulee olla nolla.</span><span class="sxs-lookup"><span data-stu-id="d1c20-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="d1c20-112">**Salli KP-tilin poisto ennen** -kenttä on määritettävä **Pääkirjanpidon asetukset** -sivulla. Tilillä ei saa olla tapahtumakirjauksia kyseisenä päivänä tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d1c20-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="d1c20-113">Jos **Tarkista KP-tilin käyttö** -kenttä on valittu **Pääkirjanpidon asetukset** -sivulla, tiliä ei voi käyttää kirjausryhmässä tai kirjauksen asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="d1c20-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d1c20-114">estää tilikartassa tarvittavia tietoja sisältävän pääkirjanpitotilin poistamisen.</span><span class="sxs-lookup"><span data-stu-id="d1c20-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="d1c20-115">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="d1c20-115">See Related Training at [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="d1c20-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d1c20-116">See Also</span></span>
[<span data-ttu-id="d1c20-117">Pääkirjanpito ja tilikartta</span><span class="sxs-lookup"><span data-stu-id="d1c20-117">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="d1c20-118">Pankkitilien täsmäytys</span><span class="sxs-lookup"><span data-stu-id="d1c20-118">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="d1c20-119">Dimensioiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="d1c20-119">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="d1c20-120">Tietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="d1c20-120">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="d1c20-121">KP-raporttimallien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="d1c20-121">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="d1c20-122">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d1c20-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]
