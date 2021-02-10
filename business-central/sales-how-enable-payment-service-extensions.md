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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3bcfac75d1d161a4163fda466e320b0efd408655
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758265"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="7467d-103">Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta</span><span class="sxs-lookup"><span data-stu-id="7467d-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="7467d-104">Pankkisiirron tai luottokorttien lisäksi asiakkaat voivat maksaa sinulle maksupalvelutilin, kuten Microsoft Payn, PayPalin tai WorldPayn, avulla.</span><span class="sxs-lookup"><span data-stu-id="7467d-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="7467d-105">Kun olet ottanut maksupalvelun käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa, palvelun linkki on käytössä sähköpostitse asiakkaille lähetettävissä myyntiasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="7467d-105">After you enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="7467d-106">Asiakkaat voivat siirtyä linkin kautta maksupalveluun ja maksaa laskun suoraan myyntiasiakirjasta.</span><span class="sxs-lookup"><span data-stu-id="7467d-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="7467d-107">Jos et halua lisätä linkkiä esimerkiksi silloin, kun asiakas maksaa käteisellä, voit poistaa maksupalvelun laskusta ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="7467d-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="7467d-108">Microsoft Pay, PayPal Payments Standard- ja WorldPay Payments Standard -laajennukset on asennettu [!INCLUDE[prod_short](includes/prod_short.md)]iin, ja ne odottavat käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="7467d-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[prod_short](includes/prod_short.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-prod_short"></a><span data-ttu-id="7467d-109">Maksupalvelun ottaminen käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa</span><span class="sxs-lookup"><span data-stu-id="7467d-109">To enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>
1. <span data-ttu-id="7467d-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupalvelut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7467d-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7467d-111">Valitse **Maksupalvelut**-sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="7467d-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="7467d-112">Valitse maksupalvelu ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="7467d-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="7467d-113">Valitse **Maksupalvelut**-sivulla **Määritys**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="7467d-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="7467d-114">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="7467d-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="7467d-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7467d-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="7467d-116">Maksupalvelun valitseminen myyntilaskussa</span><span class="sxs-lookup"><span data-stu-id="7467d-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="7467d-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7467d-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7467d-118">Avaa myyntilasku, jonka haluat maksaa maksupalvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="7467d-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="7467d-119">Valitse maksupalvelu **Maksupalvelu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7467d-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="7467d-120">**Maksupalvelu**-kenttä on käytettävissä vain, jos olet ottanut maksupalvelun käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7467d-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7467d-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7467d-121">See Also</span></span>  
[<span data-ttu-id="7467d-122">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7467d-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="7467d-123">Myynti</span><span class="sxs-lookup"><span data-stu-id="7467d-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="7467d-124">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="7467d-124">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="7467d-125">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7467d-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
