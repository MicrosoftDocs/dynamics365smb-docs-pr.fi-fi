---
title: Ehdota toimittajamaksuja -eräajon käyttäminen| Microsoft Docs
description: Määrittämällä toimittajan maksuasetukset saat ehdotuksia maksuista, joiden eräpäivä on pian tai joissa on käytettävissä alennus.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 55bed59e65971a38469b082819d3f0d679af18d0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390147"
---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="f7b55-103">Ehdota toimittajamaksuja</span><span class="sxs-lookup"><span data-stu-id="f7b55-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="f7b55-104">Voit ehdottaa maksurivejä käyttämällä **Maksupäiväkirja**-sivulla **Ehdota toimittajamaksuja** -eräajoa.</span><span class="sxs-lookup"><span data-stu-id="f7b55-104">On the **Payment Journal** page, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="f7b55-105">Asetusten mukaan ehdotetaan rivejä, kuten pian erääntyviä maksuja tai maksuja, joissa on käytettävissä maksualennus.</span><span class="sxs-lookup"><span data-stu-id="f7b55-105">Lines for payments that are due soon or payments where a payment discount is available are suggested based on your settings.</span></span>

<span data-ttu-id="f7b55-106">Maksuehdotuksia voi hyödyntää täysimääräisesti, kun toimittajat on ensin priorisoitu.</span><span class="sxs-lookup"><span data-stu-id="f7b55-106">To benefit fully from payment suggestions, you must first prioritize your vendors.</span></span> <span data-ttu-id="f7b55-107">Lisätietoja on kohdassa [Toimittajien priorisoiminen](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="f7b55-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="f7b55-108">Toimittajatapahtumia, jotka on merkitty **Estossa**-merkinnällä, ei sisällytetä eräajoon.</span><span class="sxs-lookup"><span data-stu-id="f7b55-108">Vendor ledger entries that are **On Hold** are not included in the batch job.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="f7b55-109">Jos haluat käyttää maksualennuksia ja olet antanut käytettävissä olevan summan, summaa käytetään</span><span class="sxs-lookup"><span data-stu-id="f7b55-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  
    * <span data-ttu-id="f7b55-110">priorisoiduissa erääntyvissä toimittajatapahtumissa tärkeysjärjestyksessä</span><span class="sxs-lookup"><span data-stu-id="f7b55-110">Prioritized overdue vendor entries first in order of priority.</span></span>   
    * <span data-ttu-id="f7b55-111">erääntyneissä toimittajatapahtumissa, joita ei ole priorisoitu</span><span class="sxs-lookup"><span data-stu-id="f7b55-111">Overdue vendor entries that are not prioritized.</span></span>  
    * <span data-ttu-id="f7b55-112">avoimissa toimittajatapahtumissa, joissa voi käyttää maksualennuksia, toimittajanumeron mukaan järjestettynä.</span><span class="sxs-lookup"><span data-stu-id="f7b55-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="f7b55-113">Ehdota toimittajamaksuja -toiminnon käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f7b55-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="f7b55-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f7b55-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f7b55-115">Avaa asianmukainen päiväkirja ja valitse **Ehdota toimittajamaksuja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f7b55-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="f7b55-116">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="f7b55-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="f7b55-117">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="f7b55-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="f7b55-118">Eräpäivän lisääminen maksupäiväkirjan rivien kirjauspäivämääräksi</span><span class="sxs-lookup"><span data-stu-id="f7b55-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="f7b55-119">Kun **Ehdota toimittajamaksuja** -eräajoa käytetään toimittajien maksurivien luomisessa, täyttämällä kaksi erikoiskenttää voi varmistaa, että luodut rivit käyttävät eräpäivää kirjauspäivämäärän laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="f7b55-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="f7b55-120">Nämä kentät ovat **Laske kirjauspäivämäärä kohdistuksen asiakirjan eräpäivästä** ja **Kohdistuksen asiakirjan eräpäivän siirtymä**.</span><span class="sxs-lookup"><span data-stu-id="f7b55-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="f7b55-121">Et voi käyttää **Laske kirjauspäivämäärä kohdistuksen asiakirjan eräpäivästä** -kenttää yhdessä **Hae maksualennukset**- tai **Tee yhteenveto toimittajittain** -kentän kanssa.</span><span class="sxs-lookup"><span data-stu-id="f7b55-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="f7b55-122">Jos kirjauspäivä perustuu eräpäivään, joitain maksualennuksia ei ehkä ole laskettu oikein, koska kirjauspäivä on maksualennuspäivän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f7b55-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="f7b55-123">Jos laskettu kirjauspäivämäärä on myös menneisyydessä, kirjauspäivämäärää siirretään käsittelypäivämäärään ja näyttöön tulee varoitus.</span><span class="sxs-lookup"><span data-stu-id="f7b55-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="f7b55-124">Vaihtoehtoisesti voit luoda maksurivejä manuaalisesti niin, että eräpäivää käytetään kirjauspäivämäärän laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="f7b55-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="f7b55-125">Kun kohdistat toimittajatapahtumia, voit päivittää päiväkirjan rivin kirjauspäivän liittyvän ostolaskun eräpäivällä käyttämällä **Laske kirjauspäivämäärä** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="f7b55-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="f7b55-126">Lisätietoja on kohdassa [Ostotapahtumien kohdistaminen manuaalisesti](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="f7b55-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="f7b55-127">Jos ostolasku on myöhässä, kirjauspäivämäärä määritetään käsittelypäivämääräksi ja rivin fontti muuttuu punaiseksi.</span><span class="sxs-lookup"><span data-stu-id="f7b55-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7b55-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f7b55-128">See Also</span></span>
[<span data-ttu-id="f7b55-129">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="f7b55-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="f7b55-130">Maksujen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="f7b55-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="f7b55-131">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f7b55-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="f7b55-132">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7b55-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]