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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: b31bc4fb174c78092986c14f97232d8498974834
ms.sourcegitcommit: f9f805282c86fda55843f7a11020fb3df861d50e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2019
ms.locfileid: "2764478"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="f35d2-103">Tilikartan määrittäminen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="f35d2-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="f35d2-104">Tilikartta näyttää ne kirjanpidon tilit, joihin on tallennettu taloustietoja.</span><span class="sxs-lookup"><span data-stu-id="f35d2-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="f35d2-105">sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.</span><span class="sxs-lookup"><span data-stu-id="f35d2-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="f35d2-106">Voit kuitenkin muuttaa oletustilejä ja lisätä uusia tilejä.</span><span class="sxs-lookup"><span data-stu-id="f35d2-106">However, you can change the default accounts, and you can add new accounts.</span></span> 
<br><br>  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE43KO9]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="f35d2-107">Tilien lisääminen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="f35d2-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="f35d2-108">Voit avata kunkin tilin KP-tilin tilikartasta ja lisätä tai muuttaa asetuksia.</span><span class="sxs-lookup"><span data-stu-id="f35d2-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f35d2-109">Voit poistaa pääkirjanpitotilin.</span><span class="sxs-lookup"><span data-stu-id="f35d2-109">You can delete a general ledger account.</span></span> <span data-ttu-id="f35d2-110">Ennen sen poistamista seuraavien on kuitenkin toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="f35d2-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="f35d2-111">Tilin saldon tulee olla nolla.</span><span class="sxs-lookup"><span data-stu-id="f35d2-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="f35d2-112">**Salli KP-tilin poisto ennen** -kenttä on määritettävä **Pääkirjanpidon asetukset** -sivulla. Tilillä ei saa olla tapahtumakirjauksia kyseisenä päivänä tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f35d2-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="f35d2-113">Jos **Tarkista KP-tilin käyttö** -kenttä on valittu **Pääkirjanpidon asetukset** -sivulla, tiliä ei voi käyttää kirjausryhmässä tai kirjauksen asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="f35d2-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="f35d2-114">estää tilikartassa tarvittavia tietoja sisältävän pääkirjanpitotilin poistamisen.</span><span class="sxs-lookup"><span data-stu-id="f35d2-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f35d2-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f35d2-115">See Also</span></span>
[<span data-ttu-id="f35d2-116">Pääkirjanpito ja tilikartta</span><span class="sxs-lookup"><span data-stu-id="f35d2-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="f35d2-117">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="f35d2-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="f35d2-118">Dimensioiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f35d2-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="f35d2-119">Tietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="f35d2-119">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="f35d2-120">KP-raporttimallien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f35d2-120">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="f35d2-121">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f35d2-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
