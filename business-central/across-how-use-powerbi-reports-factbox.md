---
title: Business Central -tietojen mukautettujen Power BI -raporttien näyttäminen | Microsoft Docs
description: Saat Power BI -raporttien avulla lisätietoja luetteloissa olevista tiedoista.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 04c0c5d203e78c2ae0be48609a5ee90f45b83c6f
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968383"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prodshort"></a><span data-ttu-id="ff175-103">[!INCLUDE[prodshort](includes/prodshort.md)]in luettelotiedot näyttävien Power BI -raporttien luominen</span><span class="sxs-lookup"><span data-stu-id="ff175-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

[!INCLUDE[prodlong](includes/prodlong.md)]<span data-ttu-id="ff175-104">in useilla tärkeillä luettelosivuilla on ohjausobjektina tietoruutu, jossa on lisätietoja luettelon tiedoista.</span><span class="sxs-lookup"><span data-stu-id="ff175-104">includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="ff175-105">Raportti päivitetään ja suodatetaan valitun tapahtuman mukaan, kun siirryt luettelon riveillä.</span><span class="sxs-lookup"><span data-stu-id="ff175-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="ff175-106">Voit luoda mukautettuja raportteja näyttämään tämän ohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="ff175-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="ff175-107">Raporttien toimiminen odotetusti edellyttää muutamien sääntöjen noudattamista.</span><span class="sxs-lookup"><span data-stu-id="ff175-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="ff175-108">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="ff175-108">Prerequisites</span></span>

- <span data-ttu-id="ff175-109">Power BI -tili.</span><span class="sxs-lookup"><span data-stu-id="ff175-109">A Power BI account.</span></span>
- <span data-ttu-id="ff175-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="ff175-110">Power BI Desktop.</span></span>

