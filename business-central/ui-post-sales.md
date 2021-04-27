---
title: Myyntiasiakirjojen kirjaaminen
description: Lisätietoja myyntiasiakirjojen kirjaamisessa käytetyistä kirjaustoiminnoista ja kirjattujen asiakirjojen päivittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e59c48c31e897d235c7920f4231313a2332fdf06
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783257"
---
# <a name="posting-sales"></a><span data-ttu-id="63fff-103">Myynnin kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="63fff-103">Posting Sales</span></span>

<span data-ttu-id="63fff-104">Kun valitset myyntiasiakirjan **Kirjaus**-valikon, voit valita seuraavista kirjaustoiminnoista:</span><span class="sxs-lookup"><span data-stu-id="63fff-104">Under the **Posting** menu in a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="63fff-105">**Kirjaa**</span><span class="sxs-lookup"><span data-stu-id="63fff-105">**Post**</span></span>
* <span data-ttu-id="63fff-106">**Kirjaus ja uusi**</span><span class="sxs-lookup"><span data-stu-id="63fff-106">**Post and New**</span></span>
* <span data-ttu-id="63fff-107">**Kirjaa ja lähetä**</span><span class="sxs-lookup"><span data-stu-id="63fff-107">**Post and Send**</span></span>
* <span data-ttu-id="63fff-108">**Esikatsele kirjausta**</span><span class="sxs-lookup"><span data-stu-id="63fff-108">**Preview Posting**</span></span>
* <span data-ttu-id="63fff-109">**Kirjaa erä**</span><span class="sxs-lookup"><span data-stu-id="63fff-109">**Post Batch**</span></span>
* <span data-ttu-id="63fff-110">**Testiraportti**</span><span class="sxs-lookup"><span data-stu-id="63fff-110">**Test Report**</span></span>

> [!NOTE]
> <span data-ttu-id="63fff-111">Myyntitilausten osalta voit tarkastella myös ennakkomaksutoimintoihin liittyviä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="63fff-111">For sales orders, you can also see options related to the prepayments functionality.</span></span> <span data-ttu-id="63fff-112">Lisätietoja on kohdassa [Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md).</span><span class="sxs-lookup"><span data-stu-id="63fff-112">For more information, see [Invoicing Prepayments](finance-invoice-prepayments.md).</span></span>

<span data-ttu-id="63fff-113">Kun olet täyttänyt kaikki rivit ja syöttänyt kaikki tiedot myyntitilaukseen, voit kirjata sen eli luoda vastaanoton ja laskun.</span><span class="sxs-lookup"><span data-stu-id="63fff-113">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="63fff-114">Tämä luo toimituksen ja laskun.</span><span class="sxs-lookup"><span data-stu-id="63fff-114">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="63fff-115">Kun myyntitilaus on kirjattu, asiakkaan tili, pääkirjanpito ja nimiketapahtumat päivitetään.</span><span class="sxs-lookup"><span data-stu-id="63fff-115">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="63fff-116">Jokaiselle myyntitilaukselle luodaan myyntitapahtuma **KP-tapahtuma**-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="63fff-116">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="63fff-117">Myös **Toimittajatapahtuma**-taulukon asiakkaan tilille luodaan tapahtuma. Lisäksi luodaan pääkirjanpidon tapahtuma asianmukaiselle myyntisaamistilille.</span><span class="sxs-lookup"><span data-stu-id="63fff-117">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="63fff-118">Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle.</span><span class="sxs-lookup"><span data-stu-id="63fff-118">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="63fff-119">Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -sivun **Alennuksen kirjaus** -kentän sisällön perusteella.</span><span class="sxs-lookup"><span data-stu-id="63fff-119">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="63fff-120">Jokaiselle myyntitilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos myyntiriveillä on nimikenumeroita) tai pääkirjanpidon tapahtuma **KP-tapahtuma**-taulukkoon (jos myyntiriveillä on pääkirjanpitotili).</span><span class="sxs-lookup"><span data-stu-id="63fff-120">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="63fff-121">Tämän lisäksi myyntitilaukset tallennetaan aina **Lähtevän toimituksen otsikko**- ja **Myyntilaskun otsikko** -taulukoihin.</span><span class="sxs-lookup"><span data-stu-id="63fff-121">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="63fff-122">Kun kirjaat tilauksen, voit luoda sekä toimituksen että laskun.</span><span class="sxs-lookup"><span data-stu-id="63fff-122">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="63fff-123">Tämä voidaan tehdä samaan aikaan tai erikseen.</span><span class="sxs-lookup"><span data-stu-id="63fff-123">These can be done at the same time or independently.</span></span> <span data-ttu-id="63fff-124">Voit luoda myös osittaisen toimituksen tai osittaisen laskun täyttämällä **Toimitettava määrä**- ja **Laskutettava määrä** -kentät yksittäisillä myyntitilausriveillä ennen kirjausta.</span><span class="sxs-lookup"><span data-stu-id="63fff-124">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="63fff-125">Huomaa, että laskua ei voi luoda jollekin, jota ei ole toimitettu.</span><span class="sxs-lookup"><span data-stu-id="63fff-125">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="63fff-126">Tämä tarkoittaa sitä, että ennen laskutusta on täytynyt tallentaa toimitus, tai täytyy valita yhtäaikainen toimitus ja laskutus.</span><span class="sxs-lookup"><span data-stu-id="63fff-126">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="63fff-127">Voit kirjata tai kirjata ja lähettää.</span><span class="sxs-lookup"><span data-stu-id="63fff-127">You can either post, or post and send.</span></span> <span data-ttu-id="63fff-128">Jos valitset kirjaamisen ja lähettämisen, ohjelma luo PDF-tiedoston, jonka voit lähettää.</span><span class="sxs-lookup"><span data-stu-id="63fff-128">If you choose to post and send, a PDF file is generated that you can then send.</span></span> <span data-ttu-id="63fff-129">**Kirjaa erä** -toiminnolla voit kirjata useita tilauksia samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="63fff-129">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span> <span data-ttu-id="63fff-130">Lisätietoja on kohdassa [Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md).</span><span class="sxs-lookup"><span data-stu-id="63fff-130">For more information, see [Post Multiple Documents at the Same Time](ui-batch-posting.md).</span></span>

