---
title: Varastotyöntekijöiden määrittäminen | Microsoft Docs
description: Jokainen varastotoimintoja tekevä käyttäjä on määritettävä varastotyöntekijäksi ja liitettävä yhteen oletussijaintiin ja mahdollisesti muihin sijainteihin, jotka eivät ole oletussijainteja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ebb81abd7e16e0c4aaa3f7cd52ab1b6f1a664c3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755920"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="61153-103">Varastotyöntekijöiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="61153-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="61153-104">Jokainen varastotoimintoja tekevä käyttäjä on määritettävä varastotyöntekijäksi ja liitettävä yhteen oletussijaintiin ja mahdollisesti muihin sijainteihin, jotka eivät ole oletussijainteja.</span><span class="sxs-lookup"><span data-stu-id="61153-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="61153-105">Nämä käyttäjäasetukset suodattavat kaikki tietokannan varastotoiminnot työntekijän sijainnissa niin, että työntekijä voi suorittaa varastotoimintoja vain oletussijainnissa.</span><span class="sxs-lookup"><span data-stu-id="61153-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="61153-106">Käyttäjä voidaan liittää myös muihin kuin oletussijanteihin, joissa käyttäjä voi katsella toimintorivejä mutta ei suorittaa toimintoja.</span><span class="sxs-lookup"><span data-stu-id="61153-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="61153-107">Varastotyöntekijöiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="61153-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="61153-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastotyöntekijät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="61153-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="61153-109">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="61153-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="61153-110">Valitse **Käyttäjätunnus**-kenttä ja valitse sitten käyttäjä, joka lisätään varaston työntekijäksi.</span><span class="sxs-lookup"><span data-stu-id="61153-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="61153-111">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="61153-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="61153-112">Syötä **Sijaintikoodi**-kenttään käyttäjän työskentelypaikan sijainnin koodi.</span><span class="sxs-lookup"><span data-stu-id="61153-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="61153-113">Valitse **Oletusarvo**-valintaruutu, kun haluat määrittää tämän sijainnin ainoaksi sijainniksi, jossa käyttäjä voi tehdä varastotoimintoja.</span><span class="sxs-lookup"><span data-stu-id="61153-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="61153-114">Liitä sijainteihin muita työntekijöitä tai liitä aiemmin luoduille varastotyöntekijöille muita kuin oletussijainteja toistamalla nämä vaiheet.</span><span class="sxs-lookup"><span data-stu-id="61153-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="61153-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="61153-115">See Also</span></span>  
[<span data-ttu-id="61153-116">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="61153-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="61153-117">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="61153-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="61153-118">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="61153-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="61153-119">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="61153-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="61153-120">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="61153-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="61153-121">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61153-121">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
