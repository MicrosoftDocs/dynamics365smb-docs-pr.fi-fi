---
title: SEPA-suoraveloitusmaksujen kirjaaminen | Microsoft Docs
description: "Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit kyseiselle myyntilaskuille."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0031017c96172dca76b50542e52c6a437c01427a
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="90817-103">SEPA-suoraveloitusmaksujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="90817-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="90817-104">Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit kyseiselle myyntilaskuille.</span><span class="sxs-lookup"><span data-stu-id="90817-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="90817-105">Lisätietoja on kohdassa [SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="90817-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="90817-106">Voit kirjata suoraan maksun suoraan **Suoraveloitusperinnät**-ikkunasta tai **Suoraveloitusperintätapahtumat**-ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="90817-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="90817-107">Vaihtoehtoisesti voit siirtää työn toiselle käyttäjälle valmistelemalla siihen liittyvät päiväkirjarivit.</span><span class="sxs-lookup"><span data-stu-id="90817-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="90817-108">Suoraveloitusmaksukuitin kirjaaminen suoraveloitusperinnän ikkunasta</span><span class="sxs-lookup"><span data-stu-id="90817-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="90817-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Suoraveloitusperinnät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="90817-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="90817-110">Valitse rivi suoraveloitusperinnälle, joka on viety pankkitiedostoon ja jonka pankki on käsitellyt onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="90817-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="90817-111">Lisätietoja on kohdassa [SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="90817-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="90817-112">Valitse **Kirjaa maksukuitit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="90817-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="90817-113">Täytä **Kirjaa suoraveloitusperintä** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="90817-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="90817-114">Kenttä</span><span class="sxs-lookup"><span data-stu-id="90817-114">Field</span></span>|<span data-ttu-id="90817-115">Description</span><span class="sxs-lookup"><span data-stu-id="90817-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="90817-116">**Suoraveloitusperinnän nro**</span><span class="sxs-lookup"><span data-stu-id="90817-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="90817-117">Määritä suoraveloitusperintä, johon haluat kirjata maksukuitin.</span><span class="sxs-lookup"><span data-stu-id="90817-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="90817-118">**Yleisen päiväkirjan malli**</span><span class="sxs-lookup"><span data-stu-id="90817-118">**General Journal Template**</span></span>|<span data-ttu-id="90817-119">Määritä, mitä yleisen päiväkirjan mallia käytit maksukuitin kirjaamiseen, kuten kassakuittien malli.</span><span class="sxs-lookup"><span data-stu-id="90817-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="90817-120">**Yleisen päiväkirjan erän nimi**</span><span class="sxs-lookup"><span data-stu-id="90817-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="90817-121">Määritä, mitä yleistä päiväkirjaerää käytit maksukuitin kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="90817-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="90817-122">**Luo vain päiväkirja**</span><span class="sxs-lookup"><span data-stu-id="90817-122">**Create Journal Only**</span></span>|<span data-ttu-id="90817-123">Merkitse tämä valintaruutu, jos et halua kirjata maksukuittia, kun valitset **OK**-painikkeen.</span><span class="sxs-lookup"><span data-stu-id="90817-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="90817-124">Maksukuitti valmistellaan määritetyssä päiväkirjassa eikä sitä kirjata ennen kuin joku kirjaa kyseisen päiväkirjarivin.</span><span class="sxs-lookup"><span data-stu-id="90817-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="90817-125">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="90817-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="90817-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="90817-126">See Also</span></span>  
 <span data-ttu-id="90817-127">[Maksujen kerääminen SEPA-suoraveloituksena](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="90817-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="90817-128">Myynti</span><span class="sxs-lookup"><span data-stu-id="90817-128">Sales</span></span>](sales-manage-sales.md)

