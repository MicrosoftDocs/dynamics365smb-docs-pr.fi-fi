---
title: Asiakkaiden nimikkeiden myynnin estäminen myynnissä tai ostossa
description: Nimike voidaan merkitä Business Centralissa estetyksi myynnin tai oston osalta tai kaikkia tarkoituksia varten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 268d098318b77cb89a369e8edc14729a44bedae6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795741"
---
# <a name="block-customers"></a><span data-ttu-id="557fb-103">Asiakkaiden estäminen</span><span class="sxs-lookup"><span data-stu-id="557fb-103">Block Customers</span></span>
<span data-ttu-id="557fb-104">Voit estää asiakkaan esimerkiksi maksukyvyttömyyden vuoksi niin, että asiakasta ei voi lisätä myyntiasiakirjaan tai asiakkaalle ei voi kirjata tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="557fb-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="557fb-105">Asiakkaan estämisen lisäksi voit määrittää estoon asiakkaan myyntisaatavat yhdessä muistutusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="557fb-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="557fb-106">Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="557fb-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="557fb-107">Seuraavassa taulukossa kuvaillaan eri estoasetukset.</span><span class="sxs-lookup"><span data-stu-id="557fb-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="557fb-108">Asetus</span><span class="sxs-lookup"><span data-stu-id="557fb-108">Option</span></span>|<span data-ttu-id="557fb-109">Description</span><span class="sxs-lookup"><span data-stu-id="557fb-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="557fb-110">**Tyhjä**</span><span class="sxs-lookup"><span data-stu-id="557fb-110">**Blank**</span></span>|<span data-ttu-id="557fb-111">Tapahtumat ovat sallittuja tälle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="557fb-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="557fb-112">**Toimitus**</span><span class="sxs-lookup"><span data-stu-id="557fb-112">**Ship**</span></span>|<span data-ttu-id="557fb-113">Tälle asiakkaalle ei voi luoda uusia tilauksia ja toimituksia.</span><span class="sxs-lookup"><span data-stu-id="557fb-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="557fb-114">Aiemmin luodut toimitukset, joita ei ole vielä laskutettu, saa laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="557fb-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="557fb-115">**Lasku**</span><span class="sxs-lookup"><span data-stu-id="557fb-115">**Invoice**</span></span>|<span data-ttu-id="557fb-116">Tälle asiakkaalle ei voi luoda uusia tilauksia, toimituksia ja laskuja.</span><span class="sxs-lookup"><span data-stu-id="557fb-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="557fb-117">Aiemmin luotuja toimituksia, joita ei ole vielä laskutettu, ei voi laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="557fb-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="557fb-118">**Kaikki**</span><span class="sxs-lookup"><span data-stu-id="557fb-118">**All**</span></span>|<span data-ttu-id="557fb-119">Yksikään tapahtuma ei ole sallittu tälle asiakkaalle, eivät myöskään maksut.</span><span class="sxs-lookup"><span data-stu-id="557fb-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="557fb-120">Asiakkaan estäminen</span><span class="sxs-lookup"><span data-stu-id="557fb-120">To block a customer</span></span>  
1. <span data-ttu-id="557fb-121">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="557fb-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="557fb-122">Valitse asiakas ja valitse sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="557fb-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="557fb-123">Täytä **Estetty**-kenttään jonkin yläpuolella kuvatuista vaihtoehtoista.</span><span class="sxs-lookup"><span data-stu-id="557fb-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="557fb-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="557fb-124">See Also</span></span>  
[<span data-ttu-id="557fb-125">Uusien asiakkaiden rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="557fb-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="557fb-126">Avointen saldojen perintä</span><span class="sxs-lookup"><span data-stu-id="557fb-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="557fb-127">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="557fb-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
