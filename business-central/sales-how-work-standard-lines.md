---
title: "Toistuvien myyntien ja ostojen vakiorivien määrittäminen | Microsoft Docs"
description: "Voit määrittää usein käytettäviä myynti- ja ostorivejä. Voit sitten lisätä ne myynti- ja ostoasiakirjoihin ja täyttää tällä tavoin vakiotiedot nopeasti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d3ce7b8065837d98b55b6e2dd1644f79b34e534a
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="f2a58-103">Toistuvien myynti- ja ostorivien luominen</span><span class="sxs-lookup"><span data-stu-id="f2a58-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="f2a58-104">Jos sinun on usein luotava samankaltaisia tietoja sisältäviä myynti- ja ostorivejä, voit määrittää vakiorivejä ja lisätä ne sitten toistuviin myynti- ja ostoasiakirjoihin, kuten toistuviin täydennystilauksiin.</span><span class="sxs-lookup"><span data-stu-id="f2a58-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="f2a58-105">Seuraavassa menettelyssä käsitellään vakiomyyntirivien käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="f2a58-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="f2a58-106">Niitä käytetään samalla tavoin kuin vakio-ostorivejä.</span><span class="sxs-lookup"><span data-stu-id="f2a58-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="f2a58-107">Vakiomyyntirivien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f2a58-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="f2a58-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Vakiomyyntikoodit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f2a58-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f2a58-109">Valitse **Vakiomyyntirivit** -ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2a58-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="f2a58-110">Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f2a58-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="f2a58-111">Kirjoita **Rivit**-pikavälilehden kenttiin esitiedot, jotka sopivat toistuvina riveinä myyntiasiakirjoissa käytettäviksi vakioriveiksi.</span><span class="sxs-lookup"><span data-stu-id="f2a58-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="f2a58-112">Vakiomyyntirivien lisääminen myyntilaskuun</span><span class="sxs-lookup"><span data-stu-id="f2a58-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="f2a58-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Vakiomyyntikoodit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f2a58-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="f2a58-114">Avaa myyntilasku, johon haluat lisätä vähintään yhden vakiomyyntirivin.</span><span class="sxs-lookup"><span data-stu-id="f2a58-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="f2a58-115">Valitse **Nouda toistuvat myyntirivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2a58-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="f2a58-116">Valitse **Toistuvat myyntirivit** -ikkunan **Koodi**-kentässä hakupainike ja valitse sitten vakiomyyntirivijoukko.</span><span class="sxs-lookup"><span data-stu-id="f2a58-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="f2a58-117">Lisää vakiomyyntirivit laskuun valitsemalla **OK**. Voit sitten käyttää näitä rivejä sellaisenaan tai muokata rivien tietoja.</span><span class="sxs-lookup"><span data-stu-id="f2a58-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="f2a58-118">Useiden myyntilaskujen luonti vakiomyyntirivien perusteella</span><span class="sxs-lookup"><span data-stu-id="f2a58-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="f2a58-119">Voit luoda **Luo toistuvia myyntilaskuja** -eräajolla myyntilaskuja asiakkaille määritettyjen vakiomyyntirivien mukaan siten, että niiden kirjauspäivämäärät ovat vakiomyyntikoodissa määritetyllä voimassaolon päivämäärävälillä.</span><span class="sxs-lookup"><span data-stu-id="f2a58-119">You can use the **Create Recurring Sales Inv.** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="f2a58-120">Voit määrittää **Toistuvat myyntirivit** -ikkunassa myös suoraveloitusmaksutavan ja suoraveloitusvaltakirjan.</span><span class="sxs-lookup"><span data-stu-id="f2a58-120">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="f2a58-121">Laskut, jotka luodaan **Luo toistuvia myyntilaskuja** -eräajolla, sisältävät tietoja, jotka vaaditaan maksun perimiseen SEPA-suoraveloituksen sisältävistä myyntilaskuista.</span><span class="sxs-lookup"><span data-stu-id="f2a58-121">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="f2a58-122">Lisätietoja on kohdassa [SEPA-suoraveloitusmaksujen periminen](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="f2a58-122">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="f2a58-123">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoitta **Luo toistuvia myyntilaskuja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f2a58-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="f2a58-124">Täytä **Luo toistuvia myyntilaskuja** -ikkunassa tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f2a58-124">In the **Create Recurring Sales Inv.** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="f2a58-125">Anna **Koodi**-kentässä sille asiakkaalle määritetty vakiomyyntirivien koodi, jolle haluat luoda myyntilaskuja.</span><span class="sxs-lookup"><span data-stu-id="f2a58-125">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="f2a58-126">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="f2a58-126">Choose the **OK** button.</span></span>

<span data-ttu-id="f2a58-127">Myyntilaskut luodaan asiakkaille, joilla on määrätty asiakkaan vakiomyyntikoodi ja jotkut määritetyt suoraveloitustiedot kirjaamista varten määrättynä päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="f2a58-127">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2a58-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f2a58-128">See Also</span></span>  
[<span data-ttu-id="f2a58-129">Myynti</span><span class="sxs-lookup"><span data-stu-id="f2a58-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="f2a58-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f2a58-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

