---
title: KO-kunnossapidon määrittäminen| Microsoft Docs
description: Käyttöomaisuuden korjauksia ja huoltoa hallitaan yleensä määrittämällä kunnossapidon perustiedot, työn tyyppikoodit ja kustannusten kirjaustili.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b9077224f4a0b0344b565c55dcfb14db1e90722c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380150"
---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="c1519-103">Käyttöomaisuuden huollon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c1519-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="c1519-104">Kun haluat hallita käyttöomaisuuden kunnossapitoa, määritä ensin joitakin yleisiä kunnossapitotietoja, kunnossapitokustannusten kirjaustili ja työtyyppien, kuten rutiinihuollon tai korjauksen, kunnossapitokoodit.</span><span class="sxs-lookup"><span data-stu-id="c1519-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="c1519-105">Yleisten kunnossapitotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c1519-105">To set up general maintenance information</span></span>
<span data-ttu-id="c1519-106">Jos kunnossapidolle määritetään kentät, kunnossapitokuluja voi kirjata käyttöomaisuuden päiväkirjasta.</span><span class="sxs-lookup"><span data-stu-id="c1519-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="c1519-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c1519-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="c1519-108">Valitse käyttöomaisuus, jolle määrität vakuutuksen kattavuuden, ja valitse sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="c1519-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="c1519-109">Täytä **Kunnossapito**-pikavälilehdessä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="c1519-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="c1519-110">Kunnossapitokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c1519-110">To set up maintenance codes</span></span>
<span data-ttu-id="c1519-111">Kun kunnossapitokustannuksia kirjataan (yleisestä päiväkirjasta), **Kunnossapitokoodi**-kenttään tallennetaan suoritetun kunnossapidon tyyppi, kuten rutiinihuolto tai korjaus.</span><span class="sxs-lookup"><span data-stu-id="c1519-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="c1519-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ylläpito** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c1519-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="c1519-113">Määritä **Kunnossapito**-sivulla erityyppisten kunnossapitotöiden koodit.</span><span class="sxs-lookup"><span data-stu-id="c1519-113">On the **Maintenance** page, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="c1519-114">Kunnossapitokustannusten tilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c1519-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="c1519-115">Voit kirjata kunnossapitokustannuksia, kun annat ensin tilinumeron **KO-kirjausryhmät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="c1519-115">To post maintenance costs, you must first enter an account number on the **FA Posting Groups** page.</span></span>

1. <span data-ttu-id="c1519-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c1519-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="c1519-117">Täytä **Kunnossapitokustannusten tili** -kenttä kunkin kirjausryhmän osalta.</span><span class="sxs-lookup"><span data-stu-id="c1519-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c1519-118">Voit kohdistaa kunnossapitokustannukset osastoille ja/tai projekteille määrittämällä kohdistusavaimet.</span><span class="sxs-lookup"><span data-stu-id="c1519-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="c1519-119">Lisätietoja on kohdassa [Käyttöomaisuuden yleisten ominaisuuksien määrittäminen](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="c1519-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1519-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c1519-120">See Also</span></span>
[<span data-ttu-id="c1519-121">Käyttöomaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c1519-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="c1519-122">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="c1519-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="c1519-123">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="c1519-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="c1519-124">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="c1519-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="c1519-125">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c1519-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]