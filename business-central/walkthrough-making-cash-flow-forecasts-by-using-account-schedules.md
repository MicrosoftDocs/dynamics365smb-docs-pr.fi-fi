---
title: Vaihekuvaus – Kassavirtaennusteiden tekeminen KP-raporttimallien avulla | Microsoft Docs
description: Tässä vaihekuvauksessa kuvataan, kuinka KP-raporttimallin avulla voit tehdä kassavirtaennusteita. KP-raporttimallit suorittavat laskutoimituksia, joita ei voi tehdä suoraan kassavirtakaavioihin. KP-raporttimalleissa voidaan määrittää välisummat kassavirtavastaanottoja ja suorituksia varten. Nämä välisummat voidaan sisällyttää uusiin kokonaissummiin, joita voidaan sitten käyttää kassavirtaennusteita tehtäessä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 13086d536bb1c2ea3b67c3e11d1327b045a2e744
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876917"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="c2103-106">Vaihekuvaus: tehdään kassavirtaennusteita käyttäen KP-raporttimalleja</span><span class="sxs-lookup"><span data-stu-id="c2103-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="c2103-107">Tässä vaihekuvauksessa kuvataan, kuinka KP-raporttimallin avulla voit tehdä kassavirtaennusteita.</span><span class="sxs-lookup"><span data-stu-id="c2103-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="c2103-108">KP-raporttimallit suorittavat laskutoimituksia, joita ei voi tehdä suoraan kassavirtakaavioihin.</span><span class="sxs-lookup"><span data-stu-id="c2103-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="c2103-109">KP-raporttimalleissa voidaan määrittää välisummat kassavirtavastaanottoja ja suorituksia varten.</span><span class="sxs-lookup"><span data-stu-id="c2103-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="c2103-110">Nämä välisummat voidaan sisällyttää uusiin kokonaissummiin, joita voidaan sitten käyttää kassavirtaennusteita tehtäessä.</span><span class="sxs-lookup"><span data-stu-id="c2103-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="c2103-111">Tietoja tästä vaihekuvauksesta</span><span class="sxs-lookup"><span data-stu-id="c2103-111">About This Walkthrough</span></span>  
<span data-ttu-id="c2103-112">Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="c2103-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="c2103-113">Uuden kassavirran KP-raporttimallin nimen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="c2103-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="c2103-114">Uuden KP-raporttimallin rivien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="c2103-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="c2103-115">Uuden sarakkeen asettelun määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="c2103-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="c2103-116">Sarakeasettelun määritys KP-raporttimalliin.</span><span class="sxs-lookup"><span data-stu-id="c2103-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="c2103-117">Tarkastellaan ja tulostetaan kassavirtaennustetta.</span><span class="sxs-lookup"><span data-stu-id="c2103-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="c2103-118">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="c2103-118">Prerequisites</span></span>  
<span data-ttu-id="c2103-119">Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:</span><span class="sxs-lookup"><span data-stu-id="c2103-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="c2103-120">on asennettu.</span><span class="sxs-lookup"><span data-stu-id="c2103-120">installed.</span></span>  
- <span data-ttu-id="c2103-121">Kassavirran rivit on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="c2103-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="c2103-122">Roolit</span><span class="sxs-lookup"><span data-stu-id="c2103-122">Roles</span></span>  
<span data-ttu-id="c2103-123">Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="c2103-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="c2103-124">Valvoja</span><span class="sxs-lookup"><span data-stu-id="c2103-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="c2103-125">Taustatietoja</span><span class="sxs-lookup"><span data-stu-id="c2103-125">Story</span></span>  
<span data-ttu-id="c2103-126">Ken on CRONUS -päällikkö, joka tekee kuukausittaisia kassavirtaennusteita.</span><span class="sxs-lookup"><span data-stu-id="c2103-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="c2103-127">Hän sisällyttää ennusteeseen rahoituksen, myynnin, oston ja käyttöomaisuuden ja esittelee ennusteen talousjohtaja Saaralle liiketoiminnan kuva selkeyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="c2103-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="c2103-128">Uuden KP-raporttimallin nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2103-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="c2103-129">KP-raporttimalli koostuu kassavirran KP-raporttimallin nimestä, jossa on sarja rivejä ja sarakeasettelu.</span><span class="sxs-lookup"><span data-stu-id="c2103-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="c2103-130">Uuden KP-raporttimallin nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2103-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="c2103-131">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **KP-raporttimallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="c2103-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c2103-132">Valitse **KP-raporttimallien nimet** -sivulla **Uusi**-toiminto ja luo uuden kassavirran KP-raporttimallin nimi.</span><span class="sxs-lookup"><span data-stu-id="c2103-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="c2103-133">Syötä **Nimi**-kenttään **Ennuste**.</span><span class="sxs-lookup"><span data-stu-id="c2103-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="c2103-134">Kirjoita **Kuvaus**-kenttään **Kassavirtaennuste**.</span><span class="sxs-lookup"><span data-stu-id="c2103-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="c2103-135">Älä täytä **Sarakeasettelun oletusarvo**- ja **Analyysinäkymän nimi** -kenttiä.</span><span class="sxs-lookup"><span data-stu-id="c2103-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="c2103-136">Uuden KP-raporttimallin rivien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2103-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="c2103-137">Kun KP-raporttimallin nimi on määritetty, Ken määrittää jokaisen rivin, joka näkyy kassavirran KP-raporttimallissa.</span><span class="sxs-lookup"><span data-stu-id="c2103-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="c2103-138">Ken määrittää rivit, jotka voidaan näyttää raporteissa niiden rivien lisäksi, jotka on tarkoitettu vain laskentaan.</span><span class="sxs-lookup"><span data-stu-id="c2103-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="c2103-139">Määritä KP-raporttimallin rivit</span><span class="sxs-lookup"><span data-stu-id="c2103-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="c2103-140">Valitse **KP-raporttimallien nimet** -sivulla luomasi uuden **Ennusteen** KP-raporttimallin nimi ja valitse sitten **Muokkaa KP-raporttimallia** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c2103-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created, and then choose the **Edit Account Schedule** action.</span></span>  
2.  <span data-ttu-id="c2103-141">Anna **KP-raporttimallien nimet** -sivulla kukin rivi täsmälleen seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="c2103-141">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c2103-142">Käyttämällä **Lisää kassavirtatilit** -toimintoa, voit nopeasti merkitä kassavirtatilit kassavairtatilikartallta ja kopioida ne KP-raporttimallin riveille.</span><span class="sxs-lookup"><span data-stu-id="c2103-142">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="c2103-143">Rivinro</span><span class="sxs-lookup"><span data-stu-id="c2103-143">Row No.</span></span>|<span data-ttu-id="c2103-144">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="c2103-144">Description</span></span>|<span data-ttu-id="c2103-145">Summaustyyppi</span><span class="sxs-lookup"><span data-stu-id="c2103-145">Totaling Type</span></span>|<span data-ttu-id="c2103-146">Summausväli</span><span class="sxs-lookup"><span data-stu-id="c2103-146">Totaling</span></span>|<span data-ttu-id="c2103-147">Rivityyppi</span><span class="sxs-lookup"><span data-stu-id="c2103-147">Row Type</span></span>|<span data-ttu-id="c2103-148">Summatyyppi</span><span class="sxs-lookup"><span data-stu-id="c2103-148">Amount Type</span></span>|<span data-ttu-id="c2103-149">Näytä</span><span class="sxs-lookup"><span data-stu-id="c2103-149">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="c2103-150">C10</span><span class="sxs-lookup"><span data-stu-id="c2103-150">C10</span></span>|<span data-ttu-id="c2103-151">Summa</span><span class="sxs-lookup"><span data-stu-id="c2103-151">Amount</span></span>|<span data-ttu-id="c2103-152">Nettomuutos</span><span class="sxs-lookup"><span data-stu-id="c2103-152">Net Change</span></span>|<span data-ttu-id="c2103-153">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="c2103-153">Entries</span></span>|<span data-ttu-id="c2103-154">Nettosumma</span><span class="sxs-lookup"><span data-stu-id="c2103-154">Net Amount</span></span>|<span data-ttu-id="c2103-155">Aina</span><span class="sxs-lookup"><span data-stu-id="c2103-155">Always</span></span>|  
    |<span data-ttu-id="c2103-156">C20</span><span class="sxs-lookup"><span data-stu-id="c2103-156">C20</span></span>|<span data-ttu-id="c2103-157">Summa päivämäärään</span><span class="sxs-lookup"><span data-stu-id="c2103-157">Amount until Date</span></span>|<span data-ttu-id="c2103-158">Saldo pvm:ttäin</span><span class="sxs-lookup"><span data-stu-id="c2103-158">Balance at Date</span></span>|<span data-ttu-id="c2103-159">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="c2103-159">Entries</span></span>|<span data-ttu-id="c2103-160">Nettosumma</span><span class="sxs-lookup"><span data-stu-id="c2103-160">Net Amount</span></span>|<span data-ttu-id="c2103-161">Aina</span><span class="sxs-lookup"><span data-stu-id="c2103-161">Always</span></span>|  
    |<span data-ttu-id="c2103-162">C30</span><span class="sxs-lookup"><span data-stu-id="c2103-162">C30</span></span>|<span data-ttu-id="c2103-163">Koko tilikausi</span><span class="sxs-lookup"><span data-stu-id="c2103-163">Entire Fiscal Year</span></span>|<span data-ttu-id="c2103-164">Koko tilikausi</span><span class="sxs-lookup"><span data-stu-id="c2103-164">Entire Fiscal Year</span></span>|<span data-ttu-id="c2103-165">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="c2103-165">Entries</span></span>|<span data-ttu-id="c2103-166">Nettosumma</span><span class="sxs-lookup"><span data-stu-id="c2103-166">Net Amount</span></span>|<span data-ttu-id="c2103-167">Aina</span><span class="sxs-lookup"><span data-stu-id="c2103-167">Always</span></span>|  

