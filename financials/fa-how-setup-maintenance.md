---
title: "KO-kunnossapidon määrittäminen| Microsoft Docs"
description: "Käyttöomaisuuden korjauksia ja huoltoa hallitaan yleensä määrittämällä kunnossapidon perustiedot, työn tyyppikoodit ja kustannusten kirjaustili."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cdf1183fb5383311dc34d8c2c619a1eddf7e8851
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-fixed-asset-maintenance"></a><span data-ttu-id="845f8-103">Toimintaohje: Käyttöomaisuuden kunnossapidon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="845f8-103">How to: Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="845f8-104">Kun haluat hallita käyttöomaisuuden kunnossapitoa, määritä ensin joitakin yleisiä kunnossapitotietoja, kunnossapitokustannusten kirjaustili ja työtyyppien, kuten rutiinihuollon tai korjauksen, kunnossapitokoodit.</span><span class="sxs-lookup"><span data-stu-id="845f8-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="845f8-105">Yleisten kunnossapitotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="845f8-105">To set up general maintenance information</span></span>
<span data-ttu-id="845f8-106">Jos kunnossapidolle määritetään kentät, kunnossapitokuluja voi kirjata käyttöomaisuuden päiväkirjasta.</span><span class="sxs-lookup"><span data-stu-id="845f8-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="845f8-107">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Käyttöomaisuus** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="845f8-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="845f8-108">Valitse käyttöomaisuus, jolle määrität vakuutuksen kattavuuden, ja valitse sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="845f8-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="845f8-109">Täytä **Kunnossapito**-pikavälilehdessä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="845f8-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="845f8-110">Kunnossapitokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="845f8-110">To set up maintenance codes</span></span>
<span data-ttu-id="845f8-111">Kun kunnossapitokustannuksia kirjataan (yleisestä päiväkirjasta), **Kunnossapitokoodi**-kenttään tallennetaan suoritetun kunnossapidon tyyppi, kuten rutiinihuolto tai korjaus.</span><span class="sxs-lookup"><span data-stu-id="845f8-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="845f8-112">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Kunnossapito** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="845f8-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="845f8-113">Määritä **Kunnossapito**-ikkunassa erityyppisten kunnossapitotöiden koodit.</span><span class="sxs-lookup"><span data-stu-id="845f8-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="845f8-114">Kunnossapitokustannusten tilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="845f8-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="845f8-115">Voit kirjata kunnossapitokustannuksia, kun syötät ensin tilinumeron **KO-kirjausryhmät**-ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="845f8-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="845f8-116">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="845f8-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="845f8-117">Täytä **Kunnossapitokustannusten tili** -kenttä kunkin kirjausryhmän osalta.</span><span class="sxs-lookup"><span data-stu-id="845f8-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="845f8-118">Voit kohdistaa kunnossapitokustannukset osastoille ja/tai projekteille määrittämällä kohdistusavaimet.</span><span class="sxs-lookup"><span data-stu-id="845f8-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="845f8-119">Lisätietoja on kohdassa [Toimintaohje: Käyttöomaisuuden yleisten toimintojen määrittäminen](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="845f8-119">For more information, see [How to: Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="845f8-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="845f8-120">See Also</span></span>
[<span data-ttu-id="845f8-121">Käyttöomaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="845f8-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="845f8-122">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="845f8-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="845f8-123">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="845f8-123">Finance</span></span>](finance.md)  
<span data-ttu-id="845f8-124">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="845f8-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="845f8-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="845f8-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

