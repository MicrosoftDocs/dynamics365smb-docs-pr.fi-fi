---
title: "Kustannustyyppikartan määrittäminen | Microsoft Docs"
description: "Kustannustyyppikaavio on vastaava kuin pääkirjanpidon tilikartta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: c89170fd159428d771df105ca16a1d91d29651e4
ms.contentlocale: fi-fi
ms.lasthandoff: 04/16/2018

---
# <a name="set-up-cost-types"></a><span data-ttu-id="bf830-103">Kustannustyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf830-103">Set Up Cost Types</span></span>
<span data-ttu-id="bf830-104">Kustannustyyppikartta vastaa pääkirjanpidon tilikarttaa.</span><span class="sxs-lookup"><span data-stu-id="bf830-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="bf830-105">Voit määrittää kustannustyyppikaavion seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="bf830-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="bf830-106">Kustannustyyppien kaavioiden rakenne vastaa pääkirjanpidon tuloslaskelmatilejä.</span><span class="sxs-lookup"><span data-stu-id="bf830-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="bf830-107">Sitten voit siirtää kirjanpidon tilikartan kustannustyyppikaavioon.</span><span class="sxs-lookup"><span data-stu-id="bf830-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="bf830-108">Siirron jälkeen voit tehdä tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="bf830-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="bf830-109">Luo uusi kustannustyyppien kaavio tai lisää uudet kustannustyypit aiemmin luotuun kustannustyyppien kaavioon.</span><span class="sxs-lookup"><span data-stu-id="bf830-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="bf830-110">Sinun on luotava jokainen uusi kustannustyyppi erikseen.</span><span class="sxs-lookup"><span data-stu-id="bf830-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="bf830-111">Siirrä pääkirjanpidon tilikartta kustannustyyppikaavioon</span><span class="sxs-lookup"><span data-stu-id="bf830-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="bf830-112">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannustyyppikartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="bf830-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bf830-113">Valitse **Hae kustannustyypit tilikartasta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="bf830-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="bf830-114">Vahvista siirto valitsemalla valintaikkunassa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bf830-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="bf830-115">Funktio käyttää tilikarttaa kustannustyyppikaavion luontiin.</span><span class="sxs-lookup"><span data-stu-id="bf830-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="bf830-116">Kustannustyyppikaavio sisältää nyt kaikki pääkirjanpidon tuloslaskelmat, mukaan lukien otsikot ja välisummat.</span><span class="sxs-lookup"><span data-stu-id="bf830-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="bf830-117">Voit tarvittaessa muuttaa kustannustyyppejä.</span><span class="sxs-lookup"><span data-stu-id="bf830-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="bf830-118">Voit esimerkiksi poistaa kustannustyyppien kaksoiskappaleet.</span><span class="sxs-lookup"><span data-stu-id="bf830-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="bf830-119">**Rekisteröi kustannustyypit tilikartassa** -toiminto päivittää tilikartan ja kustannustyyppukaavion välisen suhteen.</span><span class="sxs-lookup"><span data-stu-id="bf830-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="bf830-120">**Nro**-kenttä</span><span class="sxs-lookup"><span data-stu-id="bf830-120">The **No.**</span></span> <span data-ttu-id="bf830-121">on täytetty ja vahvistettu, että jokaiselle KP-tilille on liitetty vain yksi kustannuslaji.</span><span class="sxs-lookup"><span data-stu-id="bf830-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="bf830-122">Toiminto suoritetaan automaattisesti ennen KP-tapahtumien siirtämistä kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="bf830-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-window"></a><span data-ttu-id="bf830-123">Uuden kustannustyypin määrittäminen Kustannustyyppikartta-ikkunassa</span><span class="sxs-lookup"><span data-stu-id="bf830-123">To set up new cost types in the Chart of Cost Types window</span></span>  
1. <span data-ttu-id="bf830-124">Avaa **Kustannustyyppikartta**-ikkuna muokkaustilassa.</span><span class="sxs-lookup"><span data-stu-id="bf830-124">Open the **Chart of Cost Types** window in edit mode.</span></span>  
2. <span data-ttu-id="bf830-125">Täytä kentät tarvittaessa ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="bf830-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]  
   >  <span data-ttu-id="bf830-126">Voit määrittää ja ylläpitää kustannustyyppejä joko **Kustannustyypin kortti** -kortissa tai **Kustannustyyppikartta**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="bf830-126">You can set up and maintain cost types in either the **Cost Type Card** window or in the **Chart of Cost Types** window.</span></span> <span data-ttu-id="bf830-127">Tässä toimenpiteessä määrität kustannustyypit **Kustannustyyppikartta**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="bf830-127">In this procedure, you set up cost types in the **Chart of Cost Types** window.</span></span>

3. <span data-ttu-id="bf830-128">Kun olet luonut kaikki kustannustyypit, valitse **Sisennä kustannustyypit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="bf830-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="bf830-129">Valitse valintaikkunassa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bf830-129">In the dialog box, choose the **Yes** button.</span></span>  
4. <span data-ttu-id="bf830-130">Linkitä uusi kustannustyyppi vastaavalle pääkirjanpidon tilille.</span><span class="sxs-lookup"><span data-stu-id="bf830-130">Link the new cost type to the corresponding general ledger account.</span></span>  

   > [!IMPORTANT]  
   >  <span data-ttu-id="bf830-131">Jos olet antanut määritelmiä **Loppusumma**-rivien **Summausväli**-kentissä ennen **Sisennä kustannustyypit** -toiminnon suorittamista, määritelmät on annettava uudelleen, koska toiminto korvaa kaikki **Loppusumma**-kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="bf830-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="bf830-132">Päivitä kustannustyypit</span><span class="sxs-lookup"><span data-stu-id="bf830-132">To update cost types</span></span>  
1.  <span data-ttu-id="bf830-133">Valitse **Kustannuslaskennan asetukset** -ikkunassa, haluatko kustannustyyppikaavion päivittyvän automaattisesti, kun tilikarttaa muutetaan.</span><span class="sxs-lookup"><span data-stu-id="bf830-133">In the **Cost Accounting Setup** window, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="bf830-134">Voit tehdä **Tasaa KP-tili** -kentässä valinnan seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="bf830-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="bf830-135">**Ei tasausta** - Vastaavaa muutosta ei tehdä kustannustyyppikaaviossa, kun tilikarttaa muutetaan.</span><span class="sxs-lookup"><span data-stu-id="bf830-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="bf830-136">**Automaattinen** - Vastaava muutos tehdään kustannustyyppikaaviossa, kun muutat tilikartan.</span><span class="sxs-lookup"><span data-stu-id="bf830-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="bf830-137">**Kysy** - Näkyviin tulee sanoma, jossa kysytään, haluatko tehdä vastaavan muutoksen kustannustyyppien kaaviossa, kun muutat tilikarttaa.</span><span class="sxs-lookup"><span data-stu-id="bf830-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bf830-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="bf830-138">See Also</span></span>  
[<span data-ttu-id="bf830-139">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="bf830-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="bf830-140">[Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="bf830-140">[Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md) </span></span>  
<span data-ttu-id="bf830-141">[Kustannuspaikkojen ja kustannuskohteiden määrittäminen tilikarttaan](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="bf830-141">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="bf830-142">[Kustannustyypin, kustannuspaikan ja kustannusobjektin saldot](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="bf830-142">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="bf830-143">[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="bf830-143">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="bf830-144">[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="bf830-144">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="bf830-145">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="bf830-145">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="bf830-146">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf830-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

