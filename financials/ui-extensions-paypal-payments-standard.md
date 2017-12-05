---
title: "PayPal Payments Standard -laajennuksen käyttäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten laajennusten avulla asiakkaille voidaan antaa mahdollisuus suorittaa PayPal-maksuja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 43511c3c509c495555f4583fdbe982d8b98aa648
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---
# <a name="the-paypal-payments-standard-extension-to-dynamics-365-business-edition"></a><span data-ttu-id="781ea-103">Dynamics 365 Business editionin PayPal Payments Standard -laajennus</span><span class="sxs-lookup"><span data-stu-id="781ea-103">The PayPal Payments Standard Extension to Dynamics 365 Business edition</span></span> 
<span data-ttu-id="781ea-104">Asiakkaat vaativat jatkuvasti yhä korkeatasoisempaa asiakaspalvelua sekä tuotteen laadun että toimitus- ja maksuvaihtoehtojen osalta.</span><span class="sxs-lookup"><span data-stu-id="781ea-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="781ea-105">Voit parantaa asiakaspalvelun tasoa PayPal Payments Standard -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="781ea-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="781ea-106">Pankkisiirron tai luottokorttien lisäksi asiakkaille voi tarjota mahdollisuuden maksaa PayPal-tilin avulla.</span><span class="sxs-lookup"><span data-stu-id="781ea-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="781ea-107">Kun lähetät myyntilaskun tai -tilauksen sähköpostitse, sähköpostin perustekstissä ja liitetyssä PDF-tiedostossa on PayPal-linkki.</span><span class="sxs-lookup"><span data-stu-id="781ea-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="781ea-108">Kun asiakas valitsee PayPal-linkin, näyttöön avautuu asiakkaan PayPal-tilin palvelusivu, joka sisältää myyntiä koskevat maksutiedot.</span><span class="sxs-lookup"><span data-stu-id="781ea-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="781ea-109">Tämän jälkeen asiakas voi maksaa laskun kuten minkä tahansa PayPal-maksun.</span><span class="sxs-lookup"><span data-stu-id="781ea-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="781ea-110">PayPal Payments Standard -palvelusta on apua seuraavissa asioissa:</span><span class="sxs-lookup"><span data-stu-id="781ea-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="781ea-111">asiakkaan maksut saapuvat nopeammin pankkitilillesi</span><span class="sxs-lookup"><span data-stu-id="781ea-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="781ea-112">asiakkailla on useita vaihtoehtoja maksaa laskut.</span><span class="sxs-lookup"><span data-stu-id="781ea-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="781ea-113">PayPal on luotettava maksupalvelu. Asiakkaat käyttävät PayPalia mieluummin kuin syöttävät luottokorttitietonsa verkkosivulle.</span><span class="sxs-lookup"><span data-stu-id="781ea-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="781ea-114">PayPalin avulla maksuja voi käsitellä useilla eri tavoilla. Niitä ovat luottokorttikäsittely, PayPal-tilit ja muut lähteet.</span><span class="sxs-lookup"><span data-stu-id="781ea-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="781ea-115">PayPal-linkki voidaan lisätä automaattisesti myyntiasiakirjoihin. Myös käyttäjä voi lisätä linkin.</span><span class="sxs-lookup"><span data-stu-id="781ea-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="781ea-116">PayPal Payments Standard -palvelu ei sisällä kuukausi- tai aloitusmaksuja.</span><span class="sxs-lookup"><span data-stu-id="781ea-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="781ea-117">Koska palvelu on laajennus, voit ottaa PayPal Payment Standard -palvelun helposti käyttöön silloin, kun yritys tarvitsee sitä.</span><span class="sxs-lookup"><span data-stu-id="781ea-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="781ea-118">Lisätietoja on kohdassa [Toimintaohje: Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="781ea-118">For more information, see [How to: Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="781ea-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="781ea-119">See Also</span></span>
<span data-ttu-id="781ea-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="781ea-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="781ea-121">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="781ea-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="781ea-122">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="781ea-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

