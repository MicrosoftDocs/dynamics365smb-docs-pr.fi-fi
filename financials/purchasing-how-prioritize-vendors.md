---
title: "Prioriteettitason määrittäminen toimittajalle | Microsoft Docs"
description: "Voit määrittää toimittajille numeron, joka priorisoi ne ja helpottaa maksuehdotuksia Finance and Operations, Business editionissa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d44e06f4dd33332e8d96e712e93ed05c7f0a920b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="prioritize-vendors"></a><span data-ttu-id="8cd20-103">Toimittajien priorisointi</span><span class="sxs-lookup"><span data-stu-id="8cd20-103">Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="8cd20-104"> voi ehdottaa eri maksuja toimittajille, esimerkiksi maksuja, jotka erääntyvät pian, ja maksuja, joista voi saada alennuksen.</span><span class="sxs-lookup"><span data-stu-id="8cd20-104"> can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="8cd20-105">Lisätietoja on kohdassa [Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="8cd20-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="8cd20-106">Ensin priorisoidaan toimittajat liittämällä heille numerot.</span><span class="sxs-lookup"><span data-stu-id="8cd20-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>

## <a name="to-prioritize-vendors"></a><span data-ttu-id="8cd20-107">Toimittajien priorisointi</span><span class="sxs-lookup"><span data-stu-id="8cd20-107">To prioritize vendors</span></span>
1. <span data-ttu-id="8cd20-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8cd20-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="8cd20-109">Valitse asianmukainen toimittaja ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="8cd20-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="8cd20-110">Syötä **Prioriteetti**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="8cd20-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="8cd20-111">in mukaan pienin numero (paitsi 0) tarkoittaa korkeinta prioriteettia.</span><span class="sxs-lookup"><span data-stu-id="8cd20-111"> considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="8cd20-112">Siten jos käytät esimerkiksi numeroita 1, 2 ja 3, numerolla 1 on korkein prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="8cd20-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="8cd20-113">Jos et halua priorisoida toimittajaa, jätä **Prioriteetti**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="8cd20-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="8cd20-114">Tämän jälkeen kun käytät maksuehdotusominaisuutta, tämä toimittaja tulee luetteloon kaikkien niiden toimittajien jälkeen, joilla on prioriteettinumero.</span><span class="sxs-lookup"><span data-stu-id="8cd20-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="8cd20-115">Prioriteettitasoja voi syöttää kuinka monta tahansa.</span><span class="sxs-lookup"><span data-stu-id="8cd20-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cd20-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8cd20-116">See Also</span></span>
[<span data-ttu-id="8cd20-117">Ostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8cd20-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="8cd20-118">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="8cd20-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="8cd20-119">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8cd20-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

