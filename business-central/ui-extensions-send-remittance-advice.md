---
title: Lähetä Maksusuoritustietojen Ohjeet Laajennus | Microsoft Docs
description: Kuvailee Lähetä Maksusuoritustietojen Ohjeet laajennusta, joka sallii maksusuoritetietojen ohjeiden uudelleenlähettämisen maksukirjauskansiosta tai toimittajatapahtumista.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f6afaa9ade29c955033914b608806c3fb0f5a310
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912219"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="2b4ca-103">Lähetä Maksusuoritustietojen Ohjeet</span><span class="sxs-lookup"><span data-stu-id="2b4ca-103">Send Remittance Advice</span></span>

<span data-ttu-id="2b4ca-104">Kun maksusuoritetietojen ohjetta käytetään tiedottamaan toimittajia maksuista, voit nyt lähettää maksusuoritustietojen ohjeet kootusti maksukirjauskansiosta ja uudelleenlähettää ne, kun maksut on suoritettu toimittajatapahtumista käyttäen dokumenttienlähetysprofiileita.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="2b4ca-105">Tämä toiminto on tuettu vain Business Central Onlinessa ja paikallisesti seuraavissa maissa: Yhdistynyt Kunigaskunta, Yhdysvallat, Kanada, Australia, Uusi Seelanti ja Etelä-Afrikka</span><span class="sxs-lookup"><span data-stu-id="2b4ca-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="2b4ca-106">Voit lähettää maksusuoritetietojen ohjeita kahdella eri tapaa:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="2b4ca-107">**Maksukirjauskansio** -sivulla, valitse **Liittyvät**, **Maksut**, **Lähetä Maksusuoritetietojen Ohjeet** lähettääksesi sähköpostilla maksusuoritetietojen ohjeet yhdeltä tai useammalta maksukirjauskansion riviltä</span><span class="sxs-lookup"><span data-stu-id="2b4ca-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="2b4ca-108">Valitse **Toimittajatapahtumat**-sivulla **Toiminnot**, **Funktiot**, **Lähetä Maksutietojen Ohjeet** lähettääksesi sähköpostilla maksutietojen ohjeet, kun toimittajamaksut on julkaistu yhdestä tai useammasta toimittajatapahtumasta</span><span class="sxs-lookup"><span data-stu-id="2b4ca-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="2b4ca-109">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2b4ca-109">See Also</span></span>

[<span data-ttu-id="2b4ca-110">Ehdota toimittajamaksuja</span><span class="sxs-lookup"><span data-stu-id="2b4ca-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="2b4ca-111">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2b4ca-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="2b4ca-112">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2b4ca-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2b4ca-113">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="2b4ca-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
