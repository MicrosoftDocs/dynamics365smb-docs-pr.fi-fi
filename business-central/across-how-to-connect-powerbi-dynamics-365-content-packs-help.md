---
title: Power BI:n yhdistäminen Business Centraliin | Microsoft Docs
description: Analyysitietojen, liiketoimintatietoja ja tunnuslukujen hakeminen Business Central -tiedoista on helppoa Power BI- ja Business Central -sisältöpakettien avulla.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-powerbi
ms.openlocfilehash: b7e844f64a96ba02c1a5fa0231f7b6992f972677
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "932831"
---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="32d89-103">Power BI:n yhdistäminen Dynamics 365 Business Central -sisältöpaketit</span><span class="sxs-lookup"><span data-stu-id="32d89-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="32d89-104">Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietojen analysointi on helppoa Power BI- ja Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -sisältöpakettien avulla.</span><span class="sxs-lookup"><span data-stu-id="32d89-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="32d89-105">Power BI hakee tiedot ja muodostaa sitten näiden tietojen perusteella valmiin koontinäytön ja raportit.</span><span class="sxs-lookup"><span data-stu-id="32d89-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="32d89-106">Sinulla on oltava kelvollinen Dynamics 365- ja Power BI -tili.</span><span class="sxs-lookup"><span data-stu-id="32d89-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="32d89-107">Lisäksi [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) on ladattava, jos haluat luoda oman Power BI -raportteja.</span><span class="sxs-lookup"><span data-stu-id="32d89-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="32d89-108">Power BI -sisältöpakettien käyttöä varten tarvitaan niiden taulukoiden käyttöoikeus, joista tiedot noudetaan.</span><span class="sxs-lookup"><span data-stu-id="32d89-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="32d89-109">Lisätietoja on vaatimuksista on jäljempänä.</span><span class="sxs-lookup"><span data-stu-id="32d89-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="32d89-110">Yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="32d89-110">How to Connect</span></span>
1. <span data-ttu-id="32d89-111">Valitse **Nouda tiedot** vasemman siirtymisruudun alareunassa.</span><span class="sxs-lookup"><span data-stu-id="32d89-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="32d89-112">![Siirtyminen tietoja noudettaessa](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="32d89-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="32d89-113">Voit ehkä aloittaa käyttämisen Dynamics 365 Business Editionista.</span><span class="sxs-lookup"><span data-stu-id="32d89-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="32d89-114">Valitse roolikeskuksen Power BI -roolikeskuksessa **Raporttivalinta**.</span><span class="sxs-lookup"><span data-stu-id="32d89-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="32d89-115">Valitse valintanauhassa joko **Palvelu** tai **Oma organisaatio**.</span><span class="sxs-lookup"><span data-stu-id="32d89-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="32d89-116">Kun jompikumpi vaihtoehto valitaan, siirry joko Power BI:n organisaatiovalikoimaan tai Power BI:n palvelukirjastoon, joka voidaan myös suodattaa näyttämään vain [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]iin liittyvät sisältöpaketit.</span><span class="sxs-lookup"><span data-stu-id="32d89-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="32d89-117">Valitse **Palvelut**-ruudussa **Hae**.</span><span class="sxs-lookup"><span data-stu-id="32d89-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="32d89-118">Avautuvalla sivulla näkyy **AppSource** ja **Power BI -sovellusten sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="32d89-118">This will open a page with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="32d89-119">![Sisältöpakettien valitseminen verkkopalveluista](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="32d89-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="32d89-120">Valitse ensin **Sovellukset** **Power BI -sovellusten sovellukset** -välilehdessä ja sitten käytettävä **Microsoft Dynamics 365 Business Central** -sisältöpaketti. Valitse lopuksi **Hae se nyt**.</span><span class="sxs-lookup"><span data-stu-id="32d89-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="32d89-121">![Valitse ensin Dynamics 365 Business Central ja sitten Hae se nyt](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="32d89-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="32d89-122">Anna kysyttäessä *yrityksen nimi* [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="32d89-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="32d89-123">Se ei ole näyttönimi.</span><span class="sxs-lookup"><span data-stu-id="32d89-123">This is not the display name.</span></span> <span data-ttu-id="32d89-124">Yrityksen nimi sijaitsee [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] -instanssin Yritykset-sivulla.</span><span class="sxs-lookup"><span data-stu-id="32d89-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="32d89-125">![Valitse ensin Dynamics 365 Business Central ja sitten Hae se nyt](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="32d89-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="32d89-126">Kun yhteys on muodostettu, koontinäyttö, raportti ja tietojoukko ladataan automaattisesti Power BI -työtilaan.</span><span class="sxs-lookup"><span data-stu-id="32d89-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="32d89-127">Kun tämä on tehty, ruudut päivittävät tiedot [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] -yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="32d89-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="32d89-128">![Valitse ensin Dynamics 365 Business Central ja sitten Hae se nyt](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="32d89-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="32d89-129">Mitä seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="32d89-129">What Now?</span></span>

- <span data-ttu-id="32d89-130">Kokeile [kysymyksen kirjoittamista kysymys- ja vastausruutuun](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) koontinäytön yläreunassa.</span><span class="sxs-lookup"><span data-stu-id="32d89-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="32d89-131">[Vaihda ruutuja](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="32d89-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="32d89-132">[Avaa taustalla oleva raportti valitsemalla ruutu](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles).</span><span class="sxs-lookup"><span data-stu-id="32d89-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="32d89-133">Vaikka tietojoukko on ajoitettu päivittymään kerran päivässä, voit muuttaa päivitysaikataulua. Voit myös kokeilla sen päivittämistä tarvittaessa **Päivitä nyt** -vaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="32d89-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="32d89-134">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="32d89-134">System Requirements</span></span>
<span data-ttu-id="32d89-135">Jos haluat tuoda [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietoja Power BI:hen, sinulla on oltava tietojen noutamiseen käytettävien verkkopalvelujen käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="32d89-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="32d89-136">Kunkin sisältöpaketin kanssa on käytettävä esimerkiksi seuraavia verkkopalveluja:</span><span class="sxs-lookup"><span data-stu-id="32d89-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="32d89-137">Roolikeskuksen raportit</span><span class="sxs-lookup"><span data-stu-id="32d89-137">Role Center Reports</span></span>

<span data-ttu-id="32d89-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="32d89-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="32d89-139">Myyntimahdollisuudet</span><span class="sxs-lookup"><span data-stu-id="32d89-139">Sales Opportunities</span></span>
- <span data-ttu-id="32d89-140">Excel-malli Näytä yritys</span><span class="sxs-lookup"><span data-stu-id="32d89-140">Excel Template View Company</span></span>
- <span data-ttu-id="32d89-141">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-141">Power BI Report Labels</span></span>

<span data-ttu-id="32d89-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="32d89-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="32d89-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="32d89-143">PowerBIFinance</span></span>
- <span data-ttu-id="32d89-144">Excel-malli Näytä yritys</span><span class="sxs-lookup"><span data-stu-id="32d89-144">Excel Template View Company</span></span>
- <span data-ttu-id="32d89-145">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-145">Power BI Report Labels</span></span>

<span data-ttu-id="32d89-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="32d89-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="32d89-147">Projektiluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-147">Job List</span></span>
- <span data-ttu-id="32d89-148">Projektin suunnittelurivit</span><span class="sxs-lookup"><span data-stu-id="32d89-148">Job Planning Lines</span></span>
- <span data-ttu-id="32d89-149">Projektitehtävärivit</span><span class="sxs-lookup"><span data-stu-id="32d89-149">Job Task Lines</span></span>
- <span data-ttu-id="32d89-150">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-150">Power BI Report Labels</span></span>
- <span data-ttu-id="32d89-151">Excel-malli Näytä yritys</span><span class="sxs-lookup"><span data-stu-id="32d89-151">Excel Template View Company</span></span>

<span data-ttu-id="32d89-152">**Microsoft Dynamics 365 Business Central – Sales**</span><span class="sxs-lookup"><span data-stu-id="32d89-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="32d89-153">Myynnin koontinäyttö</span><span class="sxs-lookup"><span data-stu-id="32d89-153">Sales Dashboard</span></span>
- <span data-ttu-id="32d89-154">Excel-malli Näytä yritys</span><span class="sxs-lookup"><span data-stu-id="32d89-154">Excel Template View Company</span></span>
- <span data-ttu-id="32d89-155">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="32d89-156">Luettelosivun raportit</span><span class="sxs-lookup"><span data-stu-id="32d89-156">List Page Reports</span></span> 

<span data-ttu-id="32d89-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="32d89-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="32d89-158">Asiakaskohtainen nimikemyynti</span><span class="sxs-lookup"><span data-stu-id="32d89-158">Item Sales by Customer</span></span>
- <span data-ttu-id="32d89-159">Power BI -nimikkeiden ostoluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="32d89-160">Power BI -nimikkeiden myyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="32d89-161">Myynnin koontinäyttö</span><span class="sxs-lookup"><span data-stu-id="32d89-161">Sales Dashboard</span></span>
- <span data-ttu-id="32d89-162">Power BI -asiakasluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-162">Power BI Customer List</span></span>
- <span data-ttu-id="32d89-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="32d89-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="32d89-164">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-164">Power BI Report Labels</span></span> 

<span data-ttu-id="32d89-165">**Microsoft Dynamics 365 Business Central – General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="32d89-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="32d89-166">Power BI -PK-summaluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="32d89-167">Power BI -PK-budjettisumma</span><span class="sxs-lookup"><span data-stu-id="32d89-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="32d89-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="32d89-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="32d89-169">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-169">Power BI Report Labels</span></span>

<span data-ttu-id="32d89-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="32d89-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="32d89-171">Asiakaskohtainen nimikemyynti</span><span class="sxs-lookup"><span data-stu-id="32d89-171">Item Sales by Customer</span></span>
- <span data-ttu-id="32d89-172">Power BI -nimikkeiden ostoluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="32d89-173">Power BI -nimikkeiden myyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="32d89-174">Myynnin koontinäyttö</span><span class="sxs-lookup"><span data-stu-id="32d89-174">Sales Dashboard</span></span>
- <span data-ttu-id="32d89-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="32d89-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="32d89-176">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-176">Power BI Report Labels</span></span>

<span data-ttu-id="32d89-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="32d89-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="32d89-178">Power BI -projektiluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-178">Power BI Jobs List</span></span>
- <span data-ttu-id="32d89-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="32d89-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="32d89-180">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-180">Power BI Report Labels</span></span>

<span data-ttu-id="32d89-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="32d89-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="32d89-182">Power BI -ostoluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-182">Power BI Purchase List</span></span>
- <span data-ttu-id="32d89-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="32d89-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="32d89-184">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-184">Power BI Report Labels</span></span>

<span data-ttu-id="32d89-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="32d89-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="32d89-186">Power BI -myyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-186">Power BI Sales List</span></span>
- <span data-ttu-id="32d89-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="32d89-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="32d89-188">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-188">Power BI Report Labels</span></span>


<span data-ttu-id="32d89-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="32d89-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="32d89-190">Power BI -nimikkeiden ostoluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="32d89-191">Power BI -nimikkeiden myyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="32d89-192">Power BI -toimittajaluettelo</span><span class="sxs-lookup"><span data-stu-id="32d89-192">Power BI Vendor List</span></span>
- <span data-ttu-id="32d89-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="32d89-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="32d89-194">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="32d89-195">WWW-palvelut</span><span class="sxs-lookup"><span data-stu-id="32d89-195">Web Services</span></span>
<span data-ttu-id="32d89-196">Verkkopalveluja voi etsiä kätevästi hakemalla [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in verkkopalveluja.</span><span class="sxs-lookup"><span data-stu-id="32d89-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="32d89-197">Varmista, että edellä mainittujen verkkopalvelujen Julkaise-ruutu on valittu luettelossa.</span><span class="sxs-lookup"><span data-stu-id="32d89-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="32d89-198">Vianetsintä</span><span class="sxs-lookup"><span data-stu-id="32d89-198">Troubleshooting</span></span>
<span data-ttu-id="32d89-199">Power BI:n koontinäyttö käyttää julkaistuja edellä mainittuja verkkopalveluita. Koontinäytössä ovat esittely-yrityksen tiedot tai oman yrityksesi tiedot, jos toit tiedot nykyisestä rahoitusratkaisustasi.</span><span class="sxs-lookup"><span data-stu-id="32d89-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="32d89-200">Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.</span><span class="sxs-lookup"><span data-stu-id="32d89-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="32d89-201">Virheellinen yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="32d89-201">Incorrect Company Name</span></span>  
<span data-ttu-id="32d89-202">Yleinen virhe on antaa yrityksen näyttönimi yrityksen nimen sijaan.</span><span class="sxs-lookup"><span data-stu-id="32d89-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="32d89-203">Voit etsiä yrityksen nimen hakusanalla **Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="32d89-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="32d89-204">Anna sitten yrityksen nimi **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="32d89-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="32d89-205">Virheellinen käyttäjänimi ja salasana</span><span class="sxs-lookup"><span data-stu-id="32d89-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="32d89-206">Yhdistämiseen on käytettävä käyttäjänimeä ja salasanaa, joilla muodostetaan yhteys Microsoft Office 365 -tiliin.</span><span class="sxs-lookup"><span data-stu-id="32d89-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="32d89-207">Sisältöpaketit edellyttävät myös, että sinulla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tili.</span><span class="sxs-lookup"><span data-stu-id="32d89-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="32d89-208">Kun olet antanut tunnistetietosi, järjestelmä havaitsee automaattisesti ne Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -vuokraajat, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="32d89-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="32d89-209">Jos sinulla ei ole Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tilin käyttöoikeutta tai kokeiluversiota, saat virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="32d89-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="32d89-210">Avain ei vastannut mitään taulukon riviä</span><span class="sxs-lookup"><span data-stu-id="32d89-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="32d89-211">Jos annat yhteydenmuodostusprosessin aikana yrityksen nimen, joka ei ole sallittu, näyttöön voi avautua virhesanoma, jonka mukaan avain ei vastannut mitään taulukon riviä.</span><span class="sxs-lookup"><span data-stu-id="32d89-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="32d89-212">Anna oikea yrityksen nimi ja yritä muodostaa yhteys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="32d89-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="32d89-213">Katso myös</span><span class="sxs-lookup"><span data-stu-id="32d89-213">See Also</span></span>
[<span data-ttu-id="32d89-214">Power BI:n käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="32d89-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="32d89-215">Power BI – peruskäsitteet</span><span class="sxs-lookup"><span data-stu-id="32d89-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="32d89-216">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="32d89-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="32d89-217">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="32d89-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="32d89-218">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="32d89-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="32d89-219">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="32d89-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="32d89-220">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="32d89-220">Finance</span></span>](finance.md)  
<span data-ttu-id="32d89-221">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in raportoinnin määrittäminen Power BI:ssä](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="32d89-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  
