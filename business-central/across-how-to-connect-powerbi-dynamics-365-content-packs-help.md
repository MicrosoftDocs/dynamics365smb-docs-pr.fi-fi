---
title: "Power BI- ja Business Central -sovelluksen yhdistäminen | Microsoft Docs"
description: "Analyysitietojen, liiketoimintatietoja ja tunnuslukujen hakeminen Business Central -tiedoista on helppoa Power BI- ja Business Central -sisältöpakettien avulla."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 48c57e03f4679ea05792304fe13bdf896be2f1e3
ms.contentlocale: fi-fi
ms.lasthandoff: 11/22/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="01a14-103">Power BI- ja Dynamics 365 Business Central -sisältöpakettien yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="01a14-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="01a14-104">Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietojen analysointi on helppoa Power BI- ja Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -sisältöpakettien avulla.</span><span class="sxs-lookup"><span data-stu-id="01a14-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="01a14-105">Power BI hakee tiedot ja muodostaa niiden perusteella valmiin koontinäytön ja raportit.</span><span class="sxs-lookup"><span data-stu-id="01a14-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="01a14-106">Sinulla on oltava kelvollinen Dynamics 365- ja Power BI -tili.</span><span class="sxs-lookup"><span data-stu-id="01a14-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="01a14-107">Sinun on ladattava myös [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/), jos haluat luoda omia Power BI -raportteja.</span><span class="sxs-lookup"><span data-stu-id="01a14-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="01a14-108">Power BI -sisältöpakettien käyttöä varten tarvitaan niiden taulukoiden käyttöoikeus, joista tiedot noudetaan.</span><span class="sxs-lookup"><span data-stu-id="01a14-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="01a14-109">Lisätietoja on vaatimuksista on jäljempänä.</span><span class="sxs-lookup"><span data-stu-id="01a14-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="01a14-110">Yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="01a14-110">How to Connect</span></span>
1. <span data-ttu-id="01a14-111">Valitse **Nouda tiedot** vasemman siirtymisruudun alareunassa.</span><span class="sxs-lookup"><span data-stu-id="01a14-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="01a14-112">![Siirtyminen tietoja noudettaessa](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="01a14-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="01a14-113">Aloittaminen voi olla mahdollista myös Dynamics 365 Business Editionista.</span><span class="sxs-lookup"><span data-stu-id="01a14-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="01a14-114">Valitse roolikeskuksen Power BI -roolikeskuksessa **Raporttivalinta**.</span><span class="sxs-lookup"><span data-stu-id="01a14-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="01a14-115">Valitse valintanauhassa joko **Palvelu** tai **Oma organisaatio**.</span><span class="sxs-lookup"><span data-stu-id="01a14-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="01a14-116">Kun jompikumpi vaihtoehto valitaan, siirry joko Power BI:n organisaatiovalikoimaan tai Power BI:n palvelukirjastoon, joka voidaan myös suodattaa näyttämään vain [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]iin liittyvät sisältöpaketit.</span><span class="sxs-lookup"><span data-stu-id="01a14-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="01a14-117">Valitse **Palvelut**-ruudussa **Hae**.</span><span class="sxs-lookup"><span data-stu-id="01a14-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="01a14-118">Avautuvalla sivulla näkyy **AppSource** ja **Power BI -sovellusten sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="01a14-118">This will open a page with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="01a14-119">![Sisältöpakettien valitseminen verkkopalveluista](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="01a14-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="01a14-120">Valitse ensin **Sovellukset** **Power BI -sovellusten sovellukset** -välilehdessä ja sitten käytettävä **Microsoft Dynamics 365 Business Central** -sisältöpaketti. Valitse lopuksi **Hae se nyt**.</span><span class="sxs-lookup"><span data-stu-id="01a14-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="01a14-121">![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="01a14-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="01a14-122">Anna kysyttäessä *yrityksen nimi* [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="01a14-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="01a14-123">Se ei ole näyttönimi.</span><span class="sxs-lookup"><span data-stu-id="01a14-123">This is not the display name.</span></span> <span data-ttu-id="01a14-124">Yrityksen nimi sijaitsee [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] -instanssin Yritykset-sivulla.</span><span class="sxs-lookup"><span data-stu-id="01a14-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="01a14-125">![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="01a14-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="01a14-126">Kun yhteys on muodostettu, koontinäyttö, raportti ja tietojoukko ladataan automaattisesti Power BI -työtilaan.</span><span class="sxs-lookup"><span data-stu-id="01a14-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="01a14-127">Kun tämä on tehty, ruudut päivittävät tiedot [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] -yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="01a14-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="01a14-128">![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="01a14-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="01a14-129">Mitä seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="01a14-129">What Now?</span></span>

- <span data-ttu-id="01a14-130">Kokeile [kysymyksen kirjoittamista kysymys- ja vastausruutuun](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) koontinäytön yläreunassa.</span><span class="sxs-lookup"><span data-stu-id="01a14-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="01a14-131">[Vaihda ruutuja](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="01a14-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="01a14-132">[Avaa taustalla oleva raportti valitsemalla ruutu](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles).</span><span class="sxs-lookup"><span data-stu-id="01a14-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="01a14-133">Vaikka tietojoukko on ajoitettu päivittymään kerran päivässä, voit muuttaa päivitysaikataulua. Voit myös kokeilla sen päivittämistä tarvittaessa **Päivitä nyt** -vaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="01a14-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="01a14-134">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="01a14-134">System Requirements</span></span>
<span data-ttu-id="01a14-135">Jos haluat tuoda [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietoja Power BI:hen, sinulla on oltava tietojen noutamiseen käytettävien verkkopalvelujen käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="01a14-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="01a14-136">Kunkin sisältöpaketin kanssa on käytettävä esimerkiksi seuraavia verkkopalveluja:</span><span class="sxs-lookup"><span data-stu-id="01a14-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="01a14-137">Roolikeskuksen raportit</span><span class="sxs-lookup"><span data-stu-id="01a14-137">Role Center Reports</span></span>

<span data-ttu-id="01a14-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="01a14-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="01a14-139">Myyntimahdollisuudet</span><span class="sxs-lookup"><span data-stu-id="01a14-139">Sales Opportunities</span></span>
- <span data-ttu-id="01a14-140">Excel-malli Näytä yritys</span><span class="sxs-lookup"><span data-stu-id="01a14-140">Excel Template View Company</span></span>
- <span data-ttu-id="01a14-141">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-141">Power BI Report Labels</span></span>

<span data-ttu-id="01a14-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="01a14-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="01a14-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="01a14-143">PowerBIFinance</span></span>
- <span data-ttu-id="01a14-144">Excel-malli Näytä yritys</span><span class="sxs-lookup"><span data-stu-id="01a14-144">Excel Template View Company</span></span>
- <span data-ttu-id="01a14-145">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-145">Power BI Report Labels</span></span>

<span data-ttu-id="01a14-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="01a14-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="01a14-147">Projektiluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-147">Job List</span></span>
- <span data-ttu-id="01a14-148">Projektin suunnittelurivit</span><span class="sxs-lookup"><span data-stu-id="01a14-148">Job Planning Lines</span></span>
- <span data-ttu-id="01a14-149">Projektitehtävärivit</span><span class="sxs-lookup"><span data-stu-id="01a14-149">Job Task Lines</span></span>
- <span data-ttu-id="01a14-150">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-150">Power BI Report Labels</span></span>
- <span data-ttu-id="01a14-151">Excel-malli Näytä yritys</span><span class="sxs-lookup"><span data-stu-id="01a14-151">Excel Template View Company</span></span>

<span data-ttu-id="01a14-152">**Microsoft Dynamics 365 Business Central - Sales**</span><span class="sxs-lookup"><span data-stu-id="01a14-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="01a14-153">Myynnin koontinäyttö</span><span class="sxs-lookup"><span data-stu-id="01a14-153">Sales Dashboard</span></span>
- <span data-ttu-id="01a14-154">Excel-malli Näytä yritys</span><span class="sxs-lookup"><span data-stu-id="01a14-154">Excel Template View Company</span></span>
- <span data-ttu-id="01a14-155">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="01a14-156">Luettelosivun raportit</span><span class="sxs-lookup"><span data-stu-id="01a14-156">List Page Reports</span></span> 

<span data-ttu-id="01a14-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="01a14-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="01a14-158">Asiakaskohtainen nimikemyynti</span><span class="sxs-lookup"><span data-stu-id="01a14-158">Item Sales by Customer</span></span>
- <span data-ttu-id="01a14-159">Power BI -nimikeostoluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="01a14-160">Power BI -nimikemyyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="01a14-161">Myynnin koontinäyttö</span><span class="sxs-lookup"><span data-stu-id="01a14-161">Sales Dashboard</span></span>
- <span data-ttu-id="01a14-162">Power BI -asiakasluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-162">Power BI Customer List</span></span>
- <span data-ttu-id="01a14-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="01a14-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="01a14-164">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-164">Power BI Report Labels</span></span> 

<span data-ttu-id="01a14-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="01a14-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="01a14-166">Power BI -PK-summaluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="01a14-167">Power BI -PK-budjettisumma</span><span class="sxs-lookup"><span data-stu-id="01a14-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="01a14-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="01a14-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="01a14-169">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-169">Power BI Report Labels</span></span>

<span data-ttu-id="01a14-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="01a14-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="01a14-171">Asiakaskohtainen nimikemyynti</span><span class="sxs-lookup"><span data-stu-id="01a14-171">Item Sales by Customer</span></span>
- <span data-ttu-id="01a14-172">Power BI -nimikeostoluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="01a14-173">Power BI -nimikemyyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="01a14-174">Myynnin koontinäyttö</span><span class="sxs-lookup"><span data-stu-id="01a14-174">Sales Dashboard</span></span>
- <span data-ttu-id="01a14-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="01a14-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="01a14-176">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-176">Power BI Report Labels</span></span>

<span data-ttu-id="01a14-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="01a14-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="01a14-178">Power BI -projektiluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-178">Power BI Jobs List</span></span>
- <span data-ttu-id="01a14-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="01a14-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="01a14-180">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-180">Power BI Report Labels</span></span>

<span data-ttu-id="01a14-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="01a14-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="01a14-182">Power BI -ostoluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-182">Power BI Purchase List</span></span>
- <span data-ttu-id="01a14-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="01a14-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="01a14-184">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-184">Power BI Report Labels</span></span>

<span data-ttu-id="01a14-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="01a14-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="01a14-186">Power BI -myyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-186">Power BI Sales List</span></span>
- <span data-ttu-id="01a14-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="01a14-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="01a14-188">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-188">Power BI Report Labels</span></span>


<span data-ttu-id="01a14-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="01a14-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="01a14-190">Power BI -nimikeostoluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="01a14-191">Power BI -nimikemyyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="01a14-192">Power BI -toimittajaluettelo</span><span class="sxs-lookup"><span data-stu-id="01a14-192">Power BI Vendor List</span></span>
- <span data-ttu-id="01a14-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="01a14-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="01a14-194">Power BI -raporttien selitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="01a14-195">WWW-palvelut</span><span class="sxs-lookup"><span data-stu-id="01a14-195">Web Services</span></span>
<span data-ttu-id="01a14-196">Verkkopalveluja voi etsiä kätevästi hakemalla [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in verkkopalveluja.</span><span class="sxs-lookup"><span data-stu-id="01a14-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="01a14-197">Varmista, että edellä mainittujen verkkopalvelujen Julkaise-ruutu on valittu luettelossa.</span><span class="sxs-lookup"><span data-stu-id="01a14-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="01a14-198">Vianetsintä</span><span class="sxs-lookup"><span data-stu-id="01a14-198">Troubleshooting</span></span>
<span data-ttu-id="01a14-199">Power BI:n koontinäyttö käyttää julkaistuja yllä mainittuja WWW-palveluita. Koontinäytössä ovat esittely-yrityksen tiedot tai oman yrityksesi tiedot, jos toit tiedot nykyisestä rahoitusratkaisustasi.</span><span class="sxs-lookup"><span data-stu-id="01a14-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="01a14-200">Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.</span><span class="sxs-lookup"><span data-stu-id="01a14-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="01a14-201">Virheellinen yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="01a14-201">Incorrect Company Name</span></span>  
<span data-ttu-id="01a14-202">Yleinen virhe on antaa yrityksen näyttönimi yrityksen nimen sijaan.</span><span class="sxs-lookup"><span data-stu-id="01a14-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="01a14-203">Voit etsiä yrityksen nimen hakusanalla **Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="01a14-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="01a14-204">Anna sitten yrityksen nimi **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="01a14-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="01a14-205">Virheellinen käyttäjänimi ja salasana</span><span class="sxs-lookup"><span data-stu-id="01a14-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="01a14-206">Yhdistämiseen on käytettävä käyttäjänimeä ja salasanaa, joilla muodostetaan yhteys Microsoft Office 365 -tiliin.</span><span class="sxs-lookup"><span data-stu-id="01a14-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="01a14-207">Sisältöpaketit edellyttävät myös, että sinulla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tili.</span><span class="sxs-lookup"><span data-stu-id="01a14-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="01a14-208">Kun olet antanut tunnistetietosi, järjestelmä havaitsee automaattisesti ne Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -vuokraajat, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="01a14-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="01a14-209">Jos sinulla ei ole Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tilin käyttöoikeutta tai kokeiluversiota, saat virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="01a14-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="01a14-210">Avain ei vastannut mitään taulukon riviä</span><span class="sxs-lookup"><span data-stu-id="01a14-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="01a14-211">Jos annat yhteydenmuodostusprosessin aikana yrityksen nimen, joka ei ole sallittu, näyttöön voi avautua virhesanoma, jonka mukaan avain ei vastannut mitään taulukon riviä.</span><span class="sxs-lookup"><span data-stu-id="01a14-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="01a14-212">Anna oikea yrityksen nimi ja yritä muodostaa yhteys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="01a14-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="01a14-213">Katso myös</span><span class="sxs-lookup"><span data-stu-id="01a14-213">See Also</span></span>
[<span data-ttu-id="01a14-214">Power BI:n käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="01a14-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="01a14-215">Power BI – peruskäsitteet</span><span class="sxs-lookup"><span data-stu-id="01a14-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="01a14-216">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="01a14-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="01a14-217">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="01a14-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="01a14-218">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="01a14-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="01a14-219">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="01a14-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="01a14-220">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="01a14-220">Finance</span></span>](finance.md)  
<span data-ttu-id="01a14-221">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in raportoinnin määrittäminen Power BI:ssä](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="01a14-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

