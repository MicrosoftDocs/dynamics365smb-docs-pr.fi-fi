---
title: Maksualennusten ohittaminen
description: 'Käytä maksualennusten ohittamistoimintoa kokonaissumman yhteydessä, kun haluat hyväksyä maksut seuraavien ehtojen täyttyessä:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 94b5aba591d29a173a0e190ee34d4d5d9fc383fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180811"
---
# <a name="disregard-payment-discounts"></a><span data-ttu-id="bc59c-103">Maksualennusten ohittaminen</span><span class="sxs-lookup"><span data-stu-id="bc59c-103">Disregard Payment Discounts</span></span>
<span data-ttu-id="bc59c-104">Käytä maksualennusten ohittamistoimintoa kokonaissumman yhteydessä, kun haluat hyväksyä maksut seuraavien ehtojen täyttyessä:</span><span class="sxs-lookup"><span data-stu-id="bc59c-104">Use the disregard payment discount at full payment feature to accept payments when the following conditions are true:</span></span>  

- <span data-ttu-id="bc59c-105">Maksualennuksen päivämäärä < maksupäivämäärä <= maksutoleranssin päivämäärä</span><span class="sxs-lookup"><span data-stu-id="bc59c-105">Payment discount date < payment date <= payment tolerance date</span></span>  
- <span data-ttu-id="bc59c-106">Kokonaissumma >= maksun summa >= kokonaissumma - maksualennus</span><span class="sxs-lookup"><span data-stu-id="bc59c-106">Full amount >= payment amount >= full amount - payment discount</span></span>  

## <a name="to-disregard-a-payment-discount"></a><span data-ttu-id="bc59c-107">Maksualennuksen ohittaminen</span><span class="sxs-lookup"><span data-stu-id="bc59c-107">To disregard a payment discount</span></span>  

1.  <span data-ttu-id="bc59c-108">Valitse ![Etsi sivu tai raportti](../../media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Maksuehdot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="bc59c-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bc59c-109">Valitse rivi, jonka maksuehdolle haluat ottaa käyttöön maksualennuksia tai jolta haluat poistaa ne.</span><span class="sxs-lookup"><span data-stu-id="bc59c-109">Select the line with the payment term for which you want to activate or deactivate payment discounts.</span></span>  
3.  <span data-ttu-id="bc59c-110">Ota tämä toiminto käyttöön valitsemalla **Ohita maks.alen. kok.sum. yht.** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="bc59c-110">Select the **Disreg. Pmt. Disc. at Full Pmt** check box to initiate activation for this feature.</span></span> <span data-ttu-id="bc59c-111">Poista toiminto käytöstä tyhjentämällä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="bc59c-111">To deactivate, clear the check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bc59c-112">Kun yksi maksu kohdistetaan useisiin laskuihin, maksualennuksen ohitustoimintoa ei tueta kokonaissumman yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bc59c-112">When you apply one payment to multiple invoices, the feature to ignore payment discount at full payment is not supported.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bc59c-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="bc59c-113">See Also</span></span>  
<span data-ttu-id="bc59c-114">[Verkkopankkitoiminta Suomessa](electronic-banking-in-finland.md) </span><span class="sxs-lookup"><span data-stu-id="bc59c-114">[Electronic Banking in Finland](electronic-banking-in-finland.md) </span></span>  
<span data-ttu-id="bc59c-115">[Maksutiedostojen luominen](how-to-generate-payment-files.md) </span><span class="sxs-lookup"><span data-stu-id="bc59c-115">[Generate Payment Files](how-to-generate-payment-files.md) </span></span>  
[<span data-ttu-id="bc59c-116">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bc59c-116">Defining Payment Methods</span></span>](../../finance-payment-methods.md)  
<span data-ttu-id="bc59c-117">[Maksutoleranssien ja maksualennustoleranssien käsitteleminen](../../finance-payment-tolerance-and-payment-discount-tolerance.md)   </span><span class="sxs-lookup"><span data-stu-id="bc59c-117">[Work with Payment Tolerances and Payment Discount Tolerances](../../finance-payment-tolerance-and-payment-discount-tolerance.md)   </span></span>  
[<span data-ttu-id="bc59c-118">Pankin viitetiedostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bc59c-118">Set Up Bank Reference Files</span></span>](how-to-set-up-bank-reference-files.md)
