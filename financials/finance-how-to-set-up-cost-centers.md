---
title: "Kustannuspaikkojen määrittäminen | Microsoft Docs"
description: "Kustannuspaikat ovat osastoja, jotka ovat vastuussa kustannuksista ja tuloista. Kustannuspaikkakaavio vastaa pääkirjanpidon dimensiotietoja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 433526fbd2a13f32e64be94cc1936151445c19f5
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cost-centers"></a><span data-ttu-id="70c3e-104">Kustannuspaikkojen luominen</span><span class="sxs-lookup"><span data-stu-id="70c3e-104">How to: Set Up Cost Centers</span></span>
<span data-ttu-id="70c3e-105">Kustannuspaikat ovat osastoja, jotka vastaavat tuloista ja menoista.</span><span class="sxs-lookup"><span data-stu-id="70c3e-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="70c3e-106">Kustannuspaikkakaavio vastaa pääkirjanpidon dimensiotietoja.</span><span class="sxs-lookup"><span data-stu-id="70c3e-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="70c3e-107">Voit määrittää kustannuspaikkakaavion seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="70c3e-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="70c3e-108">Siirrä dimensioarvot pääkirjanpidosta kustannuspaikkakaavioon.</span><span class="sxs-lookup"><span data-stu-id="70c3e-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="70c3e-109">Siirron jälkeen voit tehdä tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="70c3e-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="70c3e-110">Luo uusi kustannuspaikan kaavio, joka on riippumaton pääkirjanpidosta, tai lisää uusi kustannuspaikka nykyiseen kustannuspaikan kaavioon.</span><span class="sxs-lookup"><span data-stu-id="70c3e-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="70c3e-111">Sinun on luotava kukin kustannuspaikka erikseen.</span><span class="sxs-lookup"><span data-stu-id="70c3e-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="70c3e-112">Siirrä dimensioarvot pääkirjanpidosta kustannuspaikkakaavioon</span><span class="sxs-lookup"><span data-stu-id="70c3e-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="70c3e-113">Määritä dimensio kustannuspaikan dimensioksi **Päivitä kustannuslaskennan dimensiot** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="70c3e-113">Set up a dimension to be the cost center dimension in the **Update Cost Acctg. Dimensions** window.</span></span> <span data-ttu-id="70c3e-114">Vain tämän dimension arvot siirretään.</span><span class="sxs-lookup"><span data-stu-id="70c3e-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="70c3e-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannuspaikkakartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="70c3e-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="70c3e-116">Valitse **Toiminnot**-välilehden **Funktiot**-ryhmässä **Nouda kustannuspaikat dimensiosta**, jolloin dimensioarvot siirretään kustannuspaikkakaavioon.</span><span class="sxs-lookup"><span data-stu-id="70c3e-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="70c3e-117">Toiminto siirtää kohdassa 1 määritetyt dimensioarvot.</span><span class="sxs-lookup"><span data-stu-id="70c3e-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="70c3e-118">Voit määrittää **Tasaa kustannuspaikan dimensio** -kentän määrittämään yksisuuntaisen dimensioarvojen synkronoinnin kirjanpidosta kustannuspaikkakaavioon.</span><span class="sxs-lookup"><span data-stu-id="70c3e-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="70c3e-119">Et voi määrittää kaavion kustannuspaikkojen synkronointia dimensioarvoihin pääkirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="70c3e-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="70c3e-120">Kustannuspaikkakaavio sisältää nyt kaikki pääkirjanpidossa määritetyt dimensioarvot, mukaan lukien otsikot ja välisummat.</span><span class="sxs-lookup"><span data-stu-id="70c3e-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a><span data-ttu-id="70c3e-121">Uuden kustannuspaikan luominen Kustannuspaikkakartta-ikkunassa</span><span class="sxs-lookup"><span data-stu-id="70c3e-121">To create new cost centers in the Chart of Cost Centers window</span></span>  
<span data-ttu-id="70c3e-122">Voit määrittää ja ylläpitää kustannuspaikkoja joko **Kustannuspaikan kortti** -kortissa tai **Kustannuspaikkakartta**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="70c3e-122">You can set up and maintain cost centers in either the **Cost Center Card** card or in the **Chart of Cost Centers** window.</span></span> <span data-ttu-id="70c3e-123">Tässä toimenpiteessä määrität kustannuspaikat **Kustannuspaikkakartta**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="70c3e-123">In this procedure, you set up cost centers in the **Chart of Cost Centers** window.</span></span>  

1. <span data-ttu-id="70c3e-124">Avaa **Kustannuspaikkakartta**-ikkuna muokkaustilassa.</span><span class="sxs-lookup"><span data-stu-id="70c3e-124">Open the **Chart of Cost Centers** window in edit mode.</span></span>  
2. <span data-ttu-id="70c3e-125">Syötä kustannuspaikkakoodi **Koodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="70c3e-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="70c3e-126">Kaikilla kustannuspaikoilla on oltava koodi.</span><span class="sxs-lookup"><span data-stu-id="70c3e-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="70c3e-127">Syötä kustannuspaikan nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="70c3e-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="70c3e-128">Määritä kustannuspaikan tarkoitus valitsemalla avattava nuoli **Rivityyppi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="70c3e-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="70c3e-129">**Summa**-tyyppisten kustannuspaikkojen osalta sinun täytyy täyttää **Summausväli**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="70c3e-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="70c3e-130">Määritä kustannuspaikkojen alueet **tai**-operaattorin avulla. Se on pystysuora viiva (**&#124;**).</span><span class="sxs-lookup"><span data-stu-id="70c3e-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="70c3e-131">Jos kustannuspaikan rivityyppi on **Loppusumma**, kenttä täytetään automaattisesti, kun käytössä on sisennystoiminto.</span><span class="sxs-lookup"><span data-stu-id="70c3e-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="70c3e-132">Täytä **Lajittelujärjestys** ja **Kustannuksen alityyppi** -kentät.</span><span class="sxs-lookup"><span data-stu-id="70c3e-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="70c3e-133">Napsauta seuraavaa tyhjää riviä uuden kustannuspaikan määrittämistä varten. Toista sitten vaiheet 2-5.</span><span class="sxs-lookup"><span data-stu-id="70c3e-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="70c3e-134">Kun olet määrittänyt kaikki kustannuspaikat, valitse **Sisennä kustannuspaikat** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="70c3e-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="70c3e-135">Valitse **Kyllä**-painike.</span><span class="sxs-lookup"><span data-stu-id="70c3e-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="70c3e-136">Jos olet antanut määritelmiä **Loppusumma**-kustannuspaikkojen **Summausväli**-kenttiin ennen sisennyksen suorittamista, määritelmät on annettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="70c3e-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="70c3e-137">Toiminto korvaa kaikki arvot **Loppusumma** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="70c3e-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="70c3e-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="70c3e-138">See Also</span></span>  
[<span data-ttu-id="70c3e-139">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="70c3e-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="70c3e-140">[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="70c3e-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="70c3e-141">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="70c3e-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="70c3e-142">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="70c3e-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="70c3e-143">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="70c3e-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

