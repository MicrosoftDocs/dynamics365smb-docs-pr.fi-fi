---
title: Tuotantotilausten luominen myyntitilauksista
description: Tuotantotilauksia voi luoda myyntitilauksista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115234"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="1b304-103">Tuotantotilausten luominen myyntitilauksista</span><span class="sxs-lookup"><span data-stu-id="1b304-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="1b304-104">Voit luoda tuotettujen nimikkeiden tuotantotilaukset suodaan myyntitilauksista.</span><span class="sxs-lookup"><span data-stu-id="1b304-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="1b304-105">Tuotantotilausten luominen myyntitilauksista</span><span class="sxs-lookup"><span data-stu-id="1b304-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="1b304-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1b304-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1b304-107">Valitse myyntitilaus, jolle haluat luoda tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="1b304-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="1b304-108">Valitse **Suunnittelu**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="1b304-108">Choose the **Planning** action.</span></span> <span data-ttu-id="1b304-109">**Myyntitilaus suunnittelu** -sivulla voi tarkastella myyntitilausnimikkeen saatavuutta.</span><span class="sxs-lookup"><span data-stu-id="1b304-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="1b304-110">Valitse **Luo tuotantotilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1b304-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="1b304-111">Valitse tila ja tilaustyyppi.</span><span class="sxs-lookup"><span data-stu-id="1b304-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="1b304-112">Valitse **Kyllä** -painike luodaksesi yhden tai useamman tuotantotilauksen niiden rivien osalta, joilla on **Tuotantotilaus** **Täydennysjärjestelmä**-kentässään.</span><span class="sxs-lookup"><span data-stu-id="1b304-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="1b304-113">Luodun tuotantotilauksen kysyntärivit, joilla on **Tuotantotilaus** niiden **Täydennysjärjestelmä** -kentässä, edustavat perustana olevia tuotantotilauksia..</span><span class="sxs-lookup"><span data-stu-id="1b304-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="1b304-114">Kun olet luonut nämä tuotantotilaukset, muista tunnistaa kaikki niihin kohdistuvat täyttämättömät komponenttivaatimukset käyttämällä **Tilauksen suunnittelu** -sivua tai **Uudelleensuunnittele**-toimintoa luoduista tilauksista.</span><span class="sxs-lookup"><span data-stu-id="1b304-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="1b304-115">Tilaustyyppi</span><span class="sxs-lookup"><span data-stu-id="1b304-115">Order type</span></span>  
<span data-ttu-id="1b304-116">Voit valita kahdesta eri tavasta luoda tuotantotilaukset seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="1b304-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="1b304-117">Asetus</span><span class="sxs-lookup"><span data-stu-id="1b304-117">Option</span></span>|<span data-ttu-id="1b304-118">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="1b304-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="1b304-119">Nimiketilaus</span><span class="sxs-lookup"><span data-stu-id="1b304-119">Item Order</span></span>|<span data-ttu-id="1b304-120">Yksi tuotantotilaus luodaan kutakin tarvittavaa tuotantotilausta varten. Sitä edustaa rivi **Myyntitilauksen suunnittelu** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="1b304-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="1b304-121">Projektitilaus</span><span class="sxs-lookup"><span data-stu-id="1b304-121">Project Order</span></span>|<span data-ttu-id="1b304-122">Yksi tuotantotilaus luodaan kaikkia tarvittavia tuotantotilauksia varten. Niitä edustavat rivit **Myyntitilauksen suunnittelu** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="1b304-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="1b304-123">Kun käytät projektitilauksia, tuotantotilauksen **Lähdetyyppi**-kentässä on **Myynnin tunnistetiedot** ja tilauksessa on useita rivejä, yksi jokaista tuotettavaa myyntirivinimikettä kohden.</span><span class="sxs-lookup"><span data-stu-id="1b304-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="1b304-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1b304-124">See Also</span></span>  
[<span data-ttu-id="1b304-125">Tuotannon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1b304-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="1b304-126">[Tuotanto](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="1b304-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="1b304-127">Varasto</span><span class="sxs-lookup"><span data-stu-id="1b304-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1b304-128">Osto</span><span class="sxs-lookup"><span data-stu-id="1b304-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1b304-129">[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="1b304-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="1b304-130">Asetukset - parhaat käytännöt: toimitusten suunnittelu</span><span class="sxs-lookup"><span data-stu-id="1b304-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="1b304-131">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b304-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
