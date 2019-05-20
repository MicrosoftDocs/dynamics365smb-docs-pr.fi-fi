---
title: Synkronoinnin tilan näyttäminen | Microsoft Docs
description: Lisätietoja yksittäisen synkronointityö tilan näyttämisestä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245683"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="3dace-103">Synkronoinnin tilan näyttäminen</span><span class="sxs-lookup"><span data-stu-id="3dace-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="3dace-104">Voit tarkastella sellaisten yksittäisten synkronointitöiden tilaa, jotka on suoritettu [!INCLUDE[crm_md](includes/crm_md.md)] -integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="3dace-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="3dace-105">Tämä sisältää synkronointityöt, jotka on suoritettu työjonosta, ja manuaaliset synkronointityöt, jotka on suoritettu [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueista.</span><span class="sxs-lookup"><span data-stu-id="3dace-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3dace-106">Tästä on hyötyä synkronointiongelmien vianmäärityksessä, koska sen avulla saat tietoja yksittäisistä virheistä.</span><span class="sxs-lookup"><span data-stu-id="3dace-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="3dace-107">Kaikkien synkronointiongelmien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="3dace-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="3dace-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Yhdistettyjen tietojen synkronointivirheet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3dace-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="3dace-109">Voit tarkastella **Yhdistettyjen tietojen synkronointivirheet** -sivulla kaikki ongelmia, joita tapahtui synkronoitaessa tietoja [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in välillä, suodattaa ja lajitella sivulla olevia tietoja taulukon ja virhesanoman mukaan sekä ratkaista ongelmia yksitellen tai joukkotoiminnolla esimerkiksi **Yritä uudelleen**- tai **Poista yhdistäminen** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="3dace-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="3dace-110">Tietyn (manuaalisesti synkronoidun) tietueen synkronointilokin näyttäminen</span><span class="sxs-lookup"><span data-stu-id="3dace-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="3dace-111">Avaa esimerkiksi asiakas-, nimike- tai muu tietue, joka synkronoi tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="3dace-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="3dace-112">Valitse **Synkronointiloki**-toiminto, jos haluat tarkastella valitun tietueen synkronointilokia. Kyse voi olla esimerkiksi tietystä manuaalisesti synkronoidusta asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="3dace-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="3dace-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3dace-113">See Also</span></span>  
[<span data-ttu-id="3dace-114">Dynamics 365 for Sales -integroinnin määrittäminen Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="3dace-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="3dace-115">Dynamics 365 for Salesin käyttö Business Centralista</span><span class="sxs-lookup"><span data-stu-id="3dace-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
