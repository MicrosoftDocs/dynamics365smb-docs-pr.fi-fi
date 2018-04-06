---
title: "Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta | Microsoft Docs"
description: "Kun otat maksupalvelut käyttöön, asiakkaiden on helpompi maksaa laskunsa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5853080ef39196e95c293415e9b81502ff03d5ed
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="b4e87-103">Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta</span><span class="sxs-lookup"><span data-stu-id="b4e87-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="b4e87-104">Pankkisiirron tai luottokorttien lisäksi asiakkaat voivat maksaa sinulle maksupalvelutilin, kuten Microsoft Payn, PayPalin tai WorldPayn, avulla.</span><span class="sxs-lookup"><span data-stu-id="b4e87-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="b4e87-105">Kun olet ottanut maksupalvelun käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, palvelun linkki on käytössä sähköpostitse asiakkaille lähetettävissä myyntiasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="b4e87-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="b4e87-106">Asiakkaat voivat siirtyä linkin kautta maksupalveluun ja maksaa laskun suoraan myyntiasiakirjasta.</span><span class="sxs-lookup"><span data-stu-id="b4e87-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="b4e87-107">Jos et halua lisätä linkkiä esimerkiksi silloin, kun asiakas maksaa käteisellä, voit poistaa maksupalvelun laskusta ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="b4e87-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="b4e87-108">Microsoft Pay, PayPal Payments Standard- ja WorldPay Payments Standard -laajennukset on asennettu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, ja ne odottavat käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="b4e87-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="b4e87-109">Maksupalvelun ottaminen käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa</span><span class="sxs-lookup"><span data-stu-id="b4e87-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="b4e87-110">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupalvelut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b4e87-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b4e87-111">Valitse **Maksupalvelut**-ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b4e87-111">In the **Payment Services** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="b4e87-112">Valitse maksupalvelu ja sulje sitten ikkuna.</span><span class="sxs-lookup"><span data-stu-id="b4e87-112">Select the payment service, and then close the window.</span></span>  
4. <span data-ttu-id="b4e87-113">Valitse **Maksupalvelut**-ikkunassa **Asetus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b4e87-113">In the **Payment Services** window, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="b4e87-114">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="b4e87-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="b4e87-115">Sulje ikkuna.</span><span class="sxs-lookup"><span data-stu-id="b4e87-115">Close the window.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="b4e87-116">Maksupalvelun valitseminen myyntilaskussa</span><span class="sxs-lookup"><span data-stu-id="b4e87-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="b4e87-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b4e87-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b4e87-118">Avaa myyntilasku, jonka haluat maksaa maksupalvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="b4e87-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="b4e87-119">Valitse maksupalvelu **Maksupalvelu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b4e87-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="b4e87-120">**Maksupalvelu**-kenttä on käytettävissä vain, jos olet ottanut maksupalvelun käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b4e87-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b4e87-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b4e87-121">See Also</span></span>  
[<span data-ttu-id="b4e87-122">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b4e87-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="b4e87-123">Myynti</span><span class="sxs-lookup"><span data-stu-id="b4e87-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="b4e87-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="b4e87-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="b4e87-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b4e87-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

