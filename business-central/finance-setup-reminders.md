---
title: Muistutusehtojen ja -tasojen määrittäminen.
description: Lue, miten voit määrittää Business Centralin lähettämään asiakkaalle muistutuksen erääntyvästä maksusta ja miten maksuun lisätään myöhästymismaksu.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 06853911f5b2858fbde4ff5371971c86f2960543
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783482"
---
# <a name="set-up-reminder-terms-and-levels"></a><span data-ttu-id="2fe6b-103">Muistutusehtojen ja -tasojen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-103">Set Up Reminder Terms and Levels</span></span>

<span data-ttu-id="2fe6b-104">Muistutusten avulla voit muistuttaa asiakkaita erääntyneistä summista.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-104">You can use reminders to remind customers about overdue amounts.</span></span> [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## <a name="reminder-terms"></a><span data-ttu-id="2fe6b-105">Muistutusehdot</span><span class="sxs-lookup"><span data-stu-id="2fe6b-105">Reminder terms</span></span>

<span data-ttu-id="2fe6b-106">Jos asiakkailla on erääntyneitä maksuja, sinun täytyy päättää, milloin ja miten heille lähetetään muistutus.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-106">If customers have overdue payments, you must decide when and how to send them a reminder.</span></span> <span data-ttu-id="2fe6b-107">Lisäksi saattaa olla tarpeen veloittaa heidän tileiltään korkoja tai maksuja.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-107">In addition, you may want to debit their accounts for interest or fees.</span></span> <span data-ttu-id="2fe6b-108">Muistutusehtoja voi määrittää kuinka monta tahansa.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-108">You can set up any number of reminder terms.</span></span>  

> [!NOTE]
> <span data-ttu-id="2fe6b-109">Jos haluat laskea erääntyneiden maksujen koron, voit tehdä sen muistutusten luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-109">If you want to calculate interest on overdue payments, you can do so when you create reminders.</span></span> <span data-ttu-id="2fe6b-110">Jos haluat laskea koron ja tiedottaa siitä asiakkaille lähettämättä muistutuksia, käytä [viivästyskululaskuja](finance-setup-finance-charges.md).</span><span class="sxs-lookup"><span data-stu-id="2fe6b-110">If, however, you just want to calculate interest and inform your customers about this without sending reminders, you should use [finance charge memos](finance-setup-finance-charges.md).</span></span> <span data-ttu-id="2fe6b-111">Lisätietoja on vastaavasti kohdissa [Muistutukset](receivables-collect-outstanding-balances.md#reminders) tai [Viivästyskulut](receivables-collect-outstanding-balances.md#finance-charges).</span><span class="sxs-lookup"><span data-stu-id="2fe6b-111">For more information, see [Reminders](receivables-collect-outstanding-balances.md#reminders) or [Finance Charges](receivables-collect-outstanding-balances.md#finance-charges), respectively.</span></span>

### <a name="to-set-up-reminder-terms"></a><span data-ttu-id="2fe6b-112">Muistutusehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2fe6b-112">To set up reminder terms</span></span>

1. <span data-ttu-id="2fe6b-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2fe6b-114">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-114">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="2fe6b-115">Voit käyttää useita muistutusehtoyhdistelmä, kun määrität kullekin koodin.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-115">To use more than one combination of reminder terms, set up a code for each one.</span></span>

## <a name="reminder-levels"></a><span data-ttu-id="2fe6b-116">Muistutustasot</span><span class="sxs-lookup"><span data-stu-id="2fe6b-116">Reminder levels</span></span>

<span data-ttu-id="2fe6b-117">Voit määrittää kullekin muistutusehtojen koodille rajoittamattoman määrän muistutustasoja.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-117">For each reminder terms code, you can define an unlimited number of reminder levels.</span></span> <span data-ttu-id="2fe6b-118">Kun asiakkaalle luodaan ensimmäinen muistutus, ohjelma käyttää tason 1 asetuksia.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-118">The first time a reminder is created for a customer, the setting from level 1 is used.</span></span> <span data-ttu-id="2fe6b-119">Kun muistutus lähetetään, tason numero rekisteröidään muistutustapahtumiin, jotka luodaan ja linkitetään yksittäisiin asiakastapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-119">When the reminder is issued, the level number is registered on the reminder entries that are created and linked to the individual customer ledger entries.</span></span> <span data-ttu-id="2fe6b-120">Jos asiakkaalle on tarpeen lähettää uusi muistutus, kaikki avoimiin asiakastapahtumiin linkitetyt muistutustapahtumat tarkistetaan suurimman tason numeron selvittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-120">If it is necessary to remind the customer again, all reminder entries linked to open customer ledger entries are checked to locate the highest level number.</span></span> <span data-ttu-id="2fe6b-121">Tämän jälkeen käytetään uutta muistutusta varten seuraavan tason numeron ehtoja.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-121">The conditions from the next level number will then be used for the new reminder.</span></span>

