---
title: "Luo taloudellisia raportteja KP-raporttimalleja käyttäen"
description: "Kuvailee, miten KP-raporttimalleja voidaan käyttää erilaisten näkymien ja raporttien luomiseen taloushallinnon suorituskykytietojen analysointia varten."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: fi-fi
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="1b3fa-103">Talousraportoinnin valmisteleminen KP-raporttimallien ja tililuokkien avulla</span><span class="sxs-lookup"><span data-stu-id="1b3fa-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="1b3fa-104">Saat KP-raporttimallien avulla tietoja tilikarttaan sisältyvistä kirjanpitotiedoista.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="1b3fa-105">KP-raporttimallit analysoivat kirjanpitotilien lukuja ja vertaavat pääkirjanpidon tapahtumia pääkirjanpidon budjettitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="1b3fa-106">Tulokset näkyvät roolikeskuksen kaavioissa, kuten kassavirtakaaviossa, ja raporteissa, kuten Tuloslaskelma- ja Tase-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="1b3fa-107">Voit käyttää näitä kahta raporttia esimerkiksi liiketoimintajohtajan ja kirjanpitäjän roolikeskusten **Tilinpäätökset** -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="1b3fa-108"> sisältää käyttövalmiita KP-raporttimalleja. Voit myös määrittää itse verrattavat luvut määrittämällä omat rivit ja sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-108"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="1b3fa-109">Voit esimerkiksi luoda KP-raporttimalleja katteen laskemista varten erilaisille dimensioille, kuten osastoille tai asiakasryhmille.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="1b3fa-110">Voit luoda niin monta mukautettua rahoituslaskelmaa kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="1b3fa-111">KP-raporttimallien määrittäminen vaatii tilikartan taloustietojen ymmärtämistä.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="1b3fa-112">Voit esimerkiksi tarkastella pääkirjanpidon tapahtumia budjettitapahtumien prosenttiosuuksina.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="1b3fa-113">Tämä edellyttää, että budjetit on luotu.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-113">This requires that budgets are created.</span></span> <span data-ttu-id="1b3fa-114">Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="1b3fa-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="1b3fa-115">Tililuokat ja KP-raporttimallit</span><span class="sxs-lookup"><span data-stu-id="1b3fa-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="1b3fa-116">Tililuokkien avulla voit muuttaa rahoituslaskelmien asettelua.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="1b3fa-117">Kun olet määrittänyt tililuokat **KP-tilin luokat** -ikkunassa ja valinnut **Luo KP-raporttimallit** -toiminnon, tärkeimpien rahoituslaskelmien perustana olevat KP-raporttimallit päivitetään.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="1b3fa-118">Kun seuraavan kerran suoritat toisen näistä raporteista, esimerkiksi Tase-raportin, uudet kokonaissummat ja korvaustapahtumat lisätään muutosten perusteella.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="1b3fa-119">Lisätietoja on kohdan [Tietoja pääkirjanpidosta ja tilikartasta](finance-general-ledger.md) Tililuokat-osassa.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="1b3fa-120">Uuden KP-raporttimallin luominen</span><span class="sxs-lookup"><span data-stu-id="1b3fa-120">To create new account schedules</span></span>  
 <span data-ttu-id="1b3fa-121">KP-raporttimallien käyttäminen kirjanpitotilien lukujen analysoimista varten tai pääkirjanpidon tapahtumien vertaamiseksi pääkirjanpidon budjettitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="1b3fa-122">Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="1b3fa-123">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1b3fa-124">Valitse **KP-raporttimallien nimet** -ikkunassa **Uusi**-toiminto ja luo uusi KP-raporttimallin nimi.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="1b3fa-125">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="1b3fa-126">Valitse **Muokkaa KP-raporttimallia** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="1b3fa-127">Täytä **KP-raporttimalli** -ikkunan kentät tarpeesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="1b3fa-128">Kun olet luonut uuden KP-raporttimallin ja määrittänyt rivit sinun täytyy määrittää sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="1b3fa-129">Voit joko määrittää ne manuaalisesti tai liittää ennalta määrätyn sarakeasettelun KP-raporttimalliisi.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="1b3fa-130">Valitse **Muokkaa sarakeasetuksia** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="1b3fa-131">Täytä **Sarakeasettelu**-ikkunan kentät tarpeesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="1b3fa-132">Jos KP-raporttimallin sarakeasettelun oletusarvoa ei määritetty, sarakkeet on määritettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="1b3fa-133">Olemassa olevan KP-raporttimallin kopioiminen</span><span class="sxs-lookup"><span data-stu-id="1b3fa-133">To copy an existing account schedule</span></span>
