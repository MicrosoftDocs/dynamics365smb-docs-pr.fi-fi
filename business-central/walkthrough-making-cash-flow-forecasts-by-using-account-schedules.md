---
title: Vaihekuvaus – Kassavirtaennusteiden tekeminen KP-raporttimallien avulla | Microsoft Docs
description: Tässä vaihekuvauksessa kuvataan, kuinka KP-raporttimallin avulla voit tehdä kassavirtaennusteita. KP-raporttimallit suorittavat laskutoimituksia, joita ei voi tehdä suoraan kassavirtakaavioihin. KP-raporttimalleissa voidaan määrittää välisummat kassavirtavastaanottoja ja suorituksia varten. Nämä välisummat voidaan sisällyttää uusiin kokonaissummiin, joita voidaan sitten käyttää kassavirtaennusteita tehtäessä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 70f1e51a0cd2c1b6c90ca3d76013fb3a5f30f80e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314842"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="6ce6a-106">Vaihekuvaus: tehdään kassavirtaennusteita käyttäen KP-raporttimalleja</span><span class="sxs-lookup"><span data-stu-id="6ce6a-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="6ce6a-107">Tässä vaihekuvauksessa kuvataan, kuinka KP-raporttimallin avulla voit tehdä kassavirtaennusteita.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="6ce6a-108">KP-raporttimallit suorittavat laskutoimituksia, joita ei voi tehdä suoraan kassavirtakaavioihin.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="6ce6a-109">KP-raporttimalleissa voidaan määrittää välisummat kassavirtavastaanottoja ja suorituksia varten.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="6ce6a-110">Nämä välisummat voidaan sisällyttää uusiin kokonaissummiin, joita voidaan sitten käyttää kassavirtaennusteita tehtäessä.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="6ce6a-111">Tietoja tästä vaihekuvauksesta</span><span class="sxs-lookup"><span data-stu-id="6ce6a-111">About This Walkthrough</span></span>  
<span data-ttu-id="6ce6a-112">Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="6ce6a-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="6ce6a-113">Uuden kassavirran KP-raporttimallin nimen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="6ce6a-114">Uuden KP-raporttimallin rivien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="6ce6a-115">Uuden sarakkeen asettelun määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="6ce6a-116">Sarakeasettelun määritys KP-raporttimalliin.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="6ce6a-117">Tarkastellaan ja tulostetaan kassavirtaennustetta.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="6ce6a-118">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="6ce6a-118">Prerequisites</span></span>  
<span data-ttu-id="6ce6a-119">Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6ce6a-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6ce6a-120">on asennettu.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-120">installed.</span></span>  
- <span data-ttu-id="6ce6a-121">Kassavirran rivit on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="6ce6a-122">Roolit</span><span class="sxs-lookup"><span data-stu-id="6ce6a-122">Roles</span></span>  
<span data-ttu-id="6ce6a-123">Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="6ce6a-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="6ce6a-124">Valvoja</span><span class="sxs-lookup"><span data-stu-id="6ce6a-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="6ce6a-125">Taustatietoja</span><span class="sxs-lookup"><span data-stu-id="6ce6a-125">Story</span></span>  
<span data-ttu-id="6ce6a-126">Ken on CRONUS -päällikkö, joka tekee kuukausittaisia kassavirtaennusteita.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="6ce6a-127">Hän sisällyttää ennusteeseen rahoituksen, myynnin, oston ja käyttöomaisuuden ja esittelee ennusteen talousjohtaja Saaralle liiketoiminnan kuva selkeyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="6ce6a-128">Uuden KP-raporttimallin nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6ce6a-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="6ce6a-129">KP-raporttimalli koostuu kassavirran KP-raporttimallin nimestä, jossa on sarja rivejä ja sarakeasettelu.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="6ce6a-130">Uuden KP-raporttimallin nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6ce6a-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="6ce6a-131">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **KP-raporttimallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6ce6a-132">Valitse **KP-raporttimallien nimet** -sivulla **Uusi**-toiminto ja luo uuden kassavirran KP-raporttimallin nimi.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="6ce6a-133">Syötä **Nimi**-kenttään **Ennuste**.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="6ce6a-134">Kirjoita **Kuvaus**-kenttään **Kassavirtaennuste**.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="6ce6a-135">Älä täytä **Sarakeasettelun oletusarvo**- ja **Analyysinäkymän nimi** -kenttiä.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="6ce6a-136">Uuden KP-raporttimallin rivien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6ce6a-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="6ce6a-137">Kun KP-raporttimallin nimi on määritetty, Ken määrittää jokaisen rivin, joka näkyy kassavirran KP-raporttimallissa.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="6ce6a-138">Ken määrittää rivit, jotka voidaan näyttää raporteissa niiden rivien lisäksi, jotka on tarkoitettu vain laskentaan.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="6ce6a-139">Määritä KP-raporttimallin rivit</span><span class="sxs-lookup"><span data-stu-id="6ce6a-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="6ce6a-140">Valitse **KP-raporttimallien nimet** -sivulla uusi **Ennuste**-KP-raporttimallin nimi, jonka loit.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="6ce6a-141">Valitse **Kotisivu**-välilehden **Käsittely**-ryhmässä **Muokkaa KP-raporttimallia**.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="6ce6a-142">Anna **KP-raporttimallien nimet** -sivulla kukin rivi täsmälleen seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-142">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6ce6a-143">Käyttämällä **Lisää kassavirtatilit** -toimintoa, voit nopeasti merkitä kassavirtatilit kassavairtatilikartallta ja kopioida ne KP-raporttimallin riveille.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="6ce6a-144">Rivinro</span><span class="sxs-lookup"><span data-stu-id="6ce6a-144">Row No.</span></span>|<span data-ttu-id="6ce6a-145">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6ce6a-145">Description</span></span>|<span data-ttu-id="6ce6a-146">Summaustyyppi</span><span class="sxs-lookup"><span data-stu-id="6ce6a-146">Totaling Type</span></span>|<span data-ttu-id="6ce6a-147">Summausväli</span><span class="sxs-lookup"><span data-stu-id="6ce6a-147">Totaling</span></span>|<span data-ttu-id="6ce6a-148">Rivityyppi</span><span class="sxs-lookup"><span data-stu-id="6ce6a-148">Row Type</span></span>|<span data-ttu-id="6ce6a-149">Summatyyppi</span><span class="sxs-lookup"><span data-stu-id="6ce6a-149">Amount Type</span></span>|<span data-ttu-id="6ce6a-150">Näytä</span><span class="sxs-lookup"><span data-stu-id="6ce6a-150">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="6ce6a-151">C10</span><span class="sxs-lookup"><span data-stu-id="6ce6a-151">C10</span></span>|<span data-ttu-id="6ce6a-152">Summa</span><span class="sxs-lookup"><span data-stu-id="6ce6a-152">Amount</span></span>|<span data-ttu-id="6ce6a-153">Nettomuutos</span><span class="sxs-lookup"><span data-stu-id="6ce6a-153">Net Change</span></span>|<span data-ttu-id="6ce6a-154">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="6ce6a-154">Entries</span></span>|<span data-ttu-id="6ce6a-155">Nettosumma</span><span class="sxs-lookup"><span data-stu-id="6ce6a-155">Net Amount</span></span>|<span data-ttu-id="6ce6a-156">Aina</span><span class="sxs-lookup"><span data-stu-id="6ce6a-156">Always</span></span>|  
    |<span data-ttu-id="6ce6a-157">C20</span><span class="sxs-lookup"><span data-stu-id="6ce6a-157">C20</span></span>|<span data-ttu-id="6ce6a-158">Summa päivämäärään</span><span class="sxs-lookup"><span data-stu-id="6ce6a-158">Amount until Date</span></span>|<span data-ttu-id="6ce6a-159">Saldo pvm:ttäin</span><span class="sxs-lookup"><span data-stu-id="6ce6a-159">Balance at Date</span></span>|<span data-ttu-id="6ce6a-160">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="6ce6a-160">Entries</span></span>|<span data-ttu-id="6ce6a-161">Nettosumma</span><span class="sxs-lookup"><span data-stu-id="6ce6a-161">Net Amount</span></span>|<span data-ttu-id="6ce6a-162">Aina</span><span class="sxs-lookup"><span data-stu-id="6ce6a-162">Always</span></span>|  
    |<span data-ttu-id="6ce6a-163">C30</span><span class="sxs-lookup"><span data-stu-id="6ce6a-163">C30</span></span>|<span data-ttu-id="6ce6a-164">Koko tilikausi</span><span class="sxs-lookup"><span data-stu-id="6ce6a-164">Entire Fiscal Year</span></span>|<span data-ttu-id="6ce6a-165">Koko tilikausi</span><span class="sxs-lookup"><span data-stu-id="6ce6a-165">Entire Fiscal Year</span></span>|<span data-ttu-id="6ce6a-166">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="6ce6a-166">Entries</span></span>|<span data-ttu-id="6ce6a-167">Nettosumma</span><span class="sxs-lookup"><span data-stu-id="6ce6a-167">Net Amount</span></span>|<span data-ttu-id="6ce6a-168">Aina</span><span class="sxs-lookup"><span data-stu-id="6ce6a-168">Always</span></span>|  

