---
title: Tietoja valmiin tuotantotilauksen kustannuksista | Microsoft Docs
description: Tuotantotilauksen valmistuminen on erittäin tärkeää tuotettavan nimikkeen kustannuselinkaaren päättämisen kannalta. Lopulliset kustannukset (tavallisen kustannusympäristön vaihtelut, FIFO-menetelmän lopputuotteet, keskiarvo tai LIFO-kustannusympäristö) lasketaan Muuta kustannuksia - Nimiketapahtumat -eräajolla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96cf025bbac137f61f41a65cbd2f9520f2c5e787
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "925351"
---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="6537b-104">Tietoja valmiin tuotantotilauksen kustannuksista</span><span class="sxs-lookup"><span data-stu-id="6537b-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="6537b-105">Tuotantotilauksen valmistuminen on erittäin tärkeää tuotettavan nimikkeen kustannuselinkaaren päättämisen kannalta.</span><span class="sxs-lookup"><span data-stu-id="6537b-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="6537b-106">Lopulliset kustannukset (tavallisen kustannusympäristön vaihtelut; FIFO-menetelmän lopputuotteet, keskiarvo tai LIFO-kustannusympäristö) lasketaan **Muuta kustannuksia - Nimiketapahtumat** -eräajolla, joka mahdollistaa nimikkeen tuotantokustannusten täsmäyttämisen.</span><span class="sxs-lookup"><span data-stu-id="6537b-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="6537b-107">Vain sellaisten nimikkeiden kustannuksia voi muuttaa, joiden tila on **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="6537b-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="6537b-108">Sen vuoksi on ehdottoman tärkeää, että valmistuneen tuotantotilauksen tilaksi vaihdetaan **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="6537b-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="6537b-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="6537b-109">Example</span></span>  
 <span data-ttu-id="6537b-110">Kun materiaalia kulutetaan tavallisessa kustannusympäristössä nimikkeen tuottamiseksi, nimikkeen kustannukset sekä työn kustannukset ja yleiskustannukset kirjataan KET-tilille.</span><span class="sxs-lookup"><span data-stu-id="6537b-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="6537b-111">Kun nimike on tuotettu, standardikustannusten summa vähennetään KET:istä.</span><span class="sxs-lookup"><span data-stu-id="6537b-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="6537b-112">Yleensä näiden kustannusten tulos ei ole nolla.</span><span class="sxs-lookup"><span data-stu-id="6537b-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="6537b-113">Jotta näiden kustannusten tulokseksi saadaan nolla, **Muuta kustannuksia - Nimiketapahtumat** -eräajo on suoritettava ja huomioitava, että vain **Valmis**-tilassa olevat tuotantotilaukset otetaan huomioon muutoksessa.</span><span class="sxs-lookup"><span data-stu-id="6537b-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6537b-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6537b-114">See Also</span></span>  
[<span data-ttu-id="6537b-115">Varaston kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="6537b-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="6537b-116">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="6537b-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="6537b-117">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6537b-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