<span data-ttu-id="2fe6b-122">Jos luot enemmän muistutuksia kuin mille olet määrittänyt tasoja, ohjelma käyttää ylimmän tason ehtoja.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-122">If you create more reminders than you have defined levels for, the conditions for the highest level will be used.</span></span> <span data-ttu-id="2fe6b-123">Luotavien muistutusten enimmäismäärä määräytyy muistutusehtojen **Muistutusten enimmäislukumäärä** -kentän mukaan.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-123">You can create as many reminders as are allowed by the **Max. No of Reminders** field in the reminder terms.</span></span>

### <a name="to-set-up-reminder-levels"></a><span data-ttu-id="2fe6b-124">Muistutustasojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2fe6b-124">To set up reminder levels</span></span>

1. <span data-ttu-id="2fe6b-125">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2fe6b-126">Valitse **Muistutusehdot**-sivulla rivi, jonka ehdoille haluat määrittää tasoja, ja valitse sitten **Tasot**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-126">On the **Reminder Terms** page, select the line with the terms you want to set up levels for, and then choose **Levels** action.</span></span>  
3. <span data-ttu-id="2fe6b-127">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-127">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > <span data-ttu-id="2fe6b-128">**Laske korko** -kentän asetus määrittää, näkyykö muistutuksessa korko, kun muistutus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-128">The setting of the **Calculate Interest** field determines if interest will appear on the reminder when the reminder is issued.</span></span> <span data-ttu-id="2fe6b-129">**Muistutusehdot**-sivun **Kirjaa korko** -kenttä määrittää, kirjataanko laskettu korko KP- ja asiakastileille.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-129">However, the **Post Interest** field in the **Reminder Terms** page determines if the calculated interest must be posted to G/L and customer accounts.</span></span>
    >
    > <span data-ttu-id="2fe6b-130">Voit määrittää, että korko lasketaan, valitsemalla **Laske korko** -kentän.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-130">To indicate that interest should be calculated, choose the **Calculate Interest** field.</span></span>

    <span data-ttu-id="2fe6b-131">Jokaiselle muistutustasolle voidaan haluttaessa määrittää lisämaksuja sekä PVA:na että ulkomaan valuuttana.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-131">Optionally, for each reminder level, specify additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="2fe6b-132">Kullekin **Muistutustasot**-sivun koodille voi määrittää useita ulkomaan valuutoissa olevia lisämaksuja.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-132">You can define many additional fees in foreign currencies for each code on the **Reminder Levels** page.</span></span>  

    <span data-ttu-id="2fe6b-133">Lisämaksut voidaan laskea kolmella eri tavalla, jotka on määritelty **Lisämaksun laskentatyyppi** -kentän arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-133">The additional fees can be calculated in three different ways that are defined by the value of the **Add. Fee Calculation Type** field.</span></span>  

    - <span data-ttu-id="2fe6b-134">**Kiinteä**</span><span class="sxs-lookup"><span data-stu-id="2fe6b-134">**Fixed**</span></span>

        <span data-ttu-id="2fe6b-135">Maksut lasketaan itse muistutustasolle rivin **Lisämaksu**-kenttien arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-135">Fees are calculated based on the values of the **Additional Fee** fields on the line for the reminder level itself.</span></span>  
    - <span data-ttu-id="2fe6b-136">**Yksittäinen dynaaminen**</span><span class="sxs-lookup"><span data-stu-id="2fe6b-136">**Single Dynamic**</span></span>

        <span data-ttu-id="2fe6b-137">Maksut lasketaan kyseiselle muistutustasolle asianmukaisen rivin **Lisämaksun asetukset**-kenttien arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-137">Fees are calculated based on the values of the fields on the relevant line in the **Additional Fee Setup** page for that reminder level.</span></span>
    - <span data-ttu-id="2fe6b-138">**Kumulatiivinen dynaaminen**</span><span class="sxs-lookup"><span data-stu-id="2fe6b-138">**Accumulated Dynamic**</span></span>

        <span data-ttu-id="2fe6b-139">Maksut lasketaan kyseiselle muistutustasolle yhdistettyjen rivien **Lisämaksun asetukset** -kenttien arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-139">Fees are calculated based on the values of the fields on the combined lines in the **Additional Fee Setup** page for that reminder level.</span></span>

