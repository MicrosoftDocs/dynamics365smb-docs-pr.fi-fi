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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: fe51ade7a46ab7a8fdf77419a0098ac47fe2e5d1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-request-quotes"></a><span data-ttu-id="6456d-103">Toimintaohje: Tarjousten pyytäminen</span><span class="sxs-lookup"><span data-stu-id="6456d-103">How to: Request Quotes</span></span>
<span data-ttu-id="6456d-104">Ostotarjousta voidaan käyttää ostotilauksen alustavana luonnoksena, jonka jälkeen tilaus voidaan muuttaa ostolaskuksi tai -tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="6456d-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or a order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="6456d-105">Uuden ostotarjouksen luominen</span><span class="sxs-lookup"><span data-stu-id="6456d-105">To create a purchase quote</span></span>
1. <span data-ttu-id="6456d-106">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostotarjoukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6456d-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="6456d-107">Luo uusi asiakirja samalla tavalla kuin tekisit ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="6456d-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="6456d-108">Lisätietoja on kohdassa[Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="6456d-108">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="6456d-109">Ostotarjousten muuttaminen ostotilauksiksi</span><span class="sxs-lookup"><span data-stu-id="6456d-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="6456d-110">Kun olet hyväksynyt toimittajan tarjouksen, voit käsitellä oston muuntaa tarjouksen ostolaskuksi tai tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="6456d-110">When you have accepted the vendors quote, you can convert it to a purchase invoice or ordfer to process the purchase.</span></span>

1. <span data-ttu-id="6456d-111">Avaa muuntovalmis ostotarjous ja valitse sitten **Tee tilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="6456d-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="6456d-112">Ostotarjous poistetaan tietokannasta.</span><span class="sxs-lookup"><span data-stu-id="6456d-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="6456d-113">Ostotarjouksen tietojen perusteella ostolasku tai -tilaus, jossa voit käsitellä oston.</span><span class="sxs-lookup"><span data-stu-id="6456d-113">A purchase invoice or a sales order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="6456d-114">Luodun ostolaskun tai -tilauksen **Tarjouksen nro** -kenttä määrittää sen ostotarjouksen numeron, josta tilaus on muunnettu.</span><span class="sxs-lookup"><span data-stu-id="6456d-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="6456d-115">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6456d-115">See Also</span></span>
[<span data-ttu-id="6456d-116">Osto</span><span class="sxs-lookup"><span data-stu-id="6456d-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="6456d-117">Ostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6456d-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="6456d-118">Toimintaohje: Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="6456d-118">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="6456d-119">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6456d-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