4.  <span data-ttu-id="6ce6a-169">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-169">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="6ce6a-170">Sarakeasettelun määritys KP-raporttimallin nimeen</span><span class="sxs-lookup"><span data-stu-id="6ce6a-170">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="6ce6a-171">Ken on nyt valmis määrittämään sarakeasettelun KP-raporttimallin nimeen.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-171">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="6ce6a-172">Määritä sarakeasettelu KP-raporttimallin nimeen.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-172">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="6ce6a-173">Valitse **KP-raporttimallien nimet** -sivun **Nimi**-kentässä **Ennuste**.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-173">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="6ce6a-174">Valitse **Sarakeasettelun oletusarvo** -kentässä **Kassavirta**-sarakeasettelu oletussarakeasetteluksi.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-174">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="6ce6a-175">Tarkastele ja tulosta kassavirtaennuste</span><span class="sxs-lookup"><span data-stu-id="6ce6a-175">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="6ce6a-176">Valitse **KP-raporttimallien nimet** -sivulla **Yleiskuvaus** ja tarkastele kassavirtaennustetta.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-176">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="6ce6a-177">**KP-raporttimallin yleiskuvaus** -sivulla voit valita summan ja näyttää sitten kassavirran tuotantoennustetapahtumat, joista summa muodostuu.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-177">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="6ce6a-178">Lisäksi voit tarkastella laskentakaavaa, jota käytetään summan laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-178">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="6ce6a-179">Voit myös suodattaa määrät dimension ja päivämäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-179">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="6ce6a-180">Tulosta kassavirtaennuste valitsemalla **Tulosta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-180">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ce6a-181">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6ce6a-181">See Also</span></span>  
 <span data-ttu-id="6ce6a-182">[KP-raporttimallien käyttäminen](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="6ce6a-182">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="6ce6a-183">Liiketoimintaprosessien vaihekuvaukset</span><span class="sxs-lookup"><span data-stu-id="6ce6a-183">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="6ce6a-184">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ce6a-184">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
