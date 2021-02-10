---
title: Ostotarjouksen luominen tarjouksen pyytämistä varten | Microsoft Docs
description: Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntöasiakirja kirjaamaan asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cff54e778beb1bb08342835419998242eed4adf3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758465"
---
# <a name="request-quotes"></a><span data-ttu-id="fe6f3-103">Tarjousten pyytäminen</span><span class="sxs-lookup"><span data-stu-id="fe6f3-103">Request Quotes</span></span>
<span data-ttu-id="fe6f3-104">Ostotarjousta voidaan käyttää ostotilauksen alustavana luonnoksena, jonka jälkeen tilaus voidaan muuttaa ostolaskuksi tai -tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="fe6f3-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="fe6f3-105">Uuden ostotarjouksen luominen</span><span class="sxs-lookup"><span data-stu-id="fe6f3-105">To create a purchase quote</span></span>
1. <span data-ttu-id="fe6f3-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotarjoukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fe6f3-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="fe6f3-107">Luo uusi asiakirja samalla tavalla kuin tekisit ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="fe6f3-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="fe6f3-108">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="fe6f3-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="fe6f3-109">Ostotarjousten muuttaminen ostotilauksiksi</span><span class="sxs-lookup"><span data-stu-id="fe6f3-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="fe6f3-110">Kun olet hyväksynyt toimittajan tarjouksen, voit käsitellä oston muuntamalla tarjouksen ostolaskuksi tai tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="fe6f3-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="fe6f3-111">Avaa muuntovalmis ostotarjous ja valitse sitten **Tee tilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="fe6f3-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="fe6f3-112">Ostotarjous poistetaan tietokannasta.</span><span class="sxs-lookup"><span data-stu-id="fe6f3-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="fe6f3-113">Ostotarjouksen tietojen perusteella luodaan ostolasku tai -tilaus, jossa voit käsitellä oston.</span><span class="sxs-lookup"><span data-stu-id="fe6f3-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="fe6f3-114">Luodun ostolaskun tai -tilauksen **Tarjouksen nro** -kenttä määrittää sen ostotarjouksen numeron, josta tilaus on muunnettu.</span><span class="sxs-lookup"><span data-stu-id="fe6f3-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe6f3-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fe6f3-115">See Also</span></span>
[<span data-ttu-id="fe6f3-116">Osto</span><span class="sxs-lookup"><span data-stu-id="fe6f3-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="fe6f3-117">Ostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fe6f3-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="fe6f3-118">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="fe6f3-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="fe6f3-119">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fe6f3-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
