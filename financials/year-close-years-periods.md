---
title: "Tilikauden ja kirjanpitojaksojen sulkemistehtävien yleiskatsaus | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan tilikauden tai kirjanpitojakson sulkemistehtävistä, joita ovat esimerkiksi varmistaminen, että asiakirjat ja päiväkirjat on kirjattu, ja pankkitilien saldojen tarkistaminen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/07/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 937b470fb5f3837b415a81b4d3924cbd5530a52a
ms.contentlocale: fi-fi
ms.lasthandoff: 04/16/2018

---
# <a name="closing-years-and-periods"></a><span data-ttu-id="11293-103">Vuosien ja kausien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="11293-103">Closing Years and Periods</span></span>
<span data-ttu-id="11293-104">Tilikauden lopussa on suoritettava joukko hallinnollisia tehtäviä. On esimerkiksi tarkistettava, että kaikki asiakirjat ja päiväkirjat on kirjattu, valuuttatiedot ovat ajan tasalla ja kirjat on suljettu.</span><span class="sxs-lookup"><span data-stu-id="11293-104">At the end of a fiscal year, there are a number of administrative tasks that you have to perform, like making sure all documents and journals are posted, making sure currency data are up-to-date, closing the books, and more.</span></span> <span data-ttu-id="11293-105">Suoritettavat tehtävät riippuvat yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="11293-105">The actual tasks will depend your company.</span></span>

<span data-ttu-id="11293-106">Seuraava taulukko sisältää yleiskuvauksen tehtävistä, joita yleensä suoritetaan vuoden ja kauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="11293-106">The following table provides an overview of tasks that you typically perform to close a year and period.</span></span>

| <span data-ttu-id="11293-107">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="11293-107">To</span></span> | <span data-ttu-id="11293-108">Katso</span><span class="sxs-lookup"><span data-stu-id="11293-108">See</span></span> |
| --- | --- |
| <span data-ttu-id="11293-109">Määritä järjestelmänlaajuiset ja käyttäjäkohtaiset kirjauspäivämäärävälit.</span><span class="sxs-lookup"><span data-stu-id="11293-109">Specify system-wide and user-specific posting date ranges.</span></span> <span data-ttu-id="11293-110">Liiketoimintatarpeittesi mukaan haluat ehkä rajoittaa käyttäjän kirjauspäivämääräalueet kauden lopussa suoritettavan prosessin alussa tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="11293-110">Depending on your business needs, you may want to restrict user posting date ranges at the start of the period-end process or after it.</span></span> |[<span data-ttu-id="11293-111">Kirjausjaksojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="11293-111">Specify Posting Periods</span></span>](finance-how-specify-posting-periods.md) |
| <span data-ttu-id="11293-112">Saat yleiskuvauksen kauden lopussa tavallisesti suoritettavista toimenpiteistä, kuten kaikkien asiakirjojen ja päiväkirjojen kirjaaminen ja KP-raporttimallien ajaminen.</span><span class="sxs-lookup"><span data-stu-id="11293-112">Get an overview of activities that are commonly performed at the end of a period, such as posting all documents and journals, or running account schedules.</span></span> |[<span data-ttu-id="11293-113">Jaksojen päättäminen</span><span class="sxs-lookup"><span data-stu-id="11293-113">Closing Periods</span></span>](year-how-complete-period-end-processes.md) |
| <span data-ttu-id="11293-114">Valuutan vaihtokurssien päivittäminen sekä kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokurssien muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="11293-114">Update currency exchange rates and adjust the exchange rates of posted customer, vendor, and bank account entries.</span></span> |[<span data-ttu-id="11293-115">Valuutan vaihtokurssien päivittäminen</span><span class="sxs-lookup"><span data-stu-id="11293-115">Update Currency Exchange Rates</span></span>](finance-how-update-currencies.md) |
| <span data-ttu-id="11293-116">Kustannusten ja tulojen kohdistaminen tileille ja dimensioille.</span><span class="sxs-lookup"><span data-stu-id="11293-116">Allocate costs and income among accounts and dimensions.</span></span> |[<span data-ttu-id="11293-117">Kustannusten ja tulojen kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="11293-117">Allocating Costs and Income</span></span>](year-allocate-costs-income.md) |
| <span data-ttu-id="11293-118">Valmistele myynnistä kerättyjen arvonlisäverosummien raportointi veroviranomaisten verkkopalveluun.</span><span class="sxs-lookup"><span data-stu-id="11293-118">Prepare to report value-added tax amounts that you have collected for sales to the tax authorities' web service.</span></span> |[<span data-ttu-id="11293-119">ALV:n raportointi veroviranomaisille</span><span class="sxs-lookup"><span data-stu-id="11293-119">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="11293-120">Raporttien tulostaminen pääkirjanpidon sekä asiakkaan, toimittajan ja pankkitilin saldojen tarkistamiseksi ennen kauden sulkemista.</span><span class="sxs-lookup"><span data-stu-id="11293-120">Print reports to verify general ledger, customer, vendor and bank account balances before closing a period.</span></span> |[<span data-ttu-id="11293-121">Sulkemista edeltävien raporttien valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="11293-121">Preparing Pre-Closing Reports</span></span>](year-prepare-preclose-reports.md) |
| <span data-ttu-id="11293-122">Kirjanpitojaksojen ja tilikausien sulkeminen, tuloslaskelmasaldojen siirtäminen tasetileille ja vuositilinpäätöstapahtuman kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="11293-122">Close accounting periods and fiscal year, transfer income statement balances to balance sheet accounts and post the year end closing entry.</span></span> |[<span data-ttu-id="11293-123">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="11293-123">Closing Books</span></span>](year-close-books.md) |
| <span data-ttu-id="11293-124">Rahoituslaskelmien luomisessa apuna käytettävien raporttien tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="11293-124">Print reports that can assist you in creating financial statements.</span></span> |[<span data-ttu-id="11293-125">Tilinpäätöslaskelmien valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="11293-125">Preparing Closing Statements</span></span>](year-prepare-close-statement.md) |

## <a name="see-also"></a><span data-ttu-id="11293-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="11293-126">See Also</span></span>
[<span data-ttu-id="11293-127">Uuden tilikauden avaaminen</span><span class="sxs-lookup"><span data-stu-id="11293-127">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="11293-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="11293-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]

