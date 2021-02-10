---
title: Prioriteettitason määrittäminen toimittajalle | Microsoft Docs
description: Voit määrittää toimittajille numeron, joka priorisoi ne ja helpottaa maksuehdotuksia Business Central -sovelluksessa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87d2f7c7fe2d395d16b41b288500f22e16bd0ba0
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758540"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="1ed9b-103">Toimittajien priorisointi</span><span class="sxs-lookup"><span data-stu-id="1ed9b-103">Prioritize Vendors</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1ed9b-104">voi ehdottaa eri maksuja toimittajille, esimerkiksi maksuja, jotka erääntyvät pian, ja maksuja, joista voi saada alennuksen.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="1ed9b-105">Lisätietoja on kohdassa [Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="1ed9b-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="1ed9b-106">Ensin priorisoidaan toimittajat liittämällä heille numerot.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a><span data-ttu-id="1ed9b-107">Toimittajien priorisointi</span><span class="sxs-lookup"><span data-stu-id="1ed9b-107">To prioritize vendors</span></span>
1. <span data-ttu-id="1ed9b-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="1ed9b-109">Valitse asianmukainen toimittaja ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="1ed9b-110">Syötä **Prioriteetti**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)]<span data-ttu-id="1ed9b-111">in mukaan pienin numero (paitsi 0) tarkoittaa korkeinta prioriteettia.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-111">considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="1ed9b-112">Siten jos käytät esimerkiksi numeroita 1, 2 ja 3, numerolla 1 on korkein prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="1ed9b-113">Jos et halua priorisoida toimittajaa, jätä **Prioriteetti**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="1ed9b-114">Tämän jälkeen kun käytät maksuehdotusominaisuutta, tämä toimittaja tulee luetteloon kaikkien niiden toimittajien jälkeen, joilla on prioriteettinumero.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="1ed9b-115">Prioriteettitasoja voi syöttää kuinka monta tahansa.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ed9b-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1ed9b-116">See Also</span></span>
[<span data-ttu-id="1ed9b-117">Ostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1ed9b-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="1ed9b-118">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="1ed9b-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="1ed9b-119">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ed9b-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