<span data-ttu-id="ff175-111">Lisätietoja aloittamisesta on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI -tietolähteenä](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="ff175-111">For more information about getting started, see [Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="ff175-112">Raportin tietojoukon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ff175-112">Defining the report data set</span></span>

<span data-ttu-id="ff175-113">Määritä tietolähde, joka sisältää luetteloon liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="ff175-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="ff175-114">Esimerkiksi myyntiluetteloa koskevaa raporttia luotaessa on varmistettava, että tietojoukko sisältää myyntiin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="ff175-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="ff175-115">Raporttisuodattimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ff175-115">Defining the report filter</span></span>

<span data-ttu-id="ff175-116">Lisäämällä suodatin raporttiin voidaan varmistaa, että tiedot päivittävät valitun tietueen luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ff175-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="ff175-117">Suodattimessa on oltava kenttä sen tietolähteen kenttä, jota käytetään *perusavaimena*.</span><span class="sxs-lookup"><span data-stu-id="ff175-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="ff175-118">Useimmissa tapauksissa luettelon perusavain on **Nro**</span><span class="sxs-lookup"><span data-stu-id="ff175-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="ff175-119">-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ff175-119">field.</span></span>

<span data-ttu-id="ff175-120">Voit määrittää raporttisuodattimen valitsemalla käytettävissä olevien kenttien luettelosta perusavaimen sekä vetämällä ja pudottamalla kyseisen kentän **Raporttisuodatin**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ff175-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="ff175-121">Suodattimen on oltava kaikille sivuille määritetty perusraporttisuodatin.</span><span class="sxs-lookup"><span data-stu-id="ff175-121">The filter must be a basic report filter that's defined for all pages.</span></span> <span data-ttu-id="ff175-122">Se ei voi olla sivu, visualisointi tai lisäsuodatus.</span><span class="sxs-lookup"><span data-stu-id="ff175-122">It can't be page, visual, or advanced filter.</span></span>

![Myyntilaskuaktiviteetti-raportin raporttisuodattimen määrittäminen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="ff175-124">Raportin koon ja värin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ff175-124">Setting the report size and color</span></span>

<span data-ttu-id="ff175-125">Raportin kooksi on määritettävä 325 x 310 kuvapistettä.</span><span class="sxs-lookup"><span data-stu-id="ff175-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="ff175-126">Koon avulla raportti voidaan skaalata oikein Power BI:n tietoruutuohjausobjektin sallimassa tilassa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="ff175-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ff175-127">Voit määrittää raportin koon viemällä kohdistuksen raportin asettelualueen ulkopuolelle ja valitsemalla maalitelakuvakkeen.</span><span class="sxs-lookup"><span data-stu-id="ff175-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Myyntilaskuaktiviteetti-raportin leveyden ja korkeuden määrittäminen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="ff175-129">Voit muuttaa raportin leveyttä ja korkeutta valitsemalla **Tyyppi**-kentässä **Mukautettu**.</span><span class="sxs-lookup"><span data-stu-id="ff175-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="ff175-130">Jos haluat, että raportin tausta sulautuu Power BI:n tietoruutuohjausobjektin taustaväriin, määritä raportin taustaväriksi *#FFFFFF*.</span><span class="sxs-lookup"><span data-stu-id="ff175-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="ff175-131">Useita sivuja sisältävien raporttien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="ff175-131">Using reports with multiple pages</span></span>

<span data-ttu-id="ff175-132">Voit luoda Power BI:ssa yhden raportin, jossa on useita sivuja.</span><span class="sxs-lookup"><span data-stu-id="ff175-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="ff175-133">Jos raportissa kuitenkin näytetään luettelosivuja, useamman kuin yhden sivun käyttö ei ole suositeltavaa.</span><span class="sxs-lookup"><span data-stu-id="ff175-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="ff175-134">Power BI -tietoruudussa näkyy vain raportin ensimmäinen sivu.</span><span class="sxs-lookup"><span data-stu-id="ff175-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="ff175-135">Raportin nimeäminen</span><span class="sxs-lookup"><span data-stu-id="ff175-135">Naming the report</span></span>

<span data-ttu-id="ff175-136">Anna raportille nimi, joka sisältää raporttiin liitetyn luettelosivun nimen.</span><span class="sxs-lookup"><span data-stu-id="ff175-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="ff175-137">Jos raportti koskee esimerkiksi **Toimittaja**-luettelosivua, nimessä on oltava sana *toimittaja*.</span><span class="sxs-lookup"><span data-stu-id="ff175-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="ff175-138">Tätä nimeämiskäytäntöä ei ole pakko noudattaa.</span><span class="sxs-lookup"><span data-stu-id="ff175-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="ff175-139">Se kuitenkin nopeuttaa raporttien valitsemista [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="ff175-139">However, it makes selecting reports in [!INCLUDE[d365fin](includes/d365fin_md.md)] quicker.</span></span> <span data-ttu-id="ff175-140">Jos raportin valintasivu avautuu luettelosivulta, se suodatetaan automaattisesti sivun nimen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ff175-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="ff175-141">Tämän suodatuksen avulla voidaan rajoittaa näytettävien raporttien määrää.</span><span class="sxs-lookup"><span data-stu-id="ff175-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="ff175-142">Tyhjentämällä suodattimen käyttäjät saavat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista.</span><span class="sxs-lookup"><span data-stu-id="ff175-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="ff175-143">Ongelmien korjaaminen</span><span class="sxs-lookup"><span data-stu-id="ff175-143">Fixing problems</span></span>

<span data-ttu-id="ff175-144">Tämän osan ohjeiden avulla voi kiertää tavallisimmat Power BI -raportin luomiseen liittyvät ongelmat.</span><span class="sxs-lookup"><span data-stu-id="ff175-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="ff175-145">Raportti ei ole näkyvissä Valitse raportti -sivulla</span><span class="sxs-lookup"><span data-stu-id="ff175-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="ff175-146">Syynä luultavasti se, että raportin nimi ei sisällä luettelosivun nimeä.</span><span class="sxs-lookup"><span data-stu-id="ff175-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="ff175-147">Saat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista tyhjentämällä suodattimen.</span><span class="sxs-lookup"><span data-stu-id="ff175-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="ff175-148">Raportti ladataan, mutta se jää tyhjäksi, sitä ei suodateta tai se suodatetaan virheellisesti</span><span class="sxs-lookup"><span data-stu-id="ff175-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="ff175-149">Tarkista, että raportin suodattimessa on oikea perusavain.</span><span class="sxs-lookup"><span data-stu-id="ff175-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="ff175-150">Useimmissa tapauksissa se on **Nro**-kenttä,</span><span class="sxs-lookup"><span data-stu-id="ff175-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="ff175-151">mutta esimerkiksi **KP-tapahtuma**-kentässä on käytettävä **Tapahtumanro**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="ff175-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="ff175-152">Raportti ladataan, mutta siinä ei näy odotettua sivua.</span><span class="sxs-lookup"><span data-stu-id="ff175-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="ff175-153">Tarkista, että sivu, jonka haluat näkyvän, on raportin ensimmäinen sivu.</span><span class="sxs-lookup"><span data-stu-id="ff175-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="ff175-154">Raportissa on tarpeettomat harmaat rajat tai se on liian pieni tai liian suuri</span><span class="sxs-lookup"><span data-stu-id="ff175-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="ff175-155">Tarkista, että raportin kooksi on määritetty 325 x 310 kuvapistettä.</span><span class="sxs-lookup"><span data-stu-id="ff175-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="ff175-156">Tallenna raportti ja päivitä sitten luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="ff175-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="ff175-157">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="ff175-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="ff175-158">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ff175-158">See Also</span></span>

[<span data-ttu-id="ff175-159">Yritystietojen ottaminen käyttöön Power BI:tä varten</span><span class="sxs-lookup"><span data-stu-id="ff175-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="ff175-160">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="ff175-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="ff175-161">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="ff175-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="ff175-162">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="ff175-162">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="ff175-163">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="ff175-163">Finance</span></span>](finance.md)  
