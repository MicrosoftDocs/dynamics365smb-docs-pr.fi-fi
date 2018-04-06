---
title: Varastotoimintorivien jakaminen | Microsoft Docs
description: "Fyysisen varastoinnin hyllytyksissä, siirroissa ja poiminnoissa sekä varaston hyllytyksissä ja poiminnoissa ohjelma ehdottaa varastopaikkoja nimikkeiden poimintaa tai hyllytystä varten. Joskus voi käydä niin, että ohjelman ehdottamassa varastopaikassa oleva määrä ei ole riittävä tai että ehdotetussa varastopaikassa ei ole tarpeeksi tilaa hyllytettävälle määrälle. Tällöin rivi on jaettava, jotta yhden rivin nimikkeet voidaan siirtää useisiin varastopaikkoihin tai hakea useista varastopaikoista."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dfb633ef874b77a3cf6060311f0bcbbf66e05102
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="split-warehouse-activity-lines"></a><span data-ttu-id="c29be-105">Varastotoimintorivien jakaminen</span><span class="sxs-lookup"><span data-stu-id="c29be-105">Split Warehouse Activity Lines</span></span>
<span data-ttu-id="c29be-106">Fyysisen varastoinnin hyllytyksissä, siirroissa ja poiminnoissa sekä varaston hyllytyksissä ja poiminnoissa ohjelma ehdottaa varastopaikkoja nimikkeiden poimintaa tai hyllytystä varten.</span><span class="sxs-lookup"><span data-stu-id="c29be-106">In warehouse put-aways, movements, or picks, and in inventory put-aways and inventory picks, bins are suggested for the picking or putting away of items.</span></span> <span data-ttu-id="c29be-107">Joskus voi käydä niin, että ohjelman ehdottamassa varastopaikassa oleva määrä ei ole riittävä tai että ehdotetussa varastopaikassa ei ole tarpeeksi tilaa hyllytettävälle määrälle.</span><span class="sxs-lookup"><span data-stu-id="c29be-107">The actual quantity in the bin suggested may not be sufficient, or there is not enough room in the suggested bin to put away the required quantity.</span></span> <span data-ttu-id="c29be-108">Tällöin rivi on jaettava, jotta yhden rivin nimikkeet voidaan siirtää useisiin varastopaikkoihin tai hakea useista varastopaikoista.</span><span class="sxs-lookup"><span data-stu-id="c29be-108">In these cases, you need to split the line, so that the items for one line are either taken from or placed into more than one bin.</span></span>  

<span data-ttu-id="c29be-109">Seuraavat toimet koskevat kaikkia fyysisen varaston asiakirjoja, kuten fyysisen varaston hyllytys-, siirto-, ja poimintarivejä tai varaston hyllytys, siirto-, ja poimintarivejä.</span><span class="sxs-lookup"><span data-stu-id="c29be-109">The following procedure applies to warehouse documents, such as warehouse put-away, movement, and pick lines, or inventory put-away, movement, and pick lines.</span></span>  

## <a name="to-split-warehouse-activity-lines"></a><span data-ttu-id="c29be-110">Jaa fyysisen varaston aktiviteettirivit</span><span class="sxs-lookup"><span data-stu-id="c29be-110">To split warehouse activity lines</span></span>  
1.  <span data-ttu-id="c29be-111">Avaa fyysisen varastoinnin toimintorivi, jolla yrität käsitellä riittämätöntä määrää.</span><span class="sxs-lookup"><span data-stu-id="c29be-111">Open a warehouse activity line where you are trying to handle an insufficient quantity.</span></span>  
2.  <span data-ttu-id="c29be-112">Anna **Käsiteltävä määrä** -kentässä vähennetty määrä, jonka voit käsitellä.</span><span class="sxs-lookup"><span data-stu-id="c29be-112">In the **Qty. to Handle** field, enter the reduced quantity that you are able to handle.</span></span>  
3.  <span data-ttu-id="c29be-113">Valitse **Rivit**-pikavälilehdessä ensin **Toiminnot**-, sitten **Toiminnot**- ja lopuksi **Jaa rivi** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c29be-113">On the **Lines** FastTab, choose the **Actions** action, choose the **Functions** action, and then choose the **Split Line** action.</span></span> <span data-ttu-id="c29be-114">Näyttöön tulee uusi rivi, joka on muuten identtinen kopio alkuperäisestä rivistä, mutta sen **Käsiteltävä määrä** -kentässä on alkuperäiseltä riviltä poistamasi määrä.</span><span class="sxs-lookup"><span data-stu-id="c29be-114">A new line appears, which is a copy of the original line, except that the **Qty. to Handle** field contains the quantity that you removed from the original line.</span></span>  
4.  <span data-ttu-id="c29be-115">Määritä tälle uudelle riville asianmukainen varastopaikka (ja alue, jos käytössä on ohjattu hyllytys ja poiminta) tai jatka tarvittaessa rivin jakamista siihen asti, kunnes löydät sopivat varastopaikat koko määrälle.</span><span class="sxs-lookup"><span data-stu-id="c29be-115">Assign an appropriate bin and, if you are using directed put-away and pick, a zone, to this new line, or continue splitting the line as necessary until you find appropriate bins for all of the quantity.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c29be-116">Jos jaat rivit, kun sijainnissa on käytössä ohjattu hyllytys ja poiminta, sinun täytyy tuntea fyysinen varasto hyvin ja pystyä valitsemaan varastopaikka, joka vastaa nimikkeen varastointitarpeita ja joka täyttää fyysisen varastoinnin asiakirjan yleiset vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="c29be-116">If the location uses directed put-away and pick and you split the lines, you must be familiar with the warehouse and be able to choose a bin that matches the storage requirements of the item and that fulfills the general requirements of the warehouse document.</span></span> <span data-ttu-id="c29be-117">Et esimerkiksi voi jakaa poiminta-asiakirjan riviä ja sijoittaa joitakin nimikkeitä irtotavaroiden varastoon.</span><span class="sxs-lookup"><span data-stu-id="c29be-117">For example, you would not split a line on a pick document and place some items in the bulk storage.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c29be-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c29be-118">See Also</span></span>  
[<span data-ttu-id="c29be-119">Varastoinninhallinta</span><span class="sxs-lookup"><span data-stu-id="c29be-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="c29be-120">Vaihto-omaisuus</span><span class="sxs-lookup"><span data-stu-id="c29be-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c29be-121">[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="c29be-121">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="c29be-122">[Kokoonpanon hallinta](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="c29be-122">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="c29be-123">Rakennetiedot: Fyysisen varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="c29be-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c29be-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c29be-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

