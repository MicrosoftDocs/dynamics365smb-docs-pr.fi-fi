---
title: "Valuutan vaihtokurssien päivittäminen| Microsoft Docs"
description: "Voit käyttää yrityksessä useita valuuttoja määrittämällä kullekin valuutalle koodin ja käyttämällä ulkoista vaihtokurssipalvelua, kuten Yahoota."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="fa784-103">Toimintaohje: Valuutan vaihtokurssien päivittäminen</span><span class="sxs-lookup"><span data-stu-id="fa784-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="fa784-104">Kaikille valuutoille täytyy määrittää koodi, jos yritys ostaa tai myy käyttäen jotain muuta valuuttaa kuin paikallista valuuttaa, jos yrityksellä on myyntisaamisia tai ostovelkoja muissa valuutoissa; tai jos yritys tallentaa KP-kauppatapahtumia eri valuuttoina.</span><span class="sxs-lookup"><span data-stu-id="fa784-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="fa784-105">Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**.</span><span class="sxs-lookup"><span data-stu-id="fa784-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="fa784-106">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="fa784-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="fa784-107">Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="fa784-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="fa784-108">Yahoon valuutanvaihtokurssit -palvelu on asennettu valmiiksi ja odottaa käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="fa784-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="fa784-109">Valuutanvaihdon kurssipalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fa784-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="fa784-110">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Valuutanvaihtokurssipalvelut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fa784-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="fa784-111">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="fa784-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="fa784-112">Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="fa784-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="fa784-113">Ota palvelu käyttöön valitsemalla **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="fa784-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="fa784-114">Valuutan vaihtokurssien päivittäminen palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="fa784-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="fa784-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Valuutat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fa784-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="fa784-116">Valitse **Päivitä valuutan vaihtokurssit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="fa784-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="fa784-117">**Valuutat**-ikkunan **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.</span><span class="sxs-lookup"><span data-stu-id="fa784-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa784-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fa784-118">See Also</span></span>
[<span data-ttu-id="fa784-119">Vuosien ja jaksojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="fa784-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="fa784-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fa784-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

