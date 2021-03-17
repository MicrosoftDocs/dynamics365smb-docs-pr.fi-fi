---
title: PayPal Payments Standard -laajennuksen käyttäminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten laajennusten avulla asiakkaille voidaan antaa mahdollisuus suorittaa PayPal-maksuja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ac0ee9bb3287542484478daf23877d3e3bebf5f7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392072"
---
# <a name="the-paypal-payments-standard-extension"></a><span data-ttu-id="9cf22-103">PayPal Payments Standard -laajennus</span><span class="sxs-lookup"><span data-stu-id="9cf22-103">The PayPal Payments Standard Extension</span></span>
<span data-ttu-id="9cf22-104">Asiakkaat vaativat jatkuvasti yhä korkeatasoisempaa asiakaspalvelua sekä tuotteen laadun että toimitus- ja maksuvaihtoehtojen osalta.</span><span class="sxs-lookup"><span data-stu-id="9cf22-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="9cf22-105">Voit parantaa asiakaspalvelun tasoa PayPal Payments Standard -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="9cf22-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="9cf22-106">Pankkisiirron tai luottokorttien lisäksi asiakkaille voi tarjota mahdollisuuden maksaa PayPal-tilin avulla.</span><span class="sxs-lookup"><span data-stu-id="9cf22-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="9cf22-107">Kun lähetät myyntilaskun tai -tilauksen sähköpostitse, sähköpostin perustekstissä ja liitetyssä PDF-tiedostossa on PayPal-linkki.</span><span class="sxs-lookup"><span data-stu-id="9cf22-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="9cf22-108">Kun asiakas valitsee PayPal-linkin, näyttöön avautuu asiakkaan PayPal-tilin palvelusivu, joka sisältää myyntiä koskevat maksutiedot.</span><span class="sxs-lookup"><span data-stu-id="9cf22-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="9cf22-109">Tämän jälkeen asiakas voi maksaa laskun kuten minkä tahansa PayPal-maksun.</span><span class="sxs-lookup"><span data-stu-id="9cf22-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="9cf22-110">PayPal Payments Standard -palvelusta on apua seuraavissa asioissa:</span><span class="sxs-lookup"><span data-stu-id="9cf22-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="9cf22-111">asiakkaan maksut saapuvat nopeammin pankkitilillesi</span><span class="sxs-lookup"><span data-stu-id="9cf22-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="9cf22-112">asiakkailla on useita vaihtoehtoja maksaa laskut.</span><span class="sxs-lookup"><span data-stu-id="9cf22-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="9cf22-113">PayPal on luotettava maksupalvelu. Asiakkaat käyttävät PayPalia mieluummin kuin syöttävät luottokorttitietonsa verkkosivulle.</span><span class="sxs-lookup"><span data-stu-id="9cf22-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="9cf22-114">PayPalin avulla maksuja voi käsitellä useilla eri tavoilla. Niitä ovat luottokorttikäsittely, PayPal-tilit ja muut lähteet.</span><span class="sxs-lookup"><span data-stu-id="9cf22-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="9cf22-115">PayPal-linkki voidaan lisätä automaattisesti myyntiasiakirjoihin. Myös käyttäjä voi lisätä linkin.</span><span class="sxs-lookup"><span data-stu-id="9cf22-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="9cf22-116">PayPal Payments Standard -palvelu ei sisällä kuukausi- tai aloitusmaksuja.</span><span class="sxs-lookup"><span data-stu-id="9cf22-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="9cf22-117">Koska palvelu on laajennus, voit ottaa PayPal Payment Standard -palvelun helposti käyttöön silloin, kun yritys tarvitsee sitä.</span><span class="sxs-lookup"><span data-stu-id="9cf22-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="9cf22-118">Lisätietoja on kohdassa [Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="9cf22-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9cf22-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9cf22-119">See Also</span></span>
<span data-ttu-id="9cf22-120">[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="9cf22-120">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="9cf22-121">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9cf22-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="9cf22-122">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9cf22-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]