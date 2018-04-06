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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 592f42f53593735526ccbd3ddaa69bb0778de0ac
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="4a919-103">Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin</span><span class="sxs-lookup"><span data-stu-id="4a919-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="4a919-104">Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="4a919-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="4a919-105">Ennen kuin suoritat prosessin pääkirjanpidon merkintöjen siirtämiseksi kustannusmerkintöihin, sinun täytyy laatia siirto manuaalisen korjauksen kirjaamisen välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="4a919-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="4a919-106">Valmistele siirto</span><span class="sxs-lookup"><span data-stu-id="4a919-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="4a919-107">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannuslaskennan asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4a919-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4a919-108">Varmista **Kustannuslaskennan asetukset** -ikkunassa, että **KP-siirron alkamispäivämäärä** -kenttään on määritetty oikea arvo.</span><span class="sxs-lookup"><span data-stu-id="4a919-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="4a919-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannustyyppikartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4a919-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="4a919-110">Varmista **Kustannustyyppikortti** -ikkunassa, että kunkin kustannustyypin **KP-tilien väli** -kenttä on linkitetty oikein, jotta tapahtumat voidaan ottaa pääkirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="4a919-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="4a919-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4a919-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="4a919-112">Tarkista, että kunkin käsiteltävän pääkirjanpidon tilin **KP-tilin kortti** -ikkunassa, että **Kustannustyypin numero**</span><span class="sxs-lookup"><span data-stu-id="4a919-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="4a919-113">.</span><span class="sxs-lookup"><span data-stu-id="4a919-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="4a919-114">Lisätietoja on ohjeaiheessa [Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="4a919-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="4a919-115">Tarkista, että kaikilla kyseessä olevilla pääkirjanpidon tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta.</span><span class="sxs-lookup"><span data-stu-id="4a919-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="4a919-116">Siirrä pääkirjanpidon tapahtumat kustannustapahtumiin</span><span class="sxs-lookup"><span data-stu-id="4a919-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="4a919-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Siirrä KP-tapahtumat kustannuslaskentaan** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4a919-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4a919-118">Aloita siirto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4a919-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="4a919-119">Prosessi siirtää kaikki pääkirjanpidon tapahtumat, joita ei ole jo siirretty.</span><span class="sxs-lookup"><span data-stu-id="4a919-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="4a919-120">Siirron aikana prosessi luo yhteyksiä tapahtumiin **Kustannustapahtuma** -taulukossa ja **Kustannusrekisteri** -taulukossa.</span><span class="sxs-lookup"><span data-stu-id="4a919-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="4a919-121">Tämä mahdollistaa kustannustapahtumien lähteen jäljittämisen.</span><span class="sxs-lookup"><span data-stu-id="4a919-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a919-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4a919-122">See Also</span></span>  
 <span data-ttu-id="4a919-123">[Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4a919-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="4a919-124">[Automaattinen siirto ja yhdistetyt tapahtumat](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4a919-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="4a919-125">[Siirron tulokset](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="4a919-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="4a919-126">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4a919-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="4a919-127">Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4a919-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

