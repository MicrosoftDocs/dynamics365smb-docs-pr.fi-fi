---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035781"
---
<span data-ttu-id="64af3-101">Kun kaikki nimikkeet on syötetty myyntiriveille, laskun alennus voidaan laskea koko myyntiasiakirjalle valitsemalla **Laske laskun alennus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="64af3-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="64af3-102">Alennus lasketaan automaattisesti, jos **Myyntien ja myyntisaamisten asetukset** -ikkunassa valitaan **Lask. laskun alennus** -kenttä ja jos teet jonkin seuraavista myyntiasiakirjassa:</span><span class="sxs-lookup"><span data-stu-id="64af3-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="64af3-103">Tarkastele tilastoja</span><span class="sxs-lookup"><span data-stu-id="64af3-103">View statistics</span></span>
* <span data-ttu-id="64af3-104">Tarkastele testiraporttia</span><span class="sxs-lookup"><span data-stu-id="64af3-104">View a test report</span></span>
* <span data-ttu-id="64af3-105">Tulosta</span><span class="sxs-lookup"><span data-stu-id="64af3-105">Print</span></span>
* <span data-ttu-id="64af3-106">Kirjaus</span><span class="sxs-lookup"><span data-stu-id="64af3-106">Post</span></span>

<span data-ttu-id="64af3-107">Alennus ositetaan kaikkien myyntiasiakirjan rivien osalta niille nimikkeille, joilla on ostorivin **Salli laskualennus** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="64af3-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="64af3-108">Tämä on oletusasetus nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="64af3-108">This is the default setting for items.</span></span>

<span data-ttu-id="64af3-109">Ohjelma käyttää laskun alennuksen laskemiseen ehtoja, jotka on määritetty **Asiakkaan laskualennukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="64af3-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="64af3-110">Myyntiasiakirjan valuuttakoodin avulla etsitään valuutalle määritetyt laskualennusehdot.</span><span class="sxs-lookup"><span data-stu-id="64af3-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="64af3-111">Mikäli laskualennuksia ei ole määritetty ulkomaisille valuutoille, ohjelma käyttää laskualennusmäärityksiä, jotka on määritetty **Asiakkaan laskualennukset** -sivulla paikallisen valuutan summina ja myyntiasiakirjan kirjauspäivämäärän vaihtokurssia ulkomaanvaluuttamääräisen laskualennuksen laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="64af3-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
