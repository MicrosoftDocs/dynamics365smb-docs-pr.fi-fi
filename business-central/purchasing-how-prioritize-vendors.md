---
title: "Prioriteettitason määrittäminen toimittajalle | Microsoft Docs"
description: "Voit määrittää toimittajille numeron, joka priorisoi ne ja helpottaa maksuehdotuksia Business Central -sovelluksessa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f7834f0f99b775125425eb7209c3c648de4ccd1f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="prioritize-vendors"></a><span data-ttu-id="db128-103">Toimittajien priorisointi</span><span class="sxs-lookup"><span data-stu-id="db128-103">Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="db128-104"> voi ehdottaa eri maksuja toimittajille, esimerkiksi maksuja, jotka erääntyvät pian, ja maksuja, joista voi saada alennuksen.</span><span class="sxs-lookup"><span data-stu-id="db128-104"> can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="db128-105">Lisätietoja on kohdassa [Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="db128-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="db128-106">Ensin priorisoidaan toimittajat liittämällä heille numerot.</span><span class="sxs-lookup"><span data-stu-id="db128-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>

## <a name="to-prioritize-vendors"></a><span data-ttu-id="db128-107">Toimittajien priorisointi</span><span class="sxs-lookup"><span data-stu-id="db128-107">To prioritize vendors</span></span>
1. <span data-ttu-id="db128-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="db128-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="db128-109">Valitse asianmukainen toimittaja ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="db128-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="db128-110">Syötä **Prioriteetti**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="db128-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="db128-111">in mukaan pienin numero (paitsi 0) tarkoittaa korkeinta prioriteettia.</span><span class="sxs-lookup"><span data-stu-id="db128-111"> considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="db128-112">Siten jos käytät esimerkiksi numeroita 1, 2 ja 3, numerolla 1 on korkein prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="db128-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="db128-113">Jos et halua priorisoida toimittajaa, jätä **Prioriteetti**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="db128-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="db128-114">Tämän jälkeen kun käytät maksuehdotusominaisuutta, tämä toimittaja tulee luetteloon kaikkien niiden toimittajien jälkeen, joilla on prioriteettinumero.</span><span class="sxs-lookup"><span data-stu-id="db128-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="db128-115">Prioriteettitasoja voi syöttää kuinka monta tahansa.</span><span class="sxs-lookup"><span data-stu-id="db128-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="db128-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="db128-116">See Also</span></span>
[<span data-ttu-id="db128-117">Ostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="db128-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="db128-118">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="db128-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="db128-119">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="db128-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