4. <span data-ttu-id="2fe6b-140">Valitse **Valuutat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-140">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="2fe6b-141">Määritä **Muistutustason valuutat** -sivulla jokaiselle muistutustason koodille ja vastaavalle muistutustason numerolle valuutan koodi ja lisämaksu.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-141">On the **Currencies for Reminder Levels** page, define for each reminder level code and corresponding reminder level number a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="2fe6b-142">Kun luot muistutuksia ulkomaan valuuttana, tässä määritettäviä ulkomaan valuutan ehtoja käytetään muistutusten luontiin.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-142">When you create reminders in a foreign currency, the foreign currency conditions that you set up here will be used to create reminders.</span></span> <span data-ttu-id="2fe6b-143">Jos ulkomaan valuuttojen ehtoja ei ole määritetty, käytetään **Muistutustasot**-sivulla määritettyjä PVA:n muistutusehtoja ja ne muunnetaan soveltuvaan valuuttaan.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-143">If there are no foreign currency reminder conditions set up, the LCY reminder conditions that are set up on the **Reminder Levels** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="2fe6b-144">Voit määrittää kutakin muistutustasoa varten tekstin, joka tulostetaan ennen muistutuksen merkintöjä (**Aloitusteksti**) tai niiden jälkeen (**Lopetusteksti**).</span><span class="sxs-lookup"><span data-stu-id="2fe6b-144">For each reminder level, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the reminder.</span></span>

