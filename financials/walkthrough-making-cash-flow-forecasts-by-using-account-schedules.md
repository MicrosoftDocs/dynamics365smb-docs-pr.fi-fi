---
title: "Vaihekuvaus – Kassavirtaennusteiden tekeminen KP-raporttimallien avulla | Microsoft Docs"
description: "Tässä vaihekuvauksessa kuvataan, kuinka KP-raporttimallin avulla voit tehdä kassavirtaennusteita. KP-raporttimallit suorittavat laskutoimituksia, joita ei voi tehdä suoraan kassavirtakaavioihin. KP-raporttimalleissa voidaan määrittää välisummat kassavirtavastaanottoja ja suorituksia varten. Nämä välisummat voidaan sisällyttää uusiin kokonaissummiin, joita voidaan sitten käyttää kassavirtaennusteita tehtäessä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 25319bae1d601d6beddca35cf8edc032ac11eda6
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="95627-106">Vaihekuvaus: tehdään kassavirtaennusteita käyttäen KP-raporttimalleja</span><span class="sxs-lookup"><span data-stu-id="95627-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="95627-107">Tässä vaihekuvauksessa kuvataan, kuinka KP-raporttimallin avulla voit tehdä kassavirtaennusteita.</span><span class="sxs-lookup"><span data-stu-id="95627-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="95627-108">KP-raporttimallit suorittavat laskutoimituksia, joita ei voi tehdä suoraan kassavirtakaavioihin.</span><span class="sxs-lookup"><span data-stu-id="95627-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="95627-109">KP-raporttimalleissa voidaan määrittää välisummat kassavirtavastaanottoja ja suorituksia varten.</span><span class="sxs-lookup"><span data-stu-id="95627-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="95627-110">Nämä välisummat voidaan sisällyttää uusiin kokonaissummiin, joita voidaan sitten käyttää kassavirtaennusteita tehtäessä.</span><span class="sxs-lookup"><span data-stu-id="95627-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="95627-111">Tietoja tästä vaihekuvauksesta</span><span class="sxs-lookup"><span data-stu-id="95627-111">About This Walkthrough</span></span>  
<span data-ttu-id="95627-112">Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="95627-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="95627-113">Uuden kassavirran KP-raporttimallin nimen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="95627-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="95627-114">Uuden KP-raporttimallin rivien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="95627-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="95627-115">Uuden sarakkeen asettelun määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="95627-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="95627-116">Sarakeasettelun määritys KP-raporttimalliin.</span><span class="sxs-lookup"><span data-stu-id="95627-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="95627-117">Tarkastellaan ja tulostetaan kassavirtaennustetta.</span><span class="sxs-lookup"><span data-stu-id="95627-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="95627-118">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="95627-118">Prerequisites</span></span>  
<span data-ttu-id="95627-119">Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:</span><span class="sxs-lookup"><span data-stu-id="95627-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="95627-120"> on asennettu.</span><span class="sxs-lookup"><span data-stu-id="95627-120">installed.</span></span>  
- <span data-ttu-id="95627-121">Kassavirran rivit on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="95627-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="95627-122">Roolit</span><span class="sxs-lookup"><span data-stu-id="95627-122">Roles</span></span>  
<span data-ttu-id="95627-123">Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="95627-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="95627-124">Valvoja</span><span class="sxs-lookup"><span data-stu-id="95627-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="95627-125">Taustatietoja</span><span class="sxs-lookup"><span data-stu-id="95627-125">Story</span></span>  
<span data-ttu-id="95627-126">Ken on CRONUSIN kirjanpitäjä, joka tekee kuukausittaiset kassavirtaennusteet.</span><span class="sxs-lookup"><span data-stu-id="95627-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="95627-127">Hän sisällyttää ennusteeseen rahoituksen, myynnin, oston ja käyttöomaisuuden ja esittelee ennusteen talousjohtaja Saaralle liiketoiminnan kuva selkeyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="95627-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="95627-128">Uuden KP-raporttimallin nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="95627-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="95627-129">KP-raporttimalli koostuu kassavirran KP-raporttimallin nimestä, jossa on sarja rivejä ja sarakeasettelu.</span><span class="sxs-lookup"><span data-stu-id="95627-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="95627-130">Uuden KP-raporttimallin nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="95627-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="95627-131">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="95627-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="95627-132">Valitse **KP-raporttimallien nimet** -ikkunassa **Uusi**-toiminto ja luo uuden kassavirran KP-raporttimallin nimi.</span><span class="sxs-lookup"><span data-stu-id="95627-132">In the **Account Schedule Names** window, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="95627-133">Syötä **Nimi**-kenttään **Ennuste**.</span><span class="sxs-lookup"><span data-stu-id="95627-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="95627-134">Kirjoita **Kuvaus**-kenttään **Kassavirtaennuste**.</span><span class="sxs-lookup"><span data-stu-id="95627-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="95627-135">Älä täytä **Sarakeasettelun oletusarvo**- ja **Analyysinäkymän nimi** -kenttiä.</span><span class="sxs-lookup"><span data-stu-id="95627-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="95627-136">Uuden KP-raporttimallin rivien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="95627-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="95627-137">Kun KP-raporttimallin nimi on määritetty, Ken määrittää jokaisen rivin, joka näkyy kassavirran KP-raporttimallissa.</span><span class="sxs-lookup"><span data-stu-id="95627-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="95627-138">Ken määrittää rivit, jotka voidaan näyttää raporteissa niiden rivien lisäksi, jotka on tarkoitettu vain laskentaan.</span><span class="sxs-lookup"><span data-stu-id="95627-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="95627-139">Määritä KP-raporttimallin rivit</span><span class="sxs-lookup"><span data-stu-id="95627-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="95627-140">Valitse **KP-raporttimallien nimet** -ikkunassa uusi **Ennuste**-KP-raporttimallin nimi, jonka loit.</span><span class="sxs-lookup"><span data-stu-id="95627-140">In the **Account Schedule Names** window, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="95627-141">Valitse **Kotisivu**-välilehden **Käsittely**-ryhmässä **Muokkaa KP-raporttimallia**.</span><span class="sxs-lookup"><span data-stu-id="95627-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="95627-142">Anna **KP-raporttimallien nimet** -ikkunassa kukin rivi täsmälleen seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="95627-142">In the **Account Schedule** window, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="95627-143">Käyttämällä **Lisää kassavirtatilit** -toimintoa, voit nopeasti merkitä kassavirtatilit kassavairtatilikartallta ja kopioida ne KP-raporttimallin riveille.</span><span class="sxs-lookup"><span data-stu-id="95627-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="95627-144">|Rivinro|Kuvaus|Summaustyyppi|Summausväli|Rivityyppi|Summatyyppi|Näytä|</span><span class="sxs-lookup"><span data-stu-id="95627-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="95627-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Summa|Nettomuutos|Tapahtumat|Nettosumma|Aina|</span><span class="sxs-lookup"><span data-stu-id="95627-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="95627-146">|C20|Summa päivämäärään|Saldo pvm:ttäin|Tapahtumat|Nettosumma|Aina|</span><span class="sxs-lookup"><span data-stu-id="95627-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="95627-147">|C30|Koko tilikausi|Koko tilikausi|Tapahtumat|Nettosumma|Aina|</span><span class="sxs-lookup"><span data-stu-id="95627-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="95627-148">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="95627-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="95627-149">Sarakeasettelun määritys KP-raporttimallin nimeen</span><span class="sxs-lookup"><span data-stu-id="95627-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="95627-150">Ken on nyt valmis määrittämään sarakeasettelun KP-raporttimallin nimeen.</span><span class="sxs-lookup"><span data-stu-id="95627-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="95627-151">Määritä sarakeasettelu KP-raporttimallin nimeen.</span><span class="sxs-lookup"><span data-stu-id="95627-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="95627-152">Valitse **KP-raporttimallien nimet** -ikkunan **Nimi**-kentässä **Ennuste**.</span><span class="sxs-lookup"><span data-stu-id="95627-152">In the **Account Schedule Names** window, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="95627-153">Valitse **Sarakeasettelun oletusarvo** -kentässä **Kassavirta**-sarakeasettelu oletussarakeasetteluksi.</span><span class="sxs-lookup"><span data-stu-id="95627-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="95627-154">Tarkastele ja tulosta kassavirtaennuste</span><span class="sxs-lookup"><span data-stu-id="95627-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="95627-155">Valitse **KP-raporttimallien nimet** -ikkunassa **Yleiskuvaus** ja tarkastele kassavirtaennustetta.</span><span class="sxs-lookup"><span data-stu-id="95627-155">In the **Account Schedule Names** window, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="95627-156">**KP-raporttimallin yleiskuvaus** -ikkunassa voit valita summan ja näyttää sitten kassavirran tuotantoennustetapahtumat, joista summa muodostuu.</span><span class="sxs-lookup"><span data-stu-id="95627-156">In the **Acc. Schedule Overview** window, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="95627-157">Lisäksi voit tarkastella laskentakaavaa, jota käytetään summan laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="95627-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="95627-158">Voit myös suodattaa määrät dimension ja päivämäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="95627-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="95627-159">Tulosta kassavirtaennuste valitsemalla **Tulosta**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="95627-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="95627-160">Katso myös</span><span class="sxs-lookup"><span data-stu-id="95627-160">See Also</span></span>  
 <span data-ttu-id="95627-161">[KP-raporttimallien käyttäminen](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="95627-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="95627-162">Liiketoimintaprosessien vaihekuvaukset</span><span class="sxs-lookup"><span data-stu-id="95627-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="95627-163">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="95627-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

