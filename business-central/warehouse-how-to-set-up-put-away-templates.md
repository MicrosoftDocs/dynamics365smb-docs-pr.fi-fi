---
title: Hyllytysmallien määrittäminen | Microsoft Docs
description: 'Ohjatussa hyllytyksessä ja poiminnassa ohjelma etsii kunakin hetkenä sopivimman varastopaikan nimikkeille seuraavien tekijöiden mukaan: fyysisen varastoinnin määritetty hyllytysmalli, varastopaikoille annetut varastopaikan luokittelut ja kiinteille varastopaikoille määritetyt vähimmäis- ja enimmäismäärät.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b2f31804dace5371da17a4c6e1eeaaac24815c6f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755917"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="eb588-103">Hyllytysmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb588-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="eb588-104">Ohjatussa hyllytyksessä ja poiminnassa ohjelma etsii kunakin hetkenä sopivimman varastopaikan nimikkeille seuraavien tekijöiden mukaan: fyysisen varastoinnin määritetty hyllytysmalli, varastopaikoille annetut varastopaikan luokittelut ja kiinteille varastopaikoille määritetyt vähimmäis- ja enimmäismäärät.</span><span class="sxs-lookup"><span data-stu-id="eb588-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="eb588-105">Voit määrittää useita hyllytysmalleja ja valita niistä yhden hallitaksesi hyllytyksiä yleisesti fyysisessä varastossa.</span><span class="sxs-lookup"><span data-stu-id="eb588-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="eb588-106">Voit valita hyllytysmallin myös mille tahansa nimikkeelle tai varastointiyksikölle, jolla voisi olla erityisiä hyllytysvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="eb588-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="eb588-107">Hyllytysmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb588-107">To set up put-away templates</span></span>

1. <span data-ttu-id="eb588-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Hyllytysmallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="eb588-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eb588-109">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="eb588-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="eb588-110">Syötä koodi, joka on yksilöivä tunniste mallille, jota olet luomassa.</span><span class="sxs-lookup"><span data-stu-id="eb588-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="eb588-111">Syötä halutessasi lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="eb588-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="eb588-112">Täytä ensimmäiselle riville varastopaikan vaatimukset, jotka haluat ohjelman ensin ja ennen kaikkea täyttävän silloin, kun se ehdottaa hyllytystä.</span><span class="sxs-lookup"><span data-stu-id="eb588-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="eb588-113">Jos esimerkiksi haluat oletushyllytystavan perustuvan kiinteisiin varastopaikkoihin, valitse **Etsi kiinteä varastopaikka** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="eb588-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="eb588-114">Täytä toiselle riville varastopaikan vaatimukset, jotka olisivat seuraava valinta etsittäessä varastopaikkaa hyllytystä varten.</span><span class="sxs-lookup"><span data-stu-id="eb588-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="eb588-115">Toista riviä käytetään vain, jos varastopaikkaa, joka vastaisi ensimmäisen rivin vaatimuksia ei löydy.</span><span class="sxs-lookup"><span data-stu-id="eb588-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="eb588-116">Jatka rivien täyttämistä siihen saakka, kune olet kuvannut kaikki hyväksyttävät varastopaikkojen sijoitukset, joita haluat ohjelman käyttävän hyllytysprosessissa.</span><span class="sxs-lookup"><span data-stu-id="eb588-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="eb588-117">Valitse hyllytysmallin viimeisellä rivillä **Etsi määrittelemätön var.p.**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="eb588-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="eb588-118">Voit luoda useita hyllytysmalleja ja käyttää niitä yrityksesi tarpeisiin sopivalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="eb588-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="eb588-119">Ohjelma viittaa ensin nimikkeelle tai varastointiyksikölle mahdollisesti valitsemaasi hyllytysmalliin.</span><span class="sxs-lookup"><span data-stu-id="eb588-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="eb588-120">Jos näitä kenttiä ei ole täytetty, käytetään sitä hyllytysmallia, jonka olet valinnut fyysiselle varastoinnille sijaintikortin **Var.paikkojen periaatteet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="eb588-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eb588-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="eb588-121">See Also</span></span>

[<span data-ttu-id="eb588-122">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="eb588-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="eb588-123">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="eb588-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="eb588-124">Varastoinninhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb588-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="eb588-125">Kokoonpanon hallinta</span><span class="sxs-lookup"><span data-stu-id="eb588-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="eb588-126">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="eb588-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="eb588-127">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eb588-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
