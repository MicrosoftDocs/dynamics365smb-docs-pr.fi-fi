---
title: Ostovelkojen hallinta| Microsoft Docs
description: "Yleiskatsaus tavoista, joilla Financials auttaa hallitsemaan ostovelkoja, kuten toimittajamaksuja, lainoja, velkaa ja erääntyvää saldoa."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-financials
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 654c34bc09967247617bda7be070a9c0ec6f635d
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="managing-payables"></a><span data-ttu-id="96bd4-103">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="96bd4-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="96bd4-104"> sisältää kaiken, mitä tarvitset ostoreskontran tehokkaaseen hallintaan.</span><span class="sxs-lookup"><span data-stu-id="96bd4-104"> has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="96bd4-105">Maksut</span><span class="sxs-lookup"><span data-stu-id="96bd4-105">Payments</span></span>
<span data-ttu-id="96bd4-106">Sen avulla on helppo priorisoida maksut, ottaa huomioon erääntymismaksut ja käsitelle aikaisin suoritettujen maksujen alennukset.</span><span class="sxs-lookup"><span data-stu-id="96bd4-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="96bd4-107">Voit kirjata maksut yleiseen päiväkirjaan ja tulostaa sitten sekit ennen maksupäiväkirjan kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="96bd4-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="96bd4-108">Voit kohdistaa maksut sulkemaan laskut maksun kirjaamisen yhteydessä tai kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="96bd4-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="96bd4-109">Toimittajalle (**toimittajakortissa**) määritetty **Kohdistustapa** määrittää, kohdistetaanko maksu manuaalisesti vai automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="96bd4-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="96bd4-110">Voit aina kohdistaa tapahtumia manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="96bd4-110">You can always apply transactions manually.</span></span> <span data-ttu-id="96bd4-111">Jos toimittajan kohdistustapa on **Kohdista vanhimpaan** etkä määritä asiakirjaa, johon maksu kohdistetaan, maksu kohdistetaan toimittajan vanhimpaan avoinna olevaan tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="96bd4-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="96bd4-112">Ehdota toimittajamaksuja</span><span class="sxs-lookup"><span data-stu-id="96bd4-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="96bd4-113"> voi ehdottaa eri maksuja toimittajille, kuten maksuja, jotka erääntyvät pian, ja maksuja, joista voi saada alennuksen.</span><span class="sxs-lookup"><span data-stu-id="96bd4-113"> can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="96bd4-114">Maksuehdotus voi ottaa huomioon summan, jonka määrität saatavilla olevina varoina maksuihin, ja kelpoisuuden maksualennuksiin.</span><span class="sxs-lookup"><span data-stu-id="96bd4-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="96bd4-115">Sekkien myöntäminen</span><span class="sxs-lookup"><span data-stu-id="96bd4-115">Issue Checks</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="96bd4-116">issa sekit voi myöntää toimittajille manuaalisesti ja sähköisesti.</span><span class="sxs-lookup"><span data-stu-id="96bd4-116"> lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="96bd4-117">Kumpikin tehdään **Maksupäiväkirjat**-ikkunassa, jossa voit myös mitätöidä sekkejä ja tarkastella sekkitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="96bd4-117">You do both in the **Payment Journals** window, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="96bd4-118">Maksujen vienti pankkitiedostoon</span><span class="sxs-lookup"><span data-stu-id="96bd4-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="96bd4-119">Kun olet valmis maksamaan toimittajille, voit viedä tiedoston päiväkirjan riveiltä **Maksupäiväkirja**-ikkunassa maksutietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="96bd4-119">When you are ready to pay a vendor, from the **Payment Journal** window you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="96bd4-120">Voit sitten ladata tiedoston verkkopankkiin rahansiirtojen käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="96bd4-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="96bd4-121">Jos et halua kirjata viedyn maksun maksupäiväkirjan riviä, koska odotat esimerkiksi pankin vahvistavan tapahtuman, voit poistaa päiväkirjan rivin.</span><span class="sxs-lookup"><span data-stu-id="96bd4-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="96bd4-122">Kun luot myöhemmin maksupäiväkirjan rivin, jolla maksetaan jäljellä oleva laskun summa, **Viety summa yhteensä** -kenttä näyttää, kuinka paljon maksun summasta on jo viety.</span><span class="sxs-lookup"><span data-stu-id="96bd4-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="96bd4-123">Saat lisätietoja viedystä kokonaissummasta valitsemalla **Hyvityksen siirron rekisterimerkinnät** -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="96bd4-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="96bd4-124">Jos odotat maksujen kirjaamista, kunnes pankki vahvistaa tapahtumien käsittelyn, voit estää avoimien asiakirjojen maksujen uudelleenviennin vahingossa kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="96bd4-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidently re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="96bd4-125">Voit lajitella maksupäiväkirjan ehdotettujen maksurivien kohdalla joko **Viety maksutiedostoon**- tai **Viety summa yhteensä** -sarakkeen mukaan ja sitten poistaa maksuehdotukset avoimilta laskuilta, jotka on jo maksettu ja joita et halua maksaa.</span><span class="sxs-lookup"><span data-stu-id="96bd4-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="96bd4-126">**Huomautus** Olet ehkä lisännyt nämä sarakkeet luetteloon.</span><span class="sxs-lookup"><span data-stu-id="96bd4-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="96bd4-127">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="96bd4-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="96bd4-128">Vaihtoehtoisesti voit määrittää **Ehdota toimittajamaksuja** -eräajossa, jossa määrität maksupäiväkirjaan sisällytettävät maksut, että vietyjen maksujen päiväkirjarivejä ei lisätä valitsemalla **Ohita viedyt maksut** -valintaruudun.</span><span class="sxs-lookup"><span data-stu-id="96bd4-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="96bd4-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="96bd4-129">See Also</span></span>
[<span data-ttu-id="96bd4-130">Maksutavat</span><span class="sxs-lookup"><span data-stu-id="96bd4-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="96bd4-131">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="96bd4-131">Finance</span></span>](finance.md)  
<span data-ttu-id="96bd4-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="96bd4-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