<span data-ttu-id="1b3fa-134">[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen vakioversion KP-raporttimallit perustuvat vakiotalousraportteihin, jotka eivät ehkä vastaa liiketoimintasi tarpeita.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="1b3fa-135">Voit nopeasti luoda omia talousraportteja kopioimalla olemassa olevan KP-raporttimallin.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="1b3fa-136">Valitse **KP-raporttimallit**-ikkunassa KP-raporttimalli ja valitse sitten **Kopioi KP-raporttimalli** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="1b3fa-137">Täytä **Kopioi KP-raporttimalli** -ikkunassa tarvittavat kentät ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="1b3fa-138">Prosenttilukuja laskevan sarakkeen luominen</span><span class="sxs-lookup"><span data-stu-id="1b3fa-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="1b3fa-139">Joskus haluat ehkä sisällyttää KP-raporttimalliin sarakkeen, joka laskee prosenttiluvut kokonaissummasta.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="1b3fa-140">Jos esimerkiksi eri rivit jakavat myynnin dimensioittain, voit lisätä sarakkeen, joka ilmoittaa kunkin rivin prosenttiosuuden kokonaissummasta.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="1b3fa-141">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b3fa-142">Valitse **KP-raporttimallien nimet** -ikkunassa KP-raporttimalli.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="1b3fa-143">Valitse **Muokkaa KP-raporttimallia** -toiminto, jos haluat määrittää KP-raporttimallin rivin, joka laskee prosenttilukujen perustana olevan kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="1b3fa-144">Lisää KP-raporttimalli-ikkunaan rivi välittömästi ensimmäisen sellaisen rivin yläpuolelle, jolla haluat näyttää prosenttiluvun.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="1b3fa-145">Täytä rivin kentät seuraavasti: valitse **Summaustyyppi**-kenttään **Määritä prosentin perusta**.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="1b3fa-146">Anna **Yhteensä**-kentässä kaava, jonka laskemaan kokonaissummaan prosenttiarvo perustuu.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="1b3fa-147">Jos esimerkiksi rivi 11 sisältää kokonaismyynnin, syötä **11**.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="1b3fa-148">Valitse **Muokkaa sarakeasetuksia** -toiminto, kun haluat määrittää sarakkeen.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="1b3fa-149">Täytä rivin kentät seuraavasti: valitse **Saraketyyppi**-kenttään **Kaava**.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="1b3fa-150">Anna **Kaava**-kenttään sen summan kaava, jolle haluat laskea prosentin, ja sen perää %-merkki.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="1b3fa-151">Jos esimerkiksi sarake N sisältää nettomuutoksen, syötä **N %**.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="1b3fa-152">Toista vaiheet 4-7 kullekin riviryhmälle, jonka haluat jakaa prosenttiluvun mukaan.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="1b3fa-153">KP-raporttimallien määrittäminen käyttäen yleiskuvauksia</span><span class="sxs-lookup"><span data-stu-id="1b3fa-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="1b3fa-154">KP-raporttimallin käyttäminen pääkirjanpidon lukuja ja pääkirjanpidon budjettilukuja vertaavan laskelman luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="1b3fa-155">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b3fa-156">Valitse **KP-raporttimallien nimet** -ikkunassa KP-raporttimalli.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="1b3fa-157">Valitse **Muokkaa KP-raporttimallia** -toiminto</span><span class="sxs-lookup"><span data-stu-id="1b3fa-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="1b3fa-158">Valitse **KP-raporttimalli** -ikkunan **Nimi**-kentässä haluamasi KP-raporttimallin nimi.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="1b3fa-159">Valitse **Syötä tilit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="1b3fa-160">Valitse tilit, joita haluat ilmoitukseesi ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="1b3fa-161">Tilit on nyt lisätty KP-raporttimalliin.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="1b3fa-162">Halutessasi voit myös muuttaa sarakeasettelua.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="1b3fa-163">Valitse **Yleiskuvaus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="1b3fa-164">Valitse **Dimensiosuodattimet**-pikavälilehti ja määritä Budjettisuodatus-kentässä haluamasi suodattimen nimi.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="1b3fa-165">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="1b3fa-166">Nyt voit kopioida ja liittää budjettierittelyn laskentataulukkoon.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="1b3fa-167">Kirjanpitojaksojen vertaaminen käyttäen jakson kaavoja</span><span class="sxs-lookup"><span data-stu-id="1b3fa-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="1b3fa-168">KP-raporttimalli voi verrata eri kirjanpitojaksojen tuloksia, kuten tämän kuun tuloksia edellisen vuoden saman kuukauden tuloksiin.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="1b3fa-169">Voit tehdä tämän lisäämällä sarakkeen, jossa on **Vertailujakson laskukaava** -kenttä ja sitten määrittämällä kentän arvoksi jakson kaava.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="1b3fa-170">Kirjanpitojakson ei tarvitse vastata kalenteria, mutta jokaisessa tilikaudessa on oltava sama määrä kirjanpitojaksoja, vaikka jaksot voivatkin olla eripituisia.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="1b3fa-171"> laskee jakson kaavan avulla vertailujakson summan suhteessa raporttipyynnön päivämääräsuodattimen jaksoon.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-171"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="1b3fa-172">Vertailujakso perustuu päivämääräsuodatuksen aloituspäivämäärän jaksoon.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="1b3fa-173">Jaksomääritysten lyhenteet ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="1b3fa-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b3fa-174">Lyhenne</span><span class="sxs-lookup"><span data-stu-id="1b3fa-174">Abbreviation</span></span></th>
<th><span data-ttu-id="1b3fa-175">Description</span><span class="sxs-lookup"><span data-stu-id="1b3fa-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b3fa-176">J</span><span class="sxs-lookup"><span data-stu-id="1b3fa-176">P</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-177">Jakso</span><span class="sxs-lookup"><span data-stu-id="1b3fa-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b3fa-178">VJ</span><span class="sxs-lookup"><span data-stu-id="1b3fa-178">LP</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-179">Tilikauden, puolen vuoden tai neljänneksen viimeinen jakso.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b3fa-180">NJ</span><span class="sxs-lookup"><span data-stu-id="1b3fa-180">CP</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-181">Tilikauden, puolen vuoden tai neljänneksen nykyinen jakso.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b3fa-182">TK</span><span class="sxs-lookup"><span data-stu-id="1b3fa-182">FY</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-183">Tilikausi.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-183">Fiscal year.</span></span> <span data-ttu-id="1b3fa-184">Esimerkiksi TK[1..3] tarkoittaa kuluvan tilikauden ensimmäistä neljännestä.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1b3fa-185">Esimerkkejä kaavoista:</span><span class="sxs-lookup"><span data-stu-id="1b3fa-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b3fa-186">Kaava</span><span class="sxs-lookup"><span data-stu-id="1b3fa-186">Formula</span></span></th>
<th><span data-ttu-id="1b3fa-187">Description</span><span class="sxs-lookup"><span data-stu-id="1b3fa-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b3fa-188">&lt;Tyhjä&gt;</span><span class="sxs-lookup"><span data-stu-id="1b3fa-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-189">Nykyinen jakso</span><span class="sxs-lookup"><span data-stu-id="1b3fa-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b3fa-190">-1J</span><span class="sxs-lookup"><span data-stu-id="1b3fa-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-191">Edellinen jakso</span><span class="sxs-lookup"><span data-stu-id="1b3fa-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b3fa-192">-1TK[1..EJ]</span><span class="sxs-lookup"><span data-stu-id="1b3fa-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-193">Koko edellinen tilikausi</span><span class="sxs-lookup"><span data-stu-id="1b3fa-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b3fa-194">-1TK</span><span class="sxs-lookup"><span data-stu-id="1b3fa-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-195">Nykyinen jakso edellisenä tilikautena</span><span class="sxs-lookup"><span data-stu-id="1b3fa-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b3fa-196">-1TK[1..3]</span><span class="sxs-lookup"><span data-stu-id="1b3fa-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-197">Edellisen tilikauden ensimmäinen vuosineljännes</span><span class="sxs-lookup"><span data-stu-id="1b3fa-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b3fa-198">-1TK[1..NJ]</span><span class="sxs-lookup"><span data-stu-id="1b3fa-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-199">Edellisen tilikauden alusta lähtien, edellisen tilikauden nykyiseen jaksoon asti, se mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="1b3fa-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b3fa-200">-1TK[NJ..EJ]</span><span class="sxs-lookup"><span data-stu-id="1b3fa-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="1b3fa-201">Edellisen tilikauden nykyisestä jaksosta alkaen, aina edellisen tilikauden viimeiseen jaksoon asti, se mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="1b3fa-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1b3fa-202">Jos haluat laskea tavallisten jaksojen mukaan, syötä kaava sen sijaan **Vertailu pvm -kaava** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="1b3fa-203">Ei ole aina selvää, mitä kausia vertailet, koska voit asettaa päivämääräsuodatuksen raportille, joka sijoittuu eri päivämääräväleille kuin kirjanpitojaksot, jotka näkyvät tilikartan tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="1b3fa-204">Voit esimerkiksi luoda KP-raporttimallin, jossa haluat verrata tätä jaksoa edellisen vuoden samaan jaksoon siten, että määrität **Vertailun päivämääräjakson suodatus** -kentän arvoksi *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="1b3fa-205">Tämän jälkeen raportti suoritetaan helmikuun 28. päivä ja määrität päivämääräsuodatukseksi tammikuun ja helmikuun.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="1b3fa-206">Tämän tuloksena KP-raporttimalli vertaa tämän vuoden tammikuuta ja helmikuuta edellisen vuoden tammikuuhun, joka on ainut viime vuonna valmistuneesta kirjanpitojaksosta.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="1b3fa-207">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1b3fa-207">See Also</span></span>
[<span data-ttu-id="1b3fa-208">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="1b3fa-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="1b3fa-209">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="1b3fa-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="1b3fa-210">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1b3fa-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="1b3fa-211">Pääkirjanpito ja tilikartta</span><span class="sxs-lookup"><span data-stu-id="1b3fa-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="1b3fa-212">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b3fa-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

