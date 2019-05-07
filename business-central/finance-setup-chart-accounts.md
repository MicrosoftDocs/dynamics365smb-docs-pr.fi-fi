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
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 8c75a214691b7d9886958866517afbb1d68b6f60
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "920699"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="55028-103">Tilikartan määrittäminen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="55028-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="55028-104">Tilikartta näyttää ne kirjanpidon tilit, joihin on tallennettu taloustietoja.</span><span class="sxs-lookup"><span data-stu-id="55028-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="55028-105">sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.</span><span class="sxs-lookup"><span data-stu-id="55028-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="55028-106">Voit kuitenkin muuttaa oletustilejä ja lisätä uusia tilejä.</span><span class="sxs-lookup"><span data-stu-id="55028-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="55028-107">Tilien lisääminen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="55028-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="55028-108">Voit avata kunkin tilin KP-tilin tilikartasta ja lisätä tai muuttaa asetuksia.</span><span class="sxs-lookup"><span data-stu-id="55028-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="55028-109">Voit poistaa pääkirjanpitotilin.</span><span class="sxs-lookup"><span data-stu-id="55028-109">You can delete a general ledger account.</span></span> <span data-ttu-id="55028-110">Ennen sen poistamista seuraavien on kuitenkin toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="55028-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="55028-111">Tilin saldon tulee olla nolla.</span><span class="sxs-lookup"><span data-stu-id="55028-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="55028-112">**Salli KP-tilin poisto ennen** -kenttä on määritettävä **Pääkirjanpidon asetukset** -sivulla. Tilillä ei saa olla tapahtumakirjauksia kyseisenä päivänä tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="55028-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="55028-113">Jos **Tarkista KP-tilin käyttö** -kenttä on valittu **Pääkirjanpidon asetukset** -sivulla, tiliä ei voi käyttää kirjausryhmässä tai kirjauksen asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="55028-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="55028-114">estää tilikartassa tarvittavia tietoja sisältävän pääkirjanpitotilin poistamisen.</span><span class="sxs-lookup"><span data-stu-id="55028-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="55028-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="55028-115">See Also</span></span>
[<span data-ttu-id="55028-116">Pääkirjanpito ja tilikartta</span><span class="sxs-lookup"><span data-stu-id="55028-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="55028-117">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="55028-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="55028-118">Dimensioiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="55028-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="55028-119">Tietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="55028-119">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="55028-120">KP-raporttimallien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="55028-120">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="55028-121">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="55028-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
