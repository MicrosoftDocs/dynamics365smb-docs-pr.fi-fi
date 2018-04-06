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
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="18cd0-103">Power BI- ja Business Central -sisältöpakettien yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="18cd0-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="18cd0-104">Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietojen analysointi on helppoa Power BI- ja Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -sisältöpakettien avulla.</span><span class="sxs-lookup"><span data-stu-id="18cd0-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="18cd0-105">Power BI hakee tiedot ja muodostaa niiden perusteella valmiin koontinäytön ja raportit.</span><span class="sxs-lookup"><span data-stu-id="18cd0-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="18cd0-106">Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Power BI -tili.</span><span class="sxs-lookup"><span data-stu-id="18cd0-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="18cd0-107">Sinun on ladattava myös [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="18cd0-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="18cd0-108">Power BI -sisältöpakettien käyttöä varten tarvitaan niiden taulukoiden käyttöoikeus, joista tiedot noudetaan.</span><span class="sxs-lookup"><span data-stu-id="18cd0-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="18cd0-109">Lisätietoja on vaatimuksista on jäljempänä.</span><span class="sxs-lookup"><span data-stu-id="18cd0-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="18cd0-110">Yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="18cd0-110">How to Connect</span></span>
1. <span data-ttu-id="18cd0-111">Valitse **Nouda tiedot** vasemman siirtymisruudun alareunassa.</span><span class="sxs-lookup"><span data-stu-id="18cd0-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="18cd0-112">![Siirtyminen tietoja noudettaessa](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="18cd0-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="18cd0-113">Valitse **Palvelut**-ruudussa **Hae**.</span><span class="sxs-lookup"><span data-stu-id="18cd0-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="18cd0-114">Avautuvassa ikkunassa näkyy **AppSource** **Power BI -sovellusten sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="18cd0-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="18cd0-115">![Sisältöpakettien valitseminen verkkopalveluista](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="18cd0-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="18cd0-116">Valitse ensin **Sovellukset** **Power BI -sovellusten sovellukset** -välilehdessä ja sitten **Microsoft Dynamics 365 Business Central** -sisältöpaketti, jota haluat käyttää. Valitse lopuksi **Hae se nyt**.</span><span class="sxs-lookup"><span data-stu-id="18cd0-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="18cd0-117">![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="18cd0-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="18cd0-118">Anna kysyttäessä *yrityksen nimi* [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="18cd0-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="18cd0-119">Se ei ole näyttönimi.</span><span class="sxs-lookup"><span data-stu-id="18cd0-119">This is not the display name.</span></span>  
<span data-ttu-id="18cd0-120">![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="18cd0-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="18cd0-121">Kun yhteys on muodostettu, koontinäyttö, raportti ja tietojoukko ladataan automaattisesti Power BI -työtilaan.</span><span class="sxs-lookup"><span data-stu-id="18cd0-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="18cd0-122">Kun tämä on tehty, ruudut päivittävät tiedot tililtäsi.</span><span class="sxs-lookup"><span data-stu-id="18cd0-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="18cd0-123">![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="18cd0-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="18cd0-124">Mitä seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="18cd0-124">What Now?</span></span>

- <span data-ttu-id="18cd0-125">[Vaihda ruutuja](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="18cd0-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="18cd0-126">[Avaa taustalla oleva raportti valitsemalla ruutu](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles).</span><span class="sxs-lookup"><span data-stu-id="18cd0-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="18cd0-127">Vaikka tietojoukko on ajoitettu päivittymään kerran päivässä, voit muuttaa päivitysaikataulua. Voit myös kokeilla sen päivittämistä tarvittaessa **Päivitä nyt** -vaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="18cd0-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="18cd0-128">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="18cd0-128">System Requirements</span></span>
<span data-ttu-id="18cd0-129">Jos haluat tuoda [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietoja Power BI:hen, sinulla on oltava tietojen noutamiseen käytettävien verkkopalvelujen käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="18cd0-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="18cd0-130">Kunkin sisältöpaketin kanssa on käytettävä esimerkiksi seuraavia verkkopalveluja:</span><span class="sxs-lookup"><span data-stu-id="18cd0-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="18cd0-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="18cd0-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="18cd0-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="18cd0-132">SalesOpportunities</span></span>
- <span data-ttu-id="18cd0-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="18cd0-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="18cd0-134">**Microsoft Dynamics 365 Business Central – Myynti**</span><span class="sxs-lookup"><span data-stu-id="18cd0-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="18cd0-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="18cd0-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="18cd0-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="18cd0-136">SalesDashboard</span></span>
- <span data-ttu-id="18cd0-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="18cd0-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="18cd0-138">**Microsoft Dynamics 365 Business Central – Rahoitus**</span><span class="sxs-lookup"><span data-stu-id="18cd0-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="18cd0-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="18cd0-139">PowerBIFinance</span></span>
- <span data-ttu-id="18cd0-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="18cd0-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="18cd0-141">**Microsoft Dynamics 365 Business Central – Projektit**</span><span class="sxs-lookup"><span data-stu-id="18cd0-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="18cd0-142">Projektiluettelo</span><span class="sxs-lookup"><span data-stu-id="18cd0-142">Job List</span></span>
- <span data-ttu-id="18cd0-143">Projektin suunnittelurivit</span><span class="sxs-lookup"><span data-stu-id="18cd0-143">Job Planning Lines</span></span>
- <span data-ttu-id="18cd0-144">Projektitehtävärivit</span><span class="sxs-lookup"><span data-stu-id="18cd0-144">Job Task Lines</span></span>

<span data-ttu-id="18cd0-145">**Microsoft Dynamics 365 Business Central – Asiakasluettelo**</span><span class="sxs-lookup"><span data-stu-id="18cd0-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="18cd0-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="18cd0-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="18cd0-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="18cd0-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="18cd0-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="18cd0-149">SalesDashboard</span></span>
- <span data-ttu-id="18cd0-150">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="18cd0-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="18cd0-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="18cd0-152">**Microsoft Dynamics 365 Business Central – Nimikeluettelo**</span><span class="sxs-lookup"><span data-stu-id="18cd0-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="18cd0-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="18cd0-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="18cd0-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="18cd0-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="18cd0-156">Nimikkeet</span><span class="sxs-lookup"><span data-stu-id="18cd0-156">Items</span></span>
- <span data-ttu-id="18cd0-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="18cd0-157">SalesDashboard</span></span>
- <span data-ttu-id="18cd0-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="18cd0-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="18cd0-159">**Microsoft Dynamics 365 Business Central – Toimittajaluettelo**</span><span class="sxs-lookup"><span data-stu-id="18cd0-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="18cd0-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="18cd0-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="18cd0-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="18cd0-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="18cd0-163">Nimikkeet</span><span class="sxs-lookup"><span data-stu-id="18cd0-163">Items</span></span>
- <span data-ttu-id="18cd0-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="18cd0-164">SalesDashboard</span></span>
- <span data-ttu-id="18cd0-165">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="18cd0-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="18cd0-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="18cd0-167">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="18cd0-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="18cd0-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="18cd0-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="18cd0-169">WWW-palvelut</span><span class="sxs-lookup"><span data-stu-id="18cd0-169">Web Services</span></span>
<span data-ttu-id="18cd0-170">Verkkopalveluja voi etsiä kätevästi hakemalla [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in verkkopalveluja.</span><span class="sxs-lookup"><span data-stu-id="18cd0-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="18cd0-171">Varmista, että edellä mainittujen verkkopalvelujen Julkaise-ruutu on valittu luettelossa.</span><span class="sxs-lookup"><span data-stu-id="18cd0-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="18cd0-172">Vianetsintä</span><span class="sxs-lookup"><span data-stu-id="18cd0-172">Troubleshooting</span></span>
<span data-ttu-id="18cd0-173">Power BI:n koontinäyttö käyttää julkaistuja yllä mainittuja WWW-palveluita. Koontinäytössä ovat esittely-yrityksen tiedot tai oman yrityksesi tiedot, jos toit tiedot nykyisestä rahoitusratkaisustasi.</span><span class="sxs-lookup"><span data-stu-id="18cd0-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="18cd0-174">Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.</span><span class="sxs-lookup"><span data-stu-id="18cd0-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="18cd0-175">Virheellinen yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="18cd0-175">Incorrect Company Name</span></span>  
<span data-ttu-id="18cd0-176">Yleinen virhe on antaa yrityksen näyttönimi yrityksen nimen sijaan.</span><span class="sxs-lookup"><span data-stu-id="18cd0-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="18cd0-177">Voit etsiä yrityksen nimen hakusanalla **Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="18cd0-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="18cd0-178">Anna sitten yrityksen nimi **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="18cd0-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="18cd0-179">Virheellinen käyttäjänimi ja salasana</span><span class="sxs-lookup"><span data-stu-id="18cd0-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="18cd0-180">Yhdistämiseen on käytettävä käyttäjänimeä ja salasanaa, joilla muodostetaan yhteys Microsoft Office 365 -tiliin.</span><span class="sxs-lookup"><span data-stu-id="18cd0-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="18cd0-181">Sisältöpaketit edellyttävät myös, että sinulla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tili.</span><span class="sxs-lookup"><span data-stu-id="18cd0-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="18cd0-182">Kun olet antanut tunnistetietosi, järjestelmä havaitsee automaattisesti ne Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -vuokraajat, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="18cd0-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="18cd0-183">Jos sinulla ei ole Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tilin käyttöoikeutta tai kokeiluversiota, saat virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="18cd0-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="18cd0-184">Avain ei vastannut mitään taulukon riviä</span><span class="sxs-lookup"><span data-stu-id="18cd0-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="18cd0-185">Jos annat yhteydenmuodostusprosessin aikana yrityksen nimen, joka ei ole sallittu, näyttöön voi tulla Avain ei vastannut mitään taulukon riviä -virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="18cd0-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="18cd0-186">Anna oikea yrityksen nimi ja yritä muodostaa yhteys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="18cd0-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="18cd0-187">Katso myös</span><span class="sxs-lookup"><span data-stu-id="18cd0-187">See Also</span></span>
[<span data-ttu-id="18cd0-188">Power BI:n käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="18cd0-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="18cd0-189">[Power BI – peruskäsitteet](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span><span class="sxs-lookup"><span data-stu-id="18cd0-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="18cd0-190">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="18cd0-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="18cd0-191">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="18cd0-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="18cd0-192">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="18cd0-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="18cd0-193">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="18cd0-193">Finance</span></span>](finance.md)  
<span data-ttu-id="18cd0-194">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in raportoinnin määrittäminen Power BI:ssä](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="18cd0-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