## <a name="viewing-ledger-entries"></a><span data-ttu-id="63fff-131">Kirjaustapahtuminen katselu</span><span class="sxs-lookup"><span data-stu-id="63fff-131">Viewing Ledger Entries</span></span>

<span data-ttu-id="63fff-132">Kun kirjaus on päättynyt, kirjatut myyntirivit poistuvat tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="63fff-132">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="63fff-133">Viesti kertoo, milloin kirjaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="63fff-133">A message tells you when the posting is completed.</span></span> <span data-ttu-id="63fff-134">Tämän jälkeen voit nähdä kirjatut tapahtumat kirjattuja tapahtumia sisältävillä sivuilla, kuten **Asiakastapahtumat**-, **KP-tapahtumat**-, **Nimiketapahtumat**-, **Kirjatut myyntitoimitukset**- ja **Kirjatut myyntilaskut** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="63fff-134">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>  

<span data-ttu-id="63fff-135">Useimmissa tapauksissa voit avata tapahtumat kortista tai asiakirjasta, johon ne vaikuttavat.</span><span class="sxs-lookup"><span data-stu-id="63fff-135">In most cases, you can open ledger entries from the affected card or document.</span></span> <span data-ttu-id="63fff-136">Valitse esimerkiksi **Asiakaskortti**-sivulla **Tapahtumat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="63fff-136">For example, on the **Customer Card** page, choose the **Ledger Entries** action.</span></span>

## <a name="editing-ledger-entries"></a><span data-ttu-id="63fff-137">Kirjaustapahtuminen muokkaus</span><span class="sxs-lookup"><span data-stu-id="63fff-137">Editing Ledger Entries</span></span>

<span data-ttu-id="63fff-138">Voit muokata arvoja kirjattujen ostoasiakirjojen tietyissä kentissä, kuten **Paketin seurantanumerossa**</span><span class="sxs-lookup"><span data-stu-id="63fff-138">You can edit certain fields on posted purchase documents, such as the **Package Tracking No.**</span></span> <span data-ttu-id="63fff-139">-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63fff-139">field.</span></span> <span data-ttu-id="63fff-140">Lisätietoja on kohdassa [Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md).</span><span class="sxs-lookup"><span data-stu-id="63fff-140">For more information, see [Edit Posted Documents](across-edit-posted-document.md).</span></span> <span data-ttu-id="63fff-141">Jos sinulla on enemmän kriittisiä kenttiä, jotka vaikuttavat jäljitysketjuun, sinun täytyy peruuttaa tai kumota kirjaus.</span><span class="sxs-lookup"><span data-stu-id="63fff-141">For more critical fields that affect the auditing trail, you must reverse or undo posting.</span></span> <span data-ttu-id="63fff-142">Lisätietoja on kohdassa [Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="63fff-142">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="63fff-143">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="63fff-143">See Related Training at [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="63fff-144">Katso myös</span><span class="sxs-lookup"><span data-stu-id="63fff-144">See Also</span></span>

[<span data-ttu-id="63fff-145">Myynti</span><span class="sxs-lookup"><span data-stu-id="63fff-145">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="63fff-146">Useiden asiakirjojen kirjaaminen samanaikaisesti</span><span class="sxs-lookup"><span data-stu-id="63fff-146">Post Multiple Documents at the Same Time</span></span>](ui-batch-posting.md)  
[<span data-ttu-id="63fff-147">Kirjattujen asiakirjojen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="63fff-147">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="63fff-148">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="63fff-148">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="63fff-149">Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="63fff-149">Correct or Cancel Unpaid Sales Invoices</span></span>](sales-how-correct-cancel-sales-invoice.md)  
[<span data-ttu-id="63fff-150">Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla</span><span class="sxs-lookup"><span data-stu-id="63fff-150">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="63fff-151">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="63fff-151">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>

[!INCLUDE[footer-include](includes/footer-banner.md)]  
