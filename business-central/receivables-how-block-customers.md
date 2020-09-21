---
title: Myynnin estäminen asiakkaille
description: Voit tarvittaessa estää asiakasta sisältymästä myyntiasiakirjoihin ja muihin myyntitapahtumiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 720eb2d5899ba067dbcee8dc97492ebcd01b1abd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779168"
---
# <a name="block-customers"></a><span data-ttu-id="e942d-103">Asiakkaiden estäminen</span><span class="sxs-lookup"><span data-stu-id="e942d-103">Block Customers</span></span>
<span data-ttu-id="e942d-104">Voit estää asiakkaan esimerkiksi maksukyvyttömyyden vuoksi niin, että asiakasta ei voi lisätä myyntiasiakirjaan tai asiakkaalle ei voi kirjata tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e942d-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="e942d-105">Asiakkaan estämisen lisäksi voit määrittää estoon asiakkaan myyntisaatavat yhdessä muistutusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="e942d-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="e942d-106">Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="e942d-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="e942d-107">Seuraavassa taulukossa kuvaillaan eri asiakkaiden estoasetukset.</span><span class="sxs-lookup"><span data-stu-id="e942d-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="e942d-108">Asetus</span><span class="sxs-lookup"><span data-stu-id="e942d-108">Option</span></span>|<span data-ttu-id="e942d-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e942d-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="e942d-110">**Tyhjä**</span><span class="sxs-lookup"><span data-stu-id="e942d-110">**Blank**</span></span>|<span data-ttu-id="e942d-111">Tapahtumat ovat sallittuja tälle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e942d-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="e942d-112">**Toimitus**</span><span class="sxs-lookup"><span data-stu-id="e942d-112">**Ship**</span></span>|<span data-ttu-id="e942d-113">Tälle asiakkaalle ei voi luoda uusia tilauksia ja toimituksia.</span><span class="sxs-lookup"><span data-stu-id="e942d-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="e942d-114">Aiemmin luodut toimitukset, joita ei ole vielä laskutettu, saa laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="e942d-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="e942d-115">**Lasku**</span><span class="sxs-lookup"><span data-stu-id="e942d-115">**Invoice**</span></span>|<span data-ttu-id="e942d-116">Tälle asiakkaalle ei voi luoda uusia tilauksia, toimituksia ja laskuja.</span><span class="sxs-lookup"><span data-stu-id="e942d-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="e942d-117">Aiemmin luotuja toimituksia, joita ei ole vielä laskutettu, ei voi laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="e942d-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="e942d-118">Voit edelleen lähettää asiakkaalle muistutuksia ja viivästyskulujen laskuja.</span><span class="sxs-lookup"><span data-stu-id="e942d-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="e942d-119">**Kaikki**</span><span class="sxs-lookup"><span data-stu-id="e942d-119">**All**</span></span>|<span data-ttu-id="e942d-120">Yksikään tapahtuma ei ole sallittu tälle asiakkaalle, eivät myöskään maksut.</span><span class="sxs-lookup"><span data-stu-id="e942d-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="e942d-121">Asiakkaan estäminen</span><span class="sxs-lookup"><span data-stu-id="e942d-121">To block a customer</span></span>  
1. <span data-ttu-id="e942d-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e942d-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="e942d-123">Valitse asiakas ja valitse sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e942d-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="e942d-124">Valitse**Estetty**-kentässä, mitä haluat estää, kuten yllä olevassa taulukossa on kuvattu.</span><span class="sxs-lookup"><span data-stu-id="e942d-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="e942d-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e942d-125">See Also</span></span>  
[<span data-ttu-id="e942d-126">Uusien asiakkaiden rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="e942d-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="e942d-127">Avointen saldojen perintä</span><span class="sxs-lookup"><span data-stu-id="e942d-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="e942d-128">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="e942d-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
