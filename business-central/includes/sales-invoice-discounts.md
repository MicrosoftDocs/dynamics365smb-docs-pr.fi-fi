---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95121642b62f33ea1fc160c103ee845816706530
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778645"
---
<span data-ttu-id="ae39c-101">Kun kaikki nimikkeet on annettu riveinä, laskun alennus voidaan laskea koko myyntiasiakirjalle valitsemalla **Laske laskun alennus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="ae39c-101">When all the items have been entered as lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="ae39c-102">Alennus lasketaan kaikkien myyntiasiakirjan rivien perusteella niille nimikkeille, joilla on ostorivin **Salli laskualennus** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ae39c-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="ae39c-103">Tämä on oletusasetus nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="ae39c-103">This is the default setting for items.</span></span> <span data-ttu-id="ae39c-104">Esimerkiksi nimikekuluja sisältäviä rivejä ei sisällytetä laskualennuksen laskentaan.</span><span class="sxs-lookup"><span data-stu-id="ae39c-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="ae39c-105">Jos haluat kohdistaa alennuksen tällaisiin riveihin, sinun täytyy asettaa **Rivialennus-%**-kenttä asianmukaisille riveille.</span><span class="sxs-lookup"><span data-stu-id="ae39c-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="ae39c-106">Alennus lasketaan automaattisesti, jos **Myyntien ja myyntisaamisten asetukset** -sivulla valitaan **Lask. laskun alennus** -kenttä ja jos teet jonkin seuraavista myyntiasiakirjassa:</span><span class="sxs-lookup"><span data-stu-id="ae39c-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="ae39c-107">Tarkastele tilastoja</span><span class="sxs-lookup"><span data-stu-id="ae39c-107">View statistics</span></span>
> * <span data-ttu-id="ae39c-108">Tarkastele testiraporttia</span><span class="sxs-lookup"><span data-stu-id="ae39c-108">View a test report</span></span>
> * <span data-ttu-id="ae39c-109">Tulosta</span><span class="sxs-lookup"><span data-stu-id="ae39c-109">Print</span></span>
> * <span data-ttu-id="ae39c-110">Kirjaus</span><span class="sxs-lookup"><span data-stu-id="ae39c-110">Post</span></span>

<span data-ttu-id="ae39c-111">Asiakkaan laskualennuksen ehdot on määritetty **Asiakkaan laskualennukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ae39c-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="ae39c-112">Myyntiasiakirjan valuuttakoodin avulla etsitään valuutalle määritetyt laskualennusehdot.</span><span class="sxs-lookup"><span data-stu-id="ae39c-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="ae39c-113">Mikäli laskualennuksia ei ole määritetty ulkomaisille valuutoille, ohjelma käyttää laskualennusmäärityksiä, jotka on määritetty **Asiakkaan laskualennukset** -sivulla paikallisen valuutan summina ja myyntiasiakirjan kirjauspäivämäärän vaihtokurssia ulkomaanvaluuttamääräisen laskualennuksen laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="ae39c-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
