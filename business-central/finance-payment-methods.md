---
title: Maksutapojen määrittäminen
description: Voit määrittää myynti- ja ostolaskuille maksutavan, kuten sekin, pankkisiirron, käteisen tai PayPal-maksun.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 01/21/2021
ms.author: bholtorf
ms.openlocfilehash: 78e754998c7adc871b57347ff0bed714db8cc83f
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035354"
---
# <a name="set-up-payment-methods"></a><span data-ttu-id="fb154-103">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fb154-103">Set Up Payment Methods</span></span>

<span data-ttu-id="fb154-104">Maksutavat määrittävät, miten asiakkaiden halutaan ensisijaisesti maksavan ja miten haluat maksaa toimittajille.</span><span class="sxs-lookup"><span data-stu-id="fb154-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="fb154-105">Maksutapa voi olla asiakas- tai toimittajakohtainen,</span><span class="sxs-lookup"><span data-stu-id="fb154-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="fb154-106">Tyypillisiä maksutapoja ovat esimerkiksi **pankki**, **käteinen**, **sekki** tai **tili**.</span><span class="sxs-lookup"><span data-stu-id="fb154-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="fb154-107">Kun maksutapa määritetään asiakkaille ja toimittajille, heille luotavissa myynti- ja ostoasiakirjoissa käytetään aina samaa maksutapaa.</span><span class="sxs-lookup"><span data-stu-id="fb154-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="fb154-108">Voit tarvittaessa muuttaa maksutapaa myynti- tai ostoasiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="fb154-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="fb154-109">Voit tehdä näin esimerkiksi tilanteessa, jossa haluat maksaa tietyn ostolaskun käteisenä sekin sijaan.</span><span class="sxs-lookup"><span data-stu-id="fb154-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="fb154-110">Tämä muutos ei vaikuta toimittajalle määritettyyn oletusmaksutapaan.</span><span class="sxs-lookup"><span data-stu-id="fb154-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="fb154-111">Myynti- ja ostoasiakirjoissa käytetään samaa maksutapaa.</span><span class="sxs-lookup"><span data-stu-id="fb154-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="fb154-112">Jos maksutavaksi on määritetty _käteinen_, sitä käytetään sekä maksuja maksettaessa että niitä vastaanotettaessa.</span><span class="sxs-lookup"><span data-stu-id="fb154-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="fb154-113">tietää, että odotat myyntilaskua luodessasi vastaanottavasi maksun ja päin vastoin ostolaskuja luotaessa.</span><span class="sxs-lookup"><span data-stu-id="fb154-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="fb154-114">Palautusten hyvityslaskut ovat kuitenkin poikkeuksia, sillä rahavirrat kulkevat vastakkaisiin suuntiin eli sinulta asiakkaalle ja toimittajalta sinulle.</span><span class="sxs-lookup"><span data-stu-id="fb154-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="fb154-115">Tämän vuoksi hyvityslaskuille ei määritetä oletusmaksutapaa.</span><span class="sxs-lookup"><span data-stu-id="fb154-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="fb154-116">Tämän voi kuitenkin kiertää, jos olet määrittänyt asiakkaalle tai toimittajalle maksuehdot.</span><span class="sxs-lookup"><span data-stu-id="fb154-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="fb154-117">Vaikka **Laske maksualen. hyvityslask.** -kenttää ei ole tarkoitettu tähän tarkoitukseen, tämän valintaruudun valitseminen **Maksuehdot**-sivulla lisää oletusmaksutavan hyvityslaskua luotaessa.</span><span class="sxs-lookup"><span data-stu-id="fb154-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="fb154-118">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fb154-118">To set up a payment method</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="fb154-119">sisältää muutamia yritysten usein käyttämiä maksutapoja.</span><span class="sxs-lookup"><span data-stu-id="fb154-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="fb154-120">Voit kuitenkin lisätä niitä tarvittavan määrän.</span><span class="sxs-lookup"><span data-stu-id="fb154-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="fb154-121">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Maksutavat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fb154-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="fb154-122">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="fb154-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="fb154-123">Vaihtoehtoisesti voit lisätä maksuehdot maksutapaan.</span><span class="sxs-lookup"><span data-stu-id="fb154-123">Optionally, add payment terms to your payment method.</span></span> <span data-ttu-id="fb154-124">Lisätietoja on ohjeaiheessa [Maksuehtojen määrittäminen](finance-payment-terms.md).</span><span class="sxs-lookup"><span data-stu-id="fb154-124">For more information, see [Set Up Payment Terms](finance-payment-terms.md).</span></span>  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="fb154-125">Maksutavan määrittely asiakkaalle tai toimittajalle</span><span class="sxs-lookup"><span data-stu-id="fb154-125">To assign a payment method to a customer or vendor</span></span>

1. <span data-ttu-id="fb154-126">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fb154-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="fb154-127">Valitse **Maksutavan koodi** -kentässä menetelmä, jota käytetään oletusarvoisesti asiakkaalle tai toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="fb154-127">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb154-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fb154-128">See Also</span></span>

[<span data-ttu-id="fb154-129">Uusien asiakkaiden rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="fb154-129">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="fb154-130">Maksuehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fb154-130">Set Up Payment Terms</span></span>](finance-payment-terms.md)  
[<span data-ttu-id="fb154-131">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="fb154-131">Finance</span></span>](finance.md)  
<span data-ttu-id="fb154-132">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fb154-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
