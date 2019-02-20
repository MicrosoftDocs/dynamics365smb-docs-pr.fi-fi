---
title: "Valuutan vaihtokurssien päivittäminen| Microsoft Docs"
description: "Voit käyttää yrityksessä useita valuuttoja määrittämällä kullekin valuutalle koodin ja käyttämällä ulkoista vaihtokurssipalvelua."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: fi-fi
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a><span data-ttu-id="639d8-103">Valuutan vaihtokurssien päivittäminen</span><span class="sxs-lookup"><span data-stu-id="639d8-103">Update Currency Exchange Rates</span></span>
<span data-ttu-id="639d8-104">Yritysten toiminnan sijoittuessa yhä useamman maan/alueen alueelle niiden on entistä tärkeämpää pystyä tekemään kauppaa ja raportoimaan taloustiedot useana valuuttana.</span><span class="sxs-lookup"><span data-stu-id="639d8-104">As companies operate in increasingly more countries/regions, it becomes more important that they be able to trade and report financials in more than one currency.</span></span> <span data-ttu-id="639d8-105">Kaikille valuutoille täytyy määrittää koodi, jos yritys ostaa tai myy käyttäen jotain muuta valuuttaa kuin paikallista valuuttaa, jos yrityksellä on myyntisaamisia tai ostovelkoja muissa valuutoissa; tai jos yritys tallentaa KP-kauppatapahtumia eri valuuttoina.</span><span class="sxs-lookup"><span data-stu-id="639d8-105">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>

<span data-ttu-id="639d8-106">Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA), mutta voit määrittää sen käyttämään myös toista valuuttaa, jolle määritetään ajantasainen vaihtokurssi.</span><span class="sxs-lookup"><span data-stu-id="639d8-106">Your general ledger is set up to use your local currency (LCY), but you can set it up to also use another currency with a current exchange rate assigned.</span></span> <span data-ttu-id="639d8-107">Kun toinen valuutta määritetään niin sanotuksi lisäraportointivaluutaksi, [!INCLUDE[d365fin](includes/d365fin_md.md)] tallentaa summat automaattisesti sekä PVA:na että lisäraportointivaluuttana kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="639d8-107">By designating a second currency as a so-called additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and other entries, such as VAT entries.</span></span> <span data-ttu-id="639d8-108">Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="639d8-108">For more information, see [Set Up an Additional Reporting Currency](finance-how-setup-additional-currencies.md).</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="639d8-109">Vaihtokurssien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="639d8-109">Adjusting Exchange Rates</span></span>
<span data-ttu-id="639d8-110">Koska vaihtokurssit vaihtelevat jatkuvasti, järjestelmän lisävaluutta-arvot on tarkistettava jaksoittain.</span><span class="sxs-lookup"><span data-stu-id="639d8-110">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="639d8-111">Jos tarkistuksia ei tehdä, ulkomaisista valuutoista (tai lisävaluutoista) muunnetut summat voivat olla harhaanjohtavia, kun ne kirjataan pääkirjanpitoon PVA:na.</span><span class="sxs-lookup"><span data-stu-id="639d8-111">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="639d8-112">Lisäksi päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin lisäämistä ohjelmaan, on päivitettävä, kun päivittäinen vaihtokurssi on lisätty.</span><span class="sxs-lookup"><span data-stu-id="639d8-112">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="639d8-113">Muuta vaihtokursseja -eräajon avulla voi muuttaa kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja.</span><span class="sxs-lookup"><span data-stu-id="639d8-113">The Adjust Exchange Rates batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="639d8-114">Sen avulla voi myös päivittää KP-tapahtumien lisäraportointivaluutan summia.</span><span class="sxs-lookup"><span data-stu-id="639d8-114">It can also update additional reporting currency amounts on G/L entries.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="639d8-115">Valuutanvaihdon kurssipalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="639d8-115">To set up a currency exchange rate service</span></span>
<span data-ttu-id="639d8-116">Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun, kuten FloatRatesin avulla.</span><span class="sxs-lookup"><span data-stu-id="639d8-116">You can use an external service to keep your currency exchange rates up to date, such as FloatRates.</span></span>

1. <span data-ttu-id="639d8-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutanvaihtokurssipalvelut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="639d8-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="639d8-118">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="639d8-118">Choose the **New** action.</span></span>
3. <span data-ttu-id="639d8-119">Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="639d8-119">On the **Currency Exchange Rate Service** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="639d8-120">Ota palvelu käyttöön valitsemalla **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="639d8-120">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="639d8-121">Valuutan vaihtokurssien päivittäminen palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="639d8-121">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="639d8-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="639d8-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="639d8-123">Valitse **Päivitä valuutan vaihtokurssit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="639d8-123">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="639d8-124">**Valuutat**-sivun **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.</span><span class="sxs-lookup"><span data-stu-id="639d8-124">The value in the **Exchange Rate** field on the **Currencies** page is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="639d8-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="639d8-125">See Also</span></span>
[<span data-ttu-id="639d8-126">Lisäraportointivaluutan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="639d8-126">Set Up an Additional Reporting Currency</span></span>](finance-how-setup-additional-currencies.md)  
[<span data-ttu-id="639d8-127">Vuosien ja jaksojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="639d8-127">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="639d8-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="639d8-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

