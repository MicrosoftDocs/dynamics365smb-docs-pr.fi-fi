---
title: Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin | Microsoft Docs
description: Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 273a8c4341f621710819fd5fbc5cb8ce579c86f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796145"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="7b806-103">Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin</span><span class="sxs-lookup"><span data-stu-id="7b806-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="7b806-104">Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="7b806-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="7b806-105">Ennen kuin suoritat prosessin pääkirjanpidon merkintöjen siirtämiseksi kustannusmerkintöihin, sinun täytyy laatia siirto manuaalisen korjauksen kirjaamisen välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="7b806-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="7b806-106">Valmistele siirto</span><span class="sxs-lookup"><span data-stu-id="7b806-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="7b806-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kustannuslaskennan asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7b806-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7b806-108">Varmista **Kustannuslaskennan asetukset** -sivulla, että **KP-siirron alkamispäivämäärä** -kenttään on määritetty oikea arvo.</span><span class="sxs-lookup"><span data-stu-id="7b806-108">On the **Cost Accounting Setup** page, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="7b806-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kustannustyyppikartta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7b806-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="7b806-110">Varmista **Kustannustyyppikortti** -sivulla, että kunkin kustannustyypin **KP-tilien väli** -kenttä on linkitetty oikein, jotta tapahtumat voidaan ottaa pääkirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="7b806-110">On the **Cost Type Card** page, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="7b806-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Tilikartta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7b806-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="7b806-112">Tarkista, että kunkin käsiteltävän pääkirjanpidon tilin **KP-tilin kortti** -sivulla, että **Kustannustyypin numero**</span><span class="sxs-lookup"><span data-stu-id="7b806-112">For each relevant general ledger account, on the **G/L Account Card** page, verify that the **Cost Type No.**</span></span> <span data-ttu-id="7b806-113">-kenttä on linkitetty oikein kustannuslajiin.</span><span class="sxs-lookup"><span data-stu-id="7b806-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="7b806-114">Lisätietoja on kohdassa [Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="7b806-114">For more information, see [Setting Up Cost Accounting](finance-set-up-cost-accounting.md).</span></span>  
7.  <span data-ttu-id="7b806-115">Tarkista, että kaikilla kyseessä olevilla pääkirjanpidon tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta.</span><span class="sxs-lookup"><span data-stu-id="7b806-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="7b806-116">Siirrä pääkirjanpidon tapahtumat kustannustapahtumiin</span><span class="sxs-lookup"><span data-stu-id="7b806-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="7b806-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirrä KP-tapahtumat kustannuslaskentaan** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7b806-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7b806-118">Aloita siirto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7b806-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="7b806-119">Prosessi siirtää kaikki pääkirjanpidon tapahtumat, joita ei ole jo siirretty.</span><span class="sxs-lookup"><span data-stu-id="7b806-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="7b806-120">Siirron aikana prosessi luo yhteyksiä tapahtumiin **Kustannustapahtuma** -taulukossa ja **Kustannusrekisteri** -taulukossa.</span><span class="sxs-lookup"><span data-stu-id="7b806-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="7b806-121">Tämä mahdollistaa kustannustapahtumien lähteen jäljittämisen.</span><span class="sxs-lookup"><span data-stu-id="7b806-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b806-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7b806-122">See Also</span></span>  
<span data-ttu-id="7b806-123">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="7b806-123">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
[<span data-ttu-id="7b806-124">Kustannuslaskennan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7b806-124">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)   
