---
title: "Hyllytysmallien määrittäminen | Microsoft Docs"
description: "Ohjatussa hyllytyksessä ja poiminnassa ohjelma etsii kunakin hetkenä sopivimman varastopaikan nimikkeille seuraavien tekijöiden mukaan: fyysisen varastoinnin määritetty hyllytysmalli, varastopaikoille annetut varastopaikan luokittelut ja kiinteille varastopaikoille määritetyt vähimmäis- ja enimmäismäärät."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0316dfe2d8e601077ed67317b4a077036e0a8c33
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="ddab2-103">Hyllytysmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ddab2-103">Set Up Put-away Templates</span></span>
<span data-ttu-id="ddab2-104">Ohjatussa hyllytyksessä ja poiminnassa ohjelma etsii kunakin hetkenä sopivimman varastopaikan nimikkeille seuraavien tekijöiden mukaan: fyysisen varastoinnin määritetty hyllytysmalli, varastopaikoille annetut varastopaikan luokittelut ja kiinteille varastopaikoille määritetyt vähimmäis- ja enimmäismäärät.</span><span class="sxs-lookup"><span data-stu-id="ddab2-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="ddab2-105">Voit määrittää useita hyllytysmalleja ja valita niistä yhden hallitaksesi hyllytyksiä yleisesti fyysisessä varastossa.</span><span class="sxs-lookup"><span data-stu-id="ddab2-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="ddab2-106">Voit valita hyllytysmallin myös mille tahansa nimikkeelle tai varastointiyksikölle, jolla voisi olla erityisiä hyllytysvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="ddab2-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="ddab2-107">Hyllytysmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ddab2-107">To set up put-away templates</span></span>  
1.  <span data-ttu-id="ddab2-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Hyllytysmallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ddab2-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ddab2-109">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ddab2-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="ddab2-110">Syötä koodi, joka on yksilöivä tunniste mallille, jota olet luomassa.</span><span class="sxs-lookup"><span data-stu-id="ddab2-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4.  <span data-ttu-id="ddab2-111">Syötä halutessasi lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ddab2-111">Enter a short description, if you wish.</span></span>  
5.  <span data-ttu-id="ddab2-112">Täytä ensimmäiselle riville varastopaikan vaatimukset, jotka haluat ohjelman ensin ja ennen kaikkea täyttävän silloin, kun se ehdottaa hyllytystä.</span><span class="sxs-lookup"><span data-stu-id="ddab2-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>  
6.  <span data-ttu-id="ddab2-113">Täytä toiselle riville varastopaikan vaatimukset, jotka olisivat seuraava valinta etsittäessä varastopaikkaa hyllytystä varten.</span><span class="sxs-lookup"><span data-stu-id="ddab2-113">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="ddab2-114">Toista riviä käytetään vain, jos varastopaikkaa, joka vastaisi ensimmäisen rivin vaatimuksia ei löydy.</span><span class="sxs-lookup"><span data-stu-id="ddab2-114">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7.  <span data-ttu-id="ddab2-115">Jatka rivien täyttämistä siihen saakka, kune olet kuvannut kaikki hyväksyttävät varastopaikkojen sijoitukset, joita haluat ohjelman käyttävän hyllytysprosessissa.</span><span class="sxs-lookup"><span data-stu-id="ddab2-115">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8.  <span data-ttu-id="ddab2-116">Valitse hyllytysmallin viimeisellä rivillä **Etsi määrittelemätön var.p.**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="ddab2-116">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="ddab2-117">Voit luoda useita hyllytysmalleja ja käyttää niitä yrityksesi tarpeisiin sopivalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ddab2-117">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="ddab2-118">Ohjelma viittaa ensin nimikkeelle tai varastointiyksikölle mahdollisesti valitsemaasi hyllytysmalliin.</span><span class="sxs-lookup"><span data-stu-id="ddab2-118">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="ddab2-119">Jos näitä kenttiä ei ole täytetty, käytetään sitä hyllytysmallia, jonka olet valinnut fyysiselle varastoinnille sijaintikortin **Var.paikkojen periaatteet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ddab2-119">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ddab2-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ddab2-120">See Also</span></span>  
[<span data-ttu-id="ddab2-121">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="ddab2-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ddab2-122">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="ddab2-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ddab2-123">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ddab2-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ddab2-124">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ddab2-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ddab2-125">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="ddab2-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ddab2-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ddab2-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

