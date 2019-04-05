---
title: Tilikauden ja kirjanpitojaksojen sulkeminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan tilikauden tai kirjanpitojakson sulkemistehtävistä, joita ovat esimerkiksi varmistaminen, että asiakirjat ja päiväkirjat on kirjattu, ja pankkitilien saldojen tarkistaminen.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 8ecd532a043ad53b7a1d5d6c38e87a7102407003
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795032"
---
# <a name="closing-years-and-periods"></a><span data-ttu-id="c242d-103">Vuosien ja kausien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="c242d-103">Closing Years and Periods</span></span>
<span data-ttu-id="c242d-104">Tilikauden lopussa on suoritettava joukko hallinnollisia tehtäviä. On esimerkiksi tarkistettava, että kaikki asiakirjat ja päiväkirjat on kirjattu, valuuttatiedot ovat ajan tasalla ja kirjat on suljettu.</span><span class="sxs-lookup"><span data-stu-id="c242d-104">At the end of a fiscal year, there are a number of administrative tasks that you have to perform, like making sure all documents and journals are posted, making sure currency data are up-to-date, closing the books, and more.</span></span> <span data-ttu-id="c242d-105">Suoritettavat tehtävät riippuvat yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="c242d-105">The actual tasks will depend your company.</span></span>

<span data-ttu-id="c242d-106">Seuraava taulukko sisältää yleiskuvauksen tehtävistä, joita yleensä suoritetaan vuoden ja kauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="c242d-106">The following table provides an overview of tasks that you typically perform to close a year and period.</span></span>

| <span data-ttu-id="c242d-107">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="c242d-107">To</span></span> | <span data-ttu-id="c242d-108">Katso</span><span class="sxs-lookup"><span data-stu-id="c242d-108">See</span></span> |
| --- | --- |
| <span data-ttu-id="c242d-109">Määritä tilikausi ja jaa se ajanjaksoiksi, joiden mukaan taloudellisesta tuloksesta raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="c242d-109">Define your fiscal year, and divide it into time periods for which to report financial performance.</span></span> | [<span data-ttu-id="c242d-110">Kirjanpitojaksojen ja tilikausien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="c242d-110">Working with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)|
| <span data-ttu-id="c242d-111">Määritä järjestelmänlaajuiset ja käyttäjäkohtaiset kirjauspäivämäärävälit.</span><span class="sxs-lookup"><span data-stu-id="c242d-111">Specify system-wide and user-specific posting date ranges.</span></span> <span data-ttu-id="c242d-112">Liiketoimintatarpeittesi mukaan haluat ehkä rajoittaa käyttäjän kirjauspäivämääräalueet kauden lopussa suoritettavan prosessin alussa tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="c242d-112">Depending on your business needs, you may want to restrict user posting date ranges at the start of the period-end process or after it.</span></span> |[<span data-ttu-id="c242d-113">Kirjausjaksojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c242d-113">Specify Posting Periods</span></span>](finance-how-specify-posting-periods.md) |
| <span data-ttu-id="c242d-114">Saat yleiskuvauksen kauden lopussa tavallisesti suoritettavista toimenpiteistä, kuten kaikkien asiakirjojen ja päiväkirjojen kirjaaminen ja KP-raporttimallien ajaminen.</span><span class="sxs-lookup"><span data-stu-id="c242d-114">Get an overview of activities that are commonly performed at the end of a period, such as posting all documents and journals, or running account schedules.</span></span> |[<span data-ttu-id="c242d-115">Jaksojen päättäminen</span><span class="sxs-lookup"><span data-stu-id="c242d-115">Closing Periods</span></span>](year-how-complete-period-end-processes.md) |
| <span data-ttu-id="c242d-116">Valuutan vaihtokurssien päivittäminen sekä kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokurssien muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="c242d-116">Update currency exchange rates and adjust the exchange rates of posted customer, vendor, and bank account entries.</span></span> |[<span data-ttu-id="c242d-117">Valuutan vaihtokurssien päivittäminen</span><span class="sxs-lookup"><span data-stu-id="c242d-117">Update Currency Exchange Rates</span></span>](finance-how-update-currencies.md) |
| <span data-ttu-id="c242d-118">Kustannusten ja tulojen kohdistaminen tileille ja dimensioille.</span><span class="sxs-lookup"><span data-stu-id="c242d-118">Allocate costs and income among accounts and dimensions.</span></span> |[<span data-ttu-id="c242d-119">Kustannusten ja tulojen kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="c242d-119">Allocating Costs and Income</span></span>](year-allocate-costs-income.md) |
| <span data-ttu-id="c242d-120">Valmistele myynnistä kerättyjen arvonlisäverosummien raportointi veroviranomaisten verkkopalveluun.</span><span class="sxs-lookup"><span data-stu-id="c242d-120">Prepare to report value-added tax amounts that you have collected for sales to the tax authorities' web service.</span></span> |[<span data-ttu-id="c242d-121">ALV:n raportointi veroviranomaisille</span><span class="sxs-lookup"><span data-stu-id="c242d-121">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="c242d-122">Raporttien tulostaminen pääkirjanpidon sekä asiakkaan, toimittajan ja pankkitilin saldojen tarkistamiseksi ennen kauden sulkemista.</span><span class="sxs-lookup"><span data-stu-id="c242d-122">Print reports to verify general ledger, customer, vendor and bank account balances before closing a period.</span></span> |[<span data-ttu-id="c242d-123">Sulkemista edeltävien raporttien valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="c242d-123">Preparing Pre-Closing Reports</span></span>](year-prepare-preclose-reports.md) |
| <span data-ttu-id="c242d-124">Kirjanpitojaksojen ja tilikausien sulkeminen, tuloslaskelmasaldojen siirtäminen tasetileille ja vuositilinpäätöstapahtuman kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="c242d-124">Close accounting periods and fiscal year, transfer income statement balances to balance sheet accounts and post the year end closing entry.</span></span> |[<span data-ttu-id="c242d-125">Kirjojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="c242d-125">Closing Books</span></span>](year-close-books.md) |
| <span data-ttu-id="c242d-126">Rahoituslaskelmien luomisessa apuna käytettävien raporttien tulostaminen.</span><span class="sxs-lookup"><span data-stu-id="c242d-126">Print reports that can assist you in creating financial statements.</span></span> |[<span data-ttu-id="c242d-127">Tilinpäätöslaskelmien valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="c242d-127">Preparing Closing Statements</span></span>](year-prepare-close-statement.md) |

## <a name="see-also"></a><span data-ttu-id="c242d-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c242d-128">See Also</span></span>
[<span data-ttu-id="c242d-129">Uuden tilikauden avaaminen</span><span class="sxs-lookup"><span data-stu-id="c242d-129">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="c242d-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c242d-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
