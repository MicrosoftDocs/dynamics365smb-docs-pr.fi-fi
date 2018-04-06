---
title: "Kustannuskohteiden määrittäminen | Microsoft Docs"
description: "Lisätietoja yleisen päiväkirjan dimensioita muistuttavien kustannuskohteiden määrittämisestä"
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f371a772f710576a70bac4808b15be091a61d66
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cost-objects"></a><span data-ttu-id="13185-103">Kustannuskohteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="13185-103">Set Up Cost Objects</span></span>
<span data-ttu-id="13185-104">Kustannuskohteet ovat yrityksen projekteja, tuotteita tai palveluja.</span><span class="sxs-lookup"><span data-stu-id="13185-104">Cost objects are projects, products, or services of a company.</span></span> <span data-ttu-id="13185-105">Kustannuskohdekaavio vastaa pääkirjanpidon dimensiotietoja.</span><span class="sxs-lookup"><span data-stu-id="13185-105">The chart of cost objects is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="13185-106">Voit määrittää kustannuskohdekaavion seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="13185-106">You can set up the chart of cost objects in the following ways:</span></span>  

* <span data-ttu-id="13185-107">Siirrä dimensioarvot pääkirjanpidosta kustannuskohdekaavioon.</span><span class="sxs-lookup"><span data-stu-id="13185-107">Transfer dimension values in the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="13185-108">Siirron jälkeen voit tehdä tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="13185-108">You can make any necessary adjustments after the transfer.</span></span>  
* <span data-ttu-id="13185-109">Luo uusi kustannuskohteen kaavio, joka on riippumaton pääkirjanpidosta, tai lisää uusi kustannuskohde nykyiseen kustannuskohteiden kaavioon.</span><span class="sxs-lookup"><span data-stu-id="13185-109">Create a new chart of cost object that is independent of the general ledger or add a new cost object to an existing chart of cost objects.</span></span> <span data-ttu-id="13185-110">Sinun on luotava kukin kustannuskohde erikseen.</span><span class="sxs-lookup"><span data-stu-id="13185-110">You must create each cost object individually.</span></span>  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a><span data-ttu-id="13185-111">Siirrä dimensioarvot pääkirjanpidosta kustannuskohdekaavioon</span><span class="sxs-lookup"><span data-stu-id="13185-111">To transfer dimension values from the general ledger to the chart of cost objects</span></span>  
1.  <span data-ttu-id="13185-112">Määritä dimensio kustannuskohteen dimensioksi **Päivitä KL-dimensiot** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="13185-112">Set a dimension to be the cost object dimension in the **Update CA Dimensions** window.</span></span> <span data-ttu-id="13185-113">Vain tämän dimension arvot siirretään.</span><span class="sxs-lookup"><span data-stu-id="13185-113">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="13185-114">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannuskohdekartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="13185-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Objects**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="13185-115">Valitse **Nouda kustannuskohteet dimensiosta** -toiminto, jolla dimensioarvot siirretään kustannuskohdekaavioon.</span><span class="sxs-lookup"><span data-stu-id="13185-115">Choose the **Get Cost Objects from Dimension** action to transfer dimension values to the chart of cost objects.</span></span> <span data-ttu-id="13185-116">Toiminto siirtää kohdassa 1 määritetyt dimensioarvot.</span><span class="sxs-lookup"><span data-stu-id="13185-116">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="13185-117">Voit määrittää **Tasaa kustannuskohteen dimensio** -kentän määrittämään yksisuuntaisen dimensioarvojen synkronoinnin kirjanpidosta kustannuskohdekarttaan.</span><span class="sxs-lookup"><span data-stu-id="13185-117">You can set up the **Align Cost Object Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="13185-118">Et voi määrittää kaavion kustannuskohteiden synkronointia dimensioarvoihin pääkirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="13185-118">You cannot define a synchronization of the chart of cost objects to dimension values from the general ledger.</span></span>  

