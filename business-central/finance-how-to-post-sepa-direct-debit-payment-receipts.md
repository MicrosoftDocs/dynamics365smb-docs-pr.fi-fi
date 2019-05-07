---
title: SEPA-suoraveloitusmaksujen kirjaaminen | Microsoft Docs
description: Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit kyseiselle myyntilaskuille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6c646575ba803358aa00309ce02742423bcc7de8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "930752"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="73901-103">SEPA-suoraveloitusmaksujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="73901-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="73901-104">Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit kyseiselle myyntilaskuille.</span><span class="sxs-lookup"><span data-stu-id="73901-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="73901-105">Lisätietoja on kohdassa [SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="73901-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="73901-106">Voit kirjata suoraan maksun suoraan **Suoraveloitusperinnät**- tai **Suoraveloitusperintätapahtumat**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="73901-106">You can post the payment receipt directly from the **Direct Debit Collections** page or the **Direct Debit Collect. Entries** page.</span></span> <span data-ttu-id="73901-107">Vaihtoehtoisesti voit siirtää työn toiselle käyttäjälle valmistelemalla siihen liittyvät päiväkirjarivit.</span><span class="sxs-lookup"><span data-stu-id="73901-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><span data-ttu-id="73901-108">Suoraveloitusmaksukuitin kirjaaminen suoraveloitusperinnän sivulta</span><span class="sxs-lookup"><span data-stu-id="73901-108">To post a direct-debit payment receipt from the Direct Debit Collections page</span></span>  
1. <span data-ttu-id="73901-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Suoraveloitusperinnät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="73901-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="73901-110">Valitse rivi suoraveloitusperinnälle, joka on viety pankkitiedostoon ja jonka pankki on käsitellyt onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="73901-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="73901-111">Lisätietoja on kohdassa [SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="73901-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="73901-112">Valitse **Kirjaa maksukuitit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="73901-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="73901-113">Täytä **Kirjaa suoraveloitusperintä**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="73901-113">On the **Post Direct Debit Collection** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="73901-114">Kenttä</span><span class="sxs-lookup"><span data-stu-id="73901-114">Field</span></span>|<span data-ttu-id="73901-115">Description</span><span class="sxs-lookup"><span data-stu-id="73901-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="73901-116">**Suoraveloitusperinnän nro**</span><span class="sxs-lookup"><span data-stu-id="73901-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="73901-117">Määritä suoraveloitusperintä, johon haluat kirjata maksukuitin.</span><span class="sxs-lookup"><span data-stu-id="73901-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="73901-118">**Yleisen päiväkirjan malli**</span><span class="sxs-lookup"><span data-stu-id="73901-118">**General Journal Template**</span></span>|<span data-ttu-id="73901-119">Määritä, mitä yleisen päiväkirjan mallia käytit maksukuitin kirjaamiseen, kuten kassakuittien malli.</span><span class="sxs-lookup"><span data-stu-id="73901-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="73901-120">**Yleisen päiväkirjan erän nimi**</span><span class="sxs-lookup"><span data-stu-id="73901-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="73901-121">Määritä, mitä yleistä päiväkirjaerää käytit maksukuitin kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="73901-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="73901-122">**Luo vain päiväkirja**</span><span class="sxs-lookup"><span data-stu-id="73901-122">**Create Journal Only**</span></span>|<span data-ttu-id="73901-123">Merkitse tämä valintaruutu, jos et halua kirjata maksukuittia, kun valitset **OK**-painikkeen.</span><span class="sxs-lookup"><span data-stu-id="73901-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="73901-124">Maksukuitti valmistellaan määritetyssä päiväkirjassa eikä sitä kirjata ennen kuin joku kirjaa kyseisen päiväkirjarivin.</span><span class="sxs-lookup"><span data-stu-id="73901-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="73901-125">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="73901-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="73901-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="73901-126">See Also</span></span>  
 <span data-ttu-id="73901-127">[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="73901-127">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="73901-128">Myynti</span><span class="sxs-lookup"><span data-stu-id="73901-128">Sales</span></span>](sales-manage-sales.md)
