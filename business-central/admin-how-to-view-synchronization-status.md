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
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620882"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="027a5-103">Synkronoinnin tilan näyttäminen</span><span class="sxs-lookup"><span data-stu-id="027a5-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="027a5-104">Voit tarkastella sellaisten yksittäisten synkronointitöiden tilaa, jotka on suoritettu [!INCLUDE[crm_md](includes/crm_md.md)] -integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="027a5-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="027a5-105">Tämä sisältää synkronointityöt, jotka on suoritettu työjonosta, ja manuaaliset synkronointityöt, jotka on suoritettu [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueista.</span><span class="sxs-lookup"><span data-stu-id="027a5-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="027a5-106">Tästä on hyötyä synkronointiongelmien vianmäärityksessä, koska sen avulla saat tietoja yksittäisistä virheistä.</span><span class="sxs-lookup"><span data-stu-id="027a5-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="027a5-107">Tarkastellaksesi synkronisaatio-ongelmia yhdistetyille tietuielle</span><span class="sxs-lookup"><span data-stu-id="027a5-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="027a5-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Yhdistettyjen tietojen synkronointivirheet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="027a5-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="027a5-109">**Yhdistettyjen Tietojen Synkrnoiniti Virheet** esittää ongelmat jotka tapahtuivat yhdistetyjen tietuiden synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="027a5-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="027a5-110">Voit suodattaa ja lajitella tietueita ja suorittaa toimintoja kuten **Palauta** tai **Poistat Tietue** ratkaistaksesi ongelmat yksi kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="027a5-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="027a5-111">Tietyn (manuaalisesti synkronoidun) tietueen synkronointilokin näyttäminen</span><span class="sxs-lookup"><span data-stu-id="027a5-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="027a5-112">Esimerkiksi, voit avata asiakkaan, esineen tai minkä tahansa muun tietueen joka synkronisoi tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="027a5-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="027a5-113">Valitse **Synkronointiloki** toimenpide tarkastellaksesi valitun tietueen synkronointilokia.</span><span class="sxs-lookup"><span data-stu-id="027a5-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="027a5-114">Esimerkiksi tiettyä asiakasta jonka synkronoit manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="027a5-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="027a5-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="027a5-115">See Also</span></span>  
[<span data-ttu-id="027a5-116">Dynamics 365 for Sales -integroinnin määrittäminen Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="027a5-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="027a5-117">Dynamics 365 for Salesin käyttö Business Centralista</span><span class="sxs-lookup"><span data-stu-id="027a5-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
