---
title: Business Central -tietojen mukautettujen Power BI -raporttien näyttäminen | Microsoft Docs
description: Power BI -raporttien avulla saadaan lisätietoja luetteloissa olevista tiedoista.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777514"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="381ad-103">[!INCLUDE[prod_short](includes/prod_short.md)]in luettelotiedot näyttävien Power BI -raporttien luominen</span><span class="sxs-lookup"><span data-stu-id="381ad-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="381ad-104">sisältää Power BI -tietoruudun ohjausobjektielementin monilla tärkeillä luettelosivuilla.</span><span class="sxs-lookup"><span data-stu-id="381ad-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="381ad-105">Tietoruudun tarkoitus on näyttää Power BI -raportteja, jotka liittyvät luetteloissa oleviin tietueisiin. Tällä tavoin tiedoista saadaan parempi käsitys.</span><span class="sxs-lookup"><span data-stu-id="381ad-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="381ad-106">Ajatuksena on, että kun luettelon riveillä siirrytään, raportti päivitetään ja suodatetaan valitun tapahtuman mukaan.</span><span class="sxs-lookup"><span data-stu-id="381ad-106">The idea is that as you move between rows in the list, the report is updated and filtered for the selected entry.</span></span>

<span data-ttu-id="381ad-107">Osa näistä raporteista toimitetaan [!INCLUDE[prod_long](includes/prod_long.md)]in mukana.</span><span class="sxs-lookup"><span data-stu-id="381ad-107">[!INCLUDE[prod_long](includes/prod_long.md)] comes ready with some of these reports.</span></span> <span data-ttu-id="381ad-108">Lisäksi tässä tietoruudussa näytettäväksi voi luoda omia mukautettuja raportteja.</span><span class="sxs-lookup"><span data-stu-id="381ad-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="381ad-109">Näiden raporttien luonti muistuttaa muiden raporttien luontia.</span><span class="sxs-lookup"><span data-stu-id="381ad-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="381ad-110">On kuitenkin muutamia suunnittelusääntöjä, joita noudattamalla voidaan varmistaa, että raportit näkyvät odotetusti.</span><span class="sxs-lookup"><span data-stu-id="381ad-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="381ad-111">Näitä sääntöjä käsitellään tässä artikkelissa.</span><span class="sxs-lookup"><span data-stu-id="381ad-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="381ad-112">Yleisiä tietoja Business Centralin Power BI -raporttien luomisesta ja julkaisemisesta on kohdassa [Power BI -raporttien muodostaminen näyttämään [!INCLUDE [prod_long](includes/prod_long.md)] -tietoja](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="381ad-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="381ad-113">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="381ad-113">Prerequisites</span></span>

- <span data-ttu-id="381ad-114">Power BI -tili.</span><span class="sxs-lookup"><span data-stu-id="381ad-114">A Power BI account.</span></span>
- <span data-ttu-id="381ad-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="381ad-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="381ad-116">Raportin luominen luettelosivulle</span><span class="sxs-lookup"><span data-stu-id="381ad-116">Create a report for a list page</span></span>

1. <span data-ttu-id="381ad-117">Käynnistä Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="381ad-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="381ad-118">Valitse **Hae tiedot** ja aloita raportin tietolähteen valitseminen.</span><span class="sxs-lookup"><span data-stu-id="381ad-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="381ad-119">Tässä vaiheessa määritetään Business Centralin luettelosivut, jotka sisältävät raportissa käytettävät tiedot.</span><span class="sxs-lookup"><span data-stu-id="381ad-119">In this step, you specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="381ad-120">Esimerkiksi myyntiluetteloa koskevaa raporttia luotaessa on varmistettava, että tietojoukko sisältää myyntiin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="381ad-120">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>

    <span data-ttu-id="381ad-121">Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen tietolähteenä Power BI Desktopissa](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="381ad-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="381ad-122">Määritä raporttisuodatin.</span><span class="sxs-lookup"><span data-stu-id="381ad-122">Set the report filter.</span></span>

    <span data-ttu-id="381ad-123">Lisäämällä suodatin raporttiin voidaan varmistaa, että tiedot päivittävät valitun tietueen luettelossa.</span><span class="sxs-lookup"><span data-stu-id="381ad-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="381ad-124">Suodattimessa on oltava sen tietolähteen kenttä, jota käytetään luettelon kunkin tietueen yksilöivään tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="381ad-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="381ad-125">Kehittäjät kutsuvat tätä kenttää *perusavaimeksi*.</span><span class="sxs-lookup"><span data-stu-id="381ad-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="381ad-126">Useimmissa tapauksissa luettelon perusavain on **Nro**</span><span class="sxs-lookup"><span data-stu-id="381ad-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="381ad-127">-kentässä.</span><span class="sxs-lookup"><span data-stu-id="381ad-127">field.</span></span>

    <span data-ttu-id="381ad-128">Määritä suodatin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="381ad-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="381ad-129">Valitse **Suodattimet**-kohdassa perusavainkenttä käytettävissä olevien kenttien luettelosta.</span><span class="sxs-lookup"><span data-stu-id="381ad-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="381ad-130">Vedä kenttä **Suodattimet**-ruutuun ja pudota se **Suodattimet kaikilla sivuilla** -ruutuun.</span><span class="sxs-lookup"><span data-stu-id="381ad-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="381ad-131">Määritä **suodattimen tyypiksi** **Perussuodatus**.</span><span class="sxs-lookup"><span data-stu-id="381ad-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="381ad-132">Se ei voi olla sivu, visualisointi tai lisäsuodatus.</span><span class="sxs-lookup"><span data-stu-id="381ad-132">It can't be page, visual, or advanced filter.</span></span>

    ![Myyntilaskuaktiviteetti-raportin raporttisuodattimen määrittäminen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="381ad-134">Suunnittele raportin asettelu.</span><span class="sxs-lookup"><span data-stu-id="381ad-134">Design the report layout.</span></span>

    <span data-ttu-id="381ad-135">Luo suunnittelu vetämällä kenttiä ja lisäämällä visualisointeja.</span><span class="sxs-lookup"><span data-stu-id="381ad-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="381ad-136">Lisätietoja on Power BI -dokumentaation kohdassa [Raporttinäkymän käyttäminen Power BI Desktopissa](/power-bi/create-reports/desktop-report-view).</span><span class="sxs-lookup"><span data-stu-id="381ad-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="381ad-137">Seuraavissa osissa on tietoja raportin koon muuttamisesta ja useiden sivujen käyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="381ad-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="381ad-138">Tallenna raportti ja anne sille nimi.</span><span class="sxs-lookup"><span data-stu-id="381ad-138">Save and name the report.</span></span>

    <span data-ttu-id="381ad-139">On tärkeää, että raportin nimi raporttiin liitetyn luettelosivun nimen.</span><span class="sxs-lookup"><span data-stu-id="381ad-139">It's important to give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="381ad-140">Jos raportti koskee esimerkiksi **Nimikkeet**-luettelosivua, nimessä on oltava sana *nimike*.</span><span class="sxs-lookup"><span data-stu-id="381ad-140">For example, if the report is for the **Items** list page, include the word *items* somewhere in the name.</span></span>  

    <span data-ttu-id="381ad-141">Tätä nimeämiskäytäntöä ei ole pakko noudattaa.</span><span class="sxs-lookup"><span data-stu-id="381ad-141">This naming convention isn't a requirement.</span></span> <span data-ttu-id="381ad-142">Se kuitenkin nopeuttaa raporttien valitsemista [!INCLUDE[prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="381ad-142">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="381ad-143">Jos raportin valintasivu avautuu luettelosivulta, se suodatetaan automaattisesti sivun nimen mukaan.</span><span class="sxs-lookup"><span data-stu-id="381ad-143">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="381ad-144">Tämän suodatuksen avulla voidaan rajoittaa näytettävien raporttien määrää.</span><span class="sxs-lookup"><span data-stu-id="381ad-144">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="381ad-145">Tyhjentämällä suodattimen käyttäjät saavat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista.</span><span class="sxs-lookup"><span data-stu-id="381ad-145">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="381ad-146">Kun olet valmis, julkaise raportti tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="381ad-146">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="381ad-147">Lisätietoja on kohdassa [Raportin julkaiseminen](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="381ad-147">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="381ad-148">Testaa raporttia.</span><span class="sxs-lookup"><span data-stu-id="381ad-148">Test the report.</span></span>

    <span data-ttu-id="381ad-149">Kun raportti on julkaistu työtilaan, sitä pitäisi voida käyttää Power BI -tietoruudusta [!INCLUDE[prod_short](includes/prod_short.md)]in luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="381ad-149">Once the reports been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="381ad-150">Testaa seuraavasti, että näin on:</span><span class="sxs-lookup"><span data-stu-id="381ad-150">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="381ad-151">Avaa [!INCLUDE[prod_short](includes/prod_short.md)] ja siirry luettelosivulle.</span><span class="sxs-lookup"><span data-stu-id="381ad-151">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="381ad-152">Jos Power BI -tietoruutu ei ole näkyvissä, valitse siinä tapauksessa toimintorivillä **Toiminnot** > **Näytä** > **Näytä tai piilota Power BI -raportit**.</span><span class="sxs-lookup"><span data-stu-id="381ad-152">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="381ad-153">Valitse Power BI -tietoruudussa ensin **Valitse raportit**, sitten raportin **Ota käyttöön** -ruutu ja lopuksi **OK**.</span><span class="sxs-lookup"><span data-stu-id="381ad-153">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="381ad-154">Oikein suunniteltu raportti tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="381ad-154">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="381ad-155">Raportin koon ja värin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="381ad-155">Set the report size and color</span></span>

<span data-ttu-id="381ad-156">Raportin kooksi on määritettävä 325 x 310 kuvapistettä.</span><span class="sxs-lookup"><span data-stu-id="381ad-156">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="381ad-157">Koon avulla raportti voidaan skaalata oikein Power BI:n tietoruutuohjausobjektin sallimassa tilassa [!INCLUDE[prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="381ad-157">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="381ad-158">Voit määrittää raportin koon viemällä kohdistuksen raportin asettelualueen ulkopuolelle ja valitsemalla maalitelakuvakkeen.</span><span class="sxs-lookup"><span data-stu-id="381ad-158">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Myyntilaskuaktiviteetti-raportin leveyden ja korkeuden määrittäminen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="381ad-160">Voit muuttaa raportin leveyttä ja korkeutta valitsemalla **Tyyppi**-kentässä **Mukautettu**.</span><span class="sxs-lookup"><span data-stu-id="381ad-160">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="381ad-161">Jos haluat, että raportin tausta sulautuu Power BI:n tietoruutuohjausobjektin taustaväriin, määritä raportin taustaväriksi *#FFFFFF* (valkoinen).</span><span class="sxs-lookup"><span data-stu-id="381ad-161">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="381ad-162">Muodosta [!INCLUDE [prod_short](includes/prod_short.md)] -teematiedoston avulla raportteja, joissa on käytössä sama värityyli kuin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="381ad-162">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="381ad-163">Lisätietoja on kohdassa [[!INCLUDE [prod_short](includes/prod_short.md)] -raportin teema](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="381ad-163">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="381ad-164">Useita sivuja sisältävät raportit</span><span class="sxs-lookup"><span data-stu-id="381ad-164">Reports with multiple pages</span></span>

<span data-ttu-id="381ad-165">Voit luoda Power BI:ssa yhden raportin, jossa on useita sivuja.</span><span class="sxs-lookup"><span data-stu-id="381ad-165">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="381ad-166">Jos raportissa kuitenkin näytetään luettelosivuja, useamman kuin yhden sivun käyttö ei ole suositeltavaa.</span><span class="sxs-lookup"><span data-stu-id="381ad-166">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="381ad-167">Power BI -tietoruudussa näkyy vain raportin ensimmäinen sivu.</span><span class="sxs-lookup"><span data-stu-id="381ad-167">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="381ad-168">Ongelmien korjaaminen</span><span class="sxs-lookup"><span data-stu-id="381ad-168">Fixing problems</span></span>

<span data-ttu-id="381ad-169">Tässä osassa on ohjeet sellaisten ongelmien korjaamiseen, joita voi esiintyä yritettäessä näyttää [!INCLUDE[prod_short](includes/prod_short.md)]in luettelosivun Power BI -raporttia.</span><span class="sxs-lookup"><span data-stu-id="381ad-169">This section provides instructions about how to fix problems that you might run into when trying to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="381ad-170">Power BI -tietoruutu ei näy luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="381ad-170">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="381ad-171">Power BI -tietoruutu on oletusarvoisesti piilotettu.</span><span class="sxs-lookup"><span data-stu-id="381ad-171">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="381ad-172">Tietoruudun voi näyttää sivulla valitsemalla toimintorivillä **Toiminnot** > **Näytä** > **Näytä tai piilota Power BI -raportit**.</span><span class="sxs-lookup"><span data-stu-id="381ad-172">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="381ad-173">Raportti ei ole näkyvissä Valitse raportti -ruudussa</span><span class="sxs-lookup"><span data-stu-id="381ad-173">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="381ad-174">Tämä johtuu luultavasti siitä, että raportin nimi ei sisällä näytettävän luettelosivun nimeä.</span><span class="sxs-lookup"><span data-stu-id="381ad-174">It's probably because the report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="381ad-175">Saat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista tyhjentämällä suodattimen.</span><span class="sxs-lookup"><span data-stu-id="381ad-175">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="381ad-176">Raportti ladataan, mutta se jää tyhjäksi, sitä ei suodateta tai se suodatetaan virheellisesti</span><span class="sxs-lookup"><span data-stu-id="381ad-176">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="381ad-177">Tarkista, että raportin suodattimessa on oikea perusavain.</span><span class="sxs-lookup"><span data-stu-id="381ad-177">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="381ad-178">Useimmissa tapauksissa se on **Nro**-kenttä,</span><span class="sxs-lookup"><span data-stu-id="381ad-178">In most cases, this field is the **No.**</span></span> <span data-ttu-id="381ad-179">mutta esimerkiksi **KP-tapahtuma**-kentässä on käytettävä **Tapahtumanro**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="381ad-179">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="381ad-180">Raportti ladataan, mutta siinä ei näy odotettua sivua.</span><span class="sxs-lookup"><span data-stu-id="381ad-180">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="381ad-181">Tarkista, että sivu, jonka haluat näkyvän, on raportin ensimmäinen sivu.</span><span class="sxs-lookup"><span data-stu-id="381ad-181">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="381ad-182">Raportissa on tarpeettomat harmaat rajat tai se on liian pieni tai liian suuri</span><span class="sxs-lookup"><span data-stu-id="381ad-182">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="381ad-183">Tarkista, että raportin kooksi on määritetty 325 x 310 kuvapistettä.</span><span class="sxs-lookup"><span data-stu-id="381ad-183">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="381ad-184">Tallenna raportti ja päivitä sitten luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="381ad-184">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="381ad-185">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="381ad-185">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="381ad-186">Katso myös</span><span class="sxs-lookup"><span data-stu-id="381ad-186">See Also</span></span>

[<span data-ttu-id="381ad-187">Yritystietojen ottaminen käyttöön Power BI:tä varten</span><span class="sxs-lookup"><span data-stu-id="381ad-187">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="381ad-188">[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="381ad-188">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="381ad-189">Valmistautuminen liiketoimintaan</span><span class="sxs-lookup"><span data-stu-id="381ad-189">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="381ad-190">[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="381ad-190">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="381ad-191">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="381ad-191">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]