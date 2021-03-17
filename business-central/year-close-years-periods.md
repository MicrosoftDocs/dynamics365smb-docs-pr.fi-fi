---
title: Tilikauden ja kirjanpitojaksojen sulkeminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan tilikauden tai kirjanpitojakson sulkemistehtävistä, joita ovat esimerkiksi varmistaminen, että asiakirjat ja päiväkirjat on kirjattu, ja pankkitilien saldojen tarkistaminen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: af455ede10bed862499b0cdfa8bff8461b4e47b7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389547"
---
# <a name="closing-years-and-periods"></a><span data-ttu-id="0d849-103">Vuosien ja kausien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="0d849-103">Closing Years and Periods</span></span>

<span data-ttu-id="0d849-104">Tilikauden lopussa on suoritettava joukko hallinnollisia tehtäviä. On esimerkiksi tarkistettava, että kaikki asiakirjat ja päiväkirjat on kirjattu, valuuttatiedot ovat ajan tasalla ja kirjat on suljettu.</span><span class="sxs-lookup"><span data-stu-id="0d849-104">At the end of a fiscal year, there are a number of administrative tasks that you have to perform, like making sure all documents and journals are posted, making sure currency data are up-to-date, closing the books, and more.</span></span> <span data-ttu-id="0d849-105">Suoritettavat tehtävät riippuvat yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="0d849-105">The actual tasks will depend your company.</span></span>

<span data-ttu-id="0d849-106">Seuraava taulukko sisältää yleiskuvauksen tehtävistä, joita yleensä suoritetaan vuoden ja kauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="0d849-106">The following table provides an overview of tasks that you typically perform to close a year and period.</span></span>

| <span data-ttu-id="0d849-107">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="0d849-107">To</span></span> | <span data-ttu-id="0d849-108">Katso</span><span class="sxs-lookup"><span data-stu-id="0d849-108">See</span></span> |
| --- | --- |
| <span data-ttu-id="0d849-109">Määritä tilikausi ja jaa se ajanjaksoiksi, joiden mukaan taloudellisesta tuloksesta raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="0d849-109">Define your fiscal year, and divide it into time periods for which to report financial performance.</span></span> | [<span data-ttu-id="0d849-110">Kirjanpitojaksojen ja tilikausien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0d849-110">Working with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)|
| <span data-ttu-id="0d849-111">Määritä järjestelmänlaajuiset ja käyttäjäkohtaiset kirjauspäivämäärävälit.</span><span class="sxs-lookup"><span data-stu-id="0d849-111">Specify system-wide and user-specific posting date ranges.</span></span> <span data-ttu-id="0d849-112">Liiketoimintatarpeittesi mukaan haluat ehkä rajoittaa käyttäjän kirjauspäivämääräalueet kauden lopussa suoritettavan prosessin alussa tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="0d849-112">Depending on your business needs, you may want to restrict user posting date ranges at the start of the period-end process or after it.</span></span> |[<span data-ttu-id="0d849-113">Kirjausjaksojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0d849-113">Specify Posting Periods</span></span>](finance-how-specify-posting-periods.md) |
| <span data-ttu-id="0d849-114">Saat yleiskuvauksen kauden lopussa tavallisesti suoritettavista toimenpiteistä, kuten kaikkien asiakirjojen ja päiväkirjojen kirjaaminen ja KP-raporttimallien ajaminen.</span><span class="sxs-lookup"><span data-stu-id="0d849-114">Get an overview of activities that are commonly performed at the end of a period, such as posting all documents and journals, or running account schedules.</span></span> |[<span data-ttu-id="0d849-115">Jaksojen päättäminen</span><span class="sxs-lookup"><span data-stu-id="0d849-115">Closing Periods</span></span>](year-how-complete-period-end-processes.md) |
| <span data-ttu-id="0d849-116">Valuutan vaihtokurssien päivittäminen sekä kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokurssien muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="0d849-116">Update currency exchange rates and adjust the exchange rates of posted customer, vendor, and bank account entries.</span></span> |[<span data-ttu-id="0d849-117">Valuutan vaihtokurssien päivittäminen</span><span class="sxs-lookup"><span data-stu-id="0d849-117">Update Currency Exchange Rates</span></span>](finance-how-update-currencies.md) |
| <span data-ttu-id="0d849-118">Kustannusten ja tulojen kohdistaminen tileille ja dimensioille.</span><span class="sxs-lookup"><span data-stu-id="0d849-118">Allocate costs and income among accounts and dimensions.</span></span> |[<span data-ttu-id="0d849-119">Kustannusten ja tulojen kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="0d849-119">Allocating Costs and Income</span></span>](year-allocate-costs-income.md) |
| <span data-ttu-id="0d849-120">Valmistele myynnistä kerättyjen arvonlisäverosummien raportointi veroviranomaisten verkkopalveluun.</span><span class="sxs-lookup"><span data-stu-id="0d849-120">Prepare to report value-added tax amounts that you have collected for sales to the tax authorities' web service.</span></span> |[<span data-ttu-id="0d849-121">ALV:n raportointi veroviranomaisille</span><span class="sxs-lookup"><span data-stu-id="0d849-121">Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="0d849-122">Raporttien tulostaminen pääkirjanpidon sekä asiakkaan, toimittajan ja pankkitilin saldojen tarkistamiseksi ennen kauden sulkemista.</span><span class="sxs-lookup"><span data-stu-id="0d849-122">Print reports to verify general ledger, customer, vendor and bank account balances before closing a period.</span></span> |[<span data-ttu-id="0d849-123">Sulkemista edeltävien raporttien valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="0d849-123">Preparing Pre-Closing Reports</span></span>](year-prepare-preclose-reports.md) |
| <span data-ttu-id="0d849-124">Kirjanpitojaksojen ja tilikausien sulkeminen, tuloslaskelmasaldojen siirtäminen tasetileille ja vuositilinpäätöstapahtuman kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="0d849-124">Close accounting periods and fiscal year, transfer income statement balances to balance sheet accounts and post the year end closing entry.</span></span> |[<span data-ttu-id="0d849-125">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="0d849-125">Closing Books</span></span>](year-close-books.md) |
| <span data-ttu-id="0d849-126">Rahoituslaskelmien luomisessa apuna käytettävien raporttien tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="0d849-126">Print reports that can assist you in creating financial statements.</span></span> |[<span data-ttu-id="0d849-127">Tilinpäätöslaskelmien valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="0d849-127">Preparing Closing Statements</span></span>](year-prepare-close-statement.md) |

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="0d849-128">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/close-fiscal-year-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="0d849-128">See Related Training at [Microsoft Learn](/learn/modules/close-fiscal-year-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="0d849-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0d849-129">See Also</span></span>

[<span data-ttu-id="0d849-130">Kirjanpitojaksojen ja tilikausien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0d849-130">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="0d849-131">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0d849-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]