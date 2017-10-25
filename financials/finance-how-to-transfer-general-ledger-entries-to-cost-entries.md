---
title: "Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin | Microsoft Docs"
description: "Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4e68378d7acc789a70caf9c5b0590a81bf874337
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="aed62-103">Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin</span><span class="sxs-lookup"><span data-stu-id="aed62-103">How to: Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="aed62-104">Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="aed62-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="aed62-105">Ennen kuin suoritat prosessin pääkirjanpidon merkintöjen siirtämiseksi kustannusmerkintöihin, sinun täytyy laatia siirto manuaalisen korjauksen kirjaamisen välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="aed62-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="aed62-106">Valmistele siirto</span><span class="sxs-lookup"><span data-stu-id="aed62-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="aed62-107">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannuslaskennan asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="aed62-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="aed62-108">Varmista **Kustannuslaskennan asetukset** -ikkunassa, että **KP-siirron alkamispäivämäärä** -kenttään on määritetty oikea arvo.</span><span class="sxs-lookup"><span data-stu-id="aed62-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="aed62-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannustyyppikartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="aed62-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="aed62-110">Varmista **Kustannustyyppikortti** -ikkunassa, että kunkin kustannustyypin **KP-tilien väli** -kenttä on linkitetty oikein, jotta tapahtumat voidaan ottaa pääkirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="aed62-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="aed62-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="aed62-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="aed62-112">Tarkista, että kunkin käsiteltävän pääkirjanpidon tilin **KP-tilin kortti** -ikkunassa, että **Kustannustyypin numero**</span><span class="sxs-lookup"><span data-stu-id="aed62-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="aed62-113">.</span><span class="sxs-lookup"><span data-stu-id="aed62-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="aed62-114">Lisätietoja on ohjeaiheessa [Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="aed62-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="aed62-115">Tarkista, että kaikilla kyseessä olevilla pääkirjanpidon tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta.</span><span class="sxs-lookup"><span data-stu-id="aed62-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="aed62-116">Siirrä pääkirjanpidon tapahtumat kustannustapahtumiin</span><span class="sxs-lookup"><span data-stu-id="aed62-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="aed62-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Siirrä KP-tapahtumat kustannuslaskentaan** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="aed62-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="aed62-118">Aloita siirto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="aed62-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="aed62-119">Prosessi siirtää kaikki pääkirjanpidon tapahtumat, joita ei ole jo siirretty.</span><span class="sxs-lookup"><span data-stu-id="aed62-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="aed62-120">Siirron aikana prosessi luo yhteyksiä tapahtumiin **Kustannustapahtuma** -taulukossa ja **Kustannusrekisteri** -taulukossa.</span><span class="sxs-lookup"><span data-stu-id="aed62-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="aed62-121">Tämä mahdollistaa kustannustapahtumien lähteen jäljittämisen.</span><span class="sxs-lookup"><span data-stu-id="aed62-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aed62-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="aed62-122">See Also</span></span>  
 <span data-ttu-id="aed62-123">[Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="aed62-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="aed62-124">[Automaattinen siirto ja yhdistetyt tapahtumat](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="aed62-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="aed62-125">[Siirron tulokset](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="aed62-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="aed62-126">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="aed62-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="aed62-127">Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aed62-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