<span data-ttu-id="13185-119">Kustannuskohdekaavio sisältää nyt kaikki pääkirjanpidossa määritetyt dimensioarvot, mukaan lukien otsikot ja välisummat.</span><span class="sxs-lookup"><span data-stu-id="13185-119">The chart of cost objects now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-window"></a><span data-ttu-id="13185-120">Uuden kustannuskohteen luominen Kustannuskohdekartta-ikkunassa</span><span class="sxs-lookup"><span data-stu-id="13185-120">To create new cost objects in the Chart of Cost Objects window</span></span>  
<span data-ttu-id="13185-121">Voit määrittää ja ylläpitää kustannuskohteita joko **Kustannuskohteen kortti** -kortissa tai **Kustannuskohdekartta**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="13185-121">You can set up and maintain cost objects in either the **Cost Object Card** card or in the **Chart of Cost Objects** window.</span></span> <span data-ttu-id="13185-122">Tässä toimenpiteessä määrität kustannuskohteet **Kustannuskohdekartta**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="13185-122">In this procedure, you set up cost objects in the **Chart of Cost Objects** window.</span></span>  

1.  <span data-ttu-id="13185-123">Avaa **Kustannuskohdekartta**-ikkuna muokkaustilassa.</span><span class="sxs-lookup"><span data-stu-id="13185-123">Open the **Chart of Cost Objects** window in edit mode.</span></span>  
2.  <span data-ttu-id="13185-124">Syötä kustannuskohdekoodi **Koodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13185-124">In the **Code** field, enter the cost object code.</span></span> <span data-ttu-id="13185-125">Kaikilla kustannuskohteilla on oltava koodi.</span><span class="sxs-lookup"><span data-stu-id="13185-125">All cost objects must have a code.</span></span>  
3.  <span data-ttu-id="13185-126">Syötä kustannuskohteen nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13185-126">In the **Name** field, enter the cost object name.</span></span>  
4.  <span data-ttu-id="13185-127">Valitse avattava nuoli **Rivityyppi**-kentässä määrittämään kustannuskohteen tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="13185-127">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost object.</span></span>  

    * <span data-ttu-id="13185-128">Jos kustannuskohteiden rivityyppi on **Yhteensä**, anna arvo **Summan lähde/kohde** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="13185-128">For cost objects of the **Total** line type, fill in the **Total From/To** field.</span></span> <span data-ttu-id="13185-129">Käytä **tai**-operaattoria, joka on pystysuora viiva (**&#124;**) kustannuskohteiden alueiden määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="13185-129">Use the **or** operator, which is a vertical line (**&#124;**), to set ranges of cost objects.</span></span>  
    * <span data-ttu-id="13185-130">Jos kustannuskohteiden rivityyppi on **Loppusumma**, kenttä täytetään automaattisesti, kun käytössä on sisennystoiminto.</span><span class="sxs-lookup"><span data-stu-id="13185-130">For cost objects of the **End-Total** line type, this field is filled in automatically when you use  the indent function.</span></span>  
5.  <span data-ttu-id="13185-131">Täytä **Lajittelujärjestys**-kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="13185-131">Fill in the **Sorting Order** field.</span></span>  
6.  <span data-ttu-id="13185-132">Napsauta seuraavaa tyhjää riviä uuden kustannuskohteen määrittämistä varten. Toista sitten vaiheet 2-5.</span><span class="sxs-lookup"><span data-stu-id="13185-132">Chose the next empty line to create a new cost object, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="13185-133">Kun olet määrittänyt kaikki kustannuskohteet, valitse **Sisennä kustannuskohteet** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="13185-133">After you have set up all the cost objects, choose the **Indent Cost Objects** action.</span></span> <span data-ttu-id="13185-134">Valitse **Kyllä**-painike.</span><span class="sxs-lookup"><span data-stu-id="13185-134">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="13185-135">Jos olet antanut määritelmiä **Loppusumma**-kustannuskohteiden **Summan lähde/kohde** -kenttiin ennen sisennyksen suorittamista, määritelmät on annettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="13185-135">If you have entered definitions in the **Total From/To** fields for **End-Total** cost objects before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="13185-136">Toiminto korvaa kaikki **Loppusumma**-kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="13185-136">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="13185-137">Katso myös</span><span class="sxs-lookup"><span data-stu-id="13185-137">See Also</span></span>  
[<span data-ttu-id="13185-138">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="13185-138">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="13185-139">[Kustannuspaikkojen ja kustannuskohteiden määrittäminen tilikarttaan](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="13185-139">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="13185-140">[Kustannustyypin, kustannuspaikan ja kustannusobjektin saldot](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="13185-140">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="13185-141">[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="13185-141">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="13185-142">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="13185-142">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="13185-143">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="13185-143">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="13185-144">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13185-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

