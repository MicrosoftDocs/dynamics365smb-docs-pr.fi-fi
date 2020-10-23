---
title: Ostolaskujen selvittäminen viipymättä
description: Jos toimittajalle on maksettava käteisellä tai sekillä, tarvittava kirjaus voidaan tehdä laskua kirjattaessa.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: bac023393d95623a2731ef1b2ada7d30b135063b
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968357"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="906c9-103">Ostolaskujen selvittäminen viipymättä</span><span class="sxs-lookup"><span data-stu-id="906c9-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="906c9-104">Jos toimittajalle on maksettava käteisellä tai sekillä, voit kirjata maksun kun kirjaat laskun.</span><span class="sxs-lookup"><span data-stu-id="906c9-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="906c9-105">Jos maksat ostolaskuja usein käteisellä, sekillä tai pankkisiirrolla, on hyvä idea perustaa tiettyjä maksutapoja joissa on vastatili ja syötä tämä metodi **Maksutapa** -kenttään toimittajakortille.</span><span class="sxs-lookup"><span data-stu-id="906c9-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="906c9-106">Ohjelma automaattisesti syöttää vastatilin numeron ja laskuotsikon joka kerta kun luot uuden laskun.</span><span class="sxs-lookup"><span data-stu-id="906c9-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="906c9-107">Lisätietoja on kohdassa [Maksutapojen määrittely](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="906c9-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="906c9-108">Ostolaskujen selvittäminen viipymättä</span><span class="sxs-lookup"><span data-stu-id="906c9-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="906c9-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="906c9-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="906c9-110">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="906c9-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="906c9-111">Jos haluat maksaa käteisellä tai pankkisiirrolla, annan kirjanpidon kassatilin tai pankkitilin numero **Vastatilin nro.** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="906c9-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="906c9-112">Kohde **Vasta tilin tyyppi** ja **Vasta. tilin nro.** -kenttiä ei sisällytetä vakiolaskun otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="906c9-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="906c9-113">Jotta voisit kirjata laskun maksun, sinun täytyy ottaa yhteyttä Microsoft-kumppaniin, joka voi lisätä kentät koodin avulla.</span><span class="sxs-lookup"><span data-stu-id="906c9-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="906c9-114">Tämä mukautus tarvitaan vain, jos et määritä vastatilejä maksutavoille yllä kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="906c9-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="906c9-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="906c9-115">See Also</span></span>

[<span data-ttu-id="906c9-116">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="906c9-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="906c9-117">Osto</span><span class="sxs-lookup"><span data-stu-id="906c9-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="906c9-118">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="906c9-118">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