4.  <span data-ttu-id="c2103-168">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="c2103-168">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="c2103-169">Sarakeasettelun määritys KP-raporttimallin nimeen</span><span class="sxs-lookup"><span data-stu-id="c2103-169">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="c2103-170">Ken on nyt valmis määrittämään sarakeasettelun KP-raporttimallin nimeen.</span><span class="sxs-lookup"><span data-stu-id="c2103-170">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="c2103-171">Määritä sarakeasettelu KP-raporttimallin nimeen.</span><span class="sxs-lookup"><span data-stu-id="c2103-171">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="c2103-172">Valitse **KP-raporttimallien nimet** -sivun **Nimi**-kentässä **Ennuste**.</span><span class="sxs-lookup"><span data-stu-id="c2103-172">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="c2103-173">Valitse **Sarakeasettelun oletusarvo** -kentässä **Kassavirta**-sarakeasettelu oletussarakeasetteluksi.</span><span class="sxs-lookup"><span data-stu-id="c2103-173">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="c2103-174">Tarkastele ja tulosta kassavirtaennuste</span><span class="sxs-lookup"><span data-stu-id="c2103-174">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="c2103-175">Valitse **KP-raporttimallien nimet** -sivulla **Yleiskuvaus** ja tarkastele kassavirtaennustetta.</span><span class="sxs-lookup"><span data-stu-id="c2103-175">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="c2103-176">**KP-raporttimallin yleiskuvaus** -sivulla voit valita summan ja näyttää sitten kassavirran tuotantoennustetapahtumat, joista summa muodostuu.</span><span class="sxs-lookup"><span data-stu-id="c2103-176">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="c2103-177">Lisäksi voit tarkastella laskentakaavaa, jota käytetään summan laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="c2103-177">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="c2103-178">Voit myös suodattaa määrät dimension ja päivämäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="c2103-178">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="c2103-179">Tulosta kassavirtaennuste valitsemalla **Tulosta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="c2103-179">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2103-180">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c2103-180">See Also</span></span>  
 <span data-ttu-id="c2103-181">[KP-raporttimallien käyttäminen](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="c2103-181">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="c2103-182">Liiketoimintaprosessien vaihekuvaukset</span><span class="sxs-lookup"><span data-stu-id="c2103-182">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="c2103-183">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2103-183">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
