---
title: Microsoft Pay Standard| Microsoft Docs
description: Antaa tietoja Microsoft Pay -laajennuksesta
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 82e5cc8ba4b9335b8282857b564f9dcb3050fca0
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784784"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="5e386-103">Microsoft Pay -laajennus</span><span class="sxs-lookup"><span data-stu-id="5e386-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e386-104">Alkaen 8. helmikuuta 2020, Microsoft Pay -palvelun muutokset vaikuttavat Microsoft Pay -laajennukseen Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)]ssa.</span><span class="sxs-lookup"><span data-stu-id="5e386-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="5e386-105">Muutosten vuoksi helmikuun 8. päivän jälkeen **Maksa nyt** -maksulinkit, joita Microsoft Pay -laajennus luo laskuille kohdassa [!INCLUDE[d365fin](includes/d365fin_md.md)], eivät avaa Microsoft Payta.</span><span class="sxs-lookup"><span data-stu-id="5e386-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[d365fin](includes/d365fin_md.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="5e386-106">Laajennusta käyttävien asiakkaiden on muutettava maksupalveluasetuksensa, jotta he voivat käyttää sen sijaan PayPal-laajennusta.</span><span class="sxs-lookup"><span data-stu-id="5e386-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="5e386-107">Tammikuun 8. päivästä alkaen näytämme ilmoituksen kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5e386-107">From January 8, we will display a notification in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5e386-108">Ilmoitus sisältää linkin asetuksiin, joita sinun on muutettava, ja lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="5e386-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="5e386-109">Helmikuun 8. päivän jälkeen Microsoft Pay -laajennos ei ole enää saatavilla kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5e386-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span><br /></br>
>
> <span data-ttu-id="5e386-110">Muutokset vaikuttavat seuraaviin Business Centralin versioihin:</span><span class="sxs-lookup"><span data-stu-id="5e386-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="5e386-111">Microsoft Dynamics 365 Business Central lokakuu 2018</span><span class="sxs-lookup"><span data-stu-id="5e386-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="5e386-112">Microsoft Dynamics 365 Business Central huhtikuu 2019</span><span class="sxs-lookup"><span data-stu-id="5e386-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="5e386-113">Microsoft Dynamics 365 Business Central 2019 julkaisuaalto 2</span><span class="sxs-lookup"><span data-stu-id="5e386-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="5e386-114">Asiakkaat vaativat jatkuvasti yhä korkeatasoisempaa asiakaspalvelua sekä tuotteen laadun että toimituksen ja maksupalvelujen osalta.</span><span class="sxs-lookup"><span data-stu-id="5e386-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="5e386-115">Voit parantaa asiakaspalvelun tasoa Microsoft Pay -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="5e386-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="5e386-116">Microsoft Pay -laajennus lisää Microsoft Pay -linkin myyntiasiakirjoihin, joten asiakkaiden on helppo maksaa Microsoft Pay -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="5e386-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="5e386-117">Voit sitten voit lähettää asiakirjojat sähköpostitse, mikä parantaa asiakaspalvelua ja nopeuttaa asiakkaiden maksujen saapumista pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="5e386-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="5e386-118">Microsoft Pay -laajennuksen edut:</span><span class="sxs-lookup"><span data-stu-id="5e386-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="5e386-119">Asiakkaan maksut saapuvat nopeammin pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="5e386-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="5e386-120">asiakkailla on useita vaihtoehtoja maksaa laskut.</span><span class="sxs-lookup"><span data-stu-id="5e386-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="5e386-121">Microsoft Pay on luotettava maksupalvelu, jota asiakkaat käyttävät mieluummin kuin antavat luottokorttitietonsa tuntemattomissa sivustoissa.</span><span class="sxs-lookup"><span data-stu-id="5e386-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="5e386-122">Microsoft Payn avulla maksuja voi käsitellä useilla eri tavoilla. Niitä ovat esimerkiksi luottokorttikäsittely, kuten PayPal ja Stripe.</span><span class="sxs-lookup"><span data-stu-id="5e386-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="5e386-123">Microsoft Pay -linkki voidaan upottaa jokaiseen lasku automaattisesti tai käyttäjä voi tehdä sen itse.</span><span class="sxs-lookup"><span data-stu-id="5e386-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="5e386-124">Tämä toiminto on luotu laajennuksena, voit päättää itse, milloin se kannattaa ottaa käyttöön liiketoimintaprosesseissa tai kannattaako sen käyttö lainkaan.</span><span class="sxs-lookup"><span data-stu-id="5e386-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="5e386-125">Maksupalvelulaajennukset voi ottaa maksutta käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Tiliä varten on kuitenkin otettava yhteys maksupalveluun.</span><span class="sxs-lookup"><span data-stu-id="5e386-125">Enabling payment service extensions is free in [!INCLUDE[d365fin](includes/d365fin_md.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="5e386-126">Lisätietoja on kohdassa [Asiakkaan maksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5e386-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5e386-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5e386-127">See Also</span></span>
<span data-ttu-id="5e386-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="5e386-128">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="5e386-129">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5e386-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="5e386-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e386-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
