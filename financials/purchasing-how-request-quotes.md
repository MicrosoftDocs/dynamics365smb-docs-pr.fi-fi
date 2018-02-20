---
title: "Tarjouksen pyytäminen toimittajalta luotavan tarjouspyynnön avulla | Microsoft Docs"
description: "Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntöasiakirja kirjaamaan asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3fe5eca9c26380248471facbd945838b1bf47a1d
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="request-quotes"></a><span data-ttu-id="cb3b1-103">Tarjousten pyytäminen</span><span class="sxs-lookup"><span data-stu-id="cb3b1-103">Request Quotes</span></span>
<span data-ttu-id="cb3b1-104">Ostotarjousta voidaan käyttää ostotilauksen alustavana luonnoksena, jonka jälkeen tilaus voidaan muuttaa ostolaskuksi tai -tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="cb3b1-105">Uuden ostotarjouksen luominen</span><span class="sxs-lookup"><span data-stu-id="cb3b1-105">To create a purchase quote</span></span>
1. <span data-ttu-id="cb3b1-106">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostotarjoukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="cb3b1-107">Luo uusi asiakirja samalla tavalla kuin tekisit ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="cb3b1-108">Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="cb3b1-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="cb3b1-109">Ostotarjousten muuttaminen ostotilauksiksi</span><span class="sxs-lookup"><span data-stu-id="cb3b1-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="cb3b1-110">Kun olet hyväksynyt toimittajan tarjouksen, voit käsitellä oston muuntamalla tarjouksen ostolaskuksi tai tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="cb3b1-111">Avaa muuntovalmis ostotarjous ja valitse sitten **Tee tilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="cb3b1-112">Ostotarjous poistetaan tietokannasta.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="cb3b1-113">Ostotarjouksen tietojen perusteella luodaan ostolasku tai -tilaus, jossa voit käsitellä oston.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="cb3b1-114">Luodun ostolaskun tai -tilauksen **Tarjouksen nro** -kenttä määrittää sen ostotarjouksen numeron, josta tilaus on muunnettu.</span><span class="sxs-lookup"><span data-stu-id="cb3b1-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb3b1-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cb3b1-115">See Also</span></span>
[<span data-ttu-id="cb3b1-116">Osto</span><span class="sxs-lookup"><span data-stu-id="cb3b1-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="cb3b1-117">Ostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cb3b1-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="cb3b1-118">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="cb3b1-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="cb3b1-119">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cb3b1-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