6. <span data-ttu-id="2fe6b-145">Valitse tilanteen mukaan joko **Aloitusteksti**- tai **Lopetusteksti**-toiminto ja täytä **Muistutusteksti**-sivun tiedot.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-145">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill in the **Reminder Text** page.</span></span>
7. <span data-ttu-id="2fe6b-146">Voit lisätä liittyviä arvoja automaattisesti muistutustekstiin käyttämällä seuraavia paikkamerkkejä **Teksti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-146">To automatically insert related values in the resulting reminder text, enter the following placeholders in the **Text** field .</span></span>  

    |<span data-ttu-id="2fe6b-147">Paikkamerkki</span><span class="sxs-lookup"><span data-stu-id="2fe6b-147">Placeholder</span></span>|<span data-ttu-id="2fe6b-148">Arvo</span><span class="sxs-lookup"><span data-stu-id="2fe6b-148">Value</span></span>|  
    |-----------------|-----------|  
    |<span data-ttu-id="2fe6b-149">%1</span><span class="sxs-lookup"><span data-stu-id="2fe6b-149">%1</span></span>|<span data-ttu-id="2fe6b-150">Muistutuksen otsikon **Asiakirjan pvm** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-150">Content of the **Document Date** field on the reminder header</span></span>|  
    |<span data-ttu-id="2fe6b-151">%2</span><span class="sxs-lookup"><span data-stu-id="2fe6b-151">%2</span></span>|<span data-ttu-id="2fe6b-152">Muistutuksen otsikon **Eräpäivä** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-152">Content of the **Due Date** field on the reminder header</span></span>|  
    |<span data-ttu-id="2fe6b-153">%3</span><span class="sxs-lookup"><span data-stu-id="2fe6b-153">%3</span></span>|<span data-ttu-id="2fe6b-154">Viivästyskuluehtojen **Korko**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-154">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
    |<span data-ttu-id="2fe6b-155">%4</span><span class="sxs-lookup"><span data-stu-id="2fe6b-155">%4</span></span>|<span data-ttu-id="2fe6b-156">Muistutuksen otsikon **Jäljellä oleva summa** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-156">Content of the **Remaining Amount** field on the reminder header</span></span>|  
    |<span data-ttu-id="2fe6b-157">%5</span><span class="sxs-lookup"><span data-stu-id="2fe6b-157">%5</span></span>|<span data-ttu-id="2fe6b-158">Muistutuksen otsikon **Korkosumma**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-158">Content of the **Interest Amount** field on the reminder header</span></span>|  
    |<span data-ttu-id="2fe6b-159">%6</span><span class="sxs-lookup"><span data-stu-id="2fe6b-159">%6</span></span>|<span data-ttu-id="2fe6b-160">Muistutuksen otsikon **Lisämaksu**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-160">Content of the **Additional Fee** field on the reminder header</span></span>|  
    |<span data-ttu-id="2fe6b-161">%7</span><span class="sxs-lookup"><span data-stu-id="2fe6b-161">%7</span></span>|<span data-ttu-id="2fe6b-162">Muistutuksen kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="2fe6b-162">The total amount of the reminder</span></span>|  
    |<span data-ttu-id="2fe6b-163">%8</span><span class="sxs-lookup"><span data-stu-id="2fe6b-163">%8</span></span>|<span data-ttu-id="2fe6b-164">Muistutuksen otsikon **Muistutustaso**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-164">Content of the **Reminder Level** field on the reminder header</span></span>|  
    |<span data-ttu-id="2fe6b-165">%9</span><span class="sxs-lookup"><span data-stu-id="2fe6b-165">%9</span></span>|<span data-ttu-id="2fe6b-166">Muistutuksen otsikon **Valuutan koodi** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-166">Content of the **Currency Code** field on the reminder header</span></span>|  
    |<span data-ttu-id="2fe6b-167">%10</span><span class="sxs-lookup"><span data-stu-id="2fe6b-167">%10</span></span>|<span data-ttu-id="2fe6b-168">Muistutuksen otsikon **Kirjauspvm** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-168">Content of the **Posting Date** field on the reminder header</span></span>|  
    |<span data-ttu-id="2fe6b-169">%11</span><span class="sxs-lookup"><span data-stu-id="2fe6b-169">%11</span></span>|<span data-ttu-id="2fe6b-170">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="2fe6b-170">The company name</span></span>|  
    |<span data-ttu-id="2fe6b-171">%12</span><span class="sxs-lookup"><span data-stu-id="2fe6b-171">%12</span></span>|<span data-ttu-id="2fe6b-172">Muistutuksen otsikon **Lisämaksu riviä kohti** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="2fe6b-172">Content of the **Add. Fee per Line** field on the reminder header</span></span>|  

    <span data-ttu-id="2fe6b-173">Jos kirjoitat kenttään esimerkiksi **Velkasi on %9 %7, joka erääntyy %2**, muistutustekstiksi tulee **Velkasi on 1200,50 PVA, joka erääntyy 2.2.2014.**.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-173">For example, if you write **You owe %9 %7 due on %2.**, then the resulting reminder will contain the following text: **You owe USD 1.200,50 due on 02-02-2014.**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fe6b-174">Eräpäivä lasketaan annetun päivämääräkaavan mukaan.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-174">The due date is calculated according to the date formula that you enter.</span></span> <span data-ttu-id="2fe6b-175">Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#using-date-formulas).</span><span class="sxs-lookup"><span data-stu-id="2fe6b-175">For more information, see [Using Date Formulas](ui-enter-date-ranges.md#using-date-formulas).</span></span>

<span data-ttu-id="2fe6b-176">Kun olet määrittänyt muistutusehdot sekä lisätasot ja tekstin, määritä jokin koodeista kussakin asiakkaan kortissa.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-176">After you have set up the reminder terms, with additional levels and text, enter one of the codes on each of the customer cards.</span></span> <span data-ttu-id="2fe6b-177">Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="2fe6b-177">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="2fe6b-178">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2fe6b-178">See also</span></span>

[<span data-ttu-id="2fe6b-179">Avointen saldojen perintä</span><span class="sxs-lookup"><span data-stu-id="2fe6b-179">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="2fe6b-180">Viivästyskuluehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2fe6b-180">Set Up Finance Charge Terms</span></span>](finance-setup-finance-charges.md)  
[<span data-ttu-id="2fe6b-181">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2fe6b-181">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]