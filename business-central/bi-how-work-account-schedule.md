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
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: fi-fi
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="b27fb-103">KP-raporttimallien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="b27fb-103">Work with Account Schedules</span></span>
<span data-ttu-id="b27fb-104">Saat KP-raporttimallien avulla tietoja tilikarttaan sisältyvistä kirjanpitotiedoista.</span><span class="sxs-lookup"><span data-stu-id="b27fb-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="b27fb-105">KP-raporttimallit analysoivat kirjanpitotilien lukuja ja vertaavat pääkirjanpidon tapahtumia pääkirjanpidon budjettitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="b27fb-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="b27fb-106">Tulokset näkyvät roolikeskuksen kaavioissa, kuten kassavirtakaaviossa.</span><span class="sxs-lookup"><span data-stu-id="b27fb-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b27fb-107"> sisältää käyttövalmiita KP-raporttimalleja. Voit myös määrittää itse verrattavat luvut määrittämällä omat rivit ja sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="b27fb-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="b27fb-108">Voit esimerkiksi luoda KP-raporttimalleja katteen laskemista varten erilaisille dimensioille, kuten osastoille tai asiakasryhmille.</span><span class="sxs-lookup"><span data-stu-id="b27fb-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="b27fb-109">Voit luoda niin monta mukautettua rahoituslaskelmaa kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="b27fb-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="b27fb-110">KP-raporttimallien määrittäminen vaatii tilikartan taloustietojen ymmärtämistä.</span><span class="sxs-lookup"><span data-stu-id="b27fb-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="b27fb-111">Voit esimerkiksi tarkastella pääkirjanpidon tapahtumia budjettitapahtumien prosenttiosuuksina.</span><span class="sxs-lookup"><span data-stu-id="b27fb-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="b27fb-112">Tämä edellyttää, että budjetit on luotu.</span><span class="sxs-lookup"><span data-stu-id="b27fb-112">This requires that budgets are created.</span></span> <span data-ttu-id="b27fb-113">Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="b27fb-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="b27fb-114">Tililuokat ja KP-raporttimallit</span><span class="sxs-lookup"><span data-stu-id="b27fb-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="b27fb-115">Tililuokkien avulla voit muuttaa rahoituslaskelmien asettelua.</span><span class="sxs-lookup"><span data-stu-id="b27fb-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="b27fb-116">Kun olet määrittänyt tililuokat **KP-tilin luokat** -ikkunassa ja valinnut **Luo KP-raporttimallit** -toiminnon, tärkeimpien rahoituslaskelmien perustana olevat KP-raporttimallit päivitetään.</span><span class="sxs-lookup"><span data-stu-id="b27fb-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="b27fb-117">Kun seuraavan kerran suoritat jonkin näistä raporteista, uudet kokonaissummat ja korvaustapahtumat lisätään muutosten perusteella.</span><span class="sxs-lookup"><span data-stu-id="b27fb-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="b27fb-118">Lisätietoja on kohdassa [Pääkirjanpito ja tilikartta](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="b27fb-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="b27fb-119">Uuden KP-raporttimallin luominen</span><span class="sxs-lookup"><span data-stu-id="b27fb-119">To create new account schedules</span></span>  
 <span data-ttu-id="b27fb-120">KP-raporttimallien käyttäminen kirjanpitotilien lukujen analysoimista varten tai pääkirjanpidon tapahtumien vertaamiseksi pääkirjanpidon budjettitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="b27fb-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="b27fb-121">Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista.</span><span class="sxs-lookup"><span data-stu-id="b27fb-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="b27fb-122">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b27fb-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b27fb-123">Valitse **KP-raporttimallien nimet** -ikkunassa **Uusi**-toiminto ja luo uusi KP-raporttimallin nimi.</span><span class="sxs-lookup"><span data-stu-id="b27fb-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="b27fb-124">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="b27fb-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="b27fb-125">Valitse **Muokkaa KP-raporttimallia** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b27fb-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="b27fb-126">Täytä **KP-raporttimalli** -ikkunan kentät tarpeesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="b27fb-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="b27fb-127">Kun olet luonut uuden KP-raporttimallin ja määrittänyt rivit sinun täytyy määrittää sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="b27fb-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="b27fb-128">Voit joko määrittää ne manuaalisesti tai liittää ennalta määrätyn sarakeasettelun KP-raporttimalliisi.</span><span class="sxs-lookup"><span data-stu-id="b27fb-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="b27fb-129">Valitse **Muokkaa sarakeasetuksia** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b27fb-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="b27fb-130">Täytä **Sarakeasettelu**-ikkunan kentät tarpeesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="b27fb-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b27fb-131">Jos KP-raporttimallin sarakeasettelun oletusarvoa ei määritetty, sarakkeet on määritettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="b27fb-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="b27fb-132">Prosenttilukuja laskevan sarakkeen luominen</span><span class="sxs-lookup"><span data-stu-id="b27fb-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="b27fb-133">Joskus haluat ehkä sisällyttää KP-raporttimalliin sarakkeen, joka laskee prosenttiluvut kokonaissummasta.</span><span class="sxs-lookup"><span data-stu-id="b27fb-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="b27fb-134">Jos esimerkiksi eri rivit jakavat myynnin dimensioittain, voit lisätä sarakkeen, joka ilmoittaa kunkin rivin prosenttiosuuden kokonaissummasta.</span><span class="sxs-lookup"><span data-stu-id="b27fb-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="b27fb-135">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b27fb-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="b27fb-136">Valitse **KP-raporttimallien nimet** -ikkunassa KP-raporttimalli.</span><span class="sxs-lookup"><span data-stu-id="b27fb-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="b27fb-137">Valitse **Muokkaa KP-raporttimallia** -toiminto, jos haluat määrittää KP-raporttimallin rivin, joka laskee prosenttilukujen perustana olevan kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="b27fb-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="b27fb-138">Lisää KP-raporttimalli-ikkunaan rivi välittömästi ensimmäisen sellaisen rivin yläpuolelle, jolla haluat näyttää prosenttiluvun.</span><span class="sxs-lookup"><span data-stu-id="b27fb-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="b27fb-139">Täytä rivin kentät seuraavasti: valitse **Summaustyyppi**-kenttään **Määritä prosentin perusta**.</span><span class="sxs-lookup"><span data-stu-id="b27fb-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="b27fb-140">Anna **Yhteensä**-kentässä kaava, jonka laskemaan kokonaissummaan prosenttiarvo perustuu.</span><span class="sxs-lookup"><span data-stu-id="b27fb-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="b27fb-141">Jos esimerkiksi rivi 11 sisältää kokonaismyynnin, syötä **11**.</span><span class="sxs-lookup"><span data-stu-id="b27fb-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="b27fb-142">Valitse **Muokkaa sarakeasetuksia** -toiminto, kun haluat määrittää sarakkeen.</span><span class="sxs-lookup"><span data-stu-id="b27fb-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="b27fb-143">Täytä rivin kentät seuraavasti: valitse **Saraketyyppi**-kenttään **Kaava**.</span><span class="sxs-lookup"><span data-stu-id="b27fb-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="b27fb-144">Anna **Kaava**-kenttään sen summan kaava, jolle haluat laskea prosentin, ja sen perää %-merkki.</span><span class="sxs-lookup"><span data-stu-id="b27fb-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="b27fb-145">Jos esimerkiksi sarake N sisältää nettomuutoksen, syötä **N %**.</span><span class="sxs-lookup"><span data-stu-id="b27fb-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="b27fb-146">Toista vaiheet 4-7 kullekin riviryhmälle, jonka haluat jakaa prosenttiluvun mukaan.</span><span class="sxs-lookup"><span data-stu-id="b27fb-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="b27fb-147">KP-raporttimallien määrittäminen käyttäen yleiskuvauksia</span><span class="sxs-lookup"><span data-stu-id="b27fb-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="b27fb-148">KP-raporttimallin käyttäminen pääkirjanpidon lukuja ja pääkirjanpidon budjettilukuja vertaavan laskelman luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="b27fb-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="b27fb-149">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b27fb-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="b27fb-150">Valitse **KP-raporttimallien nimet** -ikkunassa KP-raporttimalli.</span><span class="sxs-lookup"><span data-stu-id="b27fb-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="b27fb-151">Valitse **Muokkaa KP-raporttimallia** -toiminto</span><span class="sxs-lookup"><span data-stu-id="b27fb-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="b27fb-152">Valitse **KP-raporttimalli** -ikkunan **Nimi**-kentässä haluamasi KP-raporttimallin nimi.</span><span class="sxs-lookup"><span data-stu-id="b27fb-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="b27fb-153">Valitse **Syötä tilit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b27fb-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="b27fb-154">Valitse tilit, joita haluat ilmoitukseesi ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="b27fb-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="b27fb-155">Tilit on nyt lisätty KP-raporttimalliin.</span><span class="sxs-lookup"><span data-stu-id="b27fb-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="b27fb-156">Halutessasi voit myös muuttaa sarakeasettelua.</span><span class="sxs-lookup"><span data-stu-id="b27fb-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="b27fb-157">Valitse **Yleiskuvaus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b27fb-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="b27fb-158">Valitse **Dimensiosuodattimet**-pikavälilehti ja määritä Budjettisuodatus-kentässä haluamasi suodattimen nimi.</span><span class="sxs-lookup"><span data-stu-id="b27fb-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="b27fb-159">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="b27fb-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="b27fb-160">Nyt voit kopioida ja liittää budjettierittelyn laskentataulukkoon.</span><span class="sxs-lookup"><span data-stu-id="b27fb-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="b27fb-161">Kirjanpitojaksojen vertaaminen käyttäen jakson kaavoja</span><span class="sxs-lookup"><span data-stu-id="b27fb-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="b27fb-162">KP-raporttimalli voi verrata eri kirjanpitojaksojen tuloksia, kuten tämän kuun tuloksia edellisen vuoden saman kuukauden tuloksiin.</span><span class="sxs-lookup"><span data-stu-id="b27fb-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="b27fb-163">Voit tehdä tämän lisäämällä sarakkeen, jossa on **Vertailujakson laskukaava** -kenttä ja sitten määrittämällä kentän arvoksi jakson kaava.</span><span class="sxs-lookup"><span data-stu-id="b27fb-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="b27fb-164">Kirjanpitojakson ei tarvitse vastata kalenteria, mutta jokaisessa tilikaudessa on oltava sama määrä kirjanpitojaksoja, vaikka jaksot voivatkin olla eripituisia.</span><span class="sxs-lookup"><span data-stu-id="b27fb-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b27fb-165"> laskee jakson kaavan avulla vertailujakson summan suhteessa raporttipyynnön päivämääräsuodattimen jaksoon.</span><span class="sxs-lookup"><span data-stu-id="b27fb-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="b27fb-166">Vertailujakso perustuu päivämääräsuodatuksen aloituspäivämäärän jaksoon.</span><span class="sxs-lookup"><span data-stu-id="b27fb-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="b27fb-167">Jaksomääritysten lyhenteet ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="b27fb-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b27fb-168">Lyhenne</span><span class="sxs-lookup"><span data-stu-id="b27fb-168">Abbreviation</span></span></th>
<th><span data-ttu-id="b27fb-169">Description</span><span class="sxs-lookup"><span data-stu-id="b27fb-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b27fb-170">J</span><span class="sxs-lookup"><span data-stu-id="b27fb-170">P</span></span></p></td>
<td><p><span data-ttu-id="b27fb-171">Jakso</span><span class="sxs-lookup"><span data-stu-id="b27fb-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27fb-172">VJ</span><span class="sxs-lookup"><span data-stu-id="b27fb-172">LP</span></span></p></td>
<td><p><span data-ttu-id="b27fb-173">Tilikauden, puolen vuoden tai neljänneksen viimeinen jakso.</span><span class="sxs-lookup"><span data-stu-id="b27fb-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27fb-174">NJ</span><span class="sxs-lookup"><span data-stu-id="b27fb-174">CP</span></span></p></td>
<td><p><span data-ttu-id="b27fb-175">Tilikauden, puolen vuoden tai neljänneksen nykyinen jakso.</span><span class="sxs-lookup"><span data-stu-id="b27fb-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27fb-176">TK</span><span class="sxs-lookup"><span data-stu-id="b27fb-176">FY</span></span></p></td>
<td><p><span data-ttu-id="b27fb-177">Tilikausi.</span><span class="sxs-lookup"><span data-stu-id="b27fb-177">Fiscal year.</span></span> <span data-ttu-id="b27fb-178">Esimerkiksi TK[1..3] tarkoittaa kuluvan tilikauden ensimmäistä neljännestä.</span><span class="sxs-lookup"><span data-stu-id="b27fb-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b27fb-179">Esimerkkejä kaavoista:</span><span class="sxs-lookup"><span data-stu-id="b27fb-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b27fb-180">Kaava</span><span class="sxs-lookup"><span data-stu-id="b27fb-180">Formula</span></span></th>
<th><span data-ttu-id="b27fb-181">Description</span><span class="sxs-lookup"><span data-stu-id="b27fb-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b27fb-182">&lt;Tyhjä&gt;</span><span class="sxs-lookup"><span data-stu-id="b27fb-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="b27fb-183">Nykyinen jakso</span><span class="sxs-lookup"><span data-stu-id="b27fb-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27fb-184">-1J</span><span class="sxs-lookup"><span data-stu-id="b27fb-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="b27fb-185">Edellinen jakso</span><span class="sxs-lookup"><span data-stu-id="b27fb-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27fb-186">-1TK[1..EJ]</span><span class="sxs-lookup"><span data-stu-id="b27fb-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="b27fb-187">Koko edellinen tilikausi</span><span class="sxs-lookup"><span data-stu-id="b27fb-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27fb-188">-1TK</span><span class="sxs-lookup"><span data-stu-id="b27fb-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="b27fb-189">Nykyinen jakso edellisenä tilikautena</span><span class="sxs-lookup"><span data-stu-id="b27fb-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27fb-190">-1TK[1..3]</span><span class="sxs-lookup"><span data-stu-id="b27fb-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="b27fb-191">Edellisen tilikauden ensimmäinen vuosineljännes</span><span class="sxs-lookup"><span data-stu-id="b27fb-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27fb-192">-1TK[1..NJ]</span><span class="sxs-lookup"><span data-stu-id="b27fb-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="b27fb-193">Edellisen tilikauden alusta lähtien, edellisen tilikauden nykyiseen jaksoon asti, se mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="b27fb-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27fb-194">-1TK[NJ..EJ]</span><span class="sxs-lookup"><span data-stu-id="b27fb-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="b27fb-195">Edellisen tilikauden nykyisestä jaksosta alkaen, aina edellisen tilikauden viimeiseen jaksoon asti, se mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="b27fb-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b27fb-196">Jos haluat laskea tavallisten jaksojen mukaan, syötä kaava sen sijaan **Vertailu pvm -kaava** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="b27fb-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="b27fb-197">Ei ole aina selvää, mitä kausia vertailet, koska voit asettaa päivämääräsuodatuksen raportille, joka sijoittuu eri päivämääräväleille kuin kirjanpitojaksot, jotka näkyvät tilikartan tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="b27fb-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="b27fb-198">Voit esimerkiksi luoda KP-raporttimallin, jossa haluat verrata tätä jaksoa edellisen vuoden samaan jaksoon siten, että määrität **Vertailun päivämääräjakson suodatus** -kentän arvoksi *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="b27fb-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="b27fb-199">Tämän jälkeen raportti suoritetaan helmikuun 28. päivä ja määrität päivämääräsuodatukseksi tammikuun ja helmikuun.</span><span class="sxs-lookup"><span data-stu-id="b27fb-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="b27fb-200">Tämän tuloksena KP-raporttimalli vertaa tämän vuoden tammikuuta ja helmikuuta edellisen vuoden tammikuuhun, joka on ainut viime vuonna valmistuneesta kirjanpitojaksosta.</span><span class="sxs-lookup"><span data-stu-id="b27fb-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="b27fb-201">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b27fb-201">See Also</span></span>
[<span data-ttu-id="b27fb-202">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="b27fb-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="b27fb-203">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="b27fb-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="b27fb-204">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b27fb-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="b27fb-205">Pääkirjanpito ja tilikartta</span><span class="sxs-lookup"><span data-stu-id="b27fb-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="b27fb-206">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b27fb-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

