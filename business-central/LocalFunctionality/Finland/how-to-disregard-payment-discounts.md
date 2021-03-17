---
title: Maksualennusten ohittaminen
description: 'Käytä maksualennusten ohittamistoimintoa kokonaissumman yhteydessä, kun haluat hyväksyä maksut seuraavien ehtojen täyttyessä:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 18e16bda0b728bccc19d435e88f01bea61bb4317
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380339"
---
# <a name="disregard-payment-discounts"></a><span data-ttu-id="9fba9-103">Maksualennusten ohittaminen</span><span class="sxs-lookup"><span data-stu-id="9fba9-103">Disregard Payment Discounts</span></span>
<span data-ttu-id="9fba9-104">Käytä maksualennusten ohittamistoimintoa kokonaissumman yhteydessä, kun haluat hyväksyä maksut seuraavien ehtojen täyttyessä:</span><span class="sxs-lookup"><span data-stu-id="9fba9-104">Use the disregard payment discount at full payment feature to accept payments when the following conditions are true:</span></span>  

- <span data-ttu-id="9fba9-105">Maksualennuksen päivämäärä < maksupäivämäärä <= maksutoleranssin päivämäärä</span><span class="sxs-lookup"><span data-stu-id="9fba9-105">Payment discount date < payment date <= payment tolerance date</span></span>  
- <span data-ttu-id="9fba9-106">Kokonaissumma >= maksun summa >= kokonaissumma - maksualennus</span><span class="sxs-lookup"><span data-stu-id="9fba9-106">Full amount >= payment amount >= full amount - payment discount</span></span>  

## <a name="to-disregard-a-payment-discount"></a><span data-ttu-id="9fba9-107">Maksualennuksen ohittaminen</span><span class="sxs-lookup"><span data-stu-id="9fba9-107">To disregard a payment discount</span></span>  

1.  <span data-ttu-id="9fba9-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksuehdot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9fba9-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9fba9-109">Valitse rivi, jonka maksuehdolle haluat ottaa käyttöön maksualennuksia tai jolta haluat poistaa ne.</span><span class="sxs-lookup"><span data-stu-id="9fba9-109">Select the line with the payment term for which you want to activate or deactivate payment discounts.</span></span>  
3.  <span data-ttu-id="9fba9-110">Ota tämä toiminto käyttöön valitsemalla **Ohita maks.alen. kok.sum. yht.** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9fba9-110">Select the **Disreg. Pmt. Disc. at Full Pmt** check box to initiate activation for this feature.</span></span> <span data-ttu-id="9fba9-111">Poista toiminto käytöstä tyhjentämällä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9fba9-111">To deactivate, clear the check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9fba9-112">Kun yksi maksu kohdistetaan useisiin laskuihin, maksualennuksen ohitustoimintoa ei tueta kokonaissumman yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="9fba9-112">When you apply one payment to multiple invoices, the feature to ignore payment discount at full payment is not supported.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9fba9-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9fba9-113">See Also</span></span>  
<span data-ttu-id="9fba9-114">[Verkkopankkitoiminta Suomessa](electronic-banking-in-finland.md) </span><span class="sxs-lookup"><span data-stu-id="9fba9-114">[Electronic Banking in Finland](electronic-banking-in-finland.md) </span></span>  
<span data-ttu-id="9fba9-115">[Maksutiedostojen luominen](how-to-generate-payment-files.md) </span><span class="sxs-lookup"><span data-stu-id="9fba9-115">[Generate Payment Files](how-to-generate-payment-files.md) </span></span>  
[<span data-ttu-id="9fba9-116">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9fba9-116">Defining Payment Methods</span></span>](../../finance-payment-methods.md)  
<span data-ttu-id="9fba9-117">[Maksutoleranssien ja maksualennustoleranssien käsitteleminen](../../finance-payment-tolerance-and-payment-discount-tolerance.md)   </span><span class="sxs-lookup"><span data-stu-id="9fba9-117">[Work with Payment Tolerances and Payment Discount Tolerances](../../finance-payment-tolerance-and-payment-discount-tolerance.md)   </span></span>  
[<span data-ttu-id="9fba9-118">Pankin viitetiedostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9fba9-118">Set Up Bank Reference Files</span></span>](how-to-set-up-bank-reference-files.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]