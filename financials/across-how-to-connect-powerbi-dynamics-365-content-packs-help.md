---
title: "Power BI:n yhdistäminen Finance and Operations, Business editioniin | Microsoft Docs"
description: "Finance and Operations, Business editionin tiedoista saa kätevästi analyysi- ja BI-tietoja sekä tunnuslukuja Power BI:n ja Finance and Operations, Business editionin sisältöpaketeilla."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 02/05/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: aff8d95b13f795fa12d3146e5613712fb3baf9b4
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a><span data-ttu-id="ff2f8-103">Power BI:n yhdistäminen Finance and Operations, Business editionin sisältöpaketteihin</span><span class="sxs-lookup"><span data-stu-id="ff2f8-103">Connecting Power BI to Finance and Operations, Business edition Content Packs</span></span>
<span data-ttu-id="ff2f8-104">Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietojen analysointi on helppoa Power BI- ja Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -sisältöpakettien avulla.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="ff2f8-105">Power BI hakee tiedot ja muodostaa niiden perusteella valmiin koontinäytön ja raportit.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="ff2f8-106">Sinulla on oltava kelvollinen Dynamics 365- ja Power BI -tili.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="ff2f8-107">Sinun on ladattava myös [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="ff2f8-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="ff2f8-108">Power BI -sisältöpakettien käyttöä varten tarvitaan niiden taulukoiden käyttöoikeus, joista tiedot noudetaan.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="ff2f8-109">Lisätietoja on vaatimuksista on jäljempänä.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="ff2f8-110">Yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="ff2f8-110">How to Connect</span></span>
1. <span data-ttu-id="ff2f8-111">Valitse **Nouda tiedot** vasemman siirtymisruudun alareunassa.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="ff2f8-112">![Siirtyminen tietoja noudettaessa](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="ff2f8-113">Valitse **Palvelut**-ruudussa **Hae**.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="ff2f8-114">Avautuvassa ikkunassa näkyy **AppSource** **Power BI -sovellusten sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="ff2f8-115">![Sisältöpakettien valitseminen verkkopalveluista](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="ff2f8-116">Valitse ensin **Sovellukset** **Power BI -sovellusten sovellukset** -välilehdessä ja sitten **Microsoft Dynamics 365 for Finance and Operations** -sisältöpaketti, jota haluat käyttää. Valitse lopuksi **Hae se nyt**.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 for Finance and Operations** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="ff2f8-117">![Dynamics 365 for Finance and Operations, Business editionin ja Hae se nyt -vaihtoehdon valinta](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-117">![Select Dynamics 365 for Finance and Operations, Business edition and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="ff2f8-118">Anna kysyttäessä *yrityksen nimi* [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ff2f8-119">Se ei ole näyttönimi.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-119">This is not the display name.</span></span>  
<span data-ttu-id="ff2f8-120">![Dynamics 365 for Finance and Operations, Business editionin ja Hae se nyt -vaihtoehdon valinta](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-120">![Select Dynamics 365 for Finance and Operations, Business edition and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="ff2f8-121">Kun yhteys on muodostettu, koontinäyttö, raportti ja tietojoukko ladataan automaattisesti Power BI -työtilaan.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="ff2f8-122">Kun tämä on tehty, ruudut päivittävät tiedot tililtäsi.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="ff2f8-123">![Dynamics 365 for Finance and Operations, Business editionin ja Hae se nyt -vaihtoehdon valinta](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-123">![Select Dynamics 365 for Finance and Operations, Business edition  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="ff2f8-124">Mitä seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="ff2f8-124">What Now?</span></span>

- <span data-ttu-id="ff2f8-125">Kokeile [kysymyksen kirjoittamista kysymys- ja vastausruutuun](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) koontinäytön yläreunassa.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-125">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>  
- <span data-ttu-id="ff2f8-126">[Vaihda ruutuja](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-126">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="ff2f8-127">[Avaa taustalla oleva raportti valitsemalla ruutu](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles).</span><span class="sxs-lookup"><span data-stu-id="ff2f8-127">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="ff2f8-128">Vaikka tietojoukko on ajoitettu päivittymään kerran päivässä, voit muuttaa päivitysaikataulua. Voit myös kokeilla sen päivittämistä tarvittaessa **Päivitä nyt** -vaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-128">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="ff2f8-129">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="ff2f8-129">System Requirements</span></span>
<span data-ttu-id="ff2f8-130">Jos haluat tuoda [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietoja Power BI:hen, sinulla on oltava tietojen noutamiseen käytettävien verkkopalvelujen käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-130">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="ff2f8-131">Kunkin sisältöpaketin kanssa on käytettävä esimerkiksi seuraavia verkkopalveluja:</span><span class="sxs-lookup"><span data-stu-id="ff2f8-131">The web services required for each content pack include:</span></span>

<span data-ttu-id="ff2f8-132">**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**</span><span class="sxs-lookup"><span data-stu-id="ff2f8-132">**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**</span></span>
- <span data-ttu-id="ff2f8-133">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="ff2f8-133">SalesOpportunities</span></span>
- <span data-ttu-id="ff2f8-134">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ff2f8-134">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ff2f8-135">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Myynti**</span><span class="sxs-lookup"><span data-stu-id="ff2f8-135">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**</span></span>
- <span data-ttu-id="ff2f8-136">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ff2f8-136">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ff2f8-137">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="ff2f8-137">SalesDashboard</span></span>
- <span data-ttu-id="ff2f8-138">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ff2f8-138">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ff2f8-139">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Rahoitus**</span><span class="sxs-lookup"><span data-stu-id="ff2f8-139">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**</span></span>
- <span data-ttu-id="ff2f8-140">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="ff2f8-140">PowerBIFinance</span></span>
- <span data-ttu-id="ff2f8-141">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ff2f8-141">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ff2f8-142">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Projektit**</span><span class="sxs-lookup"><span data-stu-id="ff2f8-142">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Jobs**</span></span>
- <span data-ttu-id="ff2f8-143">Projektiluettelo</span><span class="sxs-lookup"><span data-stu-id="ff2f8-143">Job List</span></span>
- <span data-ttu-id="ff2f8-144">Projektin suunnittelurivit</span><span class="sxs-lookup"><span data-stu-id="ff2f8-144">Job Planning Lines</span></span>
- <span data-ttu-id="ff2f8-145">Projektitehtävärivit</span><span class="sxs-lookup"><span data-stu-id="ff2f8-145">Job Task Lines</span></span>

<span data-ttu-id="ff2f8-146">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Asiakasluettelo**</span><span class="sxs-lookup"><span data-stu-id="ff2f8-146">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Customers List**</span></span>
- <span data-ttu-id="ff2f8-147">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ff2f8-147">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ff2f8-148">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-148">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="ff2f8-149">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-149">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="ff2f8-150">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="ff2f8-150">SalesDashboard</span></span>
- <span data-ttu-id="ff2f8-151">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-151">Power_BI_Customer_List</span></span>
- <span data-ttu-id="ff2f8-152">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ff2f8-152">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ff2f8-153">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Nimikeluettelo**</span><span class="sxs-lookup"><span data-stu-id="ff2f8-153">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Items List**</span></span>
- <span data-ttu-id="ff2f8-154">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ff2f8-154">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ff2f8-155">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-155">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="ff2f8-156">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-156">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="ff2f8-157">Nimikkeet</span><span class="sxs-lookup"><span data-stu-id="ff2f8-157">Items</span></span>
- <span data-ttu-id="ff2f8-158">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="ff2f8-158">SalesDashboard</span></span>
- <span data-ttu-id="ff2f8-159">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ff2f8-159">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ff2f8-160">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Toimittajaluettelo**</span><span class="sxs-lookup"><span data-stu-id="ff2f8-160">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vendors List**</span></span>
- <span data-ttu-id="ff2f8-161">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ff2f8-161">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ff2f8-162">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-162">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="ff2f8-163">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-163">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="ff2f8-164">Nimikkeet</span><span class="sxs-lookup"><span data-stu-id="ff2f8-164">Items</span></span>
- <span data-ttu-id="ff2f8-165">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="ff2f8-165">SalesDashboard</span></span>
- <span data-ttu-id="ff2f8-166">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-166">Power_BI_Customer_List</span></span>
- <span data-ttu-id="ff2f8-167">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ff2f8-167">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ff2f8-168">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="ff2f8-168">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="ff2f8-169">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ff2f8-169">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="ff2f8-170">WWW-palvelut</span><span class="sxs-lookup"><span data-stu-id="ff2f8-170">Web Services</span></span>
<span data-ttu-id="ff2f8-171">Verkkopalveluja voi etsiä kätevästi hakemalla [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in verkkopalveluja.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-171">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ff2f8-172">Varmista, että edellä mainittujen verkkopalvelujen Julkaise-ruutu on valittu luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-172">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ff2f8-173">Vianetsintä</span><span class="sxs-lookup"><span data-stu-id="ff2f8-173">Troubleshooting</span></span>
<span data-ttu-id="ff2f8-174">Power BI:n koontinäyttö käyttää julkaistuja yllä mainittuja WWW-palveluita. Koontinäytössä ovat esittely-yrityksen tiedot tai oman yrityksesi tiedot, jos toit tiedot nykyisestä rahoitusratkaisustasi.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-174">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="ff2f8-175">Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-175">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="ff2f8-176">Virheellinen yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="ff2f8-176">Incorrect Company Name</span></span>  
<span data-ttu-id="ff2f8-177">Yleinen virhe on antaa yrityksen näyttönimi yrityksen nimen sijaan.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-177">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="ff2f8-178">Voit etsiä yrityksen nimen hakusanalla **Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-178">To find the company name search for **Companies**.</span></span> <span data-ttu-id="ff2f8-179">Anna sitten yrityksen nimi **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-179">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="ff2f8-180">Virheellinen käyttäjänimi ja salasana</span><span class="sxs-lookup"><span data-stu-id="ff2f8-180">Incorrect User Name and Password</span></span>  
<span data-ttu-id="ff2f8-181">Yhdistämiseen on käytettävä käyttäjänimeä ja salasanaa, joilla muodostetaan yhteys Microsoft Office 365 -tiliin.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-181">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="ff2f8-182">Sisältöpaketit edellyttävät myös, että sinulla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tili.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-182">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="ff2f8-183">Kun olet antanut tunnistetietosi, järjestelmä havaitsee automaattisesti ne Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -vuokraajat, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-183">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="ff2f8-184">Jos sinulla ei ole Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tilin käyttöoikeutta tai kokeiluversiota, saat virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-184">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="ff2f8-185">Avain ei vastannut mitään taulukon riviä</span><span class="sxs-lookup"><span data-stu-id="ff2f8-185">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="ff2f8-186">Jos annat yhteydenmuodostusprosessin aikana yrityksen nimen, joka ei ole sallittu, näyttöön voi tulla Avain ei vastannut mitään taulukon riviä -virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-186">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="ff2f8-187">Anna oikea yrityksen nimi ja yritä muodostaa yhteys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ff2f8-187">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff2f8-188">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ff2f8-188">See Also</span></span>
[<span data-ttu-id="ff2f8-189">Power BI:n käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="ff2f8-189">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="ff2f8-190">[Power BI – peruskäsitteet](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-190">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="ff2f8-191">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-191">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="ff2f8-192">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="ff2f8-192">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="ff2f8-193">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-193">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="ff2f8-194">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="ff2f8-194">Finance</span></span>](finance.md)  
<span data-ttu-id="ff2f8-195">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in raportoinnin määrittäminen Power BI:ssä](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="ff2f8-195">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

