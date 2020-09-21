---
title: Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta | Microsoft Docs
description: Kun otat maksupalvelut käyttöön, asiakkaiden on helpompi maksaa laskunsa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 753a9ae7b6b47113107bb9f9bdf439323cff615a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781733"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="b1c61-103">Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta</span><span class="sxs-lookup"><span data-stu-id="b1c61-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="b1c61-104">Pankkisiirron tai luottokorttien lisäksi asiakkaat voivat maksaa sinulle maksupalvelutilin, kuten Microsoft Payn, PayPalin tai WorldPayn, avulla.</span><span class="sxs-lookup"><span data-stu-id="b1c61-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="b1c61-105">Kun olet ottanut maksupalvelun käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, palvelun linkki on käytössä sähköpostitse asiakkaille lähetettävissä myyntiasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="b1c61-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="b1c61-106">Asiakkaat voivat siirtyä linkin kautta maksupalveluun ja maksaa laskun suoraan myyntiasiakirjasta.</span><span class="sxs-lookup"><span data-stu-id="b1c61-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="b1c61-107">Jos et halua lisätä linkkiä esimerkiksi silloin, kun asiakas maksaa käteisellä, voit poistaa maksupalvelun laskusta ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="b1c61-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="b1c61-108">Microsoft Pay, PayPal Payments Standard- ja WorldPay Payments Standard -laajennukset on asennettu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, ja ne odottavat käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="b1c61-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-d365fin"></a><span data-ttu-id="b1c61-109">Maksupalvelun ottaminen käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa</span><span class="sxs-lookup"><span data-stu-id="b1c61-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="b1c61-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupalvelut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b1c61-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b1c61-111">Valitse **Maksupalvelut**-sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b1c61-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="b1c61-112">Valitse maksupalvelu ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="b1c61-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="b1c61-113">Valitse **Maksupalvelut**-sivulla **Määritys**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b1c61-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="b1c61-114">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="b1c61-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="b1c61-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b1c61-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="b1c61-116">Maksupalvelun valitseminen myyntilaskussa</span><span class="sxs-lookup"><span data-stu-id="b1c61-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="b1c61-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b1c61-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b1c61-118">Avaa myyntilasku, jonka haluat maksaa maksupalvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="b1c61-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="b1c61-119">Valitse maksupalvelu **Maksupalvelu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b1c61-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="b1c61-120">**Maksupalvelu**-kenttä on käytettävissä vain, jos olet ottanut maksupalvelun käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b1c61-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b1c61-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b1c61-121">See Also</span></span>  
[<span data-ttu-id="b1c61-122">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b1c61-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="b1c61-123">Myynti</span><span class="sxs-lookup"><span data-stu-id="b1c61-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="b1c61-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="b1c61-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="b1c61-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b1c61-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
